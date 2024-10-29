1. **安装 JDK 和 Maven**：
    - 更新软件包索引并安装 JDK 和 Maven：

   ```sh
   sudo yum update -y
   sudo amazon-linux-extras install java-openjdk11 -y
   sudo yum install maven -y
   sudo yum install git -y
   ```

2. **克隆或下载项目代码**：
    - 将项目代码放在一个目录中，例如 `/home/ec2-user/java-netty-sample`：

   ```sh
   cd /home/ec2-user
   git clone https://github.com/yunfeilu92/java-netty-sample.git
   cd java-netty-sample
   ```

3. **编译项目**：
    - 在项目根目录下运行以下命令来编译项目：

   ```sh
   mvn clean install
   ```

4. **运行 Netty 服务器**：
    - 运行以下命令来启动 Netty 服务器：

   ```sh
   java -cp target/classes:~/.m2/repository/io/netty/netty-all/4.1.68.Final/netty-all-4.1.68.Final.jar org.example.NettyServer
   ```

5. **测试 API**：
    - 服务器启动后，你可以通过浏览器或工具（如 `curl` 或 Postman）访问 API。例如：

   ```sh
   curl http://localhost:8080/api/delay/5
   ```
