# Hyena
用户余额/积分微服务
## 积分相关接口
### 增加积分
/hyena/point/increase
### 冻结积分
/hyena/point/freeze
### 解冻积分
/hyena/point/unfreeze
### 使用积分
/hyena/point/decrease
### 使用已冻结积分
/hyena/point/decreaseFrozen
### 撤销积分
/hyena/point/cancel
### 获取用户积分列表
/hyena/point/listPoint
### 获取积分明细列表
/hyena/point/listPointRecord

## 示例代码
Maven
```
<dependency>
    <groupId>io.github.alphajiang</groupId>
    <artifactId>hyena-spring-boot-starter</artifactId>
    <version>0.0.1-SNAPSHOT</version>
</dependency>
```
Gradle
```
dependencies {
    implementation("io.github.alphajiang:hyena-spring-boot-starter:0.0.1-SNAPSHOT")
}
```
Java代码
```
@SpringBootApplication
@ComponentScan({ "io.github.alphajiang.hyena" })
@MapperScan(basePackages = { "io.github.alphajiang.hyena.ds.mapper" })
@EnableTransactionManagement
public class HyenaMain {
    public static void main(String[] args) {
        new SpringApplicationBuilder(HyenaMain.class).web(WebApplicationType.SERVLET).run(args);
    }
}
```


  

