
<template>
    <v-card   elevation="0" outlined >
      <v-card-title>
        {{notification.title}}
      </v-card-title>

      <v-card-subtitle>
          {{notification.text}}
      </v-card-subtitle>
      <div >
          <v-img :src='notification.img' ></v-img>
      </div> 

		<Notification-actions :notification='notification'/>
    </v-card>
    
</template>  
<script>
export default {
    props:[
       'notification'
    ]
}
</script>
    