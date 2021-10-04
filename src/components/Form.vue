<template>
    <div>

    <textarea class="tweet_area" cols="30" rows="10" v-model="input" placeholder="いまどうしてる？"></textarea> <br>
    <button class="btn btn-info text-white mt-2">ツイート</button> 

    </div>


</template>

<script>

export default{
    name: 'Form',
    props:{
        msg: String
    },
    data(){
        return{
            
        }
    }
}
</script>

<style>
.tweet_area{
    margin-top: 20px;
    display: block;
    margin-left: auto;
    margin-right: auto;
}
div{
text-align: center;
}

</style>