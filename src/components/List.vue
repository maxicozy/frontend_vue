<template>
  <b-row class="cols">
    <b-col v-for="category in getCategories()" :key="category">
      <b-card
        v-for="meal in tableData.filter(m => m.category.startsWith(category))"
        :key="meal.id"
        :img-src="'https://picsum.photos/600/300/?r=' + Math.random()"
        img-alt="Just a random image"
        img-top
        tag="article"
        class="mb-5"
      >
        <b-card-text img-src="https://picsum.photos/1024/480/?image=58">
          <Meal class="mahlzeit" :meal="meal" />
        </b-card-text>
      </b-card>
    </b-col>
  </b-row>
</template>

<script>
import Meal from "../components/Meal.vue";
export default {
  name: "List",
  components: {
    Meal
  },
  methods: {
    getCategories() {
      const reg = /([a-zA-Z]+)[0-9]*/;
      const allCategories = this.tableData
        .map(essen => essen.category)
        .map(s => s.match(reg)[1])

    console.log(allCategories)

      return allCategories.filter((a, b) => allCategories.indexOf(a) === b);
    }
  },
  props: {
    tableData: Array
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cols {
  margin-top: 20vh;
  margin-left: auto;
  margin-right: auto;
  padding: 0 calc(69px / 0.3);
}
</style>