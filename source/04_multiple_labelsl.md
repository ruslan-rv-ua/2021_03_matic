---
hide:
#  - navigation # Hide navigation
#  - toc        # Hide table of contents
---
# "забагато лейблів до інпута"

Пов'язування декількох `<label>` з одним і тим самим полем форми може призвести до проблем для деяких комбінацій скрінрідерів і браузерів, результати можуть бути різні. 
В деяких випадках буде "прочитано" першу мітку, в інших — останню, ще в інших — усі.

<label for="fail1">Ваше</label>
<label for="fail1">ім'я</label>
<input type="text" id="fail1" />

	:::html
	<label for="fail">Ваше</label>
	<label for="fail">ім'я</label>
	<input type="text" id="fail" />

---
Поєднання `<label>` та `aria-labelledby`:

<span id="your">Ваше</span>
<label for="fail">ім'я</label>
<input type="text" id="fail" aria-labelledby="your" />
	
	:::html
	<span id="your">Ваше</span>
	<label for="fail">ім'я</label>
	<input type="text" id="fail" aria-labelledby="your" />
