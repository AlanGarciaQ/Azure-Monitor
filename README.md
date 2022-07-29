# Azure Monitor
**Objetivo:** Conocer el funcionamiento del recurso de Azure Monitor.

![](/imagenes/monitor.jpg)

**Requisitos**
- Cuenta de Azure con una suscripción activa
- Equipo de cómputo con sistema operativo: Windows, Linux o MacOs.

**Pasos**  
Se inicia sesión en Portal.Azure.com  
Crear una máquina virtual, este proceso ya se describió anteriormente en la práctica llamada “Creación de una máquina virtual”(Dar clic sobre el nombre para que los lleve a esta práctica mencionada.)  
En la barra de búsqueda escribimos “Monitor” y lo seleccionamos.  
En el menú de la parte de la izquierda le damos clic en la opción de métricas.  
En la ventana de la derecha que se abrió seleccionamos el grupo de recursos donde esta nuestra máquina virtual.  
Seleccionamos la máquina virtual.  
Damos clic en aplicar.  
![Imagen 1](/imagenes/Imagen1.png)

En el menú de la parte de arriba le damos clic en métricas y seleccionamos la opción de Porcentaje CPU.  
![](/imagenes/Imagen2.png)

La anclamos en nuestro panel para poder ver siempre esta métrica en el panel de inicio de Azure y estar checando el recurso.  
A continuación, en el menú de la izquierda seleccionamos la opción de alertas.  
Damos clic en crear y seleccionamos reglas de alerta.  
![](/imagenes/Imagen3.png)

En la pestaña de seleccionar un recurso en filtrar por suscripción seleccionamos nuestra suscripción de Azure y le damos en listo.  
En el apartado de recurso quitamos la suscripción.  
Damos clic en seleccionar ámbito.  
Damos clic en filtrar por tipo de recurso.  
Buscamos máquinas virtuales y seleccionamos nuestra máquina virtual.  
Damos clic en listo.  
![](/imagenes/Imagen4.png)

Seleccionamos la pestaña de Detalles, ahí llenamos lo siguiente:  

**En Detalles del proyecto**  
Suscripción: La suscripción que queramos utilizar.  
Grupo de recursos: Podemos crear uno o seleccionar uno ya existente.

**En Detalles de la regla de alerta**  
Gravedad: Seleccionamos crítico.  
Nombre de la regla de alertas: Ponemos el que queramos.  
Descripción de la regla de alertas: Escribimos la descripción que tendrá nuestra alerta.  
Habilitar tras la creación: La seleccionamos.  
Resolver alertas automáticamente: La seleccionamos.  
![](/imagenes/Imagen5.png)

Seleccionamos la pestaña de Detalles, ahí llenamos lo siguiente:  
Seleccionamos la opción de porcentaje de la CPU.  
En valor del umbral ponemos 40.
en periodo le vamos a poner 1 minuto para que lo esté checando cada minuto.  
Damos clic en listo.  
Para terminar, damos clic en Revisar y crear, y luego en crear.  
![](/imagenes/Imagen6.png)

Ingresamos a nuestra máquina virtual, una vez dentro abrimos muchas ventanas en el navegador y también el administrador de tareas, esto lo hacemos para que nos salte la alarma que acabamos de crear.  
![](/imagenes/Imagen7.png)

En alertas se observa que al superar el 40% del uso de la computadora, salta la alerta que pusimos.  
![](/imagenes/Imagen8.png)
