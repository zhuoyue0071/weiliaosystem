<template>
  <div>Visit</div>
</template>
<script>
export default {
  name: 'CustomerVisit',
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
