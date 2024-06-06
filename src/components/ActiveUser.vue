<template>
    <!-- ActiveUser should output a username (h2) and age (h3) -->
    <ul>
        <li><strong><h2>Username:</h2></strong> {{username}}</li>
        <li><h3>Age:</h3> {{age}}</li>
    </ul>
</template>

<script>
    export default {
        props: ["username", "age"]
    }
</script>