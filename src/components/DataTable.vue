<template>
    <div class="data-table">
        <table border="1">
            <thead>
                <tr>
                    <th style="width: 30%;">Name</th>
                    <th style="width: 10%;">Age</th>
                    <th style="width: 10%;">Available</th>
                    <th style="width: 30%;">Last Login</th>
                </tr>
            </thead>
            <tbody>
                
                <tr v-for="user in users" :key="user.id">
                    <td>{{ user.name }}</td>
                    <td>{{ user.age }}</td>
                    <td>{{ user.available }}</td>
                    <td>{{ user.last_login }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
  
<script>
import axios from 'axios';

export default {
    name: 'DataTable',
    data() {
        return {
            users: []
        }
    },
    created() {
        this.fetchUsers();
    },
    methods: {
        async fetchUsers() {
            try {
                const response = await axios.get('https://s2grupo-b4529-default-rtdb.europe-west1.firebasedatabase.app/users.json');
                this.users = Object.values(response.data); // assuming the API returns an object where each key is a unique user id
            } catch (error) {
                console.error("Error fetching users:", error);
            }
        }
    }
}
</script>
<style scoped>
.data-table {
    flex: 1;
    text-align: center;
    overflow: auto;
    padding: 15px;
    margin-left: 8px;
    background-color: rgb(248, 249, 249);
}
</style> 
  
