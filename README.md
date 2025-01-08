# make-win-service
将java项目、springboot项目的jar包制作成window电脑开机自启服务的插件，简单易用。这个是不用联网也可以正常打包，之前在网上找了一个，需要联网才能打包成功。

## 使用说明：【可以直接仓库里的使用说明图片】

引入以下插件

```

<plugin>
    <groupId>io.github.zengziqiang</groupId>
    <artifactId>make-win-service-maven-plugin</artifactId>
    <version>1.1.RELEASE</version>
    <executions>
        <execution>
            <id>make-win-service</id>
            <phase>package</phase>
            <goals>
                <goal>make-win-service</goal>
            </goals>
        </execution>
    </executions>
    <configuration>
        <vmOptions>-Xms1024m -Xmx2048m -Dfile.encoding=UTF-8</vmOptions>
        <programArguments> --server.port=8083</programArguments>
    </configuration>
</plugin>

```

![使用说明](https://github.com/zengziqiang/make-win-service/blob/main/%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.png)
