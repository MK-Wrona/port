<template>
  <div class="highlight_wrapper"><h2>My Projects</h2></div>
  <div class="home_projects">
    <div class="home_projects-wrapper">
      <div class="project_wrapper">
        <img src="/src/assets/keyauto_pic.jpg" class="project_pic"/>
        <div class="project_desc">
          <span class="project_desc_highlight">Keyauto.ru</span>
          <ul class="project_desc_text">
            <li class="project_desc_list">Involved in writing application-level code to interact with APIs, Web Services
              using AJAX, JSON and XML.
            </li>
            <li class="project_desc_list">Developed multiple POCs to write JavaScript code to create an interactive user
              interface.
            </li>
            <li class="project_desc_list">Created configurable and reusable components using VueJS, using life cycle methods, DOM event handling.
            </li>
          </ul>
          <a href="https://keyauto.ru/" class="project_link">View Project</a>
        </div>
      </div>
      <div class="project_wrapper">
        <div class="project_desc">
          <span class="project_desc_highlight">Rolf.ru</span>
          <ul class="project_desc_text">
            <li class="project_desc_list">Developed the User Interactive webpages using web  HTML/HTML5, and CSS3, JavaScript, jQuery, PHP, Tailwind, AJAX as per company standards.
            </li>
            <li class="project_desc_list">Developed multiple screens for Mobile Browsers such as Safari, Chrome, Opera
              to support the screen Compatibility and Resolution.
            </li>
          </ul>
          <a href="https://www.rolf.ru/" class="project_link">View Project</a>
        </div>
        <img src="/src/assets/rolf_pic.jpg" class="project_pic"/>
      </div>
      <div class="project_wrapper">
        <img src="/src/assets/keylite_pic.png" class="project_pic"/>
        <div class="project_desc">
          <span class="project_desc_highlight">Keyauto-lite.ru</span>
          <ul class="project_desc_text">
            <li class="project_desc_list">Delivered the best design aesthetics under tight deadlines.
            </li>
            <li class="project_desc_list">Called the Restful web service calls for POST, PUT, DELETE and GET methods.
            </li>
            <li class="project_desc_list">Troubleshooted and investigated issues with existing software applications.
            </li>
          </ul>
          <a href="https://keyauto-lite.ru/" class="project_link">View Project</a>
        </div>
      </div>
      <div class="project_wrapper">
        <div class="project_desc">
          <span class="project_desc_highlight">Luidor-expert</span>
          <ul class="project_desc_text">
            <li class="project_desc_list">Developed and configured application's backend using Laravel, Guzzle, AJAX.
            </li>
            <li class="project_desc_list">Developed server-side application to interact with database.
            </li>
            <li class="project_desc_list">
              Systematized and organized all the data used in the application using Laravel migrations and MySQL.
            </li>
          </ul>
          <a href="https://luidor-expert.ru/" class="project_link">View Project</a>
        </div>
        <img src="/src/assets/luidor_pic.jpg" class="project_pic"/>
      </div>
      <div class="project_wrapper">
        <img src="/src/assets/landing_pic.png" class="project_pic"/>
        <div class="project_desc">
          <span class="project_desc_highlight">Russian Travel</span>
          <ul class="project_desc_text">
            <li class="project_desc_list">Designed landing pages using HTML5, CSS3, and JavaScript.
            </li>
            <li class="project_desc_list">Demonstrated experience in managing maintainable, scalable, cross-browser code that is a delight to experience on any device.
            </li>
            <li class="project_desc_list">Audited and debugged  sites to ensure it is consistent and is responsive on all devices.
            </li>
          </ul>
          <a href="https://mk-wrona.github.io/russian-travel/" class="project_link">View Project</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.home_projects-wrapper {
  padding: 20px 0px 20px;
  flex-direction: column;
  column-gap: 20px;
}

.home_projects {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.project_wrapper {
  justify-self: center;
  display: flex;
  width: 990px;
  flex-direction: row;
  border-radius: 20px;
  margin: 30px 0px 30px;
}

.project_pic {
  width: 50%;
  border-radius: 20px;
}

.project_desc_highlight {
  font-weight: normal;
  font-size: 30px;
}

.project_desc_text {
  padding: 24px 0px 24px;
}

.highlight_wrapper {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.project_desc {
  width: 50%;
  background-color: #2F2F2F;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 0px 36px 10px;
  text-align: center;
  border-radius: 20px;
}

.project_desc_list {
  list-style-type: disc;
  padding-bottom: 7px;
}

.project_link {
  border-radius: 5px;
  background-color: #3DDC84;
  text-decoration: none;
  border: none;
  font-weight: bold;
  padding: 10px 10px 10px;
  color: black;
}

.project_link:hover {
  border-radius: 5px;
  background-color: #202020;
  text-decoration: none;
  border: none;
  font-weight: bold;
  padding: 9px 9px 9px;
  color: white;
  border: 1px solid white;
}
</style>
