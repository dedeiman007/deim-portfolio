<template>
    <footer class="border-t border-gray-200 dark:border-gray-800 bg-white dark:bg-gray-900 py-6 mt-auto">
        <div
            class="container mx-auto px-4 max-w-7xl flex flex-col sm:flex-row items-center justify-between gap-4 text-sm text-gray-500">
            <p>© {{ new Date().getFullYear() }} MyApp. All rights reserved.</p>
            <div class="flex items-center gap-4">
                <NuxtLink to="/privacy" class="hover:text-primary-500 transition-colors">Privacy</NuxtLink>
                <NuxtLink to="/terms" class="hover:text-primary-500 transition-colors">Terms</NuxtLink>
            </div>
        </div>
    </footer>
</template>