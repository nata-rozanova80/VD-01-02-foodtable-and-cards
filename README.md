# VD-01-foodtable
Html-table

VD-02 Карточки персонажей

Чтобы расположить карточки (например, `card1`, `card2`, `card3`) рядом друг с другом на странице, вы можете использовать CSS для настройки их отображения. Вот несколько способов сделать это:

### 1. Flexbox

Flexbox - это современный и удобный способ для выравнивания элементов в строку.

```html
<div class="container">
    <div class="card card1">Card 1</div>
    <div class="card card2">Card 2</div>
    <div class="card card3">Card 3</div>
</div>
```

```css
.container {
    display: flex;
    justify-content: space-between; /* Распределяет карточки по всей ширине контейнера */
}

.card {
    width: 30%; /* Устанавливаем ширину карточек */
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
}
```

### 2. CSS Grid

CSS Grid также предоставляет мощный способ для создания сеток.

```html
<div class="grid-container">
    <div class="card card1">Card 1</div>
    <div class="card card2">Card 2</div>
    <div class="card card3">Card 3</div>
</div>
```

```css
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 колонки равной ширины */
    gap: 20px; /* Отступ между карточками */
}

.card {
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
}
```

### 3. Float

Если вы хотите использовать более старый метод, вы можете использовать `float`, 
но он требует дополнительной очистки.

```html
<div class="container">
    <div class="card card1">Card 1</div>
    <div class="card card2">Card 2</div>
    <div class="card card3">Card 3</div>
</div>
```

```css
.card {
    float: left;
    width: 30%; /* Устанавливаем ширину карточек */
    margin-right: 20px; /* Отступ между карточками */
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
    text-align: center;
}

.container::after {
    content: "";
    display: table;
    clear: both; /* Очистка float */
}
```

Выберите любой из предложенных способов, который вам больше подходит, и адаптируйте его
под свои нужды. Flexbox и Grid являются более современными и рекомендуемыми методами для
размещения элементов на странице.