# Módulo 1: Garantía de seguridad de la información

Para entender qué es exactamente seguridad, hay adentrarnos hacia su centro gravitacional: **La tríada CIA.**

Entonces, *¿Qué es la tríada CIA?*

La tríada CIA, es una sigla que esta compuesta por las inciales de 3 términos que simplifican el entendimiento sobre que es Seguridad.

Estos términos son: **Confidencialidad, Integridad y Disponibilidad.**

## Confidencialidad:
Se relaciona con permitir el acceso autorizado a la información y, al mismo tiempo, proteger la información de una divulgación indebida.

## La integridad:
Es la propiedad de la información mediante la cual se registra, usa y mantiene de manera que se asegure su integridad, precisión, consistencia interna y utilidad para un propósito establecido.

## Disponibilidad:
Significa que los sistemas y los datos son accesibles en el momento en que los usuarios los necesitan.

👉 Partiendo de esta base, todo el aprendizaje a continuación siempre va a relacionarse con estos 3 conceptos importantísimos.

### Principales amenazas para la confidencialidad:

- **Snooping:** persona que se dedica a fisgonear o chismear que informacion puede recopilar. Las organizaciones pueden protegerse contra el espionaje aplicando una politica de escritorio limpio.

- **Dumpster diving:** cuando el atacante busca en el contenedor de basura documentos desechados. La organizacion puede protegerse contra este tipo de ataque implementando una politica que destruya los documentos usando una trituradora de papel.

- **eavesdropping:** Pueden ser de escucha físicas o electronicas. En el caso de las fisicas es cuando tienes una conversacion delicada en un area donde exista el riesgo de que personas puedan oir tu conversacion, una organizacion puede protegerse aplicando politicas donde estas conversaciones sucedan en sala de reuniones o conferencias. La electronica es cuando un atacante obtiene acceso a una red y monitorea los datos que viajan en ella, de un dispositivo a otro. La manera correcta de protegerse contra esto es aplicando cifrado en transito.

- **wiretapping:** conocido como chuponeo. Tambien es un ataque de escucha electronica.

- **social engineer:** el atacante usa trucos psicologicos para persuadir a un empelado a que le de informacion confidencial o acceso a sistemas internos

Es muy dificil protegerse contra los ataques de ingenieria social, la mejor defensa contra estos ataques es educar a los usuarios para que reconozcan los peligros de la ingenieria social y capacitarlos para intervenir cada vez que sospechen que se esta produciendo un ataque.

### Principales amenazas para la integridad:

- **Unauthorized modification:** se produce cuando un atacante obtiene acceso a un sistema y realiza cambios que violan una politica de seguridad, este atacante puede ser un atacante externo que irrumpe un sistema financiero y se emite cheques, o un atacante interno que acceso al sistema de nominas y se aumenta su propio salario. Seguir el principio del privilegio minimo es una forma de protegerse contra ataques de integridad. Que significa el POLP: que la organizacion considere cuidadosamente los permisos que da empleado necesita para realizar su trabajo y a continuacion limitar a los empleados al conjunto mas pequeño de permisos posible.

- **Impersonation attack:** en un ataque de suplantacion, el atacante pretende hacerse pasar por un gerente, ejecutivo, etc para ganar acceso elevado de alguna manera. (si se dan cuenta se relaciona con el ataque de ingenieria social).

- **Man-in-the-middle (MITM):** es una forma de suplantacion pero electronica, porque intercepta el mensaje de un usuario hacia un sistema en la red, y luego pretende ser ese usuario, haciendole creer al sistema que puede responder con total confianza y luego se hace pasar por el sistema y le envia el mensaje recepcionado al usuario, de esa manera logra monitorear toda la conversacion entre ambos. Por ejemplo, podria robar la contraseña del usuarios para iniciar sesion en el sistema mas adelante.

- **Replay attack:** Los ataques de repeticion, a diferencia del MITM, solo tiene que encontrar la manera de observar a que un usuario legitimo inicie sesion en un sistema para luego acceder ellos mismos.

### Principales amenazas para la disponibilidad:

- **Denial of Services (DoS):** Sucede cuando una persona malitencionada envia una cantidad abrumadora de tráfico al servidor con la finalidad de que no pueda responder solicitudes de usuarios legitimos. Se puede proteger haciendo uso de un firewall.

- **Power outages:** Nos podemos defender con tener fuentes de poder redundantes y generadores.

- **Hardware failures:** Nos podemos proteger con componentes redundantes, haciendo que el sistema se mantenga activo con un nuevo hardware cuando cae el principal.

- **Destrution:** Desastes naturales por ejemplo

- **Services outages:** Puede deberse a errores de programacion, la falla del host subyacente o muchas otras razones, lo que genera que se interrumpa el acceso de los usuarios al sistema y la informacion. Podemos protegernos mediante la construccion de estrategias de conmutacion por error o Failover.

## No repudio

El no repudio es un término legal y se define como la protección contra un individuo que niega falsamente haber realizado una acción en particular. Brinda la capacidad de determinar si una persona determinada realizó una acción en particular, como crear información, aprobar información o enviar o recibir un mensaje.

## Privacidad de los datos

Como profesionales de TI, tenemos intereses en como las organizaciones recoplilan y utilizan la informacion personal. 

- **Proteger nuestros propios datos.** Quiero entender quien tiene informacion sobre mi y que estan haciendo con ella.

- Educar a los usuarios de nuestras organizaciones sobre como pueden proteger su propia informacion personal

- **Proteger los datos recopilados por las organizaciones.** Tenemos la responsabilidad de ayudar a los funcionarios de privacidad dentro de nuestra organizacion con el trabajo que deben hacer para proteger la informacion personal que se nos confia.

👉 La informacion privada puede venir en muchas formas. Dos de los elementos mas comunes son: la informacion de identificacion personal (PII) y la informacion de salud protegida (PHI).

## Autenticación

Cuando los usuarios han declarado su identidad, es necesario validar que son los legítimos propietarios de esa identidad. Este proceso de verificación o prueba de la identificación del usuario se conoce como autenticación. En pocas palabras, la autenticación es un proceso para probar la identidad del solicitante.

Hay tres métodos comunes de autenticación:

- Algo que sabes: Contraseñas o paráfrasis
- Algo que tiene: Tokens, tarjetas de memoria, tarjetas inteligentes
- Algo que eres: biometría, características medibles

### Métodos de autenticación

Hay dos tipos de autenticación. Usar solo uno de los métodos de autenticación mencionados anteriormente se conoce como autenticación de un solo factor (SFA). Otorgar acceso a los usuarios solo después de demostrar o mostrar con éxito dos o más de estos métodos se conoce como autenticación multifactor (MFA).

La mejor práctica común es implementar al menos dos de las tres técnicas comunes para la autenticación:

- Basado en el conocimiento
- basado en token
- basado en características

Adicional a esto, los sistemas de control de acceso tambien proporcionan la funcionalidad de “contabilidad” (Accounting), que permite a los administradores realizar un seguimiento de la actividad del usuario y reconstruir esas actividad a partir de registros. 

Cualquier seguimiento que se realice como parte del programa de monitoreo de una organizacion debe ajustarse a los limites establecidos por la ley y la politica de privacidad de la organizacion.

En conjunto las actividades de autenticacion, autorizacion y contabilidad se les conoce como triple AAA.
