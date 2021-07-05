<template>
  <page-toggle-transition
    :disabled="animate.disabled"
    :animate="animate.name"
    :direction="animate.direction"
  >
    <a-directory-tree
      multiple
      default-expand-all
      @select="onSelect"
      @expand="onExpand"
    >
      <a-tree-node key="0-0" title="parent 0">
        <a-tree-node key="0-0-0" title="leaf 0-0" is-leaf />
        <a-tree-node key="0-0-1" title="leaf 0-1" is-leaf />
      </a-tree-node>
      <a-tree-node key="0-1" title="parent 1">
        <a-tree-node key="0-1-0" title="leaf 1-0" is-leaf />
        <a-tree-node key="0-1-1" title="leaf 1-1" is-leaf />
      </a-tree-node>
    </a-directory-tree>
    <router-view />
  </page-toggle-transition>
</template>

<script>
import PageToggleTransition from "../components/transition/PageToggleTransition";
import { mapState } from "vuex";

export default {
  name: "TreeView",
  components: { PageToggleTransition },
  computed: {
    ...mapState("setting", ["multiPage", "animate"]),
  },
  method: {
    onSelect(keys, event) {
      console.log("Trigger Select", keys, event);
    },
    onExpand() {
      console.log("Trigger Expand");
    },
  },
};
</script>

<style scoped>
</style>
