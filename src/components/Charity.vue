<template>
<div>
  <body>
    <h2>Charity Page</h2>
    <table id="withdrawalTable" class="myWithdrawal">
      <thead>
        <tr>
          <th>Date</th>
          <th>Amount</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="row in withdrawal" :key="row.id">
          <td>{{row.Date}}</td>
          <td>{{row.Amount}}</td>
        </tr>
      </tbody>
    </table><br>
    <div class="form-group">
      <input type="number" placeholder="Amount to Withdraw" id="donation" v-model="value">
      <br>
      <button>Withdraw Amount</button>
    </div>
  </body>
</div>
</template>

<script>
export default {
  name: "Charity",
  data() {
    return {
      withdrawal: [
        { Date: "1/1/19", Amount: "200" },
        { Date: "2/1/19", Amount: "100" }
      ]
    };
  }
};
</script>
<style>
.withdraw {
  margin: 0 auto;
}

.myWithdrawal{
  margin: 0 auto;
}

.form-group {
  width: 10%;
  margin: 0 auto;
}
</style>