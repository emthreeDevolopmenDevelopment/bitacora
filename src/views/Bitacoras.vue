<template>
    <div>
        <h1 class="font-semibold uppercase mb-4">Gestión de bitácoras</h1>
        <hr class="mb-4">
        <form action="" class="text-xs mb-4">
            <input type="seach" placeholder="Buscar bitácora" class="p-2 bg-gray-100 rounded mr-4">
            <button class="p-2 rounded bg-blue-100 text-blue-500">Buscar</button>
        </form>
        <tabla/>
    </div>
</template>
<script>
import Tabla from '../components/Tabla.vue'
export default {
  components: { Tabla },
    setup() {
        
    },
}
</script>
<style scoped>

</style>