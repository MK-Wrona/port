<template xmlns="http://www.w3.org/1999/html">
  <div class="footer">
    <div class="footer__links">
      <a target="_blank" href="https://github.com/MK-Wrona">
        <img class="filter_green" src="/src/assets/github.svg"/>
      </a>
      <a target="_blank" href="https://www.linkedin.com/in/mara-krukovska-024565252/">
        <img class="filter_green" src="/src/assets/linkedin.svg"/>
      </a>
      <a href="/port/contacts/">
        <img class="filter_green" src="/src/assets/mail.svg"/>
      </a>
    </div>
    <div class="footer__copyright">
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
.footer__links {
  width:200px;
  display: flex;
  justify-content: space-evenly;
  padding:80px 0px 30px;
}
.filter_green {
  filter: invert(78%) sepia(84%) saturate(407%) hue-rotate(77deg) brightness(90%) contrast(91%);
  width: 37px;
  height: 37px;
}
.footer__copyright {
  padding:10px 0px 25px;
  display:flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
@media screen and (max-width: 500px) {
  .footer__links {
    padding:40px 0px 15px;
  }
}
</style>
