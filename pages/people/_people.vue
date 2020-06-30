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
<!-- eslint-disable -->
<!-- eslint-enable -->
<script>
/* eslint-disable camelcase, no-console */
export default {
  name: 'EchPeopleDetails',
  // eslint-disable-next-line require-await
  async asyncData({ app, route, params, store }) {
    console.log(params)

    return {
      requestHeader: {
        title: 'testingTitle',
        overview: 'testingOverview'
      }
    }
  },
  data() {
    return {
      requestHeader: {},
      people: {}
    }
  },
  head() {
    const { title, overview, posterPath } = {
      ...this.requestHeader
    }
    const defaultDesc =
      'Estrenos cine hoy: toda la info sobre películas, seríes, actores, actrices, TV Shows y programación. Movies, actor, actress, movies rating, news, tv networks'
    const routePath = 'https://www.estrenoscinehoy'
    const language = 'es'
    const defaultTitle = title || 'EstrenosCineHoy'
    const defaultDescription = overview || defaultDesc
    const overviewDefault = overview || defaultDesc
    const defaultPosterPath = posterPath || 'https://image.tmdb.org/t/p/w185_and_h278_bestv2/w58ohFF2YeEEVYRWiiMjJZ1hk9R.jpg'
    return {
      title: defaultTitle,
      description: defaultDescription,
      link: [
        {
          rel: 'canonical',
          href: `${routePath}`
        }
      ],
      htmlAttrs: {
        lang: `${language}`
      },
      meta: [
        {
          charset: 'utf-8'
        },
        {
          hid: 'title',
          name: 'title',
          content: defaultTitle
        },
        {
          hid: 'description',
          name: 'description',
          content: overviewDefault
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: defaultTitle
        },
        {
          hid: 'og:description',
          name: 'og:description',
          content: overviewDefault
        },
        {
          hid: 'og:image',
          name: 'og:image',
          content: defaultPosterPath
        },
        {
          hid: 'twitter:title',
          name: 'twitter:title',
          content: defaultTitle
        },
        {
          hid: 'twitter:description',
          name: 'twitter:description',
          content: overviewDefault
        },
        {
          hid: 'twitter:image',
          name: 'twitter:image',
          content: defaultPosterPath
        },
        {
          hid: 'twitter:url',
          name: 'twitter:url',
          content: `www.estrenoscinehoy.com`
        },
        {
          hid: 'twitter:card',
          name: 'twitter:card',
          content: defaultPosterPath
        },
        {
          hid: 'og:type',
          name: 'og:type',
          content: 'website'
        },
        {
          hid: 'og:url',
          name: 'og:url',
          content: `https://www.estrenoscinehoy.com/es/movie/details/475430-artemis-fowl`
        },
        {
          hid: 'og:site_name',
          name: 'og:site_name',
          content: `estrenoscinehoy.com`
        },
        {
          hid: 'og:locale',
          name: 'og:locale',
          content: `es`
        },
        {
          hid: 'og:image:type',
          name: 'og:image:type',
          content: 'image/jpeg'
        }
      ]
    }
  }
}
</script>
<style></style>
