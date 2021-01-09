<template>
  <div class="main-body">
    <header id="header">
        <h1 style="">
            <img src="icon.png" style="width:48px;height:48px;">
            <router-link to="/">
                OILSTAND
            </router-link>
        </h1>
    </header>
    <nuxt />
    <footer>
        &copy; OILSTAND
    </footer>
  </div>
</template>

<style>
* {
    margin:0;padding:0;
}
body {
    background-color:#F9F9F9;
}
.main-body {
}
header {
    display:flex;
}
header h1 {
    height:100%;
    display:flex;
    align-items: center;
}
header h1 a {
    display:block;
    height:100%;
    position:relative;
    vertical-align:middle;

    color:#2d2d2d;
    font-weight: 500;
}
@media screen and (max-width:959px) {
    header {
        height:50px;
        padding: 8px 16px;
    }
    header h1 a {
        line-height:50px;

        padding-left:calc(32px + 8px);
        font-size:24px;
    }

    #menu_sitemap {
        display:none;
    }
    footer {
        margin-top: 24px;
        padding: 16px 8px;
        position:relative;
    }
}
@media screen and (min-width:960px) {
    header {
        height:90px;
        padding: 16px 32px;
    }
    header h1 a {
        line-height:90px;
        padding-left:calc(16px);
    }
    footer {
        margin-top: 80px;
        padding: 8px 20px;

        width:100%;
        left:0;bottom:0;
        text-align:center;
    }
}
footer {
    background-color:#707070;
    color:white;
}
footer > div {
    max-width:1200px;
    margin:0 auto;
}
footer h2 {
    margin: 16px 0;
}
</style>

<script>
export default {
  head() {
      return {
            htmlAttrs: {
                lang: 'ja',
                prefix: 'og: http://ogp.me/ns#'
            },
            title: 'OILSTAND',
            meta: [
                { hid: 'description', name: 'description', content: `OILSTAND` },
                { hid: 'keywords', name: 'keywords', content: 'OILSTAND' },
                { hid: 'og:site_name', property: 'og:site_name', content: 'OILSTAND' },
                { hid: 'og:type', property: 'og:type', content: 'website' },
                { hid: 'og:url', property: 'og:url', content: 'https://oilstand.net' + this.$nuxt.$route.path },
                { hid: 'og:title', property: 'og:title', content: `OILSTAND` },
                { hid: 'og:description', property: 'og:description', content: 'OILSTAND' },
                { hid: 'og:image', property: 'og:image', content: 'https://oilstand.net/logo.png' },
                { name: 'twitter:card', content: 'summary' }
            ],
      }
  },
  data () {
    return {
    }
  },
  methods: {
  },
  computed: {
  },
  mounted() {
  }
}
</script>
