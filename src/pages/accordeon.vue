<script setup lang="ts">
    import { onErrorCaptured } from 'vue'
    import { RouterLink, RouterView } from 'vue-router/auto'
    import {ref} from 'vue'
    const sectionOpen = ref(1)
    onErrorCaptured((err, instance, info) => {
    console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
    return true
    })
</script>

<template>
    <section>
        <button class="text-xl" @pointerdown="sectionOpen=1">bouton 1</button>
        <p v-show="sectionOpen==1">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequuntur debitis quas aspernatur illum ab doloribus, repellendus eius, labore temporibus ratione amet architecto deserunt assumenda corporis est itaque adipisci quia explicabo?</p>
    </section>
    <section>
        <button class="text-xl" @pointerdown="sectionOpen=2">bouton 2</button>
        <p v-show="sectionOpen==2">Explicabo et veritatis natus impedit. Corrupti culpa repellat, repudiandae soluta vero modi qui. Facere iste voluptatem vel facilis eum sequi tenetur! Et a ipsam voluptatem iure sequi. Voluptates, illo odio!</p>
    </section>
    <section>
        <button class="text-xl" @pointerdown="sectionOpen=3">bouton 3</button>
        <p v-show="sectionOpen==3">Quos iusto dolores culpa impedit, earum odio provident est quam cum deleniti maiores? Quo voluptas suscipit dicta earum ab aspernatur. Ex voluptatum officiis quam qui praesentium sequi iste vitae obcaecati?</p>
    </section>
</template>