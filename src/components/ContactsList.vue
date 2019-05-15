<template>
  <table class="table">
    <thead>
      <th>Id</th>
      <th>Name</th>
      <th>Address</th>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>Pavel</td>
        <td>Botanicheskaya</td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  data: {
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
};
</script>
<style scoped>
</style>