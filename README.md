# Lab 3. Functional testing

## Обзор проекта
![Gold apple logo](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e2/CK_Calvin_Klein_logo.svg/616px-CK_Calvin_Klein_logo.svg.png)
[Calvin klein application](https://www.calvinklein.ru/)

Интернет магазин, продающий джинсы, нижнее бельё, одежду в стиле унисекс и аксессуары.

---

# Функциональные тесты:

## Модуль: аккаунт

### Тест-кейс № 1

**Название**: Просмотр зарегестрированного аккаунта

**Описание**: Регистрация и переход на страницу аккаунта после регистрации

**Предусловие**: Аккаунт ещё не зарегестрирован, выбран ещё не зарегестрированный email

**Шаги тест-кейса**: 
1. Перейти на страницу [https://www.calvinklein.ru/](https://www.calvinklein.ru/)
2. Нажать на кнопку "Войти / Зарегестрироваться"
3. Нажать на кнопку зарегестрироваться
4. Ввести данные: <br>
   &ensp; Эл. Почта: casderiopus@gmail.com <br>
   &ensp; Пароль: 12345Asd
5. Подтвердить согласие на принятие условий магазина и его политик
6. Нажать на кнопку зарегестрироваться
7. Перейти на страницу "Мой аккаунт"
8. Перейти на страницу "Моя информация"

**Ожидаемый результат**: 
Отображается страница аккаунта с введёнными при регистрации электронной почтой и паролем. 
Другая информация не заполнена.

### Тест-кейс № 2

**Название**: Отображение информации пользователя после изменения

**Описание**: Заполнение информации пользователя и просмотр изменений на странице аккаунта

**Предусловие**: Аккаунт зарегестрирован и не заполнен

**Шаги тест-кейса**:
1. Перейти на страницу [https://www.calvinklein.ru/](https://www.calvinklein.ru/)
2. Нажать на кнопку "Войти / Зарегестрироваться"
3. Ввести данные: <br>
   &ensp; Эл. Почта: casderiopus@gmail.com <br>
   &ensp; Пароль: 12345Asd
4. Нажать на кнопку "Войти"
5. Перейти на страницу "Мой аккаунт"
6. Перейти на страницу "Моя информация"
7. Указать имя, фамилию и дату рождения <br>
   Прим. Имя: Вадим, фамилия: Самаль, дата рождения: 15.04.2003
8. Нажать на кнопку сохранить изменения
9. Обновить страницу

**Ожидаемый результат**: 
На странице аккаунта в разделе "Моя информация" отображаются корректные данные, введённые пользователем при изменении профиля.

### Тест-кейс № 3

**Название**: Отображение пустого раздела "*избранное*"

**Описание**: Просмотр раздела "*избранное*" без добавления в него товара

**Предусловие**: Пользователь зарегестрирован и авторизован на сайте, список пожеланий пуст

**Шаги тест-кейса**:
1. Зайти на главную страницу [https://www.calvinklein.ru/](https://www.calvinklein.ru/)
2. Перейти в раздел "*избранное*"

**Ожидаемый результат**: 
Иконка списка пожеланий прозрачная.
На странице отображается сообщение "*Вы Пока Не Сохранили Ни Одного Товара*".
Отображается кнопка с надписью "*Начние Делать Покупки*".

### Тест-кейс № 4

**Название**: Отображение раздела "*избранное*" при наличии в нём товаров

**Описание**: Просмотр раздела "*избранное*" после добавление товаров в список пожеланий

**Предусловие**: Пользователь зарегестрирован, находится на главной странице, список пожеланий пуст

**Шаги тест-кейса**:
1. Перейти в любой раздел (прим. Одежда -> Новинки Одежда)
2. Перейти на страницу товара
3. Нажать на кнопку "В избранное" <br>
   &ensp; **Ожидаемый результат**: Кнопка поменяет свой фон с прозрачного на чёрный
4. Перейти на страницу аккаунта
5. Перейти в раздел "*избранное*"

**Ожидаемый результат**:
Иконка списка пожеланий изменила свой фон с прозрачного на черный.
В списке пожеланий отображается добавленный туда товар.

## Модуль: корзина покупок

### Тест-кейс № 5

**Название**: Отображение пустой корзины

**Описание**: Просмотр корзины без добавления в неё товаров

**Предусловие**: Пользователь зарегестрирован, корзина пустая

**Шаги тест-кейса**:
1. Перейти на страницу [https://www.calvinklein.ru/](https://www.calvinklein.ru/)
2. Перейти на страницу корзины покупок

**Ожидаемый результат**: Отображается сообщение "Ваша корзина пуста". 
Отображается кнопка с надписью "Продолжить Покупки".
Отображается список рекомендаций.

### Тест-кейс № 6

**Название**: Отображение корзины с товарами

**Описание**: Просмотр корзины после добавления в неё товаров

**Предусловие**: Пользователь зарегестрирован, корзина пустая

**Шаги тест-кейса**:
1. Перейти на страницу [https://www.calvinklein.ru/](https://www.calvinklein.ru/)
2. Перейти в любой раздел (прим. Одежда -> Новинки Одежда)
3. Перейти на страницу товара
4. Нажать на кнопку "Добавить" <br/>
   &ensp; **Ожидаемый результат**: появилось окно с выбором размера одежды.
5. Выбрать размер (прим. XXL) и нажать кнопку "Добавить В Корзину Покупок" <br>
&ensp; **Ожидаемый результат**: 
Фон кнопки перехода на страницу с корзиной покупок изменился с  прозрачного на чёрный.
У кнопки появилась надпись с числом товаров в корзине (прим. 1).
6. Перейти на страницу корзины покупок.

**Ожидаемый результат**:
Отображается добавленный пользователем товар с информацией о нём.
Отображается конечная цена корзины.
Отображается кнопка с надписью "Перейти к оформлению заказа".

