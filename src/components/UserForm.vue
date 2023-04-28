<template>
    <form @submit.prevent="submitForm">
        <label for="username">Nom d'utilisateur :</label>
        <input type="text" id="username" v-model="username" required>
        <button type="submit">Ajouter</button>
    </form>
</template>


<!-- Rest of the code -->
<script>
import userModel from '../models/userModel';


export default {
   data() {
       return {
           username: '',
       };
   },
   methods: {
       submitForm() {
           userModel.addUser({ username: this.username });
           console.log('Added '+this.username)
           this.username = '';
       },
   },
};
</script>
