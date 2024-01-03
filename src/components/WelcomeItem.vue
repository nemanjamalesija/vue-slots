<script>
export default {
  props: {
    sir: {
      type: Array
    }
  },

  data() {
    return {
      items: []
    }
  },
  mounted() {
    // mock remote data fetching
    setTimeout(() => {
      this.items = [
        { body: 'Scoped Slots', username: 'Masni sir', likes: 20 },
        { body: 'Vue testing', username: 'Mali Drazen', likes: 10 }
      ]
    }, 1000)
  }
}
</script>

<template>
  <ul>
    <li>
      <h1>{{ sir[0].name }}</h1>
    </li>
    <li v-if="!sir.length">Loading...</li>
    <li v-for="{ name } in sir">
      <slot name="item" v-bind="{ name }" />
    </li>
  </ul>
</template>

<style scoped>
ul {
  list-style-type: none;
  padding: 5px;
  background: linear-gradient(315deg, #42d392 25%, #647eff);
}
li {
  padding: 5px 20px;
  margin: 10px;
  background: #fff;
}
</style>
