<script setup>
const props = defineProps(['primeiro', 'segundo', 'opera'])
</script>

<template>
    <form class="container text-center mt-3 p-5 w-75 bg-light rounded-3 shadow">

        <input @input="props.primeiro" class="text-center form-control w-25 d-inline" type="number"
            placeholder="Primeiro número">

        <select class="mx-3 form-select d-inline" id="operacao" @change="props.opera">
            <option value="soma" class="mx-auto">+</option>
            <option value="subtrai" class="mx-auto">-</option>
            <option value="multiplica" class="mx-auto">x</option>
            <option value="divide" class="mx-auto">:</option>

        </select>
        <input @input='props.segundo' class="text-center form-control w-25 d-inline" type="number"
            placeholder="Segundo número">
    </form>
</template>