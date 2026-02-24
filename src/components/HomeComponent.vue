<template>
  <div class="dizme_tm_section" id="home">
    <div class="dizme_tm_hero">
      <div
        class="background"
        :data-img-url="`/img/slider/${dark ? 'hero-dark' : 'hero-light'}.svg`"
      ></div>
      <div class="container">
        <div class="content">
          <div class="details">
            <div class="hello">
              <h3 class="orangeText">Hello, I'm</h3>
            </div>
            <div class="name">
              <h3>Ariful Islam</h3>
            </div>
            <div class="job">
              <p>
                A <span class="greenText">Software Engineer</span> focused on <span class="purpleText">DevOps & Web Apps</span>
              </p>
            </div>
            <div class="text">
              <p>
                I'm creative designer based in New York, and I'm very passionate
                and dedicated to my work.
              </p>
            </div>
            <div class="button">
              <div class="dizme_tm_button">
                <a class="anchor" href="#about"><span>About Me</span></a>
              </div>
              <div class="social">
                <ul>
                  <li>
                    <a href="https://github.com/Ariful-Islam-official" target="_blank" rel="noreferrer">
                      <i class="icon-github-1"></i>
                    </a>
                  </li>
                  <li>
                    <a href="https://www.linkedin.com/in/ariful-islam-devops-network" target="_blank" rel="noreferrer">
                      <i class="icon-linkedin-1"></i>
                    </a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="avatar">
            <div class="image">
              <img src="/img/slider/avatar.png" alt="" />
              <span
                class="skills illustrator anim_moveBottom"
                v-html="ai"
              ></span>
              <span class="skills photoshop anim_moveBottom" v-html="ps"></span>
              <span class="skills figma anim_moveBottom" v-html="figma"></span>
            </div>
          </div>
        </div>
      </div>
      <div class="dizme_tm_down">
        <a class="anchor" href="#process" v-html="dark ? mouseDark : mouse">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import { ai, figma, mouse, mouseDark, ps } from "../svg";
export default {
  name: "HomeComponent",
  data() {
    return { ai, ps, figma, mouse, mouseDark };
  },
  props: {
    dark: { type: Boolean },
  },
};
</script>
