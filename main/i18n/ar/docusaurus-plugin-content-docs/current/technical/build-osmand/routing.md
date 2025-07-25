---
source-hash: 25c29183922ffa0df481d5ee27894c6a7f4653e20a70b824ecbc3791edaafed7
sidebar_position: 3
---

# تخصيص محرك التوجيه {#customize-routing-engine}

في بعض الحالات، قد ترغب في توسيع أو تعديل تجربة التوجيه في OsmAnd، بحيث يمكنك إضافة معلمات إضافية، أو إضافة حواجز إضافية، أو تغيير بعض العقوبات. يرجى إلقاء نظرة على [routing.xml](https://github.com/osmandapp/OsmAnd-resources/blob/master/routing/routing.xml). يستخدم توجيه OsmAnd خوارزمية A* ثنائية الاتجاه تعتمد على أسرع وقت (= المسافة/(السرعة*الأولوية) + العقوبات). إنه تنسيق سهل للغاية. وهو مقسم إلى 7 أقسام (مجموعات التقييم):

* الوصول (1 سماح، -1 عدم سماح)
* السرعة (رقم يمثل السرعة بالكيلومتر في الساعة)
* الأولوية (رقم بين 0 و 1) - مضاعف للسرعة ولا يزال مرتبطًا بالسرعة القصوى، لذلك سيتم استخدام الحد الأدنى (السرعة * المضاعف، السرعة القصوى) لـ A*
* اتجاه واحد (1، -1 أو 0) - يستخدم لتوضيح الوصول بناءً على اتجاه الحركة
* عقوبة_الانتقال (عقوبة بالثواني) - تستخدم لتحديد العقوبة عندما ينتقل المستخدم من طريق عالي الفئة إلى طريق منخفض الفئة. على سبيل المثال، طريق سريع - 10، طريق رئيسي - 15، إذا انتقل المستخدم من طريق سريع إلى طريق رئيسي، ستكون العقوبة 5 ثوانٍ (=10 - 15). سيتم استخدام هذه العقوبة بواسطة خوارزمية A*. لا توجد عقوبة إذا انتقل المستخدم من طريق سريع إلى طريق رئيسي ولا توجد عقوبة إذا استمر المسار من طريق سريع إلى طريق سريع.
* عائق (عقوبة بالثواني) - يحدد العقوبة التي تؤثر على وقت التوجيه
* وقت_العائق (عقوبة بالثواني) - يحدد العقوبة التي تظهر للمستخدم ولكن لا يأخذها محرك التوجيه في الاعتبار، أي وقت_العائق - ساعتان، عائق - دقيقة واحدة، في أقصر مسار سيجد المحرك مسارًا باستخدام عائق دقيقة واحدة ولكن المستخدم سيرى أن وقت المسار هو ساعتان.

لاختبار [routing.xml](https://github.osmandapp/OsmAnd-resources/blob/master/routing/routing.xml)، يمكنك استخدام [OsmAndMapCreator](http://download.osmand.net/latest-night-build/OsmAndMapCreator-main.zip). لاختبار routing.xml على الجهاز، يمكنك ببساطة استبدال routing.xml الافتراضي في المجلد الجذر لـ OsmAnd ببطاقة SD.