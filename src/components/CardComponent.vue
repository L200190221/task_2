<template>
  <div class="card">
    <div class="content-card" style="float :left" v-for="(data,index) in tweets" :key="data">
        <div class="profile-card" style="float :left">
            <img :src="data.avatar" alt="">
        </div>
        <div class="nama-card" style="float :left">
            {{ data.nama_tweetcard}}
        </div>
        <div class="username-card" style="float :left">
            {{ data.username_card }}
        </div>
        <br>
        <div class="tweet">
            {{ data.tweet_card }}
        </div>
        <div class="icon">
            <div class="like" style="float:left" @click="clicklike(index),data.like=!data.like">
                like
                <p v-if="data.like"> 
                   {{ data.total_like +1}}
                </p> 
                <p v-else> 
                   {{ data.total_like }}
                </p> 
            </div>
            <div class="retweet" @click="data.total_retweet++">
                retweet
                {{ data.total_retweet }}
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {tweets: Array}, 
    methods: {
        clicklike(index){
            /* this.tweets[index].like=!this.tweets */
            console.log(this.tweets[index].total_retweet)
        },
    }
}
</script>

<style>

.content-card {
    background-color: bisque;
    min-width: 835px;
    padding: 1rem;
    border-radius: 1rem;
    margin-top: 20px;
}
.tweet {
    padding-top: 5px;
    margin-left: 60px;
}
.username-card {
    margin-left: 5px;
}
.profile-card img {
    margin-right: 10px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
}
.icon {
    padding-top: 5px;
    margin-left: 60px;
}
.like {
    padding-right: 10px;
}
</style>