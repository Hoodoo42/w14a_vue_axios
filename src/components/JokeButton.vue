<template>
  <div>
    <button @click="new_joke">New Joke</button>
    <h3 v-for="(joke,index) in jokes" :key="index">{{jokes}}</h3>
  
  </div>
</template>

<script>
import axios from "axios";



export default {
data() {
    return {
        jokes: [],
    }
},

  methods: {
    new_joke() {
        this.$root.$emit(`style_joke`, this.jokes )

      axios
        .request({
          url: `https://ron-swanson-quotes.herokuapp.com/v2/quotes`,
          
        })
        .then((res) => {
           this.jokes = res[`data`]
        })
        
        .catch((err) => {
            err;
        });
    },
  },

  components: {
   
  },
};
</script>

<style scoped>
</style>