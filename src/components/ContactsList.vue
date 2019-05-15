<template>
  <table class="table">
    <thead>
      <th>Id</th>
      <th>Name</th>
      <th>Address</th>
    </thead>
    <tbody>
      <tr v-for="row in contacts" :key="row.Id">
        <td>{{ row.Id }}</td>
        <td>{{ row.Name }}</td>
        <td>{{ row.Address }}</td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  data: function() {
    return {
      contacts: [{
          Id: 1,
          Name: "Pavel",
          Address: "Botanicheskaya"
        },
        {
          Id: 2,
          Name: "Semen",
          Address: "Botanicheskaya"
        },
        {
          Id: 3,
          Name: "Oleg",
          Address: "Dickinstan"
        }
      ]
    }
  }
};
</script>
<stile scoped>
</stile>