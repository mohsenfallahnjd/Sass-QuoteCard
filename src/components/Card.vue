<template>
  <div id="card">
    <article class="text-card">
      <img
        src="../assets/stefan-stefancik-pmH_Y4Qetrk-unsplash.jpg"
        class="card--image"
      />
      <div class="card--details">
        <h3 class="card--details__title">{{ title }}</h3>
        <div class="text">
          <h4 class="card--details__description">{{ desc }}</h4>
          <h1 class="card--details__ampersand">&</h1>
        </div>
        <p class="card--details__author"><span></span>{{ author }}</p>
      </div>
    </article>
  </div>
</template>

<script>
export default {
  name: "Card",
  data: () => ({
    title: "Quote of the day",
    desc: `"We are all like the bright moon, we still have our darker side."`,
    author: "Khalil Gibran"
  })
};
</script>

<style lang="sass" scoped>
@import url('https://fonts.googleapis.com/css?family=Fugaz+One|Lora|Roboto+Slab|Andada|Libre+Baskerville&display=swap');
// @import url('https://fonts.googleapis.com/css?family=Andada&display=swap');

.text-card
  display: flex
  justify-content: center
  position: relative
  height: 600px
  width: 300px
  border-radius: 0.1rem
  box-shadow: 0.4rem -0.3rem 0.8rem rgba(0, 0, 0, 0.3)
  overflow: hidden

.text
  display: flex
  width: 230px
  justify-content: space-between

.card--image
    width: 100%
    height: 100%
    object-fit: cover
    filter: blur(0.3px) brightness(69%)

.card--details
    position: absolute
    color: #fafafa
    align-self: center
    text-rendering: optimizeLegibility
    padding-right: 20px
    padding-bottom: 50px
    &__title
      font-family: 'Lora', serif
      text-transform: uppercase
      font-size: 35px
      font-weight: 400
      line-height: 1.2
      padding-bottom: 25px
      width: 200px
    &__description
      font-family: 'Andada', serif
      font-size: 24px
      font-weight: 100
      line-height: 1.2
      width: 180px
    &__ampersand
      font-family: 'Libre Baskerville', serif
      font-size: 45px
      font-weight: 100
      opacity: 0.4
      align-self: center
      padding-bottom: 25px
      margin-right: -15px
    &__author
      font-family: 'Fugaz One', cursive
      font-size: 15px
      font-weight: 100
      position: relative
      z-index: 1
      margin-left: 23px
      padding: 0px 2px
      span
        border-top: 1.5px solid #fafafa
        left: -8%
        content: ''
        position: absolute
        top: 50%
        width: 8%
        z-index: -1
</style>
