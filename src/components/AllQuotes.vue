<template>
    <div>
        <div class="columns is-mobile">
          <app-quote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{quote}}</app-quote>
        </div>      
    </div>
</template>

<script>
    import Quote from './Quote.vue'
    import DeletQuote from './DeleteQuote.vue'

    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote,
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', this.index)
            }
        }
    }
</script>

<style>

</style>