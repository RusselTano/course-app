<template>
<section class="padd content-limit">
  <div>
    <h2>Chapitre 3 : Intéragir avec le DOM</h2>
    <h1 v-bind:class="h1title" :id="h1id">
      Bonjour <span>{{ `${name.toUpperCase()} !` }}</span>
    </h1>
  
    <div v-bind="obj">
      <h2 v-html="baliseName"></h2>
    </div>
  
    <input :type="inputType" />
  
    <h1>{{ getTitle() }}</h1>
  
    <input :type="getType()" />
    <input type="text">
  </div>
</section>

</template>

<script setup lang="ts">
const name = 'Jean'
const baliseName = 'Bonjour <strong>Jean</strong>'

const h1title = 'montitre2'
const h1id = 'unid'

const obj = {
  class: h1title,
  id: h1id,
}

const inputType = "date"

function getTitle() {
  return 'Je suis un titre';
}

function getType() {
  return 'number';
}
</script>

<style scoped>
span {
  color: red;
  font-weight: bold;
}
input{
  color: #333;
  padding: 10px 12px;

  width: 300px;
}
.montitre2 {
  background-color: rgb(4, 2, 24);
}
</style>
