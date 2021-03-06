<h1 align="center">Собеседник</h1>

<p align="center">Собеседник: последнее слово в обмене мгновенными сообщениями </p>


## Принципы дизайна

* Быть максимально красивым и простым в использовании без ущерба для безопасности или
  Конфиденциальность
* Положитесь на существующие, хорошо зарекомендовавшие себя протоколы (XMPP)
* Не требуется учетная запись Google или, в частности, Google Cloud Messaging (GCM). 

## Функции

* Сквозное шифрование с помощью [OMEMO] (http://conversations.im/omemo/) или [OpenPGP] (http://openpgp.org/about/)
* Отправлять и получать изображения, а также файлы другого типа
* Зашифрованные аудио- и видеозвонки (DTLS-SRTP)
* Поделитесь своим местоположением
* Отправлять голосовые сообщения
* Индикация, когда ваш контакт прочитал ваше сообщение
* Интуитивно понятный интерфейс, соответствующий рекомендациям по дизайну Android.
* Картинки / аватары для ваших контактов
* Синхронизируется с настольным клиентом
* Конференции (с поддержкой закладок)
* Интеграция адресной книги
* Несколько учетных записей / единый почтовый ящик
* Очень низкое влияние на время автономной работы 

### XMPP Функции

Собеседник работают с каждым XMPP-сервером. Однако XMPP - это
расширяемый протокол. Эти расширения также стандартизированы в так называемых
XEP's. Собеседник поддерживает несколько из них, чтобы пользователь в целом
опыт лучше. Есть вероятность, что ваш текущий сервер XMPP не
поддерживать эти расширения; поэтому, чтобы получить максимальную отдачу от разговоров, вы
следует подумать о переходе на сервер XMPP, который работает, или - что еще лучше -
запустить собственный сервер XMPP для себя и своих друзей. Эти XEP: 

* [XEP-0065: SOCKS5 Bytestreams](http://xmpp.org/extensions/xep-0065.html) (or mod_proxy65). Будет использован для передачи
  файлов, если обе стороны находятся за брандмауэром (NAT). 
* [XEP-0163: Personal Eventing Protocol](http://xmpp.org/extensions/xep-0163.html) для аватарок и OMEMO.
* [XEP-0191: Blocking command](http://xmpp.org/extensions/xep-0191.html) позволяет заносить в черный список спамеров или 
  блокировать контакты, не удаляя их из списка. 
* [XEP-0198: Stream Management](http://xmpp.org/extensions/xep-0198.html) позволяет XMPP выдерживать небольшие перебои 
  в работе сети и изменения базового TCP-соединения .
* [XEP-0280: Message Carbons](http://xmpp.org/extensions/xep-0280.html) который автоматически синхронизирует сообщения, 
  которые вы отправляете своему настольному клиенту, и, таким образом, позволяет вам легко переключаться с мобильного 
  клиента на настольный клиент и обратно в рамках одного разговора. 
* [XEP-0237: Roster Versioning](http://xmpp.org/extensions/xep-0237.html) в основном для экономии полосы пропускания 
  при плохих мобильных соединениях 
* [XEP-0313: Message Archive Management](http://xmpp.org/extensions/xep-0313.html) синхронизировать историю сообщений 
  с сервером. Следите за сообщениями, которые были отправлены, когда беседы были оффлайн.
* [XEP-0352: Client State Indication](http://xmpp.org/extensions/xep-0352.html) позволяет серверу знать, находятся 
  ли разговоры в фоновом режиме. Позволяет серверу экономить полосу пропускания, задерживая неважные пакеты.
* [XEP-0363: HTTP File Upload](http://xmpp.org/extensions/xep-0363.html) позволяет обмениваться файлами в конференциях 
  и с автономными контактами.
## FAQ

### Общие вопросы

#### Как установить приложение "Собеседник"?

Собеседник полностью открытый источник и лицензированы под GPLv3. Так что если вы
разработчик программного обеспечения вы можете проверить источники от GitHub и использовать Gradle, чтобы
построить ваш файл apk.

Более удобный способ - который не только дает возможность автоматического обновления, но и
поддерживает дальнейшее развитие Conversations - это купить приложение в
Google [Play Store](https://play.google.com/store/apps/details?id=eu.siacs.conversations&referrer=utm_source%3Dgithub).

#### Как мне создать учетную запись?
XMPP, как и электронная почта, является федеративным протоколом, что означает, что нет ни одной компании, в которой вы можете создать *официальную учетную запись XMPP*. Вместо этого существуют сотни или даже тысячи провайдеров. Воспользуйтесь поисковой системой по вашему выбору, чтобы найти другого провайдера. Или, может быть, он есть в вашем университете. Или вы можете запустить свою собственную. Или попросите друга запустить его. После того, как вы найдете такого провайдера, вы можете использовать Conversations для создания учетной записи. Просто выберите *register new account* на сервере в диалоге создания учетной записи.

##### Хостинг доменов
Использование собственного домена не только дает вам более узнаваемый Jabber ID, но и позволяет гибко переносить вашу учетную запись между различными XMPP-провайдерами. Это хороший компромисс между ответственностью за работу собственного сервера и недостатками зависимости от одного провайдера.


##### Запуск собственного сервера
Если у вас уже есть где-то сервер, и вы готовы и способны проделать необходимую работу, вы можете запустить свой собственный XMPP-сервер.

С 2019 года мы рекомендуем вам использовать [ejabberd](https://ejabberd.im). Конфигурационный файл по умолчанию уже включает все необходимое для прохождения теста [Conversations Compliance Suite](https://compliance.conversations.im). Убедитесь, что ваш дистрибутив Linux поставляет достаточно свежую версию.

Приложив немного усилий, можно настроить [Prosody](https://prosody.im) на поддержку всех необходимых расширений. Однако вам придется полагаться на так называемые [Community Modules](https://modules.prosody.im/) разного качества. Prosody может быть интересен людям, которые любят модифицировать свой сервер и создавать/прототипировать собственные модули.

С точки зрения производительности - для небольших развертываний - и ejabberd, и Prosody должны быть в порядке. 

#### Где я могу установить пользовательское имя хоста / порт?
Conversations автоматически ищет SRV записи для вашего доменного имени.
которые могут указывать на любую комбинацию имени хоста и порта. Если ваш сервер не предоставляет
эти записи, пожалуйста, свяжитесь с вашим администратором и попросите его прочитать
[это] (http://prosody.im/doc/dns#srv_records). Если оператор вашего сервера не желает
исправить это, вы можете включить расширенные настройки сервера в настройках эксперта в разделе
Разговоры.

#### Я получаю 'Несовместимый сервер'.

Как обычный пользователь вы должны выбрать другой сервер. Выбранный вами сервер
вероятно, небезопасен и/или очень старый.

Если вы являетесь администратором сервера, вы должны убедиться, что ваш сервер обеспечивает
STARTTLS или [XEP-0368: SRV records for XMPP over TLS](https://xmpp.org/extensions/xep-0368.html).

В редких случаях это сообщение об ошибке может быть вызвано тем, что сервер не предоставляет
механизм входа в систему (SASL), который Conversations может обрабатывать. Conversations поддерживает
SCRAM-SHA1, PLAIN, EXTERNAL (клиентские сертификаты) и DIGEST-MD5.

#### Я получаю 'Bind failure'. Что это значит?

Некоторые сбои привязки носят временный характер и устраняются после повторного подключения.

При попытке подключения к OpenFire ошибка привязки может быть постоянной проблемой, когда доменная часть Jabber ID, введенного в Conversations, не совпадает с доменом, за который отвечает сервер OpenFire. Например, OpenFire настроен на использование домена `a.tld`, но Jabber ID введен `user@b.tld`, где `b.tld` также указывает на тот же хост. Во время привязки OpenFire пытается переназначить Jabber на `user@a.tld`. Conversations это не нравится.
Это можно исправить, создав новую учетную запись в Conversations, которая использует Jabber ID `user@a.tld`. 

Примечание: Это довольно странная причуда OpenFire. Большинство других серверов просто выдадут ошибку 'Сервер не отвечает за домен' вместо того, чтобы попытаться переназначить Jabber ID.

Возможно, вы пытались использовать Jabber ID `test@b.tld`, потому что `a.tld` не указывает на правильный хост. В этом случае вам, возможно, придется включить расширенные настройки соединения в экспертных настройках Conversations и задать имя хоста.

#### Я получаю сообщение "Ошибка открытия потока". Что это значит?

В большинстве случаев эта ошибка вызвана тем, что ejabberd рекламирует поддержку TLSv1.3, но не поддерживает ее должным образом. Это может произойти, если версия OpenSSL на сервере уже поддерживает TLSv1.3, но библиотека-обертка fast\_tls, используемая ejabberd, не поддерживает его (должным образом). Обновление fast\_tls и ejabberd или - теоретически - понижение версии OpenSSL должно устранить проблему. Обходным решением является явное отключение поддержки TLSv1.3 в конфигурации ejabberd. Более подробную информацию можно найти на [эта проблема на трекере проблем ejabberd](https://github.com/processone/ejabberd/issues/2614).


#### Я получаю это раздражающее постоянное уведомление.
Начиная с Conversations 2.3.6 выпуски Conversations, распространяемые через Google Play Store, будут отображать постоянное уведомление, если вы используете его на Android 8 и выше. Это правило, которое, по сути, навязывается Google Play Store. (У вас не будет проблемы *принудительного* уведомления на переднем плане, если вы получаете приложение из F-Droid).

Однако вы можете отключить уведомление через настройки операционной системы. (Не настройки в разделе "Разговоры").

** Расход батареи и все поведение Conversations останется прежним (таким же хорошим или плохим, как и раньше). Почему Google так поступает с вами? Мы понятия не имеем.**

##### Android &lt;= 7.1 или Conversations от F-Droid (все версии Android).
Уведомление на переднем плане по-прежнему контролируется через экспертные настройки в Conversations, как это было всегда. Нужно ли его включать, зависит от того, насколько агрессивны нестандартные функции "энергосбережения", встроенные в операционную систему вашего телефона.

##### Android 8.x
Длительно нажмите на постоянное уведомление и отключите этот тип уведомления, передвинув ползунок влево. В результате уведомление исчезнет, но появится другое уведомление (на этот раз созданное самой операционной системой), которое будет жаловаться на то, что "Разговоры" (и другие приложения) расходуют заряд батареи. Начиная с Android 8.1 вы можете снова отключить это уведомление тем же способом, который описан выше.

##### Android 9.0+
Длительно нажмите на постоянное уведомление и нажмите кнопку info `(i)`, чтобы попасть на экран App info. На этом экране выберите пункт "Уведомления". На следующем экране снимите флажок с пункта "Служба переднего плана". 

#### Как работают XEP-0357: Push-уведомления?
Вы должны использовать версию Conversations для Play Store, а ваш сервер должен поддерживать push-уведомления.¹ Поскольку *Google's Firebase Cloud Messaging (FCM)* привязаны API-ключом к определенному приложению, ваш сервер не может инициировать push-сообщение напрямую. Вместо этого ваш сервер отправит push-уведомление на [Conversations App server](https://github.com/iNPUTmice/p2) (управляемый нами), который будет действовать как прокси-сервер и инициирует push-сообщение для вас. Сообщение push, отправленное с нашего сервера App через FCM, не содержит никакой личной информации. Это просто пустое сообщение, которое разбудит ваше устройство и попросит Conversations переподключиться к вашему серверу. Информация, отправляемая с вашего сервера на наш сервер приложений, зависит от конфигурации вашего сервера, но может быть ограничена именем вашей учетной записи. (В любом случае сервер приложений Conversations не будет перенаправлять какую-либо информацию через FCM, даже если ваш сервер отправит эту информацию).

В итоге Google никогда не получит никакой личной информации, кроме того, что *что-то* произошло. (Это даже не обязательно должно быть сообщение, это может быть и какое-то автоматизированное событие). Мы, как оператор сервера приложений, получим только имя вашего аккаунта (без возможности привязать его к вашему конкретному устройству).

Если вы не хотите этого, просто выберите сервер, который не предлагает Push-уведомлений, или создайте Conversations самостоятельно без поддержки push-уведомлений. (Это доступно через gradle build flavor.) Источники Conversations, не являющиеся игровыми магазинами, такие как Amazon App store, также предлагают версию без push-уведомлений. Conversations будет работать как и раньше и поддерживать свое собственное TCP-соединение в фоновом режиме.

Подробное описание того, как ваш сервер, сервер приложений и FCM взаимодействуют друг с другом, вы можете найти в [README](https://github.com/iNPUTmice/p2/blob/master/README.md) сервера приложений Conversations.

 ¹ Если вы используете версию для Play Store, вам **не** нужно запускать собственный сервер приложений. Ваш сервер должен поддерживать только серверную часть [XEP-0357: Push Notifications](http://xmpp.org/extensions/xep-0357.html) и [XEP-0198: Stream Management](https://xmpp.org/extensions/xep-0198.html). Серверные модули prosody называются *mod_cloud_notify* и *mod_smacks*. Серверные модули ejabberd называются *mod_push* и *mod_stream_mgmt*.


#### Но зачем мне нужно постоянное уведомление, если я использую Google Push?
FCM (Google Push) позволяет приложению пробуждаться из *Doze*, что (как следует из названия) является функцией спящего режима операционной системы Android, которая отключает сетевое соединение, а также уменьшает количество раз, когда приложению разрешено пробуждаться (например, для пинга сервера). Приложение может попросить исключить его из режима doze. Не push-варианты приложения (из F-Droid или если сервер не поддерживает его) будут делать это при первом запуске. Таким образом, если вы получаете исключение из *Doze*, или если вам регулярно отправляются push-события, Doze не должен представлять угрозу для нормальной работы Conversatons. Но даже при использовании *Doze* приложение все еще открыто в фоновом режиме (находится в памяти); оно просто ограничено в действиях, которые может выполнять. Conversations необходимо оставаться в памяти для хранения определенного состояния сессии (статус контактов в сети, статус присоединения к групповым чатам, ...). Однако в Android 8 Google снова изменил все это, и теперь приложение, которое хочет оставаться в памяти, должно иметь службу переднего плана, которая видна пользователю через надоедливое уведомление. Но зачем Conversations нужно хранить это состояние? XMPP - это протокол с состоянием, который имеет много информации на каждую сессию; пакеты должны быть подсчитаны, информация о присутствии должна храниться, некоторые функции, такие как Message Carbons, активируются один раз за сессию, MAM catch-up происходит один раз, обнаружение сервиса происходит только один раз; список можно продолжить. Когда Conversations был создан в начале 2014 года, ничто из этого не было проблемой, потому что приложениям просто разрешалось оставаться в памяти. Практически каждый XMPP-клиент хранит эту информацию в памяти, потому что сохранить ее на диске было бы гораздо сложнее. Полная переработка Conversations в 2019 году попытается сделать это и, вероятно, преуспеет, однако это потребует именно этого - полной переделки, которая сейчас неосуществима. Это, кстати, также является причиной того, почему трудно написать XMPP-клиент на iOS. Или, говоря более широко, это также причина, по которой другие протоколы разрабатываются как протоколы без статического состояния (часто основанные на HTTP) или переходят на них; возьмем, к примеру, переход IMAP на [JMAP](https://jmap.io/).

#### Conversations не работает у меня. Где я могу получить помощь?

Вы можете присоединиться к нашей конференц-залу на [`conversations@conference.siacs.eu`](https://conversations.im/j/conversations@conference.siacs.eu).
Многие люди там могут ответить на основные вопросы об использовании
Conversations или могут дать вам советы по запуску вашего собственного XMPP-сервера. Если
вы нашли ошибку или ваше приложение падает, пожалуйста, прочитайте раздел Разработчики / Сообщить об ошибке
раздел этого документа.

#### Мне нужна профессиональная поддержка в работе с Conversations или настройке моего сервера.

Я доступен для найма. Контактную информацию можно найти на [моем сайте](https://gultsch.de).

#### Как работает интеграция адресной книги?

Интеграция адресной книги была разработана для защиты вашей конфиденциальности. Разговоры
не загружает контакты из вашей адресной книги на ваш сервер и не заполняет вашу
ни заполняет адресную книгу ненужными контактами из вашего онлайн-реестра. Если вы вручную
добавить Jabber ID в адресную книгу вашего телефона, Conversations будет использовать имя и
изображение профиля этого контакта. Чтобы облегчить процесс добавления Jabber ID в адресную книгу
в адресную книгу, вы можете нажать на изображение профиля в контакте.
в сведениях о контакте в разделе "Разговоры". Это запустит намерение "добавить в адресную книгу".
с JID в качестве полезной нагрузки. Это не требует от Conversations наличия прав на запись
разрешения на запись в адресную книгу, а также не требует копирования/вставки JID из одного приложения в другое.
JID из одного приложения в другое.

#### Я получаю сообщение 'delivery failed' на свои сообщения.

Если вы получаете сообщения с ошибкой доставки на изображениях, это, вероятно, связано с тем, что получатель потерял
соединение с сетью во время приема. В этом случае вы можете повторить попытку через
позже.

Для текстовых сообщений ответ на ваш вопрос немного сложнее.
Когда вы видите надпись "доставка не удалась" на текстовых сообщениях, это всегда что-то, что
сообщается сервером. Наиболее распространенной причиной этого является то, что
получатель не смог возобновить соединение. Когда клиент теряет соединение на
короткое время, клиент обычно имеет пятиминутное окно, чтобы восстановить соединение.
соединение снова. Когда клиент не может этого сделать, потому что сеть
соединение отсутствует дольше этого времени, все сообщения, отправленные этому клиенту, будут
будут возвращены отправителю, что приведет к ошибке доставки.

Вместо того чтобы возвращать сообщение отправителю, и ejabberd, и prosody имеют возможность
возможность хранить сообщения в автономном хранилище, когда отключившийся клиент является
единственным клиентом. В prosody это доступно с помощью дополнительного модуля под названием
``mod_smacks_offline``. В ejabberd это доступно через некоторые конфигурационные
настройки.

Другие, менее распространенные причины: сообщение, которое вы отправили, не соответствует каким-то
критериям, установленным сервером (слишком большое, слишком много). Другой причиной может быть
что получатель находится в автономном режиме, а сервер не обеспечивает автономное хранение.

Обычно вы можете отличить эти две группы по тому, что
первая происходит всегда через некоторое время, а вторая - почти
мгновенно.

#### Где я могу посмотреть статус моих контактов? Как я могу установить статус или приоритет?

Статусы - это ужасная метрика. Установка их вручную на нужное значение редко
потому что пользователи либо ленивы, либо просто забывают о них. Установка их
автоматически также не дает качественных результатов. Клавиатура или мышь
как индикатор, например, не работает, когда пользователь просто смотрит на
что-то (читает статью, смотрит фильм). Кроме того, автоматическая установка
статуса всегда подразумевает влияние на вашу конфиденциальность (вы уверены, что хотите, чтобы
чтобы все в вашем списке контактов знали, что вы пользовались компьютером в
4 утра").

В прошлом статус использовался для оценки вероятности того, что ваши
сообщения будут прочитаны. Теперь в этом нет необходимости. С помощью маркеров чата
(XEP-0333, поддерживается в Conversations с версии 0.4) у нас есть возможность **знать**
читают ли ваши сообщения или нет.  То же самое можно сказать и о
приоритеты. В прошлом приоритеты использовались (серверами, а не клиентами!)
для направления ваших сообщений одному определенному клиенту. С углеродными сообщениями (XEP-0280,
поддерживается Conversations с версии 0.1) в этом больше нет необходимости. Использование
приоритетов для маршрутизации OTR-сообщений также нецелесообразно, поскольку их нельзя
могут быть изменены на лету. Такие метрики, как последний активный клиент (клиент, который отправил
последнее сообщение) гораздо лучше.

К сожалению, эти современные замены унаследованных функций XMPP не получили широкого распространения.
приняты. Однако Conversations должен быть мессенджером для будущего и
Вместо того, чтобы делать Conversations совместимым с прошлым, мы должны работать над тем, чтобы
внедрением новых, улучшенных технологий и внедрением их в другие клиенты XMPP
также.

Сделать эти статус и приоритет необязательными - тоже не решение, потому что
Conversations пытается избавиться от старых моделей поведения и показать пример для
другим клиентам.

#### Переводы
Переводы осуществляются на [Transifex](https://www.transifex.com/projects/p/conversations/).
Если вы хотите стать переводчиком, пожалуйста, зарегистрируйтесь на transifex, подайте заявку на вступление в
команду переводчиков, а затем зайдите в наш групповой чат на
[conversations@conference.siacs.eu](https://conversations.im/j/conversations@conference.siacs.eu)
и представьтесь `iNPUTmice`, чтобы он мог одобрить вашу заявку на вступление.

#### Как сделать резервную копию / перенести Conversations на новое устройство?
С одной стороны, Conversations поддерживает управление архивом сообщений для хранения истории ваших сообщений на стороне сервера, поэтому при переносе на новое устройство оно может отображать всю историю ваших сообщений. Однако это не работает, если вы включите OMEMO из-за его прямой секретности. (Прочитайте [The State of Mobile XMPP in 2016](https://gultsch.de/xmpp_2016.html), особенно раздел о шифровании).

Начиная с версии 2.4.0 в этом поможет встроенная функция резервного копирования и восстановления, перейдите в Настройки и найдите настройку "Создать резервную копию". В процессе создания появится уведомление, которое сообщит вам, когда все будет готово. После создания файлов, по одному для каждой учетной записи, вы можете переместить папку **Conversations** *(если вам нужны и старые медиафайлы)* или только папку **Conversations/Backup** *(только для ключей OMEMO и истории)* на новое устройство (или в место хранения), где свежеустановленный Conversations сможет восстановить каждую учетную запись. Не забудьте включить учетные записи после успешного восстановления.

Этот метод резервного копирования будет включать ваши ключи OMEMO. В силу принципа прямой секретности вы не сможете восстановить сообщения, отправленные и полученные между созданием резервной копии и ее восстановлением. Если у вас есть архив на стороне сервера (MAM), эти сообщения будут восстановлены, но отображены как *невозможно расшифровать*. По техническим причинам вы также можете потерять первое сообщение, которое вы отправили или получили после восстановления; для каждого разговора. Это сообщение также будет отображаться как *невозможно расшифровать*, но оно автоматически восстановится, если оба участника находятся на Conversations 2.3.11+. Обратите внимание, что этого не произойдет, если вы только что перешли на новый телефон, и между резервным копированием и восстановлением не было обмена сообщениями.

В подавляющем, подавляющем большинстве случаев вам не придется вручную удалять ключи OMEMO или делать что-либо подобное. Conversations представила официальную функцию резервного копирования только в версии 2.4.0 после того, как убедилась, что механизм *самовосстановления OMEMO*, представленный в версии 2.3.11, работает нормально.

**ПРЕДУПРЕЖДЕНИЕ**: Убедитесь, что вы знаете пароли своих учетных записей или нашли способ сбросить их **до** создания резервной копии, поскольку файлы шифруются с помощью этих паролей, и процесс восстановления будет запрашивать их.  
**ПРЕДУПРЕЖДЕНИЕ**: Не используйте функцию восстановления резервной копии для клонирования (одновременного запуска) установки. Восстановление резервной копии предназначено только для миграции или в случае потери оригинального устройства.

#### Conversations не хватает определенной функции.

Я открыт для предложений по новым функциям. Вы можете воспользоваться трекером [issue tracker][issues] на
GitHub.  Пожалуйста, потратьте немного времени на просмотр проблем, чтобы увидеть, не предлагал ли кто-то
уже предлагал это. Будьте уверены, что я читаю каждый билет. Если мне
понравится, я оставлю его открытым, пока он не будет реализован. Если мне это не нравится, я
закрою его (обычно с коротким комментарием). Если я не комментирую
это, вероятно, хороший знак, потому что это означает, что я согласен с вами.
Комментарии с +1 к открытым или закрытым вопросам не изменят моего мнения и не ускорят разработку.
не ускорит разработку.

#### Вы закрыли мой запрос на функцию, но я очень сильно этого хочу.

Просто напишите его сами и отправьте мне запрос на исправление. Если он мне понравится, я с радостью
если нет, по крайней мере, вы и другие единомышленники смогут им воспользоваться.

#### Мне нужна функция, и мне нужна она сейчас!

Я доступен для найма. Контактная информация на [моем сайте](https://gultsch.de).

### Безопасность

#### Почему существует два метода сквозного шифрования и какой из них выбрать?

* OMEMO работает даже тогда, когда контакт находится в автономном режиме, и работает с несколькими устройствами. Он также позволяет асинхронную передачу файлов, если на сервере есть [HTTP File Upload](http://xmpp.org/extensions/xep-0363.html). Однако OMEMO не имеет широкой поддержки и в настоящее время реализован только [горсткой клиентов](https://omemo.top).
* OpenPGP (XEP-0027) - это очень старый метод шифрования, который имеет некоторые преимущества перед OMEMO, но должен использоваться только людьми, которые знают, что они делают.

#### Как использовать OpenPGP

Прежде чем продолжить чтение, вы должны отметить, что поддержка OpenPGP в
Conversations является экспериментальной. Это не потому, что это сделает приложение нестабильным.
а потому, что фундаментальные концепции PGP еще не готовы к широкому использованию.
Принцип работы PGP заключается в том, что вы доверяете идентификаторам ключей, а не JID или адресам электронной почты.
Поэтому теоретически ваш список контактов должен состоять из идентификаторов открытых ключей, а не из JID.
JID. Но, конечно, ни один почтовый или XMPP-клиент не реализует эти концепции.
концепции. Кроме того, PGP в контексте обмена мгновенными сообщениями имеет несколько
недостатков: Он уязвим для атак повторного воспроизведения и довольно многословен.

Чтобы использовать OpenPGP, необходимо установить приложение с открытым исходным кодом
[OpenKeychain](http://www.openkeychain.org), а затем долго нажимать на учетную запись в разделе
manage accounts и в контекстном меню выбрать renew PGP announcement.

#### OMEMO выделен серым цветом. Что делать?
OMEMO доступен только в чатах 1:1 и частных (только для участников, не анонимных) групповых чатах. Шифрование публичных групповых чатов практически не имеет смысла, поскольку любой (включая гипотетического злоумышленника) может присоединиться к ним, а пользователь в любом случае не сможет проверить всех участников. Более того, для многих публичных групповых чатов желательно предоставить новым участникам доступ к полной истории.

#### OMEMO не работает. Я получаю сообщение "Что-то пошло не так" на экране "Trust OMEMO Fingerprints".
У OMEMO есть два требования: Ваш сервер и сервер вашего контакта должны поддерживать PEP. Вы оба можете проверить это индивидуально, открыв данные вашей учетной записи и выбрав в меню ``Server info``. В появившейся таблице должно быть указано, что PEP доступен. Второе требование заключается в том, что первоначальный отправитель должен иметь доступ к опубликованному ключевому материалу. Этого можно достичь либо путем взаимной подписки на присутствие (вы можете проверить это, открыв контактные данные и посмотрев, установлены ли оба флажка *Отправлять обновления присутствия* и *Получать обновления присутствия*), либо с помощью сервера, который делает материал открытого ключа доступным для всех. В [Compliance Tester](https://compliance.conversations.im) на это указывает функция 'OMEMO'. Поскольку очень часто первые сообщения обмениваются *до* добавления друг друга в список контактов, желательно использовать серверы с поддержкой 'OMEMO'.

#### Как работает шифрование групповых чатов?

##### OMEMO

Шифрование OMEMO работает только в закрытых (только для участников) неанонимных конференциях. Неанонимность (возможность узнать реальный JID других участников) - это техническое требование для открытия ключевого материала. Только для участников - это своего рода произвольное требование, навязанное Conversations. (см. "OMEMO выделено серым цветом").

Серверы всех участников должны пройти OMEMO [Compliance Test](https://conversations.im/compliance/).
Другими словами, они должны работать либо под управлением ejabberd 18.01+, либо Prosody 0.11+.

(В качестве альтернативы это также будет работать, если все участники имеют друг друга в списке контактов; но это редко случается в больших групповых чатах).

Владелец конференции может сделать публичную конференцию приватной, зайдя в раздел
подробности и нажать кнопку настроек (та, что с шестеренками) и выбрать *частная* и
*только для участников*.

##### OpenPGP

Каждый участник должен объявить свой ключ OpenPGP (см. ответ выше).
Если вы хотите отправлять зашифрованные сообщения в конференции, вы должны убедиться, что
убедиться, что у вас есть открытый ключ каждого участника в вашем OpenKeychain.
Сейчас в Conversations нет проверки, чтобы убедиться в этом.
Вы должны позаботиться об этом сами. Перейдите к деталям конференции и
коснитесь идентификатора каждого ключа (шестнадцатеричное число под контактом). Это отправит вас
в OpenKeychain, который поможет вам добавить ключ.  Это лучше всего работает в
очень маленьких конференциях с контактами, с которыми вы уже используете OpenPGP. Этот
функция считается экспериментальной. Conversations - единственный клиент, который использует
XEP-0027 в конференциях. (XEP специально не разрешает и не запрещает
это.)

#### Что такое слепое доверие до верификации / почему сообщения помечаются красным замком?

Подробнее об этой концепции читайте на https://gultsch.de/trust.html.

#### Что случилось с поддержкой OTR?
OTR был удален, потому что он был очень ненадежным. Он не работал с несколькими устройствами и никогда не был предназначен для работы с XMPP. Кодовая база была беспорядочной (там был парсер HTML, чтобы справиться с мусором, который посылали некоторые клиенты OTR). Верификация была реализована неблокирующим способом. Она сообщала вам, если текущая сессия использует неизвестный отпечаток пальца, но не останавливала отправку сообщений до тех пор, пока вы не подтвердите новый отпечаток. (Как Conversations делает сейчас с BTBV после подтверждения или когда BTBV выключен). Учитывая предыдущие пункты, с моей точки зрения, не было практически никакого желания исправлять эту потенциальную проблему безопасности или чистить кодовую базу. Другой причиной удаления было то, что люди будут использовать его *случайно* даже для общения между двумя клиентами Conversations, потому что они где-то прочитали, что OTR хорош.

### Какие клиенты я использую на других платформах
Существуют клиенты XMPP для всех основных платформ.
#### Windows / Linux
Для вашего настольного компьютера мы рекомендуем использовать [Gajim](https://gajim.org). Вам необходимо установить плагины `OMEMO`, `HTTP Upload` и `URL image preview` для наилучшей совместимости с Conversations. Плагины можно установить из приложения.
#### iOS
К сожалению, сейчас у нас нет рекомендаций для iPhone. Существует три клиента [Siskin](https://siskin.im/), [ChatSecure](https://chatsecure.org/) и [Monal](https://monal.im/). Каждый из них имеет свои плюсы и минусы.


### Разработка

<a name="beta"></a>
#### Бета-тестирование
Если вы купили приложение на [Google Play](https://play.google.com/store/apps/details?id=eu.siacs.conversations)
вы можете получить доступ к последней бета-версии, зарегистрировавшись по [этой ссылке](https://play.google.com/apps/testing/eu.siacs.conversations).

#### Как создать Разговоры

**Примечание:** Начиная с версии 2.8.0 вам потребуется скомпилировать libwebrtc.
[Инструкции](https://webrtc.github.io/webrtc-org/native-code/android/) можно найти на сайте WebRTC
сайте. Поместите полученный libwebrtc.aar в каталог `libs/`. Релиз PlayStore в настоящее время
использует стабильный релиз M90 и переименовал имя файла в `libwebrtc-m90.aar`, но потенциально вы можете ссылаться на любое имя файла, изменив `libwebrtc-m90.aar`.
ссылаться на любое имя файла, изменив `build.gradle`.

Убедитесь, что ANDROID_HOME указывает на ваш Android SDK. Используйте Android SDK Manager для установки недостающих зависимостей.

    git clone https://github.com/inputmice/Conversations.git
    cd Conversations
    ./gradlew assembleConversationsFreeSystemDebug

Доступны два варианта сборки. *free* и *playstore*. Если вы не знаете, что делаете, вам нужен только *free*.


[![Статус сборки](https://travis-ci.org/inputmice/Conversations.svg?branch=development)](https://travis-ci.org/inputmice/Conversations)

#### Как отлаживать Беседы

Если что-то идет не так, Conversations обычно выдает очень мало информации в
пользовательском интерфейсе (кроме того факта, что что-то не работает). Однако с помощью adb
(мост отладки android) вы можете извлечь больше информации из Разговоров.
Эта информация особенно полезна, если у вас возникли проблемы с
с подключением или с передачей файлов.

Для использования adb необходимо подключить мобильный телефон к компьютеру с помощью USB-кабеля
и установить `adb`. Большинство систем Linux имеют готовые пакеты для этого инструмента. На
Debian/Ubuntu, например, он называется `android-tools-adb`.

Кроме того, вам, возможно, придется включить "Отладку USB" в опциях разработчика вашего
телефона. После этого вы можете просто выполнить следующие действия на компьютере:

    adb -d logcat -v time -s conversations

При необходимости в PlayStore также есть несколько приложений, которые можно использовать для отображения logcat
прямо на вашем телефоне с рутом. (Поиск logcat). Однако для дальнейшей обработки
(например, для создания проблемы здесь на Github) удобнее просто использовать ПК.

#### Я нашел ошибку.

Пожалуйста, сообщите об этом в наш [issue tracker][issues]. Если ваше приложение падает, пожалуйста
предоставьте трассировку стека. Если вы столкнулись с неправильным поведением, пожалуйста, предоставьте
подробные шаги для воспроизведения. Всегда указывайте, используете ли вы последнюю
Play Store или текущую версию HEAD. Если у вас возникли проблемы с подключением к
XMPP-сервером или передача файлов не работает, как ожидалось, пожалуйста, всегда
приложите отладочный вывод logcat к вашей проблеме (см. выше).

[issues]: https://github.com/inputmice/Conversations/issues
