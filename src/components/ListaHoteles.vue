<template>
 <div v-if="!showDetails" class="contenido ml-0 sm:ml-64 ease-in-out transition-all duration-500 p-5" id="contenido">
        <h1 class="text-4xl font-bold">Listado de hoteles</h1>
        <div class="relative overflow-x-auto shadow-md sm:rounded-lg mt-16">
            <table class="w-full text-sm text-left bg-indigo-600 text-dark ">
                <thead class="text-xs text-white uppercase ">
                    <tr>
                        <th scope="col" class="px-6 py-3">
                            NIT
                        </th>
                        <th scope="col" class="px-6 py-3">
                            Nombre
                        </th>
                        <th scope="col" class="px-6 py-3">
                            Ciudad
                        </th>
                        <th scope="col" class="px-6 py-3">
                            Dirección
                        </th>
                        <th scope="col" class="px-6 py-3 text-center">
                            N° de habitaciones
                        </th>
                        <th scope="col" class="px-6 py-3 text-center">

                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b bg-indigo-100 hover:bg-indigo-200">
                        <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap">
                            846123002-2
                        </th>
                        <td class="px-6 py-4">
                            GHL Hotel Barranquilla
                        </td>
                        <td class="px-6 py-4">
                            Barranquilla
                        </td>
                        <td class="px-6 py-4">
                            Calle 106 # 50-11 Villa Santos
                        </td>
                        <td class="px-6 py-4 text-center">
                            226
                        </td>
                        <td class="px-6 py-4 flex items-center justify-center">
                            <a @click="loadComponent('Detalles')"
                                class="bg-yellow-500 p-1 rounded flex items-center justify-center font-medium text-white hover:bg-yellow-600">
                                Detalles
                            </a>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
    <component :is= "currentComponent"></component>
</template>

<script>
import 'tailwindcss/base.css';
import 'tailwindcss/components.css';
import 'tailwindcss/utilities.css';


import Detalles from './Detalles.vue';

export default{
    data() {
  return{
    currentComponent: null,
    showDetails: false
  }
    },
  methods: {
    
    loadComponent(nombreComponente) {
    if (nombreComponente === 'Detalles') {
      this.currentComponent = Detalles;
      this.showDetails = true;
    }
  },
  },
}



</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->