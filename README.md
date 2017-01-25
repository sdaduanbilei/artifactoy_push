### 发布aar
1.在library 项目的build.gradle 文件最后加入发布文件依赖
'
apply from: 'https://raw.githubusercontent.com/sdaduanbilei/artifactoy_push/master/artifactoy_push.gradle'
'
2.在同级的library 中新建 gradle.properties 文件 并进行如下配置
'

'
