---
hide:
#  - navigation # Hide navigation
#  - toc        # Hide table of contents
---
# "базово про ролі - неправльна роль"

## Семантика — понад усе!

Семантику можна змінити за допомогою `role`.  
Допустимі значення:

- Орієнтири: article, banner, complementary, main, navigation, region, search, contentinfo
- Віджети: alert, alertdialog, application, dialog, group, log, marquee, menu, menubar, menuitem, menuitemcheckbox, menuitemradio, progressbar, separator, slider, spinbutton, status, tab, tablist, tabpanel, timer, toolbar, tooltip, tree, treegrid, treeitem
- "Псевдо-HTML": button, button, checkbox, columnheader, combobox, contentinfo, form, grid, gridcell, heading, img, link, listbox, listitem, option, radio, radiogroup, row, rowgroup, rowheader, scrollbar, textbox
- Документ: document (коли необхідно включити документ в область іншого типу)
- Застосунок: application (область де діє "звичайна" реакція на клавіші)
- Представлення: presentation (відміна "нативної" ролі елемента)
- Інші семантичні значення: math, definition, note, directory
- Абстрактні семантичні значення: command, composite, input, landmark, range, section, sectionhead, select, structure, widget

## Приклади

Погано — перевизначення семантики:

<ul role="navigation">
	<li>Головна</li>
	<li>Послуги</li>
</ul>

	:::html
	<ul role="navigation">
		<li>Головна</li>
		<li>Послуги</li>
	</ul>
	
---
Добре — семантика не змінюється:

<div role="navigation">
	<ul>
		<li>Головна</li>
		<li>Послуги</li>
	</ul>
</div>

	:::html
	<div role="navigation">
		<ul>
			<li>Головна</li>
			<li>Послуги</li>
		</ul>
	</div>

---
Погано — конфлікт нативної семантики елемента та присвоєної ролі:

<ul role="table">
	<li>комірка 1</li>
	<li>комірка 2</li>
</ul>

	:::html
	<ul role="table">
		<li>елемент списка 1</li>
		<li>елемент списка 2</li>
	</ul>

---
Погано — неправильне семантичне значення елемента:

<a href="#" class="md-button md-button--primary">Додати товар у кошик</a>

	:::html
	<a href="#" class="md-button">Додати товар у кошик</a>

Добре — присвоєння "правильного" семантичного значення елементу:

<a role="button" href="#" class="md-button md-button--primary">Додати товар у кошик</a>

	:::html
	<a role="button" href="#" class="md-button">Додати товар у кошик</a>
	
	
---
Використання `tablist`, `presentation`:

<ul role="tablist">
  <li role="presentation">
    <a role="tab" href="#">Tab 1</a>
  </li>
  <li role="presentation">
    <a role="tab" href="#">Tab 2</a>
  </li>
  <li role="presentation">
    <a role="tab" href="#">Tab 3</a>
  </li>
</ul>

	:::html
	<ul role="tablist">
	  <li role="presentation">
		<a role="tab" href="#">Tab 1</a>
	  </li>
	  <li role="presentation">
		<a role="tab" href="#">Tab 2</a>
	  </li>
	  <li role="presentation">
		<a role="tab" href="#">Tab 3</a>
	  </li>
	</ul>
	
