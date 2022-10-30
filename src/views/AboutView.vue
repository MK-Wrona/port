<template>
  <div class="about">
    <div>
    <h2>About me</h2>
    <p class="about_desc">Nisl arcu, scelerisque neque ut. Tincidunt amet, tempor duis tortor neque auctor dis ipsum. Pretium cras amet
      odio amet eleifend id sed cras sed. Aliquet risus posuere aliquet imperdiet sit.</p>
      <a href="" class="about_link">Resume</a>
  </div>
    <img class="about_pic" src="src/assets/copy.jpg">
  </div>
</template>

<style>
.about {
  width:100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.about_pic{
  width:400px;
  height:400px;
  border-radius: 50%;
}
.about_desc{
  width:50%;
  padding: 32px 0px 32px;

}
.about_link {
  border-radius: 5px;
  background-color: #3DDC84;
  text-decoration: none;
  border:none;
  font-weight: bold;
  padding: 10px 10px 10px;
  color:black;
}
.about_link:hover {
  border-radius: 5px;
  background-color: #202020;
  text-decoration: none;
  font-weight: bold;
  padding: 9px 9px 9px;
  color:white;
  border:1px solid white;
}
</style>
