<script>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

export default {
    components: {
        AuthenticatedLayout,
        Head
    },
    props: {
        users: Object
    }
}
</script>

<template>
    <Head title="Users" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 dark:text-gray-200 leading-tight">Dashboard</h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto py-2 sm:px-6 lg:px-8" v-for="user in users">
                <div class="bg-white dark:bg-gray-800 overflow-hidden shadow-sm sm:rounded-lg" >
                    <div class="p-6 text-gray-900 dark:text-gray-100"  >{{user.name}}</div>
                    <div class="p-6 text-gray-900 dark:text-gray-100"  >{{user.email}}</div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
