# Proyecto Integrador – Introducción al Desarrollo de Nuevas Plataformas

## Descripción

Este proyecto corresponde al **Proyecto Integrador Final** del curso **Introducción al Desarrollo de Nuevas Plataformas**. La aplicación fue desarrollada utilizando **Kotlin** y **Jetpack Compose**, incorporando progresivamente las tecnologías estudiadas durante las tres unidades del curso.

La aplicación permite gestionar tareas mediante una interfaz moderna basada en **Material Design 3**, almacenando la información de forma permanente con **Room Database**, guardando las preferencias del usuario mediante **Jetpack DataStore** y ejecutando tareas automáticas en segundo plano con **WorkManager**. Además, implementa un sistema de notificaciones y se encuentra preparada para su publicación en **Google Play Store** mediante un archivo **Android App Bundle (AAB)** firmado.

---

# Evolución del proyecto

## Unidad 1 – Desarrollo inicial de la aplicación

Durante la primera unidad se desarrolló la estructura principal de la aplicación utilizando **Jetpack Compose**. Se implementó la navegación entre pantallas, formularios de ingreso de información, componentes básicos de Material Design y la administración del estado mediante `remember` y `rememberSaveable`.

### Funcionalidades implementadas

- Navegación entre pantallas mediante Navigation Compose.
- Pantalla de inicio de sesión.
- Panel principal.
- Pantalla de perfil.
- Componentes Material Design 3.
- Formularios con validaciones básicas.
- Gestión temporal del estado.
- Diseño adaptable mediante Compose.

---

## Unidad 2 – Interfaces avanzadas y arquitectura MVVM

En la segunda unidad la aplicación evolucionó incorporando una arquitectura basada en **MVVM**, separando la lógica de negocio de la interfaz de usuario.

Se implementó un tema personalizado con Material Design 3, soporte para modo claro y oscuro, listas dinámicas utilizando **LazyColumn**, filtros mediante **LazyRow**, gráficos realizados con **Canvas** y administración del estado mediante **ViewModel** y **StateFlow**.

### Funcionalidades implementadas

- Tema personalizado Material Design 3.
- Cambio automático entre modo claro y oscuro.
- Arquitectura MVVM.
- ViewModel independiente para cada pantalla.
- StateFlow y collectAsState().
- LazyColumn con elementos dinámicos.
- LazyRow para categorías.
- Búsqueda mediante TextField.
- SwipeToDismiss con opción Deshacer.
- Snackbar de confirmación.
- FloatingActionButton.
- Gráficos desarrollados con Canvas.
- Animaciones utilizando animateFloatAsState().

---

## Unidad 3 – Persistencia, procesos en segundo plano y publicación

En la tercera unidad la aplicación se convirtió en una solución completamente funcional mediante la incorporación de persistencia local, preferencias permanentes, tareas automáticas y preparación para su distribución.

La información de las tareas ahora se almacena utilizando **Room Database**, lo que permite conservar los datos aun después de cerrar la aplicación. Asimismo, las preferencias del usuario se gestionan mediante **Jetpack DataStore**, mientras que **WorkManager** ejecuta tareas programadas en segundo plano para generar recordatorios mediante notificaciones.

Finalmente, el proyecto fue preparado para su publicación en Google Play mediante la generación de un archivo **Android App Bundle (AAB)** firmado con un **Keystore** propio.

### Funcionalidades implementadas

- Persistencia de datos con Room Database.
- Entidad Tarea utilizando @Entity.
- Clave primaria autogenerada.
- DAO con operaciones CRUD.
- Repository como intermediario.
- Base de datos Room.
- Datos persistentes entre sesiones.
- Configuración mediante Jetpack DataStore.
- Preferencias almacenadas permanentemente.
- Aplicación automática del modo oscuro.
- WorkManager para tareas periódicas.
- ReminderWorker ejecutado en segundo plano.
- Constraints para controlar la ejecución del Worker.
- Canal de notificaciones.
- Compatibilidad con Android 13 mediante POST_NOTIFICATIONS.
- PendingIntent para regresar a la aplicación.
- Generación del archivo Android App Bundle (.aab).
- Firma digital mediante Keystore.
- Recursos preparados para Google Play Store.

---

# Arquitectura del proyecto

El proyecto utiliza el patrón **MVVM (Model – View – ViewModel)** para separar las responsabilidades de cada componente.

Además, WorkManager ejecuta procesos en segundo plano y NotificationHelper administra el sistema de notificaciones.

Usuario
│
▼
UI (Jetpack Compose)
│
▼
ViewModel
│
▼
Repository
│
▼
Room Database
│
▼
DAO
---

# Tecnologías utilizadas

- Kotlin
- Jetpack Compose
- Material Design 3
- Navigation Compose
- ViewModel
- StateFlow
- Room Database
- DAO
- Repository
- Jetpack DataStore
- WorkManager
- NotificationChannel
- PendingIntent
- Android App Bundle (AAB)

---

# Estructura del proyecto

---
com.aroldo.proyectointegrador
│
├── data
│ ├── dao
│ ├── database
│ ├── model
│ └── repository
│
├── datastore
│
├── notification
│
├── ui
│ ├── components
│ ├── navigation
│ ├── screens
│ ├── theme
│ └── viewmodel
│
├── worker
│
└── MainActivity.kt
---

# Funcionalidades principales

- Inicio de sesión.
- Panel principal.
- Perfil de usuario.
- Gestión de tareas.
- Agregar tareas.
- Eliminar tareas.
- Restaurar tareas.
- Buscar tareas.
- Filtrar por categoría.
- Estadísticas mediante Canvas.
- Tema claro y oscuro.
- Persistencia con Room Database.
- Configuración mediante DataStore.
- Recordatorios automáticos.
- Notificaciones.
- Preparación para Google Play.

---

# Requisitos

- Android Studio Hedgehog o superior.
- Kotlin 2.0.
- Android SDK 34 o superior.
- Gradle 8.x.
- Dispositivo o emulador Android 8.0 o superior.

---

# Ejecución

1. Clonar el repositorio.
2. Abrir el proyecto en Android Studio.
3. Sincronizar Gradle.
4. Ejecutar la aplicación en un dispositivo físico o emulador.
5. Conceder el permiso de notificaciones (Android 13+).

---

# Estado del proyecto

Proyecto Integrador Finalizado version 1.0.0.

La aplicación integra los contenidos desarrollados durante las tres unidades del curso, incorporando una arquitectura basada en MVVM, persistencia mediante Room Database, almacenamiento de preferencias con DataStore, tareas automáticas mediante WorkManager, sistema de notificaciones y preparación para su distribución en Google Play Store.

---

# Autor

**Aroldo Guillermo Muñoz Romani**

Curso: Introducción al Desarrollo de Nuevas Plataformas(E)

Escuela Profesional: Ing. Sistemas

Universidad Nacional de San Agustin
