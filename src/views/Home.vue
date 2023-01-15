<script setup>

  import * as contentful from 'contentful'
  import { documentToHtmlString } from '@contentful/rich-text-html-renderer'

  const client = contentful.createClient({
    space: "6iikf86hdaof",
    accessToken: "2LQnxlORVCt2TCU-jOVNq8KSPGNQzZTFWBfT3dxFets",
  })

  client
    .getEntry("7JOjQLs9XhN1HA1XUUJVWz")
    .then((entry) => {
      // console.log({ entry })
      const rawRichTextField = entry.fields.title
      return documentToHtmlString(rawRichTextField)
    })
    .then((renderedHtml) => {
      // console.log(renderedHtml)
      document.getElementsByTagName('h1')[0].innerHTML = renderedHtml
    })
    .catch(err => console.log(err))

</script>

<template>

  <header class="header">
    <img src="https://basho-color.fueko.net/content/images/2022/01/basho.svg">
  </header>

  <main class="main">
    <h1>
      <!-- <b>Pame Digital.</b>
      Consejos de Inversión, Marketing y Desarrollo Personal. -->
    </h1>

    <div class="action">
      <input class="input" placeholder="Escríbe a whatsapp">
      <button class="button">Contáctame</button>
    </div>

  </main>

  <section>
  </section>

  <footer>
  </footer>

</template>
