<template>
    <footer class="w-full py-10 border-t border-zinc-800/50 grid-container">
        <div class="w-full flex flex-col gap-6">
            <div class="flex justify-between max-lg:flex-col gap-8">
                <div class="flex flex-col gap-4">
                    <NuxtLink to="/" class="flex items-center gap-2">
                        <Icon name="streamline-ultimate:reward-stars-2" class="text-purple-400 text-xl"/>
                        <span class="text-lg font-semibold">ArtVault</span>
                    </NuxtLink>
                    <p class="text-zinc-400 text-sm max-w-md">
                        Откройте для себя уникальные цифровые работы. Каждая картина проверена и имеет уровень редкости.
                    </p>
                </div>
                <div class="flex flex-col gap-4">
                    <h3 class="font-semibold text-lg">Навигация</h3>
                    <div class="flex flex-col gap-2 text-sm text-zinc-400">
                        <NuxtLink to="/" class="transition-all duration-500 hover:text-white">Галерея</NuxtLink>
                        <NuxtLink to="/" class="transition-all duration-500 hover:text-white">О проекте</NuxtLink>
                        <NuxtLink to="/" class="transition-all duration-500 hover:text-white">Избранное</NuxtLink>
                    </div>
                </div>
                <div class="flex flex-col gap-4">
                    <h3 class="font-semibold text-lg">Поддержка</h3>
                    <div class="flex flex-col gap-2 text-sm text-zinc-400">
                        <NuxtLink to="/" class="transition-all duration-500 hover:text-white">Условия</NuxtLink>
                        <NuxtLink to="/" class="transition-all duration-500 hover:text-white">Конфиденциальность</NuxtLink>
                    </div>
                </div>
            </div>
            <div class="w-full h-px bg-zinc-800/50"></div>
            <p class="text-center text-sm text-zinc-500">© 2026 ArtVault. Все права защищены.</p>
        </div>
    </footer>
</template>