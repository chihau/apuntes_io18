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

### Connection
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
