Especificación de requerimientos de software para la aplicación de Uber.

Tabla de contenidos.
Introducción.   
Propósito.  
Convenciones del documento. 
Audiencia objetivo y sugerencias de lectura.    
Alcance del proyecto.   
Referencias.    
Descripción general.    
Perspectiva del producto.   
Características del producto.   
Clases y características del usuario.   
Ambiente de operación.  
Restricciones de diseño e implementación.   
Documentación para el usuario.  
Suposiciones y dependencias.    
Características del sistema.    
Requerimientos de la interfaz externa.  
Interfaces de usuario.  
Interfaces del hardware.    
Interfaces del Software.    
Requerimientos no funcionales.  
Requerimientos de desempeño.    
Requerimientos de seguridad.    
Atributos de calidad del software.  

 
Introducción.

Propósito.
El propósito del documento es analizar, aplicando el método de ingeniería inversa, la aplicación conocida como Uber, logrando obtener una descripción general de sus funciones, las características del sistema y los requerimientos tanto funcionales como no funcionales, con el fin de comprender los componentes de ingeniería de software que participan detrás de la aplicación.
Convenciones del documento.
Convención / Término    Descripción
MAYÚSCULAS  Acrónimos, abreviaciones.
Negritas    Menús y comandos de menú, botones de comandos, nombre de requerimientos y características.
Cursiva Referencia a otros documentos y citas textuales.
Nota:   Notas dentro del documento.
Audiencia objetivo y sugerencias de lectura.
Este documento va dirigido a los integrantes, compañeros y profesor del equipo E de la materia arquitectura de sistemas del grupo 801 de la licenciatura Ingeniería en Tecnología y Soluciones de Negocio de la universidad La Salle bajío.
Las sugerencias de lectura son:
"   Manual UML, Paul Kimmel.
"   Ingeniería de software, Séptima edición, Sommerville Ian.
Alcance del proyecto.
Se centrará en Uber cómo producto comercial y no en su calidad de empresa.
Se realizará un análisis de ingeniería inversa sin acceso a información privilegiada, patentada o protegida de la aplicación Uber, llegando a abarcar las características que se pueden encontrar hasta el día de hoy en el mercado de dicho software sin extenderse más allá de las características y funcionalidades evidentes que operan en la ciudad de León.
Referencias.
https://www.uber.com/
https://play.google.com/store/apps/details?id=com.ubercab&hl=es

 
Descripción general.
Perspectiva del producto.
Uber es una aplicación móvil que permite la conexión de pasajeros con los conductores registrados dentro de su sistema, los cuáles ofrecen servicio de transporte personalizado a los particulares que han solicitado el viaje.
Según las propias palabras de la empresa: "La app de Uber encuentra un conductor cerca de ti para que te lleve adondequiera que vayas."
Características del producto.
Uber cuenta con una móvil para clientes y otra para conductores, llamadas Uber y Uber Driver respectivamente; detrás de ellos, cuentan con un sistema que permite la geolocalización de dichas partes y ubicación visual para clientes y conductores en tiempo real de su geolocalización; algoritmos inteligentes de cálculo de distancias entre usuario y conductor, algoritmos para el trazo de rutas óptimas y cálculo de tarifas dinámicas y cálculo de tarifas en la realización de los viajes; sistemas de cobro de tarifas mediante tarjetas de débito, crédito, paypal o en efectivo; y un sistema de ranking con historial para usuarios y conductores así como un pequeño centro de ayuda para dar soporte técnico y comercial a las mismos en casos de controversia.
Clases y características del usuario.
Existen dos grandes clasificaciones dentro de la aplicación: Conductores y Usuarios.
"   Conductores: Son quiénes ofrecen el servicio de transporte a los Usuarios, ellos son los encargados de registrarse dentro de la aplicación Uber Driver y cumplir con los requisitos para que el registro sea correcto, deben cumplir con requerimientos legales, condiciones y características del automóvil y cumplir con los estándares de atención que la empresa Uber exige.
"   Usuarios: Son quiénes demandan el servicio de parte de los conductores, ellos interactúan mediante la aplicación Uber y deben registrar algún método de pago, cumplir con las políticas y reglamento de la empresa.
Nota: Si bien existen categorías dentro de los conductores como Uber Pool o Conductores de lujo, no se toman en cuenta ya que en la ciudad de león no se ha implementado el sistema y por lo tanto, se sale del alcance del proyecto.
Ambiente de operación.
La operación de parte de los usuarios finales del sistema se centra en las aplicaciones de Uber y Uber Driver, desde dónde se obtienen los datos necesarios para la conexión entre los usuarios y conductores, una vez conectados, el usuario obtiene información relevante del conductor al cuál fue enlazado y viceversa, pudiendo en cualquier momento cancelar el viaje de parte de las partes, posteriormente se procede a la realización del viaje y del cobro del mismo.
En la parte trasera o back-end de la aplicación es seguro asumir (ya que no tenemos acceso directo a esa información) que se cuenta con un sistema de base de datos centralizado pero con sedes en diferentes países con respaldo de información, servidores que permiten el consumo de los servicios y algoritmos que hacen funcionar a la aplicación y finalmente los programas y sistemas de software que le dan vida a los algoritmos inteligentes utilizados para el enlace y realización de los viajes.
Restricciones de diseño e implementación.
Uber tiene como motor principal, y quizá único, para la interacción con los usuarios finales dos aplicaciones móviles, lo cuál limita el uso de dicho servicio a través de software basado en web, de escritorio y software para otros tipos de dispositivos no-móviles. Esto nos lleva a dos restricciones principales:
"   Diseño basado en app móvil sin posibilidad de migrar a una plataforma web o de escritorio sin sufrir modificaciones o cambios.
"   Obsolescencia por parte de los dispositivos móviles antiguos sin soporte a los nuevos sistemas operativos del mercado en los cuáles Uber se desempeña.
Otra restricción muy importante para el uso del servicio es la conexión a Internet continua que deben tener tanto los conductores como los usuarios, pues mediante esta conexión se gestiona el levantamiento del viaje por parte del usuario, elección del cliente por parte del conductor, geolocalización de las dos partes mencionadas anteriormente y el cobro del cálculo de tarifa por viaje.
Documentación para el usuario.
Como tal, existe documentos legales disponibles para el usuario dentro del "https://www.uber.com/es-MX/ride/how-uber-works/" que pone a disposición los materiales legales necesarios.
Suposiciones y dependencias.
Uber debe trabajar amparado a las leyes de transporte vigentes en la ciudad así como los reglamentos y leyes aplicables a las sociedades empresariales de personas morales establecidos en el marco constitucional de los Estados Unidos Mexicanos.
Uber trabaja como sin dependencia y de forma independiente a cualquier órgano de ésta índole.
Nota: Las suposiciones y dependencias están centradas en la funcionalidad de Uber en Léon, Guanajuato, México.
Características del sistema.
Aplicación Uber: Es una aplicación móvil que se encuentra como una de las dos principales características del lado de usuario del sistema de Uber, en ella, se encuentran embebidas las demás características, que se mencionarán a continuación, y es la plataforma principal para que los usuarios puedan lograr conectarse a los viajes que ellos requieres. Esta característica cuanta con versiones para Android y iOS y se puede encontrar en la Play Store y Apple Store respectivamente..
Aplicación Uber Driver: Es una aplicación móvil que compagina con la aplicación Uber como las principales características del lado de usuario del sistema de Uber, en ella, los conductores que previamente ya fueron dados de alta, se conectan y son enlazados con los potenciales clientes y cuentan con características embebidas de geolocalización, ranking, perfil de conductor entre otras que a continuación se mencionan.
Sistema de geolocalización: Uber cuenta con un sistema de geolocalización que utiliza como plantilla de mapa a Google Maps, mediante este sistema, se hace el enlace entre el conductor y sus clientes, el cálculo de tarifas, historial de recorridos y visualización en tiempo real de la posición actual de los conductores y clientes que son consumidos por los dos tipos de usuario en sus respectivas aplicaciones.
Sistema de conexión cliente-conductor: Uber cuenta con algoritmos inteligentes que permiten enlazar a los usuarios y a los conductores de manera eficaz y óptima, buscando a los conductores más cercanos a los usuarios que levantan una solicitud de viaje.
Algoritmos de rutas: Se utiliza un algoritmo que permite detectar las rutas óptimas para la realización del viaje de la manera mas eficiente posible, para los usuarios se ve reflejado en un camino a seguir dentro de la aplicación que se comparte para el conductor y el cliente e n sus respectivas aplicaciones móviles.
Cálculo de tarifas: Se utilizan algoritmos para el cálculo de las tarifas probables, antes de que el usuario acepte el viaje, y reales, una vez que se realizó el viaje. Dentro de este algoritmo, se incluye las infames tarifas dinámicas, aquellas tarifas que aumentan el costo base de los viajes en base a una valoración de la oferta y la demanda que existe entre usuarios y conductores.
Medios de pago y de cobro: Se cuenta con una plataforma que se apoya de otras APIs para realizar el cobro de los usuarios y el pago a los conductores Uber que permite diferentes métodos de pago que son: Tarjeta de crédito, tarjeta de débito, PayPal y efectivo. Dentro de estos medios de pago existen descuentos que se obtienen de cupones y ofertas que el usuario haya introducido previamente a la aplicación y se aplican automáticamente a los viajes.
Ranking de usuarios: Las aplicaciones de Uber muestran información como nombre, foto, calificación de los usuarios y en adición para los conductores, sus placas, comentarios y viajes realizados. Esta información se muestra a las dos partes para que puedan conocer de antemano quién será su acompañante durante el viaje que se realizará y puedan cambiar de opinión si algo no les parece. El sistema de rankeo se basa principalmente en calificaciones que se dan los usuarios y conductores respectivamente al concluir un viaje, en base a la calidad de la compañía del acompañante en ese momento; este sistema permite filtrar a los individuos que tienen comportamientos no deseados y excluirlos de la aplicación.
Requerimientos de la interfaz externa.
Interfaces de usuario.

ID  Requerimiento   Descripción (breve)
1   ABC de Usuarios Deberá permitir ABC de la información de usuarios y conductores de las aplicaciones Uber y Uber Driver.
2   Visualización del mapa con conductores  Del lado del cliente, debe ser posible la visualización de los conductores cercanos a la zona dónde éste está ubicado.
3   Petición de viajes  Permitir que el usuario pueda elegir los puntos de inicio y término de un viaje y que se cotice el viaje y aproximado del tiempo de recorrido.
4   Puntuación del Usuario  Permitirá visualizar una puntuación propia en un ranking de 1.00 a 5.00 y de los conductores o usuarios para el viaje pedido según sea el caso.
5   Método de pago  Permitirá al usuario elegir un método de pago y modificarlo según sean sus necesidades.
6   Historial de viajes Permitir al usuario visualizar un historial de los viajes que ha realizado, con su fecha y hora, modelo del conductor o nombre del usuario (según sea el caso), cantidad del pago efectuado y la puntuación dada.
7   Ayuda de último viaje   Se le dará la opción al usuario final de reportar algún problema con su último viaje, permitiéndole elegir dentro de mensajes predeterminados cuál fue su problema, mientras se visualizan los detalles del viaje.
8   Mensajes de soporte El usuario podrá enviar mensajes con algún problema diferente para recibir soporte de la mesa de ayuda de Uber.
9   Viajes gratis y descuentos  Se podrá ingresar un código que permita obtener descuentos a los usuarios en sus próximos viajes e incluso obtener viajes gratis que se aplicarán automáticamente en el próximo viaje que éste realice.
10  Cálculo de tarifa   El usuario podrá visualizar el costo aproximado de la tarifa por el viaje antes de aceptar.
11  Tarifa de viaje El usuario podrá visualizar el costo real del viaje una vez éste se haya realizado.
12  Calificación de usuarios    Permitirá a los usuarios y conductores calificar a sus contrapartes por viaje de 1 a 5 estrellas.
13  Cancelación de viajes   Permitirá a los usuarios y conductores cancelar el viaje si así lo requiere

Interfaces del hardware.
ID  Requerimiento   Descripción (breve)
14  Posición GPS    Permitirá a los usuarios utilizar los sistemas del dispositivo móvil en cuestión de Geolocalización.
15  Conexión a Internet Permitirá a los usuarios conectar su viaje a Internet mediante el dispositivo.

Interfaces del Software.
ID  Requerimiento   Descripción (breve)
17  Tarifa dinámica Permitirá hacer un cálculo para activar o desactivar la tarifa dinámica para los usuarios por geolocalización.
18  Conexión a mesa de ayuda    El software distribuirá los mensajes de ayuda de los usuarios a la mesa de ayuda y gestionará su comunicación y solución.
19  Bloqueo de usuarios El sistema deberá bloquear a los usuarios automáticamente cuando alcancen cierta cantidad de calificaciones negativas.

Requerimientos no funcionales.
Requerimientos de desempeño.
ID  Requerimiento   Descripción (breve)
20  Alta disponibilidad El software deberá contar con un sistema de alta disponibilidad.
21  Respaldo de la información  El software deberá tener respaldo de las bases de datos.
22  Actualización de plataforma El sistema deberá siempre funcionar en los sistemas operativos mas nuevos del mercado, especialmente para Android y iOS
Requerimientos de seguridad.
ID  Requerimiento   Descripción (breve)
23  Seguir las leyes de privacidad de manejo de información.    El sistema deberá obedecer las leyes y normas para el manejo y privacidad de la información dentro del marco legal de la constitución de los Estados Unidos Mexicanos.
24  Rastreo de inseguridad  El sistema deberá atender y procesar las quejas de los conductores asaltados y crear zonas donde el servicio no se brindara por causas de privacidad 
Atributos de calidad del software.
Los atributos más importantes para poder medir la calidad del software y el sistema completo de Uber se enlistarán a continuación:
"   Tiempo entre enlace de conductor - usuario: Se medirá el tiempo de respuesta del sistema para lograr el enlace entre las dos partes para iniciar el viaje.
"   Disponibilidad de la plataforma: Se buscará mantener la plataforma disponible durante todo el tiempo que sea posible.
"   Calificación promedio de usuarios y conductores: Se monitoreará la calificación promedio de los usuarios para encontrar cuál es la satisfacción promedio que los usuarios tienen al interactuar entre sí dentro del sistema.
"   Tiempo de respuesta de la mesa de ayuda: Se medirá el tiempo de respuesta que se tiene al ingresar una queja al sistema.
"   Satisfacción en la resolución de quejas en la mesa de ayuda: Se medirá las reacciones y porcentaje de resolución de quejas en la mesa de ayuda.
