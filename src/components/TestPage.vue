<template>
  <div>
    <v-btn @click="testGet">Get Me</v-btn>
    <v-btn @click="testPost">Post Me!</v-btn>
  </div>
</template>
<script>
import axios from "axios"

export default {
  methods: {
    testGet (){
      // Make a request for a user with a given ID
      axios.get('https://reqres.in/api/users?page=2')
        .then(res => {
          // handle success
          console.log(res);
        })
        .catch(err => {
          // handle error
          console.log(err);
        })
        .then(() => {
          // always executed
          console.log("Get Action!")
        });
    },
    testPost(){
      axios.post("https://reqres.in/api/register",{
          "email": "eve.holt@reqres.in",
          "password": "pistol"
      })
      .then(res => {
        console.log(res)
      })
      .catch(err=> {
        console.log(err)
      })
      .then(()=>{
        console.log("Post Action!")
      })
    }
  }
}
</script>