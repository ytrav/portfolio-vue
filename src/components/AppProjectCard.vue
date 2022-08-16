<template>
  <div class="card">
    <div class="primg"></div>
    <div class="prinfo">
      <h3>{{ project.name }}</h3>
      <span>{{ project.year }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppProjectCard",
//   props: {
//     privateProjects: {
//       type: Array,
//       required: true,
//     },
//     workProjects: {
//       type: Array,
//       required: true,
//     },
//   },
};
</script>