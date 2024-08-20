<template>
  <div class="container">
    <Header />
    <Profile />
    <ProjectList />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Profile from './components/Profile.vue';
import ProjectList from './components/ProjectList.vue';

export default {
  components: {
    Header,
    Profile,
    ProjectList,
  },
};
</script>
