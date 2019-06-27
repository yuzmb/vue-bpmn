<template>
  <vue-bpmn
    url="/static/diagram.bpmn"
    v-on:error="handleError"
    v-on:shown="handleShown"
    v-on:loading="handleLoading"
  ></vue-bpmn>
</template>

<script>
  import VueBpmn from 'vue-bpmn'

  export default {
    components: {
      VueBpmn
    },
    methods: {
      handleError: function(err) {
        console.error('failed to show diagram', err)
      },
      handleShown: function() {
        console.log('diagram shown')
      },
      handleLoading: function() {
        console.log('diagram loading')
      }
    }
  }
</script>