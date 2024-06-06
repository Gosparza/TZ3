# TZ3
## Проект приложения для сервиса доставки еды "Не Я.Еда"
В данном сервисе доставки есть такие особенности как: заказ еды без возможности выборы времени доставки, отсутсвие услуги самовывоза, работа при предоплате через приложение(то есть оплата только картой), общение по средствам связи внутри приложения через универсального бота.
### Универсальный бот
Универсальный бот занимается решением проблем в работе приложения со всех сторон пользователей: клиентов, курьеров, ресторана.
Также, для обеспечения безопасности, бот осуществляет связь пользователей одного заказа внутри приложения, с использованием шифрования данных. То есть, при необходимости связаться с тем или иным участником заказа, пользователь пишет соответсвующее обращение через бота, а далее бот предлагает пути связи: звонок, отправка сообщения внутри приложения.
Еще бот умеет решать стандарные вопросы по заказу: уточнение времени доставки, корректировка данных после оформления заказа. Но более индивидуальные вопросы бот решить не в силах, поэтому при поступление запросов от пользователей, не подлежащих обработке, бот перенаправляет запрос в службу поддержки сервиса, которые решают проблему со своей стороны и коммуницируют с пользователями через того же универсального бота.
### Модуль оплаты
Модуль оплаты - это модуль, который проверяет прошла ли оплата от пользователя и не дает оформить заказ в случае неоплаты.
### Отмена заказа
Отмена заказа может проиходить на трех этапах:
1) в момент оплаты - модулем оплаты;
2) в момент сборки заказа в заведении - менеджером по доставке, клиентом;
3) в момент доставки - курьером, клиентом.

При отмене заказа клиентом в момент сборки заказа возвращается полная стоимость, в момент доставки лишь часть - то что идет в оплату услуг ресторана.