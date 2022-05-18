<template>
  <div id="app">
    <b-button id="button" variant="light" class="dropdown-toggle">
      <span>Button</span>
    </b-button>

    <b-popover
      target="button"
      title="Popover"
      placement="bottom"
      boundary="window"
      custom-class="popover-dropdown"
      triggers="click blur"
      no-fade
    >
      <b-pagination
        align="center"
        v-model="currentPage"
        :per-page="10"
        :total-rows="100"
        size="sm"
        limit="3"
        class="pt-2 m-0"
      ></b-pagination>
    </b-popover>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      currentPage: 1,
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
