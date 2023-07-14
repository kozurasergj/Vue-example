<script>
export default {
  data() {
    return {
      name: '',
      surname: '',
    }
  },
  methods: {
    createUser() {},
  },
}
</script>

<template>
  <h2>Users</h2>
  <input
    type="text"
    placeholder="name"
    v-bind:value="name"
    @value="setSurname"
  />
  <input
    type="text"
    placeholder="surname"
    v-bind:value="surname"
    @value="setName"
  />
  <button @click="createUser">Add user</button>
  <div v-for="user in users">
    <p>
      <span>{{ user.name }}</span>
      <span>{{ user.surname }}</span>
    </p>
  </div>
</template>

<style scoped></style>
