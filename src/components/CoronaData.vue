<template>
  <div id="app">
    <div>
      <button @click="downloadExcel">엑셀로 다운받기</button>
    </div>
  </div>
</template>

<script>
import Xlsx from 'xlsx'

export default {
  name: 'App',
  data () {
    return {
      excelData: [
        {
          날짜: '2021-10-01',
          일별확진자: 1000,
        },
        {
          날짜: '2021-10-02',
          일별확진자: 2000,
        }
      ]
    }
  },
  methods: {
    downloadExcel () {
      const workBook = Xlsx.utils.book_new()
      const workSheet = Xlsx.utils.json_to_sheet(this.excelData)
      Xlsx.utils.book_append_sheet(workBook, workSheet, 'sheet')
      Xlsx.writeFile(workBook, '코로나-확진자수-일별.xlsx')
    }
  }
}
</script>

<style>
</style>
