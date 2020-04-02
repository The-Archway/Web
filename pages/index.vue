<template>
  <div>
    <section class="banner">
      <img src="images/pexels-photo-241544.jpeg" />
    </section>
    <b-container>
      <b-row>
        <b-col>
          <logo />
          <div class="heading">
            <h1 class="title">The Archway</h1>
            <h4 class="subtitle">An open source project designed to help the average investor</h4>
            <div class="links">
              <b-button
                href="https://github.com/The-Archway"
                target="_blank"
                variant="secondary"
              >GitHub</b-button>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";

export default {
  components: {
    Logo
  }
};
</script>
<style>
.banner {
  display: flex;
}
.banner img {
  position: absolute;
  width: 100%;
}
.title,
.subtitle {
  color: #fff;
  background-color: rgba(0, 0, 0, 0.5);
  margin: 0px;
}
.heading,
.links {
  margin: 30px 0;
}
.row {
  margin: 30px 0px;
}
</style>
