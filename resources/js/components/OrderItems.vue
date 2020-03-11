<template>
  <tbody>
    <tr v-for="order in orders" :key="order.id">
      <td>{{order.id}}</td>
      <td>{{order.amount}}</td>
      <td>{{(order.isComplete) ? 'Completed' : 'Incomplete'}}</td>
      <td>
        Name: {{order.order_details.customer_name}}
        <br>
        Phone: {{order.order_details.customer_phone}}
        <br>
        Address: {{order.order_details.customer_address}}
      </td>
      <td>
        <!-- icons taken from https://coolsymbol.com -->
        <button class="btn btn-success mr-3">✔</button>
        <button class="btn btn-warning">✘</button>
      </td>
    </tr>
  </tbody>
</template>

<script>
export default {
  props: ["orders"]
};
</script>
