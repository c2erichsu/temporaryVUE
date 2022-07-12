<template>
  <div class="float-right">
    <div v-for="item in paper" :key="item">
      <b-button variant="link">{{ item.college }}</b-button>
      
      <div v-for="element in item.data" :key="element">
        --{{ element }}學年度考古題
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PaperMenu",
  components: {},
  data() {
    return {
      paper: [
        {
          college: "國立台灣大學",
          data: [110, 109, 108, 107, 106, 105],
        },
        {
          college: "國立台北大學",
          data: [110, 109, 108, 107, 106, 105],
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>