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

<script>
  document.addEventListener("DOMContentLoaded", function() {
    // 1. Skapa en stabil HTML-knapp dynamiskt
    var menuBtn = document.createElement("button");
    menuBtn.className = "custom-menu-btn";
    menuBtn.innerHTML = "☰ Menu";
    document.body.appendChild(menuBtn);

    // 2. Hitta rätt sidomeny (viktigt för Modernist-temat)
    var sidebar = document.querySelector("body > header") || 
                  document.querySelector(".wrapper > header") || 
                  document.querySelector("body > aside") || 
                  document.querySelector(".wrapper > aside");

    // 3. Hantera klick på knappen
    menuBtn.addEventListener("click", function(e) {
      e.stopPropagation();
      if (sidebar) {
        sidebar.classList.toggle("mobile-open");
      }
    });

    // 4. Stäng menyn om man klickar utanför den ute på sidan
    document.addEventListener("click", function(e) {
      if (sidebar && sidebar.classList.contains("mobile-open")) {
        if (!sidebar.contains(e.target) && e.target !== menuBtn) {
          sidebar.classList.remove("mobile-open");
        }
      }
    });
  });
</script>
