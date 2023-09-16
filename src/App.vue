<template>
  <div>
    <TheHeader></TheHeader>
    <BadgeList></BadgeList>
    <UserInfo
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></UserInfo>
    <CourseGoals>
      <template v-slot="goalprop">
        <h2>{{ goalprop.goalprop }}</h2><!--render list that the data not exist in  App but in  child---> 
        
      </template>
    </CourseGoals>
  </div>
</template>

<script>

import TheHeader   from "./components/TheHeader.vue";
import BadgeList from "./components/BadgeList.vue";
import UserInfo from "./components/UserInfo.vue";
import CourseGoals from './components/CourseGoals.vue';
export default {

  components:{

    TheHeader,
    BadgeList,
    UserInfo,
    CourseGoals,

  },
  data() {
    return {
      activeUser: {
        name: 'Amirhossein khanmohammadi',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },
};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>