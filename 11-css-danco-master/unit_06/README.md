# 11-css-danco

Общий синтаксис написания идентификатора: 
```
#имя идентификатора { свойство1: значение; свойство2: значение; ...  свойствоN: значение;}
```
Для обращения к идентификатору: Тег id="имя идентификатора"
###  Объединение идентификаторов CSS
Первый вид комбинации называется контекстный селектор. Он учитывает взаимоотношение элементов Html кода по принципу «Предок — Потомок»: 
```
селектор#идентификатор { свойство1: значение; ... свойствоN: значение}
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
   <p>Просто текст красного цвета</p> 
   <p id="block"> Этот текстовый блок серого цвета задан с помощью абсолютного позиционирования. Для задания стилей к этому блоку было использовано объединение идентификатора под именем <b>block</b> и тега<b>p</b></p>
```

### Отдельные селекторы.  
Div b {color:green;} Такие комбинации работают в любых браузерах. 

## Комбинаторы и псевдо классы.
### Комбинаторы
Существует четыре типа комбинаторов для указания отношений между элементами.
### Комбинатор потомков E F — соответствует элементу F, который является потомком элемента E. Обратите внимание, что комбинатор потомков выбирает всех потомков, а не только прямых.
```
ul li {background: red;}
```
Все 5 элементов получат красный цвт, так как все они являются потомками неупорядоченного списка.
### Комбинатор прямых потомков E > F
 — соответствует элементу F, который является прямым потомком элемента E.
Следующим типом комбинаций будет дочерний селектор, который строится на принципах взаимоотношений элементов кода по типу «Родитель — Ребенок»: Записываются они с разделяющим знаком больше: Данная запись будет трактоваться браузером так: для абзацев (Html тег P), «родителем» (ближайшим предком) которых является контейнер Div, будет использоваться выделение красным цветом. 
Дочерние селекторы не работают в браузере Ie 6. 
```

dl>dt {background: red;}
```
Только пункты 1, 2 и 3 получат красный цвет, так как являются прямыми потомками неупорядоченного списка. Пункты 2-1 и 2-2 являются "внуками".

### Комбинатор смежных родственников E + F(2) — соответствует элементу F, которому непосредственно предшествует элемент E. Только первый элемент F сразу после элемента E будет выбран.
Последняя комбинация называется соседние селекторы и отвечает принципам отношений между элементами Html кода по типу «Сестры — Братья». В качестве разделителя у них может использоваться либо «+», либо «~»: Данная запись означает, что содержимое элемента I (выделение курсивом) будет окрашено в красный цвет только тогда, если его ближайшим соседом слева является элемент B (выделение жирным). Например: 
HTML:
```
<h1>Заголовок</h1>

<p>Параграф 1</p>

<p>Параграф 2</p>

<p>Параграф 3</p>
CSS:

h1+p {font-size: 1.5em;}
```
Только параграф 1 получит увеличенный размер шрифта, так как он является смежным с элементом h1.

### Общий комбинатор родственников E ~ F — соответствует элементу F, которому предшествует элемент E. В отличие от предыдущего комбинатора, здесь выбираются все соседи, а не только непосредственные. Если записать соседний селектор в Css коде в таком виде: h1 ~ p {color:red} То это будет означать, что все параграфы (P), у которых выше по коду расположен соседний элемент H1 (заголовок), будут окрашены в красный цвет. Имеются в виду именно соседние элементы (отношения вида «Сестры — Братья»). 
```
<h1>Заголовок</h1> 
<p>Параграф 1</p> 
<p>Параграф 2</p> 
<p>Параграф 3</p> 
CSS

h1~p {font-size: 1.5em;}
```
Все три параграфа будут иметь увеличенный размер шрифта, так как всем им предшествует элемент h1.
### Используйте любые селекторы
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

Селекторы в Css можно еще и группировать. Например, если у каких-то из них используется одно или несколько одинаковых правил, то их можно объединить в группу для уменьшения объема Css кода. Обратите внимание, что при группировке селекторы пишутся через запятую. Если одинаковых правил будет больше, то и экономия кода будет более ощутимой. А те правила, которые были уникальными, нужно по-прежнему записывать индивидуально. 

### Приоритеты Css свойств (с important и без него) 
- свойства, принятые по умолчанию, имеют самый низший приоритет. 
- Более высокий приоритет имеют свойства, которые назначит пользователь в настройках своего браузера. Эти стили будут применены к любым документам, которые он просматривает в этом обозревателе. 
Это называется «пользовательские стили» и они имеют приоритет выше, чем стили, которые определены в спецификации по умолчанию. 
- Но еще больший приоритет будут иметь так называемые авторские стили. 
Под авторскими стилями имеются в виду свойства, которые подключаются к Html документу любым из трех основных способов (тег или атрибут Style в Css, а также внешний файл с таблицами стилей). Т.е., если я (разработчик сайта) захотел использовать в оформлении какого-либо элемента Html кода стили отличные от дефолтных, то пользователь своим собственным файлом Css перебить мое оформление не сможет. 

#### Important
```
p {color:red !important;} 
```
Если у пользователя в его собственном файле стилей, который он подключил к браузеру, будет прописано это же свойство с Important, то все абзацы он будет видеть в красном цвете. Но ведь и автор (разработчик) сайта мог использовать Important для этого свойства. Кто же тогда победит и чей приоритет окажется выше? 
Решили, что пользовательские стили с Important будут иметь по-любому более высокий приоритет, чем авторские стили, что с Important, что без него. 
### Приоритет будет убывать сверху вниз: 
- Пользовательские с Important 
- Авторские с Important 
- Авторские 
- Пользовательские 
Стили, принятые для Html элементов в спецификации по умолчанию (когда ни автор, ни пользователь ничего другого не задали) 
### Как повышают приоритеты Css свойств в авторских стилях 
Допустим, что у нас имеется фрагмент кода со следующими Html элементами (параграф внутри контейнера Div): 
```
<div id="in" class="box"> 
     <p id="out" class="sbox">Содержимое контейнера </p> 
</div> 
```
сначала пропишем такие свойства: 
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
Кроме этого сами селекторы имеют градацию по приоритетам. Самый высокий приоритет у ID. В этом примере цвет текста будет синим именно потому, что приоритет Id  будет выше, чем у селектора тега: 
```
p {color:red} 
#out {color:blue} 
```
Дальше по лесенке приоритетов, направленной вниз, следуют селекторы классов, псевдоклассов и атрибутов. В следующем примере опять проиграет тег (p) и цвет текста абзаца будет синим, ибо тягается он с селектором более высокого приоритета (класса): 
```
p {color:red} 
.sbox {color:blue} 
```
самым низким приоритетом (не считая универсальный *, обладающего нижайшим весом ) обладают селекторы тегов и псевдоэлементов. 

## step 00
```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>We are Elegance</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" type="text/css" href="css/normal.css">
  <link rel="stylesheet" type="text/css" href="css/styles.css">
 
  <link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
  <!--[if lt IE 9]><script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7/html5shiv.min.js"></script><![endif]-->
</head>
<body>
<!--///////////////////////////////////////////////////////
       // Navigation section 
////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // About section 
////////////////////////////////////////////////////////-->
         <h1>ABOUT</h1>
         WHO WE ARE ?
         
          <p>We are Elegance. We create stunning identities for our clients that people fall in love with.&nbsp;
            <br>Whether it's an app icon, a logo for a hot startup, or just an illustration, we'll work hard until you can't help but say "WOW!". 
          </p>
          <img src="../images/about.png" alt="about.png">
<!--///////////////////////////////////////////////////////
       // Main section 
////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // Footer section 
////////////////////////////////////////////////////////-->

</body>
</html>

```

## step 01

index.html
```
<!--///////////////////////////////////////////////////////
       // Navigation section 
////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // About section 
////////////////////////////////////////////////////////-->
  <div class="about-box" id="about">
    <section class="about-box-back">
      <div class="w-container">
        
        <div class="wrap">
          <div class="about">
            <h1 class="about-heading">ABOUT</h1>
            <div class="about-text">WHO WE ARE ?</div>
            <div class="separator"></div>
          </div>
          <p class="about-des">We are Elegance. We create stunning identities for our clients that people fall in love with.&nbsp;
            <br>Whether it's an app icon, a logo for a hot startup, or just an illustration, we'll work hard until you can't help but say "WOW!". 
          </p>
          <img class="about-img" src="../images/about.png" alt="about.png">
        </div>
      
      </div>
    </section>
  </div>
<!--///////////////////////////////////////////////////////
       // Main section 
////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // Footer section 
////////////////////////////////////////////////////////-->
```

style.css
```
body, html { font-size: 100%; padding: 0; margin: 0; height: 100%; }
body {
  overflow-x: visible;
  overflow-y: visible;
  font-size: 15px;
  line-height: 20px;
  font-family: 'Lato', Calibri, Arial, sans-serif;
  color: #b3b9bf;
  background: #f9f9f9;
}
h1 {
  margin: 10px 0px;
  color: white;
  font-size: 40px;
  line-height: 45px;
  font-weight: 700;
  text-align: center;
}

.about-box {
  padding-top: 15px;
  background-color: #323A45;
}
.about-box-back {
  background-color: transparent;
}

.about {}

.separator {
  display: block;
  width: 100%;
  height: 0px;
  margin: 0px auto 10px;
  padding-top: 0px;
  padding-bottom: 0px;
  border-bottom: 4px double rgba(0, 0, 0, 0.23);
  box-shadow: none;
  color: #333;
}

.about-text {
  display: block;
  margin: 20px auto;
  padding-left: 0px;
  color: white;
  text-align: center;
}
.about-heading {
  color: white;
}
.about-des {
  color: white;
  text-align: center;
}
.about-img {
  display: block;
  margin: 50px auto 35px;
  text-align: center;
}

.wrap {
  margin-top: 40px;
  margin-bottom: 40px;
  padding: 20px 10px;
  border-bottom: 0px none black;
  color: #333;
  }
```
normal.css
```
html
  {
    height:100%
  }

body
  {
    margin:0;
    min-height:100%;
    background-color:#fff;
    color:#333
  }

img
  {
    max-width:100%;
    vertical-align:middle;
    display:inline-block
  }

img
  {
    border:0
  }

.w-container
  {
    margin-left:auto;
    margin-right:auto;
    max-width:940px
  }
```

## step 02

```
  <link rel="stylesheet" type="text/css" href="../css/reset.css">
 
<!--///////////////////////////////////////////////////////
       // Navigation section 
////////////////////////////////////////////////////////-->


<!--///////////////////////////////////////////////////////
       // Main section 
////////////////////////////////////////////////////////-->
<!--///////////////////////////////////////////////////////
       // About section 
////////////////////////////////////////////////////////-->
  <div class="about-box" id="about">
    <section class="about-box-back">
      <div class="w-container">
        
        <div class="wrap">
          <div class="about">
            <h1 class="about-heading">ABOUT</h1>
            <div class="about-text">WHO WE ARE ?</div>
            <div class="separator"></div>
          </div>
          <p class="about-des">We are Elegance. We create stunning identities for our clients that people fall in love with.&nbsp;
            <br>Whether it's an app icon, a logo for a hot startup, or just an illustration, we'll work hard until you can't help but say "WOW!". 
          </p>
          <img class="about-img" src="../images/about.png" alt="about.png">
        </div>
      
      </div>
    </section>
  </div>

<!--///////////////////////////////////////////////////////
       // End about section 
//////////////////////////////////////////////////////////-->
  
       <!--///////////////////////////////////////////////////////
       // Who We Are Section
       //////////////////////////////////////////////////////////-->

  <div class="exp service-parlex">

    <div class="exp-back">

      <div class="w-container">

          <div class="wrap">

            <div class="w-row exp-des">
              
                <div class="w-col w-col-6 exp-col1">
                   <div class="col1-div">
                      <div class="exp-box">
                         <h3 class="exp-box-h3">Who We Are</h3>
                         <p>At Elegance, we have highly skilled and professional team of dedicated web professionals to take care of your projects.     Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. </br> Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                         </p>           
                        <div class="buttons">
                              <div class="btn-ex-one">
                                  <a class="ex-btn" href="#">Read More</a>
                              </div>
                              <div class="btn-ex-two">
                                  <a class="ex-btn-two" href="#">Buy Now!</a>
                              </div>
                        </div>
                      </div>
                  </div>
                </div>

                <div class="w-col w-col-6 exp-col2">
                  <div class="col2-div">
                    <img src="../images/who-we-are.png">
                  </div>
                </div>

            </div>

          </div>

      </div>

    </div>

  </div>


<!--///////////////////////////////////////////////////////
       // End Who We Are section 
       //////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // Call to action section 
       //////////////////////////////////////////////////////////--> 

  <div class="call-to-action">
    <div class="call-to-back">
      <div class="w-container">
        <div class="wrap">
          <div class="w-row call-row">
            <div class="w-col w-col-9 cal-col-1">
              <h3 class="call-to-h3">Elegance | Responsive Onepage HTML Tempalte</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique.&nbsp;</p>
            </div>
            <div class="w-col w-col-3"><a class="call-to-butn" href="#">Buy Now!</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>


<!--///////////////////////////////////////////////////////
       // End call to action section 
       //////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // Footer section 
////////////////////////////////////////////////////////-->

```
normal.css
```
html  {
    height:100%;
  }

body  {
    margin:0;
    min-height:100%;
    background-color:#fff;
    color:#333;
  }

img  {
    max-width:100%;
    vertical-align:middle;
    display:inline-block;
    border:0;
  }

.w-container   {
    margin-left:auto;
    margin-right:auto;
    max-width:940px;
  }

.w-container:before,.w-container:after
{
    content:" ";
    display:table;
}
     .w-container:after
{
    clear:both;
}

.w-container .w-row {
    margin-left:-10px;
    margin-right:-10px;
}

.w-row:before,.w-row:after {
    content:" ";
    display:table;
}

.w-row:after {
    clear:both;
}

.w-row .w-row {
    margin-left:0;
    margin-right:0;
}

.w-col {
    position:relative;
    float:left;
    width:100%;
    min-height:1px;
    padding-left:10px;
    padding-right:10px;
}
.w-col .w-col {
    padding-left:0;
    padding-right:0;
}

.w-col-1 {
    width:8.333333333333332%;
}
.w-col-2 {
    width:16.666666666666664%;
}
.w-col-3 {
    width:25%;
}
.w-col-4 {
    width:33.33333333333333%;
}
.w-col-5 {
    width:41.66666666666667%;
}
.w-col-6 {
    width:50%;
}
 .w-col-7 {
    width:58.333333333333336%;
}
 .w-col-8 {
    width:66.66666666666666%;
}
 .w-col-9 {
    width:75%;
}
 .w-col-10 {
    width:83.33333333333334%;
}
 .w-col-11 {
    width:91.66666666666666%;
}
 .w-col-12 {
    width:100%;
}


```
style.css
```
*, *:after, *:before { -webkit-box-sizing: border-box; -moz-box-sizing: border-box; box-sizing: border-box; }
body, html { font-size: 100%; padding: 0; margin: 0; height: 100%; }

body {
  overflow-x: visible;
  overflow-y: visible;
  font-size: 15px;
  line-height: 20px;
  font-family: 'Lato', Calibri, Arial, sans-serif;
  color: #b3b9bf;
  background: #f9f9f9;
}
h1 {
  margin: 10px 0px;
  color: white;
  font-size: 40px;
  line-height: 45px;
  font-weight: 700;
  text-align: center;
}

h3 {
  margin: 10px 0px;
  font-size: 18px;
  line-height: 30px;
  font-weight: 700;
}

p {
  margin-bottom: 5px;
  color: #d6d6d6;
  text-align: left;
}
.about-box {
  padding-top: 15px;
  background-color: #323A45;
}
.about-box-back {
  background-color: transparent;
}

.about {}

.separator {
  display: block;
  width: 100%;
  height: 0px;
  margin: 0px auto 10px;
  padding-top: 0px;
  padding-bottom: 0px;
  border-bottom: 4px double rgba(0, 0, 0, 0.23);
  box-shadow: none;
  color: #333;
}

.about-text {
  display: block;
  margin: 20px auto;
  padding-left: 0px;
  color: white;
  text-align: center;
}
.about-heading {
  color: white;
}
.about-des {
  color: white;
  text-align: center;
}
.about-img {
  display: block;
  margin: 50px auto 35px;
  text-align: center;
}

.wrap {
  margin-top: 40px;
  margin-bottom: 40px;
  padding: 20px 10px;
  border-bottom: 0px none black;
  color: #333;
  }

.exp {
  background-color: transparent;
 /* background-image: url('../images/bg.png'); */
  background-position: 0% 0%;
  background-size: 125px;
  background-repeat: repeat;
  background-attachment: scroll;
}

 .exp-des {
  display: block;
  margin: 30px 10px;
  padding: 10px 5px;
}

.exp-back {
  padding-top: 15px;
  background-color: transparent;
  background-image: -webkit-linear-gradient(rgba(179, 105, 149, 0.70), #b36995);
  background-image: -o-linear-gradient(rgba(179, 105, 149, 0.70), #b36995);
  background-image: linear-gradient(rgba(179, 105, 149, 0.70), #b36995);
}

.exp-box-h3 {
  font-size: 65px;
  font-weight: 100;
  margin-bottom: 40px;
  margin-top: 25px;
  color: #FFF;
  border-bottom: 4px double rgba(255, 255, 255, 0.53);
  padding-bottom: 45px;
}

```
## step 03

```

<!--div id='wrapper'-->
<!--///////////////////////////////////////////////////////
       // Navigation section 
////////////////////////////////////////////////////////-->


<!--///////////////////////////////////////////////////////
       // Main section 
////////////////////////////////////////////////////////-->
<!--///////////////////////////////////////////////////////
       // About section 
////////////////////////////////////////////////////////-->
  <div class="about-box" id="about">
    <section class="about-box-back">
      <div class="w-container">
        
        <div class="wrap">
          <hgroup>
            <h1 class="about-heading">ABOUT</h1>
            <div class="about-text">WHO WE ARE ?</div>
            <div class="separator"></div>
          </hgroup>
          <p class="about-des">We are Elegance. We create stunning identities for our clients that people fall in love with.&nbsp;
            <br>Whether it's an app icon, a logo for a hot startup, or just an illustration, we'll work hard until you can't help but say "WOW!". 
          </p>
          <img class="about-img" src="../images/about.png" alt="about.png">
        </div>
      
      </div>
    </section>
  </div>

<!--///////////////////////////////////////////////////////
       // End about section 
//////////////////////////////////////////////////////////-->
  
       <!--///////////////////////////////////////////////////////
       // Who We Are Section
       //////////////////////////////////////////////////////////-->

  <div class="exp service-parlex">

    <div class="exp-back">

      <div class="w-container">

          <div class="wrap">

            <div class="w-row exp-des">
              
                <div class="w-col w-col-6 exp-col1">
                   <div class="col1-div">
                      <hgroup> <!-- class="exp-box" -->
                               <h3 class="exp-box-h3">Who We Are</h3>
                               <p>
                            At Elegance, we have highly skilled and professional team of dedicated web professionals to take care of your projects.     Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. </br> Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                               </p>           
                               <div class="buttons">
                                  <div class="btn-ex-one">
                                      <a class="ex-btn" href="#">Read More</a>
                                  </div>
                                  <div class="btn-ex-two">
                                      <a class="ex-btn-two" href="#">Buy Now!</a>
                                  </div>
                               </div>
                      </hgroup>

                  </div>
                </div>

                <div class="w-col w-col-6 exp-col2">
                  <div class="col2-div">
                    <img src="../images/who-we-are.png">
                  </div>
                </div>

            </div>

          </div>

      </div>

    </div>

  </div>


<!--///////////////////////////////////////////////////////
       // End Who We Are section 
       //////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // Call to action section 
       //////////////////////////////////////////////////////////--> 


  <div class="call-to-action">
    <div class="call-to-back">
      <div class="w-container">
        <div class="wrap">
          <div class="w-row call-row">
            <div class="w-col w-col-9 cal-col-1">
              <h3 class="call-to-h3">Elegance | Responsive Onepage HTML Tempalte</h3>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique.&nbsp;</p>
            </div>
            <div class="w-col w-col-3"><a class="call-to-butn" href="#">Buy Now!</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>


<!--///////////////////////////////////////////////////////
       // End call to action section 
       //////////////////////////////////////////////////////////-->

<!--///////////////////////////////////////////////////////
       // Service section 
       //////////////////////////////////////////////////////////-->


  <section class="service-parlex" id="service">
    <section class="service-back">
      <div class="w-container">
        <div class="wrap">
          <div class="service-combo">
            <div class="services">
              <h1 class="service-heading">SERVICES</h1>
              <div class="services-text">WHAT WE DO?</div>
              <div class="separator service"></div>
            </div>
            <div class="services-text">“ THE BEST RESULTS ARE OBTAINED BY TASKING THE RIGHT PEOPLE TO THE RIGHT PROJECT ”
              <br>We understand that everybody has their unique strengths and we put that knowledge to use by assembling the most efficient team possible for your project. You know your business better than anyone. Your insights, combined with our skills
              and creativity, will result in branding and marketing that truly stand out. We’re ready to get started.</div>
            <div class="w-row">
              <div class="w-col w-col-3 services-column">
                <figure class="service-icon">
                  <img src="../images/services/Web-Design-Development.png">
                  <figurecaption>
                  <h4 class="service-head">WEB DESIGN &amp; DEVELOPMENT</h4>
                  </figurecaption>
                </figure>
              </div>
              <div class="w-col w-col-3">
                <figure class="service-icon">
                  <img src="../images/services/Branding-Identity.png">
                  <figurecaption>
                  <h4 class="service-head">Branding/Positioning &amp; IDENTITY</h4>
                  </figurecaption>
                </figure>
              </div>
              <div class="w-col w-col-3">
                <figure class="service-icon">
                  <img src="../images/services/Motion-Video.png">
                  <figurecaption>
                  <h4 class="service-head">Marketing Communications</h4>
                  </figurecaption>
                </figure>
              </div>
              <div class="w-col w-col-3">
                <figure class="service-icon">
                  <img src="../images/services/UX-UI.png">
                  <figurecaption>
                  <h4 class="service-head">UI/UX Design<br>Mobile Design</h4>
                  </figurecaption>
                </figure>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </section>

<!--///////////////////////////////////////////////////////
       // End Service section 
       //////////////////////////////////////////////////////////-->
<!--///////////////////////////////////////////////////////
       // Process section 
       //////////////////////////////////////////////////////////-->

  <div class="process-parlex">
    <div class="process-back">
      <div class="w-container">
        <div class="wrap">
          <div class="process">
            <h1 class="our-process-heading">OUR PROCESS</h1>
            <div class="separator"></div>
          </div>
          <div class="process-text">
            <div class="process-text">Our process is straight forward, simple, &amp; successful.</div>
            <div class="w-row">
              <div class="w-col w-col-3">
                <div class="hi-icon-wrap hi-icon-effect-5 hi-icon-effect-5a">
                   <a href="#set-1" class="hi-icon hi-icon-locked">Security</a>
                </div>
                <h4 class="our-process-sys">BRAINSTORM</h4>
                <p class="process-paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. Aenean faucibus nibh et justo
                  cursus id rutrum lorem imperdiet. Nunc ut sem vitae risus tristique posuere.</p>
              </div>
              <div class="w-col w-col-3">
                <div class="hi-icon-wrap hi-icon-effect-5 hi-icon-effect-5a">
          <a href="#set-1" class="hi-icon hi-icon-mobile">Mobile</a>
        </div>
                <h4 class="our-process-sys">PLAN</h4>
                <p class="process-paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. Aenean faucibus nibh et justo
                  cursus id rutrum lorem imperdiet. Nunc ut sem vitae risus tristique posuere.</p>
              </div>
              <div class="w-col w-col-3">
                <div class="hi-icon-wrap hi-icon-effect-5 hi-icon-effect-5a">
          <a href="#set-1" class="hi-icon hi-icon-screen">Desktop</a>
        </div>
                <h4 class="our-process-sys">DESIGN</h4>
                <p class="process-paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. Aenean faucibus nibh et justo
                  cursus id rutrum lorem imperdiet. Nunc ut sem vitae risus tristique posuere.</p>
              </div>
              <div class="w-col w-col-3">
                <div class="hi-icon-wrap hi-icon-effect-5 hi-icon-effect-5a">
          <a href="#set-1" class="hi-icon hi-icon-earth">Partners</a>
        </div>
                <h4 class="our-process-sys">DEVELOP</h4>
                <p class="process-paragraph">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius enim in eros elementum tristique. Duis cursus, mi quis viverra ornare, eros dolor interdum nulla, ut commodo diam libero vitae erat. Aenean faucibus nibh et justo
                  cursus id rutrum lorem imperdiet. Nunc ut sem vitae risus tristique posuere.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

<!--///////////////////////////////////////////////////////
       // End Process section 
       //////////////////////////////////////////////////////////-->
<!--///////////////////////////////////////////////////////
       // Footer section 
////////////////////////////////////////////////////////-->
<!--/div-->

```

style.css
```
@CHARSET "utf-8";
body {
  
  font-size: 15px;
  line-height: 20px;
  font-family: 'Lato', Calibri, Arial, sans-serif;
  color: #b3b9bf;
  background: #f9f9f9;
}
h1 {
  margin: 10px 0px;
  color: white;
  font-size: 40px;
  line-height: 45px;
  font-weight: 700;
  text-align: center;
}

h3 {
  margin: 10px 0px;
  font-size: 18px;
  line-height: 30px;
  font-weight: 700;
}

p {
  margin-bottom: 5px;
  color: #d6d6d6;
  text-align: left;
}
.about-box {
  padding-top: 15px;
  background-color: #323A45;
}
.about-box-back {
  background-color: transparent;
}

.separator {
  display: block;
  width: 100%;
  height: 0px;
  margin: 0px auto 10px;
  padding-top: 0px;
  padding-bottom: 0px;
  border-bottom: 4px double rgba(0, 0, 0, 0.23);
  box-shadow: none;
  color: #333;
}

.about-text {
  display: block;
  margin: 20px auto;
  padding-left: 0px;
  color: white;
  text-align: center;
}
.about-heading {
  color: white;
}
.about-des {
  color: white;
  text-align: center;
}
.about-img {
  display: block;
  margin: 50px auto 35px;
  text-align: center;
}

.wrap {
  margin-top: 40px;
  margin-bottom: 40px;
  padding: 20px 10px;
  border-bottom: 0px none black;
  color: #333;
  }

.exp {
  background-position: 0% 0%;
  background-size: 125px;
  background-repeat: repeat;
  background-attachment: scroll;
}

 .exp-des {
  display: block;
  margin: 30px 10px;
  padding: 10px 5px;
}

.exp-back {
  padding-top: 15px;
  background-color: transparent;
  background-image: -webkit-linear-gradient(rgba(179, 105, 149, 0.70), #b36995);
  background-image: -o-linear-gradient(rgba(179, 105, 149, 0.70), #b36995);
  background-image: linear-gradient(rgba(179, 105, 149, 0.70), #b36995);
}

.exp-box-h3 {
  font-size: 65px;
  font-weight: 100;
  margin-bottom: 40px;
  margin-top: 25px;
  color: #FFF;
  border-bottom: 4px double rgba(255, 255, 255, 0.53);
  padding-bottom: 45px;
}

.btn-ex-one {
  margin-top: 30px;
  float: left;
}

.ex-btn {
  color: #FFF;
  font-weight: 100;
  padding: 15px;
  border: 1px solid #FFF;
  border-radius: 4px;

  font-size: 25px;
}

.buttons {
  margin-top: 30px;
}

.ex-btn:hover {
  background: #323A45;
  color: #FFF;
  border: 1px solid #323A45;
}


.ex-btn-two:hover {
  color: #FFF;
  border: 1px solid #FFF;
  background: rgba(0, 0, 0, 0);
}

.ex-btn-two {
  color: #FFF;
  background: #223C4B;
  padding: 10px;
  border: 1px solid #223C4B;
  border-radius: 4px ;
  font-weight: 100;
  font-size: 35px;
}

.btn-ex-two {
  float: left;
  margin-top: 30px;
  margin-left: 15px;
}

.call-to-action {
  background-color: #303030;
  background-image: none;
  background-position: 0% 0%;
  background-size: auto;
  background-repeat: repeat;
  background-attachment: scroll;
}
.call-row {
  padding: 20px 15px;
  border: 1px solid #ccc;
  border-top-right-radius: 0px;
  border-bottom-left-radius: 0px;
  background-color: transparent;
}
.call-to-h3 {
  background-color: transparent;
  color: #eee;
  text-align: left;
  text-decoration: none;
}
.call-to-butn {
  display: block;
  width: 60%;
  margin: 25px auto 0px;
  padding: 9px;
  border: 1px solid #eee;
  border-radius: 2px;
  color: #eee;
  text-decoration: none;
  text-align: center;
}
.call-to-butn:hover {
  background-color: #ed5565;
  border: 1px solid #ed5565;
}
.cal-col-1 {
  border-right: 1px solid white;
}

.service-combo {
  padding-right: 10px;
  padding-left: 10px;
  background-color: transparent;
}
.service-h1 {
  padding-bottom: 12px;
  border-bottom: 2px solid #474747;
}
.service-button {
  display: block;
  margin: 10px auto;
  padding: 8px;
  background-image: -webkit-linear-gradient(#13ad7d, #13ad7d);
  background-image: -o-linear-gradient(#13ad7d, #13ad7d);
  background-image: linear-gradient(#13ad7d, #13ad7d);
  box-shadow: none;
  text-align: center;
}
.services-text {
  margin-top: 20px;
  margin-bottom: 20px;
  color: white;
  font-size: 14px;
  line-height: 25px;
  text-align: center;
}

.service-parlex {
  padding-top: 0px;
  background-image: url('../../images/bg.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}

.service-back {
  padding-top: 15px;
  background-color: transparent;
  background-image: -webkit-linear-gradient(#800b36, rgba(128, 11, 54, 0.50) 56%);
  background-image: -o-linear-gradient(#800b36, rgba(128, 11, 54, 0.50) 56%);
  background-image: linear-gradient(#800b36, rgba(128, 11, 54, 0.50) 56%);
}


.separator.service {
  border-bottom-color: white;
  box-shadow: none;
}

.service-heading {
  color: white;
}


.service-icon {
  margin: auto;
  width: 100%;
  text-align: center;
  padding-top: 20px;
  padding-bottom: 20px;
}

.service-head {
  color: white;
}

```

normal.css
```
@CHARSET "utf-8";
html, body  {
    height:100%;
    padding: 0;
    margin: 0;
    font-size: 100%;
  }

article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section{
    display: block;
}

*, *:after, *:before { -webkit-box-sizing: border-box; -moz-box-sizing: border-box; box-sizing: border-box; }

body  {
    overflow-x: visible;
    overflow-y: visible;
    min-height:100%;
    background-color:#fff;
    color:#333;
  }

#wrapper {
    max-width: 100%;
    display: -webkit-box;
    -webkit-box-orient: vertical;
}

header {
    background: #000;
    padding: 20px;
}

nav {
    background: #878787;
    color: #fff;
}

nav ul li {
    display: inline-block;
    font: bold 10px Arial;
    padding: 10px;
}
img  {
    max-width:100%;
    vertical-align:middle;
    display:inline-block;
    border:0;
  }
nav ul li a {
    color: white;
    text-decoration: none;
}
nav ul li a:hover {
    color: blue;
    text-decoration: underline;
}
.w-container   {
    margin-left:auto;
    margin-right:auto;
    max-width:940px;
  }

.w-container:before,.w-container:after
{
    content:" ";
    display:table;
}
     .w-container:after
{
    clear:both;
}

.w-container .w-row {
    margin-left:-10px;
    margin-right:-10px;
}

.w-row:before,.w-row:after {
    content:" ";
    display:table;
}

.w-row:after {
    clear:both;
}

.w-row .w-row {
    margin-left:0;
    margin-right:0;
}

.w-col {
    position:relative;
    float:left;
    width:100%;
    min-height:1px;
    padding-left:10px;
    padding-right:10px;
}
.w-col .w-col {
    padding-left:0;
    padding-right:0;
}

.w-col-1 {
    width:8.333333333333332%;
}
.w-col-2 {
    width:16.666666666666664%;
}
.w-col-3 {
    width:25%;
}
.w-col-4 {
    width:33.33333333333333%;
}
.w-col-5 {
    width:41.66666666666667%;
}
.w-col-6 {
    width:50%;
}
 .w-col-7 {
    width:58.333333333333336%;
}
 .w-col-8 {
    width:66.66666666666666%;
}
 .w-col-9 {
    width:75%;
}
 .w-col-10 {
    width:83.33333333333334%;
}
 .w-col-11 {
    width:91.66666666666666%;
}
 .w-col-12 {
    width:100%;
}

```
