### 发布aar
1.在library 项目的build.gradle 文件最后加入发布文件依赖
    
    apply from: 'https://raw.githubusercontent.com/sdaduanbilei/artifactoy_push/master/artifactoy_push.gradle'


2.在同级的library 中新建 gradle.properties 文件 并进行如下配置

    artifactory_groupid=com.ch999.baselib // 以项目包名作为groupid
    artifactory_version=1.1.2 // aar版本号
    artifactory_user=admin // artifactoy 管理账号 密码
    artifactory_password= password
    artifactory_contextUrl=http://127.0.0.1:8081/artifactory // artifactoy 地址
    
3.在终端执行一下命令
  
      gradlew assembleRelease artifactoryPublish 
     
如下提示则发布完成

      :mylibrary:artifactoryPublish
      Deploying artifact: http://127.0.0.1:8081/artifactory/libs-release-local/com/ch999/app/mylibrary/1.1.2/mylibrary-1.1.2.pom
      Deploying artifact: http://127.0.0.1:8081/artifactory/libs-release-local/com/ch999/app/mylibrary/1.1.2/mylibrary-1.1.2.aar
      Deploying build descriptor to: http://127.0.0.1:8081/artifactory/api/build
      Build successfully deployed. Browse it in Artifactory under http://127.0.0.1:8081/artifactory/webapp/builds/MyApplication/1485322079202/2017-01-25T13:27:59.113+0800/

    BUILD SUCCESSFUL

    Total time: 1 mins 5.908 secs
