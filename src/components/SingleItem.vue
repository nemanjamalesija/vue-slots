<script>
export default {
  props: {
    body: { type: String },
    username: { type: String },
    likes: { type: Number }
  }
}
</script>
<template>
  <div class="item">
    <p>{{ body }}</p>
    <p class="meta">by {{ username }} | {{ likes }} likes</p>
  </div>
</template>
