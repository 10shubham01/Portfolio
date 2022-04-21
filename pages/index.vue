<template>
  <v-row class="main">
    <v-row class="section">
      <v-col cols="12" xl="12" lg="12" md="12" sm="6" class="about">
        <p>
          Hello I'm <b style="color: red">Shubham</b>. A software engineer based
          in Mumbai, India. Currently working at
          <span class="credilio">
            Credilio Financial Technologies Private Limited
          </span>
          as Software Engineer. I specialise in creating interactive experiences
          and functional interfaces using
          <b>
            <span class="vue"> Vue</span>, <span class="react"> React</span>,
            <span class="typescript"> Typescript</span>,
            <span class="javascript"> JavaScript</span>
          </b>
          and <b> <span class="design-system"> Design Systems</span> </b>.
        </p>
      </v-col>
    </v-row>
    <v-row class="section">
      <v-col cols="12" xl="12" lg="12" md="12" sm="6">
        <h1>CAN SPEAK AND UNDERSTAND</h1>
        <p class="skills">
          Javascript, Typescript, NodeJs, HTML, CSS, SCSS, C, C++, Python
        </p>
      </v-col>
    </v-row>
    <v-row class="section">
      <v-col cols="12" xl="12" lg="12" md="12" sm="6">
        <h1>SELECTED PROJECTS</h1>

        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <span class="project" v-bind="attrs" v-on="on">
              Marvel Heros,
            </span>
          </template>
          <span class="project"
            >React, Bootstrap, CSS Modules, Marvel REST API</span
          >
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <span class="project" v-bind="attrs" v-on="on"> Tello Clone, </span>
          </template>
          <span class="tooltip"
            >React, Material ui , CSS Modules , Trello API</span
          >
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <span class="project" v-bind="attrs" v-on="on"> Memory Game, </span>
          </template>
          <span class="tooltip">HTML, CSS, Vanilla Javascript</span>
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <span class="project" v-bind="attrs" v-on="on"> Easy Bank, </span>
          </template>
          <span class="tooltip">HTML, CSS, Vanilla Javascript</span>
        </v-tooltip>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <span class="project" v-bind="attrs" v-on="on">
              Marvel REST API
            </span>
          </template>
          <span class="tooltip"
            >NodeJs, ExpressJS,PostgresSQL, Sequelize ORM</span
          >
        </v-tooltip>
      </v-col>
    </v-row>
    <v-row class="section">
      <v-col cols="12" xl="12" lg="12" md="12" sm="6">
        <h1>SOCIAL</h1>
        <div class="d-flex flex-column social">
          <span>Send me an Email</span>
          <span>Tweet me something</span>
          <span>Check my Github</span>
          <span>Get in touch on LinkedIn</span>
        </div>
      </v-col>
    </v-row>
  </v-row>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
<style scoped lang="scss">
.main {
  padding: 5% 1% 0% 5%;
  @media (max-width: 500px) {
    padding: 5% 5% 0% 5%;
  }
  .about p {
    font-size: 4rem;
    overflow: hidden;
    span {
      cursor: pointer;
    }
    .react {
      color: #1bd1f7;
    }
    .vue {
      color: #3fb27f;
    }
    .typescript {
      color: #2e74c0;
    }
    .javascript {
      color: #ceb330;
    }
    .credilio {
      color: #26479b;
    }
    .design-system {
      background: linear-gradient(to right, #ff4a4a, #00aaff 70%);
      background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    @media (max-width: 500px) {
      font-size: 1rem;
      padding: 0 0 0 0;
    }
  }
  .skills,
  .social {
    font-size: 4rem;
    @media (max-width: 500px) {
      font-size: 1rem;
    }
  }
  .social {
    cursor: pointer;
  }
  .project {
    font-size: 4rem;
    cursor: pointer;
    @media (max-width: 500px) {
      font-size: 1rem;
    }
  }
  .section {
    margin-bottom: 5%;
    @media (max-width: 500px) {
      margin-bottom: 0%;
    }
  }
}
.v-tooltip__content {
  background: #ffffff;
  color: #000000;
  font-size: 1rem;
  padding: 10px 30px;
  opacity: 1;
  font-weight: bold;
  @media (max-width: 500px) {
    padding: 5px 10px;
  }
}
h1 {
  font-size: 1.4rem;
  font-weight: normal;
  transition-duration: 0.3s;
  &:hover {
    font-weight: bold;
    letter-spacing: 5px;
    cursor: pointer;
  }
}
</style>