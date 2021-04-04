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
