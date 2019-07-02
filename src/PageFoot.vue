<template>
 <div class="block" v-if="pagination.per_page">
  <el-pagination
    background
    @current-change="handleCurrentChange"
    :current-page="pagination.current_page"
    :page-size="pagination.per_page"
    :page-sizes="[pagination.per_page]"
    layout="total, sizes, prev, pager, next, jumper"
    :total="pagination.total">
  </el-pagination>
</div>
</template>

<script>
  export default {
    name: 'page-foot',
    props: {
      pagination: {
        type: Object
      }
    },
    methods: {
      handleCurrentChange(val) {
        this.$emit('page-change', val)
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
