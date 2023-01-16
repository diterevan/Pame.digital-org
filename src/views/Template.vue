<script setup>
  import Article from '../components/Article.vue'
</script>

<template>

  <header class="header">
    <img src="https://basho-color.fueko.net/content/images/2022/01/basho.svg">
  </header>

  <main class="main">
    <h1>
      <b>This is Basho.</b>
      A digital magazine that promises to deliver inspiring stories from all disciplines.
    </h1>

    <div class="action">
      <input class="input" placeholder="Your email address">
      <button class="button">Subscribe</button>
    </div>
  </main>

  <section>
    <h2>
      See what we’ve <br>
      <b>written lately</b>
    </h2>

    <div class="articles">
      <Article />
      <Article />
      <Article />
      <Article />
      <Article />
      <Article />
    </div>

  </section> <br>

  <footer class="footer">
    <header>
      <h3 class="flat">Subscribe to <b>new posts</b></h3>

      <form>
        <input placeholder="Your email address">
        <button>Subscribe</button>
      </form>
    </header>
    <main>
      <img src="https://basho-color.fueko.net/content/images/2022/01/basho.svg">

      <p>A minimal, functional theme for running a paid-membership publication on Ghost.</p>
    </main>
  </footer>

  <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
  <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
  <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
  <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
  <br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
</template>