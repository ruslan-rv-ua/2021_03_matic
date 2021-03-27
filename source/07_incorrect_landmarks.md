---
hide:
#  - navigation # Hide navigation
#  - toc        # Hide table of contents
---
# "неправильні орієнтири"

- ВЕСЬ контент має міститись всередині лендмарків!
- найбільш "корисні": `header/banner, nav/navigation, main, footer/contentinfo`
- не більше одного `banner, main, contentinfo` на сторінку
- однакові орієнтири повинні мати програмно визначуваний ідентифікатор
- чим менше орієнтрів, тим краще

|HTML5|ARIA Role|підтримка скрінрідерами|
|-|-|-|
|`<header>`|role="banner"|так|
|`<nav>`|role="navigation"|так|
|відсутнє|role="search"|так|
|`<main>`|role="main"|так|
|`<footer>`|role="contentinfo"|так|
|`<aside>`|role="complementary"|так|
|`<section>`|role="region"|частково. Рекомедується з `aria-label` або `aria-labelledby`|
|`<article>`|role="article"|частково (JAWS)|
|`<form>`|role="form"|частково (лише якщо є `role="form"`)|


## Приклади

Добре — кожен `nav` на цій сторінці можна ідентифікувати:

	:::html
	<nav class="md-nav md-nav--primary" aria-label="Navigation" data-md-level="0">
	...
	</nav>
    ... 
	<nav class="md-nav md-nav--secondary" aria-label="Зміст">
	...
	</nav>
	
	
---
Погано — два футера, дві основні частини на цій сторінці:

<h1>Це заголовок дуже цікавої статті</h1>
<main class="article">
  <p>Текст дуже змістовної і цікавої статті. [...]</p>
  <div role="contentinfo">
	<p>[...інформація про статтю у футері...]</p>
  </div>
</main>


	:::html
	<h1>Це заголовок дуже цікавої статті</h1>
	<main class="article">
	  <p>Текст дуже змістовної і цікавої статті. [...]</p>
	  <div role="contentinfo">
		<p>[...інформація про статтю у футері...]</p>
	  </div>
	<div role="contentinfo">
	  <p>А тут футер для всієї сторінки</p>
	</div>
	</main>
	...
	<footer class="md-footer">
	...
	</footer>
