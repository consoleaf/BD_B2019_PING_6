# Задание 1. Онлайн-аукцион.

## 1. Функциональные требования
Сервис будет использоваться как для покупки, так и для продажи товаров, поэтому требуется сущность "*пользователь*", у которого есть возможность делать ставки на выставленные другими пользователями лоты и выставлять свои на продажу. У пользователей должна быть возможность просмотреть списки всех товаров доступных для покупки на момент запроса, пользователей и последних на момент запроса ставок на каждый лот. Дополнительно потребуются сущности "*лот*", "*ставка*". 
Выставление лота подразумевает внесение пользователем описание товара, начальной цены и дедлайн приема ставок (можно еще время начала проведения аукциона для отложенных лотов). 
Ставки от пользователей подразумевают предложение о покупке товара от пользователя, который не является продавцом данного товара, по цене большей предыдущей ставки или начального лота, если ставок еще не было, на величину, заранее выбранную пользователем-продавцом (некая дельта) или выбранную пользователем-покупателем.
После заврешения аукциона лот должен поменять состояние на "не в продаже", пользователю-продавцу должны придти контактные данные "победителя" аукциона для обсуждения оплаты и отправки, если что-то пойдет не так с покупателем (при подтверждении с обеих сторон), должна быть возможность перейти к следующему участнику торгов, предложившему вторую наибольшую цену (итд).
## 2. Роли пользователей
1 пользователь: "Пользователь"
Данная роль должна иметь доступ на чтение (всех) и внесение данных (своих) о ставках, чтение (всех), внесение и редактирование (своих)  данных о ползьователях, чтение (всех), внесение (своих) и редактирование (своих) данных о товарах.
## 3. Объекты
* Пользователи
* Товары (лоты)
* Ставки
## 4. Связи между объектами 
У одного пользователя может быть много товаров (продавец)
У одного пользователя может быть много ставок (покупатель)
У одного товара может быть много ставок
У одного товара может быть один продавец
У одной ставки может быть один пользователь 
У одной ставки может быть один товар 
## 5. Схема 
рядом лежит (схема довольно абстрактная, не добавил все поля в таблицы, которые скорее всего на самом деле понадобятся)
  
