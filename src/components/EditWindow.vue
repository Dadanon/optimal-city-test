<template>
    <el-dialog
    v-model="dialogVisible"
    :title="`Name: ${name}`"
    width="30%"
  >
    <p>Change value</p>
    <el-input type="text" v-model="value"/>
    <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogVisible = false">Cancel</el-button>
        <el-button type="primary" @click="confirmChanges">
          Confirm
        </el-button>
      </span>
    </template>
  </el-dialog>
</template>

<script>
export default {
    name: 'EditWindow',
    data() {
        return {
            name: '',
            value: '',
            dialogVisible: false
        }
    },
    methods: {
        confirmChanges() {
            this.dialogVisible = false;
            this.$emit('confirm', {
                name: this.name,
                value: this.value
            })
        }
    }
}
</script>
