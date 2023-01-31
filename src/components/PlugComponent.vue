<template>
  <div class="field plug">...</div>
</template>

<script>
import '@/scss/mystyles.scss'

export default {
  name: 'PlugComponent',
  components: {
},
  methods: {
  }
}
</script>

<style scoped lang="scss">
    .plug{
        background-color: rgb(94, 101, 108);
        color: rgb(191, 205, 226);
        padding: 10px;
        border-radius: 4px;
        cursor: pointer;
        font-size: 20px;
        align-items: center;
        display: flex;
        justify-content: center;
    }
</style>
