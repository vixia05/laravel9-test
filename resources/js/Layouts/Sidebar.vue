<script setup>
import { ref } from 'vue';
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue';
import BreezeDropdown from '@/Components/Dropdown.vue';
import BreezeDropdownLink from '@/Components/DropdownLink.vue';
import BreezeNavLink from '@/Components/NavLink.vue';
import BreezeResponsiveNavLink from '@/Components/ResponsiveNavLink.vue';
import { Link } from '@inertiajs/inertia-vue3';

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div>
        <div class="flex">
            <!-- Start Side Bar -->
            <div class="w-64 min-h-screen p-4 rounded-r-lg bg-slate-800 bg-opacity-90">
                <!-- 1.0 Logo -->
                <div class="my-auto w-28 h-28">
                    <BreezeApplicationLogo></BreezeApplicationLogo>
                </div>
                <!-- 2.0 Menu -->
                <div class="" id="sideNav">
                    <!-- 2.0 Start Menu -->
                    <ul class="relative space-y-3">
                        <!-- ** 2.1 Global Menu **  -->
                        <!-- 2.1.1 Dashboard -->
                        <li class="relative text-white">
                            <button type="button"
                                class="flex justify-start py-1.5 px-3 space-x-4 w-full duration-150 ease-in-out rounded-lg cursor-pointer hover:bg-slate-600">
                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                    stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                    <path stroke-linecap="round" stroke-linejoin="round"
                                        d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
                                </svg>
                                <span class="my-auto text-sm font-light leading-tight center">Dashboard</span>
                            </button>
                        </li>
                        <!-- 2.1.1 Profile -->
                        <li class="relative text-white">
                            <button type="button"
                                class="flex justify-start py-1.5 px-3 space-x-4 w-full duration-150 ease-in-out rounded-lg cursor-pointer hover:bg-slate-600">
                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                    stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                    <path stroke-linecap="round" stroke-linejoin="round"
                                        d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" />
                                </svg>
                                <span class="my-auto text-sm font-light leading-tight center">Profile</span>
                            </button>
                        </li>
                        <!-- ** 2.2 Super User **  -->
                        <li class="relative text-white rounded-lg" id="superUser">
                            <BreezeDropdown align="left">
                                <template #trigger>
                                    <a
                                        class="flex justify-between py-1.5 px-3 w-full  duration-150 ease-in-out rounded-lg cursor-pointer hover:bg-slate-600">
                                        <div class="flex space-x-4">
                                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                                stroke-width="1" stroke="currentColor" class="w-6 h-6">
                                                <text y="17" class="font-sans font-semibold text-gray-300">SU</text>
                                            </svg>
                                            <span class="my-auto text-sm font-light leading-tight center">Super
                                                User</span>
                                        </div>
                                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                                            stroke-width="1.5" stroke="currentColor" class="w-4 h-4 my-auto">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
                                        </svg>
                                    </a>
                                </template>

                                <template #content>
                                    <BreezeDropdownLink as="button">
                                        test
                                    </BreezeDropdownLink>
                                    <BreezeDropdownLink as="button">
                                        test
                                    </BreezeDropdownLink>
                                </template>
                            </BreezeDropdown>
                        </li>
                    </ul>
                    <!-- End Menu -->
                </div>
            </div>
            <!-- End Side Bar -->
        </div>
    </div>
</template>
