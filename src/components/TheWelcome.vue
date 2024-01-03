<script>
import MiddleComponent from './MiddleComponent.vue'

export default {
  components: {
    MiddleComponent
  },

  data() {
    return {
      mast: [
        { id: '1', name: 'slast' },
        { id: '2', name: 'pehar' }
      ]
    }
  }
}
</script>

<template>
  <MiddleComponent :sir="mast">
    <template v-slot:item="{ name }">
      <div class="item">
        <p>{{ body }}</p>
        <p class="meta">by {{ name }} likes</p>
      </div>
    </template>
  </MiddleComponent>
</template>
