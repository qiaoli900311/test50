<template>
  <div>
    <config-button
      :radius="1"
      :plain="false"
      bg-color="#5D81F9"
      :size="12"
      :weight="false"
      :italic="false"
      :underline="false"
      color="#fff"
      vertical="center"
      inner-text="按钮"
      :url_type="0"
      :page_new_window="false"
      :href_new_window="false"
    ></config-button>
    <config-title
      :size="14"
      :weight="false"
      :italic="false"
      :underline="false"
      title-style="title-null"
      color="#000"
      vertical="left"
      inner-text="标题"
      :url_type="0"
      :page_new_window="false"
      :href_new_window="false"
    ></config-title>
    <ve-pie
      :data="vePieData"
      :grid="vePieGrid"
      :settings="vePieSettings"
      :legend="vePieLegend"
      height="300px"
    ></ve-pie>
    <config-table
      name="基础表格"
      :visible="false"
      :pagination="configTablePagination"
      :is-operation="false"
      operation-name="操作"
      :table-data="configTableTabledata"
      :table-config="configTableTableconfig"
    ></config-table>
    <v-editor
      :upload-options="vEditorUploadoptions"
      :height="400"
      :disabled="false"
    ></v-editor>
  </div>
</template>
<script>
export default {
  components: {},
  data: function() {
    return {
      pageName: "首页",
      vePieData: {
        columns: ["日期", "访问用户"],
        rows: [
          {
            日期: "1/1",
            访问用户: 1393
          },
          {
            日期: "1/2",
            访问用户: 3530
          },
          {
            日期: "1/3",
            访问用户: 2923
          },
          {
            日期: "1/4",
            访问用户: 1723
          },
          {
            日期: "1/5",
            访问用户: 3792
          },
          {
            日期: "1/6",
            访问用户: 4593
          }
        ]
      },
      vePieGrid: {
        top: 35,
        bottom: 10
      },
      vePieSettings: {
        offsetY: 180
      },
      vePieLegend: {
        top: 5
      },
      configTablePagination: [10],
      configTableTabledata: [{}],
      configTableTableconfig: [
        {
          label: "序号",
          name: "index"
        },
        {
          label: "创建时间",
          name: "creatAt"
        },
        {
          label: "修改时间",
          name: "updateAt"
        },
        {
          label: "创建人",
          name: "createBy"
        }
      ],
      vEditorUploadoptions: {
        region: "abcd",
        bucket: "abcd",
        accessKeyId: "abcd",
        accessKeySecret: "abcd",
        value: "abcd"
      }
    }
  },
  mounted: function() {},
  watch: {},
  methods: {},
  destroyed: function() {}
}
</script>
<style lang="less" scoped="scoped"></style>
