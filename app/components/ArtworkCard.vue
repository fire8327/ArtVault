<template>
    <NuxtLink to="/" class="w-full group relative bg-zinc-900 rounded-xl overflow-hidden border hover:shadow-2xl transition-all duration-300" :class="`${rarityMeta.borderColor} ${rarityMeta.glowColor}`">
        <div class="relative aspect-square overflow-hidden bg-gradient-to-br flex items-center justify-center" :class="gradient">
            <!-- emoji -->
            <span class="text-[120px] group-hover:scale-110 transition-transform duration-500">
              {{ emoji }}
            </span>

            <!-- rarity badge -->
            <div class="absolute top-3 right-3 px-3 py-1 backdrop-blur-sm rounded-full border" :class="`${rarityMeta.bgColor} ${rarityMeta.borderColor}`">
                <div class="flex items-center gap-1.5" :class="rarityMeta.color">
                    <Icon name="streamline-ultimate:reward-stars-2" class="text-xl"/>
                    <span class="text-xs font-medium">{{ rarityMeta.label }}</span>
                </div>
            </div>
            
            <!-- favorite -->
            <button type="button" class="flex absolute top-3 left-3 p-2 bg-zinc-900/80 backdrop-blur-sm rounded-full border border-zinc-700 hover:border-red-500 transition-all opacity-0 group-hover:opacity-100">
                <Icon name="ic:outline-favorite" class="text-xl transition-all" :class="favorite ? 'text-red-500' : 'text-zinc-400'"/>
            </button>
            
            <!-- stats -->
            <div class="absolute bottom-0 left-0 right-0 p-4 opacity-0 group-hover:opacity-100 transition-opacity">
                <div class="flex items-center gap-4 text-xs text-zinc-300">
                    <div class="flex items-center gap-1">
                        <Icon name="ic:round-remove-red-eye" class="text-xl"/>
                        <span>{{ views?.toLocaleString('ru-RU') }}</span>
                    </div>
                    <div class="flex items-center gap-1">
                        <Icon name="ic:baseline-favorite-border" class="text-xl"/>
                        <span>{{ likes?.toLocaleString('ru-RU') }}</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="p-4 flex flex-col gap-2">
            <div class="flex items-center justify-between">
                <div>
                    <p class="text-xs text-zinc-500">Цена</p>
                    <p class="text-lg font-semibold">{{ price }} TON</p>
                </div>
                <div class="text-right">
                    <p class="text-xs text-zinc-500">Тираж</p>
                    <p class="text-lg font-semibold">{{ edition }}</p>
                </div>
            </div>
        </div>
    </NuxtLink>
</template>

<script setup>
const RARITY_STYLES = {
    common: {
    label: 'Обычная',
    color: 'text-gray-400',
    bgColor: 'bg-gray-500/10',
    borderColor: 'border-gray-500/30',
    glowColor: 'shadow-gray-500/20',
  },
  rare: {
    label: 'Редкая',
    color: 'text-blue-400',
    bgColor: 'bg-blue-500/10',
    borderColor: 'border-blue-500/30',
    glowColor: 'shadow-blue-500/20',
  },
  epic: {
    label: 'Эпическая',
    color: 'text-purple-400',
    bgColor: 'bg-purple-500/10',
    borderColor: 'border-purple-500/30',
    glowColor: 'shadow-purple-500/20',
  },
  legendary: {
    label: 'Легендарная',
    color: 'text-amber-400',
    bgColor: 'bg-amber-500/10',
    borderColor: 'border-amber-500/30',
    glowColor: 'shadow-amber-500/20',
  },
}

const props = defineProps({
  id: { type: String, required: true },
  title: { type: String, default: '' },
  artist: { type: String, default: '' },
  price: { type: Number, required: true },
  rarity: { type: String, default: 'common' },
  emoji: { type: String, default: '' },
  gradient: { type: String, default: '' },
  description: { type: String, default: '' },
  edition: { type: String, default: '' },
  views: { type: Number, default: 0 },
  likes: { type: Number, default: 0 },
  favorite: { type: Boolean, default: false },
})

const rarityMeta = computed(() => RARITY_STYLES[props.rarity] ?? RARITY_STYLES.common)
</script>
