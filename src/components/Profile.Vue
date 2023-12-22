<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>User Id is {{ userId }}</h2>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
      msg: 'Profile',
      userId : this.$route.params.user_id
    }
  },
  methods:{
updateId(){
this.userId = this.$route.params.user_id
}
  },
  watch:{
$route: 'updateId'
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
h1{
  color:red
}
</style>
