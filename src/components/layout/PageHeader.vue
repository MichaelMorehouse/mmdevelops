<template>
  <header>
    <img class="splash-image" src="../../assets/profile.png">
    <div class="header-text text-uppercase text-centered">Michael M Miller</div>
    <div id="header-icons">
      <font-awesome-icon :icon="['fas', 'code-branch']" size="2x"></font-awesome-icon>
      <div class="horizontal-row"></div>
      <font-awesome-icon :icon="['fas', 'chart-bar']" size="2x"></font-awesome-icon>
      <div class="horizontal-row"></div>
      <font-awesome-icon :icon="['fas', 'flask']" size="2x"></font-awesome-icon>
    </div>
  </header>
</template>

<script>
export default {
  name: "page-header"
};
</script>

<style>
header {
  background-color: rgba(45, 100, 45, 0.9);
  color: white;
  align-content: center;
  text-align: center;
}

#header-icons {
  display: flex;
  width: fit-content;
  margin: 0 auto;
  justify-content: center;
  padding: 10px 0;
}

.header-text {
  font-size: 1.6em;
  padding-top: 25px;
}

.splash-image {
  display: block;
  margin: auto;
  padding-top: 30px;
}

.horizontal-row {
  display: inline-block;
  vertical-align: middle;
  width: 30px;
  height: 2px;
  background-color: white;
  margin: auto 5px;
}

.svg-inline--fa {
  padding: 10px;
}
</style>
