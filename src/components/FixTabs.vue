<template>
    <div class="l-flex flex-row justify-end fixed-tabs">
        <v-tabs v-model="tab" bg-color="#12142a" align-with-title style="width: 300px;">
            <v-tab text="Settings" value="opt1"></v-tab>
            <v-tab text="Settings" value="opt2"></v-tab>
        </v-tabs>
        <v-tabs-window v-model="tab">
            <v-tabs-window-item value="opt1">
                <v-card flat>
                    <v-card-text>
                        <span>test</span>
                    </v-card-text>
                </v-card>
            </v-tabs-window-item>
            <v-tabs-window-item value="opt2">
                <v-card flat>
                    <v-card-text>
                        <p>Toerija2</p>
                    </v-card-text>
                </v-card>
            </v-tabs-window-item>
        </v-tabs-window>
    </div>
</template>

<script>
export default {
    data: () => ({
        tab: 'opt1,opt2',
    }),
}
</script>
