<template>
    <div class="relative min-h-screen flex items-center justify-center overflow-hidden bg-gradient-to-br from-purple-900/20 via-zinc-950 to-blue-900/20 col-span-full">
        <div class="mx-auto px-4 lg:px-8 py-20 text-center flex flex-col gap-8 items-center">
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
                <button class="px-8 py-2 bg-zinc-800 hover:opacity-80 active:opacity-50 rounded-xl border border-zinc-700 transition-all">
                    Узнать больше
                </button>
            </div>
        </div>
    </div>
    <div class="flex flex-col gap-16 items-center">
        <div class="flex flex-col gap-4 text-center">
            <h2 class="text-3xl lg:text-4xl font-bold">Почему ArtVault</h2>
            <p class="text-zinc-400 max-w-2xl mx-auto">
              Создано для коллекционеров, которые ценят редкость цифрового искусства
            </p>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="flex flex-col gap-4 h-full p-8 bg-zinc-900 rounded-2xl border border-zinc-800 hover:border-zinc-700 transition-all">
                <div class="p-3 bg-gradient-to-br from-purple-500 to-purple-600 rounded-xl shadow-lg w-fit flex">
                    <Icon name="ion:flash" class="text-2xl"/>
                </div>
                <h3 class="text-xl font-semibold">Мгновенные покупки</h3>
                <p class="text-zinc-400">Быстрая оплата через TON кошелёк с мгновенным доступом к вашей коллекции.</p>
            </div>
            <div class="flex flex-col gap-4 h-full p-8 bg-zinc-900 rounded-2xl border border-zinc-800 hover:border-zinc-700 transition-all">
                <div class="p-3 bg-gradient-to-br from-blue-500 to-blue-600 rounded-xl shadow-lg w-fit flex">
                    <Icon name="streamline-ultimate:reward-stars-2" class="text-2xl"/>
                </div>
                <h3 class="text-xl font-semibold">Система редкости</h3>
                <p class="text-zinc-400">Четыре уровня редкости: Обычная, Редкая, Эпическая и Легендарная.</p>
            </div>
            <div class="flex flex-col gap-4 h-full p-8 bg-zinc-900 rounded-2xl border border-zinc-800 hover:border-zinc-700 transition-all">
                <div class="p-3 bg-gradient-to-br from-pink-500 to-pink-600 rounded-xl shadow-lg w-fit flex">
                    <Icon name="mdi:shield" class="text-2xl"/>
                </div>
                <h3 class="text-xl font-semibold">Блокчейн TON</h3>
                <p class="text-zinc-400">Все покупки защищены технологией блокчейн для максимальной безопасности.</p>
            </div>
        </div>
    </div>
    <div class="flex flex-col gap-12 items-center">
        <div class="flex justify-between w-full">
            <div class="flex flex-col gap-4">
                <h2 class="text-3xl lg:text-4xl font-bold">Избранная коллекция</h2>
                <p class="text-zinc-400 max-w-2xl mx-auto">
                    Отобранные вручную шедевры от лучших художников
                </p>
            </div>
            <NuxtLink to="/" class="flex items-center gap-2 text-purple-400 hover:opacity-80 active:opacity-50 transition-colors group max-sm:hidden">
                <span>Смотреть все</span>
                <Icon name="material-symbols:arrow-right-alt-rounded" class="text-xl group-hover:translate-x-1 transition-transform"/>
            </NuxtLink>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 w-full">
            <ArtworkCard v-for="artwork in artworks" v-bind="artwork"></ArtworkCard>
        </div>
        <NuxtLink to="/" class="flex items-center gap-2 text-purple-400 hover:opacity-80 active:opacity-50 transition-colors group sm:hidden">
            <span>Смотреть все</span>
            <Icon name="material-symbols:arrow-right-alt-rounded" class="text-xl group-hover:translate-x-1 transition-transform"/>
        </NuxtLink>
    </div>
</template>

<script setup>
const artworks = [
{
    id: '1',
    title: 'Космический Дракон',
    artist: 'PixelMaster',
    price: 0.2,
    rarity: 'legendary',
    emoji: '🐉',
    gradient: 'from-purple-600 via-pink-600 to-red-600',
    description: 'Могущественный дракон, охраняющий врата космоса. Легендарная редкость.',
    edition: '1/1',
    views: 25847,
    likes: 4821,
  },
  {
    id: '2',
    title: 'Алмазная Корона',
    artist: 'CryptoKing',
    price: 0.18,
    rarity: 'legendary',
    emoji: '👑',
    gradient: 'from-yellow-500 via-amber-500 to-orange-600',
    description: 'Королевская корона из чистых алмазов. Символ власти и богатства.',
    edition: '1/1',
    views: 22134,
    likes: 4102,
  },
  {
    id: '3',
    title: 'Огненный Феникс',
    artist: 'BurnArt',
    price: 0.19,
    rarity: 'legendary',
    emoji: '🔥',
    gradient: 'from-red-600 via-orange-500 to-yellow-500',
    description: 'Вечное возрождение из пепла. Редчайший экземпляр.',
    edition: '1/1',
    views: 21543,
    likes: 3987,
  },
]
</script>