# Automatizador para decodificador Totalplay (Versión Simple)

## Programa para eliminar el modo reposo del decodificador Totalplay usando la placa Arduino Nano y señales IR

La empresa de Totalplay a inicios de año 2025, sacó una actualización para su decodificador la cual activa el modo reposo después de 6 horas si no detecta actividad alguna, lo cual elimina la reproducción de lo que estaba mostrando.
Esto no es una opción que se puede cambiar en el dispositivo y tampoco algo que se puede solicitar. Para un usuario normal esto no es un gran problema, pero si eres parte de un negocio o empresa que usa este servicio para mostrarlo 24/7, tendrías que estar activando manualmente cada ciertas horas.
Este programa automatiza el envío de señales infrarrojas, las mismas enviadas por el control remoto, para simular actividad hacia el decodificador.

# Hardware Utilizado
- Arduino Nano
- Push buttons
- Led ir333-a
- Resistencia 100 Ω (220 Ω si no se utilizara Transistor)
- Transistor 2N2222
- 4 Leds
- 4 Resistencias con resistencia correspondiente al led a utilizar 

# Características
- Un botón para el envío manual de la señal.
- Muestra el porcentaje de tiempo restante para el envío de la siguiente señal con 4 led (Ej. 100%: 4 leds prendidos, 25%: 1 led prendido).

# Instalación y Uso
Clona el proyecto y abrelo en el entorno de Arduino.  
Librerías requeridas:
- [IRremote](https://github.com/Arduino-IRremote/Arduino-IRremote)   

Se pueden cambiar las configuración del programa en el archivo "config.h". Las cuales son:
- Pines para los componentes.
- Tiempo entre para cada envío.
 
El ejemplo del diagrama eléctrico se encuentra en "imagenes/diagrama.PNG". Es recomendable conectar el led IR al transistor y no directamente al GPIO, esto para tener una mayor corriente e iluminación. Si deseas conectarlo al GPIO, usa una resistencia de 220 Ω.   
Una vez que se tenga corriendo apropiadamente, es conveniente dejarlo enfrente del decodificador o en un lugar donde el receptor pueda leer las señales del LED.   

Existe una version mas robusta implementando una pantalla es este repositorio: [Automatizador_Totalplay_TV](https://github.com/Cota-820/Automatizador_Totalplay_TV)

"Este proyecto no está afiliado a Totalplay. Úsalo bajo tu propia responsabilidad”.
