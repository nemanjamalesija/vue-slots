<script>
import MiddleComponent from './MiddleComponent.vue'
// import SingleItem from './SingleItem.vue'

export default {
  components: {
    MiddleComponent
    // SingleItem
  },

  data() {
    return {
      sirevi: [
        {
          id: '3',
          name: 'Drogasi masni',
          text: 'Drogasi masni testiraju scoped slots',
          nlikes: 15
        },
        {
          id: '4',
          name: 'Gordana Aksentijevic',
          text: 'Kada iskasljah zorom mladak jahasmo konje',
          nlikes: 10
        }
      ]
    }
  }
}
</script>

<!-- <SingleItem :body="body" :username="username" :likes="likes" /> -->

<template>
  <MiddleComponent :items="sirevi">
    <template v-slot:item="{ index, item }">
      <div class="item">
        <p>{{ item.body }}</p>
        <p class="meta">by {{ item.name }} | {{ item.nlikes }} likes</p>
      </div>
    </template>
  </MiddleComponent>
</template>
