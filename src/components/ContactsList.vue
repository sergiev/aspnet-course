<template>
  <table class="table">
    <thead>
      <th>Id</th>
      <th>Name</th>
      <th>Address</th>
      <th><a class="button is-primary is-rounded" v-on:click="isHidden = !isHidden" v-if="isHidden">Добавить</a>
      	<a class="delete is-small" v-if="!isHidden" v-on:click="isHidden = !isHidden"></a></th>
    </thead>
    <tbody>
    	<tr v-if="!isHidden">
    		<td> ты</td>
    		<td> kra</td>
    		<td> sav</td>
    		<td> chik</td>
    	</tr>
      <tr v-for="row in contacts" :key="row.Id">
        <td>{{ row.Id }}</td>
        <td>{{ row.Name }}</td>
        <td>{{ row.Address }}</td>
        <td><a class="button is-danger is-rounded" @click="clicked(row)">&nbsp;&nbsp;Удалить&nbsp;&nbsp;</a></td>
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
      ],
      isHidden: true
    }
  }
};
</script>
<stile scoped>
</stile>