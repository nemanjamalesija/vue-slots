<script>
import MiddleComponent from './MiddleComponent.vue'
import TheWelcomeOther from './TheWelcomeOther.vue'
// import SingleItem from './SingleItem.vue'

export default {
  components: {
    MiddleComponent,
    TheWelcomeOther
    // SingleItem
  },

  data() {
    return {
      items: [
        { id: '1', username: 'Jahac apokalipse', body: 'Slast je lorem ipsum soldum', likes: 25 },
        { id: '2', username: 'pehar', body: 'Velicanstveno somertajm sadness', likes: 50 }
      ]
    }
  }
}
</script>

<!-- <SingleItem :body="body" :username="username" :likes="likes" /> -->

<template>
  <MiddleComponent :items="items">
    <template v-slot:item="{ index, item }">
      <div class="item">
        <p>{{ item.body }}</p>
        <p class="meta">by {{ item.username }} | {{ item.likes }} likes</p>
      </div>
    </template>
  </MiddleComponent>

  <TheWelcomeOther />
</template>
