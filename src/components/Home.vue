<script lang="ts">
import { defineComponent } from 'vue'
import { NConfigProvider, NInput, NDatePicker, NSpace, NTabs, NCard, NTabPane } from 'naive-ui'
import { createTheme, inputDark, datePickerDark } from 'naive-ui'
import { zhCN, dateZhCN } from 'naive-ui'

export default defineComponent({
    components: {
        NConfigProvider,
        NInput,
        NDatePicker,
        NSpace,
        NTabs,
        NCard,
        NTabPane

    },
    setup() {
        return {
            darkTheme: createTheme([inputDark, datePickerDark]),
            zhCN,
            dateZhCN
        }
    }
})
</script>

<template>
    <n-card title="Qucik Launcher"  style="margin-bottom: 16px">
        <n-tabs type="line" animated>
            <n-tab-pane name="devtools" tab="Dev Tools">
                Dev Tools
            </n-tab-pane>
            <n-tab-pane name="office" tab="Office">
                Office
            </n-tab-pane>
            <n-tab-pane name="media" tab="Media">
                Media
            </n-tab-pane>
        </n-tabs>
    </n-card>

</template>

<style scoped>
/* .card-tabs .n-tabs-nav--bar-type {
    padding-left: 4px;
} */
</style>