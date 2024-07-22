// This component is used to display the selection menu for the signals. It contains a combobox for selecting the signals, a select for selecting the signal source, and text fields for displaying the buffer size, buffer duration, and displayed signal size.
<template>
    <div style="margin-top: 10px;">
        <v-row>
            <v-combobox
                fixed style="width: 20%;"
                clearable
                chips
                multiple
                variant="outlined"
                label="Signal selection"
                :items="['a1', 'a2', 'a3', 'a4', 'a5', 'a6']"
            >
            </v-combobox>
            <v-select
                    fixed style="width:213.663px"
                    label="Select signal source"
                    :items="['High speed AI', 'Accel', 'AUX signal']"
                    variant="outlined"
            ></v-select> 
            <v-text-field
                fixed style="width:276.5px;"
                label="Signal buffer size"
                model-value="1000 samples"
                variant="outlined"
                readonly
            ></v-text-field>
            <v-text-field
                fixed style="width:276.5px;"
                label="Signal buffer duration"
                model-value="1000 sample"
                variant="outlined"
                readonly
            ></v-text-field>
            <v-text-field
                fixed style="width:276.5px;"
                label="Displayed signal size"
                model-value="1000"
                variant="outlined"
                readonly
            ></v-text-field>
            <v-select
                fixed style="width:165.867px;margin-right: 5px;"
                label="Displayed signal"
                :items="['sample', 'ms', 'us']"
                variant="outlined"
            ></v-select> 
        </v-row>
</div>
</template>

<style scoped>
    .v-combobox {
        margin-left: 5px;
    }
    .v-text-field {
        margin-left: 5px;
    }
</style>