# Lab 6 report Ingeniería Web - Eduardo Díaz - 03/01/2020

A continuación, se proceden a indicar los pasos seguidos para la realización de la práctica.

Se inicia la aplicación web y los microservicios de la siguiente manera:

gradle :web:bootRun
![](./images/LanzadoWeb.png)


gradle :accounts:bootRun
![](./images/LanzadoAccounts.png)


gradle :registration:bootRun
![](./images/LanzadoRegistration.png)

Accediendo al servidor de registro http://localhost:1111/ podemos ver los dos microservicios registrados:
![](./images/AmbosServicios.png)

Para lanzar otro servicio accounts en el puerto 4444, modificamos el puerto indicado en el archivo 
application.yml en accounts/src/main/resources.
![](./images/Puerto4444.png)

Ahora ya se puede ver que tenemos dos servicios disponibles para accounts
![](./images/TresServicios.png)

Al matar el servicio de accounts del puerto 2222, todavia permite obtener informacion de las cuentas ya 
que queda el que esta corriendo en el puerto 4444, ya que habia dos registrados. De esta manera podemos
seguir proveyendo en servicio gracias a la replicación.