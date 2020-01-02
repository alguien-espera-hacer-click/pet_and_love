# Aplicación PetandLove
Se utilizaron las herramientas Api Rest y Graphl de magento.


### Metodología de diseño
`MVVM`
### Características de la aplicación
- Lenguaje de maquetado `XAML`
- Lenguaje de programación `C#`
- Framework Xamarin.forms 4.2.0


### Paquetes Nuget en PCL
`CardsView 2.3.7`
`Microsoft.Net.Http 2.2.29`
`Newtonsoft.Json 12.0.3`
`Plugin.Badge 2.2.1`
`sqlite-net-pcl 1.5.231`
`Unity" Version="5.11.1`
`Xamarin.FFImageLoading.Forms 2.4.11.982`
`Xamarin.Forms 4.2.0.709249`
`Xamarin.Essentials 1.2.0`
`Xamarin.Forms.Extended.InfiniteScrolling 1.0.0-preview2`
`Xamarin.Forms.RangeSlider 1.0.2`
`XamEffects 1.6.3`


### Base de datos
-Se usa la base de datos de petanlove, el acceso y manejo se hace por medio de Api-Rest y Graphl
-Las aplicaciones usan una base de datos interna. Solo hay dos tablas (userTable) y (QuoteTable).


### Notas importantes:
- Los slides de la página Inicio.xaml se obtienen del servidor en donde esta alojada la tienda de petandlove, revise la carpeta app_movil/img, estas imágenes duraran 30 días en la caché del celular pasado este tiempo se vuelven a solicitar al servidor las imágenes, por lo que no se recomienda hacer campañas de descuento o promociones, si desea cambiar este comportamiento diríjase al código fuente en el archivo Inicio.xaml y modifique la propiedad `CacheDuration=30` de la etiqueta `<ff:CachedImage>` del primer carrusel.
```xml
<cards:CarouselView IsVisible="True"  x:Name="Slider" ItemsSource="{Binding SliderInicio}" HeightRequest="190" IsCyclical="True" SlideShowDuration="8000" >
     <cards:CarouselView.ItemTemplate>
          <DataTemplate>
             <ff:CachedImage Source= "{Binding file}" Aspect="Fill" VerticalOptions="CenterAndExpand"  CacheDuration= "30" DownsampleToViewSize = "true"/>
              </DataTemplate>
      </cards:CarouselView.ItemTemplate>
</cards:CarouselView>
```
Para más información revise la documentación del paquete nuget `Xamarin.FFImageLoading.Forms`
- Las imágenes de Favoritos.xml y QuotePage.xml tiene el mismo comportamiento que los slides de la página Inicio.xaml, sus imágenes se encuentran en app_movil/img Pagina_Favoritos.png y Pagina_Carrito.png correspondientemente.
- Las Api-Rest /V1/wishlist/add/:productId y /V1/wishlist/delete/:wishlistItemId fuerón nuevos puntos finales que no están implementados en la versión magento utilizada por lo que si el sitio de magento es actualizado puede perder estas funciones en la aplicación.

### Acciones a considerar:
Por cada cambio que haga en el código fuente, se considerá una actualización de la aplicación por lo que debe generar nuevamente los archivos .apk y .apa con números de versiones incrementales y desplegarlos en las tiendas como una nueva actualización.


