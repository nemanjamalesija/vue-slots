<script>
import MiddleComponent from './MiddleComponent.vue'
import SingleItem from './SingleItem.vue'

export default {
  components: {
    MiddleComponent,
    SingleItem
  }
}
</script>

<template>
  <MiddleComponent>
    <template v-slot:item="{ body, username, likes }">
      <SingleItem :body="body" :username="username" :likes="likes" />
    </template>
  </MiddleComponent>
</template>
