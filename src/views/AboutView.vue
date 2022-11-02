<template>
  <div class="about">
    <div class="about_desc-wrapper">
      <h2 class="about_highlight">About me</h2>
      <p class="about_desc">My name is Mara Krukovska. I'm a Web-developer of Ukrainian origin based in Toronto. I
        describe myself as a passionate developer who loves coding, open source, and the web platform .</p>
      <p class="about_desc">Aside from my job, I like to create and contribute to open source projects. That helps me to learn a ton of new
        stuff, grow as a developer and support other open source projects.<br/>
        In my free time you can find me participating in DND sessions, enjoying video games or playing basketball at the
        nearest gym.</p>
      <a href="https://drive.google.com/file/d/1QnewSrliEfcUjx2tYgKT9Z0EZoUaT--q/view?usp=share_link"
         class="about_link">Resume</a>
    </div>
    <img class="about_pic" src="/src/assets/copy.jpg">
  </div>
</template>

<style>
.about {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding-top: 10px;
}
.about_desc-wrapper {
  display: flex;
  flex-direction: column;
}

.about_pic {
  width: 400px;
  height: 400px;
  border-radius: 50%;
  margin-right: 30px;
}

.about_desc {
  width: 600px;
  padding: 32px 0px 18px;
}

.about_link {
  border-radius: 5px;
  background-color: #3DDC84;
  text-decoration: none;
  border: none;
  font-weight: bold;
  padding: 10px 10px 10px;
  color: black;
  width:76px;
}

.about_link:hover {
  border-radius: 5px;
  background-color: #202020;
  text-decoration: none;
  font-weight: bold;
  padding: 9px 9px 9px;
  color: white;
  border: 1px solid white;
}
@media screen and (max-width: 1024px){
  .about {
    flex-direction: column-reverse;
  }
  .about_highlight {
    text-align: center;
    max-width: 100%;
    padding-top: 15px;
  }
  .about_link{
    align-self: end;
  }
  .about_pic {
    margin-right: 0px;
  }
}
@media screen and (max-width: 720px) {
  .about_pic {
    width: 240px;
    height: 240px;
  }

  .about_desc {
    width: 340px;
    text-align: center;
  }
}
@media screen and (max-width: 426px) {
  .about_pic {
    width: 220px;
    height: 220px;
  }

  .about_desc {
    width: 260px;
  }
  .about_link{
    align-self: center;
  }
}
</style>
