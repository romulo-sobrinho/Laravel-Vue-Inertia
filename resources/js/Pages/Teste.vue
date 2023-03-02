<template>
    <div>
        <h1>Olá {{ name }}, seja bem vindo!</h1>
    </div>
</template>


<script>
export default {
    name: "Teste",
    props: {
        name: String
    }
}

</script>
