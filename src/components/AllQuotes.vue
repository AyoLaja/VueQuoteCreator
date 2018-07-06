<template>
    <div>
        <div class="columns">
            <div class="column">
                <span class="has-text-info">
                     Hint: Click on quote to delete
                </span> 
            </div>
        </div>
        <div class="columns is-mobile all-quotes">
          <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{quote}}</app-quote>
        </div>      
    </div>
</template>

<script>
    import Quote from './Quote.vue'

    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote,
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index)
            }
        }
    }
</script>

<style>
    .all-quotes {
        max-width: 1200px;
        overflow: auto;
    }
</style>