<template>
  <table class="table">
    <thead>
      <th>Id</th>
      <th>Name</th>
      <th>Address</th>
      <th></th>
    </thead>
    <tbody>
      <tr v-for="row in contacts" :key="row.Id">
        <td>{{ row.Id }}</td>
        <td>{{ row.Name }}</td>
        <td>{{ row.Address }}</td>
        <td><a class="button is-danger" @click="clicked(row)">Удалить</a></td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  data: function() {
    return {
      contacts: [
      	{ Id: 1, Name: "Pavel", Address: "Botanicheskaya" },
        { Id: 2, Name: "ДАННЫЕ", Address: "УДАЛЕНЫ" },
        { Id: 3, Name: "Oleg", Address: "Святая Русь"}
      ]
    }
  }
};
</script>
<stile scoped>
</stile>