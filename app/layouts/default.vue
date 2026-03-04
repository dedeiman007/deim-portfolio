<template>
    <div class="min-h-screen flex flex-col bg-gray-50 dark:bg-gray-950">
        <LayoutHeader />
        <main class="flex-1 container mx-auto px-4 py-8 max-w-7xl">
            <slot />
        </main>
        <LayoutFooter />
    </div>
</template>