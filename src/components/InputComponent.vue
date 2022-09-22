<template>
    <div class="form">
        <form @submit.prevent="submit">
            <div class="input">
                <textarea rows="4" cols="110" placeholder="write something" v-model="isitweet"></textarea>
                <div class="button">
                    <button style="float: right" :disabled="isitweet.length > 10 ? true : false">submit</button>
                </div>
                <div class="footer">
                    <p>{{ isitweet.length + "/10" }}</p>
                </div>
            </div>    
        </form> 
        <div class="aku" v-for="data in tweet" :key="data">
            <h1>{{ aku.username_pribadi }}</h1>
        </div>
        <h2>{{ tweet }}</h2>
    </div>
    
</template>

<script>
export default {
    props: {pribadi: Array},
    data() {
        return {
            isitweet:'',
        }
    },
    methods: {
        submit(){
            this.$emit('addtweet',this.isitweet)
        }
        
    }
/*         submit(){
            alert("terima kasih" + this.tweet.length);
        } */
        
    
}
</script>
<style>
.input{
    border-radius: 8px;
    padding: 10px;
    background-color: rgb(27, 145, 145);
    padding-bottom: 20px;
    align-content: center;
}
textarea {
    border-radius: 8px;
}
.input button {
    border-radius: 5px;
    font-size: 18px;
    padding: 4px;
    margin-right: 20px;
}
</style>