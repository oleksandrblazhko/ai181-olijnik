# Перевірка. Оцінка архітектури

## Огляд практики безпеки
Практика оцінки архітектури (AA) гарантує, що застосування та
архітектура інфраструктури адекватно відповідає всім відповідним вимогам безпеки та вимогам відповідності і достатньою мірою пом’якшує виявлені загрози безпеці.
Перший потік зосереджений на перевірці безпеки та відповідності
вимоги, визначені в Політиці, а також відповідність і безпека
Практика вимог виконується, спочатку в певному порядку, потім більше
систематично для кожного інтерфейсу в системі. Другий потік оглядає
архітектури, спочатку для пом’якшення типових загроз, а потім проти
конкретні загрози, виявлені в практиці Оцінки загроз.

У своїй більш просунутій формі практика формалізує архітектуру безпеки
процес перегляду, постійно оцінює ефективність архітектури
засоби контролю безпеки, їх масштабованість і стратегічне узгодження. Ідентифікований
слабкі місця та можливі покращення надсилаються назад до служби безпеки
Практика архітектури для вдосконалення еталонних архітектур.

## Огляд потоків

### Потік A - Перевірка архітектури
Перевірка архітектури підтверджує безпеку програмного забезпечення та підтримки
архітектури шляхом визначення архітектури програми та інфраструктурних
компонентів та перевірки їх забезпечення цілей безпеки та
вимог.

### Потік B - Пом'якшення архітектури
Пом’якшення архітектури зосереджено на тому, щоб усі загрози, виявлені під час
Оцінка загрози були належним чином пом'якшені, і наявні посилання
архітектури, оновлені для вирішення будь-яких необроблених загроз.

## Огляд потоків по рівням зрілості
### Потік A - Перевірка архітектури

#### Рівень зрілості 1

#### Вигода
Розуміння високорівневої архітектури та розумних заходів безпеки

#### Діяльність
Створіть уявлення про загальну архітектуру та перевірте її на правильність
забезпечення загальних механізмів безпеки, таких як автентифікація,
авторизація, керування користувачами та правами, безпечний зв'язок, дані
захист, керування ключами та керування журналами. Також враховуйте підтримку
для конфіденційності. Зробіть це на основі таких артефактів проекту, як архітектура чи дизайн
документи або співбесіди з власниками бізнесу та технічним персоналом. Також
розглянути компоненти інфраструктури - це всі системи,
компоненти та бібліотеки (включаючи SDK), неспецифічні для
програму, але надає пряму підтримку для використання або керування програмами в
організація.

Зверніть увагу на всі пов’язані з безпекою функції в архітектурі та перегляньте їх
правильне забезпечення. Зробіть це в індивідуальному порядку, з точки зору
анонімні користувачі, авторизовані користувачі та конкретні ролі програми.


#### Рівень зрілості 2

#### Вигода
Послідовний процес перевірки архітектури у вашій організації

#### Діяльність
Переконайтеся, що архітектура рішення стосується всіх ідентифікованих засобів безпеки та
вимоги відповідності. Для кожного інтерфейсу в програмі виконайте ітерацію
перелік вимог безпеки та відповідності та аналіз архітектури
для їх забезпечення. Також виконайте аналіз взаємодії або потоку даних, щоб переконатися
що вимоги належним чином враховуються в різних компонентах.
Проведіть аналіз, щоб показати функції рівня дизайну, які стосуються кожного
вимога.

Виконайте цей тип аналізу на обох внутрішніх інтерфейсах, напр. між ярусами, як
а також зовнішні, напр. ті, що складають поверхню атаки. Також ідентифікуйте
і підтвердити важливі дизайнерські рішення, прийняті як частина архітектури, в
зокрема, коли вони відхиляються від доступних спільних рішень безпеки в
організація. Нарешті, оновіть висновки на основі змін, внесених під час
цикл розробки та відзначте будь-які нечіткі вимоги
надається на рівні проектування як результати оцінки.

#### Рівень зрілості 3

#### Вигода
Забезпечення ефективності засобів контролю архітектури

#### Діяльність
Перегляньте ефективність компонентів архітектури та їх надання
механізми безпеки з точки зору узгодження із загальною стратегією
організації та перевірте ступінь доступності, масштабованості та
готовність обраних рішень безпеки. У той час як тактичний вибір для a
конкретне застосування може мати сенс у конкретних контекстах, це важливо
стежте за більшою картиною та переконайтесь у майбутній готовності розробленого
рішення.
Поверніть будь-які висновки в управління дефектами для подальшого запуску
покращення архітектури.

### Потік B - Пом'якшення архітектури

#### Рівень зрілості 1

#### Вигода
Гарантує, що архітектура захищає від типових загроз безпеці.

#### Діяльність
Перегляньте архітектуру на наявність типових загроз безпеці. Технічні знання з безпеки
персонал проводить цей аналіз за допомогою архітекторів, розробників, менеджерів,
і власників бізнесу за потреби, щоб переконатися, що архітектура підходить для всіх
загальні загрози, яким команди розробників не мають спеціалізованої безпеки
експертиза, можливо, пропущена.

Типові загрози в архітектурі можуть бути пов’язані з неправильними припущеннями в або
надмірна залежність від забезпечення механізмів безпеки, таких як
автентифікація, авторизація, керування користувачами та правами, безпечний
зв'язок, захист даних, керування ключами та журналами.
З іншого боку, загрози також можуть стосуватися відомих обмежень або проблем у
технологічні компоненти або каркаси, які є частиною рішення та для
які недостатньо пом'якшують.

#### Рівень зрілості 2

#### Вигода
Усі виявлені загрози програмі обробляються належним чином.

#### Діяльність
Систематично переглядайте кожну загрозу, виявлену під час Оцінки загрози
діяльності та перевірити, як архітектура їх пом’якшує. Використовуйте a
стандартизований процес для аналізу системної архітектури та потоку даних
всередині них. Зазвичай це пов’язано з використовуваною моделлю загроз (наприклад, STRIDE).
щоб визначити відповідні цілі безпеки, які стосуються кожного типу
загроза. Для кожної загрози визначте особливості архітектури на рівні проектування
які протидіють цьому та оцінюють їх ефективність у цьому.

За наявності перегляньте записи архітектурних рішень, щоб зрозуміти
архітектурні обмеження та компроміси, зроблені під час проектування. Приймайте їхній вплив
до уваги разом із будь-якими припущеннями щодо безпеки, на яких базується сейф
функціонування системи покладається і переоцінити їх.

Збагатіть свою раніше створену модель загрози таким чином, щоб кожна загроза і її
оцінений вплив пов’язано з відповідними контрзаходами. Виробляти a
картографічний документ або інформаційну панель у спеціалізованому інструменті, щоб зробити
інформація доступна та видима для відповідних зацікавлених сторін.

#### Рівень зрілості 3

#### Вигода
Постійне вдосконалення архітектури підприємства на основі архітектури
відгуки

#### Діяльність
Як організація ви можете ще більше покращити стан безпеки свого програмного забезпечення
розуміння того, які загрози залишаються невирішеними в програмному забезпеченні
архітектури та адаптації вашої тактики, щоб запобігти цьому. Формалізуйте процес
використовуйте повторювані висновки архітектури як тригер для виявлення причин прогалин у
оцінку безпеки та роботу з ними. Поверніть висновки до дизайну
шляхом створення або оновлення відповідних еталонних архітектур, існуючих
рішення безпеки або принципи та шаблони проектування організації.