<template>
  <section class="container">
    <div>
      <app-logo/>
      <h1 class="title">
        ssr-blog
      </h1>
      <h2 class="subtitle">
        Nuxt.js project
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green">Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey">GitHub</a>
      </div>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  },
  head() {
    const vm = this
    const title = 'title Estrenos cine hoy'
    const keyword =
      'Estrenos cine hoy, peliculas, series, actores, actrices, TV Shows, movies, actor, actress, movies rating, news, tv networks'
    return {
      title: title,
      description: keyword,
      meta: [
        {
          charset: 'utf-8'
        },
        {
          hid: 'title',
          name: 'title',
          content: title
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content: keyword
        },
        {
          hid: 'description',
          name: 'description',
          content: keyword
        },
        {
          hid: 'og:title',
          property: 'og:title',
          content: title
        },
        {
          hid: 'og:description',
          name: 'og:description',
          content: "title Estrenos cine hoy description"
        },
        {
          hid: 'og:image',
          property: 'og:image',
          content: 'https://image.tmdb.org/t/p/w185_and_h278_bestv2/w58ohFF2YeEEVYRWiiMjJZ1hk9R.jpg'
        },
        {
          hid: 'twitter:title',
          property: 'og:title',
          content: "title Estrenos cine hoy"
        },
        {
          hid: 'twitter:description',
          name: 'og:description',
          content: keyword
        },
        {
          hid: 'twitter:image',
          property: 'twitter:image',
          content: 'https://image.tmdb.org/t/p/w185_and_h278_bestv2/w58ohFF2YeEEVYRWiiMjJZ1hk9R.jpg'
        },
        {
          hid: 'twitter:url',
          property: 'twitter:url',
          content: 'https://www.estrenoscinehoy.com/es/movie/details/475430-artemis-fowl'
        },
        {
          hid: 'twitter:card',
          property: 'twitter:card',
          content: 'https://www.estrenoscinehoy.com/es/movie/details/475430-artemis-fowl'
        },
        {
          hid: 'og:type',
          property: 'og:type',
          content: 'website'
        },
        {
          hid: 'og:url',
          property: 'og:url',
          content: 'https://www.estrenoscinehoy.com/es/movie/details/475430-artemis-fowl'
        },
        {
          hid: 'og:site_name',
          property: 'og:site_name',
          content: `estrenoscinehoy.com`
        },
        {
          hid: 'og:locale',
          property: 'og:locale',
          content: 'es-ES'
        },
        {
          hid: 'og:image:type',
          property: 'og:image:type',
          content: 'image/jpeg'
        }
      ]
    }
  }

}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>



