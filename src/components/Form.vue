<template>
    <div>
        <textarea class="tweet_area" cols="30" rows="10" v-model="input" placeholder="いまどうしてる？"></textarea> <br>
        <button class="btn btn-info text-white mt-2"  @click="form_action">ツイート</button> 
    </div>
    <!-- テキストエリアに書いたツイートをv-modelで監視する -->
    <!-- ツイートボタンでform_actionへ処理が行く -->
</template>

<script>

export default{
    name: 'Form',
    props:{
    },
    data(){
        return{
            
        }
    },
    methods: {
        // v-modelのinputにからデータを貰い、emitで親に送る
        form_action(){
            this.$emit('form_event', this.input);
        }
    },
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