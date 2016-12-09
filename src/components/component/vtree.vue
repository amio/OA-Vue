<template>
  <div :class="{node: true, folder: isFolder}">
    <div class="node-title" @click="onTitleClick">
      <span :class="{toggle: true, open: isOpen}" v-if="isFolder" />
      {{model.name}}
    </div>
    <div class="node-children" v-show="isOpen" v-if="isFolder">
      <vtree v-for="model in model.children" :model="model" :onNodeClick="clickCallback" />
    </div>
  </div>
</template>

<script>
module.exports = {
  name: 'vtree',
  props: {
    model: Object,
    onNodeClick: Function
  },
  data: function () {
    return {
      isOpen: this.model.open
    }
  },
  computed: {
    isFolder: function () {
      return this.model.children && this.model.children.length > 0
    }
  },
  methods: {
    onTitleClick: function () {
      if (this.isFolder) {
        this.isOpen = !this.isOpen
      }
      this.clickCallback(this.model)
    },
    clickCallback: function (model) {
      if (this.onNodeClick) {
        this.onNodeClick(model)
      }
    }
  }
}
</script>

<style>
.node {
  margin-left: 0.5em;
}
.node-title {
  cursor: pointer;
}
.node-title:hover {
  color: white;
  background-color: #333;
}
.node-children {
  margin-left: 1em;
}
.toggle {
  display: inline-block;
  margin-left: -1.5em;
  width: 1em;
  color: black;
  text-align: center;
  line-height: 1em;
  border: 1px solid #777;
}
.toggle::after {
  content: "+";
}
.toggle.open::after {
  content: "—";
}
</style>
