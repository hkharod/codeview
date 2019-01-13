<template>
  <div class="dashboard">
  	<div class="row">
		<div class="col-3">
			<sidebar></sidebar>
		</div>
		<div class="col-9">
		</div>
    </div>
  </div>
</template>

<script>
import Sidebar from '@/components/Sidebar.vue'
export default {
  components: {
  	Sidebar
  },
  name: 'dashboard'
}

</script>
