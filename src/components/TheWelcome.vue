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

<!-- <SingleItem :body="body" :username="username" :likes="likes" /> -->

<template>
  <MiddleComponent>
    <template v-slot:item="{ index, item }">
      <div class="item">
        <p>{{ item.body }}</p>
        <p class="meta">by {{ item.username }} | {{ item.likes }} likes</p>
      </div>
    </template>
  </MiddleComponent>
</template>
