// This is the LeftSideMenu component
<template>
    <v-navigation-drawer
    color="#12142a"
    permanent>
    <v-list>
        <v-list-item title="Device" subtitle="X-logger"></v-list-item>
        <v-divider></v-divider>
        <v-list-item link title="Device Properties"></v-list-item>
        <v-list-item link title="New user"></v-list-item>
    </v-list>
        <template v-slot:append>
            <div class="pa-2">
            <v-btn block color="white">
                Logout
            </v-btn>
        </div>
        </template>
    </v-navigation-drawer>
</template>
<script>

</script>