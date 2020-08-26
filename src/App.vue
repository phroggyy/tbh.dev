<template>
  <div id="app">
    <h1>To be honest...</h1>
    <p>
      You should've just
      <span class="highlighted">{{ option }}</span>
    </p>
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
}

#app {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

h1 {
  font-size: 24px;
  font-weight: normal;
  color: #4A5568;
}
p {
  font-size: 42px;
}

.highlighted {
  color: #2C5282;
  font-weight: 600;
  text-decoration: underline;
  text-decoration-color: #ED8936;
}
</style>
