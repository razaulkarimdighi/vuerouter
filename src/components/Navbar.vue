<template>
  <div>
    <nav>
      <ul>
          <li> <router-link to="/">Home</router-link></li>
          <li> <router-link :to="{name : 'about'}">About</router-link></li>
          <li> <router-link to="/Contact">Contact</router-link></li>
          <li> <router-link to="/profile">Profile</router-link></li>

      </ul>
  </nav>

  <div>
<ul>
  <li v-for="(id, index) in user_ids" :key="index">
    <router-link :to="{name : 'profile', params: {user_id:id}}">Profile</router-link>
  </li>
</ul>
<button @click="Contact">Click Me</button>
<button @click="Forward">Forward</button>
</div>

  </div>


  </template>
  <script>
export default{
  name: 'Navbar',
  data(){
    return{
      user_ids: [1,2,4,6,7]
    }
  },
  methods:{
    Contact(){
this.$router.push({name :'Contact'} )
    },
    Backward(){
this.$router.go(-1)
    },
    Forward(){
this.$router.go(1)
    }
  }
}
  </script>
  <style>
  nav{
      text-align: center;
  }
  ul li{
    list-style: none;
  }
   nav ul{

   }
   nav li{
      list-style-type: none;
      display: inline-block;
      margin: 0px;
      padding: 8px;
   }
  </style>
