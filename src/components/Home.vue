<script lang="ts">
import { defineComponent } from 'vue'
import {
    NConfigProvider,
    NInput,
    NDatePicker,
    NSpace,
    NTabs,
    NCard,
    NTabPane,
    NSpin,
    NButton,
    NLayoutHeader
} from 'naive-ui'
import { createTheme, inputDark, datePickerDark } from 'naive-ui'
import { zhCN, dateZhCN } from 'naive-ui'

import {invoke} from '@tauri-apps/api/tauri'

invoke('run_local')

export default defineComponent({
    components: {
        NConfigProvider,
        NInput,
        NDatePicker,
        NSpace,
        NTabs,
        NCard,
        NTabPane,
        NSpin,
        NButton,
        NLayoutHeader

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
    <n-card style="margin-bottom: 16px">
        <n-layout-header>
            <n-space>
                <n-button type="primary">
                    Primary
                </n-button>
            </n-space>
        </n-layout-header>
        <n-tabs type="line" animated>
            <n-tab-pane name="devtools" tab="Dev Tools">
                Dev Tools
                <n-card>
                    11111
                </n-card>
            </n-tab-pane>
            <n-tab-pane name="office" tab="Office">
                Office
            </n-tab-pane>
            <n-tab-pane name="media" tab="Media">
                <n-space>
                    <n-spin size="large" />
                </n-space>
            </n-tab-pane>
        </n-tabs>
    </n-card>
</template>

<style scoped>
.n-layout-header {
    display: flex;
    justify-content: flex-end;
}
</style>