<template>
  <div id="app">
    <div></div>
    <main class="content">
      <h1>To be honest...</h1>
      <p>
        You should've just
        <span class="highlighted">{{ option }}</span>
      </p>
    </main>
    <footer>
      <p>Built by <a href="https://blog.leosjoberg.com">Leo Sjöberg</a></p>
      <a href="https://twitter.com/phroggyy"><i class="fab fa-twitter"></i></a>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      options: [
          'used a VPS',
          'become a woodworker',
          'moved to Bali',
          'listened',
          'used server-side rendering',
          'worn a mask',
      ],
      option: null,
    }
  },
  mounted: function() {
    this.option = this.options[Math.floor(Math.random() * this.options.length)];
  }
}
</script>

<style>
body, html {
  width: 100%;
  height: 100%;
  margin: 0;
}

#app {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-rows: auto 1fr auto;
  grid-template-areas: "header" "content" "footer";
}

main h1 {
  font-size: 24px;
  font-weight: normal;
  color: #4A5568;
}
main p {
  font-size: 42px;
}

.content {
  grid-area: content;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.highlighted {
  color: #2C5282;
  font-weight: 600;
  text-decoration: underline;
  text-decoration-color: #ED8936;
}

footer {
  grid-area: footer;
}

footer a:nth-child(2) {
  font-size: 30px;
}

.fa-twitter {
  color: #1DA1F2;
}
</style>
