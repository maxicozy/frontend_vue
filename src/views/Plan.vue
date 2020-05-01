<template>
<div id="body">
    <div id="container">
  <div id="heading">
  <h2>HfG <br> Mensakarte</h2>
    <select name="wochentag" id="select">
      <option>Montag</option>
      <option>Dienstag</option>
      <option>Mittwoch</option>
      <option>Donnerstag</option>
      <option>Freitag</option>
    </select>
  </div>

  <table id="table">
    <tr>
      <th id="leftRow">Kategorie</th>
      <th id="headerRow">Bezeichnung</th>
      <th id="headerRow">Inhalte</th>
      <th id="headerRow">Labels</th>
      <th id="headerRow">Preis</th>
    </tr>
    <tr>
      <th id="leftRow">Suppe</th>
    </tr>
    <tr>
      <th id="leftRow">Hauptgericht 1</th>
    </tr>
    <tr>
      <th id="leftRow">Hauptgericht 2</th>
    </tr>
    <tr>
      <th id="leftRow">Hauptgericht 3</th>
    </tr>
    <tr>
      <th id="leftRow">Hauptgericht 4</th>
    </tr>
    <tr>
      <th id="leftRow">Beilage 1</th>
    </tr>
    <tr>
      <th id="leftRow">Beilage 2</th>
    </tr>
    <tr>
      <th id="leftRow">Beilage 3</th>
    </tr>
    <tr>
      <th id="leftRow">Beilage 4</th>
    </tr>
    <tr>
      <th id="leftRow">Beilage 5</th>
    </tr>
    <tr>
      <th id="leftRow">Beilage 6</th>
    </tr>
    <tr>
      <th id="leftRow">Nachtisch 1</th>
    </tr>
    <tr>
      <th id="leftRow">Nachtisch 2</th>
    </tr>
    <tr>
      <th id="leftRow">Nachtisch 3</th>
    </tr>
  </table>
  </div>
</div>
</template>

<script>
export default {
  name: 'Plan',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#table {
  width: 90vw;
  margin: auto;
  margin-top: 18vh;
  text-align: left;
  padding: 5px, 5px, 5px, 5px;
  border: 1px black solid;
}

#heading {
  float: left;
  height: 50px;
}

#body { 
  background-color: beige;
  font-family: Futura, "Trebuchet MS", Arial, sans-serif; 
  font-size: 28px; 
  font-style: normal; 
  font-variant: normal; 
  font-weight: 700; 
  line-height: 36.4px; 
}

#container {
  background-color: beige;
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
</style>
