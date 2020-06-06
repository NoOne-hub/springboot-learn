# json



FastJson, Gson和JackSon



JSON序列化 Jackson速度最快, 优先使用jackson



Jackson常用注解

```java
@JsonPropertyOrder(value={"password", "username"}) //更换json显示默认顺序

public class User {
    @JsonIgnore //忽略
    private Integer uid;
    @JsonProperty("auther") //起别名, json传值的时候也要改名
    private String username;
    @JsonInclude(JsonInclude.Include.NON_NULL) //当其不为空的时候序列化,
    private String password;
    //@JsonFormat(pattern="yyyy-MM-dd HH:mm:ss", timezone = "GMT+8") 日期格式序列化
    private List<Comment> comments;
}
```

还可以配置xml

```xml
server.port=8888

spring.jackson.date-format= yyyy-MM-dd HH:mm:ss
spring.jackson.time-zone= GMT+8
```

