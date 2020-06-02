# wapkassa.net-php
Мерчант - интерфейс для приема платежей через интернет. Через единую точку входа он позволяет организовать оплату на Вашем сайте множеством платежных систем. Имеет простой протокол взаимодействия и легкую интеграцию в новый или уже работающий бизнес.  Для начала работы необходимо сделать несколько шагов:  зарегистрироваться на сайте WAPKASSA.NET; добавить и настроить магазин в разделе Магазины; установить на своем сайте HTML-форму для перенаправления на оплату;  Воспользуйтесь API для взаимодействия вашего сервиса с нашей платежной системой

Пример создания формы на языке php

<?php
$data = [
    'shop_id' => 1,
    'payment_id' => 1,
    'amount' => 5,
    'description' => 'Оплата товара',
	/* 'currency' > 1, (1 - QiWi, 2 - Яндекс, 3 - Карты, 4 - PAYEER)*/

];

?>
<form method="POST" action="https://wapkassa.net/oplata.php">
    <input name="shop_id"        value="<?=$data['shop_id']; ?>">
    <input name="payment_id"     value="<?=$data['payment_id'] ?>">
    <input name="amount"      value="<?=$data['amount'] ?>">
    <input name="description" value="<?=$data['description'] ?>">
    <!--  <input name="currency"    value="<?=$data['currency'] ?>">-->

    <button>Оплатить</button>
</form>
