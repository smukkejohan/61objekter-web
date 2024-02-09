<script>
    import "../app.css";
    const year = new Date().getFullYear();
</script>

<div class="container mx-auto">
    <header class="mt-4">    
      <h1 class="text-6xl">61 Objekter</h1>
      <p class="text-2xl mt-4">Workshop collective in Copenhagen</p>

</header>
<main class="mt-4">
  <slot />
</main>

<footer>

    <address>
      Prags Boulevard 61<br>
      2300 København S<br>
      Denmark
    </address>

  <p>© {year} 61 Objekter</p>
</footer>
</div>
