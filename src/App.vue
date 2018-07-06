<template>
  <div class="container">
    <br/>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-all-quotes :quotes="quotes" @quoteDeleted="deleteQuote"></app-all-quotes>
    <div class="columns">
      <div class="column">
       <div class="notification is-info">
         <button class="delete"></button>
         To delete quote, click on a quote.
       </div>
      </div>
    </div>
  </div>
</template>

<script>
  import NewQuote from './components/NewQuote.vue'
  import Quote from './components/Quote.vue'
  import AllQuotes from './components/AllQuotes.vue'
  import Header from './components/Header.vue'

  export  default {
    components: {
      'app-new-quote': NewQuote,
      'app-quote': Quote, 
      'app-all-quotes': AllQuotes,
      'app-header': Header
    }, 
    data() {
      return {
        quotes: [
          '\"Sample quote\"',
          '\"If you try it!\"',
          '\"Guy behave yourself\"',
          '\"Don\'t let me slap you\"',
          '\"You are very stupid\"',
          '\"Abeg free me\"'
        ],
        maxQuotes: 10
      }
    },
    methods: {
      newQuote(quote) {
        let newQuote = `\"${quote}\"`
        this.quotes.push(newQuote)
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1)
      }
    }
  }
</script>

<style>

</style>
