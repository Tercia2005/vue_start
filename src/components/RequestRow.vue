<template>
  <tr>
    <td>{{ request.employeeName }}</td>
    <td>{{ request.status }}</td>
    <td>
      <button @click="$emit('approve')">Approve</button>
      <button @click="$emit('deny')">Deny</button>
    </td>
  </tr>
</template>

<script>
export default {
  props: {
    request: {
      type: Object,
      required: true
    }
  }
};
</script>