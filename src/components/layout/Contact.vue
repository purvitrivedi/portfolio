<template>
  <div id="contact" class="contact-me">
    <p>Get In Touch: <span>purvitriv@gmail.com</span></p>
  </div>
</template>

<script>
export default {
  name: 'Contact'
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');
.contact-me {
  background-color: #1b1b1b;
  color: white;
  display: flex;
  justify-content: center;
  align-items: baseline;
  padding: 20px 0px 10px 10px;
  p {
    font-size: 1em;
    margin-top: 0;
    span {
      color:#F5DD90;
      font-weight: 500;
    }
  }
}
</style>
