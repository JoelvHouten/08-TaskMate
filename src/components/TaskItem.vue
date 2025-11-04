<script setup lang="ts">
import type { Task } from '../models/Task'

// Props ontvangen van Todo.vue
const props = defineProps<{
    task: Task
    index: number
}>()

// Emit voor verwijderen
const emit = defineEmits<{
    (e: 'delete', index: number): void
}>()
</script>

<template>
    <li
        class="list-group-item d-flex justify-content-between align-items-center"
    >
        <div>
            <input
                type="checkbox"
                class="form-check-input me-2"
                v-model="props.task.done"
            />
            <span
                :class="{ 'text-decoration-line-through text-muted': props.task.done }"
            >
                {{ props.task.text }}
            </span>
        </div>

        <button
            class="btn btn-sm btn-danger"
            @click="emit('delete', props.index)"
            >
            Verwijder
        </button>
    </li>
</template>

<style scoped>
.list-group-item {
    background-color: #101620;
    color: #e2e8f0;
    border: 1px solid rgba(255, 255, 255, 0.1);
}
</style>
