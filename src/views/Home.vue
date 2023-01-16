<script setup>
  import { ref, onMounted } from 'vue'

  import * as contentful from 'contentful'
  import { documentToHtmlString } from '@contentful/rich-text-html-renderer'

  const client = contentful.createClient({
    space: "6iikf86hdaof",
    accessToken: "2LQnxlORVCt2TCU-jOVNq8KSPGNQzZTFWBfT3dxFets",
  })

  const text = ref('')

  client
    .getEntry("7JOjQLs9XhN1HA1XUUJVWz")
    .then((entry) => {
      const rawRichTextField = entry.fields.title
      return documentToHtmlString(rawRichTextField)
    })
    .then((renderedHtml) => {
      text.value = renderedHtml
    })
    .catch(err => console.log(err))


  const phone = '51936320564'
  const msg_0 = 'Hola Pame Digital'
  let   msg   = ref('')


  const click = () => {

    console.log('click ', msg.value)

    if(!msg.value) msg.value = msg_0

    const code = encodeURIComponent(msg.value)
    console.log(code)

    const url = `https://wa.me/${phone}?text=${code}`

    window.open(url)
  }

</script>

<template>

  <header class="header">
    <img src="@/assets/img/logo.svg">
  </header>

  <main class="main">
    <h1 v-html="text"></h1>

    <div class="action">
      <input class="input" v-model="msg" placeholder="Escríbe a whatsapp">
      <button class="button" @click="click">Contáctame</button>
    </div>

  </main>

  <section>
  </section>

  <footer>
  </footer>

</template>
