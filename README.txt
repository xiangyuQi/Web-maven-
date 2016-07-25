10990 漆翔宇
1.创建WEB项目
mvn archetype:generate -DgroupId=com.hand -DartifactId=webTest -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false -DarchetypeCatalog=local
2.添加jetty plugin
<plugins>
      <plugin>
                <groupId>org.eclipse.jetty</groupId>
                <artifactId>jetty-maven-plugin</artifactId>
                <version>9.2.11.v20150529</version>
                <configuration>
                    <webAppConfig>
                        <allowDuplicateFragmentNames>true</allowDuplicateFragmentNames>
                    </webAppConfig>
                </configuration>
            </plugin>
    </plugins>
3.启动服务器 mvn jetty:run
4.访问localhost:8080
备注

	<properties>  
	        <!-- 文件拷贝时的编码 -->  
	        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>  
	       <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>  
	        <!-- 编译时的编码 -->  
	        <maven.compiler.encoding>UTF-8</maven.compiler.encoding>  
    </properties>  
   

