<template>
  <div class="about-wrapper">
    <div class="about">
      <Bio />
    </div>
    <div class="about-bottom">
      <div class="contact-wrapper">
        <Contact />
      </div>
      <div class="copy-wrapper">
        <p class="copyright">
          © Copyright 2020 Purvi Trivedi - Made with VueJS
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import Bio from '../components/Bio'
import Contact from '../components/layout/Contact'
export default {
  components: { Bio, Contact }
}
</script>

<style lang="scss">
.about-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;

  @media (max-height: 700px) {
  }

  .about {
    height: 42vh;
    justify-content: center;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;

    @media (max-width: 500px) {
      height: 70vh;
    }

    @media (max-height: 700px) {
      font-size: 0.8em;
    }

    .long-bio {
      font-size: 1.25em;
      margin-bottom: 2em;

      @media (max-width: 1200px) {
        padding: 0px 20px;
        font-size: 1.15em;
      }

      .hello {
        position: relative;
        .wave {
          font-size: 20px;
          position: absolute;
          margin-left: 5px;
          top: -5px;
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

    @media (max-width: 500px) {
      height: 20vh;
    }

    .contact-wrapper {
      width: 49.85vw;
      height: 100%;
      background-color: #5220dd;

      @media (max-width: 500px) {
        width: 100vw;
      }

      .contact-me {
        height: 100%;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        .email-wrapper {
          padding: 2.438em 0px 0px 2.438em;
          p {
            margin: 0px 0px 10px 0px;
          }

          a {
            font-family: 'Space Bold', sans-serif;
            font-size: 25px;
            color: #ffc647;
            font-weight: 600;
            text-decoration: none;

            @media (max-width: 500px) {
              font-size: 1em;
            }
          }
        }
        .footer {
          display: flex;
          justify-content: space-between;

          .footer-icon {
            padding: 0px 0px 1.563em 2.438em;

            @media (max-height: 700px) {
              margin-top: 10px;
            }

            a {
              font-size: 40px;
              color: #f0f4ff;
              margin-right: 30px;

              @media (max-width: 500px) {
                font-size: 1.5em;
              }
            }
          }
        }
      }
    }
    .copy-wrapper {
      background-color: #ffc647;
      width: 49.85vw;
      height: 100%;
      display: flex;
      justify-content: flex-end;

      @media (max-width: 500px) {
        display: none;
      }

      .copyright {
        color: #17224d;
        font-size: 12px;
        padding: 0px 39px 15px 0px;
        align-self: flex-end;
      }
    }
  }
}
</style>
