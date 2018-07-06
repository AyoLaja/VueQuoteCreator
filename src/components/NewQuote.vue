<template>
    <div>
        <form>
            <div class="columns is-mobile">
                <div class="column is-half is-offset-one-quarter">
                    <textarea class="textarea" placeholder="Type in a quote" v-model="quote" required="required"></textarea>
                </div>
            </div>
            <div class="columns is-centered is-mobile">
                <div class="column is-half">
                    <button @click.prevent="newQuote" class="button is-success">Add Quote</button>
                </div>
            </div>
        </form>
        <br/>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            }
        },
        methods: {
            newQuote() {
                //this.quote is data passed that can be accessed in App.vue, when using the new quote component
                this.$emit('quoteAdded', this.quote)
                this.quote = '';
            }
        }
    }
</script>

<style scoped>

</style>