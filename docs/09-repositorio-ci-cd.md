# 9. Repositorio, Git y CI/CD

## Git vs. Plastic (Unity Version Control) — decisión

Se evaluó cambiar de Git a Plastic SCM (ahora "Unity Version Control", de Unity) y se decidió **quedarse con Git + GitHub**.

| | Git + GitHub | Plastic / Unity Version Control |
|---|---|---|
| Archivos binarios grandes | Bien con Git LFS para esta escala | Nativo, sin configurar nada extra |
| Merge de escenas/prefabs de Unity | Conflictos reales si dos tocan la misma escena | Merge semántico, mejor para eso |
| CI gratis y documentado | GameCI + GitHub Actions, muchos tutoriales | CI propio, mucha menos documentación para proyectos chicos |
| Curva de aprendizaje | Ya la tiene el equipo (repo ya armado) | Aprender una herramienta nueva desde cero |
| Costo | Gratis (repo público) o de sobra en plan gratuito | Gratis hasta cierto número de usuarios |

**Motivo de la decisión:** cambiar de sistema de control de versiones a 7 semanas de la entrega es justo el tipo de riesgo innecesario que hay que evitar. La ventaja real de Plastic (merge de escenas) se cubre con una regla de equipo más barata: **las escenas compartidas se tocan una a la vez, se avisa en el chat del equipo antes de editarlas**.

Si en algún punto el problema real es que alguien sin experiencia en terminal (ej. el equipo de arte) batalla con Git, la solución recomendada no es cambiar de VCS sino usar una interfaz gráfica como **GitHub Desktop** sobre el mismo repositorio.

## Git LFS

El proyecto va a manejar modelos 3D, texturas y audio — es necesario activar **Git LFS** para esos tipos de archivo (`git lfs track "*.fbx" "*.png" "*.wav"`, etc.) para que el repositorio no se vuelva pesado y lento.

## CI: comprobar que cada commit compila (GitHub Actions + GameCI)

Es posible y es el estándar en proyectos de Unity, usando las Actions de **GameCI** (`game-ci/unity-builder` y `game-ci/unity-test-runner`).

| Opción | Qué hace | Duración | Cuándo usarla |
|---|---|---|---|
| **Test Runner (ligera)** | Corre Unity en modo batch y ejecuta los tests EditMode — para correrlos, Unity tiene que compilar todo el proyecto primero, así que un error de compilación hace fallar el paso | ~2–5 min | Recomendada en cada push |
| **Build completo (Unity Builder)** | Genera un build real (Windows/WebGL/etc.) | 10–25+ min | Antes de un hito (vertical slice, alpha, RC), no en cada commit |

### Ejemplo de workflow (`.github/workflows/unity-ci.yml`)

```yaml
name: Unity CI

on:
  push:
    branches: ["**"]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          lfs: true

      - uses: actions/cache@v4
        with:
          path: Library
          key: Library-${{ hashFiles('Assets/**', 'Packages/**', 'ProjectSettings/**') }}
          restore-keys: Library-

      - name: Correr tests (fuerza la compilacion)
        uses: game-ci/unity-test-runner@v4
        env:
          UNITY_LICENSE: ${{ secrets.UNITY_LICENSE }}
        with:
          githubToken: ${{ secrets.GITHUB_TOKEN }}
          testMode: EditMode
```

### El único obstáculo real: la licencia de Unity

Unity necesita una licencia activada para correr en modo batch en la nube. Con Unity Personal (gratis) hay que generar un archivo de licencia una sola vez:

1. Correr Unity en modo batch localmente para pedir el archivo de activación.
2. Subirlo a la web de Unity para activarlo.
3. Guardar el `.ulf` resultante como secreto `UNITY_LICENSE` en GitHub.

GameCI tiene una guía paso a paso para esto. Es un trámite de 20–30 minutos que se hace una sola vez.

**Alternativa si la activación en la nube da problemas:** correr un "self-hosted runner" en la PC de alguien del equipo que ya tenga Unity activado localmente. Evita el problema de licencias, pero esa PC debe estar prendida cuando corra el CI, y si el repo es público hay que tener cuidado con quién puede disparar el workflow (deshabilitar Actions en PRs de forks externos).

## Pendiente de implementar

- [ ] Agregar `.github/workflows/unity-ci.yml` al repositorio.
- [ ] Generar y guardar el secreto `UNITY_LICENSE`.
- [ ] Activar Git LFS y trackear extensiones de archivos binarios.
- [ ] Asignado a G. González (arquitectura del proyecto, Fase 1) con apoyo de Dylan.
