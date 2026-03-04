<script setup lang="ts">
const colorMode = useColorMode()

const navLinks = [
    { label: 'Home', to: '/', icon: 'i-heroicons-home' },
    { label: 'Dashboard', to: '/dashboard', icon: 'i-heroicons-chart-bar' },
    { label: 'About', to: '/about', icon: 'i-heroicons-information-circle' },
]

function toggleColorMode() {
    colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
}
</script>

<template>
    <header
        class="sticky top-0 z-50 border-b border-gray-200 dark:border-gray-800 bg-white/80 dark:bg-gray-900/80 backdrop-blur">
        <div class="container mx-auto px-4 max-w-7xl flex items-center justify-between h-16">

            <NuxtLink to="/" class="font-bold text-xl text-primary-600">🚀 MyApp</NuxtLink>

            <nav class="hidden md:flex items-center gap-1">
                <UButton v-for="link in navLinks" :key="link.to" :to="link.to" :icon="link.icon" :label="link.label"
                    color="gray" variant="ghost" />
            </nav>

            <div class="flex items-center gap-2">
                <UButton :icon="colorMode.value === 'dark' ? 'i-heroicons-sun' : 'i-heroicons-moon'" color="gray"
                    variant="ghost" square @click="toggleColorMode" />
                <UDropdown
                    :items="[[{ label: 'Profile', icon: 'i-heroicons-user' }, { label: 'Logout', icon: 'i-heroicons-arrow-right-on-rectangle' }]]">
                    <UAvatar src="https://i.pravatar.cc/40" size="sm" />
                </UDropdown>
            </div>

        </div>
    </header>
</template>