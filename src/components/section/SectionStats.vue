<script>
import stats from "../../data/section/stats.json";
import StatsBar from "../item/StatsBar.vue";
export default {
  name: "SectionStats",
  components: { StatsBar },
  data() {
    return { stats: stats };
  },
};
</script>

<template>
  <section id="ms_stats">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="row row-cols-2 g-5">
          <div class="col">
            <h3>Creative Leader<span class="text_primary">.</span></h3>
            <div class="spacer pb-3"></div>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Praesentium eveniet quae pariatur? Quisquam, a soluta! Excepturi, error velit. Impedit, quia accusantium? Aliquid, fuga amet? Aut alias repellat perspiciatis neque quaerat vitae velit, adipisci corrupti atque!</p>
            <span class="fs_08 fw-bold text_dark">READ MORE</span>
          </div>
          <!-- /.col -->
          <div class="col">
            <StatsBar v-for="s in stats" :name="s.name" :percentage="s.percentage" />
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_stats -->
</template>
<style lang="scss" scoped>
@use "../../assets/scss/partials/variables" as *;
.ms_big_container {
  padding: 8rem 0;
}
</style>
