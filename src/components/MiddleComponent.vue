<script>
import WelcomeItem from './WelcomeItem.vue'

export default {
  components: {
    WelcomeItem
  }
}
</script>
<template>
  <WelcomeItem>
    <template v-for="(_, slot) in $slots" v-slot:[slot]="props">
      <slot :name="slot" v-bind="props" />
    </template>
  </WelcomeItem>
</template>
