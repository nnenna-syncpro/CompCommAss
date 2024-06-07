<template>
    <!-- UserData should output two input fields => for name and age -->
    <div>
        <label for="">Name</label>
        <input type="text" v-model="enteredName"> 
    </div>
    <div>
        <label for="">Age</label>
        <input type="number" v-model="enteredAge">
    </div>
    <div>
        <button @click="submitUser">Add User</button>
    </div>
</template>

<script>
    export default {
        emits: ["add-user"],
        data () {
            return {
                enteredName: "",
                enteredAge: "",
            };
        },
        methods: {
            submitUser(){
                //emit add-user so that I can forward user data 
                this.$emit('add-user', this.enteredName, this.enteredAge);
            }
        }
    }
</script>