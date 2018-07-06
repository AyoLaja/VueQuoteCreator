<template>
    <div>
        <div class="column">
          <div class="box">
              <div class="columns is-mobile">
                  <div class="column">
                    <slot></slot>
                  </div>
              </div>
          </div>
        </div>      
    </div>
</template>

<script>

</script>

<style>
    .box {
        font-family: 'Dancing Script', cursive;
        font-size: 20px;
        font-weight: 700;
        color: grey;
        /*padding-top: 0.5rem;*/
        padding: 1.25rem 0.75rem;
        border: 1px solid #fff;
        cursor: pointer;
        width: 250px;
    }

    .box:hover {
        border: 1px solid #ddd;
        background-color: #ba304f;
        color: #fff;
    }
</style>