# Spring-Boot
Spring MVC based examples
Spring Boot
An approach to develop spring based application with very lesser (no configuration)
Provides defaults for code and annotation configuration & set of starter POMs build files

@SpringBootApplication  ----> @EnableAutoConfiguration @Componentsacn  @SpringBootConfiguration


Annotations

@Component makes java class as Bean so that component scan mechanism can pick it up.

@Service  behaves hust like component annotation on service layer

@Repository suitable need for Data Access Object (DOA) layer

@Controller makes the class as a spring MVC controller

@Bean used to explicitly declare a single bean

@Configuration makes the class contains one or more beans defined inside config class

@RestControl combines @Controller @ResponseBody which eliminates evry request handling method of 
			 that class with @ResponseBody annotation.

@Autowired
Advantages
less code because we don't need to write the code to inject the dependency explicitly.
reduces development time by removing the necessity of specifying properties and construct arguments
DisAdvantages
less exact       overriding possibility          confusing nature

@Autowired in Setter and Constructor
Setter																Constructor
Setter methods set dependency managed 								Constructor injection uses constructor
by Spring IOV container.											to inject dependency on any spring.

does not ensures dependency injection								does ensures dependency injection

Security override													No security override

Stereotype Annotation : fulfills a role within an Application 
						reduce spring XML
eg:  @component  ----> @Controller @Service @Repository

Spring's Dispatcher Servlet: 
Acts as a FRONT CONTROLLER between the spring application and its clients. The Dispatcher Servlet intercepts al requests coming to the application and consults the handler mapping for which controller to be involved to handle  the requests.

HandlerMapping:
is responsible to find appropriate controllers that handle specific requests. The mapping between requets URLs and controller classes is doner via XML congig or annotations.

Controllerl:
is reponsible to process the requets by calling other bussiness/service classes. The output can be attached to model objects which will be sent to the view. To know which view will be rendered, the controller consults the view resolver.

View Resolver:
Finds the physical view filed from the logical names.

View: Physical view files which can be JSP, HTML, XML.
