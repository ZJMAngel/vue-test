<template>
  <div>
    <el-input
      v-if="type === 'input'"
      v-bind="$attrs"
      v-on="$listeners"
      :value="value"
    ></el-input>
    <el-tag v-if="type === 'tag'" v-bind="$attrs" v-on="$listeners">
      <slot>666</slot>
    </el-tag>
    <el-button v-if="type === 'button'" v-bind="$attrs" v-on="$listeners">
      <slot></slot>
    </el-button>
  </div>
</template>

<script>
export default {
  name: 'ElementCommonComp',
  props: {
    type: {
      type: String,
      required: true,
    },
    value: {
      type: String,
    },
  },
};
</script>
