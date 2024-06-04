<template>
    <div class="bg-red-100 flex flex-col h-screen">
        <footer>
            <ul class="mx-2 my-4 text-xs text-gray-500">
                <li class="inline-block mx-2">
                    <a href="#" class="hover:underline" @click.prevent="handleToggleDarkMode">Dark mode</a>
                </li>
            </ul>
        </footer>
    </div>
</template>
<script setup>

const emitter = useEmitter()

function handleToggleDarkMode() {
    emitter.$emit('toggleDarkMode')
}

</script>