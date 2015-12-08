# 11-css-danco
unit 11
=======

Объединение идентификаторов CSS
-------------------------------
Первый вид комбинации называется контекстный селектор. Он учитывает взаимоотношение элементов Html кода по принципу «Предок — Потомок»: 
Идентификаторы, также как и классы можно объединять с другими селекторами. Общий синтаксис такой:
селектор#идентификатор { свойство1: значение; ... свойствоN: значение}
```
<!DOCTYPE HTML>
<html>
 <head>
  <meta charset=utf-8>
  <title>Идентификаторы</title>
  <style type="text/css">
   p {
    color: red; /* Красный цвет текста */
    font-style: italic; /* Курсивное начертание текста */
   }
   P#block { 
    color: green; /* Зеленый цвет текста */
    border: 1px solid #666; /* Параметры рамки */
    background: #eee; /* Цвет фона */
    padding: 6px; /* Поля вокруг текста */
    position: absolute; /* Абсолютное позиционирование */
    left: 160px; /* Положение от левого края */
    top: 130px; /* Положение от верхнего края */
    width: 220px; /* Ширина блока */
   }
  </style> </head>  <body>
   <p>Просто текст красного цвета</p> 
   <p id="block"> Этот текстовый блок серого цвета задан с помощью абсолютного позиционирования. Для задания стилей 
к этому блоку было использовано объединение идентификатора под именем <b>block</b> и тега<b>p</b></p>
 </body> </html>
```
Отдельные селекторы в комбинации записываются через пробел, а читать ее нужно справа налево. Т.о. правила CSS будут применяться только к последнему этой комбинации (самому правому), а все, что стоит перед ним, лишь позволяет задать более точное применение (прицеливание) для наших правил (акцентировать). В первом примере говорится, что все элементы B (выделение жирным), у которых в предках есть элементы Div, будут окрашены в зеленый цвет. 
```
Div b {color:green;}
```
Такие комбинации работают в любых браузерах. 

Комбинаторы и псевдо классы.
----------------------------
Комбинаторы, как и следует из названия, предназначены для объединения различных селекторов.
Существует четыре типа комбинаторов для указания отношений между элементами.
- Комбинатор потомков E F (1) — соответствует элементу F, который является потомком элемента E. 
```
ul li {background: red;}
```

- Комбинатор прямых потомков E > F

соответствует элементу F, который является прямым потомком элемента E.
Следующим типом комбинаций будет дочерний селектор, который строится на принципах взаимоотношений элементов кода по типу «Родитель — Ребенок»: 
Записываются они с разделяющим знаком больше (>):Данная запись будет трактоваться браузером так: для абзацев (Html тег P), «родителем» (ближайшим предком) которых является контейнер Div, будет использоваться выделение красным цветом. 
Дочерние селекторы не работают в браузере Ie 6. 
```
dl>dt {background: red;}
```

- Комбинатор смежных родственников E + F — соответствует элементу F, которому непосредственно предшествует элемент E. Только первый элемент F сразу после элемента E будет выбран.
Последняя комбинация называется соседние селекторы и отвечает принципам отношений между элементами Html кода по типу «Сестры — Братья». В качестве разделителя у них может использоваться либо «+», либо «~»: Данная запись означает, что содержимое элемента I будет окрашено в красный цвет только тогда, если его ближайшим соседом слева является элемент B. Например, данное условие будет соблюдено в этом примере: 
```

<h1>Заголовок</h1>

<p>Параграф 1</p>

<p>Параграф 2</p>

<p>Параграф 3</p>
CSS:

h1+p {font-size: 1.5em;}
```
Только параграф 1 получит увеличенный размер шрифта, так как он является смежным с элементомh1.

- Общий комбинатор  родственников E ~ F — соответствует элементу F, которому предшествует элемент E. В отличие от предыдущего комбинатора, здесь выбираются все соседи, а не только непосредственные. Если записать соседний селектор в Css коде в таком виде: h1 ~ p {color:red} То это будет означать, что все параграфы (P), у которых выше по коду расположен соседний элемент H1 (заголовок), будут окрашены в красный цвет. Имеются в виду именно соседние элементы (отношения вида «Сестры — Братья»).
Комбинации соседних селекторов в браузере Ie 6 не поддерживаются. В Ie 6 поддерживается только первый вид комбинации, а в Ie 7 и выше поддерживаются все остальные. В остальных браузерах никаких проблем возникать не должно. 
```
<h1>Заголовок</h1> 
<p>Параграф 1</p> 
<p>Параграф 2</p> 
<p>Параграф 3</p> 
CSS

h1~p {font-size: 1.5em;}
```
Все три параграфа будут иметь увеличенный размер шрифта, так как всем им предшествует элементh1.

Можно использовать любой селектор в любой части комбинатора. Все приведенные селекторы являются правильными.
```
dl a[title] {   background: green; }
<dl> 
    <dt>Term списка 1 
        <dd><a href='#' title='Пункт списка 1.1'>Пункт списка 1.1</a></dd> 
        <dd>Пункт списка 1.2</dd> 
    </dt> 
    <dt>Term списка 2 
        <dd>Пункт списка 2.1</dd> 
        <dd>Пункт списка 2.2</dd> 
    </dt> 
</dl>

h2.myclass {    color:blue; } 
h2.myclass~p { color:red; } 
h2.myclass~p[class='green'] {   color:green; } 
<h2 class='myclass'>MyClass</h2> 
<p>Color Red</p> 
<p class='green'>Color Green</p> 

h2.myclass {    color:blue; } 
h2.myclass+p[class='green'] {   color:green; } 
<h2 class='myclass'>MyClass</h2> 
<p class='green'>Color Green</p> 
<p>Color Red</p> 

dl#first a[rel='external'] {    background: aqua; } 
<dl id='first'> 
    <dt>Term списка 1 
        <dd><a href='#'rel="external">Пункт списка 1.1</a></dd> 
        <dd>Пункт списка 1.2</dd> 
    </dt> 
    <dt>Term списка 2 
        <dd>Пункт списка 2.1</dd> 
        <dd>Пункт списка 2.2</dd> 
    </dt> 
</dl>
```
Как и для чего группируют селекторы в CSS коде 
-----------------------------------------------
Селекторы в Css можно группировать. Например, если у каких-то из них используется одно или несколько одинаковых правил, то их можно объединить в группу для уменьшения объема Css кода. Обратите внимание, что при группировке селекторы пишутся через запятую. Если одинаковых правил будет больше, то и экономия кода будет более ощутимой. А те правила, которые были уникальными, нужно по-прежнему записывать индивидуально. 

Приоритеты Css свойств (с important и без него) 
-----------------------------------------------
Более высокий приоритет имеют свойства, которые назначит пользователь в настройках своего браузера. Эти стили будут применены к любым документам, которые он просматривает в этом обозревателе. Правда не у всех браузеров есть такая возможность, но по крайней мер, в Ie и Опере она имеется. Т.е. при желании пользователь в качестве источника стилевой разметки сможет подключить свой собственный файл CSS. Например, в Ie для этого нужно выбрать из верхнего правого меню «Сервис» — «Свойства обозревателя», а затем на первой вкладке «Общие» щелкнуть по нижней кнопке «Оформление». В открывшемся окне вам нужно поставить галочку в поле «Оформлять, используя пользовательский стиль», и с помощью кнопки «Обзор» найти на своем компьютере нужный вам файл стилевой разметки CSS: Т.е. у пользователя есть возможность заставить любой открываемый в браузере сайт выглядеть в соответствии с его требованиями, описанными в файле CSS. Это называется «пользовательские стили» и они имеют приоритет выше, чем стили, которые определены в спецификации по умолчанию. 
Но еще больший приоритет будут иметь так называемые авторские стили. 
Под авторскими стилями имеются в виду свойства, которые подключаются к Html документу любым из трех основных способов (тег или атрибут Style в Css, а также внешний файл с таблицами стилей). Т.е., если я (разработчик сайта) захотел использовать в оформлении какого-либо элемента Html кода стили отличные от дефолтных, то пользователь своим собственным файлом Css перебить мое оформление не сможет. Пользователь будет вынужден смириться? Нет. Есть у него возможность повысить приоритет своих свойств CSS с помощью добавления Important в конце каждого из них. Пишется это слово через пробельный символ и перед ним ставится восклицательный знак: 
```
p {color:red !important;} 
```
Если у пользователя в его собственном файле стилей, который он подключил к браузеру, будет прописано это же свойство с Important, то все абзацы он будет видеть в красном цвете. Но ведь и автор (разработчик) сайта мог использовать Important для этого свойства. Кто же тогда победит и чей приоритет окажется выше? 
Решили, что пользовательские стили с Important будут иметь по-любому более высокий приоритет, чем авторские стили, что с Important, что без него. 

Приоритет будет убывать сверху вниз: 
------------------------------------

- Пользовательские с Important 
- Авторские с Important 
- Авторские 
- Пользовательские 
- Стили, принятые для Html элементов в спецификации по умолчанию (когда ни автор, ни пользователь ничего другого не задали) 
Т.е. без Important авторские стили важнее, а с них уже пользовательские стили самые важные и приоритетные. 
Как повышают приоритеты Css свойств в авторских стилях 
--------------------------------------------------------
Приоритет авторских свойств тоже должен подчиняться определенным правилам, которые позволяли бы разрулить ситуации, когда для одного и того же элемента было бы прописано несколько взаимоисключающих правил. 
Допустим, что у нас имеется фрагмент кода со следующими Html элементами (параграф внутри контейнера Div): 
```
<div id="in" class="box"> 
     <p id="out" class="sbox">Содержимое контейнера </p> 
</div> 
```
Давайте сначала пропишем такие свойства: 
```
p {color:red} 
.sbox {background:#f0f0f0} 
```
В результате будет применено и первое из них к параграфу (ибо он образован тегом P), и свойство, задающее серый фон для элемента с классом «sbox», который опять же имеется у этого параграфа: 
А теперь давайте добавим ко второму селектору (класса) еще одно свойство, которое будет конфликтовать с первой строчкой (в них обоих задается цвет для текста через color, но значения при этом используются разные): 
```
p {color:red} 
.sbox {background:#f0f0f0;color:blue} 
```
В результате цвет текста параграфа станет синим вместо красного. 
Потому что именно таким способом разрешается конфликт, когда один и тот же элемент Html кода получает сразу несколько одинаковых правил, но с разными значениями и из разных мест Css кода. Для того, чтобы определить, приоритет какого правила выше, нужно считать его селекторы. 
Кроме этого сами селекторы имеют градацию по приоритетам. Самый высокий приоритет у ID. В этом примере цвет текста будет синим именно потому, что приоритет Id (#out) будет выше, чем у селектора тега (p): 
```
p {color:red} 
#out {color:blue} 
```
В следующем примере опять проиграет тег (p) и цвет текста абзаца будет синим, ибо тягается он с селектором более высокого приоритета (класса): 
```
p {color:red} 
.sbox {color:blue} 
```
Ну, и самым низким приоритетом (не считая универсальный *, обладающего нижайшим весом и не вносящего никаких изменений в подобные бодания) обладают селекторы тегов и псевдоэлементов. 
Нужно считать количество селекторов одного и того же уровня приоритета, и чем их будет больше, тем приоритетнее будет данное свойство. Например: 
```
div p {color:red} 
p {color:blue} 
```
Т.е. сначала считаются Id. Если победитель не выявлен, то считаются классы, псевдоклассы и атрибуты. Ну, а если и там ничего не решилось или таких не было найдено, то считаются селекторы тегов и псевдоэлементов. 
Но вполне возможна ситуация, когда победитель не выявится и селекторы конкурирующих классов окажутся равного приоритета в сумме. Например, для нашего многострадального параграфа заключенного в контейнер Div: 
```
<div id="in" class="box"> 
     <p id="out" class="sbox">Содержимое контейнера </p> 
</div> 
```
Вполне можно будет написать такой кусок Css кода: 
```
div.box #out{color:red} 
#in p.sbox{color:blue} 
```
Обе комбинации описывают именно наш параграф. Первую следует, как и водится, читать справа налево: применить данные свойства (color:red) для элемента с Id #out, который стоит где-то внутри (иметь его среди «предков») контейнера Div с классом .box (div.box). Полностью подходит к нашему абзацу. 
Вторая комбинация: применить данные свойства (color:blue) для элемента параграфа с классом sbox (p.sbox), который стоит внутри любого элемента с Id #in. Опять же, она полностью описывает именно наш параграф. 

С ID в обоих комбинациях встречаются по одному разу, тоже самое можно сказать и о классах. Остается только посчитать селекторы тегов, но их тоже в обоих комбинациях используется одинаковое число раз (один). 
Получились равные приоритеты у одного и того же свойства, имеющего разные значения (цвет текста красный, либо синий). Как же браузер будет решать эту дилемму? 
Тут будет действовать правило — кто последний, тот и прав. Поэтому в моем примере цвет текста параграфа будет синим, ибо это свойство (color:blue) расположено ниже в коде. Если эти правила поменять местами: 
```
#in p.sbox{color:blue} 
div.box #out{color:red} 
```
То в результате цвет текста параграфа изменится на красный. Что и требовалось доказать. Можно дописать, например, к любой комбинации еще один селектор тега и мы перевесим чашу весов в его пользу, даже если она и не стоит ниже в коде: 
```
body #in p.sbox{color:blue} 
div.box #out{color:red} 
```
В этом случае цвет параграфа измениться на синий. Универсальный селектор «*» вообще никакого влияния на подсчет приоритетов не оказывает. Кстати, чуть выше мы рассмотрели способ повышения приоритета Css правил с помощью добавления Important. В нашем примере это может выглядеть так: 
```
p {color:green !important} 
#in p.sbox{color:blue} 
div.box #out{color:red} 
```
Второй способ повышения может заключаться в использовании стилевых свойств в атрибуте Style нужного вам Html элемента. 
Т.е. прописываете внутри того же многострадального тега P атрибут Style с заданием любого цвета: 
```
<div id="in" class="box"> 
     <p id="out" class="sbox" style="color:yellow">Содержимое контейнера </p> 
</div> 
```
список факторов, влияющих на приоритет свойства в авторских стилях по мере их убывания: 
-----------------------------------------------------------------------------------------
- Прописывание свойства в атрибуте style нужного тега вместе с Important 
- Добавление Important к свойству во внешнем файле таблиц стилей или же в теге style прямо в Html коде 
- Простое прописывание этого свойства в атрибуте style нужно элемента 
- Использование бОльшего числа Id для данного свойства 
- Использование большего числа селекторов классов, псевдоклассов или атрибутов 
- Использование большего числа селекторов тегов и псевдоэлементов 
- Более низкое расположение свойства в Css коде, при прочих равных условиях 

Псевдо-классы
-------------
Существует достаточно большой выбор псевдо-классов. Некоторые из них вы используете часто, а некоторые могут оказаться новыми для вас. W3C разделяет псевдо-классы на следующие группы:
- динамические псевдо-классы
- псевдо-класс цели
- псевдо-класс языка
- псевдо-классы состояния элементов интерфейса
- псевдо-класс отрицания
- структурные псевдо-классы
Динамические псевдо-классы
---------------------------
В нее входят псевдо-классы ссылок и действий пользователя.
Псевдо-классы ссылок
---------------------
- E:link — соответствует элементу E, который является еще не посещенной ссылкой.
- E:visited — соответствует элементу E, который является уже посещенной ссылкой.
Псевдо-классы действий пользователя 
------------------------------------
Соответствуют элементу E при определенных действиях пользователя.
- E:active — в процессе нажатия на ссылку.
- E:hover — при наведении курсора мыши на ссылку.
- E:focus — при получении ссылкой фокуса ввода.
Псевдо-класс цели
-----------------
Если вы когда-нибудь создавали ссылку с использованием символа # в адресе URL, то тем самым, создавали целевой псевдо-класс.
E:target — соответствует элементу E, который  является целью в адресе URL ссылки.
```

<a href="domain.com/this-page.html#a-specific-page-location"></a>

<span id="a-specific-page-location"></span>
CSS:

span:target {background: yellow;}
```
Желтый фон будет использован для элемента span.
Псевдо-класс языка
------------------
E:lang(fr) — соответствует элементу E с указанным языком (в примере используется “fr” - французский).
Скорее всего, вы будете очень редко использовать данный псевдо-класс. Но это отличный способ выделить текст на другом языке.
```
<body lang=fr> 
<p>Je suis français.</p> 
</body> 
CSS: 
p:lang(fr) {color: red;} 
```
Псевдо-классы состояния элементов интерфейса 
--------------------------------------------
Одним из способов воздействия на удобство интерфейса является разрешение/запрещение ввода информации в разные части формы при ее заполнении в зависимости от того, что уже заполнено.
Обратите внимание, что элементы HTML не разрешаются/запрещаются. Для этого используется JavaScript. Но можно установить атрибуты для элементов ввода.

- E:enabled — соответствует элементу интерфейса  E,  который является доступным для ввода.
- E:disabled — соответствует элементу интерфейса E, который не доступен для ввода.
- E:checked — соответствует элементу интерфейса E, который отмечен (для радиокнопок или чекбоксов).
Зеленый и красный цвета используются для информирования пользователя о доступных для ввода элементах формы. Отмеченный пункт получит желтый фон для визуального выделения.
```
<form> 
Предпочтительный способ связи: 
<input type="radio" id="prefer" value="email" checked="checked" /> Email 
<input type="radio" id="prefer" value="phone" /> Телефон 
Email: <input type="text" id="email" enabled="enabled" /> 
Телефон: <input type="text" id="phone" disabled="disabled" /> 
</form> 
CSS: 
:enabled {color: green;} 
:disabled {color: red;} 
:checked {background: yellow;} 
```
Псевдо-класс отрицания
----------------------
Псевдо-класс отрицания используется для выбора всего, что ему не соответствует.
- E:not(S) — соответствует элементу E, который не соответствует селектору  S.
Первый и третий элементы div станут оранжевыми, так как у них нет класса two.

```
<div class="one"></div> 
<div class="two"></div> 
<div class="three"></div> 
CSS: 
div:not(.two) {color: orange;}
```
 
Фильтры; 
========
Устанавливает фильтр (визуальный эффект) или их сочетание для элемента. К фильтрам относится изменение прозрачности, добавление тени, трансформация и др.
```
filter: progid:DXImageTransform.Microsoft.Фильтр(свойства)
```

Alpha
--------
Настраивает прозрачность объекта.
BasicImage
----------
Устанавливает параметры цвета, поворота изображения или прозрачности.
Blur
-------
Размывает содержимое.
Chroma
------
Показывает определенные цвета прозрачными.
DropShadow
-----------
Отображает тень.
Emboss
-------
Показывает содержимое объекта в виде барельефа.
Engrave
--------
Показывает содержимое объекта в виде черно-белой гравюры.
Glow
----
Добавляет свечение вокруг краев.
Gradient
---------
Создаёт линейный градиент.
ICMFilter
----------
Преобразует цвета содержимого на основе профиля системы управления цветом (Image Color Management, ICM).
Light
------
Создает эффект лучей света.
MaskFilter
----------
Показывает прозрачные пикселы как цветную маску, а непрозрачные пикселы наоборот, прозрачными.
Matrix
--------
Изменяет размер, поворачивает или отражает объект на основе матричных преобразований.
MotionBlur
----------
Размывает объект так, словно он быстро движется.
Shadow
-------
Добавляет тень.
Wave
------
Вносит волнообразные искажения.

Фильтры можно применять к любому видимому элементу на странице.
grayscale()
-----------
```
<img src="redwood-ukulele-top.jpg" alt="ukulele">
img { display: block; width: 90%; }
img {
  -webkit-filter: grayscale(1);
  filter: grayscale(1);
}
```
Данный пример изменит цвет контента находящегося внутри тега на ч/б.


Slider slider1.html:
------------------
```
  <!--///////////////////////////////////////////////////////
       //  Slider section 
 //////////////////////////////////////////////////////////-->


  <div class="slidersection">
    <div class="sp-slideshow">
      
        <div class="sp-content">
          <div class="sp-parallax-bg"></div>
          <ul class="sp-slider clearfix">
            <li><img src="images/slider/slider1.png" alt="image01" /></li>
            <li><img src="images/slider/slider2.png" alt="image02" /></li>
            <li><img src="images/slider/slider3.png" alt="image03" /></li>
            <li><img src="images/slider/slider4.png" alt="image04" /></li>
            <li><img src="images/slider/slider5.png" alt="image05" /></li>
          </ul>
        </div><!-- sp-content -->
        
      </div><!-- sp-slideshow -->
  </div>


<!--///////////////////////////////////////////////////////
       // End slider section 
//////////////////////////////////////////////////////////-->
/* slider */

.sp-slideshow {
    position: relative;
    
    margin: 0px auto;
    
    width: 100%;
    max-width: 1000px;
    
    min-width: 100%;
    
    height: 590px;
    
    
}
```

Slider slider2.html:
------------------
```
  
/* slider */

.sp-content {
    background: url(../images/slider/back.png) no-repeat scroll 0 0;
    
    position: relative;
    width: 100%;
    
    /* background-size: cover; */
    height: 100%;
    overflow: hidden;
    background-position: center left;
}

.sp-parallax-bg {
    background: url(../images/slider/cloud.png) repeat-x scroll 0 0;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    background-size: cover;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    
    background-color: rgba(12, 19, 29, 0.94);
    overflow: hidden;
}
```

Slider slider3.html:
------------------
```
  
/* slider */

.sp-slider {
    position: relative;
    left: 0;
    width: 500%;
    height: 100%;
    list-style: none;
    margin: 0;
    padding: 0;
    -webkit-transition: left ease-in 0.8s;
    -moz-transition: left ease-in 0.8s;
    -o-transition: left ease-in 0.8s;
    -ms-transition: left ease-in 0.8s;
    transition: left ease-in 0.8s; 
}

.sp-slider > li {
    color: #fff;
    width: 20%;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    -o-box-sizing: border-box;
    -ms-box-sizing: border-box;
    box-sizing: border-box;
    height: 100%;
    padding: 0 60px;
    float: left;
    text-align: center;
    opacity: 0.4;
    -webkit-transition: opacity ease-in 0.4s 0.8s;
    -moz-transition: opacity ease-in 0.4s 0.8s;
    -o-transition: opacity ease-in 0.4s 0.8s;
    -ms-transition: opacity ease-in 0.4s 0.8s;
    transition: opacity ease-in 0.4s 0.8s; 
}
.sp-slider > li img{
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    -o-box-sizing: border-box;
    -ms-box-sizing: border-box;
    box-sizing: border-box;
    display: block;
    margin: 0 auto;
    padding: 40px 0 50px 0;
    max-height: 100%;
    max-width: 100%;
}
```

Slider slider4.html:
------------------
```
<!--///////////////////////////////////////////////////////
       //  Slider section 
 //////////////////////////////////////////////////////////-->


  <div class="slidersection">
    <div class="sp-slideshow">
       <input id="button-1" type="radio" name="radio-set" class="sp-selector-1" checked="checked" />
        <label for="button-1" class="button-label-1"></label>
        
        <input id="button-2" type="radio" name="radio-set" class="sp-selector-2" />
        <label for="button-2" class="button-label-2"></label>
        
        <input id="button-3" type="radio" name="radio-set" class="sp-selector-3" />
        <label for="button-3" class="button-label-3"></label>
        
        <input id="button-4" type="radio" name="radio-set" class="sp-selector-4" />
        <label for="button-4" class="button-label-4"></label>
        
        <input id="button-5" type="radio" name="radio-set" class="sp-selector-5" />
        <label for="button-5" class="button-label-5"></label>
        
        <label for="button-1" class="sp-arrow sp-a1"></label>
        <label for="button-2" class="sp-arrow sp-a2"></label>
        <label for="button-3" class="sp-arrow sp-a3"></label>
        <label for="button-4" class="sp-arrow sp-a4"></label>
        <label for="button-5" class="sp-arrow sp-a5"></label>
        <div class="sp-content">
          <div class="sp-parallax-bg"></div>
          <ul class="sp-slider clearfix">
            <li><img src="images/slider/slider1.png" alt="image01" /></li>
            <li><img src="images/slider/slider2.png" alt="image02" /></li>
            <li><img src="images/slider/slider3.png" alt="image03" /></li>
            <li><img src="images/slider/slider4.png" alt="image04" /></li>
            <li><img src="images/slider/slider5.png" alt="image05" /></li>
          </ul>
        </div><!-- sp-content -->
        
      </div><!-- sp-slideshow -->
  </div>


  
/* slider */
.sp-slideshow input {
    position: absolute;
    bottom: 15px;
    left: 50%;
    width: 9px;
    height: 9px;
    z-index: 1001;
    cursor: pointer;
    -ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";
    filter: alpha(opacity=0);
    opacity: 0;
}

.sp-slideshow input + label {
    position: absolute;
    bottom: 15px;
    left: 50%;
    width: 6px;
    height: 6px;
    display: block;
    z-index: 1000;
    border: 3px solid #fff;
    border: 3px solid rgba(255,255,255,0.9);
    -webkit-border-radius: 50%;
    -moz-border-radius: 50%;
    border-radius: 50%;
    -webkit-transition: background-color linear 0.1s;
    -moz-transition: background-color linear 0.1s;
    -o-transition: background-color linear 0.1s;
    -ms-transition: background-color linear 0.1s;
    transition: background-color linear 0.1s;
}

```

Slider slider5.html:
------------------
```
/* slider */
.sp-slideshow input:checked + label {
    background-color: #fff;
    background-color: rgba(255,255,255,0.9);
}

.sp-selector-1, .button-label-1 {
    margin-left: -36px;
}

.sp-selector-2, .button-label-2 {
    margin-left: -18px;
}

.sp-selector-4, .button-label-4 {
    margin-left: 18px;
}

.sp-selector-5, .button-label-5 {
    margin-left: 36px;
}


```
Slider slider6.html:
------------------
```
/* slider */


.sp-slideshow input:checked + label {
    background-color: #fff;
    background-color: rgba(255,255,255,0.9);
}

.sp-selector-1, .button-label-1 {
    margin-left: -36px;
}

.sp-selector-2, .button-label-2 {
    margin-left: -18px;
}

.sp-selector-4, .button-label-4 {
    margin-left: 18px;
}

.sp-selector-5, .button-label-5 {
    margin-left: 36px;
}

.sp-arrow {
    position: absolute;
    top: 50%;
    width: 28px;
    height: 38px;
    margin-top: -19px;
    display: none;

    opacity: 0.8;
    cursor: pointer;
    z-index: 1000;
    background: transparent url(images/slider/arrows.png) no-repeat;
    -webkit-transition: opacity linear 0.3s;
    -moz-transition: opacity linear 0.3s;
    -o-transition: opacity linear 0.3s;
    -ms-transition: opacity linear 0.3s;
    transition: opacity linear 0.3s;
}

.sp-arrow:hover{
    opacity: 1;
}
.sp-arrow:active{
    margin-top: -18px;
}

.sp-selector-1:checked ~ .sp-arrow.sp-a2,
.sp-selector-2:checked ~ .sp-arrow.sp-a3,
.sp-selector-3:checked ~ .sp-arrow.sp-a4,
.sp-selector-4:checked ~ .sp-arrow.sp-a5 {
    right: 15px;
    display: block;
    background-position: top right;
}
.sp-selector-2:checked ~ .sp-arrow.sp-a1,
.sp-selector-3:checked ~ .sp-arrow.sp-a2,
.sp-selector-4:checked ~ .sp-arrow.sp-a3,
.sp-selector-5:checked ~ .sp-arrow.sp-a4 {
    left: 15px;
    display: block;
    background-position: top left;
}
.sp-slideshow input:checked ~ .sp-content {
    -webkit-transition: background-position linear 0.6s, background-color linear 0.8s;
    -moz-transition: background-position linear 0.6s, background-color linear 0.8s;
    -o-transition: background-position linear 0.6s, background-color linear 0.8s;
    -ms-transition: background-position linear 0.6s, background-color linear 0.8s;
    transition: background-position linear 0.6s, background-color linear 0.8s;
}

.sp-slideshow input:checked ~ .sp-content .sp-parallax-bg {
    -webkit-transition: background-position linear 0.7s;
    -moz-transition: background-position linear 0.7s;
    -o-transition: background-position linear 0.7s;
    -ms-transition: background-position linear 0.7s;
    transition: background-position linear 0.7s;
}

input.sp-selector-1:checked ~ .sp-content {
    background-position: 0 0;
    background-color: #727b7f;
}

input.sp-selector-2:checked ~ .sp-content {
    background-position: -100px 0;
    background-color: #7f7276;
}

input.sp-selector-3:checked ~ .sp-content {
    background-position: -200px 0;
    background-color: #737f72;
}

input.sp-selector-4:checked ~ .sp-content {
    background-position: -300px 0;
    background-color: #79727f;
}

input.sp-selector-5:checked ~ .sp-content {
    background-position: -400px 0;
    background-color: #7d7f72;
}
```

Slider slider7.html:
------------------
```
input.sp-selector-1:checked ~ .sp-content .sp-parallax-bg {
    background-position: 0 0;
}

input.sp-selector-2:checked ~ .sp-content .sp-parallax-bg {
    background-position: -200px 0;
}

input.sp-selector-3:checked ~ .sp-content .sp-parallax-bg {
    background-position: -400px 0;
}

input.sp-selector-4:checked ~ .sp-content .sp-parallax-bg {
    background-position: -600px 0;
}

input.sp-selector-5:checked ~ .sp-content .sp-parallax-bg {
    background-position: -800px 0;
}

input.sp-selector-1:checked ~ .sp-content .sp-slider {
    left: 0;
}

input.sp-selector-2:checked ~ .sp-content .sp-slider {
    left: -100%;
}

input.sp-selector-3:checked ~ .sp-content .sp-slider {
    left: -200%;
}

input.sp-selector-4:checked ~ .sp-content .sp-slider {
    left: -300%;
}

input.sp-selector-5:checked ~ .sp-content .sp-slider {
    left: -400%;
}

input.sp-selector-1:checked ~ .sp-content .sp-slider > li:first-child,
input.sp-selector-2:checked ~ .sp-content .sp-slider > li:nth-child(2),
input.sp-selector-3:checked ~ .sp-content .sp-slider > li:nth-child(3),
input.sp-selector-4:checked ~ .sp-content .sp-slider > li:nth-child(4),
input.sp-selector-5:checked ~ .sp-content .sp-slider > li:nth-child(5){
    opacity: 1;
}
.slidersection {
  display: block;
  padding-top: 80px;
  background: rgba(255, 255, 255, 0);
}

@media screen and (max-width: 840px){
    .sp-slideshow { height: 345px; }
}
@media screen and (max-width: 680px){
    .sp-slideshow { height: 285px; }
}
@media screen and (max-width: 560px){
    .sp-slideshow { height: 235px; }
}
@media screen and (max-width: 320px){
    .sp-slideshow { height: 158px; }
}
```

