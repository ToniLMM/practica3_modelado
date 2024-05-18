# Modelado: Práctica 3

## Parte A: Configuración

#### Objetivo:
Configurar correctamente el modelo de robot utilizado en la práctica para poder ser visualizado, operado y controlado usando el software disponible en ROS2.

## Parte B: Integración y estudio de dinámicas en Gazebo y ROS2

#### Objetivo:
Realizar la simulación en dos entornos de gazebo diferentes usando el robot realizado en la práctica 2 para estudiar el comportamiento del robot y su modelo de colisión en mundos distintos.

## Sand world

#### Rosbag del sand.world:
https://drive.google.com/drive/folders/19ltdUlZhe13wtP1IQmvR35gh_axI9uMn?usp=drive_link

[Screencast from 18-05-24 18:59:51.webm](https://github.com/ToniLMM/practica3_modelado/assets/92941378/a25b9e17-093f-48ce-953c-2fb1f03efd4e)

#### Velocidades de las ruedas publicadas en joint_states:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/0a63a7a0-e23f-4c3d-87a8-4d7854824d51)

#### Desplazamientos que el controlador cree hacer publicados en odom:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/98436ab2-dd3b-42c5-98e4-fd3bdce67a3d)

#### Aceleraciones ejercidas por el robot:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/bf4d74b1-b1e4-4452-bb9c-c422a69fad29)

#### Gráfica completa:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/b43e4ef0-8f85-4ba5-8349-aa7ff8f008c9)

Como podemos observar en la gráfica la velocidad del robot sube progresivamente, sin embargo se pueden ver oscilaciones en la velocidad de las ruedas debido al choque con los cubos, primero en las ruedas delanteras (1 y 3) y luego en las traseras (2 y 4). En cuanto al terreno (arena) por lo general tenemos un aumento de velocidad progresivo y lineal (exceptuando las oscilaciones del choque), sin embargo se puede notar que poco antes de llegar a los 5 segundos ejerce una subida más exponencial de lo antes visto, esto puede deberse a que en el tramo anterior las ruedas pudieran estar patinando con la arena. Por otro lado una vez alcanza los 5 y segundos hasta que se para podemos observar una gráfica más lineal y continua sin prácticamente fluctuaciones. Por último en la gráfica de aceleración se puede ver claramente el momento donde se produce el choque debido a los picos que muestra la grafica, tanto en el choque con las ruedas delanteras como en el choque con las ruedas traseras.


## Floor world

#### Rosbag del floor.world: 
https://drive.google.com/drive/folders/12R3op05AShdLLPu4jZoUTirK41hx1nAT?usp=drive_link

[Screencast from 18-05-24 19:07:23.webm](https://github.com/ToniLMM/practica3_modelado/assets/92941378/660247c3-7653-4ea0-b90e-0da51eab2b74)

#### Velocidades de las ruedas publicadas en joint_states:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/87348575-8920-4b59-8999-48e89fb86ab0)

#### Desplazamientos que el controlador cree hacer publicados en odom:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/9ce5bb19-ca4c-4bbe-873c-ead3785a29e7)

#### Aceleraciones ejercidas por el robot:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/7aa6806e-43f4-4a39-a0f6-b2b64db5edc8)

#### Gráfica completa:
![image](https://github.com/ToniLMM/practica3_modelado/assets/92941378/f0f83930-1ec1-4637-be88-28db93db04e8)

En este caso como en el anterior vemos como la velocidad de las ruedas aumenta progresivamente, además se pueden ver oscilaciones debido al choque como en el caso anterior, sin embargo hay que destacar las oscilaciones de las ruedas traseras, en especial la rueda 4 (trasera derecha) ya que cuando las de delante chocan y el coche se eleva esta sufre un fuerte golpe causando dicha fluctuacion. En cuanto al terreno (suelo) podemos ver más vibraciones que en el caso anterior debido a las irregularidades y pequeños baches que presenta este mapa. Por último en la gráfica de aceleración se puede ver claramente el momento donde se produce el choque debido a los picos que muestra la grafica, tanto en el choque con las ruedas delanteras como en el choque con las ruedas traseras.



