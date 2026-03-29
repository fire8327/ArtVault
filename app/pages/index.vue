<template>
    <div class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gradient-to-br from-purple-900/20 via-zinc-950 to-blue-900/20 col-span-full">
        <div class="max-w-7xl mx-auto px-4 lg:px-8 py-20 text-center flex flex-col gap-8 items-center">
            <div class="flex items-center gap-2 px-4 py-1.5 bg-zinc-800/50 backdrop-blur-sm rounded-full border border-zinc-700/50 w-fit mx-auto">
                <Icon name="streamline-ultimate:reward-stars-2" class="text-purple-400 text-xl"/>
                <p class="text-sm text-zinc-300">Откройте редкое цифровое искусство</p>
            </div>

            <h1 class="text-5xl lg:text-7xl font-bold leading-tight">
                Коллекционируйте <span class="text-transparent bg-clip-text bg-gradient-to-r from-purple-400 via-pink-400 to-blue-400">уникальные</span>
                <br />
                цифровые шедевры
            </h1>

            <p class="text-lg xl:text-xl text-zinc-400 max-w-2xl mx-auto">
              Исследуйте курируемую коллекцию цифровых призведений с проверенной редкостью. 
              Каждая работа рассказывает историю, каждый тираж ограничен.
            </p>

            <div class="flex items-center max-sm:flex-col gap-4">
                <NuxtLink to="/" class="flex items-center gap-2 group px-8 py-2 bg-gradient-to-r from-purple-600 to-blue-600 rounded-xl hover:opacity-80 active:opacity-50 transition-all shadow-lg shadow-purple-500/25 hover:shadow-purple-500/40">
                    <span>Открыть галерею</span>
                    <Icon name="material-symbols:arrow-right-alt-rounded" class="text-xl group-hover:translate-x-1 transition-transform"/>
                </NuxtLink>
                <button className="px-8 py-2 bg-zinc-800 hover:opacity-80 active:opacity-50 rounded-xl border border-zinc-700 transition-all">
                    Узнать больше
                </button>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>