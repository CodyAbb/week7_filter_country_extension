<template lang="html">
  <div class="container">
    <select v-model="countryFromList">
      <option v-for="country in countries" :value="country">{{country.name}}</option>
    </select>
    <button @click.prevent="handleClick">
      Show
    </button>
  </div>

</template>

<script>
import { eventBus } from '../main.js';

export default {
  name: "country-list",
  props: ['countries'],
  data: {
    countryFromList: ''
  },
  methods: {
    handleClick() {
      eventBus.$emit('country-selected', this.countryFromList);
    }
  }
};

</script>

<style lang="css" scoped>
</style>
