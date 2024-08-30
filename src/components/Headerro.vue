<template>
    <header class="flex flex-col justify-center py-5">
        <h1
            class="
                text-4xl
                hover:text-5xl
                object-contain
                hover:font-black
                italic
                text-transparent
                bg-clip-text
                bg-zinc-900
                hover:bg-gradient-to-r
                from-zinc-900
                to-red-500
            "
        ></h1>
    </header>
</template>

<style>
    h1:before {
        content: "Please, kindly, fill out a list of your skills for the hiring process.";
    }
    h1:hover:before {
        content: "TELL YO SKILL";
    }
    h1:hover {
        text-align: center;
    }
</style>
