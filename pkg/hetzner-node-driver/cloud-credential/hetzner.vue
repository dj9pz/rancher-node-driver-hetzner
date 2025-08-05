<script setup lang="ts">
    import { LabeledInput } from '@components/Form/LabeledInput';

    interface Props {
        mode: string,
        value: any,
    }

    const props = defineProps<Props>();

    const emit = defineEmits(['validationChanged']);

    async function test() {
        console.log('Testing Hetzner Cloud API token...');
        // TODO: Implement the actual test logic for the Hetzner Cloud API token
        // This is a placeholder for the actual API call to validate the token.
        return true;
    }

    const onInput = (event: any) => {
        console.log(event);
        props.value.setData('token', event.data);
        emit('validationChanged', true);
    }
</script>

<template>
    <div>
        <div class="row">
            <div class="col span-12">
                <LabeledInput
                :value="value.decodedData.token"
                class="mt-20"
                label-key="driver.hetzner.auth.fields.token.label"
                placeholder-key="driver.hetzner.auth.fields.token.placeholder"
                type="password"
                :mode="props.mode"
                @input="onInput"
                />
            </div>
        </div>
    </div>
</template>