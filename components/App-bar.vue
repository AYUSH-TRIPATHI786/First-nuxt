<template>
    <v-app-bar color='cyan' max-width="450" class='mx-auto'>
		<v-app-bar-nav-icon></v-app-bar-nav-icon>

		<v-toolbar-title>App Bar</v-toolbar-title>

		<v-spacer></v-spacer>

        <v-menu
        left
        nudge-right="15"
        :close-on-content-click= false
          
        
        >
            <template v-slot:activator= "{ on, attrs }" >
                <v-btn 
                icon
                v-bind= 'attrs'
                v-on='on' 
                class='d-none d-sm-flex'>
                    <v-badge
                        color="green"
                        :content= notifications.length
                    >
                        <v-icon>mdi-bell</v-icon>        
                    
                    </v-badge>
                </v-btn>
            </template>  

            <Notification :notifications='notifications' />
            
             
        </v-menu>

        <v-dialog
        width= '450'
        
        >
            <template v-slot:activator= "{ on, attrs }" >
                <v-btn 
                icon
                v-bind= 'attrs'
                v-on='on'
                class= "d-flex d-sm-none "
                >
                    <v-badge
                        color="green"
                        :content= notifications.length
                    >
                        <v-icon>mdi-bell</v-icon>        
                
                    </v-badge>
                </v-btn>
            </template>  

            <Notification :notifications='notifications' />
            

        </v-dialog>
		
    </v-app-bar>  
</template>

<script>
export default {
    props:[
       'notifications'
    ]
}
</script>
