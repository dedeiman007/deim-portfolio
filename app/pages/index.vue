<script setup lang="ts">
useHead({ title: 'Home | MyApp' })

const features = [
    { icon: 'i-heroicons-bolt', title: 'Fast', description: 'Built on Nuxt 3 with SSR for blazing speed.' },
    { icon: 'i-heroicons-paint-brush', title: 'Beautiful UI', description: 'Powered by Nuxt UI with customizable components.' },
    { icon: 'i-heroicons-shield-check', title: 'Secure', description: 'Auth middleware and server-side validation included.' },
]
</script>

<template>
    <NuxtLayout name="default">
        <div class="space-y-16">
            <section class="text-center py-20 space-y-6">
                <UBadge label="New release" color="primary" variant="soft" />
                <h1 class="text-5xl font-extrabold text-gray-900 dark:text-white">
                    Build faster with <span class="text-primary-600">Nuxt UI</span>
                </h1>
                <p class="text-xl text-gray-500 max-w-2xl mx-auto">
                    A complete starter with auth, dark mode, and beautiful components.
                </p>
                <div class="flex justify-center gap-4">
                    <UButton label="Get Started" to="/" size="lg" icon="i-heroicons-arrow-right" trailing />
                    <UButton label="GitHub" to="https://github.com" target="_blank" color="gray" variant="outline"
                        size="lg" />
                </div>
            </section>
    
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <UCard v-for="f in features" :key="f.title" class="text-center">
                    <div class="flex flex-col items-center gap-4 p-4">
                        <div class="p-4 rounded-full bg-primary-100 dark:bg-primary-900">
                            <UIcon :name="f.icon" class="text-3xl text-primary-600" />
                        </div>
                        <h3 class="text-lg font-semibold">{{ f.title }}</h3>
                        <p class="text-gray-500 text-sm">{{ f.description }}</p>
                    </div>
                </UCard>
            </div>
        </div>
    </NuxtLayout>
</template>