<template>
 <div>
    <select v-model="selectVal" name= "" id="" @change="$emit('change', selectVal)">
        <option>Rock</option>
        <option>Pop</option>
        <option>Metal</option>
    </select>
    </div>
</template>

<script>
    export default {
        name: 'SelectGenre',
        data() {
            return {
                selectVal: ''
            }
        }
    }

    </script>

<style>

</style>