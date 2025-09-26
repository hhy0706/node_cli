## 子包cli create template utils
### cli是用于执行命令 使用commander来实现命令解析，并且在package.json注册bin全局命令
###  create是用于创建项目模板，使用inquirer让用户选择模板，选择好模板并且填好项目名之后，使用npminstall包来安装依赖，也就是把模板下载到用户文件夹下，再把用户文件夹下的模板拷贝到对应项目中，使用glob获取该项目的所有文件，配合ejs实现动态模板替换。
### template存放模板。

## pnpm 
### 使用pnpm来实现monorepo 单体多项目仓库便于管理每一个子包,pnpm-workspace 文件中声明子项目中的位置，
### 两种方式在子包安装另一个子包作为依赖,第二种始终使用本地最新依赖
pnpm add @your-project/shared-ui --filter @your-project/web-app
pnpm add @your-project/shared-ui@workspace:* --filter @your-project/web-app

## changesets
最后使用changesets来管理子包的版本和改动记录以及自动发布到npm官网