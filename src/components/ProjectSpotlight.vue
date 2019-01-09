<template>
  <div id="project-spotlight">
    <div id="project-spotlight-title">{{ project.name }}</div>
    <div id="project-bullet-container">
      <div v-for="(bullet, index) in project.bullets" :key="index" class="project-bullet" v-html="bullet"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "project-spotlight",
  props: {
    project: {
      name: String,
      bullets: Array
    }
  }
};
</script>

<style>
#project-spotlight {
  border: 1px solid rgb(44, 62, 80);
  margin: 20px;
  padding: 10px 0 20px 0;
  -webkit-box-shadow: 1px 2px 1px 0px rgba(44, 62, 80, 0.6);
  -moz-box-shadow: 1px 2px 1px 0px rgba(44, 62, 80, 0.6);
  box-shadow: 1px 2px 1px 0px rgba(44, 62, 80, 0.6);
  align-content: center;
}

#project-spotlight-title {
  display: flex;
  justify-content: center;
  align-content: center;
  border-bottom: 1px solid gray;
  padding: 10px;
  margin: auto;
  width: fit-content;
  font-size: 1.2em;
}

#project-bullet-container {
  width: 80%;
  margin: 0 auto;
  text-align: left;
  padding: 0 20px;
}

.project-bullet {
  padding: 5px 0px;
}

.project-bullet::before {
  content: "- ";
}

.project-bullet:first-of-type {
  padding-top: 15px;
}
</style>
