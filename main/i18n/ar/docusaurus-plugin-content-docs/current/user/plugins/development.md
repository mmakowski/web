---
source-hash: 580c8fbd0c79564b0976cee07d1bc9d431e8f4533df5daa052bc1202ccd84564
sidebar_position: 10
title:  تطوير OsmAnd
---
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import AndroidStore from '@site/src/components/buttons/AndroidStore.mdx';
import AppleStore from '@site/src/components/buttons/AppleStore.mdx';
import LinksTelegram from '@site/src/components/_linksTelegram.mdx';
import LinksSocial from '@site/src/components/_linksSocialNetworks.mdx';
import Translate from '@site/src/components/Translate.js';
import InfoIncompleteArticle from '@site/src/components/_infoIncompleteArticle.mdx';
import InfoAndroidOnly from '@site/src/components/_infoAndroidOnly.mdx';




## نظرة عامة {#overview}

تُجمع وظائف الاختبار للتطبيق في الملحق الخاص بتطوير OsmAnd. استخدمها على مسؤوليتك الخاصة.

يتيح لك ملحق تطوير OsmAnd تجربة ميزات جديدة للتطبيق أو تهيئة OsmAnd للاختبار: محاكاة مسارات الملاحة، التحقق من أداء عرض الشاشة، إلخ. تم تصميم الملحق للمطورين والمستخدمين ذوي الخبرة ولا يلزم للاستخدام اليومي للتطبيق.


## معلمات الإعداد المطلوبة {#required-setup-parameters}

لتفعيل الميزات الخاصة للمطورين والمختبرين:

1. [فعّل](../plugins/index.md#enable--disable) ملحق تطوير OsmAnd في قسم الملحقات من *القائمة الرئيسية*.
2. قم بإجراء الإعدادات اللازمة في [قائمة إعدادات](#plugin-settings) الملحق.
3. فعّل **أدوات المطور** إذا لزم الأمر.


## إعدادات الملحق {#plugin-settings}

:::info info
إعدادات ملحق تطوير OsmAnd عالمية وتنطبق على جميع الملفات الشخصية.
:::

استخدم أحد المسارات التالية لفتح إعدادات الملحق:

- *القائمة الرئيسية ← الملحقات ← تطوير OsmAnd ← الإعدادات*.
- *القائمة الرئيسية ← [الإعدادات العامة](../personal/global-settings.md) ← الملف الشخصي ← إعدادات ملحق تطوير OsmAnd*.

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

![Development Settings Android](@site/static/img/plugins/development/development_settings_1_andr.png) ![Development Settings 2 Android](@site/static/img/plugins/development/development_settings_2_andr.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Development Settings iOS](@site/static/img/plugins/development/development_ios_1.png)

</TabItem>

</Tabs>


### التضاريس {#terrain}

- **استخدام تنسيق [SQLIte النقطي](../../technical/osmand-file-formats/osmand-sqlite) لتظليل التلال والانحدار** (*أندرويد*). تحميل خرائط نقطية بالتنسيق القديم.


### استكشاف الأخطاء وإصلاحها {#troubleshotting}

- **محاكاة موقعك** (*أندرويد* / *iOS*). [محاكاة](#gpx-track-simulation) الموقع والحركة باستخدام مسار GPX.
- **وضع توفير البطارية** (*أندرويد* / *iOS*). يقلل هذا الإعداد [معدل تحديث الشاشة](#map-rendering-fps-widget) بمقدار 20 إطارًا في الثانية للمساعدة في توفير طاقة البطارية أثناء استخدام التطبيقات.
- **استخدام أيقونات موقع ثلاثية الأبعاد** (*iOS*). يتيح لك تحديد أيقونة ثلاثية الأبعاد [لأيقونة موقعي](../personal/profiles.md#my-location-appearance).
- **محاكاة بيانات OBD** (*أندرويد*). يتيح محاكاة استخدام [ماسح OBD](./vehicle-metrics.md).
- **معلومات تصحيح الأداء** (*أندرويد*). يعرض أداء العرض والملاحة.
- **تعطيل طبقات الخريطة** (*أندرويد*). يعطل جميع طبقات الخريطة فوق الخريطة المتجهة (يتطلب إعادة التشغيل).
- **مخزن Logcat المؤقت** (*أندرويد*). تحقق وشارك السجلات التفصيلية للتطبيق.
- **إظهار إشعار حول المفتاح المضغوط** (*أندرويد*). عرض رسالة حول المفتاح.
- **<Translate android="true" ids="write_bearing"/>** (*أندرويد*). <Translate android="true" ids="write_bearing_description"/>. الاتجاه هو الاتجاه البوصلة من موقعك الحالي إلى وجهتك المقصودة. يؤثر على *[تسجيل المسار](../plugins/trip-recording.md)*.
- **<Translate android="true" ids="write_heading"/>** (*أندرويد*). <Translate android="true" ids="write_heading_description"/>. الاتجاه هو الاتجاه البوصلة من موقعك الحالي نحو الشمال الحقيقي. هذا الخيار ممكّن افتراضيًا. يؤثر على *[تسجيل المسار](../plugins/trip-recording.md)*.


### اختبار التطبيق {#application-testing}

:::caution أندرويد فقط
:::

- **محاكاة بدء تشغيل التطبيق لأول مرة**. يعيّن العلامة التي تشير إلى بدء تشغيل التطبيق لأول مرة، ويحافظ على جميع الإعدادات الأخرى دون تغيير.
- **اختبار المطالبات الصوتية**. اختر صوتًا واختبره بتشغيل الإعلانات.
- **شريط الحالة الشفاف**. تصبح الخريطة مرئية تحت شريط الحالة.
- **إظهار لافتة الإصدار المجاني**. عرض لافتة الإصدار المجاني حتى في الإصدار المدفوع.
- **إظهار معلومات التصحيح**. عرض معلومات رسومية حول موضع كل نص على الخريطة.
- **السماح بالعرض في الأعلى**. يسمح بعرض نصوص الخريطة فوق بعضها البعض.


### الخوارزميات الداخلية {#internal-algorithms}

:::caution أندرويد فقط
:::

- **الوضع الآمن**. تشغيل التطبيق في الوضع الآمن (أبطأ).


### إعدادات الذاكرة {#memory-settings}

:::caution أندرويد فقط
:::

- يسمح لك خيار **الذاكرة المخصصة للتوجيه** بتحديد مقدار الذاكرة المخصصة لحساب المسارات الطويلة. يمكنك استخدام هذا الخيار إذا تم تحديد [التوجيه القياسي A*](../navigation/guidance/navigation-settings.md#development-settings) في *إعدادات الملاحة*.

***حساب المسارات الطويلة جدًا:***

- قد يؤثر تخصيص الذاكرة العالي على أداء التطبيقات الأخرى.
- [حساب مسارات 50 كم للمشاة](../troubleshooting/navigation.md#calculation-of-50-km-routes-for-pedestrians)


### معلومات وإحصائيات {#info-and-statistics}

:::caution أندرويد فقط
:::

- **الذاكرة المخصصة**. يعرض الذاكرة المخصصة للنظام لتطبيق OsmAnd.
- **إجمالي الذاكرة الأصلية**. يعرض إجمالي مقدار الذاكرة الأصلية المخصصة للتطبيق، بما في ذلك الذاكرة التناسبية.
- **معلومات A-GPS**. يشير إلى آخر مرة تم فيها تنزيل بيانات A-GPS.
- **معلومات النهار/الليل**. يشير إلى أوقات شروق الشمس وغروبها اليوم.
- **إحصائيات الطاقة (متوسط 1 / 5 / 15 دقيقة)**. يعرض مستوى البطارية لكل دقيقة (٪) ومتوسط استهلاك الطاقة (mAh) على فترات 1 و 5 و 15 دقيقة.
- **إحصائيات العرض (متوسط 1 / 5 / 15 دقيقة)**. يعرض إحصائيات العرض، بما في ذلك FPS على آخر 1k إطار، ووحدة المعالجة المركزية (البلاط)، ووحدة المعالجة المركزية (وقت الخمول)، ووحدة المعالجة المركزية (الاستعداد) بمتوسطات على فترات 1 و 5 و 15 دقيقة.

**الزر:**

- **إعادة تعيين إعدادات الملحق إلى الافتراضي**. يعيد تعيين جميع إعدادات الملحق إلى قيمها الافتراضية.

    ![Development Settings Android](@site/static/img/plugins/development/devplugin_stat_and.png)


## أداة FPS لعرض الخريطة {#map-rendering-fps-widget}

:::info هام
يمكن إضافة أدوات مطور OsmAnd إلى الشاشة فقط عند تمكين ملحق تطوير OsmAnd.
:::

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

انتقل إلى: *<Translate android="true" ids="shared_string_menu,layer_map_appearance,map_widget_right"/> / <Translate android="true" ids="map_widget_left,developer_widgets,map_widget_rendering_fps"/>*

![Development widget fps 1](@site/static/img/plugins/development/dev_widgets_fps_1.png) ![Development widget fps 2](@site/static/img/plugins/development/dev_widgets_fps_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

انتقل إلى: *<Translate ios="true" ids="shared_string_menu,layer_map_appearance,map_widget_right"/> / <Translate ios="true" ids="map_widget_left,developer_widgets,map_widget_rendering_fps"/>*

![Development widget iOS 2](@site/static/img/plugins/development/dev_widgets_ios_fps_2.png)

</TabItem>

</Tabs>

تعرض [أداة FPS](../widgets/info-widgets.md#map-rendering-fps) مدى سرعة عرض وتحديث الخريطة وعناصر الخريطة. تُشار القيمة الرقمية بالإطارات في الثانية (FPS).


## أدوات موضع الكاميرا {#camera-position-widgets}

:::info هام
يمكن إضافة أدوات مطور OsmAnd إلى الشاشة فقط عند تمكين ملحق تطوير OsmAnd.
:::

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

انتقل إلى: *<Translate android="true" ids="shared_string_menu,layer_map_appearance,map_widget_right"/> / <Translate android="true" ids="map_widget_left,developer_widgets"/>*

![Camera position Widgets 1](@site/static/img/plugins/development/dev_widgets_camera.png) ![Camera position Widgets 2](@site/static/img/plugins/development/dev_widgets_camera_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

انتقل إلى: *<Translate ios="true" ids="shared_string_menu,layer_map_appearance,map_widget_right"/> / <Translate ios="true" ids="map_widget_left,developer_widgets"/>*

![Camera position Widgets 1](@site/static/img/plugins/development/dev_widgets_camera_ios.png) ![Camera position Widgets 2](@site/static/img/plugins/development/dev_widgets_camera_2_ios.png)

</TabItem>

</Tabs>

يمكنك استخدام [أدوات موضع الكاميرا](../widgets/info-widgets.md#camera-widgets) لإعطاء خريطة OsmAnd مظهرًا واقعيًا ومطابقة صور الأرض الملتقطة من الأعلى ومن الفضاء.


### إمالة الكاميرا {#camera-tilt}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

![Camera tilt widget Android 1](@site/static/img/plugins/development/developer_widg_cam_tilt_1.png) ![Camera tilt widget Android 2](@site/static/img/plugins/development/developer_widg_cam_tilt_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Camera tilt widget ios 1](@site/static/img/plugins/development/developer_widg_cam_tilt_ios_1.png) ![Camera tilt widget ios 2](@site/static/img/plugins/development/developer_widg_cam_tilt_ios_2.png)

</TabItem>

</Tabs>

تعرض أداة إمالة الكاميرا الميل بين متجه العرض المركزي للكاميرا (المشاهد) وأرضية مسطحة وهمية للأرض. القيمة الافتراضية هي 90 درجة (لا يوجد ميل).

:::note
تتغير إمالة الكاميرا بتحريك الكاميرا (المشاهد) بينما تظل النقطة المركزية على الخريطة (التي ننظر إليها) كما هي. المسافة إليها (في الواقع، التكبير) لا تتغير.
في الوقت نفسه، بسبب الحركة الوهمية للمشاهد، تتغير المسافة من الكاميرا إلى السطح.
:::


### ارتفاع الكاميرا {#camera-elevation}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

![Camera elevation widget Android 1](@site/static/img/plugins/development/developer_widg_cam_elevation_1.png) ![Camera elevation widget Android 2](@site/static/img/plugins/development/developer_widg_cam_elevation_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Camera elevation widget ios 1](@site/static/img/plugins/development/developer_widg_cam_elevation_ios_1.png) ![Camera elevation widget ios 2](@site/static/img/plugins/development/developer_widg_cam_elevation_ios_2.png)

</TabItem>

</Tabs>

تعرض أداة ارتفاع الكاميرا ارتفاع الكاميرا فوق مستوى السطح. يُشار إلى ارتفاع الكاميرا بالمتر / الكيلومتر.


### مستوى التكبير {#zoom-level}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

![Zoom level widget Android 1](@site/static/img/plugins/development/developer_widget_zoom_2_andr.png) ![Zoom level widget Android 2](@site/static/img/plugins/development/developer_widg_zoom_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Zoom level widget ios 1](@site/static/img/plugins/development/developer_widget_zoom_ios_1_ios.png) ![Zoom level widget ios 2](@site/static/img/plugins/development/developer_widget_zoom_ios_2_ios.png)

</TabItem>

</Tabs>

تحتوي الأداة على عرضين يتم التبديل بينهما بالنقر عليها:

- **<Translate android="true" ids="map_widget_zoom_level"/>**. يعرض مستوى التكبير الحالي للخريطة.
- **<Translate android="true" ids="map_widget_map_scale"/>**. يعرض النسبة الحالية بين المسافة على الخريطة والمسافة المقابلة على الأرض. أمثلة: "1 : 3 000"، "1 : 3.3 مليون"، "1: 340 ألف".

:::note

- مستوى التكبير الأولي (0) هو المستوى الذي تُعرض فيه كامل سطح الأرض (الخريطة الكاملة) على الشاشة، وحجمها 256 × 256 بكسل.
- كل مستوى تكبير تالٍ يقلل المسافة الوهمية إلى الأرض بحوالي 2 مرة.

:::

### المسافة إلى الهدف {#distance-to-target}

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

![Distance to target widget 1 Android](@site/static/img/plugins/development/developer_widg_distance_to_target_1.png) ![Distance to target widget 2 Android](@site/static/img/plugins/development/developer_widg_distance_to_target_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Distance to target widget 1 iOS](@site/static/img/plugins/development/developer_widg_distance_to_target_ios_1.png) ![Distance to target widget 2 iOS](@site/static/img/plugins/development/developer_widg_distance_to_target_ios_2.png)
</TabItem>

</Tabs>

تعرض أداة المسافة من الكاميرا إلى الهدف المسافة بين الكاميرا (المشاهد) ومركز الخريطة. تُعرض هذه المسافة بالمتر / الكيلومتر.


### مقارنة مع صور الأقمار الصناعية {#comparison-with-a-satellite-imagery}

![Comparison](@site/static/img/plugins/development/comparison.png)

تكشف مقارنة خريطة OsmAnd وسطح الأرض عن الأنماط التالية:

- يُلاحظ أقصى تشوه عند التكبيرات الكبيرة (تكبير 6-7 لإمالة الكاميرا 90 درجة).
- مع انخفاض إمالة الكاميرا (من 90 إلى 10 درجات)، يزداد تشوه الخريطة.
- تبدأ التشوهات في الظهور مبكرًا في خطوط العرض العليا.

يحتوي الجدول أدناه على معلومات حول إمالة الكاميرا والمسافة إلى الهدف ومستوى التكبير الذي تصبح فيه تشوهات خريطة OsmAnd مرئية. إذا استمرت الكاميرا في الابتعاد عن الهدف، سيزداد التشوه الملحوظ لخريطة OsmAnd.

|الميل (90) |خط العرض |أقصى تكبير |الارتفاع، كم |التشوه|
|-----|-----|-----|-----|-----|
|90|26|6|5500|5%|
|90|50|6|2500|5%|
|90|66|7|1300|5%|
|**الميل (60)** |**خط العرض** |**أقصى تكبير** |**الارتفاع، كم** |**التشوه**|
|65|26|8|1100|6.5%|
|65|50|8|800|6.5%|
|65|66|9|630|6.5%|
|**الميل (45)** |**خط العرض** |**أقصى تكبير** |**الارتفاع، كم** |**التشوه**|
|45|26|9|350|7.5%|
|45|50|9|320|7.5%|
|45|66|8|210|7.5%|
|**الميل (20)** |**خط العرض** |**أقصى تكبير** |**الارتفاع، كم** |**التشوه**|
|20| 26|12|30|10%|
|20| 50|11|30|10%|
|20| 66|11|30|10%|


## أداة RAM المتاحة {#available-ram-widget}

صُممت هذه الأداة خصيصًا لك عند استخدام OsmAnd لتوفير تفاعل أكثر ملاءمة وغنى بالمعلومات مع ذاكرة الوصول العشوائي (RAM) المتاحة على جهازك. تتيح لك مراقبة ذاكرة الوصول العشوائي المتاحة بسهولة وسرعة، وهو أمر مفيد بشكل خاص عند استخدام OsmAnd للملاحة. اقرأ المزيد عن الأداة في مقالة [أدوات المعلومات](../widgets/info-widgets.md#available-ram).


## محاكاة مسار GPX {#gpx-track-simulation}

يوفر OsmAnd فرصة لمحاكاة موقع جهازك وحركته باستخدام مسار GPX. لهذه الأغراض، استخدم خيار *<Translate android="true" ids="simulate_location_by_gpx"/>* في [إعدادات](#plugin-settings) ملحق تطوير OsmAnd:

- انقر على *<Translate android="true" ids="simulate_location_by_gpx"/>*.
- اختر مسارًا لمحاكاة موقع الجهاز وحركته.
- اختر سرعة محاكاة الحركة.
- انقر على زر البدء.

<Tabs groupId="operating-systems" queryString="current-os">

<TabItem value="android" label="أندرويد">

![Development Settings Android](@site/static/img/plugins/development/simulate_position_andr_1.png) ![Development Settings Android](@site/static/img/plugins/development/simulate_position_andr_2.png)

</TabItem>

<TabItem value="ios" label="iOS">

![Development Settings iOS](@site/static/img/plugins/development/development_plugin_choose_track_1_ios.png) ![Development Settings iOS](@site/static/img/plugins/development/development_plugin_choose_track_ios.png)

</TabItem>

</Tabs>

بعد تشغيل المحاكاة، سترى على الشاشة الرئيسية للتطبيق أن علامة الملاحة تتحرك وفقًا لمسار GPX. انقر على [زر موقعي](../map/interact-with-map#my-location-and-zoom) لمزامنة *موقعي* (الموقع الجغرافي المحاكي للجهاز) مع مركز الخريطة.
لإيقاف محاكاة حركة جهازك، ارجع إلى [إعدادات](#plugin-settings) تطوير OsmAnd وانقر على **إيقاف** في خيار **محاكاة موقعك**.

- يمكن الوصول إلى *<Translate android="true" ids="simulate_location_by_gpx"/>* أيضًا من خلال **[قائمة الإجراءات السريعة](../widgets/quick-action.md#navigation)**.
- يمكن تعيين سرعة حركة الموقع أثناء المحاكاة لتكون مساوية للسرعة المسجلة (1)، أو أسرع (x2، x3، x4).
- يمكنك أيضًا محاكاة الحركة على طول مسار GPX من [قائمة الملاحة](../navigation/setup/route-navigation.md#simulated-navigation) دون تمكين ملحق تطوير OsmAnd. في هذه الحالة، لن تتم مزامنة موقعك مع المسار.


## مقالات ذات صلة {#related-articles}

- [التفاعل مع الخريطة](../../user/map/interact-with-map.md)
- [الإعدادات العامة](../../user/personal/global-settings.md)
- [خرائط المتجهات (أنماط الخرائط)](../../user/map/vector-maps.md)

> *آخر تحديث: مايو 2023*