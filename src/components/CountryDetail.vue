<template lang="html">
  <article v-if="country">
    <h2>{{country.name}}</h2>
    <p>Capital: {{country.capital}}</p>
    <p>Population: {{country.population}}</p>
    <p>Spoken Languages:</p>
    <ul>
      <li v-for="language in country.languages">
        {{language.name}}
      </li>
    </ul>
    <img :src="country.flag" alt="">
  </article>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
