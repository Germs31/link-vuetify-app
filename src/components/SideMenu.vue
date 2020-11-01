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

            <v-menu v-model="menu">

            </v-menu>
        
            <v-list>
                <v-list-item-group v-model="active" active-class="black--text">
                        <div v-for="(navOption, index) in navOptions" :key="index">
                            <router-link  :to="`${navOption.path}`">
                                <v-list-item>
                                    <v-list-item-content class="mb-3">
                                        <div class="icon-cont">
                                            <v-icon class="ml-4">
                                                {{navOption.icon}}
                                                
                                            </v-icon>
                                            <v-icon small class="chevron">mdi-chevron-right</v-icon>
                                        </div>
                                        <v-list-item-subtitle align="center">{{navOption.title}}</v-list-item-subtitle>
                                    </v-list-item-content>
                                </v-list-item>
                            </router-link>
                        </div>

                </v-list-item-group>
            </v-list>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    name:'SideMenu',
    data() {
        return {
            menu: false,
            active: 0,
            navOptions: [
                {
                    title: 'Dashboard', icon: 'mdi-view-dashboard', path:'/'
                },
                {
                    title:'Account', icon: 'mdi-account-details', path:'/account'
                },
                {
                    title:'Reports', icon: 'mdi-file-chart', path:'/reports'
                },
                {
                    title:'Settings', icon: 'mdi-tune', path:'/settings'          
                } 
            ]
        }
    }
}
</script>

<style>
.icon-cont{
    display: flex;
    justify-content: center;
}

.chevron {
    position: absolute;
    left: 3px;
}
</style>