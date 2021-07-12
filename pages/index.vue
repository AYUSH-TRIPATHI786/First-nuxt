<template>
    <div>
        <App-bar 
        :notifications='notifications'
        
        />
    </div>
</template>

<script>
export default {
    data(){
		return{
			notifications:[
				{
				id:1,
				type:'concise',
				title:'Concise Notification',
				text:'This is a simple notification with a title and body.',
				img:'',
				hasNav:true,
				hasClose:  true,
				closed:false
				},
				{
				id:2,
				type:'small',
				title:'Small Image Notification',
				text:'Same as Concise Notification, but with a small image beside the notification title and body.',
				img:'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
				hasNav:true,
				hasClose: true,
				closed:false
				},
				{
				id:3,
				type:'large',
				title:'Large Image  Notification',
				text:'Same as Concise Notification, but with a large image below the notification title and body.',
				img:'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
				hasNav:true,
				hasClose: true,
				closed:false
				},
			]
		}
	}
}
</script>


 