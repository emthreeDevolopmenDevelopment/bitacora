<template>
  
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 text-xs font-bold uppercase">Nombre/Descripcion</span>
                {{nombre}}
            </td>
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 text-xs font-bold uppercase">Tipos de activos</span>
                {{tiposActivos}}
            </td>
            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 text-xs font-bold uppercase">Creado por</span>
                {{creadoPor}}
            </td>

            <td class="w-full lg:w-auto p-3 text-gray-800 text-center border border-b text-center block lg:table-cell relative lg:static">
                <span class="lg:hidden absolute top-0 left-0 bg-blue-200 px-2 py-1 text-xs font-bold uppercase">Estado</span>
                <span class="rounded bg-green-400 text-green-700 py-1 px-3 text-xs font-bold">{{estado}}</span>
          	</td>
       
</template>

<script>
export default {
    props:['nombre','tiposActivos', 'creadoPor', 'estado'],
  setup(props, context) {},
};
</script>

<style scoped></style>
