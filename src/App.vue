<script setup lang="ts">
import { onMounted, useTemplateRef } from 'vue';

import typescriptLogo from './typescript.svg'
import viteLogo from '/vite.svg'
import vueLogo from '/vue.svg'

import { setupCounter } from './counter.ts'

const btnCounter = useTemplateRef<HTMLButtonElement | null>('btn-counter')

onMounted(() => {
    setupCounter(btnCounter.value!)
})
</script>

<template>
    <div>
        <a href="https://vitejs.dev" target="_blank">
            <img :src="viteLogo" class="logo" alt="Vite logo" />
        </a>
        <a href="https://www.typescriptlang.org/" target="_blank">
            <img :src="typescriptLogo" class="logo vanilla" alt="TypeScript logo" />
        </a>
        <a href="https://vuejs.org/" target="_blank">
            <img :src="vueLogo" class="logo vue" alt="Vue logo" />
        </a>
        <h1>Vite + TypeScript + Vue</h1>
        <div class="card">
            <button id="counter" type="button" ref="btn-counter"></button>
        </div>
        <p class="read-the-docs">
            Click on the Vite and TypeScript logos to learn more
        </p>
    </div>
</template>
