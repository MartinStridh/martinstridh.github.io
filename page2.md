## Lund ECG Parser explained
The Lund ECG Parser Research 


<!-- Den globala hamburgerknappen för alla skärmar -->
<button class="fixed-hamburger-btn" id="triggerMobileMenu">☰ Menu</button>

<!-- Den fristående sidopanelen med alla dina 8 unika länkar -->
<div id="clean-mobile-drawer" class="custom-mobile-drawer">
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/page1.html">Join the community</a></li>
    <li><a href="/page2.html">Lund ECG Parser explained</a></li>
    <li><a href="/page2.html">Lund AFR Tracker explained</a></li>
    <li><a href="/page2.html">Package description</a></li>
    <li><a href="/page2.html">Downloads</a></li>
    <li><a href="/page2.html">Documentation</a></li>
    <li><a href="/page2.html">Publications</a></li>
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
