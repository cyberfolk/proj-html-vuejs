<script>
import ItemButton from "../item/ItemButton.vue";
export default {
  name: "SectionContact",
  components: { ItemButton },
};
</script>

<template>
  <section id="ms_contact" class="bg_light">
    <div class="ms_big_container">
      <div class="ms_medium_container">
        <div class="row row-cols-2 g-5">
          <div class="col">
            <div class="ms_map_container mt-5">
              <img class="ms_map" src="../../assets/img/section/contact/map.png" alt="" />
              <img class="ms_plus ms_1" src="../../assets/img/section/contact/plus.png" alt="" />
              <img class="ms_plus ms_2" src="../../assets/img/section/contact/plus.png" alt="" />
              <img class="ms_plus ms_3" src="../../assets/img/section/contact/plus.png" alt="" />
            </div>
          </div>
          <!-- /.col -->
          <div class="col">
            <h2>Contact us<span class="text_primary">.</span></h2>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Deleniti, non.</p>
            <div class="spacer mb-5"></div>
            <div class="d-flex gap-3 mb-4">
              <input type="text" class="form-control" placeholder="Your Name" />
              <input type="text" class="form-control" placeholder="Your Email" />
            </div>
            <textarea class="form-control mb-5" rows="3" placeholder="Write a message..."></textarea>
            <ItemButton :text="'SEND'" :color="'primary'" />
          </div>
          <!-- /.col -->
        </div>
        <!-- /.row -->
      </div>
      <!-- /.ms_medium_container -->
    </div>
    <!-- /.ms_big_container -->
  </section>
  <!-- /#ms_contact -->
</template>
<style lang="scss" scoped>
#ms_contact {
  padding: 8rem 0;

  .ms_map_container {
    position: relative;

    .ms_map {
      width: 100%;

    }

    .ms_plus {
      position: absolute;
      display: block;
    }

    .ms_1 {
      top: 35%;
      left: 24%;
    }

    .ms_2 {
      top: 22.5%;
      left: 52.5%;
    }

    .ms_3 {
      top: 72.5%;
      left: 85%;
    }
  }
}
</style>
