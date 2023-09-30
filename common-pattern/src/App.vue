<template>
  <div>
    <app-header :title="headerTitle"></app-header>
    <app-content :items="getItems" v-on:increase="add"></app-content>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'

export default {
  name: 'app',
  data() {
    return {
      headerTitle: 'Common Approach',
      datas: [{
        num : 10,
        id:1
      }]
    }
  },
  components: {
    AppHeader,
    AppContent
  },
  computed: {
    getItems() {
      return this.datas;
    }
  },
  methods: {
    add() {
      var beforeNum = this.datas[this.datas.length - 1].num;
      var beforeId = this.datas[this.datas.length - 1].id;
      var data = { num : beforeNum += 10, 
                   id : beforeId += 1 };
      this.datas.push(data);
    }
  }
}
</script>

<style>

</style>