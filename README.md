# yandex-test-ex1
##Тестовое задание №1. Список с ачивками.

[Репозиторий с проектом] (https://github.com/dyadyaJora/yandex-test-ex1.git) .

[Страничка GHPages] (https://dyadyajora.github.io/yandex-test-ex1/index.html) .
###Описание
Макет с шаблоном для списка ачивок. На странице автоматически сгенерировано 100 случайных ачивок для демонстрации.

HTML-код блока ачивки выглядит так:
```html
<div class="block">
<div class="main">
	<div class="achive">
		<img src="" alt="">
	</div>
	<div class="img-block">
		
	<div class="img"></div>
	</div>
	<div class="number">
		<div class="number-2">
		</div>
	</div>
	</div>
</div>
```
###Изменение внешнего вида
Изменять внешний вид ачивки можно с помощью добавления классов к родительскому блоку "block"
```html
<div class="block class1 classs2 ...">
...
</div>
```

Также внешний вид можно менять добавлением классов к DOM-элементам
```javascript
var div = document.getElementById('wrapper');
var elems = div.getElementsByTagName('*');
var i=1; //где i - номер изменяемой ачивки
elems[8*(i-1)].classList.add("class-img"); //а 8, потому что блок каждой ачивки содержит по 8 дочерних элементов, а каждый восьмой и есть "block"
```


###Добавление новых классов
Добавлять свои классы можно в файле css/screen.scss
Для изменения картинки класс должен быть следующего вида:
```scss
 .название_класса{
	.img{
		background: url("../путь_к_изображению/..");
		background-size:contain;
	}
}
```
Для изменения цветового оформления класс должен быть таким:
```scss
.название_класса{
	.achive{
		border-color: цвет;
	}
	.number{
		background:nth($colors, $i);
		.number-2:before{
			color: nth($colors, $i);
		}
	}
}
```

