<template>
       <div class="bg-primary-1 px-5 py-3 rounded"><p class="text-secondary-3 text-lg text-center">{{title}}</p>
                    <p class="text-center">{{detail}}</p></div>
</template>

<script>
export default {
    props: ["title", "detail"]
}
</script>