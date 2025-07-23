<script>
  import { reactive, ref } from 'vue';
  import AppProduct from './Products/AppProduct.vue';

  export default {
    name: 'HelloWorld',
    components: {
      AppProduct
    },
    setup(){
      const user = reactive({
        first_name: 'Jon',
        last_name: 'Snow'
      })

      const admin = ref({
        first_name: 'Admin',
        last_name: 'Master'
      })

      let name = 'Ícaro'

      const changeName = () => {
        alert('chegou')
        name = 'Jon Snow'
        user.first_name = 'Joãozinho'
        user.last_name = 'Silva'
        admin.value.first_name = 'Super'
      }

      return {
        user,
        name,
        admin,
        changeName
      }
    }
  }
</script>

<template>
  <div class="greetings">
    <h1 
      class="green"
      @click="changeName"
    >{{ name }}</h1>
    <h5>User</h5>
    <h1 
      class="green"
      @click="changeName"
    >{{ user.first_name }} {{ user.last_name }}</h1>
    <br><br>
    <h5>Admin</h5>
    <h1 
      class="green"
      @click="changeName"
    >{{ admin.first_name }} {{ admin.last_name }}</h1>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
