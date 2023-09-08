<template>
  <div class="greet-main">
    <div id="particles-js"></div>
    <div class="container">
      <div class="greet">
        <h1 class="greet-title">
          Hi, <br />
          I'm Bayzid
        </h1>
        <div class="greet-desc">
          <p>
            A passionate Full Stack Web Developer having an experience
            of building Web and Mobile applications with PHP Laravel / Vue /
            Tailwind and some other cool libraries and frameworks.
          </p>
        </div>
        <div class="social-links dn">
          <a href="" class="social">
            <span>icon</span>
          </a>
          <a href="" class="social">
            <span>icon</span>
          </a>
          <a href="" class="social">
            <span>icon</span>
          </a>
          <a href="" class="social">
            <span>icon</span>
          </a>
          <a href="" class="social">
            <span>icon</span>
          </a>
        </div>
        <div class="greet-btn-box">
          <a href="#contact" class="greet-btn">Contact me</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "../assets/js/particles";
// import '../assets/js/app';
export default {
  mounted() {
    particlesJS(
      "particles-js",

      {
        particles: {
          number: {
            value: 80,
            density: {
              enable: true,
              value_area: 800,
            },
          },
          color: {
            value: "#ffffff",
          },
          shape: {
            type: "circle",
            stroke: {
              width: 0,
              color: "#000000",
            },
            polygon: {
              nb_sides: 5,
            },
            image: {
              src: "img/github.svg",
              width: 100,
              height: 100,
            },
          },
          opacity: {
            value: 0.2,
            random: false,
            anim: {
              enable: false,
              speed: 1,
              opacity_min: 0.1,
              sync: false,
            },
          },
          size: {
            value: 3,
            random: true,
            anim: {
              enable: false,
              speed: 40,
              size_min: 0.1,
              sync: false,
            },
          },
          line_linked: {
            enable: true,
            distance: 150,
            color: "#ffffff",
            opacity: 0.4,
            width: 1,
          },
          move: {
            enable: true,
            speed: 6,
            direction: "none",
            random: false,
            straight: false,
            out_mode: "out",
            attract: {
              enable: false,
              rotateX: 600,
              rotateY: 1200,
            },
          },
        },
        interactivity: {
          detect_on: "canvas",
          events: {
            onhover: {
              enable: true,
              mode: "grab",
            },
            onclick: {
              enable: true,
              mode: "push",
            },
            resize: true,
          },
          modes: {
            grab: {
              distance: 200,
              line_linked: {
                opacity: 1,
              },
            },
            bubble: {
              distance: 400,
              size: 40,
              duration: 2,
              opacity: 8,
              speed: 3,
            },
            repulse: {
              distance: 200,
            },
            push: {
              particles_nb: 4,
            },
            remove: {
              particles_nb: 2,
            },
          },
        },
        retina_detect: true,
        config_demo: {
          hide_card: false,
          background_color: "#b61924",
          background_image: "",
          background_position: "50% 50%",
          background_repeat: "no-repeat",
          background_size: "cover",
        },
      }
    );
  },
};
</script>
