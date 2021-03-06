# ~ Payment System Unitpay ~

![screen1](https://github.com/LexaCoronos/PaymentSystemUnitpay/blob/main/img/Unitpay.png)

**Краткое описание:** Платёжная система для осуществления онлайн платежей через интернет-кассу Unitpay. Предназначена для российских интернет-магазинов.

**Категория:** Платёжные системы.

-----------------------------------

🔻 Какие возможности и принцип работы:

✅ Система интегрирована в платформу Telegram ботов. В качестве приёма платежей выступает касса **Unitpay**. Для работы системы с интернет-кассой и обработки платежей используется **Unitpay API**.

Данная платёжная система состоит из генератора платежей, системы обработки платежей и менеджера по выдачи товаров. Используется связка языков программирования для работы системы.

   - **Генератор платежей** – это менеджер по созданию заказа, который собирает нужную информацию и формирует заказ.
После создания заказа, менеджер выдаёт клиенту ссылку на оплату.

   - **Система обработки платежей** — это обработчик платежей, который принимает запросы от кассы и меняет статус заказов в базе данных на соответствующий им в данный момент.

   - **Менеджер по выдачи товаров** — это менеджер по обработке заказов, который проверяет статус платежей и при нахождении нового успешно оплаченного заказа получает информацию по платежу и выдаёт товар клиенту.

Как правило, генератор платежей и менеджер по выдачи товаров встроены в сервис и написаны на том же языке, что и сам сервис — **Java**.
Система обработки платежей написана на языке **PHP**, так как эта система работает как веб-сервис и отвечает за принятие **HTTPS** запросов.

Все запросы имеют шифрование **MD5** и данная информация дополняется контрольной подписью **HMAC_MD5** для безопасности проведения платежей.

-----------------------------------

Пример генерации платежа и направление клиента на онлайн-кассу для оплаты.
![screen2](https://github.com/LexaCoronos/PaymentSystemUnitpay/blob/main/img/PaymentCreator.png)
![screen2](https://github.com/LexaCoronos/PaymentSystemUnitpay/blob/main/img/paying.png)

-----------------------------------

Вся платёжная система, генератор платежей, система обработки платежей и менеджера по выдачи товаров написаны вручную и заточены под конкретную целевую задачу.

