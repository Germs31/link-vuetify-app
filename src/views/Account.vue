<template>
  <v-container>
      <v-row justify="space-around">
        <v-card width="400">
          <v-img 
            height="200"
            src="https://pbs.twimg.com/profile_images/1001185285508657152/BYHGqvm3_400x400.jpg"></v-img>
            <div class="account-header">
              <div>
                <v-card-title>
                    <v-avatar size="100">
                      <img src="https://media-exp1.licdn.com/dms/image/C5603AQHxc-JvESLp8Q/profile-displayphoto-shrink_200_200/0?e=1609977600&v=beta&t=-X0zyDl5RhWc2--HB-u66kghjBDHCZqt2Y16mPGijDE" alt="user avatar">
                    </v-avatar>
                </v-card-title>
              </div>
              <div>
                <v-card-title>John Doe</v-card-title>
                <v-card-subtitle>
                  Link Marine since, 2020
                </v-card-subtitle>
              </div>
            </div>

            <v-card-subtitle>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam tenetur ducimus doloribus eveniet at soluta iusto neque. Distinctio pariatur inventore illo? Nihil corrupti similique adipisci esse possimus amet ratione quas.</v-card-subtitle>


            <v-card-actions>
              <router-link to="/">
                <v-btn text color="primary">
                  Go to dashboard
                </v-btn>
              </router-link>
            </v-card-actions>
        </v-card>
      </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>
  .account-header{
    display: flex;
    align-items: center;
  }
</style>