# 11-css-danco

## reset.css

```
    <link rel="stylesheet" href="css/reset.css"> 
    /*  http://meyerweb.com/eric/tools/css/reset/ 
        v2.0 | 20110126
        License: none (public domain)
    */

```

## Тег img
﻿
Тег img предназначен для отображения на веб-странице изображений в графическом формате GIF, JPEG или PNG. Адрес файла с картинкой задаётся через атрибут src. Если необходимо, то рисунок можно сделать ссылкой на другой файл, поместив тег img в контейнер a. При этом вокруг изображения отображается рамка, которую можно убрать, добавив атрибут border="0" в тег img.

Рисунки также могут применяться в качестве карт-изображений, когда картинка содержит активные области, выступающие в качестве ссылок. Такая карта по внешнему виду ничем не отличается от обычного изображения, но при этом оно может быть разбито на невидимые зоны разной формы, где каждая из областей служит ссылкой.

Синтаксис
```
HTML    
<img src="URL" alt="альтернативный текст">
XHTML   
<img src="URL" alt="альтернативный текст" />
```
Атрибуты
- align
Определяет как рисунок будет выравниваться по краю и способ обтекания текстом.
- alt
Альтернативный текст для изображения.
- border
Толщина рамки вокруг изображения.
- height
Высота изображения.
- hspace
Горизонтальный отступ от изображения до окружающего контента.
- ismap
Говорит браузеру, что картинка является серверной картой-изображением.
- longdesc
Указывает адрес документа, где содержится аннотация к картинке.
- lowsrc
Адрес изображения низкого качества.
- src
Путь к графическому файлу.
- vspace
Вертикальный отступ от изображения до окружающего контента.
- width
Ширина изображения.
- usemap
Ссылка на тег map, содержащий координаты для клиентской карты-изображения.


Пример
```
<!DOCTYPE HTML>
<html>
 <head>
  <meta charset="utf-8">
  <title>Тег IMG</title>
 </head>
 <body> 

  <p><a href="lorem.html"><img src="images/girl.png" 
  width="189" height="255" alt="lorem"></a>
  Lorem ipsum dolor sit amet...</p>
  
  <a href="#"><img src="images/logo.png" alt="The Baker Street Inquirer" /></a>
 </body>
</html>
```

## Атрибут id
﻿
Задает стилевой идентификатор — уникальное имя элемента, которое используется для изменения его стиля и обращения к нему через скрипты. Идентификатор в коде документа должен быть в единственном экземпляре, иными словами, встречаться только один раз.

Синтаксис
```
id="имя"
```
Значения

Идентификатор должен обязательно начинаться с латинского символа и может содержать в себе латинские буквы (A–Z, a–z), цифры (0–9), символ дефиса (-) и подчеркивания (_). Использование русских букв в именах идентификатора недопустимо.

```
<div id="page"> 

<div class="inner"> 
```

## Тег ul
﻿
Тег ul устанавливает маркированный список. Каждый элемент списка должен начинаться с тега li. Если к тегу ul применяется таблица стилей, то элементы li наследуют эти свойства.

Синтаксис
```
<ul>
  <li>элемент маркированного списка</li>
</ul>
```
Атрибуты

- type
Устанавливает вид маркера списка.

Пример
```
<!DOCTYPE HTML>
<html>
 <head>
  <meta charset="utf-8">
  <title>Тег UL</title>
 </head>
 <body>

  <ul>
    <li>Чебурашка</li>
    <li>Крокодил Гена</li>
    <li>Шапокляк</li>
  </ul>

 </body>
</html>
```
Пример
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

Для отображения символов, которых нет на клавиатуре, применяются специальные знаки, начинающиеся с амперсанда (&) и заканчивающиеся точкой с запятой (;). 
некоторые популярные спецсимволы
```
&#8220;
&#8221;

&#8217;

&nbsp;

&amp;

&copy;
```
## Нумерованные списки

type="A | a | I | i | 1"


Нумерованные списки представляют собой набор элементов с их порядковыми номерами. Вид и тип нумерации зависит от атрибутов тега ol, который и используется для создания списка. В качестве маркеров могут быть следующие значения:

- заглавные латинские буквы;
- строчные латинские буквы;
- заглавные римские цифры;
- строчные римские цифры;
- арабские цифры.


### li type

Устанавливает вид маркера. Тип маркера и его значение зависит от внешнего контейнера ul или ol.

Для маркированного списка (тег ul) маркеры могут принимать один из трех видов: круг, окружность и квадрат.


## Тег figure
﻿
Используется для группирования любых элементов, например, изображений и подписей к ним.

Пример

```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8" />
  <title>Тег FIGURE</title>
  <script>
   document.createElement('figure');
   document.createElement('figcaption');
  </script>
  <style>
   figure {
    background: #5f6a72; /* Цвет фона */
    padding: 10px; /* Поля вокруг */
    display: block; /* Блочный элемент */
    width: 150px; /* Ширина */
    float: left; /* Блоки выстраиваются по горизонтали */
    margin: 0 10px 10px 0; /* Отступы */
    text-align: center; /* Выравнивание по центру */
   }
   figcaption {
    color: #fff; /* Цвет текста */
   }
  </style>
 </head>
 <body>
  <article>
   <figure>
    <p><img src="images/thumb1.jpg" alt="" /></p>
    <figcaption>Софийский собор</figcaption>
   </figure>
   <figure>
    <p><img src="images/thumb2.jpg" alt="" /></p>
    <figcaption>Польский костел</figcaption>
   </figure>
  </article>
 </body>
</html>

```
## Тег figcaption
﻿
Содержит описание для тега figure. Тег figcaption должен быть первым или последним элементом в группе.


```
    <section> 
        <article><!-- section.intro --> 
            <div class='intro'>      
            </div>   
        </article><!-- /end .section.intro --> 

    </section> 

    <footer> 

        <p>&copy; 2015 QALight. All rights reserved.</p> 
     
    </footer> 
```

### background

Применяется Ко всем элементам
Ссылка на спецификацию  http://www.w3.org/TR/CSS21/colors.html#propdef-background

Универсальное свойство background позволяет установить одновременно до пяти характеристик фона. Значения могут идти в любом порядке, браузер сам определит, какое из них соответствует нужному свойству. Для подробного ознакомления смотрите информацию о каждом свойстве отдельно. В CSS3 допустимо указывать параметры сразу нескольких фонов, перечисляя их через запятую.

Синтаксис
```
background: [background-attachment || background-color || background-image 
  || background-position || background-repeat] | inherit

background: [фон, ]* последний_фон
```
Здесь:
```
фон = [background-attachment || background-image || background-position || background-repeat] | inherit

последний_фон = [background-attachment || background-color || background-image || background-position || background-repeat] | inherit
```
Если наряду с фоновыми изображениями требуется задать цвет фона элемента, он указывается в последнюю очередь после перечисления.

Любые комбинации пяти значений, разделяемых между собой пробелом, определяющих стиль фона, в произвольном порядке. Ни одно значение не является обязательным, поэтому неиспользуемые можно опустить. inherit наследует значение у родительского элемента.

Пример 1
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" 
  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
  <title>background</title>
  <style type="text/css">
   div {
    height: 200px; /* Высота блока */
    width: 200px; /* Ширина блока */
    overflow: auto; /* Добавляем полосы прокрутки */
    padding-left: 15px; /* Отступ от текста слева */
    background: url(images/hand.png) repeat-y #fc0; /* Цвет фона, 
                                                    путь к фоновому изображению и 
                                                    повторение фона по вертикали */
   }
  </style>
 </head>
 <body>

  <div>
   Duis te feugifacilisi. Duis autem dolor in hendrerit in vulputate velit esse molestie 
   consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et 
   iusto odio dignissim qui blandit praesent luptatum zzril delenit au gue duis dolore
   te feugat nulla facilisi. Ut wisi enim ad minim veniam, quis nostrud exerci taion 
   ullamcorper suscipit lobortis nisl ut aliquip ex en commodo consequat. Duis te 
   feugifacilisi per suscipit lobortis nisl ut aliquip ex en commodo consequat.
  </div>

 </body>
</html>
```

Пример 2
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>background</title>
  <style>
   body {
    background: url(images/hand.png) repeat-y, 
                #fc0 url(images/bg-right.png) repeat-y 100% 0;
   }
  </style>
 </head>
 <body>
 </body>
</html>
```

Пример 3
```
h1 { 
    background: url("../images/logo-bg.png") no-repeat 50% 0; 
} 

#page { 
    background: url("../images/rag.png") repeat-x; 
    padding: 2em 0; 
} 

/* main styles */ 
body { 
    background: #E4E4E4 url("../images/bg.png"); 
    color: #292929; 
    color: rgba(0, 0, 0, 0.82); 
    font: normal 100% Cambria, Georgia, serif; 
    -moz-text-shadow: 0 1px 0 rgba(255, 255, 255, 0.8); 
    -webkit-text-shadow: 0 1px 0 rgba(255, 255, 255, 0.8); 
    text-shadow: 0 1px 0 rgba(255, 255, 255, 0.8); 
    -webkit-text-size-adjust: none; 
} 

```

### font

Универсальное свойство, которое позволяет одновременно задать несколько характеристик шрифта и текста.

Синтаксис
```
font: [font-style||font-variant||font-weight] font-size [/line-height] font-family | inherit
```
Значения
В качестве обязательных значений свойства font указывается размер шрифта и его семейство. Остальные значения являются опциональными и задаются при желании. Для подробного ознакомления смотрите информацию о каждом свойстве отдельно.

- inherit
Наследует значение родителя.

Допускается в качестве значения использовать ключевые слова, определяющие шрифт различных элементов операционной системы пользователя.

- caption
Шрифт для текста элементов форм вроде кнопок.
- icon
Шрифт для текста под иконками.
- menu
Шрифт применяемый в меню.
- message-box
Шрифт для диалоговых окон.
- small-caption
Шрифт для подписей к небольшим элементам управления.
- status-bar
Шрифт для строки состояния окон.
Примеры использования
```
p { font: 12pt/10pt sans-serif; }
```
Из типографики пошла запись указывать через слэш размер шрифта и межстрочное расстояние (интерлиньяж). Поэтому 12pt в данном случае означает размер основного текста в пунктах, а 10pt — интерлиньяж. В качестве семейства указывается рубленый шрифт (sans-serif).
```
p { font: bold italic 110% serif; }
```
Значение bold устанавливает жирное начертание текста, а italic — курсивное. В данном случае их порядок не важен, поэтому bold и italic можно поменять местами. Размер текста задается в процентах, а в качестве гарнитуры используется шрифт с засечками (serif).
```
p { font: normal small-caps 12px/14px fantasy; }
```
Значение small-caps принадлежит свойству font-variant и устанавливает текст в виде капители (заглавные буквы уменьшенного размера). Значение normal применяется сразу к двум свойствам: font-style и font-weight.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>font</title>
  <style>
   .layer1 {
    font: 12pt sans-serif;  
   } 
   h1 {
    font: 200% serif;
   }
  </style>
 </head>
 <body> 
  <div class="layer1">
  <h1>Duis te feugifacilisi</h1>
  Duis autem dolor in hendrerit in vulputate velit esse molestie consequat, vel 
  illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio 
  dignissim qui blandit praesent luptatum zzril delenit au gue duis dolore te 
  feugat nulla facilisi.
  </div>
 </body>
</html>
```

### font-family

Устанавливает семейство шрифта, которое будет использоваться для оформления текста содержимого. Список шрифтов может включать одно или несколько названий, разделенных запятой. Если в имени шрифта содержатся пробелы, например, Trebuchet MS, оно должно заключаться в одинарные или двойные кавычки.

Когда браузер встречает первый шрифт в списке, он проверяет его наличие на компьютере пользователя. Если такого шрифта нет, берется следующее имя из списка и также анализируется на присутствие. Поэтому несколько шрифтов увеличивает вероятность, что хотя бы один из них будет обнаружен на клиентском компьютере. Заканчивают список обычно ключевым словом, которое описывает тип шрифта — serif, sans-serif, cursive, fantasy или monospace. Таким образом, последовательность шрифтов лучше начинать с экзотических типов и заканчивать обобщенным именем, которое задает вид начертания.

Синтаксис
```
font-family: имя шрифта [, имя шрифта[, ...]] | inherit
```
Любое количество имен шрифтов разделенных запятыми. Универсальные семейства шрифтов:

- serif — шрифты с засечками (антиквенные), типа Times;
- sans-serif — рубленные шрифты (шрифты без засечек или гротески), типичный представитель — Arial;
- cursive — курсивные шрифты;
- fantasy — декоративные шрифты;
- monospace — моноширинные шрифты, ширина каждого символа в таком семействе одинакова (шрифт Courier).
- inherit Наследует значение родителя.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>font-family</title>
  <style>
   h1 {
    font-family: Geneva, Arial, Helvetica, sans-serif;
   } 
   p {
    font-family: Georgia, 'Times New Roman', Times, serif;
   }
  </style>
 </head> 
 <body> 
  <h1>Duis te feugifacilisi</h1>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem 
  nonummy nibh euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. 
  Ut wisis enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit 
  lobortis nisl ut aliquip ex ea commodo consequat.</p>
 </body>
</html>
```

## font-style
Определяет начертание шрифта — обычное, курсивное или наклонное. Когда для текста установлено курсивное или наклонное начертание, браузер обращается к системе для поиска подходящего шрифта. Если заданный шрифт не найден, браузер использует специальный алгоритм для имитации нужного вида текста. Результат и качество при этом могут получиться неудовлетворительными, особенно при печати документа.

Синтаксис
```
font-style: normal | italic | oblique | inherit
```
Значения
- normal
Обычное начертание текста.
- italic
Курсивное начертание.
- oblique
Наклонное начертание. Курсив и наклонный шрифт при всей их похожести не одно и то же. Курсив это специальный шрифт имитирующий рукописный, наклонный же образуется путем наклона обычных знаков вправо.
- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>font-style</title>
  <style>
   h1 {
    font-family: Verdana, Arial, Helvetica, sans-serif; /* Рубленый шрифт заголовка */
   } 
   p {
    font-family: 'Times New Roman', Times, serif; /* Шрифт с засечками */
    font-style: italic; /* Курсивное начертание */
   }
  </style>
 </head>
 <body> 
  <h1>Duis te feugifacilisi</h1>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem 
  nonummy nibh euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. 
  Ut wisis enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit 
  lobortis nisl ut aliquip ex ea commodo consequat.</p>
 </body>
</html>
```

## font-size

Определяет размер шрифта элемента. Размер может быть установлен несколькими способами. Набор констант (xx-small, x-small, small, medium, large, x-large, xx-large) задает размер, который называется абсолютным. По правде говоря, они не совсем абсолютны, поскольку зависят от настроек браузера и операционной системы.

Другой набор констант (larger, smaller) устанавливает относительные размеры шрифта. Поскольку размер унаследован от родительского элемента, эти относительные размеры применяются к родительскому элементу, чтобы определить размер шрифта текущего элемента.

В конечном итоге, размер шрифта сильно зависит от значения свойства font-size у родителя элемента.

Сам размер шрифта определяется как высота от базовой линии до верхней границы кегельной площадки, как показано на 

Синтаксис
```
font-size: абсолютный размер | относительный размер | значение | проценты | inherit
```
Для задания абсолютного размера используются следующие значения: xx-small, x-small, small, medium, large, x-large, xx-large.

Размер шрифта в CSS и HTML
```
CSS     xx-small    x-small small   medium  large   x-large xx-large     
HTML    1           2       3       4       5       6       7
```
Относительный размер шрифта задается значениями larger и smaller.

Также разрешается использовать любые допустимые единицы CSS: em (высота шрифта элемента), ex (высота символа х), пункты (pt), пикселы (px), проценты (%) и др. За 100% берется размер шрифта родительского элемента. Отрицательные значения не допускаются.

- inherit Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>font-size</title>
  <style>
   h1 {
    font-family: 'Times New Roman', Times, serif; /* Гарнитура текста */ 
    font-size: 250%; /* Размер шрифта в процентах */ 
   } 
   p {
    font-family: Verdana, Arial, Helvetica, sans-serif; 
    font-size: 11pt; /* Размер шрифта в пунктах */ 
   }
  </style>
 </head> 
 <body> 
  <h1>Duis te feugifacilisi</h1>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem 
  nonummy nibh euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. 
  Ut wisis enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit 
  lobortis nisl ut aliquip ex ea commodo consequat.</p>
 </body>
</html>
```
### font-weight

Устанавливает насыщенность шрифта. Значение устанавливается от 100 до 900 с шагом 100. Сверхсветлое начертание, которое может отобразить браузер, имеет значение 100, а сверхжирное — 900. Нормальное начертание шрифта (которое установлено по умолчанию) эквивалентно 400, стандартный полужирный текст — значению 700.

Синтаксис
```
font-weight: bold|bolder|lighter|normal|100|200|300|400|500|600|700|800|900
```
Значения
Насыщенность шрифта задаётся с помощью ключевых слов: bold — полужирное начертание, normal — нормальное начертание. Также допустимо использовать условные единицы от 100 до 900. Значения bolder и lighter изменяют жирность относительно насыщенности родителя, соответственно, в большую и меньшую сторону.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>font-weight</title>
  <style>
   h1 {
    font-weight: normal; /* Нормальное начертание */
   } 
   .select {
    color: maroon; /* Цвет текста */
    font-weight: 600; /* Жирное начертание */
   }
  </style>
 </head>
 <body>
  <h1>Duis te feugifacilisi</h1>
  <p><span class="select">Lorem ipsum dolor sit amet</span>, 
  consectetuer adipiscing elit, sed diem nonummy nibh euismod tincidunt ut lacreet 
  dolore magna aliguam erat volutpat. Ut wisis enim ad minim veniam, quis nostrud 
  exerci tution ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo
  consequat.</p>
 </body>
</html>
```

### font-variant

Определяет, как нужно представлять строчные буквы — оставить их без модификаций или делать их все прописными уменьшенного размера. Такой способ изменения символов называется капителью.

Синтаксис
```
font-variant: normal | small-caps | inherit
```
Значения
- normal
Оставляет регистр символов исходным, заданным по умолчанию.
- small-caps
Модифицирует все строчные символы как заглавные уменьшенного размера, как показано на рис. 1.
- inherit
Наследует значение родителя

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>font-variant</title>
  <style>
   h1 {
    font-variant: small-caps; /* Устанавливаем капитель для заголовка */
   } 
  </style>
 </head>
 <body> 
  <h1>Duis te feugifacilisi</h1>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem 
  nonummy nibh euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. 
  Ut wisis enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit 
  lobortis nisl ut aliquip ex ea commodo consequat.</p>
 </body>
</html>
```

#### @font-face

Правило @font-face позволяет определить настройки шрифтов, а также загрузить специфичный шрифт на компьютер пользователя.

Синтаксис
```
@font-face { свойства шрифта }
```
Значения
Внутри конструкции @font-face может находиться набор свойств для изменения параметров шрифта (font-family, font-size, font-style и др.), а также ссылка на шрифтовой файл. Ссылка записывается в виде src: url(URI), где URI — относительный или абсолютный путь к файлу.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>@font-face</title>
  <style>
   @font-face {
    font-family: Pompadur; /* Имя шрифта */
    src: url(fonts/pompadur.ttf); /* Путь к файлу со шрифтом */
   }
   P {
    font-family: Pompadur;
   }
  </style>
 </head>
 <body>
  <p>Протяженность варьирует дорийский микрохроматический интервал, 
     но если бы песен было раз в пять меньше, было бы лучше для всех.</p>
 </body>
</html>
```

## Тег a
﻿
Тег a является одним из важных элементов HTML и предназначен для создания ссылок. В зависимости от присутствия атрибутов name или href тег a устанавливает ссылку или якорь. Якорем называется закладка внутри страницы, которую можно указать в качестве цели ссылки. При использовании ссылки, которая указывает на якорь, происходит переход к закладке внутри веб-страницы.

Для создания ссылки необходимо сообщить браузеру, что является ссылкой, а также указать адрес документа, на который следует сделать ссылку. В качестве значения атрибута href используется адрес документа (URL, Universal Resource Locator, универсальный указатель ресурсов), на который происходит переход. Адрес ссылки может быть абсолютным и относительным. Абсолютные адреса работают везде и всюду независимо от имени сайта или веб-страницы, где прописана ссылка. Относительные ссылки, как следует из их названия, построены относительно текущего документа или корня сайта.

Синтаксис
```
<a href="URL">...</a>
<a name="идентификатор">...</a>
```
Атрибуты
- accesskey
Активация ссылки с помощью комбинации клавиш.
- coords
Устанавливает координаты активной области.
- download
Предлагает скачать указанный по ссылке файл.
- href
Задает адрес документа, на который следует перейти.
- hreflang
Идентифицирует язык текста по ссылке.
- name
Устанавливает имя якоря внутри документа.
- rel
Отношения между ссылаемым и текущим документами.
- rev
Отношения между текущим и ссылаемым документами.
- shape
Задает форму активной области ссылки для изображений.
- tabindex
Определяет последовательность перехода между ссылками при нажатии на кнопку Tab.
- target
Имя окна или фрейма, куда браузер будет загружать документ.
- title
Добавляет всплывающую подсказку к тексту ссылки.
- type
Указывает MIME-тип документа, на который ведёт ссылка.

Пример
```
<!DOCTYPE HTML>
<html>
 <head>
   <meta charset="utf-8">
  <title>Тег А</title>
 </head>
 <body>
  <p><a href="images/xxx.jpg">Посмотрите на мою фотографию!</a></p>
  <p><a href="tip.html">Как сделать такое же фото?</a></p> 
</body>
</html>
```

## a:hover
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


```

Если вы разрабатываете тянущийся сайт с использованием ширин в процентах, то знаете, что эти проценты соотносятся с размерами контейнера элемента, так что если у вас есть элемент, которому вы хотите поставить ширину в 40% от его родительского элемента, ширина которого — 75%, тогда придется устанавливать ширину этого элемента в 53,33333%.

```
.inner { 
    margin: 0 auto; 
    width: 93.75%;      /* 960px / 1024px */ 
} 

aside { 
    float: left; 
    width: 31.875%; /* 306px / 960px */ 
} 

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

## float: right; 
```
section, 
footer { 
    float: right; 
    width: 65.9375%;    /* 633px / 960px */ 
} 

```

### margin

Устанавливает величину отступа от каждого края элемента. Отступом является пространство от границы текущего элемента до внутренней границы его родительского элемента.

Если у элемента нет родителя, отступом будет расстояние от края элемента до края окна браузера с учетом того, что у самого окна по умолчанию тоже установлены отступы. Чтобы от них избавиться, следует устанавливать значение margin для селектора body равное нулю.

Свойство margin позволяет задать величину отступа сразу для всех сторон элемента или определить ее только для указанных сторон.

Синтаксис
```
margin: [значение | проценты | auto] {1,4} | inherit
```
Значения
Разрешается использовать одно, два, три или четыре значения, разделяя их между собой пробелом. Эффект зависит от количества значений и приведен в табл. 1.

Зависимость от числа значений

- 1   Отступы будут установлены одновременно от каждого края элемента.
- 2   Первое значение устанавливает отступ от верхнего и нижнего края, второе — от левого и правого.
- 3   Первое значение задает отступ от верхнего края, второе — одновременно от левого и правого края, а третье — от нижнего края.
- 4   Поочередно устанавливается отступ от верхнего, правого, нижнего и левого края.
Величину отступов можно указывать в пикселах (px), процентах (%) или других допустимых для CSS единицах. Значение может быть как положительным, так и отрицательным числом.

- auto
Указывает, что размер отступов будет автоматически рассчитан браузером.
- inherit
Наследует значение родителя.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>margin</title>
  <style>
   body { 
    margin: 0; /* Убираем отступы */
   }
   .parent {
    margin: 20%; /* Отступы вокруг элемента */
    background: #fd0; /* Цвет фона */
    padding: 10px; /* Поля вокруг текста */
   } 
   .child {
    border: 3px solid #666; /* Параметры рамки */
    padding: 10px; /* Поля вокруг текста */
    margin: 10px; /* Отступы вокруг */
   }
  </style>
 </head> 
 <body> 
  <div class="parent">
   <div class="child">
    Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem nonummy nibh 
    euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. Ut wisis enim 
    ad minim veniam, quis nostrud exerci tution ullamcorper suscipit lobortis nisl 
    ut aliquip ex ea commodo consequat. 
   </div>
  </div>
 </body>
</html>
```


```
.intro { 
    margin-top: 117px; 
} 
.intro div { 
    line-height: 1.4; 
} 

article h3 { 
    font: normal 2em "Hoefler Text", "Baskerville old face", Garamond, "Times New Roman", serif; 
    text-align: center; 
    margin-bottom: 0.25em; 
} 

section h2 { 
    background: url("../images/ornament.png") no-repeat 0 50%; 
    font-size: 1.4em; 
    text-transform: lowercase; 
    text-align: center; 
    margin: 0.75em 0 1em; 
} 
```

## padding

Устанавливает значение полей вокруг содержимого элемента. Полем называется расстояние от внутреннего края рамки элемента до воображаемого прямоугольника, ограничивающего его содержимое.

Свойство padding позволяет задать величину поля сразу для всех сторон элемента или определить ее только для указанных сторон.

Синтаксис
```
padding: [значение | проценты] {1, 4} | inherit
```
Значения
Разрешается использовать одно, два, три или четыре значения, разделяя их между собой пробелом. Эффект зависит от количества значений.

Зависимость от числа значений

- 1   Поля будут установлены одновременно от каждого края элемента.
- 2   Первое значение устанавливает поля от верхнего и нижнего края, второе — от левого и правого.
- 3   Первое значение задает поле от верхнего края, второе — одновременно от левого и правого края, а третье — от нижнего края.
- 4   Поочередно устанавливается поля от верхнего, правого, нижнего и левого края.
Величину полей можно указывать в пикселах (px), процентах (%) или других допустимых для CSS единицах. Значение inherit указывает, что оно наследуется у родителя. При указании поля в процентах, значение считается от ширины родителя элемента.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>padding</title>
  <style>
   .layer {
    background: #fc3; /* Цвет фона */
    border: 2px solid black;  /* Параметры рамки */
    padding: 20px; /* Поля вокруг текста */
   }
  </style>
 </head>
 <body>
  <div class="layer">
   Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem nonummy nibh 
   euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. Ut wisis enim 
   ad minim veniam, quis nostrud exerci tution ullamcorper suscipit lobortis nisl 
   ut aliquip ex ea commodo consequat.
  </div>
 </body>
</html>
```

## text-align

Определяет горизонтальное выравнивание текста в пределах элемента.

Синтаксис
```
CSS2.1  
text-align: center | justify | left | right | inherit
CSS3    
text-align: center | justify | left | right | start | end
````
Значения
- center
Выравнивание текста по центру. Текст помещается по центру горизонтали окна браузера или контейнера, где расположен текстовый блок. Строки текста словно нанизываются на невидимую ось, которая проходит по центру веб-страницы. Подобный способ выравнивания активно используется в заголовках и различных подписях, вроде подрисуночных, он придает официальный и солидный вид оформлению текста. Во всех других случаях выравнивание по центру применяется редко по той причине, что читать большой объем такого текста неудобно.
- justify
Выравнивание по ширине, что означает одновременное выравнивание по левому и правому краю. Чтобы произвести это действие браузер в этом случае добавляет пробелы между словами.
- left
Выравнивание текста по левому краю. В этом случае строки текста выравнивается по левому краю, а правый край располагается «лесенкой». Такой способ выравнивания является наиболее популярным на сайтах, поскольку позволяет пользователю легко отыскивать взглядом новую строку и комфортно читать большой текст.
- right
Выравнивание текста по правому краю. Этот способ выравнивания выступает в роли антагониста предыдущему типу. А именно, строки текста равняются по правому краю, а левый остается «рваным». Из-за того, что левый край не выровнен, а именно с него начинается чтение новых строк, такой текст читать труднее, чем, если бы он был выровнен по левому краю. Поэтому выравнивание по правому краю применяется обычно для коротких заголовков объемом не более трех строк. Мы не рассматриваем специфичные сайты, где текст приходится читать справа налево, там возможно подобный способ выравнивания и пригодится.
- auto
Не изменяет положение элемента.
- inherit
Наследует значение родителя.
- start
Аналогично значению left, если текст идёт слева направо и right, когда текст идёт справа налево.
- end
Аналогично значению right, если текст идёт слева направо и left, когда текст идёт справа налево.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>text-align</title>
  <style>
   div {
    border: 1px solid black; /* Параметры рамки */
    padding: 5px; /* Поля вокруг текста */
    margin-bottom: 5px; /* Отступ снизу */
   }
   #left { text-align: left; }
   #right { text-align: right; }
   #center { text-align: center; }
   .content {
    width: 75%; /* Ширина слоя */
    background: #fc0; /* Цвет фона */
   }
  </style>
 </head>
 <body>
  <div id="left"><div class="content">Выравнивание по левому краю</div></div>
  <div id="center"><div class="content">Выравнивание по центру</div></div>
  <div id="right"><div class="content">Выравнивание по правому краю</div></div>
 </body>
</html>
```

### text-decoration

Добавляет оформление текста в виде его подчеркивания, перечеркивания, линии над текстом и мигания. Одновременно можно применить более одного стиля, перечисляя значения через пробел.

Синтаксис
```
text-decoration: [ blink || line-through || overline || underline ] | none | inherit
```
Значения
- blink
Устанавливает мигающий текст. Такой текст периодически, примерно раз в секунду исчезает, потом вновь появляется на прежнем месте. Это значение в настоящее время не поддерживается браузерами и осуждается в CSS3, взамен рекомендуется использовать анимацию.
- line-through
Создает перечеркнутый текст (пример).
- overline
Линия проходит над текстом (пример).
- underline
Устанавливает подчеркнутый текст (пример).
- none
Отменяет все эффекты, в том числе и подчеркивания у ссылок, которое задано по умолчанию.
- inherit
Значение наследуется у родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>text-decoration</title>
  <style>
   a { 
    text-decoration: none; /* Убираем подчеркивание у ссылок */
   }
   a:hover { 
    text-decoration: underline; /* Добавляем подчеркивание 
                                   при наведении курсора мыши на ссылку */
   }
  </style> 
 </head> 
 <body>
  <p><a href="1.html">Стратегическое нападение</a></p>
 </body>
</html>
```
### text-indent

Устанавливает величину отступа первой строки блока текста (например, для абзаца p). Воздействия на все остальные строки не оказывается. Допускается отрицательное значение для создания выступа первой строки, но следует проверить, чтобы текст не выходил за пределы окна браузера.

Синтаксис
```
text-indent: <значение> | <проценты> | inherit
```
Значения
В качестве значений принимаются любые единицы длины, принятые в CSS — например, пикселы (px), дюймы (in), пункты (pt) и др. При задании значения в процентах, отступ первой строки вычисляется в зависимости от ширины блока. Допустимо использовать отрицательные значения, но при этом в разных браузерах возможно появление ошибок.

- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>text-indent</title>
  <style>
   P { 
    text-indent: 1.5em; /* Отступ первой строки */
    text-align: justify; /* Выравнивание по ширине */
   }
  </style> 
 </head> 
 <body>
   <p>Огневое нападение бывает пяти видов: первое, когда   
   сжигают людей; второе, когда сжигают запасы; третье, 
   когда сжигают   обозы; четвертое, когда сжигают склады; 
   пятое, когда сжигают отряды.</p>
   <p>Сунь-цзы, Искусство войны. Перевод Николай Конрад.</p>
 </body>
</html>
```

### text-overflow

Определяет параметры видимости текста в блоке, если текст целиком не помещается в заданную область. Возможны два варианта: текст обрезается; текст обрезается и к концу строки добавляется многоточие. text-overflow работает в том случае, если для блока значение свойства overflow установлено как auto, scroll или hidden.

Синтаксис
```
text-overflow: clip | ellipsis
```
Значения
- clip
Текст обрезается по размеру области.
- ellipsis
Текст обрезается и к концу строки добавляется многоточие.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>text-overflow</title>
  <style>
   p.clip {
    white-space: nowrap; /* Запрещаем перенос строк */
    overflow: hidden; /* Обрезаем все, что не помещается в область */
    background: #fc0; /* Цвет фона */
    padding: 5px; /* Поля вокруг текста */
    text-overflow: ellipsis; /* Добавляем многоточие */
   }
  </style>
 </head>
 <body>
  <p class="clip">Магнитное поле ничтожно гасит большой круг небесной сферы, 
  в таком случае эксцентриситеты и наклоны орбит возрастают.</p>
 </body>
</html>
```
### text-transform
Управляет преобразованием текста элемента в заглавные или прописные символы. Когда значение отлично от none, регистр исходного текста будет изменен.

Синтаксис
```
text-transform: capitalize | lowercase | uppercase | none | inherit
```
Значения
- capitalize
Первый символ каждого слова в предложении будет заглавным. Остальные символы свой вид не меняют.
- lowercase
Все символы текста становятся строчными (нижний регистр).
- uppercase
Все символы текста становятся прописными (верхний регистр).
- none
Не меняет регистр символов.
- inherit
Наследует значение родителя.
Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>text-transform</title>
  <style>
   h1 { 
    text-transform: uppercase; /* Заглавные буквы */
   }
   p { 
    text-transform: capitalize; /* Каждое слово начинается с заглавной буквы */
   }
  </style>
 </head>
 <body> 
  <h1>Lorem ipsum dolor sit amet</h1>
  <p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diem 
  nonummy nibh euismod tincidunt ut lacreet dolore magna aliguam erat volutpat. 
  Ut wisis enim ad minim veniam, quis nostrud exerci tution ullamcorper suscipit 
  lobortis nisl ut aliquip ex ea commodo consequat.</p> 
 </body>
</html>
```
### text-shadow

Добавляет тень к тексту, а также устанавливает её параметры: цвет тени, смещение относительно надписи и радиус размытия. Свойство text-shadow может работать совместно с псевдоэлементами :first-letter и :first-line.

Синтаксис
```
text-shadow: none | тень [,тень]*
где тень:
<сдвиг по x> <сдвиг по y> <радиус размытия> <цвет>
```
Значения

- none
Отменяет добавление тени.
- цвет
Цвет тени в любом доступном CSS формате. По умолчанию цвет тени совпадает с цветом текста. Необязательный параметр.
- сдвиг по x
Смещение тени по горизонтали относительно текста. Положительное значение этого параметра задает сдвиг тени вправо, отрицательное — влево. Обязательный параметр.
- сдвиг по y
Смещение тени по вертикали относительно текста. Также допустимо использовать отрицательное значение, которое поднимает тень выше текста. Обязательный параметр.
- радиус
Задает радиус размытия тени. Чем больше это значение, тем сильнее тень сглаживается, становится шире и светлее. Если этот параметр не задан, по умолчанию устанавливается равным 0. Учтите, что алгоритм сглаживания в браузерах обычно разный, поэтому вид тени может несколько различаться в зависимости от заданных параметров сглаживания.
Допускается указывать несколько параметров тени, разделяя их между собой запятой. В CSS3 учитывается следующий порядок: первая тень в списке размещается на самом верху, последняя в списке — в самом низу. В CSS2 порядок наоборот: первая тень размещается в самом низу, а последняя на самом верху.

Пример
```
<!DOCTYPE html>
<html>
 <head>
  <meta charset="utf-8">
  <title>text-shadow</title>
  <style>
   .shadowtext {
    text-shadow: 1px 1px 2px black, 0 0 1em red; /* Параметры тени */
    color: white; /* Белый цвет текста */
    font-size: 2em; /* Размер надписи */
   }
  </style>
 </head>
 <body>
  <p class="shadowtext">В чащах юга жил бы цитрус? Да, но фальшивый экземпляр!</p> 
 </body>
</html>
```

### exersise
Создать страницу index.html, с фоном bg.png, сбросив предварительно все свойства тегов.
Страница должна быть разделена на 2 части 
- слева 30 процентов
- справа 70 процентов

В правой части разместить текстовый блок, выделив его заголовок.
Ниже разместить блоки с изображениями, по 3 в строке
Подписать каждое изображение текстовым блоком
Все свойства элементов поместить в файл main.css

```
images/
    bg.png
    logo.png
    rag.png
    ...
css/
    reset.css
    main.css
index.html
```