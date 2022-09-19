<template>
  <div class="navbar">
    <div class="navbar-content">
      <div class="tittle" style="float: left">
        <h2>Simple Twitter Clone With Vue</h2>
      </div>
      <div class="profile" style="float:right">
        <img :src="poto" alt="">
      </div>
      <div class="user" style="float: right">
        <div class="nama-user">{{nama_user}}</div>
        <div class="username">{{ username }}</div>  
      </div>
    </div>
  </div>
</template>

<script>
export default {
  inject: ['nama_user','username','profile'],
  data(){
    return {
      poto:this.profile
    }
  }

};
</script>

<style>
* {
  margin: 0px auto;
  padding: 0px;
}
.navbar {
  height: 80px;
  max-width: 100%;
  background: rgb(130, 130, 255);
}
.navbar-content {
  text-align: right;
  align-content: center;
  margin: 0px 250px 250px;
  padding-top: 20px;
}
.tittle {
  color: rgb(0, 0, 0);
}
.nama-user {
  color: white;
}
.username {
  color: aqua;
}
.profile img {
  align-content: center;
  padding-left: 5px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
}
.user {
}
</style>