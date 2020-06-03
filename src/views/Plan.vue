<template>
  <div id="body">
    <div id="container">
      <div id="heading">
        <div id="title">
          HfG
          <span id="lead">Mensakarte</span>
        </div>
      </div>
      <div class="datepicker">
        <label for="example-datepicker"></label>
        <b-form-datepicker value-as-date id="example-datepicker" v-model="selectedDay" class="mb-2"></b-form-datepicker>
      </div>
    </div>
    <list
      :tableData="loadedData.filter(essen => this.selectedDay && (this.day(essen.day) === this.selectedDay.getDay()))"
    />
  </div>
</template>
<script>
import List from "../components/List.vue";
import axios from "axios";

export default {
  name: "Plan",
  components: {
    List
  },
  props: {
    msg: String
  },
  data: function() {
    return {
      loadedData: [],
      days: [],
      selectedDay: undefined
    };
  },
  methods: {
    selectDay: function(day) {
      this.selectedDay = day;
    },
    day(string) {
      return ["So", "Mo", "Di", "Mi", "Do", "Fr", "Sa"].indexOf(string);
    }
  },
  mounted() {
    axios
      .get("http://localhost:3000/api/getData")
      .then(response => {
        this.loadedData = response.data;
        this.days = this.loadedData.map(essen => essen.day);
        this.days = this.days.filter((a, b) => this.days.indexOf(a) === b);
        this.selectedDay = this.days[0];
      })
      .catch(err => {
        console.log(err);
      });
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.datepicker {
  width: 25vw;
  margin: auto;
}

#container {
  background-color: rgb(211, 211, 211);
  margin: 0 calc(69px / 0.3);
  border-radius: 3px 3px 15px 15px;
  padding-top: 69px;
  padding-bottom: calc(69px * 1);
}

p {
  padding: 0;
}

#title {
  color: white;
  text-align: center;
  font-size: 80pt;
  line-height: 80pt;
  margin-bottom: 10px;
}

#lead {
  font-size: 40pt;
  line-height: 40pt;
}
</style>
