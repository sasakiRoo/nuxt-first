<template>
    <header class="bg-red-700 text-white p-2">
        <nav class="flex justify-evenly">
            <NuxtLink to="/">Kiroo Blog</NuxtLink>
            <ul class="flex justify-around">
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/posts/1">Post 1</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/posts/2">Post 2</NuxtLink>
                </li>
            </ul>
        </nav>
    </header>
</template>