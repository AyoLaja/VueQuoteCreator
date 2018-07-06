<template>
  <div>
    
      <!--<div class="columns">
        <div class="column">
          <div class="content">
          <h1>Nigerian Quotes</h1>
          </div>
        </div>
      </div>-->
      
    <div class="container">
      <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
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
  .container {
    border: 1px solid #eee;
    padding: 20px;
    margin: 20px auto;
    border-radius: 25px;
  }
</style>
