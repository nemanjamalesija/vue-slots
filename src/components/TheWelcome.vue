<script>
import MiddleComponent from './MiddleComponent.vue'

export default {
  components: {
    MiddleComponent
  }
}
</script>

<template>
  <MiddleComponent>
    <template v-slot:item="{ body, username, likes }">
      <div class="item">
        <p>{{ body }}</p>
        <p class="meta">by {{ username }} | {{ likes }} likes</p>
      </div>
    </template>
  </MiddleComponent>
</template>
