---
source-hash: 2f59b1c67bc9886426af5d0c0cd282853675b77154ff95cd42a65f37a70509cb
sidebar_position: 17
title: El tiempo
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/buttons/AndroidStore.mdx';
import AppleStore from '@site/src/components/buttons/AppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';
import InfoIncompleteArticle from '@site/src/components/_infoIncompleteArticle.mdx';
import ProFeature from '@site/src/components/buttons/ProFeature.mdx';
import InfoAndroidOnly from '@site/src/components/_infoAndroidOnly.mdx';

## Descripción general {#overview}

:::info Función de pago
 <ProFeature/> El complemento El tiempo es una [función de pago](../purchases/index.md) de la aplicación OsmAnd.
:::

Las capas interactivas del mapa meteorológico de la aplicación OsmAnd te permiten controlar la temperatura, la presión atmosférica, la nubosidad, la velocidad del viento y las precipitaciones en tu ciudad o en cualquier otro lugar en un mapa interactivo global. El complemento El tiempo proporciona pronósticos meteorológicos por hora para los próximos 7 días directamente en el mapa de OsmAnd. La información meteorológica también se puede descargar para usarla sin conexión.

La fuente de datos para el complemento El tiempo es el [Sistema de Pronóstico Global](https://www.ncei.noaa.gov/products/weather-climate-models/global-forecast) operado por el Servicio Meteorológico Nacional de los Estados Unidos (NWS) y el Centro Europeo de Pronósticos Meteorológicos de Rango Medio ([ECMWF](https://www.ecmwf.int/)).

## Parámetros de configuración requeridos {#required-setup-parameters}

Los siguientes ajustes son *necesarios* para mostrar el tiempo en el mapa de OsmAnd:

**1.** [Adquirir la **suscripción OsmAnd Pro**](../purchases/).

**2.** [Habilitar](../plugins/#enable--disable) el complemento El tiempo en la sección *Complementos* del *Menú principal*.

**3.** [Seleccionar las **unidades de medida**](#weather-settings) para los fenómenos meteorológicos.

**4.** [Mostrar las **capas de El tiempo**](#customize-weather-layers) en el mapa usando el elemento de menú El tiempo en el menú Configurar mapa (recuerda alejar el zoom).

**5.** [Ver el **pronóstico del tiempo**](#weather-forecast-screen) para el área seleccionada (este menú permite que la pantalla principal del mapa de OsmAnd no se sature con capas meteorológicas).

**6.** [Descargar](#offline-forecast) el pronóstico del tiempo si planeas usarlo sin conexión.

**7.** [Habilitar los **widgets de El tiempo**](#weather-widgets) si deseas ver información meteorológica actualizada diariamente.

:::caution Renderizado requerido
El complemento El tiempo solo está disponible con el motor de renderizado de mapas [Versión 2](../personal/global-settings/#map-rendering-engine) (OpenGL).
:::

## Mostrar el tiempo en el mapa {#display-weather-on-the-map}

### Pantalla de pronóstico del tiempo {#weather-forecast-screen}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Ir a: *Complemento habilitado → <Translate android="true" ids="shared_string_menu,shared_string_weather"/>*

![Weather Dashboard Android 2](@site/static/img/plugins/weather/weather_dashbord_andr_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

Ir a: *Complemento habilitado → <Translate ios="true" ids="shared_string_menu,shared_string_weather"/>*

![Weather Dashboard in iOS](@site/static/img/plugins/weather/weather_dashbord_ios_2.png)

</TabItem>

</Tabs>

El menú lateral principal tiene un elemento de menú dedicado **El tiempo** que proporciona acceso rápido a todas las herramientas meteorológicas. La *pantalla de pronóstico del tiempo* muestra información sobre *temperatura*, *presión atmosférica*, *velocidad del viento*, *nubosidad* y *precipitación*.

En la parte inferior de la pantalla se encuentra la *barra de herramientas del tiempo*. Puedes usar los botones de día y el deslizador de tiempo para establecer la hora exacta en que se mostrará el pronóstico del tiempo.

### Personalizar capas de El tiempo {#customize-weather-layers}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Ir a: *Complemento habilitado → <Translate android="true" ids="shared_string_menu,quick_action_add_configure_map,shared_string_show,shared_string_weather"/>*

![Weather Dashboard Android 2](@site/static/img/plugins/weather/weather_customize_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

Ir a: *Complemento habilitado → <Translate ios="true" ids="shared_string_menu,configure_map,map_settings_overunder,shared_string_weather"/>*

![Weather Dashboard in iOS](@site/static/img/plugins/weather/weather_customize_ios.png)

</TabItem>

</Tabs>

Para mostrar las capas meteorológicas en la pantalla del mapa de OsmAnd, debes usar el menú *Configurar mapa*. Ve al menú, busca el elemento *El tiempo* en la lista (solo disponible cuando el complemento está habilitado) y tócalo.

En este menú, puedes cambiar la **visibilidad** y los [ajustes](#weather-settings) de cada capa, seleccionar el tipo de líneas de contorno y descargar el [pronóstico del tiempo sin conexión de 7 días](#offline-forecast) (*solo disponible para Android aquí*).

### Ajustes de El tiempo {#weather-settings}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

- *Menú principal → Complementos → El tiempo → Ajustes*
- *Menú principal → Ajustes → Perfil → Ajustes de complemento → El tiempo*

![Weather Settings Android](@site/static/img/plugins/weather/weather_settings_andr_1.png) ![Weather Settings 2 Android](@site/static/img/plugins/weather/weather_settings_andr_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

- *Menú principal → Ajustes → Perfil → Complementos → El tiempo*

![Weather Settings iOS](@site/static/img/plugins/weather/weather_settings_ios.png) ![Weather Settings iOS 2](@site/static/img/plugins/weather/weather_settings_ios_2.png)

</TabItem>

</Tabs>

Es importante decidir en qué unidades de medida te resulta conveniente ver los [datos meteorológicos](#weather-layers) en el mapa y en la sección [widgets de El tiempo](#weather-widgets) de la pantalla. Puedes elegir las unidades de medida adecuadas para cada parámetro o usar los valores predeterminados (*solo iOS*). En la versión de iOS de la aplicación OsmAnd, también puedes habilitar la opción de pronóstico sin conexión para evitar el uso de datos móviles mientras viajas.

:::note
En la versión de iOS de OsmAnd, puedes cambiar las unidades de medida y el nivel de transparencia en el menú que se abre después de una pulsación larga del icono de la capa de mapa requerida.
:::

### Capas de El tiempo {#weather-layers}

Todos los datos meteorológicos se presentan como capas de mapa separadas. Para ver las capas meteorológicas en el mapa, debes alejar el zoom, solo están disponibles en escalas de zoom 2-12. Las capas meteorológicas utilizan [paletas meteorológicas](../personal/color-palette-schemes.md#weather) para colorear el mapa, estas paletas pueden [cambiarse](../personal/color-palette-schemes.md#edit-palette-file) si es necesario.

| |
|------------|
| La **capa de precipitación** muestra información sobre eventos meteorológicos cuando el agua en diferentes estados agregados cae del cielo al suelo. La precipitación es lluvia, nieve, aguanieve o granizo. La escala de precipitación se gradúa en milímetros (o pulgadas) de agua que cae sobre 1 metro cuadrado en 24 horas. 1 mm de lluvia corresponde a 1 litro de agua por 1 metro cuadrado. |
|![Precipitation sheme](@site/static/img/plugins/weather/precipitation.png)|
| La **temperatura** expresa la percepción cuantitativa de calor y frío. Se mide en grados. En OsmAnd, puedes elegir entre la escala Celsius y Fahrenheit. |
|![Temperature sheme](@site/static/img/plugins/weather/temperature.png)|
| El **viento** es el movimiento del aire causado por el calentamiento desigual de la Tierra por el sol y su propia rotación. Los vientos pueden variar desde brisas ligeras hasta desastres naturales como huracanes y tornados. En OsmAnd, la velocidad del viento se puede mostrar en metros por segundo (m/s), kilómetros por hora (km/h), millas por hora (mph) y nudos (kt). |
|![Wind sheme](@site/static/img/plugins/weather/wind.png)|
| La **nubosidad** es la fracción promedio del cielo cubierta por nubes cuando se observa desde un lugar en particular. Se mide en %. |
|![Clouds sheme](@site/static/img/plugins/weather/clouds.png)|
| La **presión atmosférica** es causada por el peso del aire sobre el punto de medición. Disminuye con el aumento de la elevación. La presión atmosférica se puede mostrar en hectopascales (hPa), milímetros de mercurio (mmHg) y pulgadas de mercurio (inHg). |
| ![Pressure sheme](@site/static/img/plugins/weather/pressure.png) |
| La **animación del viento** incluye representaciones dinámicas que muestran la dirección y la velocidad del viento en toda la región. |
| ![Wind annimation](@site/static/img/plugins/weather/wind_annimation.gif) |

### Combinar mapas {#combine-maps}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Combine Weather layers on Android](@site/static/img/plugins/weather/weather_combine_layers_andr_1.png) ![Combine Weather layers on Android](@site/static/img/plugins/weather/weather_combine_layers_andr_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Combine Weather layers on iOS](@site/static/img/plugins/weather/weather_combine_layers_ios_1.png) ![Combine Weather layers on iOS](@site/static/img/plugins/weather/weather_contours.png)

</TabItem>

</Tabs>

Para obtener información meteorológica completa, puedes usar las capas del mapa por separado o combinarlas fácilmente. También se pueden añadir isolíneas de un tipo específico a la capa de El tiempo. Simplemente toca el botón *Capas* o *Isolíneas* en la pantalla.

### Acciones rápidas para capas {#quick-actions-for-layers}

![QA Weather layers](@site/static/img/plugins/weather/QA_weather_layers_andr.png)

Para cambiar la visibilidad de las capas meteorológicas, puedes usar los botones de *Acción rápida* en la pantalla del mapa. Los ajustes generales para mostrar u ocultar capas se pueden encontrar en la [sección de El tiempo](#weather-forecast-screen) separada del *Menú principal*. En el artículo [Acción rápida](../widgets/quick-action.md#configure-map), encontrarás una lista de las capas disponibles para mostrar. Si necesitas acceso rápido a esta configuración del mapa, usa la herramienta *Botón personalizado*.

- Ve a [Añadir acción](../widgets/quick-action.md#custom-buttons): *Menú → Configurar pantalla → Botones personalizados → Acción rápida → Añadir acción → Configurar mapa*.
- Añade uno o más botones de QA para cambiar la visibilidad de una capa meteorológica en particular.

## Pronóstico sin conexión {#offline-forecast}

### Caché {#cache}

Cuando la pestaña El tiempo está abierta, a menos que se especifique lo contrario, la información meteorológica requerida se descarga de la red. Puedes usar el [pronóstico del tiempo](#download-forecast) precargado en tus dispositivos. La información meteorológica se almacena automáticamente en caché después de la descarga y se puede usar sin conexión hasta que el pronóstico caduque.

:::tip
En dispositivos Android, puedes verificar cuándo se han descargado los datos meteorológicos tocando el *widget de El tiempo*. El complemento de desarrollo de OsmAnd debe estar habilitado.
![Date of weather cash android](@site/static/img/plugins/weather/weather_cash_andr.png)
:::

### Descargar pronóstico {#download-forecast}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

![Weather plugin in Android](@site/static/img/plugins/weather/download_weather_android.png) ![Weather plugin in Android](@site/static/img/plugins/weather/download_weather_1_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Weather plugin in iOS](@site/static/img/plugins/weather/download_weather_ios.png) ![Weather plugin in iOS](@site/static/img/plugins/weather/download_weather_1_ios.png)

</TabItem>

</Tabs>

Para cada país, puedes descargar el **Pronóstico sin conexión** (hasta 7 días). Cuanto más cerca esté de la fecha actual, más preciso será. Si deseas usar el pronóstico del tiempo sin conexión, debes descargar los datos meteorológicos con anticipación.

En el menú de descarga del pronóstico, puedes obtener información y establecer parámetros para mantener los datos meteorológicos actualizados.

- **Creado** (*Android*) / **Actualizado** (*iOS*). Muestra cuándo se realizó la última actualización.
- **Próxima actualización** (*iOS*). Cuándo estará disponible la próxima actualización.
- **Tamaño** (*Android*) / **Tamaño de las actualizaciones** (*iOS*). Muestra el tamaño de todas las actualizaciones.
- Botón **Actualizar** (*Android*) / **Actualizar ahora** (*iOS*). Cuando está activo, te permite actualizar los datos meteorológicos manualmente sin esperar una actualización automática.
- **Frecuencia de actualización** (*iOS*). Se puede configurar en 12 horas, 24 horas o semanalmente.
- *Actualizar solo a través de Wi-Fi* (*iOS*). Habilita esta opción si no deseas usar datos móviles para las descargas.
- Botón **Eliminar** *papelera* (*Android*) / **Eliminar pronóstico** (*iOS*). Te permite eliminar todos los datos del pronóstico para esta región.
- Botón **Editar** *lápiz* (*Android*). Te permite cambiar el nombre del archivo meteorológico.

:::info
OsmAnd genera un nuevo pronóstico cada 6 horas.
:::

## Widgets de El tiempo {#weather-widgets}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="Android">

Ir a: *<Translate android="true" ids="shared_string_menu,map_widget_config,shared_string_widgets"/> → Elegir un panel → <Translate android="true" ids="shared_string_weather"/>*

![Weather widgets on Android](@site/static/img/plugins/weather/weather_widgets_1_android.png) ![Weather widgets on Android](@site/static/img/plugins/weather/weather_widgets_2_android.png)

</TabItem>

<TabItem value="ios" label="iOS">

Ir a: *<Translate ios="true" ids="shared_string_menu,layer_map_appearance,shared_string_widgets"/> → Elegir un panel → <Translate ios="true" ids="shared_string_weather"/>*

![Weather widgets on iOS](@site/static/img/plugins/weather/weather_widgets_1_ios.png)

</TabItem>

</Tabs>

Los [widgets de El tiempo](../widgets/info-widgets.md#weather-widgets) como Temperatura, Presión atmosférica, Viento, Nubes y Precipitación muestran los datos meteorológicos actuales para el **punto central del mapa**.

- Los widgets de El tiempo solo se muestran cuando la [pantalla de El tiempo](#weather-forecast-screen) está activada.
- Para activar los widgets de El tiempo, selecciona el elemento del menú principal *Configurar pantalla*, el panel en el que colocarlos y los widgets necesarios de la lista.

## Artículos relacionados {#related-articles}

- [Interactuar con el mapa](../../user/map/interact-with-map.md)
- [Ajustes globales](../../user/personal/global-settings.md)
- [Mapas vectoriales (Estilos de mapa)](../../user/map/vector-maps.md)

> *Última actualización: Noviembre de 2024*