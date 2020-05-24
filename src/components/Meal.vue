<template>
  <tr>
    <td>{{meal.category}}</td>
    <td>{{meal.name}}</td>
    <td>
      <p v-for="content in meal.contentInformation" :key="content">{{content}}</p>
    </td>
    <td>{{meal.labels.split(',').join(', ')}}</td>
    <td>
      <p v-for="k in Object.keys(meal.cost)" :key="k">{{costCategories[k] }}: {{ meal.cost[k]}}</p>
    </td>
  </tr>
</template>
<script>
export default {
  name: "Meal",
  data() {
    return {
      costCategories: {
        employees: "Angestellte",
        guests: "Gäste",
        students: "Studenten"
      }
    };
  },
  props: {
    meal: Object
  }
};
</script>
<style scoped>
td {
  padding-top: 10px;
  padding-bottom: 10px;
  font-family: inherit;
  font-size: 20px;
  font-weight: normal;
  padding-left: 10px;
}
</style>