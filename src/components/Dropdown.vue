<template>
  <select v-on:change="$emit('select', $event.target.value)" name="wochentag" id="select">
    <option v-for="day in days" :value="day" :selected="selectedDay === day" :key="day">{{dayNames[day]}}</option>
  </select>
</template>

<script>
export default {
  name: "Dropdown",
  data() {
    return {
      dayNames: {
        Mo: "Montag",
        Di: "Dienstag",
        Mi: "Mittwoch",
        Do: "Donnerstag",
        Fr: "Freitag"
      }
    };
  },
  props: {
    selectedDay: {
      type: String
    },
    days: {
      type: Array
    }
  }
};
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