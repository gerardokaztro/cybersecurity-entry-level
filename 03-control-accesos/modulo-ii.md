# Módulo 2: Control de acceso lógico

## Account Monitoring o monitoreo de cuentas
Se requiere prestar mucha atencion a los permisos y al uso de las cuentas de usuario final para protegerse contra incidentes de seguridad

### Buenas practicas de monitoreo de cuentas que las organizaciones debe implementar:

Inaccurate permissions o Permisos inexactos:
- son permisos que se asignan a las cuentas e impiden que un usuarios haga su trabajo o violan el principio minimo privilegio.
- Una manera facil de caer es cuando el empleado cambio de rol en el trabajo y se le añaden nuevos permisos pero nunca se revocan los antiguos
- Una manera de protegerse es realizar auditorias periodicas de cuentas de usuarios en cooperacion con los administradores

Auditores de cuentas de usuarios: 
- Deben obtener una lista de todos los permisos
- Revisar los permisos en conjunto con los administradores
- Hacer los ajustes necesarios

Algunas organizaciones usan un proceso de certificacion formal en el que los auditores revisan la documentacion para asegurarse de que los administradores hayan aprobado formalmente la cuenta y los permisos de acceso a cada usuario.

Otro problema es el uso no autorizado de permisos, ya sea por alguen no legitimo que hace uso de la cuenta o por el usuario legitimo que realiza alguna accion ilegitima. La proteccion contra el uso no autorizado de permisos es complicada porque puede ser dificil de detectar.

Se requiere el uso de sistemas de monitoreo continuo de cuentas que:
- vigilan la actividad sosprechosa
- y alertan a los  administradores sobre acciones extrañas

Por ejemplo un sistema de monitoreo continuo de cuentas puede alertas sobre violaciones de las politicas de acceso como:
- Inicio de sesion desde ubicaciones geograficas extrañas
- Inicio de sesion desde ubicaciones de red inusuales
- Inicio de sesion en horarios inusuales
- Desviaciones las transferencias de volumenes de datos
- Detecta cualquier otro tipo de comportamiento anormal

A medida que continue mejorando sus mejores practicas de monitoreo es posible que desee agregar informacion adicional, util y relevante para implementar politicas de seguridad en las cuentas de usuario. 

Ejemplo:
- **Geotagging o Geo-etiquetado** registra informacion geografica al registro de inicio de sesion.
- **Geofencing** dibuja cuadros de limites alrededor de ubicaciones geograficas y notifica/alerta cuando un dispositivo abandona un limite definido.

## Provisionamiento y desaprovisionamiento

Un administrador de usuarios tiene dos funciones basicas a realizar:
- Provisionamiento: cuando un nuevo empleado ingresa a la empresa, tiene que dar de alta a su usuarios, y compartirles las credenciales de autenticacion y otorgar el permiso apropiado en funcion a su rol dentro de la empresa.
- Desaprovisionamiento: Durante el proceso de baja del empleado, los administradores de cuenta debe deshabilitar la cuenta de usuario y revocar los permisos en el tiempo y forma.

### Prompt termination is critical o la Pronta Terminación es Crítica
- Cuando un empleado abandona la organizacion es crucial actuar rapidamente para eliminar su acceso de los sistemas informaticos
- Previene que los usuarios que dejaron a la organizacion sigan accediendo a los sistemas e informacion.

### Routine Workflow

Se debe tener un proceso solido, diseñado para eliminar el acceso, preferiblemente de manera automatizada o semiautomatizada. Esta rutina de flujo de trabajo debe iniciar cuando un supervisor informa al area de people sobre la inminente salida de un trabajador. El administrador de cuentas debe configurar la cuenta del usuario para que caduque automaticamente en la fecha que abandone la organizacion.

### Emergency Workflow

Este es un flujo de trabajo usado para emergencias, por ejemplo cuando un empleado es separado de la organizacion inesperadamente. Es importante que haya una perfecta sincronizacion entre el area de recursos humanos y el departamente de TI para suspender la cuenta del usuario en el tiempo justo en que se le notifica la separacion de la organizacion.

### Revocacion de cuentas en tiempos incorrectos

Si un administrador de cuenta no cronometra bien el momento exacto para suspender una cuenta pueden ocurrir dos cosas:
- Si la cuenta se cancela antes de que el empleado sea notificado, éste puede tomar medidas de represalia contra el empleador
- Si la cuenta se cancela despues de avisar al empleado de su separación, este aun podria acceder a los sistemas y tomar medidas de represalia.

## Autorizacion:

Es le paso final del proceso de control de acceso.
La authZ (autorización) determina lo que un usuario authN (autenticación) puede hacer

**POLP:** el principio de minimo privilegio dice que un usuario debe tener el conjunto de permisos minimos para realizar sus funciones laborales.

Aplicar POLP es bueno por 2 razones:
- Reduce el daño potencial de un ataque interno
- Limita al ataque externo de alguien que comprometio la cuenta de un empleado

Existen varios enfoques diferentes al momento de diseñar un sistema de control de acceso:

**Mandatory Access Control (MAC):** El propio sistema operativo restringe los permisos que se puden otirgar a los usuarios y procesos sobre los recursos del sistema. Los propios usuarios no pueden modificar ningun permiso. Raramente se implementa en producion. MAC normalmente se implementa como un sistema de control de acceso basado en reglas donde los usuarios y recursos tienen etiquetas y el sistema operativo toma desiciones control de acceso comparando esas etiquetas.

**Discretionary Access Control (DAC):** Permite un enfoque mas flexible de autorizacion. Permite a los usuarios asignar permisos de acceso a otros usuarios. Los propietarios del sistema, archivos, recursos tiene. la discrecion de configurar los permisos como mejor les parezca. Al ser un sistema de autorizacion flexible es adoptado por muchas organizaciones, tener en cuenta que no se requiere ser del departamento de TI, basta con que seas el owner del archivo o recurso para poder asignar permisos sobre el a otros usuarios.

**Role-based Access Control (RBAC):** Simplifica enormemente la administracion de autorizaciones. En lugar de administrar permisos para cada usuario individual, los administradores crean roles basados en trabajos y asignan permisos a esos roles. Luego pueden asignar usuarios a los roles en funcion de sus trabajos. 

En lugar de intentar administrar todos los permisos para cada usuario individual, los administradores crean roles basados en trabajos y, a continuación, asignan permisos a esos roles. A continuación, pueden asignar usuarios a los roles en función de sus trabajos. Ahora esto podría ser un poco más de trabajo por adelantado, pero hace la vida mucho más fácil en el futuro. Cuando un nuevo usuario llega a la organización, el administrador no necesita averiguar todos los permisos individuales que requiere ese usuario. Simplemente asignan al usuario al rol o roles apropiados, y todos los permisos seguirán. Del mismo modo, cuando un grupo de usuarios necesita un nuevo permiso, el administrador no necesita aplicar ese permiso a cada usuario individual. En su lugar, pueden aplicar el permiso al rol y todos los usuarios con ese rol recibirán el permiso automáticamente. Ahora, cuando estamos diseñando un sistema de control de acceso, necesitamos seleccionar el enfoque que mejor equilibre los requisitos de seguridad y las necesidades comerciales en nuestra organización. Si elegimos un sistema que no es lo suficientemente estricto, podríamos poner en peligro involuntariamente nuestra seguridad. Por otro lado, si elegimos un sistema que es demasiado estricto, podríamos hacer que sea demasiado difícil para las personas hacer su trabajo.