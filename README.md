# homeworks-aqa-4_1-TestPlan
# План автоматизации тестирования возможности записи на обучение профессии "Тестировщик ПО" на сайте Netology.ru
## Введение
***Цель создания плана*** - описание процесса автоматизации тестирования перехода к форме записи и заполнения этой формы.

***Виды тестирования*** - модульное тестирование, тестирование методом черного ящика, тестирование удобства использования.

## Перечень автоматизируемых сценариев
### 1. Способы поиска курса обучения ["Тестировщик ПО"](https://netology.ru/programs/qa?recommended_by=catalog&recommended_code=);

1. На главной страницe сайта [Netology.ru](https://netology.ru/), с помощью выпадающего меню "Каталог курсов" -> Программирование -> Тестировщик ПО;

2. На главной странице сайта [Netology.ru](https://netology.ru/), с помощью выпадающего меню "Каталог курсов" -> Найти курс -> Программирование -> Тестировщик ПО;

3. На главной странице сайта [Netology.ru](https://netology.ru/), с помощью выпадающего меню "Каталог курсов" -> Все курсы -> Программирование -> Тестировщик ПО;

4. На главной странице сайта [Netology.ru](https://netology.ru/), после раздела "Выберите вектор развития", с помощью кнопки "Выбрать курс" -> Программирование -> Тестировщик ПО;

5. На главной странице сайта [Netology.ru](https://netology.ru/), внизу страницы с помощью меню "Каталог курсов" -> Программирование -> Тестировщик ПО;
 
### 2. Способы поиска формы для записи на курс обучения;

1. На странице ["Тестировщик ПО"](https://netology.ru/programs/qa?recommended_by=catalog&recommended_code=#/) - в верхней части страницы нажать на кнопку "Записаться";

2. На странице ["Тестировщик ПО"](https://netology.ru/programs/qa?recommended_by=catalog&recommended_code=#/) - прокрутить всю страницу профессии до формы для записи на курс.

### 3. Позитивный тест: Запись на курс обучения авторизованного пользователя;

1. Авторизоваться на сайте [Netology.ru](https://netology.ru/);

2. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

3. Поля ***"Имя"*** и ***"Телефон"*** заполнены автоматически;

4. Нажать на кнопку "Записаться";

#### Ожидаемый результат:

Появляется сообщение: "Заявка принята. В ближайшее время с Вами свяжется наш менеджер".

### 4. Негативный тест: Запись на курс обучения авторизованного пользователя;

1. Авторизоваться на сайте [Netology.ru](https://netology.ru/);

2. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

3. В поле ***"Имя"*** ввести невалидные данные - "рвнер@@#7756";

4. В поле ***"Телефон"*** ввести невалидные данные - "крр64654№"№;%";

5. Нажать на кнопку "Записаться";

#### Ожидаемый результат:

Появляются сообщения об ошибках в полях ввода и пользователь не записывается 

### 5. Позитивный тест: Запись на курс обучения неавторизованного пользователя;

1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

2. В поле "Имя" ввести валидные данные - "Василий";

3. В поле "Телефон" ввести валидные данные - "79998884466";

4. В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

5. Нажать на кнопку "Записаться";

#### Ожидаемый результат:

Появляется сообщение: "Заявка принята. В ближайшее время с Вами свяжется наш менеджер".


### 6. Негативный тест: Запись на курс обучения неавторизованного пользователя;

1. Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

2. В поле ***"Имя"*** ввести невалидные данные - ";%;№ВУ";

3. В поле ***"Телефон"*** ввести невалидные данные - "ВАР:%;34";

4. В поле ***"Электронная почта"*** ввести невалидные данные - "13пдо13";

5. Нажать на кнопку "Записаться";

#### Ожидаемый результат:

Появляются сообщения об ошибках в полях ввода и пользователь не записывается

### 7. Негативные тесты: Проверка поля "Имя" с неверными данными;

#### 1. Поле ***"Имя"*** состоит из одного символа.

1.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

1.2 В поле ***"Имя"*** ввести данные из одного символа - "А";

1.3 В поле ***"Телефон"*** ввести валидные данные - "79998884466";

1.4 В поле ***"Электронная почта"*** ввести невалидные данные - "qa2022@mail.ru";

1.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Имя" появилась надпись красного цвета: "Длина поля должна быть не короче 2-х символов".

#### 2. Поле ***"Имя"*** состоит из цифр.

2.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

2.2 В поле ***"Имя"*** ввести данные из одного цифр - "123";

2.3 В поле ***"Телефон"*** ввести валидные данные - "79998884466";

2.4 В поле ***"Электронная почта"*** ввести невалидные данные - "qa2022@mail.ru";

2.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Имя" появилась надпись красного цвета: "Поле должно состоять из букв".

#### 3. Поле ***"Имя"*** состоит из спецсимволов.

3.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

3.2 В поле ***"Имя"*** ввести данные из спецсинволов - "@#$%^^";

3.3 В поле ***"Телефон"*** ввести валидные данные - "79998884466";

3.4 В поле ***"Электронная почта"*** ввести невалидные данные - "qa2022@mail.ru";

3.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Имя" появилась надпись красного цвета: "Поле должно состоять из букв".

#### 4. Поле ***"Имя"*** пустое.

4.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

4.2 В поле ***"Имя"*** оставить пустым - " ";

4.3 В поле ***"Телефон"*** ввести валидные данные - "79998884466";

4.4 В поле ***"Электронная почта"*** ввести невалидные данные - "qa2022@mail.ru";

4.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Имя" появилась надпись красного цвета: "Поле не может быть пустным".

### 8. Негативные тесты: Проверка поля "Телефон" с неверными данными;

#### 1. Поле ***"Телефон"*** состоит из одного символа.

1.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

1.2 В поле "Имя" ввести валидные данные - "Василий";

1.3 В поле "Телефон" ввести валидные данные - "7";

1.4 В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

1.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Телефон" появилась надпись красного цвета: "Номер должен быть в формате +9 (999) 999-99-99".

#### 2. Поле ***"Телефон"*** состоит из пяти цифр.

2.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

2.2 В поле "Имя" ввести валидные данные - "Василий";

2.3 В поле "Телефон" ввести валидные данные - "34567";

2.4 В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

2.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Телефон" появилась надпись красного цвета: "Номер должен быть в формате +9 (999) 999-99-99".

#### 3. Поле ***"Телефон"*** состоит из десяти цифр.

3.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

3.2 В поле "Имя" ввести валидные данные - "Василий";

3.3 В поле "Телефон" ввести валидные данные - "7951516697";

3.4 В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

3.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Телефон" появилась надпись красного цвета: "Номер должен быть в формате +9 (999) 999-99-99".

#### 4. Поле ***"Телефон"*** состоит из спецсимволов.

4.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

4.2 В поле "Имя" ввести валидные данные - "Василий";

4.3 В поле "Телефон" ввести валидные данные - "@#$%^&$^&*^";

4.4 В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

4.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Телефон" появилась надпись красного цвета: "Номер должен быть в формате +9 (999) 999-99-99".

#### 5. Поле ***"Телефон"*** состоит из букв.

5.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

5.2 В поле "Имя" ввести валидные данные - "Василий";

5.3 В поле "Телефон" ввести валидные данные - "gasdgh";

5.4 В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

5.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Телефон" появилась надпись красного цвета: "Номер должен быть в формате +9 (999) 999-99-99".

#### 6. Поле ***"Телефон"*** пустое.

6.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

6.2 В поле "Имя" ввести валидные данные - "Василий";

6.3 В поле "Телефон" ввести валидные данные - " ";

6.4 В поле "Электронная почта" ввести валидные данные - "qa2022@mail.ru";

6.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Телефон" появилась надпись красного цвета: "Поле не может быть пустным".


### 9. Негативные тесты: Проверка поля "Электронная почта" с неверными данными;

#### 1. Поле ***"Электронная почта"*** состоит из одного символа.

1.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

1.2 В поле "Имя" ввести валидные данные - "Василий";

1.3 В поле "Телефон" ввести валидные данные - "79998884466";

1.4 В поле "Электронная почта" ввести валидные данные - "q";

1.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Электронная почта" появилась надпись красного цвета: "Неверный формат электронной почты".

#### 2. Поле ***"Электронная почта"*** состоит из цифр.

2.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

2.2 В поле "Имя" ввести валидные данные - "Василий";

2.3 В поле "Телефон" ввести валидные данные - "79998884466";

2.4 В поле "Электронная почта" ввести валидные данные - "4678";

2.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Электронная почта" появилась надпись красного цвета: "Неверный формат электронной почты".

#### 3. Поле ***"Электронная почта"*** состоит из спецсимволов.

3.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

3.2 В поле "Имя" ввести валидные данные - "Василий";

3.3 В поле "Телефон" ввести валидные данные - "79998884466";

3.4 В поле "Электронная почта" ввести валидные данные - "#$%^&";

3.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Электронная почта" появилась надпись красного цвета: "Неверный формат электронной почты".

#### 4. Поле ***"Электронная почта"*** без символа "@".

4.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

4.2 В поле "Имя" ввести валидные данные - "Василий";

4.3 В поле "Телефон" ввести валидные данные - "79998884466";

4.4 В поле "Электронная почта" ввести валидные данные - "1989gmail.ru";

4.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Электронная почта" появилась надпись красного цвета: "Неверный формат электронной почты".

#### 5. Поле ***"Электронная почта"*** пустое.

5.1 Открыть форму записи на курс обучения, выбрав один из вариантов поиска формы;

5.2 В поле "Имя" ввести валидные данные - "Василий";

5.3 В поле "Телефон" ввести валидные данные - "79998884466";

5.4 В поле "Электронная почта" ввести валидные данные - " ";

5.5 Нажать на кнопку "Записаться";

#### Ожидаемый pезультат:

Под полем "Электронная почта" появилась надпись красного цвета: "Поле не может быть пустным".

## Перечень используемых инструментов с обоснованием выбора
***1. IntelliJ IDEA*** - интеллектуальная среда разработки. Умная и удобная среда разработки для Java с поддержкой всех последних технологий и фреймворков.

***2. Java JDK 11*** - популярный язык программирования для написания автотестов, имеет набор готового ПО для разработки и запуска приложений.

***3. Gradle*** - система автоматической сборки, построенная на принципах Apache Ant и Apache Maven, но предоставляющая DSL на языках Groovy и Kotlin вместо традиционной XML-образной формы представления конфигурации проекта.

***4. JUnit 5*** - тестовый фреймворк. Библиотека для модульного тестирования программного обеспечения на языке Java.

***5. Selenide*** - это библиотека для написания лаконичных и стабильных UI тестов с открытым исходным кодом.

***6. JavaFaker*** - библиотека для генерации случайных тестовых данных.

***7. Lombok*** - позволяет оптимизировать код автотестов, добавляет в Java новые «ключевые слова» и превращает аннотации в Java-код, уменьшая усилия на разработку и обеспечивая некоторую дополнительную функциональность.

***8. Rest Assured*** - java-библиотека для тестирования REST API, позволяет автоматизировать тестирование get и post запросов.

***9. Браузеры: Google Chrome, Mozilla Firefox, Microsoft Edge, Safari*** - необходимы для проведения кросс-браузерного тестирования.

***10. Allure*** - фреймворк для создания отчетов о тестировании, для наглядного отображения прохождения тестов и ошибок.

***11. Git и GitHub*** - для хранения кода. Git достаточно прост и удобен для управления исходным кодом, очень распространенная система контроля версий, поэтому достаточно хорошо взаимодействует с различными ОС. GitHub специализированный веб-сервис с удобным интерфейсои, интегрирован с Git.

***12. Docker*** — это программное обеспечение, которое дает возможность на определенном участке памяти изолированно установить необходимую ОС (операционную систему), версию Java, настроить переменные окружения, установить различные зависимости и дать доступ только при определенных условиях.

***13. AppVeyor*** - для визуального отображения статуса интеграции. Этот сервис удобен тем что он имеет бесплатный базовый тариф, может осуществлять сборку как под управлением Linux, так и под Windows, а если необходимо, то под несколькими сразу. Имеет интеграцию с GitHub.

## Перечень необходимых разрешений/данных/доступов
+ Разрешение на проведение автоматизированного тестирования сайта Netology.ru;
+ Доступ к базе данных сайта Netology.ru;
+ API для отправки GET и POST запросов на сервер;

## Перечень и описание возможных рисков при автоматизации
+ Возможность изменения структуры сайта.
+ Возможность изменения CSS-селекторов сайта.
+ Возможность изменения названия обучаемой профессии.
+ Возможность изменения количества обязательных полей ввода данных, как для авторизованных, так и для неавторизованных пользователей сайта.
+ Возможность удаления обучаемой профессии.

## Перечень необходимых специалистов для автоматизации
Нужен QA Инженер по автоматизированному тестированию c навыками программирования.

## Интервальная оценка с учётом рисков (в часах)
Для написания тестов и тестирования, подготовки отчетности необходимо 20 - 30 часов рабочего времени.
