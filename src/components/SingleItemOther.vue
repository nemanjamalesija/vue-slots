<script>
export default {
  props: {
    body: { type: String },
    name: { type: String },
    nlikes: { type: Number }
  }
}
</script>
<template>
  <div class="item">
    <p>{{ body }}</p>
    <p class="meta">by {{ name }} | {{ nlikes }} likes</p>
  </div>
</template>
