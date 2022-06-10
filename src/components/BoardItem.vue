<template>
  <div :class="
  'board-item '
    + (selected ? 'selected ' : '')
    + (closed ? ' closed' : '')
    ">
    <i v-if="icon" :class="'icon icon-' + icon"></i>
  </div>
</template>

<script>
export default {
  name: 'BoardItem',
  
  props: {
    icon: {
      type: Number,
      required: false,
      default: 0,
    },
    selected: {
      type: Boolean,
      required: false,
      default: false,
    },
    closed: {
      type: Boolean,
      required: false,
      default: false,
    }
  }
}
</script>

<style>
.board-item {
  border: 1px solid #2c3e50;
  width: 48px;
  height: 48px;
  position: relative;
}
.selected {
  background-color: #00ff0077;
}
.closed {
  background-color: #00ff0022;
}
.icon-1 {
  background: url('../assets/icons.png') ;
}
</style>