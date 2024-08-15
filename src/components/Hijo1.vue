<template class="text-center">
    <div>
        <h1>Soy el hijo1</h1>
        <h2> Te llamas {{ nombre }} y tienes {{ edad }} años</h2>
        <button @click="enviar">Cambiar valores</button>
    </div>
</template>

<script setup>


    const props = defineProps({
        nombre: String,
        edad: Number,
    });

    const emit = defineEmits(['modificar'])

    const enviar = () => {
        emit('modificar', 'Vue', 9)


    };
</script>
<style lang="css" scoped>

</style>