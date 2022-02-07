# What is an API? In English, please.

![What is an API? In English, please.](https://cdn-media-1.freecodecamp.org/images/1*F8R-PEI9iVJ-sY3qFZemCg.png)

**by Petr Gazarov**

قبل أن أبدا تعلم تطوير البرمجيات، اعتقدت أن API هو نوع من الكحوليات.

والآن استخدم هذا المصطلح كثيرا لدرجة أني حاولت أن أطلبه من النادل.

ولكن النادل أعطاني  error 404 .

في حياتي أقابل العديد من الناس، بعضهم يعمل في المجال التقني والبعض الآخر لا، ممن يملكون فكرة خاطئة أو غير مكتملة عن معنى هذا المصطلح الشائع.

تقنيا ً، API هو اختصار لـ  **Application Programming Interface**.  في مرحلة ما أو في أخرى، معظم الشركات الكبيرة تقوم ببناء APIs لعملائهم، أو لتسهيل العمل داخل الشركة

ولكن كيف تشرح  API بالعربية البسيطة؟ وهل هناك معنى أشمل من المعنى المنتشر في بيئات التطوير والأعمال؟ أولاً لنعد خطوة للوراء ونأخذ نظرة عن كيفية عمل الـ Web. 

## WWW and remote servers
عندما أفكر في الـ Web . أتخيل  شبكة عملاقة من الـ servers المتصلة ببعضها البعض.

أي صفحة على الإنترنت مخزنة علىremote server. مصطلح الـ remote server ليس بالغموض الذي يبدوا عليه — هو فقط مجرد جهاز كمبيوتر بعيد تم اعداده ليقدم خدمة معالجة الطلبات بشكل أفضل.

لنضع الأمور في نصابها، يمكنك إعداد server على حاسبك الشخصي وجعله قادر على استضافة موقع كامل على الإنترنت (في الحقيقة، هذه هي الطريقة التي يستخدمها المهندسون لتطوير المواقع قبل إطلاقها للعالم).

عندما تكتب   [www.facebook.com](https://www.facebook.com/) في مستعرض الإنترنت، يرسل المستعرض طلب (Request) إلى الـ remote server الخاص بفيسبوك . وعندما يستقبل المستعرض إستجابة، يقوم بتفسير الكود وعرضه على الصفحة.

بالنسبة للمستعرض - يعرف أيضاً بـ Client- الـ server الخاص بفيسبوك هو API. وهذا يعني أنه في كل مرة تزور صفحة على الإنترنت, تتفاعل مع remote server’s API.

ولكن الـ API ليس هو نفسه الـ remote server—ولكنه فقط **جزء من الـ server مسؤول عن استقبال الطلبات والاستجابة لها** 

## APIs كطريقة لخدمة عملائك
 على الأرجح سمعت عن شركات تقدم APIs كمنتج لها. على سبيل المثال تبيع Weather Underground الوصول لـ  [weather data API](https://www.wunderground.com/weather/api).

**مثال من الواقع**: الموقع الخاص بشركتك  يحتوي على form يستخدم لتسجيل مواعيد للعملاء. و تريد أن تعطي عملائك القدرة على تسجيل الموعد بكل تفاصيله في Google calendar بشكل تلقائي .

**استخدام الـ API**: الفكرة أن تجعل السيرفر الخاص بموقعك يتواصل مع السيرفر الخاص بجوجل عن طريق request لانشاء حدث في Google calendar شامل تفاصيل الموعد. ومن ثم  سيستقبل السيرفر الخاص بك response من جوجل ويعالجها  ثم يقوم بارسال المعلومات المرتبطة بها الى المستعرض، كمثال لهذه المعلومات: ارسال رسالة تأكيد للمستخدم.

كبديل عن ذلك، يمكن أن يقوم المستعرض بارسال API request مباشرة للسيرفر الخاص بجوجل .

**ما الفرق بين  Google Calendar’s API و أي API اخر خاص بأي remote server ؟**

**من منظور تقني**، الفارق يكمن في صياغة (format)  الـ request و الـ response.

لعرض صفحات الويب، يستقبل المستعرض response في شكل HTML، والذي يحتوي على كود يخبره بكيفية عرض الصفحة (presentational code)، ولكن مع Google Calendar’s API سيستقبل فقط بيانات - على الأغلب على شكل JSON.

عندما يقوم السيرفر الخاص بك بارسال API request، فانه يلعب دور الـ Client (مثل ما يفعل المستعرض عادة عند تصفح الويب).

**من منظور المستخدم**، تسمح الـ APIs للمستخدم باكمال مهمة معينة بدون مغادرة الموقع.

أغلب المواقع الحديثة تستخدم بعض الـ third-party APIs.

العديد من المشاكل الآن يمكن إيجاد حلول لها من third-party ، على شكل مكتبة برمجية  أو خدمة. حيث عادة يكون من الأفضل والأضمن استخدام حل موجود ومجرب مسبقا.

أيضا ليس من غير المألوف بالنسبة للمطورين تقسيم تطبيقاتهم على أكثر من سيرفر تتواصل مع بعضها البعض باستخدام APIs . وتسمي السيرفرات التي توفر خدمات مساعدة للتطبيقات الرئيسية   [_microservices_](http://microservices.io/patterns/microservices.html)_._

و كملخص، عندما توفر شركة ما API لعملائها، هذا يعني فقط أنهم أنشأوا مجموعة من عناوين URL المخصصة التي تعرض  بيانات فقط كـ responses  -**أو بمعنى اخر لن يوفر الـ response طريقة لعرض البيانات كما  يوجد دائما في واجهات المستخدم التي يوفرها المستعرض.**

هل يمكن تنفيذ هذه الـ requests باستخدام المستعرض؟ في أغلب الأحوال، نعم حيث أن نقل البيانات باستخدام HTTP يحدث على شكل نصوص، و سيحاول المستعرض دائما عرض هذه البيانات بأفضل طريقة ممكنة.

على سبيل المثال، يمكنك الوصول لـ GitHub’s API باستخدام المستعرض مباشرة حتى بدون الحاجة إلىaccess token. وهذه هي الـJSON response التي ستحصل عليها عندما تحاول الوصول لـ GitHub user’s API route من المستعرض (https://api.github.com/users/petrgazarov): 

```
{  "login": "petrgazarov",  "id": 5581195,  "avatar_url": "https://avatars.githubusercontent.com/u/5581195?v=3",  "gravatar_id": "",  "url": "https://api.github.com/users/petrgazarov",  "html_url": "https://github.com/petrgazarov",  "followers_url": "https://api.github.com/users/petrgazarov/followers",  "following_url": "https://api.github.com/users/petrgazarov/following{/other_user}",  "gists_url": "https://api.github.com/users/petrgazarov/gists{/gist_id}",  "starred_url": "https://api.github.com/users/petrgazarov/starred{/owner}{/repo}",  "subscriptions_url": "https://api.github.com/users/petrgazarov/subscriptions",  "organizations_url": "https://api.github.com/users/petrgazarov/orgs",  "repos_url": "https://api.github.com/users/petrgazarov/repos",  "events_url": "https://api.github.com/users/petrgazarov/events{/privacy}",  "received_events_url": "https://api.github.com/users/petrgazarov/received_events",  "type": "User",  "site_admin": false,  "name": "Petr Gazarov",  "company": "PolicyGenius",  "blog": "http://petrgazarov.com/",  "location": "NYC",  "email": "petrgazarov@gmail.com",  "hireable": null,  "bio": null,  "public_repos": 23,  "public_gists": 0,  "followers": 7,  "following": 14,  "created_at": "2013-10-01T00:33:23Z",  "updated_at": "2016-08-02T05:44:01Z"}
```
يبدوا أن المستعرض قام بعرض هذا الـ response بشكل جيد. كما يبدو امامك هذا الـ response جاهز تماما للاستخدام في الكود. ومن السهل استخراج البيانات منه. وبالتالي يمكنك فعل ما تريد بهذه البيانات

## A is for “Application”
كختام، هيا نلقي نظرة على مثالين آخرين لاستخدام الـ APIs.

مصطلح Application يمكن أن يشير للعديد من الأشياء.فيما يلي بعض منهم في سياق مناقشة الـ API:
1. برمجية معينة تؤدي وظيفة محددة
2. سيرفر كامل، أو تطبيق كامل ، أو جزء صغير من تطبيق.

بشكل أساسي أي برمجية يمكن أن تكون موجودة بشكل منفصل عن بيئتها، يمكن أن تمثل حرف الـ A في كلمة API، وعلى الأرجح ستمتلك هي الآخرى API بشكل أو بآخر.

لنفترض أنك تستخدم في كودك third-party library. بمجرد إدماجها مع كودك  تصبح المكتبة جزء من التطبيق النهائي. ولكن لكونها برمجية منفصلة فغالبا هي تمتلك API تتواصل من خلاله مع بقية الكود.

مثال آخر: في ال **Object Oriented Design**، يتم تنظيم الكود على هيئة objects. عند تصميم تطبيق يمكن أن يحتوي على مئات ال objects التي تتواصل مع بعضها البعض.

كل object يوفر API - مجموعة من الـ methods و الـ properties يستخدمها للتواصل مع باقي الـ objects.

يمكن للـ object أن يملك أيضاinner logic that is private ، مما يعني أنه غير ظاهر للخارج (أو ليس جزء من الـ API).

مما قمنا بتغطيته، أتمنى أن تكون استطعت تكوين صورة شاملة عن معنى مصطلح API بالإضافة الى بعض الاستخدامات الشائعة لهذا المصطلح.

### بعض المصادر المثيرة للاهتمام ( مواضيع لم أقم بتغطيتها ولكن مازالت مهمة):
[A great youtube video on DNS (Domain Name System)](https://www.youtube.com/watch?v=72snZctFFtA&feature=youtu.be)

[HTTP protocol basics](https://simple.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

[An Awesome Khan Academy video on Object Oriented Design Principles](https://www.khanacademy.org/computing/computer-programming/programming/object-oriented/p/object-types#)