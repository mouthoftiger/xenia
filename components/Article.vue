<template>
  <div
    v-editable="blok"
    class="p-4 md:p-8">
    <div class="main-content">
      <h1 class="mb-6">{{ blok.title }}</h1>
      <component
        v-for="blok in blok.body"
        :key="blok._uid"
        :blok="blok"
        :is="blok.component" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true
    }
  }
}
</script>
