<template>
<div id="body">
    <div id="container">
      <div id="heading">
        <h2>HfG <br> Mensakarte</h2>
      </div> 
      <dropdown></dropdown>
    <list></list>
    {{loadedData}}
    </div>
</div>
</template>
<script>  
import List from '../components/List.vue'
import Dropdown from '../components/Dropdown.vue'
import axios from 'axios'

export default {
  name: 'Plan',
  components: {
    Dropdown,
    List
  },
  props: {
    msg: String
  },
    data: function () {
    return {
      loadedData: undefined,
    }
  },
  mounted() {
    axios.get("http://localhost:3000/api/getData")
      .then(response => {
        this.loadedData = response.data;
      })
      .catch(err => {
        console.log(err)
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#heading {
  float: left;
  height: 50px;
}

#body { 
  padding: 20px;
  background-color: beige;
  font-family: Futura, "Trebuchet MS", Arial, sans-serif; 
  font-size: 28px; 
  font-style: normal; 
  font-variant: normal; 
  font-weight: 700; 
  line-height: 36.4px; 
}

#container {
  background-color: white;
  font-family: Futura, "Trebuchet MS", Arial, sans-serif; 
  font-size: 28px; 
  font-style: normal; 
  font-variant: normal; 
  font-weight: 700; 
  line-height: 36.4px; 
  height: 115vh;
  width: 90vw;
  margin: auto;
  padding-left: 40px;
  padding-top: 15px;
  padding-right: 40px;
}
</style>
