<template>
    <div>
        <h2>Liste des utilisateurs</h2>
        <UserList ref="userList" />
        <h1>Ajouter un utilisateur</h1>
        <UserForm />
    </div>
 </template>
 
 
 <script>
 import UserForm from '../components/UserForm.vue';
 import UserList from '../components/UserList.vue';
 
 
 export default {
    components: {
        UserForm,
        UserList,
    }
 };
 </script>
 