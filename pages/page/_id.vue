<template>
  <div>
    <h2>Page {{ id }}</h2>
    <input v-model="value" type="text" />
  </div>
</template>

<script>
export default {
  meta: {
    key: 'path',
    title(route) {
      return `Page ${route.params.id}`
    }
  },

  data() {
    return {
      id: this.$route.params.id,
      value: ''
    }
  }
}
</script>
