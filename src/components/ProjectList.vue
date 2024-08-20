<template>
    <section class="projects">
      <h2>Projects</h2>
      <ul>
        <li v-for="project in projects" :key="project.id">
          <strong>{{ project.name }}</strong>: {{ project.description }}
        </li>
      </ul>
    </section>
  </template>
  
  <script>
  export default {
    name: 'ProjectList',
    data() {
      return {
        projects: [
          { id: 1, name: 'Project 1', description: 'Description of project 1' },
          { id: 2, name: 'Project 2', description: 'Description of project 2' },
          { id: 3, name: 'Project 3', description: 'Description of project 3' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .projects {
    margin: 20px;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    margin: 10px 0;
  }
  </style>
  