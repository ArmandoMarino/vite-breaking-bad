<script>
export default {
    name: 'DropMenu',
    data() {
        return {
            selected: ''
        }
    },
    props: {
        options: Array
    },
    emits: ['selected-change']
}
</script>

<template>
    <div class="dropdown">
        <label for="options">Choose type:</label>
        <select v-model="selected" name="options" id="options" @click="$emit('selected-change', selected)">
            <option value="">---</option>
            <option v-for="option in options" :value="option">{{ option }}</option>
        </select>
    </div>
</template>

<style>

</style>