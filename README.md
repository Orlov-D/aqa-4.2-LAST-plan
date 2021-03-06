# План тестирования возможности записи на обучение профессии "Тестировщик ПО".

В связи с тем, что необходимо протестировать отдельную часть функционала сайта Нетология достаточно будет использовать модульное тестирование. А именно, автоматизировать возможность записи на курс Тестировщик ПО. Это будет проверка функциональная проверка пользовательского интерфейса.

## Автоматизируемые сценарии.

Автоматизированные сценарии включают в себя открытие страницы профессии "Тестировщик ПО". Добраться до странички профессии возможно несколькими способами:
* нажав на картинку НЕО для начинающих и выбором профессии Тестировщик ПО
* через выпадающие меню Каталог курсов - Программирование - Тестировщик ПО
* через выпадающие меню Каталог курсов - Полный каталог

На самой страничке профессии есть несколько способов записи на курс.
Функциональные тесты будут включать в себя как позитивные так и негативные кейсы.
В позитивных тестах будет проверено, что при заполнение реальных имен, телефонов в формате +7 (999) 999 99 99 и почт в формате xxx@domen.ru, запись будет осуществлена.
Например, 
* Дмитрий
* +7 916 915 32 54
* dmitry@yandex.ru
* Ожидаемый результат: Заявка на запись курса создана, о чем сообщает всплывающее окно.

Негативные кейсы - проверка полей ввода на наличие валидации.
Отправка пустой формы. 
Ожидаемый результат: Надпись Обязательное поле под каждым полем ввода.

1. Слишком короткое имя.
* У
* +7 916 915 32 54
* dmitry@yandex.ru
* Ожидаемый результат: Слишком короткое Имя.
2. Цифры в имени.
* 456
* +7 916 915 32 54
* dmitry@yandex.ru
* Ожидаемый результат: Имя должно состоять из букв.
3. Неверный формат номера.
* Дмитрий
* 5 916 915 32 54
* dmitry@yandex.ru
* Ожидаемый результат: Номер в формате +7 (999) 999-99-99.
4. Короткий номер.
* Дмитрий
* 5 916
* dmitry@yandex.ru
* Ожидаемый результат: Слишком короткий номер.
5. Отсутствие @ в почте.
* Дмитрий
* +7 916 915 32 54
* dmitryyandex.ru
* Ожидаемый результат: Неверный формат почты.
6. Отсутствует домен в почте.
* Дмитрий
* +7 916 915 32 54
* dmitry@yandexru
* Ожидаемый результат: Неверный формат почты.


## Используемые инструменты.
### IntelliJ IDEA Community Edition с 11 версией java.
В IDEA можно подключить множество зависимостей и плагинов, которые понадобятся нам для тестирования данного функционала. Сам инструмент удобен, интерфейс интуитивно понятен. Также IDEA является бесплатной, что не менее важно.
### Браузер Google Chrome версией не ниже 92.
Браузер Google Chrome является наиболее популярным и стабильным браузером.
### Фреймворк Selenide
Удобный и бесплатный фреймворк, который очень удобен для тестирования веб-интерфейсов. Так же прост в конфигурации.


## Необходимые разрешения/данные/доступы.
Тестовая площадка и доступ к ней для проверки проверяемого функционала. 
Если тестовой площадки нету, то необходимо разрешение на автоматизированное тестирование сайта https://netology.ru/ и тестовые данные, которые не будут приняты за реальных пользователей.
Доступ к базе данных на чтение для проверки создания успешной записи.

## Возможные риски при автоматизации.
### Возможность падения тестов в связи с изменениями сайта.
Если изменится название профессии, если изменится количество полей в форме записи, если поменяется структура сайта, то тесты перестанут проходить.
### Сложности с поиском правильных локаторов на странице.
Не у всех элементов есть уникальные номера,часть элементов может быть скрыта или недоступна. В связи с этим поиск нужных локаторов может осложнится.
### Возможность уронить сайт в ходе тестирования.
В связи с частыми записями на курс или данные будут введены не туда, куда нужно, сайт может отработать это некорректно или упасть совсем.

## Специалисты для автоматизации.
Необходим специалист по тестированию с навыками автоматизированного тестирования и знанием java, для создания и поддержания тестов в актуальном состояние.

## Оценка необходимого времени.
На тестирование данного функционала понадобится 5 рабочих дня или 24 часа (5 х 8 = 40) рабочего времени.


