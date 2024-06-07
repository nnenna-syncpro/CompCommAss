<template>
    <section>
        <header>
            <h1>Users</h1>
        </header>
        <div>
            <user-data @add-user="addUser"></user-data>
            <ul>
                <!-- User data should be output in ActiveUser -->
                <active-user v-for="user in users" :key="user.id" :username="user.username" :age="user.age"></active-user>
            </ul>
        </div>
    </section>
</template>

<script>
import ActiveUser from './components/ActiveUser.vue'
import UserData from './components/UserData.vue'
    export default {
  components: { ActiveUser, UserData},
        data () {
            return {
                users: []
            }
        },
        methods: {
            addUser(username, age){
                // Add user data and ensure it contains a name and age
                const newUser = {
                    id: new Date().toISOString(),
                    username: username,
                    age: age
                };
                this.users.push(newUser);
            }
        }

    }
</script>

