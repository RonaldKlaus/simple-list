<template>
  <v-card>
    <v-toolbar>
      <v-toolbar-title>{{ title }}</v-toolbar-title>
    </v-toolbar>
    <v-list>
      <v-list-item-group v-for="(item, index) in listItems" :key="index">
        <ListItem :id="item.id" :name="item.name" :description="item.description" />
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
import ListItem from './ListItem.vue'

export default {
  components: {
    ListItem
  },
  props: {
    id: { type: Number, default: -1 },
    title: { type: String, default: null },
    listItems: { type: Array, default () {} }
  }
}
</script>

<style lang='css' scoped>

</style>
