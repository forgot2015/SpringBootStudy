# SpringBootStudy
#一个SpringBoot学习的工程，记录个人学习心得

## 将SpringBoot开发完的项目部署到远程服务器上：

### 第一步。本地项目打包
在pom.xml中的<build>标签内设置打包之后的名字
<finalName>helloworld</finalName>
完整的如下
````
  <build>
    <finalName>helloworld</finalName>
    <plugins>
      <plugin>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-maven-plugin</artifactId>
      </plugin>
    </plugins>
  </build>
````
### 第二步。
点击IDEA右边的 "Maven Projects" - "Lifecycle" - "package"
等待命令执行，执行完就生成jar包了，到提示的目录下找包（一般是在 target 文件夹下)

### 第三步。
把这个jar包拷贝到服务器的某目录下，如 “\tomcat\webapps”

### 第四步。
到该jar包目录下，运行命令 java -jar helloworld.jar 
等待项目启动，若失败则根据错误信息来修改

### 第五步。
打开你设置好的目录，查看你的杰作吧 比如 http://192.168.0.61:8080
