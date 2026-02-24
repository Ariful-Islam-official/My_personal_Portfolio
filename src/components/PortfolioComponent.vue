<template>
  <div class="dizme_tm_section" id="portfolio">
    <div class="dizme_tm_portfolio">
      <div class="container">
        <div class="dizme_tm_main_title" data-align="center">
          <span>Portfolio</span>
          <h3>My Amazing Works</h3>
          <p>
            A selection of recent work across DevOps, web applications, and automation. (Project descriptions are placeholder text for now.)
          </p>
        </div>
        <div class="portfolio_filter">
          <ul>
            <li>
              <a
                class="c-pointer"
                :class="activeNav === '1' ? 'current' : ''"
                @click.prevent="() => (this.activeNav = '1')"
                data-filter="*"
                >All</a
              >
            </li>
            <li>
              <a
                class="c-pointer"
                :class="activeNav === '2' ? 'current' : ''"
                @click.prevent="() => (this.activeNav = '2')"
                data-filter=".youtube"
                >DevOps</a
              >
            </li>
            <li>
              <a
                class="c-pointer"
                :class="activeNav === '3' ? 'current' : ''"
                @click.prevent="() => (this.activeNav = '3')"
                data-filter=".vimeo"
                >Web Apps</a
              >
            </li>
            <li>
              <a
                class="c-pointer"
                :class="activeNav === '4' ? 'current' : ''"
                @click.prevent="() => (this.activeNav = '4')"
                data-filter=".soundcloud"
                >Automation</a
              >
            </li>
            <li>
              <a
                class="c-pointer"
                :class="activeNav === '5' ? 'current' : ''"
                @click.prevent="() => (this.activeNav = '5')"
                data-filter=".popup"
                >Training</a
              >
            </li>
            <li>
              <a
                class="c-pointer"
                :class="activeNav === '6' ? 'current' : ''"
                @click.prevent="() => (this.activeNav = '6')"
                data-filter=".detail"
                >Detail</a
              >
            </li>
          </ul>
        </div>
        <div class="dizme_tm_portfolio_titles"></div>
        <div class="portfolio_list wow fadeInUp" data-wow-duration="1s">
          
          <ul class="gallery_zoom grid">
            <li class="youtube grid-item">
              <div class="inner">
                <div class="entry dizme_tm_portfolio_animation_wrap" data-title="CI/CD Pipeline Automation" data-category="DevOps">
                  <a href="#" @click.prevent="() => onClick('img', '/img/portfolio/1.jpg')">
                    <img src="/img/thumbs/42-56.jpg" alt="" />
                    <div class="main" data-img-url="/img/portfolio/1.jpg"></div>
                  </a>
                </div>
                <div class="mobile_title">
                  <h3>CI/CD Pipeline Automation</h3>
                  <span>DevOps</span>
                </div>
              </div>
            </li>

            <li class="youtube grid-item">
              <div class="inner">
                <div class="entry dizme_tm_portfolio_animation_wrap" data-title="Kubernetes Deployment Setup" data-category="DevOps">
                  <a href="#" @click.prevent="() => onClick('img', '/img/portfolio/2.jpg')">
                    <img src="/img/thumbs/42-56.jpg" alt="" />
                    <div class="main" data-img-url="/img/portfolio/2.jpg"></div>
                  </a>
                </div>
                <div class="mobile_title">
                  <h3>Kubernetes Deployment Setup</h3>
                  <span>DevOps</span>
                </div>
              </div>
            </li>

            <li class="vimeo grid-item">
              <div class="inner">
                <div class="entry dizme_tm_portfolio_animation_wrap" data-title="Django Web Application" data-category="Web Apps">
                  <a href="#" @click.prevent="() => onClick('img', '/img/portfolio/3.jpg')">
                    <img src="/img/thumbs/42-56.jpg" alt="" />
                    <div class="main" data-img-url="/img/portfolio/3.jpg"></div>
                  </a>
                </div>
                <div class="mobile_title">
                  <h3>Django Web Application</h3>
                  <span>Web Apps</span>
                </div>
              </div>
            </li>

            <li class="vimeo grid-item">
              <div class="inner">
                <div class="entry dizme_tm_portfolio_animation_wrap" data-title="ML + Django Project" data-category="Web Apps">
                  <a href="#" @click.prevent="() => onClick('img', '/img/portfolio/4.jpg')">
                    <img src="/img/thumbs/42-56.jpg" alt="" />
                    <div class="main" data-img-url="/img/portfolio/4.jpg"></div>
                  </a>
                </div>
                <div class="mobile_title">
                  <h3>ML + Django Project</h3>
                  <span>Web Apps</span>
                </div>
              </div>
            </li>

            <li class="soundcloud grid-item">
              <div class="inner">
                <div class="entry dizme_tm_portfolio_animation_wrap" data-title="Google Sheets Automation" data-category="Automation">
                  <a href="#" @click.prevent="() => onClick('img', '/img/portfolio/5.jpg')">
                    <img src="/img/thumbs/42-56.jpg" alt="" />
                    <div class="main" data-img-url="/img/portfolio/5.jpg"></div>
                  </a>
                </div>
                <div class="mobile_title">
                  <h3>Google Sheets Automation</h3>
                  <span>Automation</span>
                </div>
              </div>
            </li>

            <li class="soundcloud grid-item">
              <div class="inner">
                <div class="entry dizme_tm_portfolio_animation_wrap" data-title="Utility Apps Collection" data-category="Automation">
                  <a href="#" @click.prevent="() => onClick('img', '/img/portfolio/6.jpg')">
                    <img src="/img/thumbs/42-56.jpg" alt="" />
                    <div class="main" data-img-url="/img/portfolio/6.jpg"></div>
                  </a>
                </div>
                <div class="mobile_title">
                  <h3>Utility Apps Collection</h3>
                  <span>Automation</span>
                </div>
              </div>
            </li>
          </ul>

        </div>
      </div>
      <div class="brush_1 wow zoomIn" data-wow-duration="1s">
        <img src="/img/brushes/portfolio/1.png" alt="" />
      </div>
      <div class="brush_2 wow fadeInRight" data-wow-duration="1s">
        <img src="/img/brushes/portfolio/2.png" alt="" />
      </div>
    </div>
  </div>
  <MagnificPopUpVue
    :modal="modal"
    :close="closeModal"
    :name="name"
    :src="src"
  />
  <div :class="`${active === 1 ? '' : 'hidden_content'}`">
    <ModalBox :close="close">
      <div class="popup_details">
        <div class="top_image">
          <img src="img/thumbs/4-2.jpg" alt="" />
          <div
            class="main"
            data-img-url="img/portfolio/6.jpg"
            style="background-image: url('img/portfolio/6.jpg')"
          ></div>
        </div>
        <div class="portfolio_main_title">
          <h3>Global Evolution</h3>
          <span><a href="#">Detail</a></span>
          <div></div>
        </div>
        <div class="main_details">
          <div class="textbox">
            <p>
              We live in a world where we need to move quickly and iterate on
              our ideas as flexibly as possible.
            </p>
            <p>
              Mockups are useful both for the creative phase of the project -
              for instance when you're trying to figure out your user flows or
              the proper visual hierarchy - and the production phase when they
              phase when they will represent the target product. Building
              mockups strikes the ideal balance ease of modification.
            </p>
          </div>
          <div class="detailbox">
            <ul>
              <li>
                <span class="first">Client</span>
                <span>Alvaro Morata</span>
              </li>
              <li>
                <span class="first">Category</span>
                <span><a href="#">Detail</a></span>
              </li>
              <li>
                <span class="first">Date</span>
                <span>March 07, 2021</span>
              </li>
            </ul>
          </div>
        </div>
        <div class="additional_images">
          <ul>
            <li>
              <div class="list_inner">
                <div class="my_image">
                  <img src="img/thumbs/4-2.jpg" alt="" />
                  <div
                    class="main"
                    data-img-url="img/portfolio/1.jpg"
                    style="background-image: url('img/portfolio/1.jpg')"
                  ></div>
                </div>
              </div>
            </li>
            <li>
              <div class="list_inner">
                <div class="my_image">
                  <img src="img/thumbs/4-2.jpg" alt="" />
                  <div
                    class="main"
                    data-img-url="img/portfolio/2.jpg"
                    style="background-image: url('img/portfolio/2.jpg')"
                  ></div>
                </div>
              </div>
            </li>
            <li>
              <div class="list_inner">
                <div class="my_image">
                  <img src="img/thumbs/4-2.jpg" alt="" />
                  <div
                    class="main"
                    data-img-url="img/portfolio/3.jpg"
                    style="background-image: url('img/portfolio/3.jpg')"
                  ></div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </ModalBox>
  </div>
</template>

<script>
import MagnificPopUpVue from "./popup/MagnificPopUp.vue";
import ModalBox from "./popup/ModalBox.vue";
export default {
  name: "PortfolioComponent",
  data() {
    return {
      activeNav: "1", // props
      name: "",
      src: "",
      modal: false,
      // Content
      active: 0,
    };
  },
  mounted() {
    let Isotope = require("isotope-layout");
    setTimeout(() => {
      let iso = new Isotope(".gallery_zoom", {
        itemSelector: ".grid-item",
        //    layoutMode: "fitRows",
        percentPosition: true,
        masonry: {
          columnWidth: ".grid-item",
        },
        animationOptions: {
          duration: 750,
          easing: "linear",
          queue: false,
        },
      });
      let filterFns = {
        // show if number is greater than 50
        numberGreaterThan50: function (itemElem) {
          let number = itemElem.querySelector(".number").textContent;
          return parseInt(number, 10) > 50;
        },
        // show if name ends with -ium
        ium: function (itemElem) {
          let name = itemElem.querySelector(".name").textContent;
          return name.match(/ium$/);
        },
      };
      // bind filter button click filter main funtion
      let filtersElem = document.querySelector(".portfolio_filter ul");
      filtersElem.addEventListener("click", function (event) {
        if (event.target.getAttribute("data-filter")) {
          let filterValue = event.target.getAttribute("data-filter");
          filterValue = filterFns[filterValue] || filterValue;
          iso.arrange({ filter: filterValue });
        }
      });
    }, 1000);
  },
  methods: {
    onClick(name, src) {
      this.name = name;
      this.src = src;
      this.modal = true;
    },
    closeModal() {
      this.modal = false;
      this.name = "";
      this.src = "";
    },
    close() {
      this.active = 0;
    },
  },
  components: { MagnificPopUpVue, ModalBox },
};
</script>
