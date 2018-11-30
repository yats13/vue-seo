<template lang="html">
  <section id="Categories">
    <h1>Категории</h1>
    <router-link v-for='item in all' :key='item.id' :to="{ name: 'category', params: {id:item.id} }">{{item.name}}</router-link>
  </section>
</template>

<script>
export default {
  name:'Categories',
  props:{
    all:Array
  }
}
</script>

<style lang="css">
</style>
