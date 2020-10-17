<template>
  <div class="slug">
    <p>_slug.vue</p>
    <p>{{ params }}</p>
  </div>
</template>

<script>
export default {
  name: 'Slug',
  asyncData({ params }) {
    return {
      params: JSON.stringify(params),
    }
  },
}
</script>

<style scoped></style>
