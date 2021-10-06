<template>
<!-- Formコンポーネントから来たform_eventにて、イベントappformを発火 -->
<Form  
  @form_event="appform_action"
/>


<hr class="line" size="7" />
<h3>これまでのツイート</h3>

<!-- v-bindで送られて来たツイートをtweetコンポーネントへ渡す -->
<!-- v-forで呟いた数だけコンポーネントを回して表示させる。キーはtweetコンポーネントへ渡す -->
<tweet 
  :tweet_msg="tweet_data"
  v-for="num of tweet_data.length"
  :key="num"
  :number="num-1"
/>
</template>

<script>
import Form from './components/Form.vue'
import tweet from './components/tweet.vue'

export default {
  name: 'App',
  components: {
    Form,
    tweet
  },
  data(){
    return{
      tweet_data:[],
    }
  },
  methods:{

    // Formコンポーネントから受け取った引数をtweetコンポーネントへ渡すために
    // tweet_dataへ格納
    appform_action(tweet_msg){
      this.tweet_data.push(tweet_msg);
    }
  },
}
</script>

<style>
div{
  margin: auto;
  width:auto;

}
.line{
  margin: auto;
  margin-top: 20px;
  width:auto;
  max-width:300px;
}
</style>

