<template>
  <div class="about-wrapper">
    <div class="about">
      <Bio />
    </div>
    <div class="about-bottom">
      <div class="contact-wrapper">
        <Contact />
      </div>
      <div class="skills-wrapper">
        <Skills />
      </div>
    </div>
  </div>
</template>

<script>
import Skills from '../components/skills/AllSkills'
import Bio from '../components/Bio'
import Contact from '../components/layout/Contact'
export default {
  components: { Skills, Bio, Contact }
}
</script>

<style lang="scss">
.about-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;

  .about {
    height: 42vh;
    justify-content: center;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    .long-bio {
      font-size: 15px;
      margin-bottom: 2em;
      .hello {
        position: relative;
        font-size: 20px;
        .wave {
          font-size: 20px;
          position: absolute;
          margin-left: 5px;
          top: -7px;
          animation-name: shaking;
          animation-duration: 1s;
          animation-iteration-count: infinite;
        }

        @keyframes shaking {
          0% {
            transform: rotate(0deg);
          }

          50% {
            transform: rotate(20deg);
          }

          100% {
            transform: rotate(0deg);
          }
        }
      }
    }
  }

  .about-bottom {
    width: 100vw;
    height: 50vh;
    display: flex;
    justify-content: space-between;

    .contact-wrapper {
      width: 49.85vw;
      height: 100%;
      background-color: #5220dd;

      .contact-me {
        height: 100%;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        .email-wrapper {
          // background-color: red;
          padding: 39px 0px 0px 39px;
          p {
            margin: 0px 0px 10px 0px;
          }

          a {
            font-size: 25px;
            color: #ffc647;
            font-weight: 600;
            text-decoration: none;
          }
        }
        .footer {
          background-color: powderblue;
        }

        .copyright {
          align-self: flex-end;
        }
      }
    }
    .skills-wrapper {
      background-color: #ffc647;
      width: 49.85vw;
      height: 100%;
      display: flex;
      align-items: center;

      .skill-svg {
        display: flex;

        .icon {
          border: 1px solid #17224d;
          border-radius: 0.25rem;
          margin: 10px;

          svg {
            width: px;
            padding: 12px 24px;
          }

          p {
            margin-top: 0px;
            font-size: 11px;
          }
          svg:hover {
            transform: scale(1.1);
          }
        }
      }
    }
  }
}
</style>
