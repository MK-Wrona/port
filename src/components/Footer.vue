<template xmlns="http://www.w3.org/1999/html">
  <div class="footer">
    <div class="footer_links">
      <a href="https://github.com/MK-Wrona">
        <img class="filter_green" src="/src/assets/github.svg"/>
      </a>
      <a href="https://www.linkedin.com/in/mara-krukovska-024565252/">
        <img class="filter_green" src="/src/assets/linkedin.svg"/>
      </a>
      <a href="/port/contacts/">
        <img class="filter_green" src="/src/assets/mail.svg"/>
      </a>
    </div>
    <div class="footer_copyright">
      <span>Mara Krukovska</span>
      <p>&copy; {{new Date().getFullYear()}}</p>
    </div>
  </div>
</template>

<style scoped>
.footer {
  width:100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.footer_links {
  width:200px;
  display: flex;
  justify-content: space-evenly;
  padding:100px 0px 35px;
}
.filter_green {
  filter: invert(78%) sepia(84%) saturate(407%) hue-rotate(77deg) brightness(90%) contrast(91%);
  width: 37px;
  height: 37px;
}
.footer_copyright {
  padding:10px 0px 25px;
  display:flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
