<template>
    <button @click="dialogFormVisable = true">打开</button>
    <el-dialog 
    v-model="dialogFormVisable"
    :before-close="beforeClose"
    title="添加权限"
    width="500"
    >
    <el-form
        ref="formRef"
        label-width="100ox"
        label-position="left"
        :model="form"
    >

    </el-form>
    </el-dialog>

</template>


<script setup>
import { ref, reactive} from 'vue'
//form数据


//弹窗的显示隐藏
const dialogFormVisable = ref(false)

const beforeClose =() => {
    dialogFormVisable.value = false
}

</script>
<style lang="less" scoped></style>