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
      params,
    }
  },
  head() {
    return {
      title: `title: ${this.params.slug}`,
      meta: [
        {
          hid: 'og:title',
          name: 'og:title',
          property: 'og:title',
          content: `title is ${this.params.slug}`,
        },
        {
          hid: 'description',
          name: 'description',
          content: `uniq url is ${this.params.slug}`,
        },
        {
          hid: 'og:description',
          name: 'og:description',
          property: 'og:description',
          content: `uniq url is ${this.params.slug}`,
        },
      ],
    }
  },
}
</script>

<style scoped></style>
