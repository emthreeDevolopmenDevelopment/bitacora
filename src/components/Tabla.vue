<template>
  <div class="px-10">
    <table class="border-collapse w-full shadow rounded">
      <thead>
        <tr class="text-xs leading-none uppercase bg-gray-900 text-white">
          <th class="p-3 border border-gray-300 hidden lg:table-cell">
            Nombre/Descripcion
          </th>
          <th class="p-3 border border-gray-300 hidden lg:table-cell">
            Tipos de activos
          </th>
          <th class="p-3 border border-gray-300 hidden lg:table-cell">
            Creado por
          </th>
          <th class="p-3 border border-gray-300 hidden lg:table-cell">
            Estado
          </th>
          <th class="p-3 border border-gray-300 hidden lg:table-cell"></th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(bitacoras, index) in arrayData" :key="index" class="bg-white lg:hover:bg-gray-100 flex lg:table-row flex-row lg:flex-row flex-wrap lg:flex-no-wrap mb-10 lg:mb-0 cursor-pointer">
          <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
            <span class="lg:hidden absolute top-0 left-0 bg-gray-100 text-gray-600 rounded-r mt-3 px-2 py-1 text-xs font-bold uppercase">Nombre</span>
            {{ bitacoras.NOMBRE }}
          </td>
          <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
            <span class="lg:hidden absolute top-0 left-0 bg-gray-100 text-gray-600 rounded-r mt-3 px-2 py-1 text-xs font-bold uppercase">Tipos</span>
            {{ bitacoras.TIPOS }}
          </td>
          <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
            <span class="lg:hidden absolute top-0 left-0 bg-gray-100 text-gray-600 rounded-r mt-3 px-2 py-1 text-xs font-bold uppercase">Creado por</span>
            {{ bitacoras.CREADOPOR }}
          </td>

          <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
            <span class="lg:hidden absolute top-0 left-0 bg-gray-100 text-gray-600 rounded-r mt-3 px-2 py-1 text-xs font-bold uppercase">Estado</span>
            <span class="rounded bg-green-400 text-green-700 py-1 px-3 text-xs font-bold">{{ bitacoras.ESTADO }}</span>
          </td>
          <td class="w-full lg:w-auto text-center border border-b block lg:table-cell relative lg:static overflow-hidden bg-blue-300 text-blue-800 text-xs uppercase font-bold ">
            <router-link :to="`/bitacoradetalle/${bitacoras.ID}`" class=" flex justify-center items-center h-full py-2">Editar</router-link>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { useFetch } from "../hooks/useFetch";
export default {
  components: {},
  setup() {
    return { ...useFetch("bitacoras.json") };
  }
};
</script>

<style scoped></style>
