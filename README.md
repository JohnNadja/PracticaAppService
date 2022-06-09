# Práctica de App Service para despliegue de una página estática web usando Azure de Microsoft.

![App service Icon](https://github.com/JohnNadja/PracticaAppService/blob/main/images/app-service-web-app-icon.png)

## Breve descripción
Una Aplicación de Servicios (App Service) de Azure es una es un servicio de tipo [PaaS](https://azure.microsoft.com/es-mx/overview/what-is-paas/) que se ejecuta en la [nube](https://azure.microsoft.com/es-mx/overview/what-is-the-cloud/) de Azure y ésta  permite hacer el despligeue de p+aginas web estáticas a través del [portal de Azure](https://portal.azure.com/#home). Para más información, se puede consultar la siguiente [página](https://docs.microsoft.com/es-es/azure/app-service/) de Microsoft Docs.


-----------

## Requisitos
 - Tener una cuenta de Azure para realizar la práctica en su [Portal](https://portal.azure.com/#home) (si aún no se cuenta con alguna, se puede hacer el registro en el siguiente [enlace](https://azure.microsoft.com/es-mx/free/)). Esto es ya que el recurso de la App Service está hecha para hacerse como pago por uso (Servicio Premium). Es decir, se paga por lo que se consume.
 - Contar con una suscripción activa de Azure para poder crear un recurso de App Service. 
 - Contar con el código fuente de alguna página web creada en un repositorio de GitHub (de preferencia, el nuestro) para poder realizar la práctica. 

-----------

## Instrucciones

Una vez creada la cuenta de Azure y haber ingresado al [portal de Azure] [App Service](https://portal.azure.com/#view/HubsExtension/BrowseResource/resourceType/Microsoft.Web%2Fsites) para realizar los siguientes pasos:

1. Se selecciona la opción **Crear** para acceder a la configuración de una nueva aplicación web (App Service).
![1](https://github.com/JohnNadja/PracticaAppService/blob/main/images/1.png)

2. Como se muestra en la imagen anterior, en **Datos básicos** nos corresponde configurar lo siguente:
    - ***Suscripción*** = la suscripción que se ha creado en Azure.
    - **Grupo de recursos** = el grupo de recursos que se haya creado en Azure. Si no se ha creado ninguno, se crea uno en la sección **Crear nuevo** y se le asigna un nombre.
    - **Nombre** = para nuestra nueva instancia.
    - **Publicar** = Se selecciona la opción *código* ya que se trata de una página web estática y fue creada en un repositorio de GitHub.
    - **Pila de entorno en tiempo de ejecución** = Es para determinar el lenguaje en el que se va a ejecutar la página web. En este caso será *PHP 8.0*.
    - **Región** = La más cercana y disponible para nuestra instancia.
    ![2.1.png](https://github.com/JohnNadja/PracticaAppService/blob/main/images/2.1.png)
    - Más abajo, en la sección de **Plan de App Service**, se encuentra **SKU y tamaño**. Nos quedaremos con la que se muestra en la siguiente imagen pirque su costo es alto si se deja encenido este servicio:
    ![2.2.png](https://github.com/JohnNadja/PracticaAppService/blob/main/images/2.2.png)
    - Por último se selecciona la opción **Revisar y crear** para finalizar con este apartado y se espera a que se cree la instancia.
    ![2.3](https://github.com/JohnNadja/PracticaAppService/blob/main/images/2.3.png)
    ![2.4](https://github.com/JohnNadja/PracticaAppService/blob/main/images/2.4.png)

3. Una vez creado el servicio, se accederá a nuestro repositorio de GitHub y se copiará el código fuente de la página web que se quiere desplegar. Para ahorrar tiempo, se usará la página de un [repositorio](https://github.com/JohnNadja/PaginaWebmuestraAppService) previemante creado.

4. Con nuestro recurso de App Service recién creado en nuestro panel de incio del Portal de Azure, se buscará aque que diga **App Service** como tipo de recurso. 
    ![4.1](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.1.png)
    - Una vez dentro, se mostrará en la parte casi superior derecha una URL, dicha URL nos permitirá acceder al despligue de la página web Por le momento no mostrará nada porque no contiene los datos (el repositorio). Se irá al apartado de *Centro de implementación* que se encuentra en la sección ***Implementación***.
    ![4.2](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.2.png)
    -  En dicho apartado, se encuentra la opción **Origen**, que es de donde obtendremos el código fuente (repositorio).
    ![4.3](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.3.png)
    -  Se selecciona GitHub como opción y se  tendrá que dar clic en el botón de **Autorizar**.
    ![4.4](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.4.png)
    - Se accede a nuestra cuenta de GitHub y se busca el repositorio que contiene la página web que se quiere desplegar.
    ![4.5](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.5.png)
    - Se guardan las modificaciones y en nuestro GitHub, en la sección de ***Actios*** (del repositorio de la página web) se encuentra un proceso activo para el despligue. En las sisguientes imágenes se muestra cómo debería quedar el proceso:
    ![4.6](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.6.png)
    ![4.7](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.7.png)
    - Una vez que todo esté de forma correcta, se puede ingresar a la página web desplegada accediendo al apartado de las siguentes imágenes (o bien se puede acceder desde el panel general de App Service):
    ![4.8](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.8.png) 
    ![4.9](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.9.png)
    ![4.10](https://github.com/JohnNadja/PracticaAppService/blob/main/images/4.10.png)

### Listo, ya está creado el servicio de App Service con una página web estática.

----
# **⚠Importante⚠**: 
### Recordar eliminar el grupo de recursos que se creó en Azure para evitar costos extras no deseados en caso de no ocupar el servicio.
Se puede hacer desde el panel de Azure en inicio y buscando el tipo de recurso que se llama **Grupo de Recursos**.
![5](https://github.com/JohnNadja/PracticaAppService/blob/main/images/5.png)

## Hasta aquí la finalización de la práctica.
