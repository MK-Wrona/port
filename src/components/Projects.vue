<template>
  <div class="highlight_wrapper"><h2>My Projects</h2></div>
  <div class="home_projects">
  <div class="home_projects-wrapper">
    <div class="project_wrapper">
      <img src="src/assets/keyauto_pic.jpg" class="project_pic"/>
      <div class="project_desc">
        <span class="project_desc_highlight">Rolf.ru</span>
        <p class="project_desc_text">I created this personal project in order to show how to create an interface in Figma using a portfolio as an example.</p>
        <a href="https://www.rolf.ru/" class="project_link" >View Project</a>
      </div>
    </div>
    <div class="project_wrapper">
      <div class="project_desc">
        <span class="project_desc_highlight">Rolf.ru</span>
        <p class="project_desc_text">I created this personal project in order to show how to create an interface in Figma using a portfolio as an example.</p>
        <a href="https://www.rolf.ru/" class="project_link" >View Project</a>
      </div>
      <img src="src/assets/rolf_pic.jpg" class="project_pic"/>
    </div>
    <div class="project_wrapper">
      <img src="src/assets/keyauto_pic.jpg" class="project_pic"/>
      <div class="project_desc">
        <span class="project_desc_highlight">Rolf.ru</span>
        <p class="project_desc_text">I created this personal project in order to show how to create an interface in Figma using a portfolio as an example.</p>
        <a href="https://www.rolf.ru/" class="project_link" >View Project</a>
      </div>
    </div>
    <div class="project_wrapper">
      <div class="project_desc">
        <span class="project_desc_highlight">Rolf.ru</span>
        <p class="project_desc_text">I created this personal project in order to show how to create an interface in Figma using a portfolio as an example.</p>
        <a href="https://www.rolf.ru/" class="project_link" >View Project</a>
      </div>
      <img src="src/assets/rolf_pic.jpg" class="project_pic"/>
    </div>
  </div>
  </div>
</template>

<style>
.home_projects-wrapper {
  padding:20px 0px 20px;
  flex-direction: column;
  column-gap: 20px;
}
.home_projects {
  width:100%;
  display:flex;
  flex-direction: column;
  align-items: center;
}
.project_wrapper {
  justify-self: center;
  display: flex;
  width: 990px;
  flex-direction: row;
  border-radius: 20px;
  margin:30px 0px 30px;
}
.project_pic {
  width:50%;
  border-radius: 20px;
}
.project_desc_highlight {
  font-weight: normal;
  font-size: 30px;
}
.project_desc_text {
  padding:24px 0px 24px;
}

.highlight_wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.project_desc {
  width:50%;
  background-color: #2F2F2F;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding:0px 36px 0px;
  text-align: center;
  border-radius: 20px;
}
.project_link {
  border-radius: 5px;
  background-color: #3DDC84;
  text-decoration: none;
  border:none;
  font-weight: bold;
  padding: 10px 10px 10px;
  color:black;
}
.project_link:hover {
  border-radius: 5px;
  background-color: #202020;
  text-decoration: none;
  border:none;
  font-weight: bold;
  padding: 9px 9px 9px;
  color:white;
  border:1px solid white;
}
</style>
