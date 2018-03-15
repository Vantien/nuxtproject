<template>
  <div>
    <h1>user</h1>
    <ul>
      <li v-for="user in users" v-bind:key="user.id">
        {{ user }}
      </li>
    </ul>
    </div>
</template>
<script>
import axios from 'axios'

export default {
  
  data () {
    return {
    users: []
    }
  },
  mounted() {
    var self = this
    axios.get('https://jsonplaceholder.typicode.com/users')
  .then(function (response) {
    console.log(response);
    self.users =  response.data
  })
  .catch(function (error) {
    console.log(error);
  });
  }
}
</script>
