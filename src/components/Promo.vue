<script setup>
</script>

<template>
  <div class="home__wrapper">
    <div class="home_text">
      <span class="highlight">Hi there, I'm Mara Krukovska</span>
      <p>Short text with details about you, what you do or your professional career. You can add more information on the about page.</p>
      <div class="home_button-holder">
        <button class="home_btn">Indeed</button>
        <button class="home_btn">LinkedIn</button>
      </div>
    </div>
    <img class="home__photo" src="../assets/photo_of_me_cut.jpg">
  </div>
</template>
<style>
.home__photo {
  width:200px;
  height:250px;
}
.home__wrapper {
  padding:54px 0px 54px;
  width:100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.highlight {
  font-size: 64px;
  font-weight: bold;
}
.home_text {
  width:480px;
}
.home_button-holder{
  width:50%;
  display: flex;
  justify-content: space-between;
}
.home_btn {
  background-color: cornflowerblue;
  border:none;
  font-weight: bold;
}
.home_btn:hover {
  color:white;
  cursor: pointer;
  background-color: #2c3e50;
}
</style>
