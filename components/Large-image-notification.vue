
<template>
    <v-card   elevation="0" outlined class='tile' >
      <v-card-title class=' text-truncate text-subtitle-2 text-sm-h6'>
        {{notification.title}}
      </v-card-title>

      <v-card-subtitle class=' text-truncate text-caption text-sm-subtitle-1'>
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
    