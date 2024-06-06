<template>
    <!-- ActiveUser should output a username (h2) and age (h3) --> 
    <li><strong><h2>Username:</h2></strong> {{username}}</li>
    <li><strong><h3>Age:</h3></strong> {{age}}</li>
</template>

<script>
    export default {
        props: ["username", "age"]
    }
</script>