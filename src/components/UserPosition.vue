<template>
  <div class="field user-component">
    <div class="position">{{ user.position }}</div>
    <div class="name">{{ user.name }}</div>
    <div class="date">{{ parseDate() }}</div>
    <div class="exp">{{ user.experience }}</div>
    <div class="lvl">{{ user.level }}</div>
  </div>
</template>

<script>
 import '@/scss/mystyles.scss'

export default {
  name: 'UserPosition',
  components: {
  },
  props: {
    user: Object,
  },
  methods: {
    parseDate() {
        const userSince = new Date(this.user.since);
        const userLastSeen = new Date(this.user.last_seen);
        return `Пользователь на сайте с ${userSince.toJSON().slice(0, 10)}.
         Последний раз был в сети ${userLastSeen.toJSON().slice(0, 10)}`
    }
  }
}
</script>

<style lang="scss">
    .user-component{
        display: flex;
        flex-direction: row;
        text-align: center;
        & .position{
            flex: 0.5;
        }
        & .name{
            flex: 2;
            text-align: start;
        }
        & .date{
            flex: 4;
        }
        & .exp{
            flex: 1;
        }
        & .lvl{
            flex: 0.5;
        }
    }
</style>
