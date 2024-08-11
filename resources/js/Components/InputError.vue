<script setup>
import {computed} from 'vue';

const props = defineProps({
    messages: {
        type: [String, Array],
    },
});

const errors = computed(() => {
    return Array.isArray(props.messages) ? props.messages : [props.messages];
});
</script>

<template>
    <div v-show="messages">
        <p
            v-for="(message, index) in errors"
            :key="index"
            class="text-sm text-red-500 dark:text-red-300"
        >
            {{ message }}
        </p>
    </div>
</template>

<script>
//compu
</script>
