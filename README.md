# Tablero Hospitalario — aplicación de escritorio

Aplicación de escritorio basada en el HTML del tablero. Está preparada para generar instaladores de Windows y macOS mediante Electron y GitHub Actions.

## Requisitos para ejecutar localmente

- Node.js 22 o superior
- npm

```bash
npm install
npm start
```

## Crear instaladores en tu computadora

```bash
npm run dist
```

Los archivos generados estarán en `dist/`.

## Generar instaladores desde GitHub

1. Sube el contenido de este proyecto a un repositorio de GitHub.
2. En la pestaña **Actions**, habilita los workflows si GitHub lo solicita.
3. Ejecuta **Build desktop installers** manualmente, o publica un tag que empiece por `v`, por ejemplo `v1.0.0`.
4. Abre la ejecución del workflow y descarga los artefactos `installers-windows` y `installers-macos`.
5. Para distribuir públicamente, crea un **GitHub Release** y adjunta los instaladores descargados.

## Datos y privacidad

Los registros se guardan en el almacenamiento local de la aplicación en ese equipo. No se sincronizan entre computadoras. Como el tablero puede contener datos de pacientes, mantén el repositorio sin datos reales y privado si incluye información interna. Usa contraseñas de equipo, permisos y copias de seguridad de acuerdo con las políticas del hospital.

## Reloj y clima

El reloj usa la hora local del sistema y funciona sin internet. El clima necesita conexión para actualizarse; sin conexión solo se puede mostrar el último dato guardado, no una temperatura en tiempo real.

## Limitaciones de distribución

Los instaladores no están firmados con certificados de desarrollador. macOS o Windows pueden mostrar avisos de seguridad. Para una distribución institucional amplia, conviene configurar firma de código y notarización de macOS.
