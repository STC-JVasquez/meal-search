<script setup>
import MealItem from './MealItem.vue'

const props = defineProps({
    meals: {
        type: Array,
        required: true,
        default: () => []
    }
})
</script>

<template>
    <div class="grid grid-cols-3 gap-5 p-8">
        <MealItem v-for="meal in meals" :key="meal.idmeal" :meal="meal" />
    </div>
    <div v-if="!meals.length" class="flex justify-center text-gray-600">
        Meals not found
    </div>
</template>
