# React + Vite

1.  pom.xml에 아래를 추가

        	<plugin>
        		<groupId>org.apache.tomcat.maven</groupId>
        		<artifactId>tomcat7-maven-plugin</artifactId>
        		<version>2.2</version>
        		<configuration>
        			<url>http://192.168.0.24:9999/manager/text</url>
        			<username>admin</username>
        			<password>1234</password>
        		</configuration>
        	</plugin>

2.vite.config.js에 아래를 추가

base: "./", // 상대 경로 설정

3.아래의 명령어 실행
npm run build && rm -rf ../src/main/resources/static && mkdir -p ../src/main/resources/static && mv dist/\* ../src/main/resources/static
