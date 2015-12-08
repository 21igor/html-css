# 11-css-danco

```
 <div class="buttons">
            <div class="btn-ex-one">
                   <a class="ex-btn" href="#">Read More</a>
               </div>
               <div class="btn-ex-two">
                   <a class="ex-btn-two" href="#">Buy Now!</a>
               </div>
 </div>

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

.call-row {
  padding: 20px 15px;
  border: 1px solid #ccc;
  border-top-right-radius: 0px;
  border-bottom-left-radius: 0px;
  background-color: transparent;
}
```

### border-bottom-left-radius

Устанавливает радиус скругления левого нижнего уголка рамки. Если рамка не задана, то скругление также происходит и с фоном.
```
border-bottom-left-radius: [значение | проценты] [значение | проценты]
```
В качестве радиуса указывается любое допустимое в CSS значение (px, cm, in, em и др.), а также проценты, в этом случае радиус скругления считается от ширины блока.
Необязательное второе значение предназначено для создания эллиптического уголка, первое значение при этом устанавливает радиус по горизонтали, а второе — радиус по вертикали 
```
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
```
### services
```
           <div class="w-row">
              <div class="w-col w-col-3 services-column">
                <figure class="service-icon">
                  <img src="images/services/Web-Design-Development.png">
                  <figurecaption>
                  <h4 class="service-head">WEB DESIGN &amp; DEVELOPMENT</h4>
                  </figurecaption>
                </figure>
              </div>

.service-icon {
  margin: auto;
  width: 100%;
  text-align: center;
  padding-top: 20px;
  padding-bottom: 20px;
}

.service-parlex {
  padding-top: 0px;
  background-image: url('../images/bg.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
```
## background-size
Масштабирует фоновое изображение согласно заданным размерам.
```
background-size: [ <значение> | <проценты> | auto ]{1,2} | cover | contain
```
- значение
Задает размер в любых доступных для CSS единицах — пикселы (px), сантиметры (cm), em и др.
- проценты
Задает размер фоновой картинки в процентах от ширины или высоты элемента.
- auto
Если задано одновременно для ширины и высоты (auto auto), размеры фона остаются исходными; если только для одной стороны картинки (100px auto), то размер вычисляется автоматически исходя из пропорций картинки.
- cover
Масштабирует изображение с сохранением пропорций так, чтобы его ширина или высота равнялась ширине или высоте блока.
- contain
Масштабирует изображение с сохранением пропорций таким образом, чтобы картинка целиком поместилась внутрь блока.

## background-image

Устанавливает фоновое изображение для элемента. Если одновременно для элемента задан цвет фона, он будет показан, пока фоновая картинка не загрузится полностью. То же произойдет, если изображения не доступны или их показ в браузере отключен. В случае наличия в рисунке прозрачных областей, через них будет проглядывать фоновый цвет. В CSS3 допустимо указывать несколько фоновых изображений, перечисляя их параметры через запятую.
```
CSS2.1 background-image: url(путь к файлу) | none | inherit
CSS3    background-image: url(путь к файлу) | none[, url(путь к файлу) | none]*
```
- url В качестве значения используется путь к графическому файлу, который указывается внутри конструкции url(). Путь к файлу при этом можно писать как в кавычках (двойных или одинарных), так и без них.

- none Отменяет фоновое изображение для элемента.
- inherit Наследует значение родителя.

## Свойство background-attachment
Свойство background-attachment устанавливает, будет ли прокручиваться фоновое изображение вместе с содержимым элемента. Изображение может быть зафиксировано и оставаться неподвижным, либо перемещаться совместно с документом. В CSS3 можно указать несколько значений для ряда фоновых изображений, перечисляя значения через запятую.
```
CSS2.1 background-attachment: fixed | scroll | inherit
CSS3    background-attachment: fixed | scroll | local[, fixed | scroll | local]*
```
- fixed Делает фоновое изображение элемента неподвижным.
- scroll Позволяет перемещаться фону вместе с содержимым.
- inherit Наследует значение родителя.
- local Фон фиксируется с учётом поведения элемента. Если элемент имеет прокрутку, то фон будет прокручиваться вместе с содержимым, но фон выходящий за рамки элемента остаётся на месте.

## background-repeat
Определяет, как будет повторяться фоновое изображение, установленное с помощью свойства background-image. Можно установить повторение рисунка только по горизонтали, по вертикали или в обе стороны. В CSS3 допустимо указывать несколько значений для каждого фона, перечисляя значения через запятую.

```
CSS2.1 background-repeat: no-repeat | repeat | repeat-x | repeat-y | inherit
CSS3    background-repeat: <повторение> [ , <повторение> ]* 

<повторение> = repeat-x | repeat-y | [repeat | space | round | no-repeat]{1,2}
```
Допустимо указывать два значения, первое ключевое слово задаёт повторение по горизонтали, второе по вертикали.

- no-repeat Устанавливает одно фоновое изображение в элементе без его повторений, положение которого определяется свойством background-position (по умолчанию в левом верхнем углу). Аналогично no-repeat no-repeat.
- repeat Фоновое изображение повторяется по горизонтали и вертикали. Аналогично repeat repeat.
```
<повторение> = repeat-x | repeat-y | [repeat | space | round | no-repeat]{1,2}
```
- repeat-x Фоновый рисунок повторяется только по горизонтали. Аналогично repeat no-repeat.
- repeat-y Фоновый рисунок повторяется только по вертикали. Аналогично no-repeat repeat.
- inherit Наследует значение родителя.
- space Изображение повторяется столько раз, чтобы полностью заполнить область; если это не удаётся, между картинками добавляется пустое пространство.
- round Изображение повторяется так, чтобы в области поместилось целое число рисунков; если это не удаётся сделать, то фоновые рисунки масштабируются.
```
<div class="w-row">

  <div class="w-col w-col-3">

  <div class="hi-icon-wrap hi-icon-effect-5 hi-icon-effect-5a">
 
 <a href="#set-1" class="hi-icon hi-icon-locked">   Security</a>
 </div>
```
## Правило @font-face
 Правило @font-face позволяет определить настройки шрифтов, а также загрузить специфичный шрифт на компьютер пользователя.
```
@font-face { свойства шрифта }
```
Внутри конструкции @font-face может находиться набор свойств для изменения параметров шрифта (font-family, font-size, font-style и др.), а также ссылка на шрифтовой файл. Ссылка записывается в виде src: url(URI), где URI — относительный или абсолютный путь к файлу.
```
@font-face {
  font-family: 'ecoicon';
  src:url('../fonts/ecoicons/ecoicon.eot');
  src:url('../fonts/ecoicons/ecoicon.eot?#iefix') format('embedded-opentype'),
    url('../fonts/ecoicons/ecoicon.woff') format('woff'),
    url('../fonts/ecoicons/ecoicon.ttf') format('truetype'),
    url('../fonts/ecoicons/ecoicon.svg#ecoicon') format('svg');

  font-weight: normal;
  font-style: normal;
}

.hi-icon-wrap {
  text-align: center;
  margin: 0 auto;
  padding: 2em 0 1em;
}

.hi-icon {
  display: inline-block;
  font-size: 0px;
  cursor: pointer;
  margin: 15px 30px;
  width: 90px;
  height: 90px;
  border-radius: 50%;
  text-align: center;
  position: relative;
  z-index: 1;
  color: #fff;
}
```
## cursor: pointer;
Устанавливает форму курсора, когда он находится в пределах элемента. 
```
cursor: [url('путь к курсору'),] | [ auto | crosshair | default | e-resize | help | move | n-resize | ne-resize | nw-resize | pointer | progress | s-resize | se-resize | sw-resize | text | w-resize | wait | inherit ]
```
- url Позволяет установить свой собственный курсор, для этого нужно указать путь к файлу с курсором.
- auto Вид курсора по умолчанию для текущего элемента.
- inherit Наследует значение родителя.

## z-index: 1;
Любые позиционированные элементы на веб-странице могут накладываться друг на друга в определенном порядке, имитируя тем самым третье измерение, перпендикулярное экрану. Каждый элемент может находиться как ниже, так и выше других объектов веб-страницы, их размещением по z-оси и управляет z-index. Это свойство работает только для элементов, у которых значение position задано как absolute, fixed или relative.

Синтаксис
```
z-index: число | auto | inherit

.hi-icon:after {
  pointer-events: none;
  position: absolute;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  content: '';
  -webkit-box-sizing: content-box; 
  -moz-box-sizing: content-box; 
  box-sizing: content-box;
}
```
## border-radius
Устанавливает радиус скругления уголков рамки. 
Если рамка не задана, то скругление также происходит и с фоном.
```
border-radius: <радиус>{1,4} [ / <радиус>{1,4}]
```
- 1   Радиус указывается для всех четырех уголков.
- 2   Первое значение задает радиус верхнего левого и нижнего правого уголка, второе значение — верхнего правого и нижнего левого уголка.
- 3   Первое значение задает радиус для верхнего левого уголка, второе — одновременно для верхнего правого и нижнего левого, а третье — для нижнего правого уголка.
- 4   По очереди устанавливает радиус для верхнего левого, верхнего правого, нижнего правого и нижнего левого уголка.

```
.hi-icon-screen:before {
  content: "\e00a";
}

.hi-icon-locked:before {
  content: "\e001";
}

.hi-icon-videos:before {
  content: "\e005";
}
```
## Псевдоэлемент :before
Псевдоэлемент :before применяется для отображения желаемого контента до содержимого элемента, к которому он добавляется. Работает совместно со свойством content.

При добавлении :before к блочному элементу, значение свойства display может быть только: block, inline, none, list-item. Все остальные значения будут трактоваться как block.
При добавлении :before к встроенному элементу, display ограничен значениями inline и none. Все остальные будут восприниматься как inline.
```
:before наследует стиль от элемента, к которому он добавляется.

элемент:before { content: "текст" }

.hi-icon-effect-5 .hi-icon {
  box-shadow: 0 0 0 4px rgba(255,255,255,1);
  overflow: hidden;
  -webkit-transition: background 0.3s, color 0.3s, box-shadow 0.3s;
  -moz-transition: background 0.3s, color 0.3s, box-shadow 0.3s;
  transition: background 0.3s, color 0.3s, box-shadow 0.3s;
}
```
## box-shadow
Добавляет тень к элементу. 

Допускается использовать несколько теней, указывая их параметры через запятую, при наложении теней первая тень в списке будет выше, последняя ниже. 

Если для элемента задается радиус скругления через свойство border-radius, то тень также получится с закругленными уголками. 

Добавление тени увеличивает ширину элемента, поэтому возможно появление горизонтальной полосы прокрутки в браузере.
```
box-shadow: none | <тень> [,<тень>]*
```
где тень:
```
inset <сдвиг по x> <сдвиг по y> <радиус размытия> <растяжение> <цвет>
```
- none Отменяет добавление тени.

- inset Тень выводится внутри элемента. Необязательный параметр.

- Цвет Цвет тени в любом доступном CSS формате, по умолчанию тень черная. Необязательный параметр.

####  сдвиг по x
Смещение тени по горизонтали относительно элемента. Положительное значение этого параметра задает сдвиг тени вправо, отрицательное — влево. Обязательный параметр.

#### сдвиг по y
Смещение тени по вертикали относительно элемента. Положительное значение задает сдвиг тени вниз, отрицательное — вверх. Обязательный параметр.

### размытие
Задает радиус размытия тени. Чем больше это значение, тем сильнее тень сглаживается, становится шире и светлее. Если этот параметр не задан, по умолчанию устанавливается равным 0, тень при этом будет четкой, а не размытой.

### растяжение
Положительное значение растягивает тень, отрицательное, наоборот, ее сжимает. Если этот параметр не задан, по умолчанию устанавливается 0, при этом тень будет того же размера, что и элемент.

## Свойство overflow
Свойство overflow управляет отображением содержания блочного элемента, если оно целиком не помещается и выходит за область заданных размеров.
```
overflow: auto | hidden | scroll | visible | inherit
```
- visible Отображается все содержание элемента, даже за пределами установленной высоты и ширины.
- hidden Отображается только область внутри элемента, остальное будет скрыто.
- scroll Всегда добавляются полосы прокрутки.
- auto Полосы прокрутки добавляются только при необходимости.
- inherit Наследует значение родителя.

## transition
Универсальное свойство, которое позволяет одновременно задать значения transition-property, transition-duration, transition-timing-function и transition-delay. Устанавливает эффект перехода между двумя состояниями элемента, они могут быть определены с помощью псевдоэлемента :hover или :active.
```
transition: <переход> [, <переход> ]*

<переход> = [ none | <transition-property> ] || <transition-duration> || 
<transition-timing-function> || <transition-delay>


.hi-icon-effect-5 .hi-icon:after {
  display: none;
}

.no-touch .hi-icon-effect-5 .hi-icon:hover {
  background: rgba(255,255,255,1);
  color: #3DE6BA;
  box-shadow: 0 0 0 8px rgba(255,255,255,0.3);
}

 <script src="js/modernizr.js"></script>

</body>
</html>
```
