<template>
  <div class="dizme_tm_section">
    <div class="dizme_tm_skills">
      <div class="container">
        <div class="wrapper">
          <div class="left">
            <div
              class="dizme_tm_main_title wow fadeInUp"
              data-wow-duration="1s"
              data-align="left"
            >
              <span>Skills</span>
              <h3>I Build, Automate, and Ship with Confidence</h3>
              <p>
                A practical mix of DevOps, backend development, and hands-on training experience. I focus on building reliable systems and shipping features fast.ing websites that work well on
                desktop is responsive and adaptive design
              </p>
            </div>
            <div class="dodo_progress wow fadeInUp" data-wow-duration="1s">
              <div
                class="progress_inner skillsInner___"
                data-value="88"
                data-color="#f75023"
              >
                <span
                  ><span class="label">DevOps & Cloud</span
                  ><span class="number">88%</span></span
                >
                <div class="background">
                  <div class="bar"><div class="bar_in"></div></div>
                </div>
              </div>
              <div
                class="progress_inner skillsInner___"
                data-value="95"
                data-color="#1cbe59"
              >
                <span
                  ><span class="label">Web App Development</span
                  ><span class="number">95%</span></span
                >
                <div class="background">
                  <div class="bar"><div class="bar_in"></div></div>
                </div>
              </div>
              <div
                class="progress_inner skillsInner___"
                data-value="75"
                data-color="#8067f0"
              >
                <span
                  ><span class="label">CI/CD & Automation</span
                  ><span class="number">75%</span></span
                >
                <div class="background">
                  <div class="bar"><div class="bar_in"></div></div>
                </div>
              </div>
            </div>
          </div>
          <div class="right">
            <img :src="`/img/skills/${dark ? 2 : 1}.jpg`" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SkillComponent",
  components: {},
  props: {
    dark: { type: Boolean },
  },
};
</script>
