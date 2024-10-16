Портал «Работа России»
# **О портале**
Работа России — федеральная государственная информационная система, проект Федеральной службы по труду и занятости.

Портал помогает гражданам найти работу, а работодателям – сотрудников. Все услуги портала предоставляются бесплатно.

Портал обеспечивает:

- Бесплатное использование
- Отсутствие рекламы
- Перспективные стажировки и практики для студентов
- Надёжные работодатели и вакансии, проверенные службой занятости

  На портале собираются вакансии:

- От работодателей, проверенных либо центрами занятости, либо с помощью средств криптографической защиты информации.
- От крупнейших коммерческих порталов по поиску работы и сотрудников.
# **Постановка задачи**
  Основная задача заключается в разработке и реализации системы, которая обеспечит безопасность всех взаимодействий пользователей с порталом. Это включает в себя как защиту личной информации пользователей, так и безопасность данных о вакансиях и работодателях.

  **Цели**

1. Обеспечение безопасности передачи данных – подразумевает защиту личной информации пользователей и данных о вакансиях во время их передачи по сети.
1. Предоставление уникальных данных для каждой сессии - каждая сессия пользователя должна иметь уникальный идентификатор для предотвращения подделки или повторного использования сессий.
1. Обеспечение конфиденциальности данных - защита информации о пользователях и работодателях от несанкционированного доступа.
1. Целостность данных - гарантия, что информация о вакансиях и резюме не была изменена в процессе передачи.

  **Предположения безопасности**

1. Пользователи будут использовать надежные пароли и менять их регулярно.
1. Все данные передаются через защищенные каналы связи (например, HTTPS).
1. Система имеет механизмы обнаружения и предотвращения попыток несанкционированного доступа (например, системы IDS/IPS).

**Компоненты портала:**

Веб-сервис. 

- Обеспечивает функционал поиска работы и размещения вакансий через интерфейс для пользователей. 
- Реализует бизнес-логику, связанную с обработкой запросов.

Мобильное приложение - предоставляет доступ к функционалу портала через мобильные устройства, позволяя пользователям удобно находить вакансии и управлять своими резюме.

Модуль безопасности контроля авторизаций - отвечает за безопасную аутентификацию пользователей с использованием многофакторной авторизации, включая OTP и другие методы.
one time password, OTP) — это пароль, действительный только для одного сеанса аутентификации.

Модуль обработки вакансий - позволяет работодателям добавлять, редактировать и удалять вакансии, обеспечивая их проверку и соответствие критериям безопасности.

Модуль обработки резюме - управляет загрузкой и обработкой резюме, позволяя пользователям легко обновлять свои данные и работодателям находить подходящих кандидатов.

Центр мониторинга безопасности - слежение за действиями пользователей на портале для выявления и предотвращения потенциальных угроз безопасности.

База данных вакансий и резюме - обеспечивает хранение и защиту всех данных с использованием шифрования и технологий защиты от несанкционированного доступа.

API для интеграции с внешними системами - позволяет взаимодействовать с другими платформами, чтобы расширить функционал портала и увеличить доступность вакансий.

Модуль уведомлений - отправляет пользователям уведомления о новых вакансиях и изменениях статуса их резюме, поддерживая высокий уровень вовлеченности.

Модуль аналитики - собирает и анализирует данные о взаимодействии пользователей с порталом, что позволяет улучшать качество предоставляемых услуг и адаптировать функционал под потребности пользователей.
  # Алгоритм работы сайта
1. Регистрация. Пользователь начинает процесс регистрации на портале Работа России через госуслуги, используя свой аккаунт на государственном портале.
2. Портал направляет запрос на аутентификацию в Госуслуги. Пользователь вводит свои учетные данные на портале Госуслуги.
3. После успешной аутентификации Госуслуги возвращают необходимые данные о пользователе.
4. Портал Работа России создает учетную запись для пользователя на основе полученной информации и отправляет уведомление об успешной регистрации.
5. Пользователь получает доступ к основным функциям портала, включая возможность создания резюме, откликов на вакансии и получения уведомлений о событиях (например, приглашениях на собеседования).
6. Управление резюме и откликами:
- Пользователь создает резюме и сохраняет его в системе.
- Система отслеживает просмотры резюме и отклики на вакансии, информируя пользователя о соответствующих событиях.
- Запросы и уведомления:
- Пользователь может отправлять заявки на вакансии, а также просматривать отклики и приглашения.
- Система уведомляет пользователя о новых собеседованиях, откликах на его резюме и других событиях.
7. Раздел для студентов - пользователи-студенты могут получить доступ к специальному разделу, где представлены предложения по прохождению практики и стажировок на предприятиях.

   Запросы на стажировки и практики:

- Студенты могут просматривать доступные программы стажировок и подавать заявки.
- Портал предоставляет информацию о целевом обучении, включая возможность заключения договоров между абитуриентами и организациями.
8. Пользователь может настроить автопоиск вакансий, основываясь на своих предпочтениях. 
9. Обработка жалоб и сообщений - пользователь может подавать жалобы или сообщения, которые обрабатываются службой поддержки портала. Система ведет учет всех жалоб и действий по ним.
10. Сбор метрических данных и составление рекомендаций:
- Портал собирает метрические данные о взаимодействии пользователя с сервисом (например, количество просмотров резюме, откликов и т.д.).
- На основе этих данных формируются рекомендации по улучшению профиля и повышению шансов на трудоустройство.
  # Угрозы безопасности сайта по списку OWASP

  |**Тип Уязвимости**|**Риск**|**Количество**|**% от общего**|
  | :- | :- | :- | :- |
  |Раскрытие PII|Высокий|2274|7106,2|
  |CSP: script-src unsafe-eval|Средний|17|53,1|
  |CSP: style-src небезопасный встроенный|Средний|17|53,1|
  |CSP: Директива подстановочного знака|Средний|17|53,1|
  |Заголовок Content Security Policy (CSP) не задан|Средний|1696|5300,0|
  |Междоменная неправильная конфигурация|Средний|11|34,4|
  |Отсутствует заголовок для защиты от кликджекинга|Средний|10|31,2|
  |Отсутствуют токены против CSRF атак|Средний|3|9,4|
  |Параметр X-Frame-Options искажен|Средний|564|1762,5|
  |Уязвимость JS Библиотеки|Средний|10|31,2|
  |CSP: Уведомления|Низкий|17|53,1|
  |Cookie No HttpOnly Flag|Низкий|2308|7212,5|
  |Cookie без атрибута SameSite|Низкий|2289|7153,1|
  |Cookie с атрибутом SameSite нет|Низкий|43|134,4|
  |Включение исходного файла междоменного JavaScript|Низкий|193|603,1|
  |Заголовок Strict-Transport-Security не установлен|Низкий|675|2109,4|
  |Заголовок X-Content-Type-Options отсутствует|Низкий|756|2362,5|
  |Множественные записи заголовков Strict-Transport-Security|Низкий|638|1993,8|
  |Раскрытие информации - сообщения об ошибках отладки|Низкий|1|3,1|
  |Раскрытие отметки времени - Unix|Низкий|488|1525,0|
  |Раскрытие ошибок приложения|Низкий|11|34,4|
  |Сервер утечка информации о версии через поле заголовка HTTP-ответа|Низкий|2|6,2|
  |Cookie с произвольным ограничением|Информационный|95|296,9|
  |Session Management Response Identified|Информационный|1248|3900,0|
  |Атрибут элемента HTML, управляемый пользователем (потенциальный XSS)|Информационный|136|425,0|
  |Кодировка, управляемая пользователем|Информационный|1|3,1|
  |Обнаружен заголовок только для отчетов политики безопасности содержимого (CSP)|Информационный|564|1762,5|
  |Пересмотрите директивы управления кэшем|Информационный|97|303,1|
  |Получено из кеша|Информационный|12|37,5|
  |Раскрытие информации - конфиденциальная информация в URL|Информационный|17|53,1|
  |Раскрытие информации - подозрительные комментарии|Информационный|1519|4746,9|
  |Современное веб-приложение|Информационный|1143|3571,9|

  Выводы:

1. Высокий риск раскрытия PII: значительное количество уязвимостей, связанных с раскрытием персональной информации, требует немедленного внимания и исправлений.
1. Недостатки в CSP: множество проблем, связанных с Content Security Policy, указывает на необходимость улучшения защиты от атак через скрипты и стили.
1. Куки без защиты: высокое количество куки без HttpOnly и SameSite атрибутов представляет собой серьезный риск для безопасности.
1. Ошибки конфигурации заголовков: отсутствие критически важных заголовков, таких как X-Content-Type-Options и Strict-Transport-Security, ставит под угрозу защиту данных пользователей.
1. Хотя многие проблемы отмечены как информационные, такие как раскрытие ошибок и подозрительных комментариев, они могут также предоставить злоумышленникам дополнительные данные для атак.
1. Рекомендуется проводить регулярные аудиты безопасности для выявления и исправления уязвимостей, особенно в свете высокой общей активности в области безопасности на сайте.
   # Рекомендации по повышению безопасности сайта
   Для повышения безопасности сайта "Портал Работа в России" можно применить следующие методы и практики:

   1\. Защита личных данных (PII)

- использовать HTTPS для защиты данных при передаче.
- собирать только необходимую информацию и удалять ненужные данные.

  2\. Content Security Policy (CSP)

- настройка CSP: внедрить строгую политику CSP, ограничивающую источники скриптов и стилей.
- избегать unsafe-eval и inline-скриптов, это уменьшит риск XSS-атак.

  3\. Защита куки

- установить куки с флагами HttpOnly и Secure для защиты от XSS.
- использовать атрибут SameSite для защиты от CSRF атак.

  4\. Защита от кликджекинга

- X-Frame-Options: установить заголовок X-Frame-Options, чтобы предотвратить отображение сайта в iframe на других доменах.
- Content Security Policy: включить директиву frame-ancestors для контроля того, какие сайты могут отображать ваш контент.

  5\. Защита от CSRF

- Токены CSRF: использовать уникальные токены для форм и запросов, чтобы предотвратить атаки на подделку запросов.

  6\. Регулярные обновления

- Регулярно обновлять библиотеки и фреймворки для устранения известных уязвимостей.
- Использовать инструменты для автоматического мониторинга уязвимостей в используемых библиотеках.

  7\. Защита заголовков

- Включить заголовки, такие как X-Content-Type-Options, Strict-Transport-Security и X-XSS-Protection.

  8\. Управление ошибками

- Убедиться, что сообщения об ошибках не раскрывают конфиденциальную информацию.
- Записывать ошибки и подозрительные действия для последующего анализа (логирование).

  9\. Тестирование и аудит безопасности

- Периодически проводить аудит безопасности для выявления уязвимостей.
- Применять сканеры безопасности для выявления слабых мест.

  10\. Обучение и повышение осведомленности

- Проводить тренинги по безопасности для всех сотрудников, работающих с системой.

  # Заключение
В целом, портал "Работа России" представляет собой полезный инструмент для пользователей и работодателей. Однако, для повышения уровня безопасности и защиты данных, необходимо предпринять дополнительные меры и проводить регулярные аудиты системы. Это позволит не только защитить личную информацию пользователей, но и укрепить доверие к платформе в целом.

  # Список используемой литературы
- https://habr.com/ru/companies/simplepay/articles/258499/
- https://owasp.org/Top10/
- https://cwe.mitre.org/
- https://github.com/carlosdg/NginxReverseProxyWithModsecurity
- https://habr.com/ru/companies/first/articles/709586/
