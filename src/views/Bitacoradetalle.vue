<template>
    <h1>Detalle de la bitacora</h1>
    <div class="flex items-start justify-start w-full">
        <div class="flex flex-col bg-gray-900 text-white p-4 justify-center items-start">
            <h1>ID: {{ID}}</h1>
        </div>

    </div>
</template>
<script>
export default {
    props:['ID'],
    setup(props) {
        console.log(props.ID);
    },
};
</script>
<style scoped>

</style>