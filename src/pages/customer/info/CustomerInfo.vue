<template>
  <div>Info</div>
</template>
<script>
export default {
  name: 'CustomerInfo',
  methods: {
    onSelect(keys, event) {
      console.log('Trigger Select', keys, event);
    },
    onExpand() {
      console.log('Trigger Expand');
    },
  },
};
</script>
