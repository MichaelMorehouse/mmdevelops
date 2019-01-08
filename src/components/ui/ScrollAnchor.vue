<template>
  <div :id="id" class="scroll-anchor" :style="{ top: top + 'px', left: left + 'px' }"></div>
</template>

<script>
export default {
  name: "scroll-anchor",
  props: {
    id: String,
    top: Number,
    left: Number
  }
};
</script>

<style>
.scroll-anchor {
  position: absolute;
}
</style>
