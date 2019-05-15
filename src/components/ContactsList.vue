<template>
  <table class="table">
    <thead>
      <th style="width:65px;">ID</th>
      <th style="width:100px;">Name</th>
      <th style="width:100px;">Address</th>
      <th style="text-align: right; width: 40px;">
        <a v-on:click="isHidden = !isHidden" v-if="isHidden">
          <span class="icon has-text-success">
            <i class="fa fa-lg fa-plus-circle"></i>
          </span>
        </a>
        <a v-on:click="isHidden = !isHidden" v-if="!isHidden">
          <span class="icon has-text-danger">
            <i class="fa fa-lg fa-chevron-circle-up"></i>
          </span></a>
      </th>
    </thead>
    <tbody>
      <tr v-if="!isHidden">
        <td style="width:65px;"><input class="input is-hovered" type="text" placeholder="ID"></td>
        <td style="width:40px;"><input class="input is-hovered" type="text" placeholder="Name"></td>
        <td style="width:40px;"><input class="input is-hovered" type="text" placeholder="Address"></td>
        <td style="text-align: right; width:40px;">
          <a v-on:click="isHidden = !isHidden">
            <span class="icon has-text-success">
              <i class="fa fa-lg fa-plus-circle"></i>
            </span>
          </a>
        </td>
      </tr>
      <tr v-for="row in contacts" :key="row.Id">
        <td style="text-align:right;">{{ row.Id }}</td>
        <td>{{ row.Name }}</td>
        <td>{{ row.Address }}</td>
        <td style="text-align: right;">
          <a @click="clicked(row)">
            <span class="icon has-text-grey">
              <i class="fa fa-lg fa-times-circle"></i>
            </span></a></td>
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
        { Id: 3, Name: "Oleg", Address: "Святая Русь" }
      ],
      isHidden: true
    }
  }
};
</script>
<stile scoped>
</stile>