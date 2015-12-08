# 11-css-danco
unit 09
=======

```
<!--///////////////////////////////////////////////////////
    // portfolio section 
//////////////////////////////////////////////////////////-->


 <section class="portfolio-paralax" id="portfolio">
    <section class="portfolio-back">
      <div class="w-container">
        <div class="wrap">
          

            <div class="portfolio">
              <h1 class="portfolio-heading">PORTFOLIO</h1>
              <div class="portfolio-text">OUR WORK</div>
              <div class="sepreater"></div>
            </div>
          
          
        </div>
      </div>
    </section>
  </section>


<!--///////////////////////////////////////////////////////
    // End portfolio section 
 //////////////////////////////////////////////////////////-->


.portfolio-paralax {
  background: url('images/parlex.png');
  padding-top: 0px;
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;

}
.portfolio-back {
  padding-top: 15px;
  background-color: transparent;
  background-image: -webkit-linear-gradient(rgba(72, 207, 173, 0.99), rgba(72, 207, 173, 0.78));
  background-image: -o-linear-gradient(rgba(72, 207, 173, 0.99), rgba(72, 207, 173, 0.78));
  background-image: linear-gradient(rgba(72, 207, 173, 0.99), rgba(72, 207, 173, 0.78));
}

```
box-shadow:
-------------
Добавляет тень к элементу. Допускается использовать несколько теней, указывая их параметры через запятую, при наложении теней первая тень в списке будет выше, последняя ниже. Если для элемента задается радиус скругления через свойство border-radius, то тень также получится с закругленными уголками. Добавление тени увеличивает ширину элемента, поэтому возможно появление горизонтальной полосы прокрутки в браузере.

Синтаксис
```
box-shadow: none | <тень> [,<тень>]*
где <тень>:
inset <сдвиг по x> <сдвиг по y> <радиус размытия> <растяжение> <цвет>
```
Значения
- none
Отменяет добавление тени.
- inset
Тень выводится внутри элемента. Необязательный параметр.
- сдвиг по x
Смещение тени по горизонтали относительно элемента. Положительное значение этого параметра задает сдвиг тени вправо, отрицательное — влево. Обязательный параметр.
- сдвиг по y
Смещение тени по вертикали относительно элемента. Положительное значение задает сдвиг тени вниз, отрицательное — вверх. Обязательный параметр.
- размытие
Задает радиус размытия тени. Чем больше это значение, тем сильнее тень сглаживается, становится шире и светлее. Если этот параметр не задан, по умолчанию устанавливается равным 0, тень при этом будет четкой, а не размытой.
- растяжение
Положительное значение растягивает тень, отрицательное, наоборот, ее сжимает. Если этот параметр не задан, по умолчанию устанавливается 0, при этом тень будет того же размера, что и элемент.
- цвет
Цвет тени в любом доступном CSS формате, по умолчанию тень черная. Необязательный параметр.
Допускается указывать несколько теней, разделяя их параметры между собой запятой. Учитывается следующий порядок: первая тень в списке размещается на самом верху, последняя в списке — в самом низу.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>box-shadow</title>
  <style>
   .shadow {
    background: #fc0; /* Цвет фона */
    box-shadow: 0 0 10px rgba(0,0,0,0.5); /* Параметры тени */
    padding: 10px;
   }
  </style>
 </head>
 <body>
  <div class="shadow">В чащах юга жил бы цитрус? Да, но фальшивый экземпляр!</div> 
 </body>
</html>
```
portfolio section
-----------------
```
<!--///////////////////////////////////////////////////////
    // 
//////////////////////////////////////////////////////////-->


  <section class="service-paralax" id="portfolio">
    <section class="portfolio-back">
      <div class="w-container">
        <div class="wrap">
          

            <div class="portfolio">
              <h1 class="portfolio-heading">PORTFOLIO</h1>
              <div class="portfolio-text">OUR WORK</div>
              <div class="sepreater"></div>
            </div>
            <p class="porfolio-paragraph">THE BEST RESULTS ARE OBTAINED BY TASKING THE RIGHT PEOPLE TO THE RIGHT PROJECT
            <br>We do what we love. Our clients love what we do.</p>


            <div class="container demo-1">
              <ul class="grid cs-style-1">
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/1.jpg" alt="img01">
                    <figcaption>
                      <h3>Camera</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/2.jpg" alt="img02">
                    <figcaption>
                      <h3>Music</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/4.jpg" alt="img04">
                    <figcaption>
                      <h3>Settings</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/5.jpg" alt="img05">
                    <figcaption>
                      <h3>Safari</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/3.jpg" alt="img03">
                    <figcaption>
                      <h3>Phone</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/6.jpg" alt="img06">
                    <figcaption>
                      <h3>Game Center</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/7.jpg" alt="img06">
                    <figcaption>
                      <h3>Game Center</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/8.jpg" alt="img06">
                    <figcaption>
                      <h3>Game Center</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
                <li>
                  <figure>
                    <img class="portfolio-images" src="images/portfolio/9.jpg" alt="img06">
                    <figcaption>
                      <h3>Game Center</h3>
                      <span>Jacob Cummings</span>
                      <a href="#">Take a look</a>
                    </figcaption>
                  </figure>
                </li>
              </ul>
            </div><!-- /container -->
          
          
        </div>
      </div>
    </section>
  </section>


<!--///////////////////////////////////////////////////////
    // End portfolio section 
 //////////////////////////////////////////////////////////-->


.portfolio-images {
  border: 10px solid #FFF;
  margin-bottom: 10px;
  margin-right: 15px;
  box-shadow: 5px 5px 0px #20AE61;
}


 ```

Радиус скругления для создания разных типов уголков border-radius:
-------------------------------------------------------------------

Устанавливает радиус скругления уголков рамки. Если рамка не задана, то скругление также происходит и с фоном.

Синтаксис
```
border-radius: <радиус>{1,4} [ / <радиус>{1,4}]
```
Значения
Разрешается использовать одно, два, три или четыре значения, перечисляя их через пробел. Также допустимо писать два значения через слэш (/). В качестве значений указываются числа в любом допустимом для CSS формате. В случае применения процентов, отсчет ведется относительно ширины блока.

Зависимость от числа значений
-----------------------------

- 1 Радиус указывается для всех четырех уголков.
- 2 Первое значение задает радиус верхнего левого и нижнего правого уголка, второе значение — верхнего правого и нижнего левого уголка.
- 3 Первое значение задает радиус для верхнего левого уголка, второе — одновременно для верхнего правого и нижнего левого, а третье — для нижнего правого уголка.
- 4 По очереди устанавливает радиус для верхнего левого, верхнего правого, нижнего правого и нижнего левого уголка.
В случае задания двух параметров через слэш, то первый задает радиус по горизонтали, а второй по вертикали (эллиптические уголки).

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>border-radius</title>
  <style>
   .radius {
    background: #f0f0f0; /* Цвет фона */
    border: 1px solid black; /* Параметры рамки */
    padding: 15px; /* Поля вокруг текста */
    margin-bottom: 10px; /* Отступ снизу */
   }
  </style>
 </head> 
 <body> 
  <div style="border-radius: 50px 0 0 50px;" class="radius">
   border-radius: 50px 0 0 50px;
  </div>
  <div style="border-radius: 40px 10px" class="radius">
   border-radius: 40px 10px;
  </div>
  <div style="border-radius: 10em/1em;" class="radius">
   border-radius: 13em/3em;
  </div>
  <div style="border-radius: 13em 0.5em/1em 0.5em;" class="radius">
   border-radius: 13em 0.5em/1em 0.5em;
  </div>
  <div style="border-radius: 8px;" class="radius">
   border-radius: 8px;
  </div>
 </body> 
</html>
```

 portfolio2.html
 ----------------
 ```
.grid {
  padding: 20px 20px 0px 20px;
  margin: 0 auto;
  list-style: none;
  text-align: center;
}

.grid li {
  display: inline-block;
  width: 210px;
  margin: 0;
  text-align: left;
  position: relative;
  margin-right: 20px;
  margin-bottom: 15px;
}

.grid figure {
  margin: 0;
  position: relative;
}

.grid figure img {
  max-width: 100%;
  display: block;
  position: relative;
}

.grid figcaption {
  position: absolute;
  top: 0;
  left: 0;
  padding: 20px;
  background: #2c3f52;
  color: #ed4e6e;
}

.grid figcaption h3 {
  margin: 0;
  padding: 0;
  color: #fff;
}

.grid figcaption span:before {
  content: 'by ';
}

.portfolio-images {
  border: 10px solid #FFF;
margin-bottom: 10px;
margin-right: 15px;
box-shadow: 5px 5px 0px #20AE61;
}

.grid figcaption a {
  text-align: center;
  padding: 5px 10px;
  border-radius: 2px;
  display: inline-block;
  background: #ed4e6e;
  color: #fff;
}
 ```
opacity:
---------

Определяет уровень прозрачности элемента веб-страницы. При частичной или полной прозрачности через элемент проступает фоновый рисунок или другие элементы, расположенные ниже полупрозрачного объекта.

В качестве значения выступает число из диапазона [0.0; 1.0]. Значение 0 соответствует полной прозрачности элемента, а 1, наоборот — его непрозрачности. Дробные числа вида 0.6 устанавливают полупрозрачность. Допускается писать числа без нуля впереди, вида opacity: .6.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>opacity</title>
  <style>
   .semi {
    opacity: 0.5; /* Полупрозрачность элемента */
   }
  </style>
 </head>
 <body>
  <p>
    <img src="images/igels.png" alt="Обычный рисунок">
    <img src="images/igels.png" alt="Полупрозрачный рисунок" class="semi">
  </p>
 </body>
</html>
```
-webkit-backface-visibility
---------------------------
Свойство -webkit-backface-visibility определяет будет ли видно контент элемента, который с помощью 3d трансформаций отвернут лицом от пользователя.

Допустимые значения

- visible — контент элемента виден даже тогда, когда элемент отвернут лицом от пользователя
- hidden — если элемент отвернут лицом от пользователя, контент этого элемента не виден
- Значение по умолчанию visible
- Применимо к блочным и строчным элементам
- Наследование  нет

Поддерживается браузерами 
---------------------------
Safari 4.0.3/Mac OS X и выше, и с Safari 5/Win и выше
Пример

```
div {
width:100px;
height:50px;
-webkit-transform:rotate3d(0, 0, -1, 170deg) skewX(15deg);
-webkit-backface-visibility:hidden;
}
```
transform:
-----------

Трансформирует элемент, в частности, позволяет его масштабировать, вращать, сдвигать, наклонять, а также комбинировать виды трансформаций.

Синтаксис
```
transform: <функция> [<функция>]* | none
```
Значения
- функция
- Функция трансформации.
- none
Отменяет действие трансформации.
- Функции трансформации
- matrix
Задаёт матрицу преобразований.

- rotate
Поворот элемента на заданный угол относительно точки трансформации, задаваемой свойством transform-origin.
```
transform: rotate(<угол>)
```
- scale
Масштаб элемента по горизонтали и вертикали.
```
transform: scale(sx[, sy]);
```
Значение больше 1 увеличивает масштаб элемента, меньше 1 — уменьшает масштаб.

- scaleX
Масштабирует элемент по горизонтали.
```
transform: scaleX(sx);
```
- scaleY
Масштабирует элемент по вертикали.
```
transform: scaleY(sy);
```
- skewX
Наклоняет элемент на заданный угол по вертикали.
```
transform: skewX(<угол>)
```
- skewY
Наклоняет элемент на заданный угол по горизонтали.
```
transform: skewY(<угол>)
```
- translate
Сдвигает элемент на заданное значение по горизонтали и вертикали.
```
transform: translate(tx[, ty])
```
- translateX
Сдвигает элемент по горизонтали на указанное значение. Положительное значение сдвигает вправо, отрицательное влево.
```
transform: translateX(tx)
```
- translateY
Сдвигает элемент по вертикали на указанное значение. Положительное значение сдвигает вниз, отрицательное вверх.
```
transform: translateY(ty)
```
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>transform</title>
  <style>
   .turn:hover {
    -moz-transform: rotate(15deg); /* Для Firefox */
    -ms-transform: rotate(15deg); /* Для IE */
    -webkit-transform: rotate(15deg); /* Для Safari, Chrome, iOS */
    -o-transform: rotate(15deg); /* Для Opera */
    transform: rotate(15deg);
   }
  </style>
 </head>
 <body>
  <p><img src="images/igels.png" alt="Ёжик" class="turn">
     <img src="images/igels.png" alt="Ёжик" class="turn"></p>
 </body>
</html>
```

portfolio3.html
----------------
 ```
/* Individual Caption Styles */

/* Caption Style 1 */
.cs-style-1 figcaption {
  height: 100%;
  width: 100%;
  opacity: 0;
  text-align: center;
  -webkit-backface-visibility: hidden;
  -moz-backface-visibility: hidden;
  backface-visibility: hidden;
  -webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
  -moz-transition: -moz-transform 0.3s, opacity 0.3s;
  transition: transform 0.3s, opacity 0.3s;
}

.no-touch .cs-style-1 figure:hover figcaption,
.cs-style-1 figure.cs-hover figcaption {
  opacity: 1;
  -webkit-transform: translate(15px, 15px);
  -moz-transform: translate(15px, 15px);
  -ms-transform: translate(15px, 15px);
  transform: translate(15px, 15px);
}

.cs-style-1 figcaption h3 {
  margin-top: 25px;
}

.cs-style-1 figcaption span {
  display: block;
}

.cs-style-1 figcaption a {
  margin-top: 30px;
}

.no-touch .cs-style-7 figure:hover figcaption h3,
.no-touch .cs-style-7 figure:hover figcaption span,
.no-touch .cs-style-7 figure:hover figcaption a,
.cs-style-7 figure.cs-hover figcaption h3,
.cs-style-7 figure.cs-hover figcaption span,
.cs-style-7 figure.cs-hover figcaption a {
  -webkit-transition: opacity 0.3s 0.2s;
  -moz-transition: opacity 0.3s 0.2s;
  transition: opacity 0.3s 0.2s;
  opacity: 1;
}
 ```

transition:
-----------

Универсальное свойство, которое позволяет одновременно задать значения transition-property, transition-duration, transition-timing-function и transition-delay. Устанавливает эффект перехода между двумя состояниями элемента, они могут быть определены с помощью псевдоэлемента :hover или :active, а также динамически через JavaScript.

Синтаксис
```
transition: <переход> [, <переход> ]*
```
Здесь:
```
<переход> = [ none | <transition-property> ] || <transition-duration> || 
<transition-timing-function> || <transition-delay>
```
Значения
- none
Отменяет эффект перехода.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>transition</title>
  <style>
   #bar {
    top:-5.5em; right:5em; /* Положение */
     padding: .5em; /* Поля */
     margin: 0; /* Отступы */
     position: absolute; /* Абсолютное позиционирование */
     width: 2em; /* Ширина */
     background: #333; /* Цвет фона */
     color: #fff; /* Цвет текста */
     text-align: center; /* Выравнивание по центру */
     /* Переход */
     -webkit-transition: top 1s ease-out 0.5s;
     -moz-transition: top 1s ease-out 0.5s;
     -o-transition: top 1s ease-out 0.5s;
     transition: top 1s ease-out 0.5s;
    }
   #bar:hover { top: 0; }
  </style>
 </head>
 <body>
  <ul id="bar">
   <li>1</li><li>2</li>
   <li>3</li><li>4</li>
   <li>&darr;</li>
  </ul>
 </body>
</html>
```

Правило @media
---------------
Правило @media позволяет указать тип носителя, для которого будет применяться указанный стиль. В качестве типов выступают различные устройства, например, принтер, КПК, монитор и др. В табл. 1 перечислены некоторые из них.

Типы носителей и их описание
-----------------------------

- all Все типы. Это значение используется по умолчанию.
- aural Речевые синтезаторы, а также программы для воспроизведения текста вслух. Сюда, например, можно отнести речевые браузеры.
- braille Устройства, основанные на системе Брайля, которые предназначены для слепых людей.
- handheld  Наладонные компьютеры и аналогичные им аппараты.
- print Печатающие устройства вроде принтера.
- projection  Проектор.
- screen  Экран монитора.
- tv  Телевизор.
Синтаксис
```
@media тип1 [, тип2] {
  Описание стиля 
}
```
Значения
После ключевого слова @media идет один или несколько типов носителя, перечисленных в табл. 1; если их больше одного, то они разделяются между собой запятой. После чего следуют обязательные фигурные скобки, внутри которых идет обычное описание стилевых правил.

Пример 
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" 
  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>@media</title>
  <style type="text/css">
   @media screen { /* Стиль для отображения в браузере */
    body {
     font-family: Arial, Verdana, sans-serif; /* Рубленый шрифт */
     font-size: 0.9em; /* Размер шрифта */
     color: #000080; /* Цвет текста */
    }
    h1 {
     background: #faf0e6; /* Цвет фона под текстом */
     border: 2px dashed #800000; /* Рамка вокруг заголовка */
     color: #a0522d; /* Цвет текста */
     padding: 7px; /* Поля вокруг текста */
    }
    h2 {
     color: #556b2f; /* Цвет текста */
     margin: 0; /* Убираем отступы */
    }
    p {
     margin-top: 0.5em; /* Отступ сверху */
    }
   }
   @media print { /* Стиль для печати */
    body {
     font-family: Times, 'Times New Roman', serif; /* Шрифт с засечками */
    }
    h1, h2, p {
     color: #000; /* Черный цвет текста */
    }
   }
  </style>
 </head>
 <body>
   <h1>Метод ловли льва в пустыне</h1>
   <h2>Метод последовательного перебора</h2>
   <p>Пусть лев имеет габаритные размеры LxWxH, где L — длина льва от кончика носа 
   до кисточки хвоста, W — ширина льва, а H — его высота. После чего пустыню разбиваем на 
   ряд элементарных прямоугольников, размер которых совпадает с шириной и длиной льва. 
   Учитывая, что лев может находиться не строго на заданном участке, а одновременно на 
   двух из них, клетку для ловли следует делать повышенной площади, а именно 2Lx2W. 
   Благодаря этому мы избежим ошибки, когда в клетке окажется пойманным лишь половина 
   льва или, что хуже, только его хвост.</p>
   <p>Далее последовательно накрываем каждый из размеченных прямоугольников пустыни 
   клеткой и проверяем, пойман лев или нет. Как только лев окажется в клетке, процедура 
   поимки считается завершенной.</p>
 </body>
</html>
```
В данном примере вводится два стиля — один для изменения вида элементов при их обычном отображении в браузере, а второй — при выводе страницы на печать. 


portfolio4.html
----------------

 ```
@media screen and (max-width: 31.5em) {
  .grid {
    padding: 10px 10px 100px 10px;
  }
  .grid li {
    width: 100%;
    min-width: 210px;
  }
}


 ```