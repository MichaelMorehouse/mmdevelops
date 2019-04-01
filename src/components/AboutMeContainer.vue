<template>
  <div id="about-me">
    <h2 id="about-title" class="text-uppercase">About Me</h2>
    <div id="about-content" class="about-grid">
      <div class="col-one">
        <p>
          <span class="leadin-text">&emsp;&emsp;Hello there, I'm Michael!</span>
          As a Pacific Northwest native, I graduated cum laude from Western Washington University with a BS in Biochemistry. Upon returning to the Portland area I worked as an analytical chemist in QC and environmental testing laboratories. Being successful in such work requires efficient time management, team communication, and a dedication to doing the job well.
        </p>
        <p>
           &emsp;&emsp;I was introduced to programming through a position developing analytical testing methods. We had adopted an SQL database based program to manage, analyse and report our data. After diving into SQL so that I could successfully develop and validate our laboratories methods, I discovered a interest in programming, and continued learning SQL and JavaScript independently for a time. My interest continued to grow, and it led me to explore options for a career change. Attending a local accelerated programming school was a good option; I attended the Tech Academy in Portland in 2018.
        </p>
      </div>
      <div class="col-two">
        <p>
          &emsp;&emsp;My focus is C# and .NET development, and Javascript, including Node and the frontend frameworks React and Vue. I have a firm grasp of object oriented programming principles and additional experience in C++ and Java. As a scientist I enjoy data analysis and effectively presenting data and information and am excited to combine that passion with software development. I am a lifelong learner who is comfortable working independently but prefers working in small teams. An effective team environment promotes sharing of knowledge and expertise and collaborative problem solving to the benefit of everyone. I enjoy building, being a part of, and leading such teams.
        </p>
        <p>&emsp;&emsp;On top of all that, I love to cook, and would be a welcome addition to any office potluck!</p>
        <p>Let's talk more about my fit with your team. Email me or contact me via the methods below.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#about-me {
  padding: 20px 10%;
  color: rgb(44, 62, 80);
}
#about-title {
  text-align: center;
}

#about-content {
  text-align: left;
}

.leadin-text {
  font-size: 1.2em;
}

.col-one {
  grid-area: colone;
  border-right: 1px rgb(44, 62, 80, 0.5) solid;
}
.col-two {
  grid-area: coltwo;
}

.about-grid {
  display: grid;
  grid-auto-columns: auto auto;
  grid-template-areas: "colone coltwo";
}

.about-grid > div {
  padding: 0px 20px;
}
</style>
