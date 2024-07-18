<template>
    <div>
        <v-expansion-panels>
            <v-expansion-panel>
                <v-expansion-panel-header>
                    Panel 1
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                    Content for Panel 1
                </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
                <v-expansion-panel-header>
                    Panel 2
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                    Content for Panel 2
                </v-expansion-panel-content>
            </v-expansion-panel>

            <v-expansion-panel>
                <v-expansion-panel-header>
                    Panel 3
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                    Content for Panel 3
                </v-expansion-panel-content>
            </v-expansion-panel>
        </v-expansion-panels>
    </div>
</template>

<script>
export default {
    name: 'NestedExpand',
}
</script>

<style scoped>
/* Add your custom styles here */
</style>