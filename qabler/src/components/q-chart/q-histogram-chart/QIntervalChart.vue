<template>
  <div>
    <v-chart :forceFit="true" :height="height" :data="data">
      <v-tooltip />
      <v-axis />
      <v-bar position="x*y" />
    </v-chart>
  </div>
</template>

<script>
  const data = [
    { x: '分类一', y: [ 76, 100 ] },
    { x: '分类二', y: [ 56, 108 ] },
    { x: '分类三', y: [ 38, 129 ] },
    { x: '分类四', y: [ 58, 155 ] },
    { x: '分类五', y: [ 45, 120 ] },
    { x: '分类六', y: [ 23, 99 ] },
    { x: '分类七', y: [ 18, 56 ] },
    { x: '分类八', y: [ 18, 34 ] },
  ];

  export default {
    name: 'QIntervalChart',
    props: {
      data: {
        type: Array,
        default: function() {
          return data
        }
      },
      height: {
        type: Number,
        default: 300
      }
    },
  }
</script>

<style scoped>

</style>