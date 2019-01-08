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
        v-on:activate-project="activeProject = project"
      />
    </div>
    <transition name="fade">
      <project-spotlight v-if="projectsExist()" :project="activeProject"></project-spotlight>
    </transition>
    <scroll-anchor id="project-anchor" top="-100" left="0"/>
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
            "Site purposefully built entirely without scripting - HTML/CSS only"
          ],
          icon: "pdxp.png"
        },
        {
          name: "MushBox - Arduino/Node",
          bullets: [
            "Controlled environment for growing edible mushrooms at home",
            "Temperature and humidity monitored and controlled by an Arduino microcontroller with C++ firmware",
            "A NodeJS web API logs environment data posted by microcontroller to a PostgreSQL database"
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
    }
  },
  watch: {
    activeSkill: function() {
      console.log("frrrrt");
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
