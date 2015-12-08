# 11-css-danco
unit 10
=======

plan1.html:
-----------
```
<!--///////////////////////////////////////////////////////
       // Our-plan section 
//////////////////////////////////////////////////////////-->
  

  <style type="text/css">
  .our-plan-paralax {

  }
  .our-plan-back {

  }
  .our-plans {

  }
  .ourplan-heading {

  }
  .our-plan-text {

  }
  .our-plan-paragraph {

  }
  .plan1 {

  }
  .plan2 {

  }
  .plan3 {

  }
  .plan4 {

  }
  .price {

  }
  .plan-1-butn {

  }
  .plan-4-butn2 {

  }
  .plan-4-butn3 {

  }
  .plan-4-butn4 {

  }

  .plan-center {

  }
  .plan1-center {

  }
  .plan2-center {

  }
  .plan3-center{

  }
  .plan1-center {

  }
  </style>
  
    <div class="our-plan-paralax">
    <div class="our-plan-back">
      <div class="w-container">
        <div class="wrap">
          <div class="our-plans">
            <h1 class="ourplan-heading">OUR PLANS</h1>
            <div class="our-plan-text">SELECT YOUR BEST PLAN</div>
          </div>
          <div class="sepreater"></div>
          <p class="our-plan-paragraph">As a creative studio we believe no client is too big nor too small to work with us. We love what we do. And that shows.
            <br>We like to create things with fun, like-minded people.</p>
          <div class="w-row">
            <div class="w-col w-col-3">
              <div class="plan1">
                <div class="plan1-center">
                  <h4>PERSONAL SITE</h4>
                  <div class="price">$15 / Month</div>
                </div>
                <p class="plan-center">
                  <br>Unlimited&nbsp;Email-Addresses
                  <br>
                  <br>50GB&nbsp;Disk&nbsp;Space
                  <br>
                  <br>Unlimited&nbsp;MySQL-Databases
                  <br>
                  <br>Unlimited&nbsp;Domains
                  <br>
                  <br>Free&nbsp;Billing Systems</p><a class="plan-1-butn" href="#">Sign Up!</a>
              </div>
            </div>
            <div class="w-col w-col-3">
              <div class="plan1 plan2">
                <div class="plan2-center">
                  <h4>SMALL BUSINESS</h4>
                  <div class="price">$25 / Month</div>
                </div>
                <p class="plan-center">
                  <br>Unlimited&nbsp;Email-Addresses
                  <br>
                  <br>80GB&nbsp;Disk&nbsp;Space
                  <br>
                  <br>Unlimited&nbsp;MySQL-Databases
                  <br>
                  <br>Unlimited&nbsp;Domains
                  <br>
                  <br>Free&nbsp;Billing Systems</p><a class="plan-1-butn2 plan-1-butn" href="#">Sign Up!</a>
              </div>
            </div>
            <div class="w-col w-col-3">
              <div class="plan1 plan3">
                <div class="plan1-center plan3-center">
                  <h4>CORPORATE SITE</h4>
                  <div class="price">$50 / Month</div>
                </div>
                <p class="plan-center">
                  <br>Unlimited&nbsp;Email-Addresses
                  <br>
                  <br>120GB&nbsp;Disk&nbsp;Space
                  <br>
                  <br>Unlimited&nbsp;MySQL-Databases
                  <br>
                  <br>Unlimited&nbsp;Domains
                  <br>
                  <br>Free&nbsp;Billing Systems</p><a class="plan-1-butn plan-1-butn3" href="#">Sign Up!</a>
              </div>
            </div>
            <div class="w-col w-col-3">
              <div class="plan1 plan4">
                <div class="plan1-center plan4-center">
                  <h4>E-COMMERCE SITE</h4>
                  <div class="price">$90&nbsp;/ Month</div>
                </div>
                <p class="plan-center">
                  <br>Unlimited&nbsp;Email-Addresses
                  <br>
                  <br>120GB&nbsp;Disk&nbsp;Space
                  <br>
                  <br>Unlimited&nbsp;MySQL-Databases
                  <br>
                  <br>Unlimited&nbsp;Domains
                  <br>
                  <br>Free&nbsp;Billing Systems</p><a class="plan-1-butn plan-4-butn4" href="#">Sign Up!</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>


<!--///////////////////////////////////////////////////////
       // End Our-Plan section 
//////////////////////////////////////////////////////////-->

```
plan1.htm2:
-----------

```

  .our-plan-paralax {
    background-image: none;
    background-position: 0% 0%;
    background-size: auto;
    background-repeat: repeat;
    background-attachment: scroll;

  }
  .our-plan-back {
    padding-top: 15px;
    background-color: transparent;
    background-image: -webkit-linear-gradient(#00b8b1, rgba(7, 148, 143, 0.92));
    background-image: -o-linear-gradient(#00b8b1, rgba(7, 148, 143, 0.92));
    background-image: linear-gradient(#00b8b1, rgba(7, 148, 143, 0.92));

  }
  
  .ourplan-heading {
    color: white;
  }
  .our-plan-text {
    margin-top: 20px;
    margin-bottom: 20px;
    color: white;
    font-size: 15px;
    text-align: center;
  }
  .our-plan-paragraph {
    margin-top: 20px;
    margin-bottom: 20px;
    color: white;
    text-align: center;
  }
```

plan3.html:
-------------

```
.plan1 {
  padding-left: 0px;
  border-style: solid;
  border-width: 1px 1px 4px;
  border-color: #ffce54;
}
.plan1.plan3 {
  border-color: #a0d468;
}
.plan1.plan4 {
  border-color: #fc6e51;
}
.plan2 {
  border-width: 1px 1px 4px;
  border-color: #ed5565;
}


.price {
  display: block;
  margin-right: auto;
  margin-left: auto;
  padding-right: 10px;
  padding-bottom: 10px;
  padding-left: 10px;
  text-align: center;
}
```

plan4.html:
-------------
```
  .plan-center {
  margin-top: 10px;
  margin-right: 0px;
  margin-bottom: 30px;
  padding: 0px 10px 20px;
  border-bottom: 2px dashed #eee;
  color: white;
  text-align: center;
}

 .plan1-center {
  background-color: #ffce54;
}

.plan2-center {
  background-color: #ed5565;
}

.plan1-center.plan3-center {
  background-color: #a0d468;
}
.plan1-center.plan4-center {
  background-color: #fc6e51;
}

```

plan5.html:
-------------
```
 .plan-1-butn {
  display: block;
  width: 40%;
  margin: 10px auto 20px;
  padding: 10px;
  border-radius: 0px;
  background-color: #ffce54;
  box-shadow: none;
  color: black;
  text-align: center;
  text-decoration: none;
}

.plan-1-butn:hover {
  border-radius: 0px;
  background-color: #ffce54;
  box-shadow: none;
  color: white;
}
.plan-1-butn.plan-1-butn2 {
  background-color: #ed5565;
  box-shadow: none;
}
.plan-1-butn.plan-1-butn3 {
  background-color: #a0d468;
  box-shadow: none;
}
.plan-1-butn.plan-4-butn4 {
  background-color: #fc6e51;
  box-shadow: none;
}

```
contact1.html
----------------
```
.contact-paralax {

}
.contact-back {
  padding-top: 15px;
  background-color: #cece54;

}

.contact-heading {
  color: white;
}
.contact-center {
  margin-top: 20px;
  margin-bottom: 30px;
  color: white;
  text-align: center;
}

.contac-map {
  background-color: transparent;
  color: black;
}


.contact-col {
  display: block;
  margin: 50px auto 30px;
  padding-top: 0px;
}
.contact-col-head {
  color: white;
}
.contact-col-text {
  border-right: 4px solid white;
  border-left: 4px none white;
  color: white;
  text-align: center;
}
.contact-col-text-bar-last {
  border-right: 0px none white;
  color: white;
  text-align: center;
}
```
Тег form
===========

Тег form устанавливает форму на веб-странице. Форма предназначена для обмена данными между пользователем и сервером. Область применения форм не ограничена отправкой данных на сервер, с помощью клиентских скриптов можно получить доступ к любому элементу формы, изменять его и применять по своему усмотрению.

Документ может содержать любое количество форм, но одновременно на сервер может быть отправлена только одна форма. По этой причине данные форм должны быть независимы друг от друга.

Для отправки формы на сервер используется кнопка Submit, того же можно добиться, если нажать клавишу Enter в пределах формы. Если кнопка Submit отсутствует в форме, клавиша Enter имитирует ее использование.

Когда форма отправляется на сервер, управление данными передается программе, заданной атрибутом action тега form. Предварительно браузер подготавливает информацию в виде пары «имя=значение», где имя определяется атрибутом name тега input, а значение введено пользователем или установлено в поле формы по умолчанию. 

Параметры перечисляются после вопросительного знака, указанного после адреса CGI-программы и разделяются между собой символом амперсанда (&). Нелатинские символы преобразуются в шестнадцатеричное представление (в форме %HH, где HH — шестнадцатеричный код для значения ASCII-символа), пробел заменяется на плюс (+).

Допускается внутрь контейнера form помещать другие теги, при этом сама форма никак не отображается на веб-странице, видны только ее элементы и результаты вложенных тегов.

Синтаксис
```
<form action="URL">
  ...
</form>
```
Атрибуты
---------
- accept-charset
Устанавливает кодировку, в которой сервер может принимать и обрабатывать данные.
- action
Адрес программы или документа, который обрабатывает данные формы.
- autocomplete
Включает автозаполнение полей формы.
- enctype
Способ кодирования данных формы.
- method
Метод протокола HTTP.
- name
Имя формы.
- novalidate
Отменяет встроенную проверку данных формы на корректность ввода.
- target
Имя окна или фрейма, куда обработчик будет загружать возвращаемый результат.

Тег input
---------
Тег input является одним из разносторонних элементов формы и позволяет создавать разные элементы интерфейса и обеспечить взаимодействие с пользователем. Главным образом input предназначен для создания текстовых полей, различных кнопок, переключателей и флажков. Хотя элемент input не требуется помещать внутрь контейнера form, определяющего форму, но если введенные пользователем данные должны быть отправлены на сервер, где их обрабатывает серверная программа, то указывать form обязательно. То же самое обстоит и в случае обработки данных с помощью клиентских приложений, например, скриптов на языке JavaScript.

Основной атрибут тега input, определяющий вид элемента — type. Он позволяет задавать следующие элементы формы: текстовое поле (text), поле с паролем (password), переключатель (radio), флажок (checkbox), скрытое поле (hidden), кнопка (button), кнопка для отправки формы (submit), кнопка для очистки формы (reset), поле для отправки файла (file) и кнопка с изображением (image). Для каждого элемента существует свой список атрибутов, которые определяют его вид и характеристики. Кроме того, в HTML5 добавлено еще более десятка новых элементов.

Атрибуты
--------
- accept
Устанавливает фильтр на типы файлов, которые вы можете отправить через поле загрузки файлов.
- accesskey
Переход к элементу с помощью комбинации клавиш.
- align
Определяет выравнивание изображения.
- alt
Альтернативный текст для кнопки с изображением.
- autocomplete
Включает или отключает автозаполнение.
- autofocus
Устанавливает фокус в поле формы.
- border
Толщина рамки вокруг изображения.
- checked
Предварительно активированный переключатель или флажок.
- disabled
Блокирует доступ и изменение элемента.
- form
Связывает поле с формой по её идентификатору.
- formaction
Определяет адрес обработчика формы.
- formenctype
Устанавливает способ кодирования данных формы при их отправке на сервер.
- formmethod
Сообщает браузеру каким методом следует передавать данные формы на сервер.
- formnovalidate
Отменяет встроенную проверку данных на корректность.
- formtarget
Определяет окно или фрейм в которое будет загружаться результат, возвращаемый обработчиком формы.
- list
Указывает на список вариантов, которые можно выбирать при вводе текста.
- max
Верхнее значение для ввода числа или даты.
- maxlength
Максимальное количество символов разрешенных в тексте.
- min
Нижнее значение для ввода числа или даты.
- multiple
Позволяет загрузить несколько файлов одновременно.
- name
Имя поля, предназначено для того, чтобы обработчик формы мог его идентифицировать.
- pattern
Устанавливает шаблон ввода.
- placeholder
Выводит подсказывающий текст.
- readonly
Устанавливает, что поле не может изменяться пользователем.
- required
Обязательное для заполнения поле.
- size
Ширина текстового поля.
- src
Адрес графического файла для поля с изображением.
- step
Шаг приращения для числовых полей.
- tabindex
Определяет порядок перехода между элементами с помощью клавиши Tab.
- type
Сообщает браузеру, к какому типу относится элемент формы.
- value
Значение элемента.

Поле textarea
-------------
Поле textarea представляет собой элемент формы для создания области, в которую можно вводить несколько строк текста. В отличие от тега input в текстовом поле допустимо делать переносы строк, они сохраняются при отправке данных на сервер.

Синтаксис
```
<textarea атрибуты>
  текст
</textarea>
```
Атрибуты
- accesskey
Переход к полю с помощью сочетания клавиш.
- autofocus
Автоматическое получение фокуса.
- cols
Ширина поля в символах.
- disabled
Блокирует доступ и изменение элемента.
- form
Связывает текстовое поле с формой по её идентификатору.
- maxlength
Максимальное число введенных символов.
- name
Имя поля, предназначено для того, чтобы обработчик формы мог его идентифицировать.
- placeholder
Указывает замещающийся текст.
- readonly
Устанавливает, что поле не может изменяться пользователем.
- required
Обязательное для заполнения поле.
- rows
Высота поля в строках текста.
- tabindex
Порядок перехода между элементами при нажатии на клавишу Tab.
- wrap
Параметры переноса строк.

Элемент fieldset
-----------------
Элемент fieldset предназначен для группирования элементов формы. Такая группировка облегчает работу с формами, содержащими большое число данных. Например, один блок может быть предназначен для ввода текстовой информации, а другой — для флажков.

Синтаксис
```
<form>
  <fieldset>...</fieldset>
</form>
```
Атрибуты
- disabled
Блокирует поля формы в группе.
- form
Связывает группу с формой.
- title
Добавляет всплывающую подсказку к группе формы.

Тег legend
----------
Тег legend применяется для создания заголовка группы элементов формы, которая определяется с помощью тега fieldset. Группа элементов обозначается в браузере с помощью рамки, а текст, который располагается внутри контейнера legend, встраивается в эту рамку.

Синтаксис
```
<fieldset>
  <legend>Текст</legend>
</fieldset>
```
Атрибуты
- accesskey
Переход к группе элементов формы с помощью комбинации клавиш.
- align
Определяет выравнивание текста.
- title
Добавляет всплывающую подсказку к тексту заголовка.

Тег select
----------
Тег select позволяет создать элемент интерфейса в виде раскрывающегося списка, а также список с одним или множественным выбором, как показано далее. Конечный вид зависит от использования атрибута size тега select, который устанавливает высоту списка. Ширина списка определяется самым широким текстом, указанным в теге option, а также может изменяться с помощью стилей. Каждый пункт создается с помощью тега option, который должен быть вложен в контейнер select. Если планируется отправлять данные списка на сервер, то требуется поместить элемент select внутрь формы. Это также необходимо, когда к данным списка идет обращение через скрипты.

Синтаксис
```
<select>
  <option>Пункт 1</option>
  <option>Пункт 2</option>
</select>
```
Атрибуты
- accesskey
Позволяет перейти к списку с помощью некоторого сочетания клавиш.
- autofocus
Устанавливает, что список получает фокус после загрузки страницы.
- disabled
Блокирует доступ и изменение элемента.
- form
Связывает список с формой.
- multiple
Позволяет одновременно выбирать сразу несколько элементов списка.
- name
Имя элемента для отправки на сервер или обращения через скрипты.
- required
Список обязателен для выбора перед отправкой формы.
- size
Количество отображаемых строк списка.
- tabindex
Определяет последовательность перехода между элементами при нажатии на клавишу Tab

Тег button
----------
Тег button создает на веб-странице кнопки и по своему действию напоминает результат, получаемый с помощью тега input (с атрибутом type="button | reset | submit"). В отличие от этого тега, button предлагает расширенные возможности по созданию кнопок. Например, на подобной кнопке можно размещать любые элементы HTML, в том числе изображения. Используя стили можно определить вид кнопки путем изменения шрифта, цвета фона, размеров и других параметров.

Теоретически, тег button должен располагаться внутри формы, устанавливаемой элементом form. Тем не менее, браузеры не выводят сообщение об ошибке и корректно работают с тегом button, если он встречается самостоятельно. Однако, если необходимо результат нажатия на кнопку отправить на сервер, помещать button в контейнер form обязательно.

Синтаксис
```
<form>
  <button>...</button>
</form>
```
Атрибуты
- accesskey
Доступ к элементам формы с помощью горячих клавиш.
- autofocus
Устанавливает, что кнопка получает фокус после загрузки страницы.
- disabled
Блокирует доступ и изменение элемента.
- form
Связывает между собой форму и кнопку.
- formaction
Задаёт адрес, на который пересылаются данные формы при нажатии на кнопку.
- formenctype
Способ кодирования данных формы.
- formmethod
Указывает метод пересылки данных формы.
- formnovalidate
Отменяет проверку формы на корректность.
- formtarget
Открывает результат отправки формы в новом окне или фрейме.
- name
Определяет уникальное имя кнопки.
- type
Тип кнопки — обычная, для отправки данных формы на сервер или для очистки формы.
- value
Значение кнопки, которое будет отправлено на сервер или прочитано с помощью скриптов.
