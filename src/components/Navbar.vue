<template>
    <nav class="navbar">
        <a href="http://localhost:8080/">Home</a>
        <a href="#">Movies</a>
        <a href="#">About</a>
    </nav>
</template>
<script>
export default {
    name:'NavbarComponent',
}
</script>
<style>
    .navbar {
        background: black;
        padding: 20px;
    }

    .navbar a{
        color: white;
        text-decoration: none;
        padding: 1em;
    }
</style>