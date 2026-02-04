<template>
    <div class="min-h-screen bg-black relative overflow-hidden flex items-center justify-center">
        <!-- Background Pattern -->
        <div class="absolute inset-0 opacity-10">
            <div class="grid grid-cols-12 gap-4 transform rotate-12 scale-150">
                <div v-for="i in 144" :key="i"
                    class="w-8 h-8 border border-green-500 rounded flex items-center justify-center text-green-500 text-xs">
                    {{ patternIcons[(i - 1) % 10] }}
                </div>
            </div>
        </div>

        <!-- Main Card -->
        <div
            class="relative z-10 bg-gray-900 rounded-2xl py-8 px-4 w-full max-w-md mx-4 shadow-2xl border border-gray-800">
            <!-- Profile Circle -->
            <div class="flex justify-center mb-6">
                <div @click="redirectToTg"
                    class="cursor-pointer w-20 h-20 bg-black rounded-full border-2 border-white flex items-center justify-center">
                    <img src="/icon.jpeg" class="rounded-full" alt="">
                </div>
            </div>

            <!-- Title -->
            <h1 class="text-white text-2xl font-bold text-center mb-2 leading-tight">
                🏆 BANKNIFTY SNIPER BOT(FREE BOT) 🏆
            </h1>

            <!-- Key Features Header -->
            <div class="text-white text-sm mb-3 text-center">
                <span class="text-blue-400 font-semibold">👉🏻 Key Features:</span>
            </div>

            <!-- Features List -->
            <div class="space-y-2 text-white text-sm ">
                <div class="flex items-center justify-center text-center">
                    <span>🤖 Start Your Trading Journey with Banknifty Sniper AI Bot</span>
                </div>
                <div class="flex items-center justify-center text-center">
                    <span>📊 India's Best Channel For Auto Option Tarding</span>
                </div>
                <div class="flex items-center justify-center text-center">
                    <span>🔑 Auto Option Buying In Nifty & Banknifty with BOT</span>
                </div>


            </div>

            <!-- Join Channel Text -->
            <p class="text-white text-center my-6 font-medium">
                👇🏻Click on the below link Before it Expires 👇🏻
            </p>

            <!-- Join Button with Shine Effect -->
            <div class="flex justify-center">
                <button @click="redirectToTg"
                    class="join-button relative bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-8 rounded-full transition-all duration-300 overflow-hidden transform hover:scale-105">
                    <span class="relative z-10">Join Channel</span>
                    <!-- Shine Effect -->
                    <div
                        class="shine-overlay absolute inset-0 bg-gradient-to-r from-transparent via-white/30 to-transparent transform -translate-x-full skew-x-12">
                    </div>
                </button>
            </div>

            <!-- Updated Content -->
<div class="text-sm text-white/40 leading-tight mt-4">
                Disclaimer:
Stock market investing and algorithmic trading involve significant risk. Past performance is not indicative of future results. Any information, tools, or strategies provided on this website are for educational and informational purposes only and should not be considered financial or investment advice. Users should conduct their own research or consult a qualified financial advisor before making any investment decisions. We do not guarantee profits or protection from losses.
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const redirectToTg = () => {
    window.open('https://t.me/+WAfw2vaRnQk1MDc1', '_blank')
}
const patternIcons = ['📊', '💰', '📈', '🎯', '⚡', '💹', '📋', '⏰', '🔔', '💎']
</script>

<style scoped>
@keyframes shine {
    0% {
        transform: translateX(-100%) skewX(-15deg);
    }

    100% {
        transform: translateX(200%) skewX(-15deg);
    }
}

.join-button:hover .shine-overlay {
    animation: shine 0.8s ease-in-out;
}

.join-button {
    position: relative;
    background: linear-gradient(45deg, #2563eb, #3b82f6);
    box-shadow: 0 4px 15px rgba(37, 99, 235, 0.3);
}

.join-button:hover {
    box-shadow: 0 6px 20px rgba(37, 99, 235, 0.4);
    transform: scale(1.05) translateY(-1px);
}

.join-button::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
    animation: shine-continuous 3s infinite;
    z-index: 1;
}

@keyframes shine-continuous {
    0% {
        left: -100%;
    }

    50% {
        left: 100%;
    }

    100% {
        left: 100%;
    }
}

/* Background animation */
.bg-black {
    background: radial-gradient(ellipse at center, #1a1a2e 0%, #000000 70%);
}
</style>
