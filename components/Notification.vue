<template>
	<v-card
	max-width="450"
	class='noti'        
	>
		
    	<Notification-bar/>

		<div v-for='item in notifications' :key="item.id">   
    		<div v-if="(item.type === 'concise' && item.closed===false)">
				<Concise-notification :notification='item'/>
			</div>
			<div v-if='item.type==="small" && item.closed===false'>
				<Small-image-notification :notification='item'/>
			</div>
			<div v-if='item.type==="large" && item.closed === false'>
				<Large-image-notification :notification='item'/>
			</div>	    
		</div>

  </v-card>
</template>

<script>
export default {
	props:[
		'notifications'
		]

	
}
</script>


<style >

.tile{
	margin:10px 0;
}
</style>
