<template>
  <div class="home">
    <navbar-component />
    <div class="main">
      <div class="inputcard">
        <input-component />
      </div>
      <h2>Feeds</h2>
      <div class="feeds">
        <card-component :tweets="tweet" />
      </div>
    </div>
  </div>
</template>
<script>
import NavbarComponent from "./components/NavbarComponent.vue";
import CardComponent from "./components/CardComponent.vue";
import InputComponent from "./components/InputComponent.vue"
import gambar from "./assets/profil_1.jpeg"
export default {
  components: {
    NavbarComponent,CardComponent,InputComponent
  },
  data(){
    return {
      tweet: [
        {
          id:'1',
          username_card:'@userpertama', 
          nama_tweetcard:"Nama Pertama",
          tweet_card:"wide strong closer upper house strip equally oil stock book pure blood ",
          avatar:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQTMibLqRBcNCrlCcJuZ2uW7V1yC3lJD2bdGg&usqp=CAU",
          total_retweet:8,
          total_like:2,
        },
        {
          id:'2',
          username_card:"@Userkedua",
          nama_tweetcard:"Nama Kedua",
          tweet_card:"eager tomorrow anyway summer whale floor dark explore tip become sat improve loose greatly principle dried first health silk watch social wonder quietly thou",
          avatar:"https://cdn.myanimelist.net/images/characters/9/310307.jpg",
          total_retweet:10,
          total_like:5,
        }
      ]
    }
  },
  provide(){
    return {
      nama_user: 'muhammad mubarok',
      username: '@awok',
      profile: gambar
    }
  },
  methods: {
    plus(){
      this.total_retweet++
    }
  }
};
</script>

<style>
.main {
  align-content: center;
  margin: 0px 250px 250px;
  padding-top: 20px;
}
</style>