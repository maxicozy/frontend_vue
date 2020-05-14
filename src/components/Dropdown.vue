<template>
  <select name="wochentag" id="select">
    <option v-if="days.includes('Mo')">Montag</option>
    <option v-if="days.includes('Di')">Dienstag</option>
    <option v-if="days.includes('Mi')">Mittwoch</option>
    <option v-if="days.includes('Do')">Donnerstag</option>
    <option v-if="days.includes('Fr')">Freitag</option>
  </select>
</template>

<script>
export default {
  name: 'Dropdown',
  props: {
    days: {
      type: Array
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#select {
  position: absolute;
  width: 160px;
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