<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: left;
    color: #2c3e50;
  }

  .el-dialog {
    padding: 0;
  }
  .el-dialog .el-dialog__header {
    padding: 2px 4px 3px 10px;
    background-color: #409EFF;
    color: white;
    border-top-left-radius: 1px;
    border-top-right-radius: 1px;
  }
  .el-dialog .el-dialog__header .el-dialog__headerbtn {
    top: 5px;
    right: 6px;
  }
  .el-dialog .el-dialog__headerbtn .el-dialog__close {
    color: #C0C4CC;
  }
  .el-dialog .el-dialog__headerbtn .el-dialog__close:hover {
    color: white;
  }
  .el-dialog .el-dialog__body {
    padding: 10px 10px 5px 10px;
  }
  .el-dialog .el-dialog__footer {
    padding: 5px 10px 10px 10px;
  }

  .sent {
  }
  .sent .stroke {
    stroke: #f0c78a;
    stroke-width: 2;
    stroke-dasharray: 3,3;
  }

  .recv {
  }
  .recv .stroke {
    stroke: #cf9236;
    stroke-width: 2;
  }

  .status-running {
    color: #67C23A;
  }
  .status-stopped {
    color: #F56C6C;
  }
</style>
