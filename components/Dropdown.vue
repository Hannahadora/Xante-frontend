<template>
  <div class="custom-select" :tabindex="tabindex" @blur="open = false">
    <div class="selected" :class="{ open: open }" @click="open = !open">
      {{ dTitle }}
    </div>
    <div class="items" :class="{ selectHide: !open }">
      <div
        v-for="(option, i) in options"
        :key="i"
        @click="
          selected = option;
          open = false;
          $emit('input', option);
        "
      >
      {{ option.name }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    dTitle: {
      type: String,
      required: true
    },
    options: {
      type: Array,
      required: true,
    },
    default: {
      type: String,
      required: false,
      default: null,
    },
    tabindex: {
      type: Number,
      required: false,
      default: 0,
    },
  },
  data() {
    return {
      // selected: this.default
      //   ? this.default
      //   : this.options.length > 0
      //   ? this.options[0]
      //   : null,
      selected: '',
      open: false,
    };
  },
  methods: {
   
  },
  mounted() {
    // this.$emit("input", this.selected);
  },
};
</script>
<style scoped>

.custom-select {
  position: relative;
  display: inline-block;
  text-align: left;
  width: 115px;
  border-radius: 40px;
  padding: 10px 5px;
}

.custom-select .selected {
  color: #fff;
  /* width: inherit; */
  user-select: none;
  transition: none;
  padding: 4px 8px;
  background: #1F2B4A;
  border-radius: 2px;
  max-width: 118px;
  cursor: pointer;
}

.custom-select .selected.open {
  /* border: 1px solid #ad8225; */
  border-radius: 10px 10px 0px 0px;
  width: inherit;
}

.custom-select .selected:after {
  position: absolute;
  content: "";
  top: 22px;
  right: 2px;
  width: 0;
  height: 0;
  border: 5px solid transparent;
  border-color: #fff transparent transparent transparent;
}

.custom-select .items {
  margin-top: 20px;
  color: #fff;
  padding: 24px;
  /* overflow: hidden; */
  /* border-right: 1px solid #ad8225;
  border-left: 1px solid #ad8225;
  border-bottom: 1px solid #ad8225; */
  position: absolute;
  background-color: #1F2B4A;
  width: 375px;
  z-index: 1;
}

.custom-select .items div {
  color: #fff;
  /* padding-left: 1em; */
  padding: 2px 2px;
  cursor: pointer;
  user-select: none;
}

.custom-select .items div:hover {
  background-color: #ad8225;
}

.selectHide {
  display: none;
}
</style>

</style>