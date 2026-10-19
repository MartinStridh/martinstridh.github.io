e ---
layout: default
---
An open research community dedicated to developing and applying the Lund ECG Parser software in ECG-related research.

# Welcome to the Lund ECG Parser Research Community homepage
This is an open research community dedicated to developing and applying the Lund ECG Parser software (formerly commercialized under the names Cardiolund ECG Parser and Cardiolund AFR Tracker) in ECG-related research.

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

<!-- Den globala hamburgerknappen för alla skärmar -->
<button class="fixed-hamburger-btn" id="triggerMobileMenu">☰ Menu</button>

<!-- Den fristående sidopanelen med alla dina 8 unika länkar -->
<div id="clean-mobile-drawer" class="custom-mobile-drawer">
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/use-lund-ecg-parser">Use Lund ECG Parser</a></li>
    <li><a href="/community-purpose">Community purpose</a></li>
    <li><a href="/join-the-community">Join the community</a></li>
    <li><a href="/lund-ecg-parser">Lund ECG Parser</a></li>
    <li><a href="/lund-afr-tracker">Lund AFR Tracker</a></li>
    <li><a href="/documentation">Documentation</a></li>
    <li><a href="/publications">Publications</a></li>
  </ul>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    var btn = document.getElementById("triggerMobileMenu");
    var drawer = document.getElementById("clean-mobile-drawer");

    if (btn && drawer) {
      // Öppna och stäng stabilt vid tryck/klick
      btn.addEventListener("click", function(e) {
        e.stopPropagation();
        drawer.classList.toggle("drawer-is-open");
      });

      // Stäng menyn om man klickar på texten utanför sidopanelen
      document.addEventListener("click", function(e) {
        if (drawer.classList.contains("drawer-is-open")) {
          if (!drawer.contains(e.target) && e.target !== btn) {
            drawer.classList.remove("drawer-is-open");
          }
        }
      });
    }
  });
</script>
