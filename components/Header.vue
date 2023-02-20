<template>
    <header class="bg-red-700 text-white p-2 fixed w-full">
        <nav class="flex justify-evenly">
            <NuxtLink to="/">Kiroo Blog</NuxtLink>
            <ul class="flex justify-around">
                <li class="mx-10">
                    <NuxtLink to="/tutorial">Tutorial</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
            </ul>
        </nav>
    </header>
</template>