<template>
    <v-navigation-drawer
        app
        value="true"
        mini-variant
        mini-variant-width="100"
        dark
        color="primary"
        floating
        permanent>

        <v-list flat>
            <!-- here to add space -->
            <v-list-item>
                <v-list-item-content></v-list-item-content>
            </v-list-item>
        
            <v-list-item-group v-model="active" color="grey darken-4">
                <v-list-item 
                  v-for="(navOption, index) in navOptions"
                  :key="index">
                    <v-list-item-content class="mb-3">
                        <v-icon class="mb-2">{{navOption.icon}}</v-icon>
                        <v-list-item-subtitle align="center">{{navOption.title}}</v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
            </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    name:'SideMenu',
    data() {
        return {
            active: 0,
            navOptions: [
                {
                    title: 'Dashboard', icon: 'mdi-view-dashboard'
                },
                {
                    title:'Account', icon: 'mdi-account-details'
                },
                {
                    title:'Reports', icon: 'mdi-file-chart'
                },
                {
                    title:'Settings', icon: 'mdi-tune'
                } 
            ]
        }
    }
}
</script>

<style>
</style>