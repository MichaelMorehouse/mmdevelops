<template>
  <div id="projects">
    <h2 class="projects-title text-uppercase">Projects</h2>
    <div id="project-grid">
      <project-item
        v-for="(project, index) in projects"
        v-bind:key="index"
        :class="'project' + (index + 1)"
        :project="project"
        :isActive="project == activeProject"
        v-on:activate-project="activateProject(project)"
      />
    </div>
    <scroll-anchor id="project-anchor" top="0" left="0"/>
    <transition name="fade">
      <project-spotlight v-if="projectsExist()" :project="activeProject"></project-spotlight>
    </transition>
  </div>
</template>

<script>
import ProjectItem from "./ProjectItem.vue";
import ProjectSpotlight from "./ProjectSpotlight.vue";
import ScrollAnchor from "./ui/ScrollAnchor.vue";

export default {
  name: "project-container",
  components: {
    ProjectItem,
    ProjectSpotlight,
    ScrollAnchor
  },
  data: function() {
    return {
      activeProject: "",
      projects: [
        {
          name: "PDXPrivacy Website - HTML/CSS",
          bullets: [
            "Home on the web for a Portland-area privacy activism group",
            "Site purposefully built entirely without scripting - HTML/CSS only",
            "<a href='http://pdxprivacy.mmdevelops.com' target='_blank'>Visit the site</a>"
          ],
          icon: "pdxp.png"
        },
        {
          name: "MushBox - Arduino/Node",
          bullets: [
            "Controlled environment for growing edible mushrooms at home",
            "Temperature and humidity monitored and controlled by an Arduino microcontroller with C++ firmware. <a href='https://github.com/MichaelMorehouse/MushBox-firmware' target='_blank'>View code at Github</a>",
            "A NodeJS web API logs environment data posted by microcontroller to a PostgreSQL database. <a href='https://github.com/MichaelMorehouse/MushBox-api' target='_blank'>View code at Github</a>"
          ],
          icon: "mush.png"
        }
      ]
    };
  },
  methods: {
    projectsExist: function() {
      if (this.activeProject == "" && this.projects[0]) {
        this.activeProject = this.projects[0];
      }
      return this.activeProject ? true : false;
    },
    activateProject: function(project) {
      this.activeProject = project;
      document.getElementById("project-anchor").scrollIntoView();
    }
  }
};
</script>

<style>
#projects {
  position: relative;
  color: rgb(44, 62, 80);
  text-align: center;
  padding: 20px 25%;
}

project-spotlight {
  grid-area: project-spotlight;
}

.project1 {
  grid-area: projectone;
}
.project2 {
  grid-area: projecttwo;
}

@media screen {
  #project-grid {
    display: grid;
    grid-template-columns: auto auto;
    gap: 20px;
    justify-content: space-evenly;
    grid-template-areas: "projectone projecttwo";
  }
}
</style>
