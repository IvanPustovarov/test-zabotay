<template>
  <div class="field user-component">
    <div class="position">#{{ user.position }}</div>
    <div class="name">{{ user.name }}</div>
    <div class="date-since">{{ parseDate(user.since) }}</div>
    <div class="date-last">{{ parseDate(user.last_seen) }}</div>
    <div class="exp">{{ user.experience }}</div>
    <div class="lvl">{{ user.level }}</div>
  </div>
</template>

<script>
 import '@/scss/mystyles.scss'
 import '@/scss/user-position.scss';

export default {
  name: 'UserPosition',
  components: {
  },
  props: {
    user: Object,
  },
  methods: {
    parseDate(date) {
      return `${new Intl.DateTimeFormat('en-GB').format(date)}`
    }
  },
  computed:{
  }
}
</script>

<style scoped lang="scss">
.user-component{
  background-color: rgb(20, 63, 109);
  color: rgb(191, 205, 226);
  padding: 10px;
  border-radius: 4px;
  cursor: pointer;
  &:hover{
    background-color: rgb(34, 102, 174);
    color: rgb(195, 208, 224);
  }
}
</style>
