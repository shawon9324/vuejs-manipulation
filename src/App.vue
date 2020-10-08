 <!-- This is The Master Component -->

<template>
  <div id="app">
    <h2>{{ title }} </h2>
    <Navbar></Navbar>
    <AllFriends :friends="friends" @delete="deleteFriend">
    </AllFriends>
    <OnlineFriends :friends="friends"></OnlineFriends>
  </div>
</template>
 
<script>
    import Navbar from './components/Navbar.vue'
    import AllFriends from './components/AllFriends.vue'
    import OnlineFriends from './components/OnlineFriends.vue'
    export default {
      name: 'App',
      data() {
        return {
          title: 'Congratz, Our Vue Website is Working Fine With VUE.JS!',
          friends:[
            {   name:'Shawon',    online:true     },
            {   name:'Shahriar',  online:false    },
            {   name:'Jhon',      online:true     },
            {   name:'David',     online:false    },
            {   name:'Miller',    online:true     },
            {   name:'Watson',    online:true     }
          ]
        }
      },
      components:{
        Navbar,
        AllFriends,
        OnlineFriends
      },
      methods: {
        deleteFriend(payload){
          // console.log(payload);
          this.friends = this.friends.filter(friend =>{
            return friend.name !== payload.name;
          })
        }
      },
    
  }
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
