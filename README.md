## План функционального тестирования возможности открытия вклада "Накопилка"
### Автоматизируемые сценарии
#### Подготовительные шаги:
* Перейти на сайт https://alfabank.ru/
* Навести курсор на раздел “Вклады”
* Дождаться всплывающего меню
* Нажать на “Накопилка”
 
#### Позитивные сценарии:
##### Переход на страницу анкеты через кнопку “Заполнить заявку” в блоке “Накопительный счет “Накопилка”:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести валидное имя;
* В поле “Мобильный телефон” ввести валидный номер телефона;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: надпись “Спасибо, скоро мы вам перезвоним!”
#### Переход на страницу анкеты через кнопку “Заполнить заявку” в блоке “Как открыть счет и услугу “Копилка для сдачи”?”:
* Пролистать страницу до блока “Как открыть счет и услугу “Копилка для сдачи”?”
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести валидное имя;
* В поле “Мобильный телефон” ввести валидный номер телефона;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: надпись “Спасибо, скоро мы вам перезвоним!”
#### Негативные сценарии:
##### Незаполнение поля “Имя”:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Мобильный телефон” ввести валидный номер телефона;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: ошибка.
##### Использование спецсимвола в поле “Имя”:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести спецсимвол;
* В поле “Мобильный телефон” ввести валидный номер телефона;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: ошибка.
##### Использование цифр в поле “Имя”:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести цифры;
* В поле “Мобильный телефон” ввести валидный номер телефона;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: надпись ошибка.
##### Незаполнение поля “Мобильный телефон”:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести валидное имя;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: ошибка.
##### Использование номера неверной длины в поле “Мобильный телефон”:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести валидное имя;
* В поле “Мобильный телефон” ввести номер телефона, состоящий 9 цифр;
* Нажать на чекбокс  “Я согласен(а) на обработку персональных данных”
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: ошибка.
##### Отсутствие согласия на обработку персональных данных:
* Нажать на кнопку “Заполнить заявку”;
* В поле “Имя” ввести валидное имя;
* В поле “Мобильный телефон” ввести валидный номер телефона;
* Нажать на кнопку “Мы перезвоним”

**Ожидаемый результат**: ошибка.
### Используемые инструменты
* Среда разработки *IntelliJ IDEA*;
* Язык программирования *Java SЕ 11*; 
* Библиотека *Lombok* для генерации бойлерплейт-кода и повышения читаемости в целом;
* Библиотека *JavaFaker* для генерации уникальных значений при каждом запуске тестов;
* Фреймворк *JUnit 5*, как один из самых популярных проектов для автоматического тестирования;
* Фреймворк *Selenide* для написания хорошо читаемых и удобно поддерживаемых тестов.
### Необходимые разрешений/данных/доступов от банка 
* Разрешение на тестирование
* Разрешение на автоматизацию тестирования
* Доступ к СУБД для проверки создания заявки
### Возможные риски при автоматизации
* Принципиальное отсутствие возможности перехода на страницу накопительного счета «Накопилка» из меню “Вклады”, хотя представители банка сообщили о том, что данный способ является предпочтительным для пользователя ведет к дополнительным согласованиям
* Отсутствие ТЗ может привести к неверному пониманию ожидаемого результата(как пример поле “Имя”, которое принимает любые значения)
* Отсутствие обозначенных временных рамок проведения тестирования и доступа к системе контроля версий может привести к устареванию тестов еще до их написания
 
### Необходимые специалисты для автоматизации
Специалист по автоматизированному тестированию 
### Интервальная оценка с учётом рисков
Время, необходимо на тестирование, составлет 4 часа. С учетом срабатывания рисков - 6 часов.
