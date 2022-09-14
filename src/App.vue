<template>
  <div class="home">
    <navbar-component />
    <div class="main">
      <div class="feeds">
        <h2>Feeds</h2>
      </div>
    </div>
  </div>
</template>

<script>
import NavbarComponent from "./components/NavbarComponent.vue";
import gambar from "./assets/profil_1.jpeg"
export default {
  components: {
    NavbarComponent,
  },
  provide(){
    return {
      nama_user: 'muhammad mubarok',
      username: '@awok',
      profile: gambar
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