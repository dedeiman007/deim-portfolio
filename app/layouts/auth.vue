<template>
    <div
        class="min-h-screen flex items-center justify-center bg-gradient-to-br from-primary-50 to-primary-100 dark:from-gray-900 dark:to-gray-800 p-4">
        <div class="w-full max-w-md">
            <div class="text-center mb-8">
                <NuxtLink to="/" class="text-3xl font-bold text-primary-600">🚀 MyApp</NuxtLink>
            </div>
            <UCard>
                <slot />
            </UCard>
        </div>
    </div>
</template>