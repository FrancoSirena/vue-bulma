<template>
  <div class="faq">
    <div class="container">
      <section class="section">
        <h1 class="title">{{ heading }}</h1>
        <h2 class="subtitle is-4">{{ subheading }}</h2>

        <div class="columns" v-if="faqs && faqs.length">
          <div class="column is-one-third" :key="faq.id" v-for="faq of faqs">
            <div class="card">
              <div class="card-content">
                <p class="title">{{faq.title}}</p>
                <p class="answer">{{faq.body}}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'faq',
  data: function() {
    return {
      faqs: [],
      errors: [],
      heading: 'FAQ Page',
      subheading: 'Lorem Ipsum is a simple demo text for the print and typeface industry. Lorem Ipsum has been the standard demo text in the industry since 1500, when an unknown writer took a handful of words and jumbled them to create a sample book.'
    }
  },
  created: function() {
    axios.get('http://jsonplaceholder.typicode.com/posts')
      .then(response => {
        this.faqs = response.data.slice(0, 10);
      })
      .catch(e => {
        this.errors.push(e)
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import '../mq'

  .pd
    padding: 2.5rem 0 1.5rem 0

  .answer
    margin-top: 10px !important
    color: gray
  .columns
    flex-wrap: wrap
</style>
