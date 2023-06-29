<script setup>
import KinstaLayout from "../Layouts/KinstaLayout.vue";
import { Link } from "@inertiajs/inertia-vue3";

defineProps({
    article: Object,
});
</script>

<template>
    <KinstaLayout>
        <article class="mx-auto mt-10 flex justify-center max-w-5xl border-b-2">
            <img
                src="/images/kinsta-logo1.png"
                class="w-80 h-80 rounded-xl mx-auto py-5"
                alt=""
            />
            <div class="text-left flex flex-col pt-5 pb-10 px-10">
                <h1 class="text-xl font-semibold mb-10">{{ article.title }}</h1>
                <p>{{ article.body }}</p>
                <Link :href="route('home')"
                class="text-indigo-600 hover:text-indigo-800 w-fit self-end font-semibold"
                >Back</Link>
            </div>
        </article>
    </KinstaLayout>
</template>