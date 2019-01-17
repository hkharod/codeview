<template>
  <div class="sidebar">
  	<a class="toggle close" href="#">
  		<span style="color: black;">
  			<i class="far fa-times-circle"></i>
  		</span>
  	</a>
    
    <div class="menu-container">
      <a class="btn-floating btn-large waves-effect waves-light red"><i class="material-icons">+</i><span> New Project</span></a>
      <ul>
      	<li>Project 1</li>
      	<li>Project 2</li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: 'sidebar'
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
</style>