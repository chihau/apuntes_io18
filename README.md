# Mis Apuntes del Google I/O 18

## What’s new with Android TV

- Más de 100 partners, SmartTVs, STB, Pay TV operators
- 3600+ apps and games
- Soporta Assistent, interfaz natural usando la voz, permite estar concentrado en el contenido. Este año será soportado en más países
- Nueva experiencia en el Android TV, una fila para apps preferidas, una fila para recomendaciones de contenido
- El asistente funcionará desde Android M+
- Google Play Movies permite comprar contenido
- Video Preview
- Progress indicator para ver hasta dónde viste el contenido específico
- Se puede programar un Channel para poder ofrecer mi contenido a través de un content provider
- Nuevo Intent INITIALIZE_PROGRAMS para poner contenido en el HOME?
- “Play Big Bug Bunny” para reproducir la película
-  onPause “Hey Google, Pause the Movie”, onSeekTo() “Hey Google, rewind 30 seconds” onSkipToNext() “Hey Google, Play next song”
- Buenas prácticas, Agregar la mayormetadata posible, mostrar previews de videos, mantener contenido actualizado, MediaSession es tu amigo
- JBL Link Bar, una barra-speaker con Android TV que se conecta a la TV vía HDMI, con Assistent, se lanzará a finales de 2018. Soporta varios dispositivos conectados vía HDMI al mismo tiempo, por ejemplo **podemos ver información de un videojuego mientras estamos jugando al video juego**
- ADT-2 Developer Device a finales del verano

### Lo nuevo que tendrá la versión con Android P
- Se enfocarán en Performance sobre todo en dispositivos menos potentes, isLowRamDevice(), Android Vitals, Android Studio Memory Profiler
- Setup más sencillo, se puede hacer sign-in desde el teléfono iOS, Android o web
- Play Auto Installs, te sugiera que apps instalar en base a instalación antigua
- Autofill with Google, autocompleta passwords
- Configuraciones Sugeridas
- Soporte para Cámaras

[https://android-developers.googleblog.com/2017/10/video-playback-with-google-assistant-on.html](https://android-developers.googleblog.com/2017/10/video-playback-with-google-assistant-on.html)

## What’s new in Wear OS by Google

- Ya son 4 años desde que se lanzó
- 50 relojes disponibles actualmente
- 1 de 3 usuarios usan un teléfono iOS, esa es la razón porque se cambió el nombre de Android Wear a Wear OS by Google
- En focado en 3 áreas: Connection, Health and Fitness, Google Assistant
- Nueva Companion App para iOS
- Mejoras en la optimización de la batería
- 11 lanzamientos desde junio 2017 y 49 nuevas funciones agregadas
- App Compat con mejoras para Wear OS g.co/dev/appcompat
- Un reloj tiene un 10% de la batería de un celular
- Mejoras en el consumo de la batería en Android P, Jobs and Alarms que sólo pueden funcionar cuando están en Foreground, saver mode para relojes, Dark UI System theme de #232E33 a #000000
- Como consejo juntar las network request y sensor request para mejorar el consumo de la batería
- Ahora soporta Kotlin, SDL
- Se vienen más actualizaciones durante el año

### Connection
- Podemos utilizar el reloj sin necesidad de tener el teléfono a mano
- Adaptive Text Sizing
- Darker background
- Complications
- Notification Complication
- Recently Launch App Complication

### Health and Fitness
- Trackear de mejor manera nuestra actividad
- Touch lock para bloquear en encendido de la pantalla al tocarla, se desactiva con el botón
- Music
- Continua lectura de Heart rate

### Assistant
- Always present microphone?
- Text to Speech, se puede escuchar una respuesta en un parlante bluetooth conectado al celular
- Sugerencias para la conversación
- La mayoría de las funciones de Google Assistant funcionan en Wear OS
- Vocal responses?

## Android fireside chat

- Android aún soporta tablets, pero se está apostando por incentivar ChromeOS, además las apps Android se pueden correr en ChromeOS
- Seguirán invirtiendo esfuerzos en soporta Java y C++
- 28 de las 100 tops apps usan kotlin, el 35% de los devs usan kotlin
- La versión P beta AOSP es visualmente distinta a la Pixel

## The future of computing: a conversation with John Hennesy

- En los últimos años no se está logrando cumplir la ley de Moore
- Mientras más chicos son los procesadores más están consumiendo energía, por lo que este último se está volviendo el factor límite
- La Eficiencia Energética es la nueva métrica
- Google Assistant por ejemplo necesita que el CPU está funcionando todo el tiempo
- En datacenter el costo de los servidores es casi el mismo que el de la energía necesaria para hacerlos funcionar
- En los últimos años el rendimiento de los procesadores ha crecido casi nada (3% por año)
- Domain Specific Architectures (DSA), HW específico para hacer cierta tarea
- Google Duplex en el ámbito de la reserva de una cita pasó el test de Turing
- El gobierno de USA ha sido pieza clave para la innovación, por ejemplo la inteligencia artificial la ha desarrollado durante más de 50 años

## What’s new in Android

- Android App Bundles
- Android JetPack: un conjunto de bibliotecas para ayudarte a desarrollar aplicaciones Android
- Todas las bibliotecas tipo android.support.v\*.\* ahora serán llamadas androidx.\*
- Android Test ahora soporta clases Kotlin, reduce el boilerplate code y mejora la lectura del código
- JetPack Architecture: Lifecycles, ViewModel, Room, LiveData
- WorkManager es una alternativa nueva a JobSchedule
- Batería: App Standby Buckets, Background restrictions
- Background Input & privacy, ya no se puede acceder al micrófono, cámara y otros sensores en background, antiguamente las apps maliciosas intentaban mantenerse en memoria reproducción un leve sonido o escuchando a través del micrófono
- Kotlin: muchas mejoras de rendimiento, ART, D8 & R8, support library y libcore, mejoras en nullability anotation, android-ktx
- Nuevo framework para hacer Mocks
- Desplegar texto en la UI es una de las tareas más “caras” y se puede convertir en un problema de rendimiento
- El 80 o 90% de las operaciones que se realizan en el UI Thread para desplegar texto ocurren en el Text Measurement, se puede hacer un precómputo utilizando la Text API que utilizar un Thread independiente para hacer el trabajo. PrecomputedText.create()
- Un magnificador del texto para ayudar a la selección de texto
- Smart Linkify
- Nuevo paquete android.net.wifi.rtt.\* WiFi Round-Trip-Time APIs para posicionamiento indoor de tu dispositivo, no se necesita estar conectado al API, se necesita HW compatible
- Mejoras en Accesibilidad
- Seguridad: BiometricDialog unificado, FingerprintManager obsoleto, Build.SERIAL ya no se usa
- Enterprise: Ahora se puede hacer un switch entre perfil personal y trabajo para mostrar las apps por separado
- Mejoras en el modo Kiosk
- Soporte para Display Cutout, para soportar los “notch” (o multiples nothes)
- Slices: es una nueva forma de desplegar contenido que pertenece a otra app, es contenido estructurado y con templates flexibles, interactivo, actualizable, y soporta content URI y se puede implementar desde kitkat con la Support Library
- Actions: son Intents visibles a través de un botón (chips) se definen las acciones en actions.xml, se puede registrar en App Indexing para que aparezcan en los resultados de las búsquedas.
- Notificaciones: mejoras en la forma de mostrar los mensajes, soporta Smart Reply UI
- Desde Agosto 2018, las apps que se publiquen en Google Play deberán tener el Target API en 26
- Desde Noviembre 2018, las actualizaciones que se publiquen en Google Play deben tener el Target API en 26
- Desde Agosto de 2019, Si tienes apps con NDK, requerirán que soporte 64-bit ABI (32-bit será opcional)
- NDK, versión r17, soporta Neural Networks API, JNI Shared Memory API, elimina soporte para ARMv5, MIPS y MIPS64 y otras cosas nuevas…, la versión r18 eliminará GCC, soporte para simpleperf profiler
- Cámara: soporte para cámaras USB, soportará multiples cámaras
- ImageDecoder: reemplazo del BitmapFactory
- Media: soporte para HDR VP9, HDR rendering para HW compatible, soporte para formato HEIF
- Vulkan 1.1, low level graphics API
- Neural Networks API 1.1, C API diseñada para ML
- ARCore, soporta AR desde el Emulator (genera una escena Virtual)
- Sceneform: Herramienta para hacer rendering del escenario utilizado para ARCore
- ChromeOS: puedes correr Android Studio y apps Linux

## Customize Material Components for your product

- Material Design se lanzó el año 2014
- Ganadores de Material Design Awards: NYTimes 2015, Airbnb 2016, Blinkist 2017
- Material Theme Editor herramienta para utilizar en conjunto con Sketch
- Material Palete Generator para crear mi paleta de color
- Permite seleccionar la tipografía
- Nuevos íconos
- Gallery a una herramienta para trabajar un diseño en conjunto con otros diseñadores
- Crane es una travel app de ejemplo
- MDC son bibliotecas open source para implementar material design en Android, iOS, Flutter y Web
- Reply app de correo de ejemplo para Android
- Nueva Bottom App Bar (la barra superior de acciones pasa para abajo)
- Chips
- Tipografía nueva Work Sans
- Shrine es una app de compras de ejemplo
- Una app debería tener al menos 3 capas, la navegación debería ser a través de tabs

## Building Material Design Across Platforms

- Material es un sistema de diseño adaptable, respaldado por código open source, que ayuda a los equipos a desarrollar de forma sencilla experiencias digitales de alta calidad
- En 2014 había 0 apps con MD, ahora hay 1.5 millones de apps
- Nuevo sitio Materio.io, dividido en 3 secciones: Design, Develop y Tools
- Material Components, bibliotecas opensource para diseñadores y desarrolladores
- Es un framework multiplataforma, Android, iOS, Web y Flutter
- Un objetivo es desarrollar productos de calidad en corto tiempo
- Un desarrollador sin grandes conocimientos en diseño podría implementar MD
- La sección Design: System, Foundation, Guidelines
- fonts.google.com sitio complementario para las fuentes
- Material Palette generator para implementar la paleta de colores que tendrá mi app
- Tools: Gallery para compartir diseños con mi equipo, Icons, Color Tool, Material Theme Editor es un plugin para Sketch

### Material Theme Editor

- io18_lib.sketch
- Motions, Colors, Layers and Shapes
- Utiliza la fuente Google Sans
- gallery.io para diseño colaborativo con el equipo

### Material Components

- También lo utiliza Google en sus propias apps
- En Android viene con Android Design Support Library
- En Web se instala un módulo node a través de npm
- En Flutter viene incluído por defecto
- En iOS se incluye en CocoPods

## Code beautiful UI with Flutter and Material Design

- Flutter es la forma de desarrollar aplicaciones nativas para Android y iOS
- Se caracteriza por la forma rápida de iterar
- Soporta Material Design de forma nativa
- Shrine es una app retail de ejemplo
- El gran problema de las apps con MD v1 es que se parecen mucho una de otra
- MD 2 es mucho más expresivo ya que es más customizable
- MD 2 esta mejorado ya que contiene nuevos componentes y estilos
- MD 2 facilita el desarrollo ya que proporciona herramientas y componentes
- En Flutter todo es un Widget
- Lo primero que hay que tomar en cuenta para empezar a desarrollar mi app es: Font, logo, shape, layout y Color
- copyWith() es un método que se usa mucho en los Widgets de Flutter, permite copiar una nueva instancia pero asignarle valores distintos a los parámetros
- Todos los Widgets tiene un método build()
- Backdrop es esencialmente una pila, tiene un front panel y un back panel
- AnimationController es una clase open source encargada de administrar todas las animaciones
- En esta demo se utiliza Android Studio con el plugin de Flutter instalado
- Gesture Detectors como onTap, onDrag, onLongPress para detectar gestos que se hacen con los dedos
- Flutter Inspector nos permite inspeccionar los widgets que componen la interfaz, al parecer sólo está disponible para Android Studio y IntelliJ IDE
- Las pantallas rojas de error que tiene flutter sólo se mostrarán en la parte que contiene el problema, eso nos permite hacernos una idea de dónde está el problema

## Build the new, modular Android App Bundle

- El formato es un archivo ZIP
- Es un formato para publicar, no puede ser instalado directamente en el dispositivo, contiene archivos metadata que nos permitirán archivos APK, es más estricto que el de un APK.
- Los directorios raíces de un AAB son los módulos de la aplicación
- resources.pb es el equivalente al resources.arc que se puede encontrar en la mayoría de los APK, que describe los recursos presentes en tu app y su objetivo, la extensión .pb es del formato protocol buffer que permite convertir en formato binario antes de generar el APK
- assets.pb y native.pb son los equivalentes a los assets y native libraries
- File targeting: Los archivos correctos para los usuarios/dispositvos correctos, es el principal concepto de Google Play Dynamic Delivery.
- Permite reducir el tamaño de tus APK
- Ahora soporta Assets Targeting
- Ej: assets/strings#lang_fr/dictionary.pb que contiene texto para dispositivos en frances
- Google Play servirá sólo lo necesario en el APK por ejemplo para un Samsung Galaxy J5 en Inglés -> xhdpi, arm, en
- Esto funcionará desde Lollipop en adelante
- Los APK serán 20% más pequeños, es decir te vas a ahorrar un 20% de descarga cada vez que la app tenga que actualizarse
- Se puede probar en AS 3.2 Canary
- La herramienta generará un archivo llamado bundle.aab (No un APK) firmado y listo para publicar, luego Google Play genera los APK automáticamente
- Para publicar en Google Play hay que subir nuestra Release Key para firmar los APK generados
- Bundle Explorer me permite verificar los APK que se van a generar, cuanto se va a ahorrar en espacio, a los dispositivos que va a llegar, etc.
- Publishing API soporta AAB
- Para testear mi app puedo instalar un APK generado con AAB directamente desde AS
- También podemos utilizar canales alpha y beta, además de un track interno de 100 testers máximo
- bundletool para probar los APK generados de forma local desde la línea de comandos directamente a los dispositivos conectados
- bundletool es la misma herramienta que utiliza AS para generar un archivo .aab, es open source github.com/google/bundletool
- Para reducir más espacio aún se puede modularizar la app, quitando las funcionalidades que menos se utilizan utilizando Dynamic Module
- Se tiene que declarar en el AndroidManifest.xml y en el build.gradle
- Play Core Library para comunicarse con Google Play Service para descargar el Dynamic Module utilizando IPC
- Para descargar módulos muy grandes, el usuario tendrá que aceptar un aviso
