<script setup>
    const props = defineProps(['calcula'])
</script>

<template>
    <div class="container pt-1 pb-3 mt-3 text-center rounded-3 w-75 shadow-lg" id="result">
        <span class="m-3 d-block h4">RESULTADO</span>

        <span class="h2">
            {{props.calcula }}

        </span>

    </div>
</template>

<style>
#result {
  background-color: rgb(165, 181, 195);
}
</style>