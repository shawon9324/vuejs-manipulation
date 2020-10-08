<template>
    <div class="Hook">
        <h1>{{titile}}</h1>
        <button @click="changeTitle">Change Title</button>
    </div>
</template>

<script>
export default {
  name: "Hook",
  data() {
    return {
        titile: 'Hook Data'
    };
  },
  methods: {
    changeTitle(){
            this.titile = 'Title Changed'
    }
  },
  beforeCreate() {
      
  },
  created() {
  },
  beforeUpdate() {
      alert('Before UPDATE TITLE')
  },
  
};
</script>
 
<style scoped>
    
</style>
