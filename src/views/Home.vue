<template>
  <div class="home">
    <categories v-bind:all='categories'></categories>
  </div>
</template>

<script>
// @ is an alias to /src
import Categories from '@/components/Categories.vue'

export default {
  name: 'home',
  components: {
    Categories
  },
  data(){
    return{
      categories:[],
      activeCategory:0
    }
  },
  methods:{
    getCategories(){
      this.axios
        .get('https://worldinfo.com.ua/api/categories')
        .then(response => {
          this.categories = response.data;
          console.log(response.data)
        })
        .catch(error => {
          console.log(error);
          this.errored = true;
        });
    }
  },
  mounted(){
    this.getCategories();
  }
}
</script>
