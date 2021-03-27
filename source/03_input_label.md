---
hide:
#  - navigation # Hide navigation
#  - toc        # Hide table of contents
---
# "відсутність лейби до інпута"

Мітки:

- ясно і чітко визначають призначення контрола
- зв'язані з контролом
- видимі у будь-який час
- близько розташовані до відповідного контрола

Як:

- `aria-labelledby` — неклікабельно
- `aria-label` — взагалі невидимий
- `<label>` — найкраще
- `title` — невидимий, не рекомендується
- `placeholder` — як додатковий метод

## Приклади

Добре — найкращий спосіб:

<p>
  <label for="fname_a">First Name:</label> 
  <input type="text" name="fname_a" id="fname_a">
</p>
<p>
  <label for="lname_a">Last Name:</label>
  <input type="text" name="lname_a" id="lname_a">
</p>

	:::html
	<p>
	  <label for="fname_a">First Name:</label> 
	  <input type="text" name="fname_a" id="fname_a">
	</p>
	<p>
	  <label for="lname_a">Last Name:</label>
	  <input type="text" name="lname_a" id="lname_a">
	</p>
	
	
---
Добре — aria-labelledby:

<p>
	<span id="Nickname">Nickname:</span>
	<input type="text" aria-labelledby="Nickname">
</p>

	:::html
	<p>
		<span id="Nickname">Nickname:</span>
		<input type="text" aria-labelledby="Nickname">
	</p>
	
---
Погано — зображення без альтернативного текста як мітка:

<p>
  <label for="fa-search-no-alt">
    <img src="label-search.png">
  </label>
  <input type="text" id="fa-search-no-alt">
</p>

	:::html
	<p>
	  <label for="fa-search-no-alt">
		<img src="label-search.png">
	  </label>
	  <input type="text" id="fa-search-no-alt">
	</p>