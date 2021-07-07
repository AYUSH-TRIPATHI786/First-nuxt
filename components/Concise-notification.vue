<template>
    <v-card elevation="0" outlined >
      <v-card-title>
        {{notification.title}}
      </v-card-title>
      <v-card-subtitle>
          {{notification.text}}
      </v-card-subtitle>
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
    