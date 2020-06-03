<template>
  <div>
    <h4>
      {{meal.category}}
      <span class="buttons h4">
        <button v-on:click="postLike(meal.id)">
          <b-icon-hand-thumbs-up v-if="liked" variant="success" />
          <b-icon-hand-thumbs-up v-else />
        </button>
        <button v-on:click="postDislike(meal.id)">
          <b-icon-hand-thumbs-down v-if="disliked" variant="danger" />
          <b-icon-hand-thumbs-down v-else />
        </button>
      </span>
    </h4>
    <h3>{{meal.name}}</h3>
    <div class="td" v-for="content in meal.contentInformation" :key="content">{{content}}</div>
    <p />
    <h5>{{meal.cost.students}} €</h5>
  </div>
</template>
<script>
import axios from "axios";

export default {
  name: "Meal",
  data() {
    return {
      costCategories: {
        employees: "Angestellte",
        guests: "Gäste",
        students: "Studenten"
      },
      liked: false,
      disliked: false
    };
  },
  methods: {
    postLike(id) {
      this.liked = !this.liked;
      axios.post(`http://localhost:3000/api/like/${id}`)
      this.disliked = this.disliked && !this.liked;

    },
    postDislike() {
      this.disliked = !this.disliked;
      this.liked = this.liked && !this.disliked;
    }
  },
  props: {
    meal: Object
  }
};
</script>
<style scoped>
button {
  background-color: white;
  box-shadow: unset;
  border: unset;
}

* {
  text-align: left;
}

.buttons {
  float: right;
}

.td {
  display: inline-block;
  font-family: inherit;
  font-size: 8pt;
  font-weight: normal;
  margin-right: 10px;
}
</style>