# Практика. Качество кода

В качестве основы взята практическая работа по верстке сайта из модуля 18. Здесь лежит [изначальный вариант](https://github.com/AndrejKonanykhin/Module-18.git) работы.

### Что было сделано:

---

По CSS-стилям:

1. Был произведен поиск дублирующих свойств, уже заданных в стилях родительских элементов. <br>Например, у _body_ было задано свойство _box-sizing: border-box_, уже определенное для всех элементов страницы. Принцип _DRY_

2. Также удалены классы, у которых был задан только цвет. К этим элементам применен уже существующий класс _.orange_. Принцип _DRY_

3. Классы в CSS-файле сгруппированы по секциям в том порядке, как они выводятся на странице в браузере сверху-вниз. И снабжены соответствующими комментариями. Принцип _KISS_

4. Свойства каждого класса или тэга расположены в определенном порядке от параметров самого блока к параметрам его содержимого: размеры, внешние и внутренние отступы, фон, границы, тень, отобращение, позициоирование, цвет и параметры шрифта. Принцип _KISS_

По CSS и HTML:

1. Удалены необязательные классы, вместо них использовано наследование. Например вместо класса _.header-container_ используется связка _header .container_. В CSS почти ничего не изменилось, а HTML код стал полегче. Аналогично поступил с кнопками и ссылками. Принцип _KISS_

2. Всем кнопкам при подключении скрипта, нужно будет добавить идентификаторы. Не стал пока этого делать, т.к. не требуется на этом этапе. Принцип _YAGNI_

3. При верстке номера телефонов сделал ссылками, а также кнопки инстаграма и почты с выдуманными адресами. Хотя этого не требовалось по ТЗ. Принцип _YAGNI_

4. Добавил класс _.desktop_ для элементов, скрываемых в мобильной версии. Теперь вместо списка классов со свойством _display: none_ в медиазапросе записан только _.desktop {display: none};_. Принцип _KISS_

5. К повторяющимся блокам применил методологию БЭМ: навигация _nav_, блоки отзывов клиентов и стилей ремонта _section-column_, заголовки секций _section-title_.

6. Макет верстки проверен в валидаторе [W3C](https://validator.w3.org/nu/#textarea). Результат: без ошибок. Скорость проверки нового варианта 36 миллисекунд, старого 43 миллисекунды. Количество строк кода сократилось с 530 до 510. Внешний вид страницы не изменился.

---
В качестве линтера использую расширение для VS-code - Prettier. Не идеал, конечно. Попробую другие, предложенные в модуле.
