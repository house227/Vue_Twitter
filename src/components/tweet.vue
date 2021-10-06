<template>

    <div class="past_tweet">
        <!-- 受け取った配列のキー番目を表示 -->
        {{tweet_msg[number]}}
    </div>
</template>

<script>

export default{
    name:'tweet',
    data(){
        return{
            first_tweet: "こんにちは",
        }
    },
    props:{
        // ツイートの受け取り
        tweet_msg: Object,
        number:Number,
    },
}
</script>

<style>
.past_tweet{
    border:  1px solid gray;
    padding: 10px;
    margin-bottom: 50px;
    border-radius: 5px;
    text-align: left;
    max-width:280px;
}
</style>