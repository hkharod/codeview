<template>
  <div class="dashboard">
    <div class="header">
      <a class="toggle open" href="#sidebar">
        <span style="color: black;">
          <i class="fas fa-bars"></i>
        </span>
      </a>
      <a class="dashboardTitle">Code View</a>
    </div>
		<sidebar id="sidebar"></sidebar>
    <main-content id="content"></main-content>
  </div>
</template>

<script>

import Sidebar from '@/components/Sidebar.vue'
import MainContent from '@/components/MainContent.vue'

export default {
  components: {
  	Sidebar,
    MainContent
  },
  name: 'dashboard'
}

</script>

<style>
  .dashboard {
    display: grid;
    grid-template-columns: 1fr 3fr;
  }
  .header {
    background: #ded;
    display: none;
    font-size: 24px;
  }
  #sidebar {
    background: #eee;
  }
  #content {
    background: #ddd;
  }
  .toggle {
    display: none;
  }

  @media only screen and (max-width: 800px) {
    .dashboard {
      grid-template-columns: 1fr;
    }
    #sidebar {
      position: fixed;
      top: 0;
      bottom: 0;
      left: -340px;
      width: 300px;
      transition: transform .3s ease-in-out;
    }
    #sidebar:target {
      transform: translateX(340px);
    }
    .header {
      display: grid;
      grid-template-columns: 1fr 1fr;
      padding: 20px;
    }
    .open {
      justify-self: start;
      align-self: center;
      cursor: pointer;
    }
    .dashboardTitle {
      justify-self: end;
      align-self: center;
    }
    .toggle {
      display: block;
    }
  }
</style>