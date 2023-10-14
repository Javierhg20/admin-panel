<template>
    <div class="contenido ml-0 sm:ml-64 ease-in-out transition-all duration-500 p-10" id="contenido">
        <h1 class="text-4xl font-bold">Agregar hotel</h1>
        <div class="container mx-auto mt-10">
            <form class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class="relative">
                    <input type="nomber" id="nit"
                        class="bg-indigo-100 block rounded-t-lg px-2.5 pb-2.5 pt-5 w-full text-sm text-gray-900 border-0 border-b-2 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-indigo-600 peer"
                        placeholder=" " />
                    <label for="nit"
                        class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-4 z-10 origin-[0] left-2.5 peer-focus:text-indigo-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-4">Ingrese
                        el NIT</label>
                    <p class="mt-1 text-sm text-red-600 font-medium">*Mensaje de error!</p>
                </div>
                <div class="relative">
                    <input type="text" id="nombre"
                        class="bg-indigo-100 block rounded-t-lg px-2.5 pb-2.5 pt-5 w-full text-sm text-gray-900 border-0 border-b-2 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-indigo-600 peer"
                        placeholder=" " />
                    <label for="nombre"
                        class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-4 z-10 origin-[0] left-2.5 peer-focus:text-indigo-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-4">Ingrese
                        el nombre del hotel</label>
                    <p class="mt-1 text-sm text-red-600 font-medium">*Mensaje de error!</p>
                </div>
                <div class="relative">
                    <input type="text" id="ciudad"
                        class="bg-indigo-100 block rounded-t-lg px-2.5 pb-2.5 pt-5 w-full text-sm text-gray-900 border-0 border-b-2 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-indigo-600 peer"
                        placeholder=" " />
                    <label for="ciudad"
                        class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-4 z-10 origin-[0] left-2.5 peer-focus:text-indigo-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-4">Ingrese
                        el nombre del hotel la ciudad</label>
                    <p class="mt-1 text-sm text-red-600 font-medium">*Mensaje de error!</p>
                </div>
                <div class="relative">
                    <input type="text" id="direccion"
                        class="bg-indigo-100 block rounded-t-lg px-2.5 pb-2.5 pt-5 w-full text-sm text-gray-900 border-0 border-b-2 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-indigo-600 peer"
                        placeholder=" " />
                    <label for="direccion"
                        class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-4 z-10 origin-[0] left-2.5 peer-focus:text-indigo-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-4">Ingrese
                        la direccion</label>
                    <p class="mt-1 text-sm text-red-600 font-medium">*Mensaje de error!</p>
                </div>
             <div class="relative">
                    <input type="text" id="habitaciones"
                        class="bg-indigo-100 block rounded-t-lg px-2.5 pb-2.5 pt-5 w-full text-sm text-gray-900 border-0 border-b-2 border-gray-300 appearance-none focus:outline-none focus:ring-0 focus:border-indigo-600 peer"
                        placeholder=" " />
                    <label for="habitaciones"
                        class="absolute text-sm text-gray-500 duration-300 transform -translate-y-4 scale-75 top-4 z-10 origin-[0] left-2.5 peer-focus:text-indigo-600 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-4">Ingrese
                        el numero de habitaciones</label>
                    <p class="mt-1 text-sm text-red-600 font-medium">*Mensaje de error!</p>
                </div>
            </form>
            <div class="flex justify-between items-center mt-10">
                <button @click="openMesaje" type="button"  
                    class="text-gray-950  bg-gradient-to-r from-green-400 via-green-500 to-green-600 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-green-300 dark:focus:ring-green-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center mr-2 mb-2">
                    Agregar
                </button>
                <a href="../App.vue" type="button"
                    class="text-gray-950 bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center mr-2 mb-2">Regresar</a>
            </div>
        </div>
    </div>

    <div v-if="showModal" class="fixed z-10 inset-0 overflow-y-auto">
    <div class="flex items-end justify-center min-h-screen pt-4 px-4 pb-20 text-center sm:block sm:p-0">
      <div class="fixed inset-0 transition-opacity">
        <div class="absolute inset-0 bg-gray-500 opacity-75"></div>
      </div>
      <div class="inline-block align-bottom bg-white rounded-lg text-left overflow-hidden shadow-xl transform transition-all sm:my-8 sm:align-middle sm:max-w-lg sm:w-full">
        <div class="bg-white px-4 pt-5 pb-4 sm:p-6 sm:pb-4">
          <h2 class="text-lg leading-6 font-medium text-gray-900">Agregar Hotel</h2>
          <div class="mt-2">
            <p class="text-sm leading-5 text-gray-500">¿Desea  Guardar El nuevo Hotel?</p>
          </div>
        </div>
        <div class="bg-gray-50 px-4 py-3 sm:px-6 sm:flex sm:flex-row-reverse">
          <span class="flex w-full rounded-md shadow-sm sm:ml-3 sm:w-auto">
            <button @click="confirm" class="inline-flex justify-center w-full rounded-md border border-transparent px-4 py-2 bg-red-600 text-base leading-6 font-medium text-white shadow-sm hover:bg-red-500 focus:outline-none focus:border-red-700 focus:shadow-outline-red transition ease-in-out duration-150 sm:text-sm sm:leading-5">Aceptar</button>
          </span>
          <span class="mt-3 flex w-full rounded-md shadow-sm sm:mt-0 sm:w-auto">
            <button @click="cancel" class="inline-flex justify-center w-full rounded-md border border-gray-300 px-4 py-2 bg-white text-base leading-6 font-medium text-gray-700 shadow-sm hover:text-gray-500 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue transition ease-in-out duration-150 sm:text-sm sm:leading-5">Cancelar</button>
          </span>
        </div>
      </div>
    </div>
  </div>

</template>
<script>
import Swal from 'sweetalert2';

export default{
    data(){
        return{
            showModal: false
        }
    },
    methods:{
        openMesaje(){
            this.showModal= true;
        },
        confirm(){
            this.showModal = false;

            Swal.fire({
                icon: 'success',
                title: '¡ GUARDADO !',
                text: 'El Hotel se Agrego con Exito.'
            })
        },
        cancele(){
            this.showModal = false;
        },
    }
}
</script>