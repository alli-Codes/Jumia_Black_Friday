<template>
    <div
        class="bg-white w-52 absolute top-10 left-[-3rem] rounded drop-shadow-[0_10px_10px_rgba(0,0,0,0.2)]">
        <ul class="flex flex-col text-sm font-normal" aria-labelledby="dropdownDefault">
            <li class="p-2 hover:bg-gray-100 hover:font-semibold"><a href="" class="flex items-center px-3 gap-3">
                    <Icon icon="la:user" width="25" />
                    <p>My Account</p>
                </a></li>
            <li class="p-2 hover:bg-gray-100 hover:font-semibold"><a href="" class="flex items-center px-3 gap-3">
                    <Icon icon="la:user" width="25" />
                    <p>My Account</p>
                </a></li>
            <li class="p-2 hover:bg-gray-100 hover:font-semibold"><a href="" class="flex items-center px-3 gap-3">
                    <Icon icon="la:user" width="25" />
                    <p>My Account</p>
                </a></li>
            <li class="p-2 hover:bg-gray-100 hover:font-semibold"><a href="" class="flex items-center px-3 gap-3">
                    <Icon icon="la:user" width="25" />
                    <p>My Account</p>
                </a></li>
            <li class="p-2 hover:bg-gray-100 hover:font-semibold"><a href="" class="flex items-center px-3 gap-3">
                    <Icon icon="la:user" width="25" />
                    <p>My Account</p>
                </a></li>

        </ul>

        <footer
            class="w-full p-2 border-t-solid border-t-gray-100 border-t-2 flex justify-center text-sm text-[#f68b1e]">
            <button class="hover:bg-orange-100 h-8 px-3 rounded">LOGOUT</button>
        </footer>
    </div>
</template>

<script>
import { Icon } from '@iconify/vue';
export default {
    components: {
        Icon
    }
}
</script>