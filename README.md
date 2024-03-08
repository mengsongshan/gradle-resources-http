# gradle-resources-http
gradle resources-http custom ignore https certs vrify

# gradle-api是gradle发布的二进制包，maven仓库没有，但是编译器源码对其有依赖，故将gradle-api.jar安装到本地maven仓库
mvn install:install-file -DgroupId=org.gradle -DartifactId=gradle-api -Dversion=7.4.2 -Dpackaging=jar -Dfile=gradle-api-7.4.2.jar

修改gradle下载三方jar的httpclient的配置类DefaultHttpSettings, 将DefaultHttpSettings重新编译后，替换gradle-resources-http-7.4.2.jar插件中相应的类。
gradle-resources-http-7.4.2.jar所在目录，参考： E:\gradle\wrapper\dists\gradle-7.4.2-bin\48ivgl02cpt2ed3fh9dbalvx8\gradle-7.4.2\lib\plugins

根据使用的gradle版本的不同，下载不同版本的gradle下resource-http源码，替换对应版本的插件。
