<script>
import clients from "../../data/section/clients.json";
export default {
  name: "SectionClients",
  data() {
    return {
      clients: clients,
      hover: [],
    };
  },
  methods: {
    srcHover(i) {
      if (this.hover[i] == true) {
        return clients[i].hover;
      } else {
        return clients[i].path;
      }
    },
  },
  created() {
    this.clients.forEach((i) => this.hover.push(false));
  },
};
</script>

<template>
  <section id="ms_team" class="bg_light">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="row row-cols-3 row-cols-lg-5 g-5">
          <div class="col" v-for="(client, i) in clients">
            <a href="#"> <img :src="srcHover(i)" @mouseover="hover[i] = true" @mouseleave="hover[i] = false" alt="" /> </a>
          </div>
          <!-- /.col -->
        </div>
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_team -->
</template>
<style lang="scss" scoped>
#ms_team {
  padding-bottom: 8rem;
}
</style>
