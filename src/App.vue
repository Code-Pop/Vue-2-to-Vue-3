<template>
  <div id="app">
    <BaseInput
      v-model="email"
      @blur="email = 'blurrr@its.cold'"
      label="Email:"
      type="email"
      class="thicc"
    />

    <pre>{{ email }}</pre>
  </div>
</template>

<script>
import { ref } from 'vue'
import BaseInput from './components/BaseInput'

export default {
  name: 'App',
  components: {
    BaseInput
  },
  setup () {
    const email = ref('')

    return {
      email
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

pre {
  font-size: 1.5rem;
}

button,
label,
input,
optgroup,
select,
textarea {
  display: inline-flex;
  font-family: "Open sans", sans-serif;
  font-size: 100%;
  line-height: 1.15;
  margin: 0;
}
input,
textarea {
  box-sizing: border-box;
  border: solid 1px rgba(0, 0, 0, 0.4);
}
input.thicc {
  border-width: 4px;
}
textarea {
  width: 100%;
  overflow: auto;
  font-size: 20px;
}
[type="checkbox"],
[type="radio"] {
  box-sizing: border-box;
  padding: 0;
  margin-right: 0.5rem;
}
[type="number"]::-webkit-inner-spin-button,
[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
[type="search"] {
  -webkit-appearance: textfield;
  outline-offset: -2px;
}
[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
[type="text"],
[type="number"],
[type="search"],
[type="password"] {
  height: 52px;
  width: 100%;
  padding: 0 10px;
  font-size: 20px;
}
[type="text"]:focus,
[type="number"]:focus,
[type="search"]:focus,
[type="password"]:focus {
  border-color: #39b982;
}
select {
  height: 52px;
  padding: 0 24px 0 10px;
  vertical-align: middle;
  background: #fff
    url("data:image/svg+xml;charset=utf8,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 4 5'%3E%3Cpath fill='%23343a40' d='M2 0L0 2h4zm0 5L0 3h4z'/%3E%3C/svg%3E")
    no-repeat right 12px center;
  background-size: 8px 10px;
  border: solid 1px rgba(0, 0, 0, 0.4);
  border-radius: 0;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
}
select:focus {
  border-color: #39b982;
  outline: 0;
}
select:focus::ms-value {
  color: #000;
  background: #fff;
}
select::ms-expand {
  opacity: 0;
}
</style>
