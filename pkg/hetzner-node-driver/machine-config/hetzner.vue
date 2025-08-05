<script setup lang="ts">
interface Props {
    uuid: string,
    cluster: Object,
    credentialId: string,
    provider: string,
    disabled: boolean,
    busy: boolean,
}

const props = withDefaults(defineProps<Props>(), {
    cluster: () => ({}),
    disabled: false,
    busy: false,
});
</script>

<script lang="ts">
import CreateEditView from '@shell/mixins/create-edit-view';
import { defineComponent } from "vue";
// import your mixin
export default defineComponent({
    mixins: [CreateEditView]
});
</script>

<template>
    <div>
        <div class="hetzner-config">
            Hello, world!
        </div>
    </div>
</template>