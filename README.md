# Finanzas

Scaffold mínimo de una app Android nativa en Kotlin y Jetpack Compose, basado en la estructura Empty Activity de la guía oficial. Creado manualmente; no generado por el asistente de Android Studio.

Una Activity, una pantalla vacía, Material 3, tema claro/oscuro y vista previa de Compose. Paquete provisional: `com.example.finanzas`. Android mínimo: 6.0 (API 23). Compile/target SDK: 36.

## Abrir y ejecutar

1. Abrir Android Studio y elegir **Open** → esta carpeta.
2. Esperar la sincronización de Gradle. La primera vez necesita Internet para descargar las dependencias.
3. En **Settings → Build, Execution, Deployment → Build Tools → Gradle**, usar el Gradle Wrapper del proyecto y un Gradle JDK 17 o el JDK integrado compatible de Android Studio.
4. Seleccionar un teléfono con depuración USB habilitada o un emulador desde Device Manager.
5. Pulsar **Run ▶**. La app debe mostrar una pantalla vacía.

Desde una terminal normal en esta carpeta:

```sh
./gradlew assembleDebug
./gradlew lintDebug
```

El APK se genera en `app/build/outputs/apk/debug/app-debug.apk`.

## Archivos principales

- `app/src/main/java/com/example/finanzas/MainActivity.kt`: entrada y pantalla vacía.
- `app/src/main/java/com/example/finanzas/ui/theme/Theme.kt`: tema de Compose.
- `app/src/main/AndroidManifest.xml`: declaración de la app y Activity de inicio.
- `app/build.gradle.kts`: configuración del módulo Android.
- `gradle/libs.versions.toml`: versiones y dependencias.
- `local.properties`: ruta local del SDK; excluida de Git.

AGP 9.0.1 incorpora Kotlin 2.2.10; el plugin de Compose utiliza esa misma versión. Gradle Wrapper 9.3.1. Dependencias estables fijadas, sin versiones dinámicas. No hace falta instalar Kotlin ni Gradle globalmente.

## Revisión del entorno — 4 de octubre de 2026

| Componente | Detectado |
| --- | --- |
| Equipo | MacBook Pro, Apple M1, 8 GB de RAM |
| macOS | 26.6.2, ARM64 |
| Espacio libre | Aproximadamente 53 GiB |
| Android Studio | Instalado, versión del bundle 2025.3 |
| Java | Temurin OpenJDK 17.0.20.1 ARM64 |
| Android SDK | `~/Library/Android/sdk`, plataforma API 36 |
| Build Tools | 35.0.0, 36.0.0 y 36.1.0 |
| Herramientas | adb, sdkmanager y emulator en PATH |
| Dispositivos virtuales | Pixel 9 API 36 y Medium Phone API 36.1, ARM64 |
| Gradle | Distribución 9.3.1 disponible localmente |

No se detectaron herramientas básicas faltantes. La documentación oficial pide 8 GB para Android Studio y 16 GB para Studio junto con el emulador en macOS. Con este equipo se recomienda comenzar usando un teléfono físico y mantener pocas aplicaciones abiertas. Hay emuladores configurados, pero no se verificó su arranque ni la conexión de un teléfono.

## Estado de validación

Revisados XML, catálogo TOML, scripts y contenido del Wrapper. No se ha confirmado la compilación ni la ejecución de la app: el entorno restringido de esta sesión impide crear los sockets internos de Gradle (`SocketException: Operation not permitted`) y resolver los servidores de descarga. Ejecutar los comandos anteriores desde una terminal normal o sincronizar desde Android Studio para completar la validación.

## Documentación oficial

- [Crear tu primera app con Empty Activity](https://developer.android.com/codelabs/basic-android-kotlin-compose-first-app)
- [Configurar Jetpack Compose](https://developer.android.com/develop/ui/compose/setup)
- [Requisitos de Android Studio](https://developer.android.com/studio/install)
- [Compatibilidad de AGP 9.0 y Kotlin integrado](https://developer.android.com/build/releases/agp-9-0-0-release-notes)
- [Versiones de Compose con BOM](https://developer.android.com/develop/ui/compose/bom)
