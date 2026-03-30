<template>
    <NuxtLink to="/" class="group relative bg-zinc-900 rounded-xl overflow-hidden border hover:shadow-2xl transition-all duration-300" :class="`${rarity?.borderColor} ${rarity?.glowColor}`">
        <div class="relative aspect-square overflow-hidden bg-gradient-to-br flex items-center justify-center" :class="`${artwork?.gradient}`">
            <!-- emoji -->
            <span className="text-[120px] group-hover:scale-110 transition-transform duration-500">
              {{artwork?.emoji}}
            </span>

            <!-- rarity badge -->
            <div class="absolute top-3 right-3 px-3 py-1 backdrop-blur-sm rounded-full border" :class="`${rarity?.bgColor} ${rarity?.borderColor}`">
                <div class="flex items-center gap-1.5" :class="`${rarity?.color}`">
                    <Icon name="streamline-ultimate:reward-stars-2" class="text-xl group-hover:translate-x-1 transition-transform"/>
                    <span class="text-xs font-medium">{{ rarity?.label }}</span>
                </div>
            </div>
            
            <!-- favorite -->
            <button class="absolute top-3 left-3p-2 bg-zinc-900/80 backdrop-blur-sm rounded-full border border-zinc-700 hover:border-red-500 transition-all opacity-0 group-hover:opacity-100">
                <Icon name="ic:outline-favorite" class="text-xl transition-all" :class="`${favorite ? 'text-red-500' : 'text-zinc-400'}`"/>
            </button>
            
            <!-- stats -->
            <div class="absolute bottom-0 left-0 right-0 p-4 opacity-0 group-hover:opacity-100 transition-opacity">
                <div class="flex items-center gap-4 text-xs text-zinc-300">
                    <div class="flex items-center gap-1">
                        <Icon name="ic:round-remove-red-eye" class="text-xl"/>
                        <span>{{artwork?.views?.toLocaleString('ru-RU')}}</span>
                    </div>
                    <div class="flex items-center gap-1">
                        <Icon name="ic:round-remove-red-eye" class="text-xl"/>
                        <span>{{artwork?.likes?.toLocaleString('ru-RU')}}</span>
                    </div>
                </div>
            </div>
        </div>
    </NuxtLink>
</template>