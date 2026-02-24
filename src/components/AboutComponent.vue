<template>
  <div class="dizme_tm_section" id="about">
    <div class="dizme_tm_about">
      <div class="container">
        <div class="wrapper">
          <div class="left">
            <div class="image">
              <img :src="`/img/about/${dark ? 2 : 1}.jpg`" alt="" />
              <div class="numbers year">
                <div class="wrapper">
                  <h3>
                    <VueJsCounter end="3"></VueJsCounter>
                  </h3>
                  <span class="name">Years of<br />Experience</span>
                </div>
              </div>
              <div class="numbers project">
                <div class="wrapper">
                  <h3 style="display: flex">
                    <VueJsCounter as="span" end="20"></VueJsCounter>K
                  </h3>
                  <span class="name">Projects<br />Built</span>
                </div>
              </div>
            </div>
          </div>
          <div class="right">
            <div class="title wow fadeInUp" data-wow-duration="1s">
              <span>I'm a Software Engineer</span>
              <h3>I Build Reliable Systems & Web Apps</h3>
            </div>
            <div class="text wow fadeInUp" data-wow-duration="1s">
              <p>
                Hello! I'm Ariful Islam, a Software Engineer focused on DevOps, cloud infrastructure, and web application development. I enjoy automating deployments, designing scalable architectures, and building clean, maintainable products that solve real problems.
              </p>
            </div>
            <div class="dizme_tm_button wow fadeInUp" data-wow-duration="1s">
              <a class="anchor" href="#contact"><span>Let's Talk</span></a>
            </div>
          </div>
        </div>
      </div>
      <div class="brush_1 wow fadeInLeft" data-wow-duration="1s">
        <img src="/img/brushes/about/1.png" alt="" />
      </div>
      <div class="brush_2 wow fadeInRight" data-wow-duration="1s">
        <img src="/img/brushes/about/2.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
import VueJsCounter from "vue-js-counter";
export default {
  name: "AboutComponent",
  components: { VueJsCounter },
  props: {
    dark: { type: Boolean },
  },
};
</script>
