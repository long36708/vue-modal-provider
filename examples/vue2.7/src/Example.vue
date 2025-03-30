<!--
 * @Author: longmo
 * @Date: 2025-03-30 17:44:55
 * @LastEditTime: 2025-03-30 18:02:05
 * @FilePath: examples/vue2.7/src/Example.vue
 * @Description:
 -->
<template>
  <div>
    <el-card title="基础使用">
      <el-button type="primary" @click="onChange()">打开弹窗</el-button>
    </el-card>
  </div>
</template>
<script setup>
import MyDialog from "./components/MyDialog/MyDialog.vue";
import { useModal } from "vue-modal-provider";
import { provide, ref } from "vue";

const msg = ref(0);
provide("test", 1);
const { show } = useModal(MyDialog, { msg: msg.value });

const onChange = () => {
  show({ msg: msg.value });
};
</script>

<style scoped></style>
