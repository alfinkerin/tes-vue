<template>
  <div>
    <paginate
      :page-count="20"
      :page-range="3"
      :margin-pages="2"
      :click-handler="clickCallback"
      :prev-text="'Prev'"
      :next-text="'Next'"
      :container-class="'pagination'"
      :page-class="'page-item'"
    >
    </paginate>
  </div>
</template>

<script>
import Paginate from "vuejs-paginate-next";
export default {
  components: {
    paginate: Paginate,
  },
  methods: {
    clickCallback(pageNum) {
      console.log(pageNum);
    },
  },
};
</script>

<style lang="css" scoped>
@import "https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css";
</style>
