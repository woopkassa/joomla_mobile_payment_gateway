# joomla_mobile_payment_gateway
Woopkassa mobile payment gateway for Joomla CMS as a module.
## Требрвания и установка
1. Необходима установленная и настроенная платформа [VirtueMart](https://virtuemart.net/downloads)
2. Настройка в Virtuemart параметров валюты (Currencies), оставляем только тенге (KZT)
3. Заходим в VirtueMart -> Shop -> Shop, выбираем пункт Vendor и ставим значение Currncy = Kazakhstani tenge
4. Переходим на вкладку Расширения -> Менеджер расширений, выбираем пункт установка и выбираем необходимый нам модуль
5. Возвращаемся в VirtueMart и выбираем пункт Payment Methods, удаляем все ненужные методы и создаем свой
6. Указываем ему название и обязательно выбираем один из двух пунктов в зависимости от того что мы хотим добавить VM Payment - Wooppay Mobile/VM Payment - Wooppay. Нажимаем кнопку сохранить.
7. После того как метод сохранен мы можем его настроить, выбираем пункт Configuration и заполняем его в соответствии с вашими данными
### Пример:
```
Инфраструктура: Тестовый сервер
Логин: test_merch
Пароль: A12345678a
Префикс заказа: mobile
Имя сервиса: test_merch_invoice
```
Для работы модуля мобильной оплаты необходимо создать дополнительной поле в разделе заказа и выполнить следующие пункты:
8. Переходим в VirtueMart->Configuration->Shopper Fields
9. Создаем новое поле
10. Field name = wooppay_auth_code
11. Field title, по желанию но чтобы он отражал смысл поля
12. Из дополнительных параметров в положение "Да" мы переводим только Show in cart form и Published
13. Теперь если пользователь выберет в заказе мобильную оплату - после первого подтверждения на номер который он указал вышлется
смс с кодом подтверждения, как только он введет его в это поле сумма заказа спишется с его баланса
14. Можно работать

