<template>
  <v-list-item :key="id" two-line>
    <v-list-item-content>
      <v-list-item-title>{{ name }}</v-list-item-title>
      <v-list-item-subtitle>{{ description }}</v-list-item-subtitle>
    </v-list-item-content>
  </v-list-item>
</template>

<script>
export default {
  name: 'ListItem',
  props: {
    id: { type: Number, default: -1, required: true },
    name: { type: String, default: 'An example item' },
    description: { type: String, default: 'An example description' }
  }
}
</script>

<style lang="css" scoped>

</style>
