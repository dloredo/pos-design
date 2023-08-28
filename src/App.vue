<script >
import { ref } from 'vue'
import Sidebar from './components/shared/Sidebar.vue'

export default {
    components: {
        Sidebar
    },
    setup() {
        let showMenu = ref(false)
        let showOrders = ref(false)
        const setMenu = () => {
            showMenu.value = !showMenu.value
            showOrders.value = false
        }
        const setOrders = () => {
            showOrders.value = !showOrders.value
            showMenu.value = false
        }
        return{
            showMenu,
            showOrders,
            setMenu,
            setOrders,
        };
    }
}   
</script>

<template>
    <div class="bg-[#262837] w-full min-h-screen">
        <Sidebar :showMenu="showMenu"/>

        <!-- Menu movil -->
        <nav class="bg-[#1F1D2B] lg:hidden fixed w-full bottom-0 left-0 text-3xl text-gray-400 py-1 px-4 flex items-center justify-between rounded-tl-xl rounded-tr-xl">
            <button class="p-2 px-4">
                <i class="ri-user-line"></i>
            </button>
            <button class="p-2 px-4">
                <i class="ri-pie-chart-line"></i>
            </button>
            <button @click="setOrders()" class="p-2 px-4">
                <i class="ri-list-ordered"></i>
            </button>
            <button @click="setMenu()" class="text-white p-2 px-4">
                <i :class="[showMenu ? 'ri-close-line' : 'ri-menu-3-line']"></i>
            </button>
        </nav>

        <main class="lg:pl-28 grid grid-cols-1 lg:grid-cols-8 pb-20">
            <div class="lg:col-span-6 md:p-8 p-4">
                <header>
                    <div class="flex flex-col md:flex-row md:justify-between md:items-center gap-4 mb-6">
                        <div>
                            <h1 class="text-2xl text-gray-300">David Loredo</h1>
                            <p class="text-gray-500">20/04/2023</p>
                        </div>
                        
                        
                        <form>
                            <div class="w-full relative">
                                <i class="ri-search-line absolute left-3 top-1/2 -translate-y-1/2 text-gray-300"></i>
                                <input type="text" placeholder="Search" name="" id="" class="bg-[#1F1D2B] w-full py-2 pl-10 pr-4 rounded-lg text-gray-300 outline-none">
                            </div>
                        </form>
                    </div>

                    <nav class="text-gray-300 flex items-center justify-between md:justify-start md:gap-8 border-b mb-6">
                        <a href="#" 
                        class="relative py-2 pr-4 before:w-1/2 before:h-[2px] before:absolute before:bg-[#EC7C6A] before:left-0 before:rounded-full before:-bottom-[1px] text-[#EC7C6A]">Hot dishes</a>
                        <a href="#" class="py-2 pr-4">Cold dishes</a>
                        <a href="#" class="py-2 pr-4">Prueba dishes</a>
                        <a href="#" class="py-2 ">Hola dishes</a>

                    </nav>

                    
                </header>
                <div class="flex items-center justify-between mb-16">
                    <h2 class="text-xl text-gray-300 ">Choose dishes</h2>
                    <button class="flex items-center gap-4 text-gray-300 bg-[#1F1D2B] py-2 px-4 rounded-lg">
                        <i class="ri-arrow-down-s-line"></i>Dine in
                    </button>
                </div>
                <div class="p-8 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-14 font-semibold">
                    <div class="bg-[#1F1D2B] p-8 rounded-xl flex flex-col items-center gap-2 text-gray-300 text-center">
                        <img src="../public/photos/platillo.png" alt="" class="w-40 h-40 object-cover -mt-20 shadow-2xl rounded-full">
                        <p class="text-2xl">Titulo de prueba comida</p>
                        <span class="text-gray-400">$150</span>
                        <p class="text-gray-500">Mini descripcion</p>
                    </div>
                    <div class="bg-[#1F1D2B] p-8 rounded-xl flex flex-col items-center gap-2 text-gray-300 text-center">
                        <img src="../public/photos/platillo.png" alt="" class="w-40 h-40 object-cover -mt-20 shadow-2xl rounded-full">
                        <p class="text-2xl">Titulo de prueba comida</p>
                        <span class="text-gray-400">$150</span>
                        <p class="text-gray-500">Mini descripcion</p>
                    </div>
                    <div class="bg-[#1F1D2B] p-8 rounded-xl flex flex-col items-center gap-2 text-gray-300 text-center">
                        <img src="../public/photos/platillo.png" alt="" class="w-40 h-40 object-cover -mt-20 shadow-2xl rounded-full">
                        <p class="text-2xl">Titulo de prueba comida</p>
                        <span class="text-gray-400">$150</span>
                        <p class="text-gray-500">Mini descripcion</p>
                    </div>
                    <div class="bg-[#1F1D2B] p-8 rounded-xl flex flex-col items-center gap-2 text-gray-300 text-center">
                        <img src="../public/photos/platillo.png" alt="" class="w-40 h-40 object-cover -mt-20 shadow-2xl rounded-full">
                        <p class="text-2xl">Titulo de prueba comida</p>
                        <span class="text-gray-400">$150</span>
                        <p class="text-gray-500">Mini descripcion</p>
                    </div>
                    <div class="bg-[#1F1D2B] p-8 rounded-xl flex flex-col items-center gap-2 text-gray-300 text-center">
                        <img src="../public/photos/platillo.png" alt="" class="w-40 h-40 object-cover -mt-20 shadow-2xl rounded-full">
                        <p class="text-2xl">Titulo de prueba comida</p>
                        <span class="text-gray-400">$150</span>
                        <p class="text-gray-500">Mini descripcion</p>
                    </div>
                    <div class="bg-[#1F1D2B] p-8 rounded-xl flex flex-col items-center gap-2 text-gray-300 text-center">
                        <img src="../public/photos/platillo.png" alt="" class="w-40 h-40 object-cover -mt-20 shadow-2xl rounded-full">
                        <p class="text-2xl">Titulo de prueba comida</p>
                        <span class="text-gray-400">$150</span>
                        <p class="text-gray-500">Mini descripcion</p>
                    </div>
                </div>
            </div>
            <div class="lg:col-span-2 fixed top-0 bg-[#1F1D2B] w-full lg:w-96 lg:right-0 h-full transition-all" :class="[showOrders ? 'right-0':'-right-full']">
                <!-- Orderns -->
                <div class="relative pt-16 lg:pt-4 text-gray-300 p-8 h-full">
                    <i @click="showOrders = !showOrders" class="ri-close-line lg:hidden absolute left-4 top-4 p-2 box-content text-gray-300 bg-[#262837] rounded-lg text-xl"></i>
                    <h1 class="text-2xl my-4">Orders #500</h1>
                    <!-- Pills -->
                    <div class="flex items-center gap-4 flex-wrap mb-8">
                        <button class="bg-[#EC7C6A] text-white px-4 py-2 rounded-xl">Dine in</button>
                        <button class="text-[#EC7C6A] px-4 py-2 rounded-xl border border-gray-500">Prueba</button>
                        <button class="text-[#EC7C6A] px-4 py-2 rounded-xl border border-gray-500">Hola</button>
                    </div>
                    <!-- Products -->
                    <div class="h-[400px] md:h-[700px] lg:h-[540px] overflow-scroll">
                        <!-- Carrito -->
                        <div>
                            <div class="grid grid-cols-6 mb-4 p-4">
                                <h5 class="col-span-4">Item</h5>
                                <h5>Qty</h5>
                                <h5>Price</h5>
                            </div>
                            <!-- Products -->
                            <div class="bg-[#262837] p-4 rounded-xl mb-4">
                                <div class="grid grid-cols-6 mb-2">
                                    <!-- Product description -->
                                    <div class="col-span-4 flex items-center gap-2">
                                        <img src="../public/photos/platillo.png" alt="" class="w-10 h-10 object-cover">
                                        <div class=" text-gray-300">
                                            <h5 class="text-sm ">Nombre de producto prueba..</h5>
                                            <p class="text-xs text-gray-500">$29</p>
                                        </div>
                                    </div>
                                    <!-- Qty -->
                                    <div>
                                        <span>2</span>
                                    </div>
                                    <!-- Price -->
                                    <div>
                                        <span>$45</span>
                                    </div>
                                </div>
                                <!-- Note -->
                                <div class="grid grid-cols-6 items-center">
                                    <form class="col-span-5">
                                        <input type="text" name="" id="" 
                                        class="bg-[#1F1D2B] py-2 px-4 rounded-lg outline-none" 
                                        placeholder="Order note...">
                                    </form>
                                    <div>
                                        <button class="border border-red-500 p-2 rounded-lg">
                                            <i class="ri-delete-bin-6-line text-red-500"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                            <div class="bg-[#262837] p-4 rounded-xl mb-4">
                                <div class="grid grid-cols-6 mb-2">
                                    <!-- Product description -->
                                    <div class="col-span-4 flex items-center gap-2">
                                        <img src="../public/photos/platillo.png" alt="" class="w-10 h-10 object-cover">
                                        <div class=" text-gray-300">
                                            <h5 class="text-sm ">Nombre de producto prueba..</h5>
                                            <p class="text-xs text-gray-500">$29</p>
                                        </div>
                                    </div>
                                    <!-- Qty -->
                                    <div>
                                        <span>2</span>
                                    </div>
                                    <!-- Price -->
                                    <div>
                                        <span>$45</span>
                                    </div>
                                </div>
                                <!-- Note -->
                                <div class="grid grid-cols-6 items-center">
                                    <form class="col-span-5">
                                        <input type="text" name="" id="" 
                                        class="bg-[#1F1D2B] py-2 px-4 rounded-lg outline-none" 
                                        placeholder="Order note...">
                                    </form>
                                    <div>
                                        <button class="border border-red-500 p-2 rounded-lg">
                                            <i class="ri-delete-bin-6-line text-red-500"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                            <div class="bg-[#262837] p-4 rounded-xl mb-4">
                                <div class="grid grid-cols-6 mb-2">
                                    <!-- Product description -->
                                    <div class="col-span-4 flex items-center gap-2">
                                        <img src="../public/photos/platillo.png" alt="" class="w-10 h-10 object-cover">
                                        <div class=" text-gray-300">
                                            <h5 class="text-sm ">Nombre de producto prueba..</h5>
                                            <p class="text-xs text-gray-500">$29</p>
                                        </div>
                                    </div>
                                    <!-- Qty -->
                                    <div>
                                        <span>2</span>
                                    </div>
                                    <!-- Price -->
                                    <div>
                                        <span>$45</span>
                                    </div>
                                </div>
                                <!-- Note -->
                                <div class="grid grid-cols-6 items-center">
                                    <form class="col-span-5">
                                        <input type="text" name="" id="" 
                                        class="bg-[#1F1D2B] py-2 px-4 rounded-lg outline-none" 
                                        placeholder="Order note...">
                                    </form>
                                    <div>
                                        <button class="border border-red-500 p-2 rounded-lg">
                                            <i class="ri-delete-bin-6-line text-red-500"></i>
                                        </button>
                                    </div>
                                </div>
                            </div> 
                        </div>
                    </div>

                    

                    <!-- Submit payment -->
                    <div class="bg-[#262837] absolute w-full bottom-0 left-0 p-4">
                        <div class="flex items-center justify-between mb-4">
                            <span class="text-gray-400">Discount</span>
                            <span>$0</span>
                        </div>
                        <div class="flex items-center justify-between mb-6">
                            <span class="text-gray-400">Subtotal</span>
                            <span>$500</span>
                        </div>
                        <div>
                            <button class="bg-[#EC7C6A] w-full py-2 px-4 rounded-lg">Pagar</button>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>
    
</template>
