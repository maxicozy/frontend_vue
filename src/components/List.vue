<template>
  <table id="table">
    <tr>
      <th id="leftRow">Kategorie</th>
      <th id="headerRow">Bezeichnung</th>
      <th id="headerRow">Inhalte</th>
      <th id="headerRow">Labels</th>
      <th id="headerRow">Preis</th>
    </tr>

    <meal v-for="meal in tableData" :meal="meal" :key="meal.id" />
  </table>
</template>

<script>
import Meal from "../components/Meal.vue";
export default {
  name: "List",
  components: {
    Meal,
  },
  props: {
    tableData: Array
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#table {
  width: 90vw;
  margin: auto;
  margin-top: 18vh;
  text-align: left;
  padding: 5px;
  border: 1px black solid;
}

#headerRow {
  width: 350px;
}

#leftRow {
  width: 250px;
}

th {
  padding-top: 10px;
  padding-bottom: 10px;
  font-family: inherit;
  font-size: 24px;
  font-weight: bold;
  padding-left: 10px;
}

td {
  padding-top: 10px;
  padding-bottom: 10px;
  font-family: inherit;
  font-size: 20px;
  font-weight: normal;
  padding-left: 10px;
}
</style>