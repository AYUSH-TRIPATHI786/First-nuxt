<template>
    <v-card-actions>
        <v-spacer></v-spacer>
        <v-btn v-if='notification.hasClose===true' @click='close' :x-small='$vuetify.breakpoint.xs'>
            Close
        </v-btn>
        <v-btn v-if='notification.hasNav===true' :x-small='$vuetify.breakpoint.xs'>
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


        