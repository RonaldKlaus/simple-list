<template>
  <div>
    <h1>Alle Listen im Überblick</h1>
    <div v-for="(list, index) in lists" :key="index">
      <List :key="list.id" :title="list.title" :list-items="list.items" />
    </div>
  </div>
</template>

<script>

import List from '../../components/List.vue'

export default {
  components: {
    List
  },
  data () {
    return {
      lists: [
        {
          id: 1,
          title: 'Futter',
          items: [
            { id: 1, name: 'Bananen', description: '5 Stück' },
            { id: 2, name: 'Tomaten', description: '2kg' }
          ]
        },
        {
          id: 2,
          title: 'Technikkrams',
          items: [
            { id: 1, name: 'Playstation 5', description: 'Yiiieehaa' },
            { id: 2, name: 'OLED TV', description: '4K muss sein' }
          ]
        }
      ]
    }
  }
}
</script>
