# autowired
Spring 4.2.8 lombok 的 @AllArgsConstructor 需要写成 @AllArgsConstructor(onConstructor = @_({@Autowired}))
    4.3.14.RELEASE 直接写 @AllArgsConstructor 即可
    核心容器额外提供了更丰富的元数据来改进编程。
    默认 Java 8 的方法检测为 bean 属性的 getter/setter 方法。 
    如果目标 bean 只定义了一个构造函数,则它无需要指定@Autowired注解  ⭐
    @Configuration类支持构造函数注入。
    任何 SpEL 表达式用于指定@EventListener的 condition 引用到 bean（例如@beanName.method()）。
    组成注解现在可以用一个包含元注解中的数组属性的数组组件类型的元素来覆盖。例如，@RequestMapping的的String[] path 可以在组成注解用 String path 覆盖。
    @Scheduled和@Schedules现在是作为元注解用来通过属性覆盖来创建自定义的组成注解。
    @Scheduled适当支持任何范围内的 bean。
    
    
    Web 改进
      内建支持 HTTP HEAD 和 HTTP OPTIONS.
      新的组合注解 @GetMapping, @PostMapping, @PutMapping, @DeleteMapping, 和 @PatchMapping 用于 @RequestMapping。
      详见 @RequestMapping 组合变种
      新的@RequestScope, @SessionScope, 和 @ApplicationScope用于 web 范围的组合注解
      Request scope, Session scope, 和 Application scope
      新的 @RestControllerAdvice 注解是 @ControllerAdvice 和 @ResponseBody 的语义结合
      @ResponseStatus现在在类级别被支持，并被所有方法继承
      新的 @SessionAttribute 注解用于访问 session 属性 (见例子)
      新的 @RequestAttribute 注解用于访问请求属性 (见例子)
      @ModelAttribute 允许通过 binding=false 来避免数据绑定(见引用)
      错误和自定义抛出，将被统一到 MVC 异常处理器中处理
      HTTP 消息转换编码一致处理，包括默认 UTF-8 用于多部分文本内容
      静态资源处理使用配置的ContentNegotiationManager用于媒体类型计算
      RestTemplate 和 AsyncRestTemplate 支持通过DefaultUriTemplateHandler 来实现严格的URI变量编码
      AsyncRestTemplate支持请求拦截
      
      http://blog.csdn.net/changsimeng/article/details/65938158
