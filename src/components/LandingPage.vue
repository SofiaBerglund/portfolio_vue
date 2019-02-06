<template>
  <div>
    <div class="landing-page-container">
      <div class="header-container">
        <div class="leftofheader-container">
          <div class="image-container">
            <img src="header-image.JPG" alt="portrait">
          </div>
          <div class="contact-info">
            <p>berglund.sofia@gmail.com</p>
            <p>073-650 84 80</p>
          </div>
        </div>
        <header>
          <p class="name-header">Sofia Berglund</p>
          <h1>FRONTEND DEVELOPER</h1>
          <p>
            Hi! I am a junior frontend developer with previous experience in
            accounting and biology. I love solving problems and writing
            beautiful code. I am a curious and creative perfectionist and a
            team player who love to share knowledge and to learn from
            others.
          </p>
          <a href="https://github.com/SofiaBerglund">
            <button>SEE MY GITHUB</button>
          </a>
        </header>
      </div>
      <div class="tech-summary">
        <h1>TECH</h1>
        <p>
          HTML5, CSS, SASS, Javascript, ES6, JSX, React, Vue.js, Node.js,
          API:s &bull; 6 sprints with demos together with companies like
          Volumental, Bonnier, Comprend and Svenska Spel @ Technigo &bull;
          Presently at Visual Art building templates in CMS systems for
          digital signage
        </p>
      </div>
      <div class="projects-container">
        <Project
          v-for="project in projects.projects"
          :key="project.id"
          :title="project.title"
          :image="project.image"
          :link="project.link"
        />
        <a href="https://github.com/SofiaBerglund/portfolio_vue">
          <p>(Portfolio built in Vue.js)</p>
        </a>
      </div>
      <div class="skills-container">
        <h1>SKILLS</h1>
        <div class="skills-content">
          <div>
            <h2>CODE</h2>
            <ul>
              <li>HTML5</li>
              <li>CSS</li>
              <li>JavaScript ES6</li>
              <li>React</li>
              <li>Vue.js</li>
              <li>SASS</li>
              <li>GitHub</li>
              <li>Node.js</li>
              <li>MongoDB</li>
            </ul>
          </div>
          <div>
            <h2>TOOLBOX</h2>
            <ul>
              <li>Visual Studio Code</li>
              <li>Atom</li>
              <li>Postman</li>
              <li>Microsoft Azure</li>
              <li>CMS systems</li>
              <li>Microsoft Dynamics NAV</li>
              <li>Palette</li>
              <li>Centsoft</li>
              <li>Visma Business</li>
            </ul>
          </div>
          <div>
            <h2>MORE</h2>
            <ul>
              <li>Team leader</li>
              <li>System administration</li>
              <li>Process development</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="studies-container">
        <h1>STUDIES</h1>
        <div class="studies-content">
          <h2>FRONTEND DEVELOPER</h2>
          <p>
            Technigo. Full-time 12 week boot camp / intensive program.
            Covering everything from the basics of programming to how to
            structure and build bigger web projects. Focus on JavaScript.
            Total 480 coding hours, 50+ individual tasks (in HTML5, CSS,
            SASS, JavaScript, JSX, React, Node.js) and 6 sprints with demos
            together with companies like Volumental, Bonnier, Comprend and
            Svenska Spel.
            <br>Stockholm Sept - Nov 2018
          </p>
          <h2>ACCOUNTING CONSULTANT</h2>
          <p>Frans Schartaus Handelsinstitut. Higher Vocational Education.
            <br>Stockholm 2011 - 2013
          </p>
          <h2>BIOLOGY</h2>
          <p>
            Stockholm University. Master’s biology program specializing in
            plant systematics.
            <br>Stockholm 2005 - 2011
          </p>
        </div>
      </div>

      <div>
        <a href="https://www.linkedin.com/in/sofia-berglund-b04344a7/">
          <button>SEE MY LINKEDIN</button>
        </a>
      </div>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Project from "./Project.vue";
import Footer from "./Footer.vue";
import projects from "../tech-projects.json";

export default {
  name: "LandingPage",
  components: {
    Project,
    Footer
  },
  data() {
    return {
      projects
    };
  }
};
</script>

<style lang="scss">
h1 {
  font-family: BigJohn, Futura, Arial;
  color: #000;
}
a {
  text-decoration: inherit;
  color: inherit;
}
button {
  padding: 10px 20px;
  margin-top: 20px;
  border: none;
  border-radius: 50px;
  font-family: BigJohn, Futura, Arial;
  font-size: 16px;
  color: #f6a623;
  background-color: #feeed7;
  cursor: pointer;
}
.landing-page-container {
  margin-bottom: 60px;
  padding: 0 250px;
  .header-container {
    width: 100%;
    display: flex;
    header {
      font-size: 16px;
      padding-left: 50px;
      .name-header {
        font-size: 20px;
        font-style: italic;
      }
    }
    .leftofheader-container {
      width: 80%;
      height: auto;
      p {
        margin: 0;
      }
      .image-container {
        width: 100%;
        img {
          width: 100%;
        }
      }
    }
  }
  .tech-summary p {
    font-style: italic;
  }
  .projects-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
  }
  .skills-container {
    width: 70%;
    .skills-content {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
    }
  }
}

@media (max-width: 1200px) {
  .landing-page-container {
    padding: 0 50px;
    .header-container {
      header {
        width: 80%;
        padding-left: 20px;
      }
      .leftofheader-container {
        width: 50%;
      }
    }
    .projects-container {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  }
}
@media (max-width: 450px) {
  .landing-page-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 10px;
    .header-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      header {
        width: 100%;
        padding-left: 0;
      }
      .leftofheader-container {
        width: 100%;
      }
    }
    .skills-container {
      width: 100%;
      .skills-content {
        display: flex;
        flex-direction: column;
      }
    }
  }
}
</style>