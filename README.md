# Página PetandLove
La página de PetandLove es un e-commerce creado en Magento CE 2.3.0, se eligió esta herramienta por ser una de los CMS en comercio electrónico más grandes y estables en el mercado, a diferencia de otras plataformas de comercio como WooCommerce de Wordpress o Prestashop, magento da una mayor flexibilidad y adaptación del FrontEnd y BackEnd.

# Hospedaje
Magento es una plataforma con requisitos específicos para su despliegue en un servidor web por lo que se recomienda revisar su documentación (https://devdocs.magento.com/guides/v2.3/install-gde/system-requirements-tech.html), tenga en cuenta que si se cambia de proveedor el hospedaje debe tener acceso a conexiones SSH externas entre otras cosas que se explican en los archivos de magento, es importante que no contrate un hosting compartido ya que la plataforma de magento y la plantilla utilizada pueden no funcionar correctamente por los recursos limitados de estos planes de hospedaje.

Actualmente la página esta hospedada en `Hostinger` con un plan de Cloud Hosting Professional.

### Características del sitio

- Servicio de alojamiento Cloud Hosting Professional `Hostinger`,
- Gestor phpmyadmin.
- Plataforma de comercio electrónico Magento CE 2.3.0
- Tema del sitio plantilla Sirena Premium magento theme by MeigeeTeam (https://meigeeteam.com/sirena-multipurpose-responsive-magento-theme)


### Base de datos
Revise la Carpeta **Sitio PetandLove** y elija el fichero BD.


### Notas importantes:

- Para modificar y administrar la plataforma debe usar el administrador de magento http://www.petandlove.mx/admin_1r3tho/, revise el archivo de contraseñas.
- Se modificaron los archivos app/code/Meigee/Sirena/Block/Html/MeigeeTopmenu.php en la línea 391 y de la línea 422 a la 444
 Así como app/code/Meigee/CategoriesEnhanced/view/frontend/web/css/megamenu.css, estos cambios se hicierón para agregar el evento clicked en las imagenes del menú.
- Cuando se hagan modificaciones en los archivos css, debe hacerlo en la carpeta sirena_child tal como lo marca la documentación del theme.
- Todos los archivos css en sirena_child que fuerón modificados tienen comentarios de /*Cambio*/ o /*Nuevo*/, esto indica que un estilo fue modificado de su valor original o se añadio uno nuevo para obtener el estilo deseado.
- El sitio tiene paypal como un método de pago, revise el archivo de contraseñas para acceder a su panel de paypal.
- La integración de OpenPay quedo pendiente. Este método de pago esta implementado en SandBox, se debe actualizar la cuenta a productiva.

### Accesos 
Vea el archivo contraseñas en el drive.
