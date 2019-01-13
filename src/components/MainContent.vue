<template>
  <div class="content">
  	<div class="contentHeader">
  		<template v-if="newProject">
	  		<h2><u>New Project</u></h2>
			<form-input 
				label="Project Name" 
				type="text" 
				placeholder="Name" 
				description="Title your project"
				:input-style="inputStyle">
			</form-input>
			<form-input 
				label="Project Description" 
				type="textarea" 
				placeholder="Description" 
				description="Provide a brief description for your project"
				:input-style="textareaStyle">
			</form-input>
		</template>
		<template v-else>
			<h2><u>{{project.name}}</u></h2>
			<p>
				{{project.description}}
			</p>
		</template>
  	</div>
  	<div class="contentBody">

  	</div>
  </div>
</template>

<script>

import FormInput from '@/components/FormInput.vue'

export default {
  components: {
  	FormInput
  },
  name: 'maincontent',
  data() {
  	return {
  		inputStyle: {
  			padding: '5px'
    	},
    	textareaStyle: {
    		backgroundColor: '#ddd',
    		padding: '5px'
    	},
    	newProject: true,
    	project: {
    		name: "Project Name",
    		description: "Small description here"
    	}
  	}
  }
}

</script>

<style scoped>
	.content {
		display: grid;
		grid-template-columns: 1fr; 
		padding: 20px;
	}

	.contentHeader {
		display: grid;
		grid-template-columns: 1fr;
		grid-gap: 5px;
	}
</style>