## Join the Community!



<!-- Den globala hamburgerknappen för alla skärmar -->
<button class="fixed-hamburger-btn" id="triggerMobileMenu">☰ Menu</button>

<!-- Den fristående sidopanelen med alla dina 8 unika länkar -->
<div id="clean-mobile-drawer" class="custom-mobile-drawer">
  <ul>
    <li><a href="/">Home</a></li>
    <li><a href="/join-community">Join the community</a></li>
    <li><a href="/ECG-explained">Lund ECG Parser explained</a></li>
    <li><a href="/AFR-explained">Lund AFR Tracker explained</a></li>
    <li><a href="/package-description">Package description</a></li>
    <li><a href="/downloads">Downloads</a></li>
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
