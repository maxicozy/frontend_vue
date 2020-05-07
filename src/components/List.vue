<template>
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
</template>

<script>
export default {
  name: 'List',
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