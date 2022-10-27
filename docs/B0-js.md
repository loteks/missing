---
title: JS
url: ./js/
---

# Missing.js

Missing.js is a JavaScript library implementing common UI patterns.


## Tabs

_See [ARIA &sect; Tabs](/docs/aria/#tabs)_

Add `tabs.js` **as a module script** to your page
and mark up your tabs with the appropriate ARIA roles.
Behavior will be added automatically.

~~~
<script type="module" src="https://the.missing.style/tabs.js">
~~~

<div class="info box">

### Initializing dynamic content {.titlebar}

For dynamically inserted content: initialize it as such:

<figure class="plain">

~~~ js
import tabs from "https://the.missing.style/tabs.js";
// ... insert some content ...
tabs(theContentIJustInserted);
~~~

<figcaption>Initializing a missing.js behavior on newly inserted content</figcaption>

</figure>

Any elements that are inside a shadow DOM will also need to be initialized explicitly this way.

All of our components will find elements that need initialization within the subtree you pass in ---
you could pass the whole `document` every time if you wanted to.

</div>

## Menu

_See [ARIA &sect; Tabs](/docs/aria/#tabs)_

~~~ html
<script type="module" src="https://the.missing.style/tabs.js">
~~~

All notes above about initializing dynamic content apply here.


## Expand/collapse navbar

_See [Components &sect; Navbar](/docs/components/#navbar)_

~~~ html
<script type="module" src="https://the.missing.style/overflow-nav.js">
~~~

Make sure to add:

 - the `data-overflow-nav` attribute to your navbar.
 - inside that navbar, a button with a `data-nav-expander` attribute.

<figure>

~~~ html
<header class="navbar" data-overflow-nav>
    <button class="iconbutton" data-nav-expander aria-hidden>
        &#x2630; <!-- trigram for heaven -->
    </button>
    <!-- rest of navbar... -->
</header>
~~~

</figure>

The navbar will remain horizontally scrollable.

All notes above about initializing dynamic content apply here
(for all those times you dynamically add navbars to your page).