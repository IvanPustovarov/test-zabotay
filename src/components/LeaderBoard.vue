<template>
    <div class="box">
        <UserPosition
            v-for="user in data"
            :key="user.id"
            :user="user"
        />
    </div>
</template>

<script>
import usersData from '../../user-data.json';
import '@/scss/mystyles.scss'
import UserPosition from './UserPosition.vue';

export default {
  name: 'LeaderBoard',
  components: {
    UserPosition
  },
  data () {
    return {
        data: usersData
    }
  }
}
</script>

<style lang="scss">

</style>
