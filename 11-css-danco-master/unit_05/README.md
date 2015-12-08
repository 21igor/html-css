# 11-css-danco unit -5

index.html
```
 <aside>
        <h1><a href="#"><img src="images/logo.png" alt="The Baker Street Inquirer" /></a></h1>
        <nav>
            <ul>
              <li class="first"><a href="#"><i>The</i> Weblogue</a></li>
              <li><a href="#"><i>Back</i> Issues</a></li>
              <li><a href="#"><i>About</i> Our Paper</a></li>
            </ul>
        </nav><!-- /end nav -->
 </aside><!-- /end aside -->

```
main.css
```
a {
    color: #890101;
    text-decoration: none;
    -moz-transition: 0.2s color linear;
    -webkit-transition: 0.2s color linear;
    transition: 0.2s color linear;
}
a:hover {
    color: #DF3030;
}
nav ul a {
    background: url("../images/ornament.png") no-repeat 0 100%;
    font: bold 14px/1.2 "Book Antiqua", "Palatino Linotype", Georgia, serif;
    display: block;
    text-align: center;
    letter-spacing: 0.1em;
    padding: 1em 0.5em 3em;
    margin-bottom: -1em;
    text-transform: uppercase;
}

nav ul a:hover {
    background-position: 50% 100%;
}

li.first a {
    border-top: 1px solid #FFF9EF;
    padding-top: 1.25em;
}

nav ul i {
    font: normal 10px Baskerville, Garamond, Palatino, "Palatino Linotype", "Hoefler Text", "Times New Roman", serif;
    display: block;
    letter-spacing: 0.05em;
}
section:after,
nav ul:after {
    content: ".";
    display: block;
    height: 0;
    clear: both;
    visibility: hidden;
}
```

### Создаем раскрывающееся меню для сайта

1
```
    <style type="text/css">
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>

```
###  display

Многоцелевое свойство, которое определяет, как элемент должен быть показан в документе.

Синтаксис
```
display: block | inline | inline-block | inline-table | list-item | none | run-in | table | table-caption | table-cell | table-column-group | table-column | table-footer-group | table-header-group | table-row | table-row-group
```
Значения
Список возможных значений этого свойства, понимаемый разными браузерами очень короткий — block, inline, list-item и none. Все остальные допустимые значения поддерживаются браузерами выборочно. 


- block   Элемент показывается как блочный. Применение этого значения для встроенных элементов, например тега span, заставляет его вести подобно блокам — происходит перенос строк в начале и в конце содержимого.                                          
- inline  Элемент отображается как встроенный. Использование блочных тегов, таких как div и p, автоматически создает перенос и показывает содержимое этих тегов с новой строки. Значение inline отменяет эту особенность, поэтому содержимое блочных элементов начинается с того места, где окончился предыдущий элемент.                                         
- inline-block    Это значение генерирует блочный элемент, который обтекается другими элементами веб-страницы подобно встроенному элементу. Фактически такой элемент по своему действию похож на встраиваемые элементы (вроде тега img). При этом его внутренняя часть форматируется как блочный элемент, а сам элемент — как встроенный.                                           
- inline-table    Определяет, что элемент является таблицей как при использовании тега table, но при этом таблица является встроенным элементом и происходит ее обтекание другими элементами, например, текстом.                                            
- list-item   Элемент выводится как блочный и добавляется маркер списка.                                          
- none    Временно удаляет элемент из документа. Занимаемое им место не резервируется и веб-страница формируется так, словно элемента и не было. Изменить значение и сделать вновь видимым элемент можно с помощью скриптов, обращаясь к свойствам через объектную модель. В этом случае происходит переформатирование данных на странице с учетом вновь добавленного элемента.                                           
- run-in  Устанавливает элемент как блочный или встроенный в зависимости от контекста.                                            
- table   Определяет, что элемент является блочной таблицей подобно использованию тега table.                                           
- table-caption   Задает заголовок таблицы подобно применению тега caption.                                          
- table-cell  Указывает, что элемент представляет собой ячейку таблицы (тег td или th).                                            
- table-column    Назначает элемент колонкой таблицы, словно был добавлен тег col.                                           
- table-column-group  Определяет, что элемент является группой одной или более колонок таблицы, как при использовании тега colgroup.                                             
- table-footer-group  Используется для хранения одной или нескольких строк ячеек, которые отображаются в самом низу таблицы. По своему действию сходно с работой тега tfoot.
- table-header-group  Элемент предназначен для хранения одной или нескольких строк ячеек, которые представлены вверху таблицы. По своему действию сходно с работой тега <thead>.                                           
table-row   Элемент отображается как строка таблицы (тег <tr>).                                          
table-row-group Создает структурный блок, состоящий из нескольких строк таблицы аналогично действию тега tbody.                                            
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>display</title>
  <style>
   .example {
    border: dashed 1px #634f36; /* Параметры рамки */
    background: #fffff5; /* Цвет фона */
    font-family: "Courier New", Courier, monospace; /* Шрифт текста */
    padding: 7px; /* Поля вокруг текста */
    margin: 0 0 1em; /* Отступы вокруг */
   }
   .exampleTitle {
    border: 1px solid black; /* Параметры рамки */
    border-bottom: none; /* Убираем линию снизу */
    padding: 3px; /* Поля вокруг текста */
    display: inline; /* Устанавливаем как встроенный элемент */
    background: #efecdf; /* Цвет фона */
    font-weight: bold; /* Жирное начертание */
    font-size: 90%; /* Размер текста */
    margin: 0; /* Убираем отступы вокруг */
    white-space: nowrap; /* Отменяем переносы текста */
   }
  </style>
 </head> 
 <body> 
  <p class="exampleTitle">Пример</p>
  <p class="example">
  &lt;!DOCTYPE HTML PUBLIC &quot;-//W3C//DTD HTML 4.01 Transitional//EN&quot;&gt;<br>
  &lt;html&gt;<br>
  &lt;body&gt;<br>
  &lt;b&gt;Формула серной кислоты:&lt;/b&gt;
  &lt;i&gt;H&lt;sub&gt;&lt;small&gt;2&lt;/small&gt;&lt;/sub&gt;
  SO&lt;sub&gt;&lt;small&gt;4&lt;/small&gt;
  &lt;/sub&gt;&lt;/i&gt;<br>
  &lt;/body&gt;<br>
  &lt;/html&gt;</p>
 </body>
</html>
```

## list-style
Универсальное свойство, позволяющее одновременно задать стиль маркера, его положение, а также изображение, которое будет использоваться в качестве маркера. Для подробного ознакомления смотрите информацию о каждом свойстве list-style-type, list-style-position и list-style-image отдельно.

Синтаксис
```
list-style: list-style-type || list-style-position || list-style-image | inherit
```
Значения
Любые комбинации трех значений определяющих стиль маркеров, они разделяются между собой пробелом. Комбинации значений должны следовать в указанном порядке: вначале идет тип маркера, затем положение и картинка. Ни одно значение не является обязательным, поэтому неиспользуемые можно опустить.

- inherit Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>list-style</title>
  <style>
   ul {
    list-style: square outside; /* Квадратные маркеры */
                               /* Маркеры размещаются за 
                                  пределами текстового блока */
   }
  </style>
 </head> 
 <body> 
  <ul>
   <li>Lorem ipsum dolor sit amet</li>
   <li>Consectetuer adipiscing elit</li>
   <li>Sed diem nonummy nibh euismod</li>
   <li>Tincidunt ut lacreet dolore magna aliguam erat volutpat. Ut wisis 
    enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit lobortis 
    nisl ut aliquip ex ea commodo consequat.</li>
  </ul>
 </body>
</html>
```
### list-style: list-style-type
Изменяет вид маркера для каждого элемента списка. Это свойство используется только в случае, когда значение list-style-image установлено как none. Маркеры различаются для маркированного списка (тег ul) и нумерованного (тег ol).

Синтаксис
```
list-style-type: circle | disc | square | armenian | decimal | decimal-leading-zero | georgian | lower-alpha | lower-greek | lower-latin | lower-roman | upper-alpha | upper-latin | upper-roman | none | inherit
```

Значения зависят от того, к какому типу списка они применяются: маркированному или нумерованному.

### Маркированный список
- circle
Маркер в виде кружка.
- disc
Маркер в виде точки.
- square
Маркер в виде квадрата.
### Нумерованный список
- armenian
Традиционная армянская нумерация.
- decimal
Арабские числа (1, 2, 3, 4,...).
- decimal-leading-zero
Арабские числа с нулем впереди для цифр меньше десяти (01, 02, 03,...).
- georgian
Традиционная грузинская нумерация.
- lower-alpha
Строчные латинские буквы (a, b, c, d,...).
- lower-greek
Строчные греческие буквы (α, β, γ, δ,...).
- lower-latin
Это значение аналогично lower-alpha.
- lower-roman
Римские числа в нижнем регистре (i, ii, iii, iv, v,...).
- upper-alpha
Заглавные латинские буквы (A, B, C, D,...).
- upper-latin
Это значение аналогично upper-alpha.
- upper-roman
Римские числа в верхнем регистре (I, II, III, IV, V,...).
- none
Отменяет маркеры для списка.
- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>list-style-type</title>
  <style>
   ol {
    list-style-type: upper-alpha; /* Заглавные буквы */
   }
  </style>
 </head>
 <body> 
  <ol>
   <li>Lorem ipsum dolor sit amet</li>
   <li>Consectetuer adipiscing elit</li>
   <li>Sed diem nonummy nibh euismod</li>
   <li>Tincidunt ut lacreet dolore magna aliguam erat volutpat. Ut wisis 
    enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit lobortis 
    nisl ut aliquip ex ea commodo consequat.</li>
   </ol>
 </body>
 </html>
 ```
### list-style-position 

Определяет, как будет размещаться маркер относительно текста. Имеется два значения: outside — маркер вынесен за границу элемента списка и inside — маркер обтекается текстом.

Синтаксис
```
list-style-position: inside | outside
```
Значения
- inside
Маркер является частью текстового блока и отображается в элементе списка.
- outside
Текст выравнивается по левому краю, а маркеры размещаются за пределами текстового блока.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>list-style-position</title>
  <style>
   ul {
    list-style-image: url(images/book.gif); /* Путь к рисунку для установки маркера */
    list-style-position: inside; /* Маркер обтекается текстом */
   }
  </style>
 </head> 
 <body> 
  <ul>
   <li>Lorem ipsum dolor sit amet</li>
   <li>Consectetuer adipiscing elit</li>
   <li>Sed diem nonummy nibh euismod</li>
   <li>Tincidunt ut lacreet dolore magna aliguam erat volutpat. Ut wisis 
   enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit lobortis 
   nisl ut aliquip ex ea commodo consequat.</li>
  </ul>
 </body>
</html>
```
### list-style-image
Устанавливает адрес изображения, которое служит в качестве маркера списка. Это свойство наследуется, поэтому для отдельных элементов списка для восстановления маркера используется значение none.

Синтаксис
```
list-style-image: none | url('путь к файлу') | inherit
```
Значения
- none
Отменяет изображение в качестве маркера для родительского элемента.
- url
Относительный или абсолютный путь к графическому файлу. Значение можно указывать в одинарных, двойных кавычках или без них.
- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>list-style-image</title>
  <style>
   ul {
    list-style-image: url(images/book.gif);
   }
  </style>
 </head> 
 <body> 
  <ul>
   <li>Lorem ipsum dolor sit amet</li>
   <li>Consectetuer adipiscing elit</li>
   <li>Sed diem nonummy nibh euismod</li>
   <li>Tincidunt ut lacreet dolore magna aliguam erat volutpat. Ut wisis 
   enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit lobortis 
   nisl ut aliquip ex ea commodo consequat.</li>
  </ul>
 </body>
</html> 
```

2. 

```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>

```
## position

Устанавливает способ позиционирования элемента относительно окна браузера или других объектов на веб-странице.

Синтаксис
```
position: absolute | fixed | relative | static | inherit
```
Значения
- absolute
Указывает, что элемент абсолютно позиционирован, при этом другие элементы отображаются на веб-странице словно абсолютно позиционированного элемента и нет. Положение элемента задается свойствами left, top, right и bottom, также на положение влияет значение свойства position родительского элемента. Так, если у родителя значение position установлено как static или родителя нет, то отсчет координат ведется от края окна браузера. Если у родителя значение position задано как fixed, relative или absolute, то отсчет координат ведется от края родительского элемента.
- fixed
По своему действию это значение близко к absolute, но в отличие от него привязывается к указанной свойствами left, top, right и bottom точке на экране и не меняет своего положения при прокрутке веб-страницы. Браузер Firefox вообще не отображает полосы прокрутки, если положение элемента задано фиксированным, и оно не помещается целиком в окно браузера. В браузере Opera хотя и показываются полосы прокрутки, но они никак не влияют на позицию элемента.
- relative
Положение элемента устанавливается относительно его исходного места. Добавление свойств left, top, right и bottom изменяет позицию элемента и сдвигает его в ту или иную сторону от первоначального расположения.
- static
Элементы отображаются как обычно. Использование свойств left, top, right и bottom не приводит к каким-либо результатам.
- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>position</title>
  <style>
   .layer1 {
    position: relative; /* Относительное позиционирование */
    background: #f0f0f0; /* Цвет фона */
    height: 200px; /* Высота блока */
   }
   .layer2 {
    position: absolute; /* Абсолютное позиционирование */
    bottom: 15px; /* Положение от нижнего края */
    right: 15px; /* Положение от правого края */
    line-height: 1px;
   }
  </style>
 </head>
 <body>
  <div class="layer1">
   <div class="layer2">
     <img src="images/girl.jpg" alt="Девочка" />
   </div>
  </div>
 </body>
</html>
```

## float

Определяет, по какой стороне будет выравниваться элемент, при этом остальные элементы будут обтекать его с других сторон. Когда значение свойства float равно none, элемент выводится на странице как обычно, при этом допускается, что одна строка обтекающего текста может быть на той же линии, что и сам элемент.

Синтаксис
```
float: left | right | none | inherit
```
Значения
- left
Выравнивает элемент по левому краю, а все остальные элементы, вроде текста, обтекают его по правой стороне.
- right
Выравнивает элемент по правому краю, а все остальные элементы обтекают его по левой стороне.
- none
Обтекание элемента не задается.
- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>float</title>
  <style>
   .layer1 {
    float: left; /* Обтекание по правому краю */
    background: #fd0; /* Цвет фона */
    border: 1px solid black; /* Параметры рамки */
    padding: 10px; /* Поля вокруг текста */
    margin-right: 20px; /* Отступ справа */
    width: 40%; /* Ширина блока */
   }
  </style>
 </head> 
 <body> 
  <div class="layer1">
   Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem nonummy nibh 
   euismod tincidunt ut lacreet dolore magna aliguam erat volutpat.
  </div>
  <div>
   Duis autem dolor in hendrerit in vulputate velit esse molestie consequat, vel 
   illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio 
   dignissim qui blandit praesent luptatum zzril delenit au gue duis dolore te 
   feugat nulla facilisi.
  </div>
 </body>
</html>
```

3 

```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>

```

4 

```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }

    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>


```
5 
```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>


```


6. 

```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    ul.submenu {
    display: none;
    position: absolute;
    width: 120px;
    top: 37px;
    left: 0;
    background-color: white;
    border: 1px solid red;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>
```

7. display: block; 

```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    ul.submenu {
    /*display: none;*/
    position: absolute;
    width: 120px;
    top: 37px;
    left: 0;
    background-color: white;
    border: 1px solid red;
    }
    ul.submenu > li {
    display: block;
    }

    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>
```

8 
```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    ul.submenu {
    /*display: none;*/
    position: absolute;
    width: 120px;
    top: 37px;
    left: 0;
    background-color: white;
    border: 1px solid red;
    }
    ul.submenu > li {
    display: block;
    }
ul.submenu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
}
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>
```

9 
```
    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    ul.submenu {
    display: none;
    position: absolute;
    width: 120px;
    top: 37px;
    left: 0;
    background-color: white;
    border: 1px solid red;
    }
    ul.submenu > li {
    display: block;
    }
ul.submenu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
}
ul.submenu > li > a:hover {
    text-decoration: underline;
}
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>
```
10  
```
body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }

    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    ul.submenu {
    display: none;
    position: absolute;
    width: 120px;
    top: 37px;
    left: 0;
    background-color: white;
    border: 1px solid red;
    }
    ul.submenu > li {
    display: block;
    }
ul.submenu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
}
ul.submenu > li > a:hover {
    text-decoration: underline;
}
    ul.menu > li:hover > ul.submenu {
    display: block;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>
```

11  
```
ul:after { 
    display: block; 
    content: ' '; 
    clear: both; 
    float: none; 
}

    body {
        font: 14px 'Verdana';
        margin: 0;
        padding: 0;
    }
    .center-text {
    width: 80%;
    height: auto;
    font-size: 1.4em;
    text-align: left;
    background-color: #fafafa;
    border: solid 1px lightgray;
    }
    ul {
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    }
ul:after {
    display: block;
    content: ' ';
    clear: both;
    float: none;
}
    ul.menu > li {
    float: left;
    position: relative;
    }
    ul.menu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
    }
    ul.menu > li > a:hover {
    background-color: black;
    }
    ul.submenu {
    display: none;
    position: absolute;
    width: 120px;
    top: 37px;
    left: 0;
    background-color: white;
    border: 1px solid red;
    }
    ul.submenu > li {
    display: block;
    }
ul.submenu > li > a {
    display: block;
    padding: 10px;
    color: white;
    background-color: red;
    text-decoration: none;
}
ul.submenu > li > a:hover {
    text-decoration: underline;
}
    ul.menu > li:hover > ul.submenu {
    display: block;
    }
    </style>
</head>
<ul class="menu">
    <li><a href=#>Menu 1</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
            <li><a href=#>Sudmenu 1</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 2</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
            <li><a href=#>Sudmenu 2</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 3</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
            <li><a href=#>Sudmenu 3</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 4</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
            <li><a href=#>Sudmenu 4</a></li>
        </ul>
    </li>
    <li><a href=#>Menu 5</a>
        <ul class="submenu">
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
            <li><a href=#>Sudmenu 5</a></li>
        </ul>
    </li>
</ul>
```
## Задание

- Изменить горизонтальное меню на вертикальное

