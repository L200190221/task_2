<template>
    <form @submit="submit">
        <div class="input">
            <textarea rows="4" cols="110" placeholder="write something" v-model="tweet"></textarea>
            <div class="button">
                <button style="float: right" :disabled="tweet.length > 10 ? true : false">submit</button>
            </div>
            <div class="footer">
                <p>{{ tweet.length + "/10" }}</p>
            </div>
        </div>    
    </form>
</template>

<script>
export default {
    data() {
        return {
            tweet: '',
        }
    },
    methods : {
        submit(){
            alert("terima kasih" + this.tweet.length);
        }
        
    }
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