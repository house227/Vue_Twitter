<template>
<Form />
<tweet />
</template>

<script>
import Form from './components/Form.vue'
import tweet from './components/tweet.vue'

export default {
  name: 'App',
  components: {
    Form,
    tweet
  }
}
</script>

<style>
div{
  margin: auto;
  width:auto;
  max-width:600px;
}
</style>

