<template>
  <Layout>
    <div class="page">
      <h1>{{ isHover ? "But you can call me" : "Hey, my name is" }}</h1>
      <div class="name color">
        <div class="text-wrapper">
          <div
            class="letters disable-select"
            v-on:click="touchName"
            v-on="isMobile ? {} : { mouseenter: nameHoverEnter }"
            v-on:mouseleave="nameHoverExit"
          >
            <span>
              <Name class="name-style" first="O" middle="svaldo Pere" last="z." />
            </span>
          </div>
        </div>
      </div>
      <img
        loading="lazy"
        class="avatar"
        src="https://avatars1.githubusercontent.com/u/463779"
        alt="Avatar"
        border="2"
      />
      <p>I'm a software developer based in Chicago, IL who enjoys building web apps that make lives of others easier. I enjoy working with JavaScript frameworks and cloud platforms.</p>
      <p>I have over 8 years of programming experience, during which I have led development teams and delivered robust software solutions across various industries.</p>
      <p>Currently, I am a Full Stack Developer at Exceleras. My role involves improving their platform and modernizing the tech stack to ensure it meets contemporary standards and delivers optimal performance for our users.</p>
      <p>Here's a few technologies I've been working with recently:</p>
      <ul class="color">
        <li>Ruby</li>
        <li>Ruby on Rails</li>
        <li>JavaScript &amp; TypeScript</li>
        <li>HTML &amp; CSS</li>
        <li>Vue</li>
        <li>Node.js</li>
        <li>Angular</li>
        <li>C#</li>
      </ul>
      <p>Outside of programming and spending time with my wife, I enjoy video games, videography, tacos and discovering new places.</p>
      <footer class="color">
        <div class="social-links">
          <a
            href="https://github.com/xi-osman/profile"
            target="_blank"
            rel="nofollow noopener noreferrer"
          >
            <div>Designed &amp; Built by Osvaldo Perez</div>
          </a>
        </div>
        <div class="social-links">
          <a href="https://github.com/xi-osman" target="_blank" rel="nofollow noopener noreferrer">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 438.549 438.549">
              <title>Github</title>
              <path
                d="M409.132,114.573c-19.608-33.596-46.205-60.194-79.798-79.8C295.736,15.166,259.057,5.365,219.271,5.365 c-39.781,0-76.472,9.804-110.063,29.408c-33.596,19.605-60.192,46.204-79.8,79.8C9.803,148.168,0,184.854,0,224.63 c0,47.78,13.94,90.745,41.827,128.906c27.884,38.164,63.906,64.572,108.063,79.227c5.14,0.954,8.945,0.283,11.419-1.996 c2.475-2.282,3.711-5.14,3.711-8.562c0-0.571-0.049-5.708-0.144-15.417c-0.098-9.709-0.144-18.179-0.144-25.406l-6.567,1.136 c-4.187,0.767-9.469,1.092-15.846,1c-6.374-0.089-12.991-0.757-19.842-1.999c-6.854-1.231-13.229-4.086-19.13-8.559 c-5.898-4.473-10.085-10.328-12.56-17.556l-2.855-6.57c-1.903-4.374-4.899-9.233-8.992-14.559 c-4.093-5.331-8.232-8.945-12.419-10.848l-1.999-1.431c-1.332-0.951-2.568-2.098-3.711-3.429c-1.142-1.331-1.997-2.663-2.568-3.997 c-0.572-1.335-0.098-2.43,1.427-3.289c1.525-0.859,4.281-1.276,8.28-1.276l5.708,0.853c3.807,0.763,8.516,3.042,14.133,6.851 c5.614,3.806,10.229,8.754,13.846,14.842c4.38,7.806,9.657,13.754,15.846,17.847c6.184,4.093,12.419,6.136,18.699,6.136 c6.28,0,11.704-0.476,16.274-1.423c4.565-0.952,8.848-2.383,12.847-4.285c1.713-12.758,6.377-22.559,13.988-29.41 c-10.848-1.14-20.601-2.857-29.264-5.14c-8.658-2.286-17.605-5.996-26.835-11.14c-9.235-5.137-16.896-11.516-22.985-19.126 c-6.09-7.614-11.088-17.61-14.987-29.979c-3.901-12.374-5.852-26.648-5.852-42.826c0-23.035,7.52-42.637,22.557-58.817 c-7.044-17.318-6.379-36.732,1.997-58.24c5.52-1.715,13.706-0.428,24.554,3.853c10.85,4.283,18.794,7.952,23.84,10.994 c5.046,3.041,9.089,5.618,12.135,7.708c17.705-4.947,35.976-7.421,54.818-7.421s37.117,2.474,54.823,7.421l10.849-6.849 c7.419-4.57,16.18-8.758,26.262-12.565c10.088-3.805,17.802-4.853,23.134-3.138c8.562,21.509,9.325,40.922,2.279,58.24 c15.036,16.18,22.559,35.787,22.559,58.817c0,16.178-1.958,30.497-5.853,42.966c-3.9,12.471-8.941,22.457-15.125,29.979 c-6.191,7.521-13.901,13.85-23.131,18.986c-9.232,5.14-18.182,8.85-26.84,11.136c-8.662,2.286-18.415,4.004-29.263,5.146 c9.894,8.562,14.842,22.077,14.842,40.539v60.237c0,3.422,1.19,6.279,3.572,8.562c2.379,2.279,6.136,2.95,11.276,1.995 c44.163-14.653,80.185-41.062,108.068-79.226c27.88-38.161,41.825-81.126,41.825-128.906 C438.536,184.851,428.728,148.168,409.132,114.573z"
              />
            </svg> GitHub
          </a>
          <a href="https://twitter.com/xiosman" target="_blank" rel="nofollow noopener noreferrer">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-twitter-x"
              viewBox="0 0 16 16">
              <title>X</title>
              <path
                d="M12.6.75h2.454l-5.36 6.142L16 15.25h-4.937l-3.867-5.07-4.425 5.07H.316l5.733-6.57L0 .75h5.063l3.495 4.633L12.601.75Zm-.86 13.028h1.36L4.323 2.145H2.865z" />
            </svg> Twitter
          </a>
          <a href="https://vimeo.com/xiosman" target="_blank" rel="nofollow noopener noreferrer">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24">
              <title>Vimeo</title>
              <path
                d="M22.875 10.063c-2.442 5.217-8.337 12.319-12.063 12.319-3.672 0-4.203-7.831-6.208-13.043-.987-2.565-1.624-1.976-3.474-.681l-1.128-1.455c2.698-2.372 5.398-5.127 7.057-5.28 1.868-.179 3.018 1.098 3.448 3.832.568 3.593 1.362 9.17 2.748 9.17 1.08 0 3.741-4.424 3.878-6.006.243-2.316-1.703-2.386-3.392-1.663 2.673-8.754 13.793-7.142 9.134 2.807z"
              />
            </svg> Vimeo
          </a>
          <a href="https://www.linkedin.com/in/xiosman" target="_blank" rel="nofollow noopener noreferrer">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 430.117 430.117">
              <title>LinkedIn</title>
              <path
                d="M430.117,261.543V420.56h-92.188V272.193c0-37.271-13.334-62.707-46.703-62.707 c-25.473,0-40.632,17.142-47.301,33.724c-2.432,5.928-3.058,14.179-3.058,22.477V420.56h-92.219c0,0,1.242-251.285,0-277.32h92.21 v39.309c-0.187,0.294-0.43,0.611-0.606,0.896h0.606v-0.896c12.251-18.869,34.13-45.824,83.102-45.824 C384.633,136.724,430.117,176.361,430.117,261.543z M52.183,9.558C20.635,9.558,0,30.251,0,57.463 c0,26.619,20.038,47.94,50.959,47.94h0.616c32.159,0,52.159-21.317,52.159-47.94C103.128,30.251,83.734,9.558,52.183,9.558z M5.477,420.56h92.184v-277.32H5.477V420.56z"
              />
            </svg> LinkedIn
          </a>
          <a href="mailto:xiosman@gmail.com">
            <svg xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 24 24">
              <title>Email</title>
              <path
                d="M24 0l-6 22-8.129-7.239 7.802-8.234-10.458 7.227-7.215-1.754 24-12zm-15 16.668v7.332l3.258-4.431-3.258-2.901z"
              />
            </svg> Email
          </a>
        </div>
      </footer>
    </div>
  </Layout>
</template>

<script>
import anime from "animejs/lib/anime.es.js";
import Name from "../components/Name";

export default {
  data: function() {
    return {
      isHover: false,
      isMobile: false,
      animeLoop: null
    };
  },
  mounted: function () {
    this.$nextTick(function() {
      this.isMobile = window.matchMedia(
        "only screen and (max-width: 760px)"
      ).matches;
    });
    console.log('%c Want the code? Go to the link below!', 'background-color: white; font-weight: bold; font-size: 30px;color: red; text-shadow: 1px 1px 0 rgb(217,31,38) , 2px 2px 0 rgb(226,91,14) , 3px 3px 0 rgb(245,221,8) , 4px 4px 0 rgb(5,148,68) , 5px 5px 0 rgb(2,135,206) , 6px 6px 0 rgb(4,77,145) , 7px 7px 0 rgb(42,21,113)');
    console.log('https://github.com/xi-osman/profile')
    this.animeLoop = setInterval(() => { this.touchName() }, 6000);
  },
  methods: {
    touchName: function() {
      if (this.isHover) this.nameHoverExit();
      else this.nameHoverEnter()
    },
    nameHoverEnter: function(event) {
      this.isHover = true;

      if(event !== null)
        clearInterval(this.animeLoop)

      anime.remove(".box");
      anime.remove(".name .letter");
      anime({
        targets: ".name .letter",
        translateY: "2em",
        duration: 525,
        delay: anime.stagger(30)
      });
      anime({
        targets: ".box",
        duration: 2800,
        translateX: "-5.64em"
      });
    },
    nameHoverExit: function(event) {
      this.isHover = false;

      if(event !== null)
        clearInterval(this.animeLoop)

      anime.remove(".box");
      anime.remove(".name .letter");
      anime({
        targets: ".name .letter",
        translateY: 0,
        duration: 525,
        delay: anime.stagger(30, { direction: "reverse" })
      });
      anime({
        targets: ".box",
        duration: 1700,
        translateX: 0
      });
    }
  },
  metaInfo: {
    title: "Osvaldo Perez | Software Developer"
  },
  components: {
    Name
  }
};
</script>


<style>
.page {
  font-size: calc(10px + 0.33vw);
  -webkit-font-smoothing: antialiased;
  padding: 5vh 10vw;
  color: #121314;
}
p {
  font-size: 1.6em;
  font-weight: 300;
  line-height: 1.4;
  max-width: 26em;
}
a {
  text-decoration: none;
  position: relative;
}
a:after {
  content: "";
  position: absolute;
  z-index: -1;
  top: 60%;
  left: -0.1em;
  right: -0.1em;
  bottom: 0;
  transition: top 200ms cubic-bezier(0, 0.8, 0.13, 1);
  background-color: rgba(79, 192, 141, 0.5);
}
a:hover:after {
  top: 0%;
}

ul {
  padding-left: 1.5em;
  font-weight: 300;
  line-height: 1.4;
  max-width: 30em;
  columns: 2;
  -webkit-columns: 2;
  -moz-columns: 2;
  list-style-type: none;
}

li::before {
  content: ">";
  position: relative;
  padding-right: 10px;
  /* left: -20px; */
  color: rgba(79, 192, 141, 0.5);
  font-size: 16px;
  line-height: 12px;
  font-weight: 500;
}

footer {
  margin-top: 2em;
  flex-direction: row;
  text-align: center;
  height: auto;
  min-height: 70px;
}

footer svg {
  width: 20px;
  height: 20px;
}

.name {
  cursor: pointer;
  margin-top: 0.5em;
  position: relative;
  font-weight: 500;
}

.name .text-wrapper {
  position: relative;
  display: inline-block;
  padding-right: 0.05em;
  padding-bottom: 0.1em;
  overflow: hidden;
}

.name .letter {
  display: inline-block;
  min-width: 0.24em;
}

.name-style {
  font-size: 2.8em;
  padding-right: 1.5em;
  display: inline-flex;
}

/* Small screens */
@media all and (max-width: 600px) {
  .avatar {
    float: none !important;
    display: block;
    margin: auto !important;
    margin-top: 6em !important;
  }
}

.avatar {
  margin: 2em;
  max-width: 20em;
  border-radius: 30%;
  float: right;
}

.social-links {
  margin: 2em 3em 0 3em;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.social-links a{
  margin: 10px 20px 0 20px;
}

.disable-select {
  user-select: none; /* supported by Chrome and Opera */
  -webkit-user-select: none; /* Safari */
  -khtml-user-select: none; /* Konqueror HTML */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* Internet Explorer/Edge */
}
</style>

