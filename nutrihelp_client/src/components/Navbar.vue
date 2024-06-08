<template>
    <nav
        class="flex-no-wrap w-full relative flex justify-between py-2 shadow-md shadow-black/5 bg-gray-800 p-4 lg:py-4 sm:flex-row sm:text-left sm:justify-between px-6 shadow sm:items-baseline">

        <div class="mb-2 sm:mb-0 flex flex-row w-full">



            <div class="mb-2 sm:mb-0 flex flex-row">
                <div class="h-10 w-10 self-center mr-2">
                    <span class="[&>svg]:w-5">
                        <img class="h-10 w-10 self-center mr-2" src="../assets/logo.svg" alt="Nutrihelp Logo">
                    </span>
                </div>
                <div>


                    <div class="text-2xl hover:text-blue-dark font-medium text-white mr-3">Nutrihelp</div>
                    <p class="text-white">Eat good</p>

                </div>
            </div>

            <ul class="flex justify-around">
                <NavItem v-for="tab in tabs" :key="tab.name" :label="tab.label" :route="tab.route"
                    :isActive="isActive(tab.route)" @click="navigate(tab.route)" />
            </ul>

            <!-- Right elements -->
            <div class="relative flex items-center justify-end ml-5 w-full">

                <a class="me-4 ml-3 text-neutral-500 hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
                    href="#">


                    <svg fill="white" class="h-6 w-6" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 95.469 95.469" xml:space="preserve"
                        stroke="#ffffff">
                        <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                        <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                        <g id="SVGRepo_iconCarrier">
                            <g>
                                <g>
                                    <rect x="71.875" y="66.208" width="5.486" height="14.061"></rect>
                                    <circle cx="74.619" cy="61.311" r="3.217"></circle>
                                    <path
                                        d="M74.457,48.639c-6.041,0-11.475,2.579-15.311,6.672l-1.068-0.492l-4.947-4.17l-8.502,8.455l-8.523-8.455l-4.947,4.17 L20.86,59.561c-1.523,0.625-2.875,1.707-3.781,3.228L0,87.296l63.133,0.028c3.273,2.104,7.154,3.339,11.324,3.339 c11.586,0,21.012-9.427,21.012-21.013C95.468,58.065,86.043,48.639,74.457,48.639z M74.457,84.438 c-8.154,0-14.787-6.634-14.787-14.787c0-8.152,6.633-14.785,14.787-14.785c8.152,0,14.785,6.633,14.785,14.785 C89.242,77.804,82.609,84.438,74.457,84.438z">
                                    </path>
                                    <path
                                        d="M44.562,51.667v0.003c0.008,0,0.02-0.002,0.029-0.002c0.004,0,0.012,0.002,0.02,0.002c0,0,0.004,0,0.006,0 c0.004,0,0.006,0,0.008,0c0.006,0,0.014-0.002,0.02-0.002c0.01,0,0.02,0.002,0.029,0.002v-0.003 c12.004,0.183,19.301-10.324,19.49-27.646C64.285,12.004,56.832,5.133,44.695,4.81V4.805c-0.02,0-0.033,0.001-0.051,0.001V4.805 c-0.012,0-0.02,0-0.027,0.001c-0.008-0.001-0.018-0.001-0.025-0.001v0.001c-0.02,0-0.033-0.001-0.049-0.001V4.81 c-12.139,0.324-19.592,7.195-19.471,19.212C25.259,41.343,32.556,51.85,44.562,51.667z">
                                    </path>
                                </g>
                            </g>
                        </g>
                    </svg>

                </a>
                <a class="me-4 text-neutral-500 hover:text-neutral-700 focus:text-neutral-700 disabled:text-black/30 dark:text-neutral-200 dark:hover:text-neutral-300 dark:focus:text-neutral-300 [&.active]:text-black/90 dark:[&.active]:text-neutral-400"
                    href="#">

                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" class="h-6 w-6">
                        <path fill-rule="evenodd"
                            d="M11.078 2.25c-.917 0-1.699.663-1.85 1.567L9.05 4.889c-.02.12-.115.26-.297.348a7.493 7.493 0 00-.986.57c-.166.115-.334.126-.45.083L6.3 5.508a1.875 1.875 0 00-2.282.819l-.922 1.597a1.875 1.875 0 00.432 2.385l.84.692c.095.078.17.229.154.43a7.598 7.598 0 000 1.139c.015.2-.059.352-.153.43l-.841.692a1.875 1.875 0 00-.432 2.385l.922 1.597a1.875 1.875 0 002.282.818l1.019-.382c.115-.043.283-.031.45.082.312.214.641.405.985.57.182.088.277.228.297.35l.178 1.071c.151.904.933 1.567 1.85 1.567h1.844c.916 0 1.699-.663 1.85-1.567l.178-1.072c.02-.12.114-.26.297-.349.344-.165.673-.356.985-.57.167-.114.335-.125.45-.082l1.02.382a1.875 1.875 0 002.28-.819l.923-1.597a1.875 1.875 0 00-.432-2.385l-.84-.692c-.095-.078-.17-.229-.154-.43a7.614 7.614 0 000-1.139c-.016-.2.059-.352.153-.43l.84-.692c.708-.582.891-1.59.433-2.385l-.922-1.597a1.875 1.875 0 00-2.282-.818l-1.02.382c-.114.043-.282.031-.449-.083a7.49 7.49 0 00-.985-.57c-.183-.087-.277-.227-.297-.348l-.179-1.072a1.875 1.875 0 00-1.85-1.567h-1.843zM12 15.75a3.75 3.75 0 100-7.5 3.75 3.75 0 000 7.5z"
                            clip-rule="evenodd" />
                    </svg>
                </a>







            </div>
        </div>
    </nav>
</template>

<script>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
import NavItem from './NavItem.vue';

export default {
    name: 'Navbar',
    components: {
        NavItem
    },
    setup() {
        const router = useRouter();
        const activePage = ref('home');
        const tabs = ref([
            { name: 'home', label: 'Home', route: 'home' },
            { name: 'about', label: 'Personal Info', route: 'about' },
            { name: 'create-ration', label: 'Create Ration', route: 'ration' },
            { name: 'close', label: 'Close', route: 'close' },
        ]);

        const navigate = (route) => {
            activePage.value = route;
            router.push({ name: route });
        };

        const isActive = (route) => {
            return activePage.value === route;
        };

        return {
            tabs,
            activePage,
            navigate,
            isActive
        };
    }
};
</script>

<style scoped>
/* Additional styles if needed */
</style>