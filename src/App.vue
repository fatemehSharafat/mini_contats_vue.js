<template>
  <div id="app" class="container">
    <user-create  @add-user="addUser">  </user-create>
   <user :items="items"></user>
   
   
   
  </div>
</template>

<script>
import User from './components/User.vue';
import UserCreate from './components/UserCreate.vue';


export default {
  name: 'App',
  components: {
    User,
    UserCreate
  },
  data() {
    return {
    
      items: [
        {
          pnum: 'تلفن همراه',

        },
      ]
    }
  },
  methods: {
    addUser(pnum){
      this.items.push({pnum})
      console.log(this.items)
    }
  },
  
 
}
</script>

<style>
#app{
    
    width:100%;
    margin-top: 20px;
  }
</style>
