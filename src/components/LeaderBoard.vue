<template>
    <div class="box">
      <div class="user-component field graph-container">
        <div class="position graph">№</div>
        <div class="name graph">Имя</div>
        <div class="date-since graph">На сайте с:</div>
        <div class="date-last graph">Последний раз был(а):</div>
        <div class="exp graph">Опыт</div>
        <div class="lvl graph">Уровень</div>
      </div>
        <UserPosition
            v-for="user in data"
            :key="user.id"
            :user="user"
            :selectedUser="selectedUser"
        />
        <PlugComponent />
    </div>
</template>

<script>
import '@/scss/mystyles.scss';
import '@/scss/user-position.scss';
import usersData from '../../user-data.json';
import PlugComponent from './PlugComponent.vue';
import UserPosition from './UserPosition.vue';

export default {
  name: 'LeaderBoard',
  components: {
    UserPosition,
    PlugComponent
},
  data () {
    return {
        data: usersData,
        selectedUser: 121232, // id of registered user
    }
  }
}
</script>

<style scoped lang="scss">
.graph-container{
  padding: 10px;
  background-color: rgb(32, 30, 45);
  border-radius: 4px;
.graph{
    color: white;
  }
}

</style>
