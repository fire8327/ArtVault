<template>
    <div class="flex flex-col items-center text-center gap-6 pt-8">
        <div class="flex items-center justify-center w-16 h-16 bg-gradient-to-br from-purple-600 to-blue-600 rounded-full">
            <Icon name="streamline-ultimate:reward-stars-2" class="text-white text-xl"/>
        </div>
        <h1 class="text-4xl md:text-5xl font-bold">О проекте ArtVault</h1>
        <p class="text-lg text-zinc-400 max-w-3xl mx-auto">ArtVault — это современный маркетплейс для коллекционирования уникальных цифровых произведений искусства с системой редкости на блокчейне TON. Мы делаем цифровое искусство доступным для всех.</p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="flex flex-col gap-2 p-4 md:p-6 bg-zinc-900 rounded-xl border border-zinc-800">
            <div class="flex items-center justify-center w-12 h-12 bg-gradient-to-br from-purple-600 to-blue-600 rounded-xl">
                <Icon name="material-symbols:target" class="text-white text-2xl"/>
            </div>
            <p class="text-xl font-bold bg-clip-text bg-gradient-to-r from-purple-400 to-blue-400">Наша миссия</p>
            <p class="text-sm text-zinc-400">Мы создаём доступную платформу для коллекционирования уникального цифрового искусства на блокчейне TON.</p>
        </div>
        <div class="flex flex-col gap-2 p-4 md:p-6 bg-zinc-900 rounded-xl border border-zinc-800">
            <div class="flex items-center justify-center w-12 h-12 bg-gradient-to-br from-purple-600 to-blue-600 rounded-xl">
                <Icon name="solar:users-group-rounded-bold" class="text-white text-2xl"/>
            </div>
            <p class="text-xl font-bold bg-clip-text bg-gradient-to-r from-purple-400 to-blue-400">Для кого мы</p>
            <p class="text-sm text-zinc-400">Для всех, кто хочет владеть частью цифровой культуры и инвестировать в редкие произведения.</p>
        </div>
        <div class="flex flex-col gap-2 p-4 md:p-6 bg-zinc-900 rounded-xl border border-zinc-800">
            <div class="flex items-center justify-center w-12 h-12 bg-gradient-to-br from-purple-600 to-blue-600 rounded-xl">
                <Icon name="material-symbols:trending-up-rounded" class="text-white text-2xl"/>
            </div>
            <p class="text-xl font-bold bg-clip-text bg-gradient-to-r from-purple-400 to-blue-400">Наше будущее</p>
            <p class="text-sm text-zinc-400">Расширение коллекции, добавление новых художников и создание крупнейшего маркетплейса на TON.</p>
        </div>
    </div>
    <div class="flex items-center max-md:flex-col justify-center gap-6">
        <div class="flex flex-col items-center text-center gap-2 flex-1">
            <p class="flex items-center justify-center w-12 h-12 bg-gradient-to-br from-purple-600 to-blue-600 rounded-full text-xl font-bold">
                1
            </p>
            <h3 class="font-semibold">Выберите работу</h3>
            <p class="text-sm text-zinc-400">Найдите понравившееся произведение в галерее</p>
        </div>
        <div class="flex flex-col items-center text-center gap-2 flex-1">
            <p class="flex items-center justify-center w-12 h-12 bg-gradient-to-br from-purple-600 to-blue-600 rounded-full text-xl font-bold">
                2
            </p>
            <h3 class="font-semibold">Оплатите в TON</h3>
            <p class="text-sm text-zinc-400">Сканируйте QR-код для быстрой оплаты</p>
        </div>
        <div class="flex flex-col items-center text-center gap-2 flex-1">
            <p class="flex items-center justify-center w-12 h-12 bg-gradient-to-br from-purple-600 to-blue-600 rounded-full text-xl font-bold">
                3
            </p>
            <h3 class="font-semibold">Владейте</h3>
            <p class="text-sm text-zinc-400">Наслаждайтесь своей коллекцией</p>
        </div>
    </div>
    <div class="p-12 bg-gradient-to-br from-purple-900/30 to-blue-900/30 rounded-3xl border border-purple-500/20 text-center">
        <h2 class="text-3xl fony-bold mb-4">Готовы начать?</h2>
        <p class="text-lg text-zinc-400 mb-8 max-w-2xl mx-auto">Присоединяйтесь к сообществу коллекционеров и начните собирать уникальное цифровое искусство уже сегодня</p>
        <NuxtLink to="/" class="flex items-center gap-2 group px-8 py-2 bg-gradient-to-r from-purple-600 to-blue-600 rounded-xl hover:opacity-80 active:opacity-50 transition-all shadow-lg shadow-purple-500/25 hover:shadow-purple-500/40 w-fit mx-auto">
            <span>Открыть галерею</span>
            <Icon name="material-symbols:arrow-right-alt-rounded" class="text-xl group-hover:translate-x-1 transition-transform"/>
        </NuxtLink>
    </div>
</template>