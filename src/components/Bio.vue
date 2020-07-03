<template>
  <div class="long-bio">
    <p class="hello">Hiya! <span class="wave">👋</span></p>
    <p>
      I’m a software engineer with experience in UX Research and Music
      Technology.
    </p>
    <p>
      I decided to learn how to code after participating in a workshop where I
      used a language called Littlefoot to make music on the Lightpad Block.
    </p>
    <p>
      I was blown away by the possibility of creating interfaces that make human
      interaction with technology fun and couldn't stop myself from exploring
      further.
    </p>
    <p>
      Recently, I finished the Software Engineering Immersive course at General
      Assembly, where I trained as a Full-Stack Engineer
    </p>

    <p>
      I am now looking for my first role as a developer I am now looking to work
      as a developer in a collaborative team where I can share my creativity and
      learn from others.
    </p>
  </div>
</template>

<script>
export default {
  name: 'Bio'
}
</script>

<style lang="scss">
.long-bio {
  padding: 0px 0.85em;

  .green {
    color: #06d6a0;
    font-weight: bold;
  }
  .hello {
    position: relative;
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
</style>
