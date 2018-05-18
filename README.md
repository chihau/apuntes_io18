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
