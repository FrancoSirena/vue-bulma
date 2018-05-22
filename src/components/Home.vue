<template>
  <div class="home">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            {{ heading }}
          </h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle is-4">{{ subheading }}</h2>
          </div>
          <a href="#" class="button is-large is-primary" id="learn">Learn More</a>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-1 has-text-centered"><i class="fa fa-cog is-primary"></i></div>
          <div class="column is--one-third-desktop">
            <p class="title"><strong>Some random subtitle</strong></p>
          </div>
          <div class="column">
            <p>Lorem Ipsum is a simple demo text for the print and typeface industry. Lorem Ipsum has been the standard demo text in the industry since 1500, when an unknown writer took a handful of words and jumbled them to create a sample book.</p>
          </div>
        </div>
      </div>

      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">Some Testimonial</p>
              <p class="subtitle">Franco Sirena</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">Some Testimonial</p>
              <p class="subtitle">Franco Sirena</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">Some Testimonial</p>
              <p class="subtitle">Franco Sirena</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data: function() {
    return {
      heading: 'Main Title',
      subheading: 'Lorem Ipsum is a simple demo text for the print and typeface industry. Lorem Ipsum has been the standard demo text in the industry since 1500, when an unknown writer took a handful of words and jumbled them to create a sample book. Not only has it survived five centuries, but it has also made a spell in electronic font editing (note, almost unchanged). It became known in 1960, with the appearance of "Letraset", which contains passages from Lorem Ipsum, as well as desktop software like "Aldus PageMaker" - also with Lorem Ipsum.'
    }
  }
}
</script>

<style scoped lang="sass">
  @import '../mq'

  .hero
    background: url('../assets/clouds.jpg')
    backgroun-size: cover

    .title
      +mobile
        font-weight: bold
      +tablet
        font-size: 2.5rem
      +desktop
        font-size: 4rem
        margin-top: 2rem
  h2
    margin: 1.5rem 0 2rem 0 !important

  .fa-cog
    font-size: 40px

  #learn
    +desktop
      margin-bottom: 2rem

  .pd
    +tablet
      padding: 2rem 0


</style>
