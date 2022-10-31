<script setup>
</script>

<template>
  <div class="home__wrapper">
    <div class="promo_text">
      <span class="promo_prof">WEB-DEVELOPER</span>
      <span class="promo_highlight">Hello, my name is Mara Krukovska</span>
      <p class="promo_desc">Hardworking and highly motivated individual who is striving to obtain a challenging position in a highly regarded company where one can demonstrate extensive knowledge towards the company's growth and profitability.</p>
      <div class="home_button-holder">
        <a href="https://www.linkedin.com/in/mara-krukovska-024565252/" class="home_btn">LinkedIn</a>
        <a href="https://drive.google.com/file/d/1QnewSrliEfcUjx2tYgKT9Z0EZoUaT--q/view?usp=sharing" class="home_btn">Resume</a>
      </div>
    </div>
    <img class="home__photo" src="../assets/photo_of_me_cut.jpg">
  </div>
</template>
<style>
.home__photo {
  border-radius: 50%;
  width:500px;
  height:500px;
}
.home__wrapper {
  padding:40px 0px 65px;
  width:100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.promo_prof{
  color: #3DDC84;
  font-weight: bold;
  padding-bottom: 20px;
}
.promo_highlight {
  font-size: 64px;
  font-weight: 500;
  line-height: 76px;
}
.promo_desc {
  padding: 32px 0px 32px;
}
.promo_text {
  width:550px;
  display: flex;
  flex-direction: column;
  padding-top: 50px;
}
.home_button-holder {
  width:40%;
  display: flex;
  justify-content: space-between;
}
.home_btn {
  background-color: #3DDC84;
  border:none;
  font-weight: bold;
  border-radius: 10px;
  padding: 10px 10px 10px;
  text-decoration: none;
  color:black;
}
.home_btn:hover {
  color:white;
  cursor: pointer;
  background-color: #2F2F2F;
  border: 1px solid white;
  border-radius: 10px;
  padding: 9px 9px 9px;
}
</style>
