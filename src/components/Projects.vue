<template>
  <div class="home_projects">
    <span>My Projects</span>
    <div class="home_projects-wrapper">
      <div class="project_wrapper">1</div>
      <div class="project_wrapper">2</div>
      <div class="project_wrapper">3</div>
      <div class="project_wrapper">4</div>
    </div>
  </div>
</template>

<style>
.home_projects {
  width:990px;
  display: grid;
  grid-template-columns: repeat(auto-fit, 1fr);
}
.home_projects-wrapper {
  width:100%;
}
.project_wrapper {
  display: flex;
  justify-content: center;
}
</style>
