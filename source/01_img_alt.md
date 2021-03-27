---
hide:
#  - navigation # Hide navigation
 - toc        # Hide table of contents
---
# "відсутність альт тексту"

Альтернативний текст:

- детектується програмно
- описує зображене
- не те саме що і підпис
- короткий
- не містить "зображення", "графіка", ...

Як:

- `aria-labelledby`
- `aria-label`
- `alt`
- `title` (неоднозначно)

## Приховуємо декоративні зображення

- `alt=""`
- `role="presentation"`
- CSS backgrounds

## Приклади

Добре — декоративне зображення детектується як таке:

<img alt="" src="https://dummyimage.com/200x200/777777/ffffff&text=image">

    :::HTML
    <img alt="" src="https://dummyimage.com/200x200/777777/ffffff&text=image">
	

---
Погано — декоративне зображення, неоднзначна ситуація:

<img src="https://dummyimage.com/200x200/777777/ffffff&text=image">

    :::HTML
    <img src="https://dummyimage.com/200x200/777777/ffffff&text=image">


---
Погано — опис зображення дублює текст посилання:

<a href="http://google.com">
    <img alt="Гугл" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">
    Гугл
</a>

    :::html
    <a href="http://google.com">
        <img alt="Гугл" src="...">
        Гугл
    </a>

---
Добре — зрозумілий текст посилання:

<a href="http://google.com">
    <img alt="Пошукова система Гугл" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">
</a>

    :::html
    <a href="http://google.com">
        <img alt="Пошукова система Гугл" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">
    </a>

---
Погано — занадто довгий текст, "зайва" інформація:

    :::html
    <a href="http://google.com">
        <img alt="Клацніть тут щоб перейти до Пошукова система Гугл" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png">
    </a>

---
Погано — зображення як контрол без текстового контента:

<input type="image" src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png" name="submit">

	:::html
	<input type="image" src="submit.png" name="submit">