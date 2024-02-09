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

<footer class="mt-6">
    <h2 class="text-xl">Contact</h2>
<p>For inquiries, please contact <a href="mailto:public@johan.cc">public@johan.cc</a></p>

<div class="flex">

<div class="mt-4">
  <h2 class="text-xl">Find us at</h2>
<address>
  Prags Boulevard 61<br>
  2300 København S<br>
  Denmark
</address>
</div>

</div>

  <p class="mt-6">© {year} 61 Objekter</p>
</footer>
</div>
