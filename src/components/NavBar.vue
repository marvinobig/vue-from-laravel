<template>
    <nav class="p-6 shadow-lg  mx-auto max-w-[1000px] rounded-lg bg-gray-800 text-white">
        <div class="flex gap-2 justify-between items-center">
            <RouterLink class="text-[24px] hover:text-blue-300" to="/">Home</RouterLink>
            <img alt="Vue logo" class="max-w-[40px]" src="@/assets/logo.svg" />
            <RouterLink class="text-[24px] hover:text-blue-300" to="/posts">Posts</RouterLink>
        </div>
    </nav>
</template>