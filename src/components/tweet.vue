<template>

<hr />
<h3>これまでのツイート</h3>
    <div class="past_tweet">
        {{first_tweet}}
    </div>
</template>

<script>

export default{
    name:'tweet',
    data(){
        return{
            first_tweet: "こんにちは"
        }
    },
}
</script>

<style>
.past_tweet{
    border:  1px solid gray;
    padding: 10px;
    border-radius: 5px;
    text-align: left;
}
</style>