# тема 1. Youtube Канал

## HTML

Начинаем с тега `section`, объясняем, что он нужен для создания разделов на сайте(блоков/секций и тд) 
```HTML
<section></section>
```

Добавляем `img`, картинку лучше искать прямоугольной формы
```HTML
<section>
  <img src="">
</section>
```

Название канала `h1`, можно объяснить разницу между `h1-h6`
```HTML
<section>
  <img src="">
  <h1>CATS LOADING</h1>
</section>
```

Два тега `p` для информации о канале
```HTML
<section>
  <img src="">
  <h1>Название канала</h1>
  <p>@CatsLoading &bull; 25,8 тыс. подписчиков &bull; 18 видео</p>
  <p>funny cat videos every saturday :)</p>
</section>
```

Кнопку "подписаться" `button`
```HTML
<section>
  <img src="">
  <h1>Название канала</h1>
  <p>@CatsLoading &bull; 25,8 тыс. подписчиков &bull; 18 видео</p>
  <p>funny cat videos every saturday :)</p>
  <button>Подписаться</button>
</section>
```


## CSS

Если чувствуете, что ребята успевают, можно начать с ресета отступов(объяснить про стандартные отсупы брааузера), либо пропустите. Разницу между внешними и внутренними отступами оставим на потом. А про звёздочку объясняем, что она позволяет обратиться ко всем элементам на сайте. Разницу ребята сразу увидят, так как все отступы пропадут.
```CSS
* {
  margin: 0;
  padding: 0;
}
```

Дальше можно действовать в свободном формате и спрашивать ребят, что они хотят поменять на сайте. Так как мы делаем 1в1, то лишнего они не скажут, поэтому можно делать в любом порядке все нижеперечисленные свойства и объяснять их значения.
Я начну с цвета фона, можно делать любой, но для повторения ютуба могут написать такой же код цвета. И скорее всего, сразу заметят, что надо поменять цвет текста на белый.
(Так же часто обращают внимания на шрифт, можно его тоже изменить)
```CSS
body {
  background-color: #0f0f0f;
  color: white;
  font-family: "Roboto","Arial",sans-serif;
}
```

Сделаем наш `section` по центру. Ширину ставими меньше, если экран ученика маленький. Примерно пикселей 800 универсальное значение. Этот пункт можно пропустить, если ребята медленно работают. Так как тут надо объяснить про отступы. Лучше всего отступы отложить на конец урока и добавить все за раз.
```CSS
section {
  width: 1400px;
  margin: 0 auto;
}
```

Дальше уменьшим и слегка закруглим края картинки.
```CSS
img {
    width: 100%;
    border-radius: 20px;
}
```

Увеличим размер заголовка
```CSS
h1 {
    font-size: 36px;
}
```

Поменяем цвет описания
```CSS
p {
    color: #aaaaa4;
}
```

Осталось стилизовать `button`. Тут можно объяснить про внутренние отступы, жирность текста и курсор. Всё остальное уже знаем.
```CSS
button {
    background-color: white;
    color: black;
    border-radius: 20px;
    padding: 10px 15px;
    font-size: 15px;
    font-weight: bold;
    border: none;
    cursor: pointer;
}

```

Сделаем подсветку кнопки при наведении, объясняем про псевдокласс `:hover`
```CSS
button:hover {
    background-color: #d9d9d9;
}
```

## Дополнительно: Фиксим положение

Немного объясняем принцип работы `display:flex` и дефолтного позиционирования в HTML. Делаем следующее:
```HTML
 <section>

        <div>
            <img src="https://yt3.googleusercontent.com/MFqu2XKraDas32RhQmYqmuv0jQmjyiueV2-sYJ4lTR1SRRdHpIuY-vvEqU5Sx1CNGTB_PRfPKb4=s160-c-k-c0x00ffffff-no-rj">
            <span>
                <h1>CATS LOADING</h1>
                <p>@CatsLoading &bull; 25,8 тыс. подписчиков &bull; 18 видео</p>
                <p>funny cat videos every saturday :)</p>
                <button>Подписаться</button>
            </span>
        </div>
        
    </section>
```
Делаем `div` и `span`, если понимаете, что до классов дойти не успеваем. Иначе можно сделать два тега `div` с класами.
И применяем flex
```CSS
div {
    display: flex;
}
```

## Дополнительно: добавляем аватарку канала
 
Если не знакомились с классами - их не делаем.
```HTML
 <section>
        <img src="https://yt3.googleusercontent.com/P1LWScF6lRalekSJQtw_WG7Icg7R5kokKig-syVzth_oVYHcI4SCjYfdmhc0iyx6FTWaq7Rh8A=w1707-fcrop64=1,00005a57ffffa5a8-k-c0xffffffff-no-nd-rj" class="banner__img">

        <div>
        <img src="https://yt3.googleusercontent.com/MFqu2XKraDas32RhQmYqmuv0jQmjyiueV2-sYJ4lTR1SRRdHpIuY-vvEqU5Sx1CNGTB_PRfPKb4=s160-c-k-c0x00ffffff-no-rj" class="channel__img">
        <span>  
            <h1>CATS LOADING</h1>
            <p>@CatsLoading &bull; 25,8 тыс. подписчиков &bull; 18 видео</p>
            <p>funny cat videos every saturday :)</p>
            <button>Подписаться</button>
        </span>
    </div>
    </section>
```

Задаем размеры для аватарки. Если делали классы, то через них.
```CSS
div img { 
    border-radius: 100%;
    width: 160px;
    height: 160px;
}
```

## Дополнительно: отступы

Рассказываем принцип работы отступов. Сначала практикуемся устно в выборе направлений и тд. Затем делаем в коде поправки.
```CSS
img {
  margin-bottom: 15px;
}

div img {
  margin-right: 15px;
}

h1 {
    margin-bottom: 10px;
}

p {
    margin-bottom: 10px;
}
```
