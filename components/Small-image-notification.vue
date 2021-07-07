<template>
    <v-card elevation="0"  outlined >
      <v-container>
        <v-row >
          <v-col cols="8" style='padding-left:0px'>
              <v-card-title >
                {{notification.title}}
              </v-card-title>

              <v-card-subtitle >
                {{notification.text}}
              </v-card-subtitle>
          </v-col>
          <v-col cols='4' >
              <div style='padding:16px 0;'>
                <v-img :src=notification.img ></v-img>
              </div>
          </v-col>
        </v-row>
      </v-container>
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
    