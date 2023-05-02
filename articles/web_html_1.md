# Введение в HTML

Содрано [отсюда](https://msiter.ru/tutorials/html-nachalnogo-urovnya)

## Что нужно, чтобы создать веб-страницу

Большинство вещей в сети ничем не отличаются от аналогичных вещей в вашем домашнем компьютере: такие же файлы, хранящиеся в таких же подкаталогах.

HTML файлы – это обычные текстовые файлы. Таким образом, чтобы начать писать на языке HTML, вам необходим всего лишь обычный текстовый редактор.

Например, создайте файл `myfirstpage.html` с содержимым

```
Это моя первая веб-страница
```

Чтобы просматривать HTML файлы, они не обязательно должны быть размещены в сети Интернет. Откройте браузер и в адресной строке, где вы обычно вводите адрес сайтов, введите адрес созданного вами файла (например, `c:\html\myfirstpage.html`) и нажмите ввод.

## Структура HTML документа

Хотя основа документа HTML – простой текст, чтобы создать настоящий HTML документ, необходимо кое-что еще. А именно задать структуру документа HTML.

Структура документа HTML состоит из тегов, которые окружают содержимое и придают ему определенное техническое значение.

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html>
    <body>
        Это моя первая веб-страница
    </body>
</html>
```

Теперь сохраните документ, вернитесь в браузер и выберите команду "Обновить".

Внешний вид страницы никак не изменился. Однако предназначение HTML – определение значения для содержимого, а не внешнего представления, и данный пример показал нам несколько фундаментальных элементов веб-страницы, задающих базовую структуру документа HTML.

Первая строка, начинающаяся с `<!DOCTYPE...` говорит браузеру, что вы знаете, что делаете. Возможно в данный момент вы в действительности не представляете, что вы делаете, однако данная команда важна и стоит ее всегда писать. Если этого не сделать, то браузеры переключатся в режим "обратной совместимости" и будут действовать весьма своеобразным образом. Сейчас не стоит особенно беспокоиться об этой команде и ее значимости для структуры документа HTML. Подробнее о типах документов вы узнаете несколько позже. А пока просто запомните, что эту команду следует включать в начало любой веб-страницы.

Вернемся к нашему примеру. Следующая команда в структуре документа HTML, команда `<html>`, - открывающий тег, который прекращает все недомолвки и прямо говорит браузеру, что все, что между ним и закрывающим тегом `</html>`, является HTML документом. Все что находится между `<body>` и `</body>` является основным содержимым веб-страницы и выводится в окне браузера.

### Закрывающие теги

Теги `</body>` и `</html>` закрывают соответствующие открывающие теги. Все теги в структуре документа HTML должны быть закрыты. Хотя более ранние стандарты прохладно смотрели на то, что некоторые теги оставались открытыми, новые стандарты языка требуют, чтобы абсолютно все теги были закрыты. В любом случае следование этому правилу будет хорошей привычкой.

Не у всех тегов есть соответствующие закрывающие теги (вроде `<html></html>`). Некоторые теги, которые не заключают в себе контент, закрывают сами себя. Например, тег разрыва строки выглядит следующим образом: `<br/>`. Мы вернемся к этому примеру позднее. Все что нужно запомнить, это то, что все теги в структуре документа HTML должны быть закрыты, и большинство из них (те которые содержат какой-нибудь контент) имеют следующую форму: `открывающий тег → контент → закрывающий тег`.

### Атрибуты

У тегов также могут быть атрибуты. Атрибуты – это определенная дополнительная информация. Атрибуты определяются в открывающем теге, а их значения всегда заключаются в кавычки. Все это выглядит следующим образом:

```
<тег атрибут="значение">
    контент
</тег>
```

Подробнее о тегах с атрибутами мы поговорим немного позже.

### Элементы

Предназначение тегов – обозначать начало и конец элемента структуры документа HTML. Элементы же это кирпичики, из которых складывается веб-страница. Так, например, все что находится между тегами `<body>` и `</body>`, включая сами эти теги, является элементом body.

## Заголовок веб-документа

У каждой веб-страницы должна быть головная часть или заголовок документа.

Чтобы добавить заголовок документа HTML, измените код вашей веб-страницы следующим образом:

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html>
    <head>
        <title>
            Моя первая веб-страница
        </title>
    </head>
    <body>
        Это моя первая веб-страница
    </body>
</html>
```

Мы добавили два новых элемента. Они начинаются с тегов `<head>` и `<title>` (также обратите внимание, как они оба закрываются).

Элемент `<head>` располагается перед элементом `<body>`. Он содержит информацию о веб-странице. Это и есть заголовок документа HTML. Информация, расположенная в элементе `<head>`, не отображается в окне браузера.

Позднее вы убедитесь, что внутри заголовка документа HTML могут располагаться некоторые другие элементы, и одним из самых важных является элемент `<title>`.

Если вывести в браузер нашу вновь модифицированную веб-страницу, то вы увидите строку "Моя первая веб-страница", появившуюся в верхней части браузера, там, где всегда отображается название файла. Таким образом, текст, помещенный между тегами `<title>` и `</title>`, стал названием веб-страницы. Если добавить эту веб-страницу в "Избранное", то вы заметите, что и здесь используется это же "название" страницы.

## Абзац в веб-документе

Теперь, когда у вас есть базовая структура документа HTML, можно наконец добавить немного контента.

Вернитесь в текстовый редактор и добавьте в код вашей веб-страницы еще одну строку:

```html
<body>
    Это моя первая веб-страницы
    Вот здорово
</body>
```

Посмотрите на получившийся документ в браузере.

Наверное, вы ожидали, что в браузере ваш документ будет отображаться так же, как вы его писали, т.е. на двух строчках. Однако вместо этого вы увидите что-то вроде:

```
Это моя первая веб-страница Вот здорово
```

Это произошло потому, что браузер совершенно не обращает внимание на количество строк, на которых расположен код веб-страницы. Также ему безразлично сколько пробелов вы ввели между словами (вы получите тот же результат, если напишите " Это моя первая веб-страница Вот здорово").

Если вы хотите, чтобы текст отображался на разных строках, вы должны ясно указать это, определив абзац HTML.

Измените две строки вашего контента следующим образом:

```html
<p>Это моя первая веб-страница</p>
<p>Вот здорово</p>
```

Тег `<p>` создает параграф или абзац HTML.

Посмотрите на получившуюся веб-страницу в браузере: теперь две строки текста в браузере отображаются также на двух строках.

Рассматривайте контент HTML документа, как текст книги – с делением на параграфы и абзацы HTML там, где это необходимо.

## Выделение текста

Вы можете внутри абзаца HTML выделять текст при помощи тега `<em>` (акцент) и тега `<strong>` (усиленный акцент). Оба эти тега в принципе делают одно и то же – выделяют текст, хотя традиционно браузеры отображают текст внутри тега `<em>` курсивом, а внутри тега `<strong>` жирным шрифтом.

```html
<p>
    Вот это <em>простой акцент</em>.
    А это <strong>усиленный акцент</strong>.
</p>
```

## Разрыв строки

Для разделения строк также можно использовать тег разрыва строки `<br/>`:

```html
Это моя первая веб-страница<br />
Вот здорово!
```

Тем не менее, данный метод часто приводит к разным злоупотреблениям и в тех случаях, когда один блок текста должен быть отделен от другого, не рекомендуется к использованию (так как если речь идет об абзацах HTML, то лучше использовать элемент `<p>`).

## Шесть уровней текстовых заголовков

Тег `<p>` – это всего лишь один из тегов форматирования текста.

Если у вас есть документы с настоящими заголовками, то следующие теги HTML вам очень пригодятся.

Это теги `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>` и `<h6>`.

Измените код вашей первой веб-страницы следующим образом:

```html
<body>
   <h1>Моя первая веб-страница</h1>
   <h2>Что это такое</h2>
   <p>Простая страница, созданная при помощи HTML</p>
   <h2>Для чего это нужно</h2>
   <p>Чтобы изучить HTML</p>
</body>
```

Обратите внимание, что тег `<h1>` мы использовали всего один раз. Это потому что он считается основным заголовком страницы и не должен использоваться больше одного раза на странице.

Тем не менее, все остальные теги заголовков от `<h2>` до `<h6>` можно использовать столько раз сколько хотите. Однако их всегда следует использовать в соответствующем порядке. Например, `<h4>` должен быть подзаголовком `<h3>`, который в свою очередь должен быть подзаголовком `<h2>`.

## Упорядоченные и неупорядоченные списки

Существует три типа списков: упорядоченные, неупорядоченные и списки определений. Здесь мы рассмотрим первые два вида списков, а о списках определений вы узнаете позже.

Упорядоченные и неупорядоченные списки работают одинаково, за исключением того, что последние используются для представления непоследовательных списков, элементы которых обычно маркируются крупной черной точкой (буллитом), а первые используются для представления последовательных списков, которые обычно имеют вид элементов пронумерованных в возрастающем порядке.

Для определения неупорядоченных списков используется тег `<ul>`, а для определения упорядоченных списков – тег `<ol>`. Внутри списков для определения каждого отдельного элемента списка используется тег `<li>`.

Измените свою веб-страницу следующим образом:

```html
<body>
   <h1>Моя первая веб-страница</h1>
   <h2>Что это такое</h2>
   <p>Простая страница, созданная при помощи HTML</p>
   <h2>Для чего это нужно</h2>
   <ul>
       <li>Чтобы изучить HTML</li>
       <li>Чтобы похвастать</li>
       <li>Потому что я обожаю свой компьютер и хочу привить ему любовь к HTML</li>
   </ul>
</body>
```

Если посмотреть эту веб-страницу в браузере, то увидите список, маркированный буллитами. Замените тег `<ul>` на тег `<ol>`, и вы увидите, что список стал нумерованным.

Кроме всего прочего можно включать одни списки в другие, формируя тем самым структурированную иерархию элементов.

Замените код списка из предыдущего примера следующим:

```html
<ul>
   <li>Чтобы изучить HTML</li>
   <li>Чтобы похвастать
       <ol>
           <li>перед начальником</li>
           <li>перед друзьями</li>
           <li>перед моей кошкой</li>
           <li>перед маленькой говорящей уткой в моей голове</li>
       </ol>
   </li>
   <li>Потому что я обожаю свой компьютер и хочу привить ему любовь к HTML</li>
</ul>
```

## Определение HTML cсылок

До сих пор вы создавали одиночные веб-страницы, которые хороши сами по себе и работают хорошо, но вещь, делающая Интернет таким особенным, это то, что все страницы пересекаются, т.е. ссылаются друг на друга. Ведь буквы "HT" в аббревиатуре "HTML" обозначают слово "гипертекст", что в основе своей означает "текст со ссылками".

Чтобы определить ссылку, используется тег `<a>`, однако этому тегу требуется еще кое-что – направление ссылки, т.е. то, куда будет попадать пользователь при нажатии на ссылку.

Добавьте в свою веб-страницу следующее:

```html
<body>
    <h1>Моя первая веб-страница</h1>
    <h2>Что это такое</h2>
    <p>Простая страница, созданная при помощи HTML</p>
    <h2>Для чего это нужно</h2>
    <p>Чтобы изучить HTML</p>
    <h2>Где найти учебник</h2>
    <p><a href="http://www.msiter.ru">MSITER.RU</a></p>
</body>
```

Направление ссылки задается в атрибуте href тега `<a>`. Ссылка может быть абсолютной, такой как "http://www.msiter.ru", или относительной, указывающей на текущую страницу. Таким образом, если, например, у вас другой файл с именем "flyingmoss.html", то код примет вид `<a href="flyingmoss.html">Чудо летающего мха</a>`.

Ссылка не обязательно должна ссылаться на другой HTML файл. Она может ссылаться на любой файл в сети.

Кроме этого ссылка может отсылать пользователя к другой части той же самой страницы. Для этого нужно добавить атрибут id к любому тегу, например, `<h2 id="moss">Мох</h2>`, а затем создать ссылку на этот тег, например, следующим образом: `<a href="#moss">Перейти к моху</a>`. При нажатии на такую ссылку браузер перелистнет страницу прямо к элементу с данным идентификатором id.

Тег `<a>` позволяет сделать так, чтобы ссылка открывалась в новом окне браузера, а не замещала ту страницу, на которой находится пользователь. Это может показаться разумной мыслью, так как в этом случае пользователь не покидает ваш веб-сайт. Тем не менее, существует множество причин, почему не стоит этого делать. С точки зрения удобства использования подобная практика нарушает линию навигации. Наиболее часто используемым инструментом навигации является кнопка браузера "Назад". При открытии нового окна браузера эта функция становится недоступной. Если же брать еще шире и перейти вообще к проблемам удобства использования, то пользователь вообще относится отрицательно к самовольно открывающимся окнам браузера. Если пользователь захочет открыть ссылку в новом окне, то у него всегда есть возможность сделать это средствами самого браузера.

## Как добавить изображения

Один сплошной текст может казаться довольно скучным и плоским. Но ведь Интернет не только текст. Это мультимедийная сеть, и наиболее распространенная форма медийного представления информации – изображение.

Для того чтобы определить изображение в HTML документе, используется тег `<img>`. И выглядит это следующим образом:

```html
<img 
    src="http://www.msiter.ru/images/logo.gif" 
    width="157" 
    height="70" 
    alt="MSITER.RU" />
```

Атрибут *src* показывает браузеру, где находится изображение. Как и при определении ссылки (о чем рассказывалось ранее) путь может быть абсолютным, как в примере, но обычно используется относительный путь. Например, если вы создадите свое изображение и сохраните его под именем "alienpie.jpg" в директории "images", то тег примет следующий вид: `<img src='images/alienpie.jpg'`

Атрибуты *width* и *height* определяют ширину и высоту изображения в пикселях. Хотя это и необязательные атрибуты, лучше всего их указывать, так как если их опустить, то браузер будет рассчитывать размер изображения по мере его загрузки, что может привести к искажениям внешнего вида веб-страницы. Кроме этого эти атрибуты позволяют манипулировать отображаемыми размерами изображения. Тем не менее, следует помнить, что реальный размер файла изображения в килобайтах останется прежним, и прежним будет время его загрузки.

Атрибут *alt* – альтернативное описание. Оно полезно, если браузеру по той или иной причине не удалось загрузить изображение; при этом в том месте, где должно быть изображение, будет показан текст этого атрибута.

Обратите внимание, что тег `<img>` не имеет закрывающего тега и закрывает сам себя при помощи завершающей конструкции `/>`.

>[Таблицы](https://msiter.ru/tutorials/html-nachalnogo-urovnya/tablitsy) я пропущу, т.к. в современной вёрстке они используются редко и вы сами при необходимости их изучите 

## Span и Div

Все в HTML предназначено для того, чтобы придать контенту некое значение. В то время как большинство HTML тегов в полной мере выполняют это предназначение (тег `<p>` создает параграф, тег `<h1>` – заголовок и т.д.), теги `<span>` и `<div>` никакого значения не имеют, что может вызвать некоторые сомнения в необходимости их существования. Однако эти теги используются чрезвычайно активно совместно с технологией CSS.

Они используются для того, чтобы группировать области HTML кода и затем подключать к этой группе определенные стили CSS. Это осуществляется при помощи атрибутов *class* и *id*, ассоциирующих данные элементы с селекторами класса или идентификатора CSS.

Разница между тегом `<span>` и тегом `<div>` заключается в том, что элемент `<span>` является строчным и обычно используется для группирования небольших областей строчного HTML кода, а элемент `<div>` является блоковым (что, грубо говоря, выражается в наличие перевода строки до и после этого элемента) и используется для группирования более крупных областей кода.

```html
<div id="scissors">
   <p>Это <span class="paper">здорово</span></p>
</div>
```