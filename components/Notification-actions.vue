<template>
    <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn v-if='notification.hasClose===true' @click='close'>
            Close
        </v-btn>
        <v-btn v-if='notification.hasNav===true'>
            Navigate
        </v-btn>
    </v-card-actions>
</template>

<script>
export default {
    props:[
       'notification'
    ],
    methods:{
        close(){
            this.notification.closed=true
        }
    }
}
</script>
        