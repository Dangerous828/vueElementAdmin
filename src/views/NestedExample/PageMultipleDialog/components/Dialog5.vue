<template>
  <el-dialog
    class="Dialog5"
    width="54%"
    title="提示"
    :destroy-on-close="true"
    :close-on-click-modal="false"
    :visible.sync="dialogVisible"
  >
    <span>Dialog5</span>
    <span slot="footer" class="dialog-footer">
      <el-button @click="dialogVisible = false">取 消</el-button>
      <el-button type="primary" @click="dialogVisible = false">确 定</el-button>
    </span>
  </el-dialog>
</template>

<script>
export default {
  name: 'Dialog5',
  props: {},
  data() {
    return {
      dialogVisible: false,
      data: {}
    }
  },
  created() {},
  mounted() {},
  methods: {
    show(data) {
      this.data = data
      this.dialogVisible = true
    },
    hide() {
      this.data = {}
      this.dialogVisible = false
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/styles/public.scss';
  .Dialog5{
    @include flex();
  }
</style>
