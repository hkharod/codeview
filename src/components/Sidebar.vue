<template>
  <div class="sidebar">
  	<a class="toggle close" href="#">
  		<span style="color: black;">
  			<i class="far fa-times-circle"></i>
  		</span>
  	</a>
    <div class="sidebar-logo">
      <img src="/img/codeview.png"/>
    </div>
    <div class="menu-container">
      <a class="btn-floating btn-large waves-effect waves-light cv-black"><i class="material-icons">+</i><span> New Project</span></a>
      <ul v-if="projects.length">
      	<li v-for="project in projects">{{ project.name }}</li>
      </ul>
      <p v-if="!projects.length">You don't have any projects, click the button above to add one!</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'sidebar',
  data() {
    return {
      projects: [],
    }
  }
}

</script>

<style scoped>
  .menu-container {
    width: 50%;
    display: block;
    margin: 0 auto;
    padding-top: 20px;
    text-align: center;
  }

  .sidebar-logo {
    border-bottom: 1px lightgrey solid;
  }

  .sidebar-logo img {
    display: block;
    margin: 0 auto;
    width: 50%;
    padding: 20px;
  }

  .cv-black {
    background-color: #1B2B34;
  }
</style>