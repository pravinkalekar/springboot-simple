## Introduction

This is a Simple SpringBoot application created using Maven Archetype.

Simple example shows how a command line spring application can execute an
injected bean service. Also demonstrates how you can use @Value to inject
command line args ('--name=whatever') or application properties

## Highlights -
-	Notice that the Spring Application can also be annotated with `@SpringBootApplication`, which is a convenience annotation that is equivalent to declaring `@Configuration`, `@EnableAutoConfiguration` and `@ComponentScan`.

-	Notice how we can use JUnit [`@Rule`](https://github.com/junit-team/junit4/wiki/Rules) to capture output from `System.out` and `System.err` using `org.springframework.boot.test.OutputCapture` class

```
@Rule
public OutputCapture outputCapture = new OutputCapture();
...

String output = this.outputCapture.toString();
```