<script >
import { ref } from 'vue'

export default {
    components: {
        
    },
    props:{
        showMenu: Boolean
    },
    setup() {

    }
}   
</script>

<template>
    <div class="bg-[#1F1D2B] fixed lg:left-0 top-0 w-28 h-full flex flex-col justify-between py-6 rounded-tr-xl rounded-br-xl z-50 transition-all" :class="[showMenu ? 'left-0':'-left-full']">
        <div>
            <ul class="pl-4">
                <li>
                    <h1 class="text-2xl text-gray-300 uppercase font-bold text-center my-5">
                        Logo
                    </h1>
                </li>
                <li class="bg-[#262837] p-4 rounded-tl-xl rounded-bl-xl"> 
                    <a href="#" class="bg-[#EC7C6A] p-4 flex justify-center rounded-xl text-white">
                        <i class="ri-home-6-line text-2xl"></i>
                    </a>
                </li>

                <li class="hover:bg-[#262837] p-4 rounded-tl-xl rounded-bl-xl group transition-colors"> 
                    <a href="#" class="group-hover:bg-[#EC7C6A] p-4 flex justify-center rounded-xl text-[#EC7C6A] group-hover:text-white transition-colors">
                        <i class="ri-store-3-line text-2xl"></i>
                    </a>
                </li>

                <li class="hover:bg-[#262837] p-4 rounded-tl-xl rounded-bl-xl group transition-colors"> 
                    <a href="#" class="group-hover:bg-[#EC7C6A] p-4 flex justify-center rounded-xl text-[#EC7C6A] group-hover:text-white transition-colors">
                        <i class="ri-inbox-line text-2xl"></i>
                    </a>
                </li>

                <li class="hover:bg-[#262837] p-4 rounded-tl-xl rounded-bl-xl group transition-colors"> 
                    <a href="#" class="group-hover:bg-[#EC7C6A] p-4 flex justify-center rounded-xl text-[#EC7C6A] group-hover:text-white transition-colors">
                        <i class="ri-settings-5-line text-2xl"></i>
                    </a>
                </li>

            </ul>    
        </div>
        <div>
            <ul class="pl-4">
                <li class="hover:bg-[#262837] p-4 rounded-tl-xl rounded-bl-xl group transition-colors"> 
                    <a href="#" class="group-hover:bg-[#EC7C6A] p-4 flex justify-center rounded-xl text-[#EC7C6A] group-hover:text-white transition-colors">
                        <i class="ri-logout-box-line text-2xl"></i>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>