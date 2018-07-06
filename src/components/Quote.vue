<template>
    <div>
        <div class="column">
          <div class="box">
              <div class="box-header">
                <!--<app-delete-quote></app-delete-quote>           -->
              </div>
              <div class="columns">
                  <div class="column">
                    <slot></slot>
                  </div>
              </div>
          </div>
        </div>      
    </div>
</template>

<script>
    import DeletQuote from './DeleteQuote.vue'

    export default {
        components: {
            'app-delete-quote': DeletQuote
        }
    }
</script>

<style>
    .box {
        font-family: 'Arizonia', cursive;
        font-size: 20px;
        color: grey;
        /*padding-top: 0.5rem;*/
        border: 1px solid #fff;
        cursor: pointer;
        /*width: 250px;*/
    }

    .box:hover {
        border: 1px solid #ddd;
        background-color: lightcoral;
        color: #fff;
    }

    .box-header {
        text-align: right;
    }

    span {
        cursor: pointer;
        border: 1px solid #eee;
        border-radius: 50%;
        padding: 10px;
        font-size: 15px;
    }

    span:hover {
        border: 1px solid lightcoral;
    }
</style>