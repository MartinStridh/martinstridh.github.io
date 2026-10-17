
<!-- Enkel och stabil hamburgerknapp för mobilen -->
<button class="custom-menu-btn" onclick="document.getElementById('my-mobile-menu').classList.toggle('drawer-open')">☰ Menu</button>

<!-- En stabil mobilrubrik som ALDRIG kan flytta på sig -->
<div class="custom-mobile-title">
  <h1>Min Hemsida</h1>
</div>

<!-- En dedikerad mobilsidomeny (Kopiera dina menylänkar hit inuti <ul>) -->
<div id="my-mobile-menu" class="custom-mobile-drawer">
  <h3>Navigering</h3>
  <ul>
    <li><a href="/">Hem</a></li>
    <li><a href="/om">Om</a></li>
    <!-- Lägg till dina egna menylänkar här -->
  </ul>
</div>

---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

An open research community dedicated to developing and applying the Lund ECG Parser software in ECG-related research.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```

<!-- Vi skapar ett dolt element som hjälper skriptet att hitta din sidomeny -->
<span id="sidebar-marker" style="display:none;"></span>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    var wrapper = document.querySelector(".wrapper");
    if (!wrapper) return;

    var realSidebar = null;

    // 1. Skanna av ALLA headers/asides på sidan
    var elements = document.querySelectorAll("header, aside");
    for (var i = 0; i < elements.length; i++) {
      var el = elements[i];
      
      // En artikelrubrik ligger ALLTID inuti en <section>. Om den gör det, hoppa över!
      if (el.closest("section")) continue;

      // Temats äkta meny innehåller alltid ord som "github", "view" eller "download"
      var content = el.innerHTML.toLowerCase();
      if (content.includes("github") || content.includes("download") || content.includes("project")) {
        realSidebar = el;
        break;
      }
    }

    // 2. Om vi hittade den äkta menyn, starta hamburger-logiken
    if (realSidebar) {
      realSidebar.setAttribute("id", "my-true-mobile-sidebar");

      // Skapa hamburgerknappen
      var menuBtn = document.createElement("button");
      menuBtn.className = "custom-menu-btn";
      menuBtn.innerHTML = "☰ Menu";
      document.body.appendChild(menuBtn);

      // Klickfunktion för att öppna/stänga
      menuBtn.addEventListener("click", function(e) {
        e.stopPropagation();
        realSidebar.classList.toggle("mobile-drawer-open");
      });

      // Stäng menyn vid klick utanför
      document.addEventListener("click", function(e) {
        if (realSidebar.classList.contains("mobile-drawer-open")) {
          if (!realSidebar.contains(e.target) && e.target !== menuBtn) {
            realSidebar.classList.remove("mobile-drawer-open");
          }
        }
      });
    }
  });
</script>

