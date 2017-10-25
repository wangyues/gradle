apply plugin: 'java'

repositories {
	maven {
		url 'http://rnd-mirrors.huawei.com/maven/'
	}
}

sourceCompatibility = 1.8
targetCompatibility = 1.8

dependencies {
    compile "joda-time:joda-time:2.2"
    testCompile "junit:junit:4.12"
}

jar {
    baseName = 'gradle-demo'
	manifest {
        attributes 'Main-Class': 'hello.HelloWorld'
		
    }
	from configurations.compile.collect { zipTree it}
}

http://blog.csdn.net/forezp/article/details/70148833

spring cloud => http://projects.spring.io/spring-cloud/spring-cloud.html#_features
