<template>
    <section>
        <header>
            <h1>Users</h1>
        </header>
        <div>
            <user-data></user-data>
            <ul>
                <active-user></active-user>
            </ul>
        </div>
    </section>
</template>

<script>
import ActiveUser from './components/ActiveUser.vue'
import UserData from './components/UserData.vue'
    export default {
  components: { ActiveUser, UserData},

    }
</script>

