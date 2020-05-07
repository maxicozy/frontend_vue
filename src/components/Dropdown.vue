<template>
  <select name="wochentag" id="select">
    <option>Montag</option>
    <option>Dienstag</option>
    <option>Mittwoch</option>
    <option>Donnerstag</option>
    <option>Freitag</option>
  </select>
</template>

<script>
export default {
  name: 'Dropdown',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#select {
  position: absolute;
  font-family: inherit;
  font-size: 24px; 
  padding: 5px;
  background-color: white;
  border: 1px rgb(96, 96, 96) solid; 
  right: 4.6vw;
  top: 75px;
} 

#select:hover {
  background-color: lightgray;
}


option {
  background-color: white;
  padding-top: 5px;
  padding-bottom: 5px;
}
</style>