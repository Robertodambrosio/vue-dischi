<template>
 <div class="container-input">
    <select v-model="selectVal" name= "Select Genre" id="" @change="$emit('change', selectVal)" >
        <option>Rock</option>
        <option>Pop</option>
        <option>Metal</option>
        <option>Jazz</option>
    </select>
    <button @click.prevent="$emit('change','')">View all</button>
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

<style lang="scss" scoped>
 .container-input{
        text-align: center;

        select, button{
            background-color: #2e3a46;
            margin: 0 10px;
            padding: 10px 15px;
            border: none;
            color: white;
            text-transform: uppercase;
            font-weight: bold;
        }

        button {
            background-color: #1ed760;
        }
    }
</style>