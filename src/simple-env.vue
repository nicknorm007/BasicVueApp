<template>
  <div>
    <a class="button is-info" @click="getBuildJson">Dev Env Info</a>
    <a class="button is-warning" v-on:click="">QA Env Info</a>
    <a class="button is-success" v-on:click="">STG Env Info</a>
    <a class="button is-danger" v-on:click="">PROD Env Info</a>
  </div>
</template>

<script>

  export default {
    name: 'simple-env',
    data: function () {
      return {
        counter: 0
      }
    },
    methods: {
      getBuildJson: function() {

        alert("getBuildJSon")

      },
    }
}
</script>
