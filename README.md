# Путешествия по России

Проект третьего спринта о пушешествиях по России.

## Что это?

Одностраничный сайт, адаптирующийся под экран пользователя. При расширении или уменьшении экрана размеры и порядок элементов меняются.

##  Использованные технологии

### Адаптивная верстка

Сайт адаптирован под экраны популярных девайсов, начиная малыми мобильными устройствами и заканчивая большими дэсктопными экранами. 

### Grid-Layout

Две секции проекта созданы на Grid Layout. 
Расположение и размер элементов в сетке адаптируются под экран пользователя.

##### Фото галерея

По мене увеличения экрана количество ячеек на одной строке увеличивается.

На больших экранах:

```css
.photo-grid {
  grid-template-columns: repeat(4, minmax(min-content, max-content));
}
```

На средних экранах:

```css
.photo-grid {
  grid-template-columns: repeat(2, minmax(min-content, max-content));
}
```

#### Карточки

На мобильных экранах все элементы карточек выстраиваются в одну колонну. Для позиционирования элементов используется назнычение им грид-линий.s

### Относительные единицы измерения

Ширина многих элементов задана функцией calc(). Из ширины страницы вычитаются внешние отступы, заставляя ширину элементов адаптироваться под размер экрана:

```css
.lead {
    width: calc(100% - (48px*2));
    max-width: 984px;
  }
```

### :after

Для затемнения секции "cover" при наведении на нее курсора создан псевдо-элемент с отсутсвующим контентом и абсолютным позиционированием.  

```css
.cover__background::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: #2A2C2F;
  opacity: 0.3;
  z-index: -1;
```


## Посмотреть проект

[Нажми меня](https://margof94.github.io/russian-travel/)