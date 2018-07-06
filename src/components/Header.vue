<template>
    <div>
        <div class="content">
            <h5>Quotes Added</h5>
        </div>
        <div class="columns">
            <div class="column is-11">
                <progress class="progress is-success" max="100" min="0" :value="(quoteCount/maxQuotes) * 100"></progress> 
            </div>
            <div class="column is-1">
                <span>{{quoteCount}} / {{maxQuotes}}</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['quoteCount', 'maxQuotes']
    }
</script>

<style scoped>
    .content {
        margin-bottom: 10px;
    }
</style>