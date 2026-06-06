# cssMemeSlider
css Meme Slider

A responsive CSS-only meme slider created for the RS School Bootcamp task.

## Task

https://github.com/rolling-scopes-school/tasks/blob/master/stage0.5%20Bootcamp/tasks/css-meme-slider/README.md

## Features

- Pure HTML and CSS implementation
- No JavaScript
- Responsive desktop and mobile layout
- Smooth image transitions
- Smooth text transitions
- Custom slider controls
- Hover and active states for controls

## Tested resolutions

- Desktop: 1024px and above
- Mobile: 500px

## Project structure

```text
cssMemeSlider/
  index.html
  style.css
  assets/
    meme-1.jpg
    meme-2.jpg
    meme-3.jpg
    meme-4.jpg
```    

## Description 

Hi, this is my CSS Meme Slider project for the first week RS School Bootcamp task.

I am showing the project in VS Code and the result in the browser. The project is built with plain HTML and CSS only. There is no JavaScript, no npm packages, no CSS framework, and no CSS preprocessor.

First, I will temporarily disable the stylesheet link in the HTML. Now, in the browser, we can see the raw HTML structure: radio inputs, images, text captions, and labels for controls. So the content exists as normal document flow, and the slider behaviour is not coming from JavaScript.

Now I enable the CSS again. The layout turns into a centered responsive slider. The main image area uses an overflow-hidden container. Inside it, all slides are placed in one horizontal flex track. Each slide takes 100 percent of the visible slider width.

The slider state is stored in radio inputs. All radio inputs have the same name, so only one of them can be checked at the same time. The labels are connected to the inputs through the for attribute. When I click a control, the browser checks the related radio input.

CSS reads that state through the checked pseudo-class. For example, when slide two is checked, the CSS selector targets the image track and moves it with transform translateX minus 100 percent. That means the whole track moves left by exactly one slide. Slide three uses minus 200 percent, and slide four uses minus 300 percent.

I use transform instead of left or position because the task requires normal document flow and does not allow position, top, left, right, or bottom. Transform is also better for animation because it does not trigger layout recalculation in the same way and usually gives smoother movement.

The image movement is animated with transition. Transition is perfect here because the element moves smoothly from one state to another. Keyframes are better for multi-step animations, but this slider only needs state-based transitions between slides.

The captions are not part of the images. They are real text paragraphs in a separate caption track. The caption track is moved with the same translateX logic, so the text changes smoothly together with the image.

The controls also meet the interaction requirements. The visible dot is smaller than the full clickable label area, so the user has a larger click target. There are hover styles, active styles, an active slide indicator, and cursor pointer.

For layout, I use Flexbox for the slide track and controls, and Grid for the footer area with the caption and controls. On desktop, the caption and controls sit in one row. On mobile, a media query changes the layout so they stack neatly.

The project uses relative units like rem, percent, viewport units, and fr. Pixels are used only in the media query breakpoint. I also avoided float and pseudo-elements. I use pseudo-classes like checked, hover, and active, but not pseudo-elements like before or after.

Finally, the repository follows the required workflow: the work is inside the cssMemeSlider folder on the gh-pages branch, there are at least five commits, the commit messages follow the convention and include timestamps, and the Pull Request description includes the tested desktop and mobile resolutions.

## Описание 

Привет, это мой проект CSS-слайдера с мемами для задания первой недели буткемпа RS School.

Я показываю проект в VS Code, а результат — в браузере. Проект создан только с использованием чистого HTML и CSS. Здесь нет JavaScript, пакетов npm, CSS-фреймворков и препроцессоров CSS.

Сначала я временно отключу ссылку на таблицу стилей в HTML. Теперь в браузере мы видим исходную структуру HTML: радиокнопки, изображения, текстовые подписи и метки для элементов управления. Таким образом, контент существует как обычный поток документа, и поведение слайдера не зависит от JavaScript.

Теперь я снова включаю CSS. Макет превращается в центрированный адаптивный слайдер. Основная область изображения использует контейнер с атрибутом overflow-hidden. Внутри него все слайды размещены в одной горизонтальной дорожке flex. Каждый слайд занимает 100 процентов видимой ширины слайдера.

Состояние слайдера хранится в радиокнопках. Все радиокнопки имеют одно и то же имя, поэтому одновременно может быть выбран только один из них. Метки связаны с полями ввода через атрибут `for`. При щелчке по элементу управления браузер проверяет соответствующее поле ввода радиокнопки.

CSS считывает это состояние через псевдокласс `checked`. Например, когда выбран второй слайд, селектор CSS нацеливается на дорожку изображения и перемещает её с помощью `transform translateX минус 100 процентов`. Это означает, что вся дорожка перемещается влево ровно на один слайд. Для третьего слайда используется `-200 процентов`, а для четвёртого — `-300 процентов`.

Я использую `transform` вместо `left` или `position`, потому что задача требует обычного потока документа и не допускает `position`, `top`, `left`, `right` или `bottom`. `transform` также лучше подходит для анимации, поскольку он не вызывает перерасчёт макета таким же образом и обычно обеспечивает более плавное движение.

Движение изображения анимируется с помощью `transition`. `transition` здесь идеально подходит, потому что элемент плавно переходит из одного состояния в другое. Ключевые кадры лучше подходят для многошаговой анимации, но этому слайдеру нужны только переходы между слайдами на основе состояний.

Подписи не являются частью изображений. Это реальные текстовые абзацы в отдельной дорожке для подписей. Дорожка для подписей перемещается с использованием той же логики translateX, поэтому текст плавно изменяется вместе с изображением.

Элементы управления также соответствуют требованиям к взаимодействию. Видимая точка меньше, чем вся область кликабельной метки, поэтому у пользователя больше область для клика. Есть стили при наведении курсора, стили активности, индикатор активного слайда и указатель курсора.

Для компоновки я использую Flexbox для дорожки слайда и элементов управления, и Grid для области нижнего колонтитула с подписью и элементами управления. На настольных компьютерах подпись и элементы управления располагаются в один ряд. На мобильных устройствах медиазапрос изменяет компоновку, чтобы они аккуратно располагались друг над другом.

В проекте используются относительные единицы измерения, такие как rem, проценты, единицы области просмотра и fr. Пиксели используются только в контрольной точке медиазапроса. Я также избегал использования float и псевдоэлементов. Я использую псевдоклассы, такие как checked, hover и active, но не псевдоэлементы, такие как before или after.

Наконец, репозиторий соответствует требуемому рабочему процессу: работа находится в папке cssMemeSlider в ветке gh-pages, имеется не менее пяти коммитов, сообщения коммитов соответствуют соглашениям и включают метки времени, а описание запроса на слияние (Pull Request) содержит информацию о протестированных разрешениях для настольных компьютеров и мобильных устройств.