<template>
  <v-row class="main font">
    <v-row class="section">
      <v-col cols="12" xl="12" lg="12" md="12" sm="6" class="about">
        <p class="">
          Hello I'm <b class="name">Shubham</b>. A software engineer based in
          Mumbai, India. Currently working at
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
          Javascript, Typescript, NodeJs, HTML, CSS, SCSS, C, C++, Python,
          Hindi, English
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
          <span class="tooltip"
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
$background: #e0e0e0;
$secondary: salmon;
.main {
  padding: 5% 1% 0% 5%;
  -webkit-user-select: none; /* Safari */
  -ms-user-select: none; /* IE 10 and IE 11 */
  user-select: none; /* Standard syntax */
  font-weight: bold;
  @media (max-width: 500px) {
    padding: 5% 5% 0% 5%;
    text-align: center;
  }
  .about p {
    font-size: 4rem;
    // overflow: hidden;
    span {
      cursor: pointer;
      transition: 0.3s;
    }
    .react {
      &:hover {
        color: #1bd1f7;
      }
    }
    .vue {
      &:hover {
        color: #3fb27f;
      }
    }
    .typescript {
      &:hover {
        color: #2e74c0;
      }
    }
    .javascript {
      &:hover {
        color: #ceb330;
      }
    }
    .credilio {
      &:hover {
        color: #26479b;
      }
    }
    .name {
      cursor: pointer;
      &:hover {
        color: $secondary;
      }
    }
    .design-system {
      &:hover {
        background: linear-gradient(to right, #ff4a4a, #00aaff 70%);
        background-clip: text;
        -webkit-text-fill-color: transparent;
      }
    }

    @media (max-width: 500px) {
      font-size: 1.5rem;
      padding: 0 0 0 0;
    }
  }
  .skills,
  .social {
    font-size: 4rem;
    @media (max-width: 500px) {
      font-size: 1.5rem;
    }
  }
  .social {
    cursor: pointer;
  }
  .project {
    font-size: 4rem;
    cursor: pointer;
    &:hover {
      @media (min-width: 700px) {
        letter-spacing: 5px;
      }
    }
    @media (max-width: 500px) {
      font-size: 1.5rem;
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
  font-size: 1.5rem;
  letter-spacing: 2px;
  padding: 10px 30px;
  opacity: 1;
  font-weight: bold;
  @media (max-width: 500px) {
    padding: 5px 10px;
  }
}
h1 {
  font-size: 1.4rem;
  font-weight: bold;
  transition-duration: 0.3s;
  @media (min-width: 700px) {
    &:hover {
      font-weight: bold;
      letter-spacing: 5px;
      cursor: pointer;
    }
  }
}
@mixin shadow($color, $steps, $glow) {
  $all: ();
  $all: append($all, -1px 1px 0 rgba($color, 0.1), comma);
  $all: append($all, 1px -1px 0 rgba($glow, 0.1), comma);
  $all: append($all, 1px -1px 150px $glow, comma);
  @for $i from 1 through $steps {
    $all: append(
      $all,
      append($i * -1px $i * 1.9px $i * 1px, rgba($color, 4 / $i))
    );
  }
  text-shadow: $all;
}

.font,
.font span {
  transition: 0.2s;
}

.font {
  color: $background;
  @include shadow(darken($background, 20%), 25, white);
}
</style>