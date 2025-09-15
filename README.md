# Complete Java/Spring Boot Interview Preparation Guide 2025

## Study Plan Overview

• Beginner Level: 2-3 weeks preparation
• Intermediate Level: 3-4 weeks preparation
• Advanced Level: 4-6 weeks preparation

---

## LEVEL 1: BEGINNER (0-2 Years Experience)

### Core Java Fundamentals

#### Basic Concepts

1. **What is the difference between JDK, JRE, and JVM?**
   - **JDK (Java Development Kit)**: Complete development environment containing compiler (javac), debugger, and tools needed to develop Java applications
   - **JRE (Java Runtime Environment)**: Runtime environment that provides libraries and JVM to run Java applications
   - **JVM (Java Virtual Machine)**: Runtime engine that executes Java bytecode and provides platform independence

2. **What are the main features of Java (OOP principles)?**
   - **Object-Oriented**: Everything is an object with data and methods
   - **Platform Independent**: Write once, run anywhere (WORA)
   - **Simple and Secure**: Easy syntax, no pointers, bytecode verification
   - **Robust**: Strong memory management, exception handling
   - **Multithreaded**: Built-in support for concurrent programming
   - **High Performance**: Just-in-time compilation

3. **What are primitive data types in Java?**
   - **byte**: 8-bit signed integer (-128 to 127)
   - **short**: 16-bit signed integer (-32,768 to 32,767)
   - **int**: 32-bit signed integer (-2^31 to 2^31-1)
   - **long**: 64-bit signed integer (-2^63 to 2^63-1)
   - **float**: 32-bit floating point
   - **double**: 64-bit floating point
   - **boolean**: true or false
   - **char**: 16-bit Unicode character

4. **What is autoboxing and unboxing?**
   - **Autoboxing**: Automatic conversion of primitive types to their wrapper classes (int → Integer)
   - **Unboxing**: Automatic conversion of wrapper classes to primitive types (Integer → int)
   ```java
   Integer num = 10; // Autoboxing
   int primitive = num; // Unboxing
   ```

5. **What are access modifiers in Java (private, protected, public, default)?**
   - **private**: Accessible only within the same class
   - **default**: Accessible within the same package (no modifier)
   - **protected**: Accessible within package and by subclasses
   - **public**: Accessible from anywhere

6. **What is a package in Java?**

   A package is a namespace that organizes related classes and interfaces. It provides access control and prevents naming conflicts.
   ```java
   package com.example.util;
   import java.util.List;
   ```

8. **What is a static keyword? Static variables and methods?**
   - **Static variables**: Belong to the class, not instances. Shared among all objects
   - **Static methods**: Can be called without creating an object. Cannot access non-static members
   ```java
   public class Counter {
       static int count = 0; // Static variable
       static void increment() { count++; } // Static method
   }
   ```

9. **What is a Constructor in Java? Types of constructors?**   
A constructor initializes an object when it's created.
   - **Default Constructor**: No parameters, provided by compiler if none defined
   - **Parameterized Constructor**: Takes parameters to initialize with specific values
   - **Copy Constructor**: Not directly supported, but can be implemented manually

10. **Can we use static methods in a Constructor?**  
Yes, static methods can be called from constructors since they belong to the class and are available during object creation.

#### OOP Concepts

10. **What is inheritance? Types of inheritance in Java?**
Inheritance allows a class to inherit properties and methods from another class.
    - **Single Inheritance**: Class inherits from one parent class
    - **Multilevel Inheritance**: Chain of inheritance (A→B→C)
    - **Hierarchical Inheritance**: Multiple classes inherit from one parent
    - **Multiple Inheritance**: Not supported with classes (only interfaces)

11. **What is polymorphism? Give examples**
Polymorphism allows objects of different types to be treated as objects of a common base type.
    - **Compile-time**: Method overloading
    - **Runtime**: Method overriding
    ```java
    Animal animal = new Dog();
    animal.makeSound(); // Calls Dog's makeSound method
    ```

12. **What is encapsulation and abstraction?**
    - **Encapsulation**: Bundling data and methods together, hiding internal details using access modifiers
    - **Abstraction**: Hiding implementation details and showing only essential features using abstract classes/interfaces

13. **What is method overloading vs method overriding?**
    - **Overloading**: Same method name with different parameters in same class (compile-time)
    - **Overriding**: Subclass provides specific implementation of parent class method (runtime)

14. **When to use Interface vs Abstract Class?**
    - **Interface**: When you need multiple inheritance, contract definition, unrelated classes
    - **Abstract Class**: When you have common code to share, related classes, non-public methods needed

15. **What is a Marker Interface? Why use it?**
An interface with no methods, used to mark classes for special treatment by JVM or frameworks.
Examples: Serializable, Cloneable, Remote

#### String Handling

16. **What is the difference between String, StringBuilder, and StringBuffer?**
    - **String**: Immutable, creates new object on each modification
    - **StringBuilder**: Mutable, not thread-safe, better performance
    - **StringBuffer**: Mutable, thread-safe, synchronized methods

17. **Difference between creating String with literal and new operator**
    ```java
    String s1 = "Hello"; // String literal, goes to string pool
    String s2 = new String("Hello"); // Creates new object in heap
    ```

18. **What is String pool and how does it work?**
String pool is a special memory area in heap where string literals are stored. JVM reuses strings to save memory.

19. **What are the advantages of String pool?**
    - Memory optimization by reusing string objects
    - Faster string comparison using == for literals
    - Reduced garbage collection overhead

20. **Why String is immutable?**
    - Security: String objects used in network connections, file paths
    - Thread Safety: No synchronization needed
    - Caching: hashCode can be cached
    - String Pool: Enables string pooling

#### Basic Collections

21. **What is a Collection in Java?**
Collection is a framework that provides architecture to store and manipulate groups of objects. It includes interfaces (List, Set, Queue) and implementations.

22. **Difference between Array and ArrayList?**
    - **Array**: Fixed size, can store primitives and objects, faster access
    - **ArrayList**: Dynamic size, stores only objects, provides utility methods

23. **What is the difference between ArrayList and LinkedList?**
    - **ArrayList**: Dynamic array, O(1) random access, O(n) insertion/deletion
    - **LinkedList**: Doubly-linked list, O(n) random access, O(1) insertion/deletion at known position

24. **What is a HashMap? Basic operations?**
HashMap stores key-value pairs using hash table. Basic operations: put(), get(), remove(), containsKey()
    ```java
    Map<String, Integer> map = new HashMap<>();
    map.put("key", 100);
    Integer value = map.get("key");
    ```

25. **What is the difference between HashSet and TreeSet?**
    - **HashSet**: Uses hash table, O(1) operations, no ordering
    - **TreeSet**: Uses red-black tree, O(log n) operations, sorted order

26. **What is an Iterator?**
    Iterator provides a way to traverse collection elements sequentially without exposing underlying structure.
    ```java
    Iterator<String> it = list.iterator();
    while(it.hasNext()) {
        System.out.println(it.next());
    }
    ```

27. **What is the difference between List and Set?**
    - **List**: Allows duplicates, maintains insertion order, indexed access
    - **Set**: No duplicates, may or may not maintain order

28. **Array vs List**
    - **Array**: Fixed size, can store primitives, direct memory access
    - **List**: Dynamic size, wrapper objects only, more functionality

29. **Set vs List**
    - **Set**: Unique elements, no duplicates allowed
    - **List**: Allows duplicates, maintains insertion order

#### Exception Handling

30. **What is an Exception? Types of exceptions?**
    Exception is an event that disrupts normal program flow.
    - **Checked Exceptions**: Must be handled or declared (IOException, SQLException)
    - **Unchecked Exceptions**: Runtime exceptions (NullPointerException, IllegalArgumentException)
    - **Errors**: Serious problems, usually not recoverable (OutOfMemoryError)

31. **What is the difference between checked and unchecked exceptions?**
    - **Checked**: Compiler forces handling, occurs at compile time
    - **Unchecked**: Not forced to handle, occurs at runtime

32. **What is try-catch-finally block?**
    ```java
    try {
        // Code that may throw exception
    } catch (SpecificException e) {
        // Handle specific exception
    } finally {
        // Always executes (cleanup code)
    }
    ```

33. **Can we use try without catch?**
    Yes, with finally block: try-finally is valid. Also try-with-resources doesn't need catch.

34. **What is throw vs throws?**
    - **throw**: Used to explicitly throw an exception in code
    - **throws**: Used in method signature to declare exceptions that method might throw

35. **What are the use cases of creating user-defined exceptions?**
    - Business logic specific exceptions
    - Better error categorization
    - Meaningful error messages
    - Application-specific error handling

36. **How to handle user-defined exception?**
    ```java
    public class CustomException extends Exception {
        public CustomException(String message) {
            super(message);
        }
    }
    
    try {
        throw new CustomException("Custom error");
    } catch (CustomException e) {
        System.out.println(e.getMessage());
    }
    ```

37. **What is a NullPointerException & how to prevent it?**
    NPE occurs when trying to access methods/fields on null reference.
    Prevention: Null checks, Optional class, defensive programming

38. **What is a ClassCastException?**
    Thrown when trying to cast an object to a class it's not an instance of.
    ```java
    Object obj = "String";
    Integer num = (Integer) obj; // Throws ClassCastException
    ```

39. **What is Error vs Exception?**
    - **Error**: Serious problems, usually unrecoverable (OutOfMemoryError, StackOverflowError)
    - **Exception**: Problems that can be handled by application code

#### Basic Control Structures

40. **Explain the difference between break and continue statements**
    - **break**: Exits the loop completely
    - **continue**: Skips current iteration and continues with next iteration

41. **What is the difference between == and .equals()?**
    - **==**: Compares references (memory addresses) for objects, values for primitives
    - **equals()**: Compares actual content/values of objects

### Spring Boot Basics

#### Core Concepts

42. **What is Spring Boot?**
    Spring Boot is a framework that simplifies Spring application development by providing auto-configuration, embedded servers, and production-ready features out of the box.

43. **What are the advantages of Spring Boot?**
    - Auto-configuration reduces boilerplate code
    - Embedded servers (Tomcat, Jetty)
    - Production-ready features (health checks, metrics)
    - Starter dependencies simplify dependency management
    - Minimal XML configuration

44. **What is @SpringBootApplication annotation?**
    It's a convenience annotation combining:
    - @Configuration: Marks class as configuration source
    - @EnableAutoConfiguration: Enables auto-configuration
    - @ComponentScan: Enables component scanning

45. **What is the difference between @Component, @Service, and @Repository?**
    - **@Component**: Generic stereotype for any Spring-managed component
    - **@Service**: Specialization of @Component for service layer
    - **@Repository**: Specialization of @Component for data access layer, provides exception translation

46. **What is dependency injection?**
    A design pattern where objects receive their dependencies from external sources rather than creating them internally. Spring IoC container manages this.

47. **What is @Autowired?**
    Annotation that enables automatic dependency injection. Spring automatically injects matching beans by type.

48. **What are Spring Boot starters?**
    Pre-configured dependency descriptors that include commonly used libraries for specific functionality (spring-boot-starter-web, spring-boot-starter-data-jpa).

49. **What is application.properties file?**
    Configuration file where you can externalize configuration properties like database settings, server port, logging levels.

50. **Difference between Spring and Spring Boot?**
    - **Spring**: Comprehensive framework requiring extensive configuration
    - **Spring Boot**: Built on Spring, provides auto-configuration and conventions over configuration

51. **What is IOC container in Spring?**
    Inversion of Control container manages object creation, configuration, and lifecycle. It inverts the control of object creation from application to framework.

#### REST API Basics

52. **What is HTTP? Common HTTP methods?**
    HTTP is a protocol for communication between client and server.
    - **GET**: Retrieve data
    - **POST**: Create new resource
    - **PUT**: Update entire resource
    - **PATCH**: Partial update
    - **DELETE**: Remove resource

53. **What are HTTP status codes (200, 404, 500)?**
    - **200 OK**: Request successful
    - **404 Not Found**: Resource not found
    - **500 Internal Server Error**: Server encountered an error

54. **What is REST API?**
    Representational State Transfer - architectural style for designing web services using HTTP methods and stateless communication.

55. **What is JSON?**
    JavaScript Object Notation - lightweight data interchange format that's easy to read and write.

56. **What is @RestController vs @Controller?**
    - **@Controller**: Returns view names for MVC applications
    - **@RestController**: Combines @Controller + @ResponseBody, returns data directly

57. **What is the process of creating a REST API (with example)?**
    ```java
    @RestController
    @RequestMapping("/api/users")
    public class UserController {
        
        @GetMapping
        public List<User> getAllUsers() {
            return userService.findAll();
        }
        
        @PostMapping
        public User createUser(@RequestBody User user) {
            return userService.save(user);
        }
    }
    ```

---

## LEVEL 2: INTERMEDIATE (2-4 Years Experience)

### Advanced Core Java

#### Collections Deep Dive

58. **Contract between hashCode() and equals() methods?**
    - If two objects are equal (equals() returns true), they must have the same hash code
    - If two objects have the same hash code, they don't need to be equal
    - If you override equals(), you must override hashCode()

59. **Explain the internal working of HashMap in Java**
    HashMap uses array of buckets. Each bucket contains linked list (or tree in Java 8+). Hash function determines bucket index. Collisions are handled by chaining.

60. **What happens on a HashMap collision?**
    When two keys hash to the same bucket, they form a linked list. In Java 8+, if list size exceeds 8, it converts to a balanced tree (red-black tree) for better performance.

61. **What is the load factor in HashMap?**
    Load factor (default 0.75) determines when to resize the HashMap. When size > capacity × load factor, HashMap doubles its capacity and rehashes all elements.

62. **Difference between HashMap, LinkedHashMap, and TreeMap?**
    - **HashMap**: No ordering, O(1) operations
    - **LinkedHashMap**: Maintains insertion order, O(1) operations
    - **TreeMap**: Sorted order, O(log n) operations, implements NavigableMap

63. **Difference between HashMap, LinkedHashMap, and ConcurrentHashMap**
    - **HashMap**: Not thread-safe
    - **LinkedHashMap**: Not thread-safe, maintains order
    - **ConcurrentHashMap**: Thread-safe, segment-based locking

64. **How can you convert a HashMap into an ArrayList?**
    ```java
    HashMap<String, Integer> map = new HashMap<>();
    ArrayList<Integer> values = new ArrayList<>(map.values());
    ArrayList<String> keys = new ArrayList<>(map.keySet());
    ```

65. **What are the differences between Comparable and Comparator?**
    - **Comparable**: Natural ordering, implemented by the class itself, compareTo() method
    - **Comparator**: Custom ordering, separate class, compare() method

66. **What is a ConcurrentHashMap? How does it work?**
    Thread-safe HashMap implementation using segment-based locking (Java 7) or CAS operations and synchronized buckets (Java 8+).

67. **What's the difference between Hashtable and ConcurrentHashMap?**
    - **Hashtable**: Synchronizes entire table, poor performance
    - **ConcurrentHashMap**: Segment-based locking, better concurrency

68. **What is the difference between Vector and ArrayList?**
    - **Vector**: Synchronized, thread-safe, legacy class
    - **ArrayList**: Not synchronized, better performance, preferred choice

69. **HashMap vs HashTable**
    - **HashMap**: Not synchronized, allows null values/keys, introduced in Java 1.2
    - **HashTable**: Synchronized, doesn't allow null, legacy class from Java 1.0

70. **ArrayList vs LinkedList**
    - **ArrayList**: Better for random access, implements RandomAccess
    - **LinkedList**: Better for frequent insertions/deletions, implements Deque

#### Java 8 Features

71. **What is a Functional Interface?**
    Interface with exactly one abstract method. Can have default and static methods. Examples: Runnable, Callable, Comparator.

72. **Explain Java 8 features (Lambdas, Streams, Optional)**
    - **Lambda Expressions**: Anonymous functions for cleaner code
    - **Stream API**: Functional programming for collections
    - **Optional**: Container to avoid null pointer exceptions
    - **Method References**: Shorthand for lambda expressions
    - **Default Methods**: Methods in interfaces with implementation

73. **Difference between map() vs flatMap() in Java 8?**
    - **map()**: One-to-one transformation (Stream<T> → Stream<R>)
    - **flatMap()**: One-to-many transformation, flattens nested streams

74. **What is Stream API and its advantages?**
    Stream API enables functional programming on collections. Advantages: readable code, lazy evaluation, parallel processing, immutability.

75. **What is Stream pipeline?**
    Chain of operations: Source → Intermediate operations → Terminal operation
    ```java
    list.stream().filter(x -> x > 5).map(x -> x * 2).collect(toList());
    ```

76. **Difference between intermediate and terminal operators in Stream API**
    - **Intermediate**: Return stream, lazy evaluation (filter, map, sorted)
    - **Terminal**: Return non-stream result, trigger execution (collect, forEach, reduce)

77. **Using Stream API, find the 2nd highest salary from employee objects list**
    ```java
    Optional<Employee> secondHighest = employees.stream()
        .sorted(Comparator.comparing(Employee::getSalary).reversed())
        .skip(1)
        .findFirst();
    ```

78. **Use of Stream API in projects**
    - Data transformation and filtering
    - Report generation
    - Business rule validation
    - Bulk operations on collections
    - Parallel processing for performance

79. **Lambda expressions vs Anonymous classes**
    - **Lambda**: More concise, compile to invokedynamic, functional interfaces only
    - **Anonymous classes**: More flexible, can implement multiple methods, creates class files

#### Advanced OOP

80. **What is a Functional Interface?**
    (Duplicate of #71) Interface with single abstract method, can be used with lambda expressions.

81. **What are Sealed Classes (Java 17)?**
    Classes that restrict which classes can extend them using 'permits' clause. Provides controlled inheritance.
    ```java
    public sealed class Shape permits Circle, Rectangle, Triangle {
    }
    ```

82. **What is Fail-Fast Iteration & how to handle it?**
    Iterator fails immediately upon detecting concurrent modification. Handle using ConcurrentHashMap or synchronized collections.

83. **What is ConcurrentModificationException? Fail safe and fail fast iterators?**
    - **Fail-fast**: Throws exception on concurrent modification (ArrayList iterator)
    - **Fail-safe**: Works on copy, allows concurrent modification (ConcurrentHashMap iterator)

84. **Final, finally and finalize()?**
    - **final**: Keyword for constants, prevents inheritance/overriding
    - **finally**: Block that always executes in try-catch
    - **finalize()**: Method called before garbage collection (deprecated)

85. **Autoboxing vs Unboxing**
    (Duplicate of #4) Automatic conversion between primitives and wrapper objects.

86. **What is Cloneable? Deep clones vs shallow clones**
    - **Cloneable**: Marker interface enabling object.clone()
    - **Shallow clone**: Copies object but not referenced objects
    - **Deep clone**: Copies object and all referenced objects

87. **Shallow Copy vs Deep Copy**
    - **Shallow**: Copies references to original objects
    - **Deep**: Creates new instances of all referenced objects

#### Memory Management

88. **Explain Java memory management**
    Java memory divided into: Heap (objects), Stack (method calls, local variables), Method Area (class metadata), PC Register, Native Method Stack.

#### **Overview**

Java memory management is **automatic**, thanks to the **JVM (Java Virtual Machine)**. Developers don’t manually allocate or free memory (unlike C/C++).

Memory in Java is broadly divided into:

1. **Heap** – stores **objects** and **instance variables**.
2. **Stack** – stores **primitive variables**, **references to objects**, and **method call frames**.
3. **Metaspace / PermGen** – stores **class metadata** (class definitions, method info).


#### **Heap Memory**

* The **heap** is where **all objects live**.
* Divided into **generations** for efficient garbage collection:

| Generation               | Purpose                                        |
| ------------------------ | ---------------------------------------------- |
| Young Generation         | Short-lived objects (temporary objects)        |
| - Eden space             | New objects are allocated here                 |
| - Survivor spaces        | Objects survive minor GC cycles                |
| Old / Tenured Generation | Long-lived objects (cached, static data, etc.) |
| Permanent / Metaspace    | Class metadata, loaded classes                 |

* **Garbage Collector (GC)** cleans the heap by removing objects **no longer referenced**.



#### **Stack Memory**

* Stores **method call frames**:

  * Local variables (primitives and object references)
  * Method parameters
  * Return addresses

* **LIFO structure:** last method called → first to return.

* Stack memory is automatically freed when a method completes.

**Example:**

```java
void foo() {
    int x = 10;          // stored on stack
    String s = "Hello";  // reference stored on stack, object on heap
}
```

* `x` is primitive → fully on stack.
* `s` is reference → stack holds pointer, heap holds the `"Hello"` object.

#### **Program Counter (PC) Register**

Each thread has its own PC register.

Stores the address of the currently executing JVM instruction.

Helps JVM know which instruction to execute next in a thread.

#### **Native Method Stack**

Stores information for native methods (methods written in languages like C/C++ and called via JNI).

Each thread has its own native stack.

Similar to JVM stack but used for native code execution.

#### **Garbage Collection (GC)**

* **GC automatically frees unused objects** in the heap.
* **Reachability-based:** an object is eligible for GC if **no live references point to it**.

**Common GC Algorithms:**

1. **Serial GC** – single-threaded, simple, for small apps.
2. **Parallel GC** – uses multiple threads, reduces pause time.
3. **CMS (Concurrent Mark Sweep)** – minimizes GC pauses, concurrent with app threads.
4. **G1 (Garbage First)** – divides heap into regions, balances pause time and throughput.

**GC Phases:**

1. **Mark** – find live objects.
2. **Sweep** – delete unreachable objects.
3. **Compact** – reduce fragmentation (optional, some collectors do it).


#### **Memory Leaks in Java**

Even though Java has GC, **memory leaks can still happen** if references are unintentionally held. Examples:

* Static collections holding objects forever.
* Event listeners not deregistered.
* Caches without eviction policies.



#### **Best Practices**

1. Prefer **local variables** and scope-limited references.
2. Use **try-with-resources** to close streams and connections.
3. Avoid **long-lived object references** if not necessary.
4. Choose **appropriate GC and JVM tuning** for high-performance apps.
5. Use **profiling tools** (VisualVM, JConsole, JProfiler) to monitor memory usage.


#### **Summary Diagram (Mental Model)**

```
Stack (method calls, primitives, references)
 └─> Reference to object on Heap
Heap (objects)
 ├─> Young Generation (Eden + Survivor)
 ├─> Old Generation (Tenured)
 └─> Metaspace (class metadata)
Garbage Collector cleans unreachable objects
```

💡 **Key Insight:**

* **Stack = short-lived, method-scoped data**
* **Heap = objects with variable lifespan**
* **GC = automatically frees memory, but you must avoid lingering references**



90. **What is garbage collection in Java? Types of GC?**
    Automatic memory management that reclaims unused objects.
    Types: Serial GC, Parallel GC, G1GC, ZGC, Shenandoah.

91. **What is the finalize() method?**
    Method called by garbage collector before object destruction. Deprecated in Java 9+ due to unpredictability.

92. **Stack vs Heap Memory Allocation**
    - **Stack**: Method calls, local variables, faster access, automatic cleanup
    - **Heap**: Objects, instance variables, slower access, garbage collected

93. **How to handle OutOfMemoryException?**
    - Increase heap size (-Xmx)
    - Fix memory leaks
    - Optimize data structures
    - Use profiling tools
    - Implement proper caching strategies

#### Multithreading Basics

93. **What is multithreading in Java? Thread lifecycle?**
    Multithreading allows concurrent execution. Lifecycle: NEW → RUNNABLE → BLOCKED/WAITING/TIMED_WAITING → TERMINATED

94. **What is synchronization in Java? synchronized keyword?**
    Synchronization prevents race conditions by allowing only one thread to access synchronized block/method at a time.

95. **What is the difference between wait() and sleep()?**
    - **wait()**: Releases lock, waits for notify(), Object class method
    - **sleep()**: Doesn't release lock, waits for time, Thread class method

96. **What is the volatile keyword?**
    Ensures variable visibility across threads. Prevents caching in CPU registers, guarantees happens-before relationship.

97. **What is ThreadLocal?**
    Provides thread-confined variables. Each thread has its own copy of the variable.
    ```java
    ThreadLocal<String> threadLocal = new ThreadLocal<>();
    threadLocal.set("thread-specific-value");
    ```

98. **What is a deadlock in Java? How can it be avoided?**
    Deadlock occurs when two or more threads wait for each other indefinitely.
    Prevention: Lock ordering, timeout, avoid nested locks, use concurrent utilities.

99. **Thread vs Runnable**
    - **Thread**: Class inheritance, limited (single inheritance)
    - **Runnable**: Interface implementation, more flexible, better design

100. **What is the difference between Runnable and Callable?**
     - **Runnable**: No return value, cannot throw checked exceptions
     - **Callable**: Returns value, can throw exceptions, used with ExecutorService

101. **Synchronized methods vs Synchronized blocks**
     - **Method**: Synchronizes entire method, less flexible
     - **Block**: Synchronizes specific code section, more control, better performance

### Spring Boot Intermediate

#### Advanced Configuration

102. **How does Spring Boot auto-configuration work?**
     Uses @EnableAutoConfiguration to scan classpath and automatically configure beans based on available dependencies and properties.

103. **What is the role of @Configuration and @Bean?**
     - **@Configuration**: Marks class as source of bean definitions
     - **@Bean**: Defines a bean to be managed by Spring container
     ```java
     @Configuration
     public class AppConfig {
         @Bean
         public DataSource dataSource() {
             return new HikariDataSource();
         }
     }
     ```

104. **How do profiles work in Spring Boot (@Profile use case)?**
     Profiles allow environment-specific configurations. Use @Profile annotation or application-{profile}.properties files.
     ```java
     @Service
     @Profile("dev")
     public class DevEmailService implements EmailService {
     }
     ```

105. **What is @Transactional, and what's the benefit?**
     Manages database transactions declaratively. Benefits: ACID properties, rollback on exceptions, transaction propagation control.

106. **How do you write a global exception handler in Spring Boot?**
     ```java
     @ControllerAdvice
     public class GlobalExceptionHandler {
         @ExceptionHandler(Exception.class)
         public ResponseEntity<String> handleException(Exception e) {
             return ResponseEntity.status(500).body(e.getMessage());
         }
     }
     ```

107. **Difference between application.properties and application.yml?**
     - **Properties**: Key-value pairs, simpler syntax
     - **YAML**: Hierarchical structure, more readable for complex configurations

108. **What is the use of CommandLineRunner and ApplicationRunner?**
     Both run code after Spring Boot application starts.
     - **CommandLineRunner**: Receives raw string arguments
     - **ApplicationRunner**: Receives ApplicationArguments object

109. **How does the embedded server (Tomcat) work in Spring Boot?**
     Spring Boot includes embedded Tomcat as dependency. Auto-configuration creates and configures TomcatServletWebServerFactory.

110. **How do you override default auto-configurations?**
     - Define custom beans with same name
     - Use @ConditionalOnMissingBean
     - Exclude specific auto-configurations
     - Use properties to customize behavior

111. **How do you handle circular dependencies in Spring Boot?**
     - Use @Lazy annotation
     - Constructor injection → setter injection
     - @PostConstruct for initialization
     - Redesign to eliminate circular dependency

#### Dependency Injection

112. **What is constructor injection vs field injection vs setter injection?**
     - **Constructor**: Immutable, required dependencies, testable
     - **Field**: Simple but hard to test, reflection-based
     - **Setter**: Optional dependencies, mutable

113. **What is @Qualifier and @Primary annotation?**
     - **@Qualifier**: Specifies which bean to inject when multiple candidates exist
     - **@Primary**: Marks preferred bean when multiple candidates exist

114. **If both @Qualifier and @Primary are used, which one will take precedence?**
     @Qualifier takes precedence over @Primary because it's more specific.

115. **How to avoid bean creation failures in dependency injection?**
     - Use @ConditionalOnBean/@ConditionalOnMissingBean
     - Proper dependency ordering
     - Use @DependsOn annotation
     - Handle circular dependencies

116. **@Autowired vs @Qualifier**
     - **@Autowired**: Enables dependency injection
     - **@Qualifier**: Specifies which bean to inject

117. **@Primary vs @Qualifier**
     - **@Primary**: Default choice among multiple beans
     - **@Qualifier**: Explicit choice for specific injection point

#### REST API Advanced

118. **@RequestMapping vs @GetMapping**
     - **@RequestMapping**: Generic mapping, supports all HTTP methods
     - **@GetMapping**: Shorthand for @RequestMapping(method = GET)

119. **@PathVariable vs @RequestParam**
     - **@PathVariable**: Extracts values from URI path
     - **@RequestParam**: Extracts values from query parameters

120. **@PostMapping vs @PutMapping**
     - **@PostMapping**: Create new resource, non-idempotent
     - **@PutMapping**: Update entire resource, idempotent

121. **PUT vs PATCH**
     - **PUT**: Replace entire resource
     - **PATCH**: Partial update of resource

122. **@ExceptionHandler vs @ControllerAdvice**
     - **@ExceptionHandler**: Handles exceptions in single controller
     - **@ControllerAdvice**: Global exception handling across controllers

#### Spring Boot Annotations

123. **@ComponentScan vs @EnableAutoConfiguration**
     - **@ComponentScan**: Scans for user-defined components
     - **@EnableAutoConfiguration**: Enables Spring Boot's auto-configuration

124. **@Configuration vs @Bean**
     - **@Configuration**: Marks configuration class
     - **@Bean**: Defines individual bean method

125. **@Async vs @Scheduled**
     - **@Async**: Executes method asynchronously
     - **@Scheduled**: Executes method on schedule

126. **@Cacheable vs @CacheEvict**
     - **@Cacheable**: Caches method result
     - **@CacheEvict**: Removes entries from cache

#### Database & JPA Basics

127. **What is ORM?**
     Object-Relational Mapping maps database tables to Java objects, eliminating need for SQL in many cases.

128. **What is JPA? Difference between JPA and Hibernate?**
     - **JPA**: Java Persistence API, specification for ORM
     - **Hibernate**: JPA implementation, provides additional features

129. **What is an Entity in JPA?**
     Java class that represents database table, annotated with @Entity.

130. **What are JPA annotations (@Entity, @Id, @GeneratedValue)?**
     - **@Entity**: Marks class as JPA entity
     - **@Id**: Marks primary key field
     - **@GeneratedValue**: Specifies primary key generation strategy

131. **What is the difference between persist() and merge()?**
     - **persist()**: Makes transient object persistent
     - **merge()**: Updates detached object or creates if not exists

132. **What are JPA relationships (@OneToMany, @ManyToOne, etc.)?**
     - **@OneToOne**: One entity relates to one other entity
     - **@OneToMany**: One entity relates to many other entities
     - **@ManyToOne**: Many entities relate to one entity
     - **@ManyToMany**: Many entities relate to many other entities

133. **What is JPQL?**
     Java Persistence Query Language - object-oriented query language for JPA entities.

134. **What is lazy loading vs eager loading?**
     - **Lazy**: Load data when accessed, better performance
     - **Eager**: Load data immediately, may cause N+1 problem

135. **What is the difference between save() and saveAndFlush()?**
     - **save()**: Persists entity, may not hit database immediately
     - **saveAndFlush()**: Persists and immediately flushes to database

136. **In Hibernate, what is the difference between get() and load() methods?**
     - **get()**: Returns null if not found, hits database immediately
     - **load()**: Throws exception if not found, returns proxy (lazy loading)

#### Testing Basics

137. **What is JUnit? Basic annotations?**
     JUnit is testing framework for Java. Annotations: @Test, @BeforeEach, @AfterEach, @BeforeAll, @AfterAll.

138. **What is @Mockito? When to use @Mock?**
     Mockito is mocking framework. Use @Mock to create mock objects for testing in isolation.

139. **What is the difference between @Mock, @MockBean, and @Spy?**
     - **@Mock**: Mockito mock object
     - **@MockBean**: Spring Boot mock bean in application context
     - **@Spy**: Partial mock, calls real methods unless stubbed

140. **How do you test REST controllers using MockMvc?**
     ```java
     @Test
     public void testGetUser() throws Exception {
         mockMvc.perform(get("/api/users/1"))
                .andExpect(status().isOk())
                .andExpect(jsonPath("$.name").value("John"));
     }
     ```

141. **What is @SpringBootTest vs @WebMvcTest?**
     - **@SpringBootTest**: Loads full application context, integration testing
     - **@WebMvcTest**: Loads only web layer, unit testing controllers

#### Security Basics

142. **What is Authentication vs Authorization?**
     - **Authentication**: Verifying user identity (who you are)
     - **Authorization**: Checking user permissions (what you can do)

143. **What is Spring Security?**
     Framework providing authentication and authorization for Java applications. Handles security concerns declaratively.

144. **How do you secure REST APIs using Spring Security?**
     Configure SecurityFilterChain, add authentication mechanisms (JWT, OAuth), define authorization rules.
     ```java
     @Configuration
     @EnableWebSecurity
     public class SecurityConfig {
         @Bean
         public SecurityFilterChain filterChain(HttpSecurity http) throws Exception {
             return http.authorizeRequests()
                       .requestMatchers("/api/public/**").permitAll()
                       .anyRequest().authenticated()
                       .and().build();
         }
     }
     ```

145. **What is BasicAuth vs JWT?**
     - **BasicAuth**: Username/password sent with each request, stateful
     - **JWT**: Token-based, stateless, contains user information and claims

146. **What are HTTP status codes: 401, 403, 404, 500, 502, 503?**
     - **401 Unauthorized**: Authentication required
     - **403 Forbidden**: Access denied despite authentication
     - **404 Not Found**: Resource doesn't exist
     - **500 Internal Server Error**: Server-side error
     - **502 Bad Gateway**: Invalid response from upstream server
     - **503 Service Unavailable**: Server temporarily unavailable

---

## LEVEL 3: ADVANCED (4+ Years Experience)

### JVM Internals & Performance

147. **How does the JVM work internally? (Class loader, memory areas, GC)**
     JVM loads classes via ClassLoader, manages memory in Heap/Stack/Method Area, executes bytecode via execution engine, and reclaims memory via Garbage Collector.

148. **What are the different types of class loaders in Java?**
     - **Bootstrap ClassLoader**: Loads core Java classes
     - **Extension ClassLoader**: Loads extension classes
     - **Application ClassLoader**: Loads application classes
     - **Custom ClassLoaders**: User-defined for specific requirements

149. **What are strong, weak, soft, and phantom references in Java?**
     - **Strong**: Normal references, never GC'd while reachable
     - **Weak**: GC'd when only weakly reachable
     - **Soft**: GC'd when memory is low
     - **Phantom**: Used for cleanup actions, object already GC'd

150. **How does Java handle memory leaks despite having garbage collector?**
     Memory leaks occur when objects remain reachable but unused (static collections, listeners not removed, ThreadLocal not cleared, connections not closed).

151. **What are different GC algorithms? When to use which?**
     - **Serial GC**: Single-threaded, small applications
     - **Parallel GC**: Multi-threaded, throughput-focused
     - **G1GC**: Low latency, large heaps
     - **ZGC/Shenandoah**: Ultra-low latency, very large heaps

152. **How do you tune JVM performance?**
     - Adjust heap size (-Xms, -Xmx)
     - Choose appropriate GC algorithm
     - Monitor GC logs
     - Tune GC parameters
     - Profile application to identify bottlenecks

153. **What is JIT compilation?**
     Just-In-Time compilation converts frequently executed bytecode to native machine code for better performance.

154. **What are JVM memory areas (Heap, Stack, Method Area, PC Register)?**
     - **Heap**: Object storage, divided into Young and Old generation
     - **Stack**: Method call frames, local variables
     - **Method Area**: Class metadata, constant pool
     - **PC Register**: Current executing instruction pointer

155. **What is metaspace in Java 8+?**
     Replaced PermGen in Java 8. Stores class metadata in native memory, automatically sized, reduces OutOfMemoryError.
In **Java 8**, **Metaspace** is a memory space in the JVM that **replaced the PermGen (Permanent Generation)** used in earlier versions (Java 7 and below) for storing **class metadata**. Here’s a detailed breakdown:

#### 1. **Purpose of Metaspace**

Metaspace stores **metadata about classes** loaded by the JVM, such as:

* Class names
* Method and field information
* Runtime constant pool
* Annotations and bytecode-related metadata

> Note: Unlike object instances, this is about the **structure of classes themselves**, not the objects created from them.

#### 2. **Memory Management**

* Metaspace **uses native memory**, not part of the Java heap.
* JVM dynamically grows Metaspace as more classes are loaded.
* You can **limit its size** using JVM flags:

  ```bash
  -XX:MetaspaceSize=128m       # Initial Metaspace size
  -XX:MaxMetaspaceSize=512m    # Maximum Metaspace size
  ```
* If you don’t set `MaxMetaspaceSize`, it can grow until the system runs out of memory.

#### 3. **Benefits of Metaspace**

* Reduces `OutOfMemoryError` due to class metadata.
* Removes the artificial fixed size limit of PermGen.
* Easier class unloading when applications dynamically load/unload classes (e.g., in web servers or frameworks like Spring).


### 4. **Common Metaspace Issues**

* **Classloader leaks**: Classes are not unloaded because references are retained.
* **Excessive class loading**: Libraries generating lots of dynamic classes (e.g., proxies in Hibernate or Spring AOP) can exhaust Metaspace.


**Summary:**
Metaspace in Java 8 is an **off-heap memory area** for class metadata that **replaces PermGen**, automatically grows by default, and reduces memory errors related to class loading.



156. **How do you analyze heap dumps and thread dumps?**
     - **Heap Dumps**: Use Eclipse MAT, VisualVM to find memory leaks
     - **Thread Dumps**: Analyze thread states, find deadlocks, identify blocking

### Advanced Concurrency

157. **What is the Executor framework in Java?**
     High-level API for managing threads. Provides ThreadPoolExecutor, ScheduledExecutorService, and various factory methods.
     
| Interface                  | Description                                                                                   |
| -------------------------- | --------------------------------------------------------------------------------------------- |
| `Executor`                 | The simplest interface. Has a single method `execute(Runnable command)` to run tasks.         |
| `ExecutorService`          | Extends `Executor`. Provides more control (submit tasks, shutdown, get results via `Future`). |
| `ScheduledExecutorService` | Extends `ExecutorService`. Supports scheduling tasks to run after a delay or periodically.    |


| Implementation         | Description                                                        |
| ---------------------- | ------------------------------------------------------------------ |
| `FixedThreadPool`      | A pool with a fixed number of threads.                             |
| `CachedThreadPool`     | A pool that creates new threads as needed but reuses idle threads. |
| `SingleThreadExecutor` | Ensures only one thread executes tasks sequentially.               |
| `ScheduledThreadPool`  | Supports scheduling tasks to run after a delay or periodically.    |


159. **What is a Future in Java?**
Represents result of asynchronous computation. Provides methods to check completion, wait for completion, retrieve result.


| Method                                  | Description                                                                           |
| --------------------------------------- | ------------------------------------------------------------------------------------- |
| `get()`                                 | Waits if necessary for the computation to complete and returns the result.            |
| `get(long timeout, TimeUnit unit)`      | Waits up to the specified time for the computation to complete.                       |
| `cancel(boolean mayInterruptIfRunning)` | Attempts to cancel the task. Returns `true` if successful.                            |
| `isDone()`                              | Returns `true` if the task is completed (successfully, cancelled, or with exception). |
| `isCancelled()`                         | Returns `true` if the task was cancelled before completion.                           |

Future works with Callable<V> (which returns a value) and Runnable (wrapped as RunnableFuture).

Calling get() blocks until the result is ready, but you can check isDone() first.

You can cancel a task if it hasn’t finished yet.

**Java 8 introduced CompletableFuture, which is more flexible and allows non-blocking callbacks and chaining.**

160. **What is a ThreadPool and why should you use it?**
     Manages collection of worker threads. Benefits: reduces thread creation overhead, controls resource usage, improves performance.

161. **What are the real differences between ReentrantLock and synchronized?**
     - **ReentrantLock**: Explicit locking, interruptible, try-lock, fair/unfair
     - **synchronized**: Implicit locking, built-in language support, simpler syntax
synchronized: Lock is automatically acquired when entering a block/method and released when leaving (even on exceptions).

ReentrantLock: Lock must be manually acquired and released

162. **How does volatile differ from synchronized?**
     - **volatile**: Ensures visibility, no atomicity, no blocking
     - **synchronized**: Ensures visibility and atomicity, can block threads

163. **What's the difference between thread safety and atomicity?**
     - **Thread Safety**: Safe access from multiple threads
     - **Atomicity**: Operation completes entirely or not at all

164. **When would you use CountDownLatch vs CyclicBarrier?**
     - **CountDownLatch**: One-time use, threads wait for event
     - **CyclicBarrier**: Reusable, threads wait for each other

165. **What is the difference between busy-waiting vs blocking vs non-blocking calls?**
     - **Busy-waiting**: Continuously checks condition, wastes CPU
     - **Blocking**: Thread sleeps until condition met
     - **Non-blocking**: Returns immediately, may indicate not ready

166. **How does CompletableFuture work internally?**
     Uses ForkJoinPool for async execution, maintains completion state, supports chaining and combining operations.

167. **How do you avoid thread starvation?**
     - Use fair locks
     - Avoid holding locks too long
     - Use appropriate thread priorities
     - Monitor thread pool health (Monitor thread usage and task queue size. Ensure there are enough threads for all critical tasks.)

168. **How would you write a thread-safe singleton?**
     ```java
     public class Singleton {
         private static volatile Singleton instance;
         
         public static Singleton getInstance() {
             if (instance == null) {
                 synchronized (Singleton.class) {
                     if (instance == null) {
                         instance = new Singleton();
                     }
                 }
             }
             return instance;
         }
     }
     ```

169. **What is the Producer-Consumer pattern? Implement with BlockingQueue?**
The Producer-Consumer pattern is a classic concurrency design pattern where:

Producers generate data and put it into a shared resource (buffer).

Consumers take data from the buffer and process it.

The goal is to decouple production from consumption, allowing both to work at their own pace while safely sharing data.

In Java, this pattern can be easily implemented using BlockingQueue, which handles all the thread-safety and blocking mechanics.
```java
     BlockingQueue<Integer> queue = new LinkedBlockingQueue<>();
     
     // Producer
     queue.put(item);
     
     // Consumer
     Integer item = queue.take();
```

170. **What is ForkJoinPool and how it differs from regular thread pools?**
     Designed for divide-and-conquer algorithms. Uses work-stealing algorithm where idle threads steal work from busy threads.
      Key Classes
      
      ForkJoinPool – the pool itself.
      
      RecursiveTask<V> – a task that returns a result.
      
      RecursiveAction – a task that does not return a result.

| Feature         | Regular Thread Pool (`ExecutorService`) | ForkJoinPool                                                    |
| --------------- | --------------------------------------- | --------------------------------------------------------------- |
| Task Type       | Independent tasks                       | Recursive, divisible tasks                                      |
| Work-Stealing   | ❌ Usually not                           | ✅ Idle threads steal work from busy threads                     |
| Thread Usage    | Fixed number of threads or bounded pool | Typically one thread per CPU core (common parallelism = #cores) |
| Suitable For    | I/O-bound or independent tasks          | CPU-bound, divide-and-conquer tasks                             |
| Task Submission | `submit()` / `execute()`                | `fork()` / `join()` / `invoke()`                                |
| Result Handling | `Future`                                | `join()` (blocking) or `invoke()`                               |


172. **How do Java Stream operations work internally (parallel vs sequential)?**
     - **Sequential**: Single thread, processes elements in order
     - **Parallel**: Uses ForkJoinPool, splits work across multiple threads

173. **What is a live-lock and how is it different from deadlock?**
     - **Deadlock**: Threads permanently blocked waiting for each other
     - **Livelock**: Threads continuously change state in response to others, no progress. Threads are not blocked, but they cannot make progress because they keep responding to each other.

174. **What is the Java Memory Model (JMM)?**
     Defines how threads interact through memory, specifies happens-before relationships, visibility guarantees.

175. **How does a Semaphore work? Real-life examples?**
     Controls access to resource pool. Examples: connection pool, rate limiting, resource allocation.

176. **What is a BlockingQueue? Types and use cases?**
     Thread-safe queue that blocks on empty (take) or full (put).
     Types: ArrayBlockingQueue, LinkedBlockingQueue, PriorityBlockingQueue, SynchronousQueue.

### Advanced Spring Boot

175. **How does Spring manage bean lifecycle? What are the hooks?**

#### Spring Bean Lifecycle

Spring manages beans in the **ApplicationContext (IoC container)**, and their lifecycle goes through several phases:

1. **Instantiation** → Spring creates the bean instance (using `new` or factory methods).
2. **Populate Properties** → Dependency Injection (DI) happens (e.g., `@Autowired` fields, setters).
3. **BeanNameAware & BeanFactoryAware** → If the bean implements these, Spring injects metadata (bean name, BeanFactory, etc.).
4. **BeanPostProcessors (before init)** → `postProcessBeforeInitialization()` is called for all registered `BeanPostProcessor`s.
5. **Initialization**

   * If bean implements `InitializingBean` → `afterPropertiesSet()` runs.
   * If `initMethod` is defined in `@Bean` or XML → that method runs.
6. **BeanPostProcessors (after init)** → `postProcessAfterInitialization()` is called.
7. **Bean is Ready to Use** 🚀
8. **Destruction** (when context closes or bean is removed)

   * If bean implements `DisposableBean` → `destroy()` runs.
   * If `destroyMethod` is defined in `@Bean` or XML → that method runs.


#### Bean Lifecycle Hooks (Ways to Intervene)

Spring gives you multiple hooks to interact with bean lifecycle:

### **1. Annotations**

* `@PostConstruct` → method called after bean initialization.
* `@PreDestroy` → method called before bean destruction.

```java
@Component
public class MyBean {
    @PostConstruct
    public void init() {
        System.out.println("Bean is initialized!");
    }

    @PreDestroy
    public void cleanup() {
        System.out.println("Bean is about to be destroyed!");
    }
}
```


### **2. Interfaces**

* `InitializingBean.afterPropertiesSet()` → init logic.
* `DisposableBean.destroy()` → cleanup logic.

```java
@Component
public class MyBean implements InitializingBean, DisposableBean {
    @Override
    public void afterPropertiesSet() {
        System.out.println("Init via InitializingBean");
    }

    @Override
    public void destroy() {
        System.out.println("Cleanup via DisposableBean");
    }
}
```



### **3. @Bean Config Methods**

In Java config:

```java
@Configuration
public class AppConfig {
    @Bean(initMethod = "customInit", destroyMethod = "customDestroy")
    public MyBean myBean() {
        return new MyBean();
    }
}
```



### **4. BeanPostProcessor**

* Customizes beans **before and after initialization**.
* Useful for cross-cutting logic (logging, proxies, AOP).

```java
@Component
public class MyBeanPostProcessor implements BeanPostProcessor {
    @Override
    public Object postProcessBeforeInitialization(Object bean, String beanName) {
        System.out.println("Before init: " + beanName);
        return bean;
    }

    @Override
    public Object postProcessAfterInitialization(Object bean, String beanName) {
        System.out.println("After init: " + beanName);
        return bean;
    }
}
```


#### Summary

* **Lifecycle stages**: instantiation → DI → initialization → usage → destruction.
* **Hooks**:

  * `@PostConstruct`, `@PreDestroy`
  * `InitializingBean`, `DisposableBean`
  * `@Bean(initMethod, destroyMethod)`
  * `BeanPostProcessor` (before/after init).


176. **What is a proxy in Spring? JDK vs CGLIB proxies?**

#### What is a Proxy in Spring?

A **proxy** is a wrapper object created by Spring **around a bean** to intercept method calls.

* Instead of calling the actual bean directly, Spring returns a **proxy object**.
* The proxy can **add behavior before/after the actual method execution** (e.g., transactions, security checks, logging).
* This is how Spring implements **cross-cutting concerns** without modifying business logic.

 Example: If you put `@Transactional` on a method, Spring creates a **transactional proxy** around that bean. The proxy opens/closes the transaction before/after calling your method.


#### Two Types of Proxies in Spring

### 1. **JDK Dynamic Proxies**

* Uses the Java Reflection API (`java.lang.reflect.Proxy`).
* Works only if the bean implements at least **one interface**.
* Proxy **implements the same interfaces** as the bean.
* When you call a method via the proxy, it delegates to the target bean.

**Example:**

```java
public interface PaymentService {
    void pay();
}

@Service
public class PaymentServiceImpl implements PaymentService {
    public void pay() {
        System.out.println("Payment processed");
    }
}
```

If proxied, Spring will create a **JDK proxy** that implements `PaymentService`.


### 2. **CGLIB Proxies**

* Uses **CGLIB (Code Generation Library)** to generate a subclass of the target class at runtime.
* Works even if the bean has **no interfaces**.
* Proxy = **subclass** of the target bean, with method interception.
* Limitations:

  * Can’t proxy `final` classes.
  * Can’t override `final` methods.

**Example:**

```java
@Service
public class NotificationService {
    public void send() {
        System.out.println("Notification sent");
    }
}
```

 ince there’s no interface, Spring will use **CGLIB** to create a subclass proxy.


#### Key Differences

| Feature            | JDK Proxy                           | CGLIB Proxy                                              |
| ------------------ | ----------------------------------- | -------------------------------------------------------- |
| **Requirement**    | Target must implement interface     | Works on classes (no interface needed)                   |
| **Implementation** | Uses `java.lang.reflect.Proxy`      | Uses subclassing via CGLIB                               |
| **Limitations**    | Interfaces only                     | Cannot proxy `final` classes/methods                     |
| **Performance**    | Slightly slower for interface calls | Slightly faster for direct method calls (since subclass) |
| **Spring Default** | JDK (if interface present)          | Falls back to CGLIB otherwise                            |

---

####  Choosing Proxy Type

* If your bean **implements an interface** → Spring uses **JDK proxy by default**.
* If your bean **does not implement an interface** → Spring uses **CGLIB proxy**.
* You can force CGLIB with:

```properties
spring.aop.proxy-target-class=true
```


 **Summary:**

* A **proxy** in Spring is a wrapper around a bean to apply AOP features (transactions, security, logging).
* **JDK proxies** → interface-based.
* **CGLIB proxies** → subclass-based, used when no interface exists.


177. **What is the difference between @Autowired, @Inject, and @Resource?**
     - **@Autowired**: Spring-specific, by type then by name
     - **@Inject**: JSR-330 standard, by type
     - **@Resource**: JSR-250 standard, by name then by type

178. **Can you inject a prototype bean into a singleton? How?**
Yes, you can inject a prototype bean into a singleton, but by default, the prototype bean will only be created once when the singleton is instantiated, effectively making it behave like a singleton. Here are several solutions to get a new prototype instance each time:
The Problem
```java
@Component
@Scope("singleton") // default scope
public class SingletonService {
    
    @Autowired
    private PrototypeBean prototypeBean; // Only created once!
    
    public void doSomething() {
        prototypeBean.performTask(); // Always same instance
    }
}

@Component
@Scope("prototype")
public class PrototypeBean {
    // New instance should be created each time
}
```
Solutions
1. @Lookup Method (Recommended)
```java
@Component
public abstract class SingletonService {
    
    public void doSomething() {
        PrototypeBean prototypeBean = getPrototypeBean(); // New instance each call
        prototypeBean.performTask();
    }
    
    @Lookup
    protected abstract PrototypeBean getPrototypeBean();
}
```
2. ObjectFactory or Provider
```java
@Component
public class SingletonService {
    
    @Autowired
    private ObjectFactory<PrototypeBean> prototypeBeanFactory;
    
    public void doSomething() {
        PrototypeBean prototypeBean = prototypeBeanFactory.getObject(); // New instance
        prototypeBean.performTask();
    }
}

// Or using Provider (JSR-330)
@Component
public class SingletonService {
    
    @Autowired
    private Provider<PrototypeBean> prototypeBeanProvider;
    
    public void doSomething() {
        PrototypeBean prototypeBean = prototypeBeanProvider.get(); // New instance
        prototypeBean.performTask();
    }
}
```
179. **What is the default scope of a bean in Spring?**
     Singleton scope - one instance per Spring container.

180. **How do you create custom auto-configuration?**
     Create @Configuration class with @ConditionalOn* annotations, add to META-INF/spring.factories.

181. **What is Spring Boot Actuator? Important endpoints?**
     Production-ready features for monitoring and managing applications.
     Endpoints: /health, /metrics, /info, /env, /loggers, /httptrace.

182. **How do you implement custom health checks?**
     ```java
     @Component
     public class CustomHealthIndicator implements HealthIndicator {
         @Override
         public Health health() {
             return Health.up().withDetail("custom", "All good").build();
         }
     }
     ```

183. **What is @ConditionalOnProperty, @ConditionalOnClass?**
     - **@ConditionalOnProperty**: Bean created if property exists/matches value
     - **@ConditionalOnClass**: Bean created if class is present on classpath

184. **How do you implement custom metrics and monitoring?**
     Use MeterRegistry to create custom metrics, integrate with Prometheus/Grafana.

185. **What are the Scopes in Spring?**
     - **Singleton**: One instance per container
     - **Prototype**: New instance each time
     - **Request**: One instance per HTTP request
     - **Session**: One instance per HTTP session
     - **Application**: One instance per ServletContext

186. **Prototype vs Request Scope?**
     - **Prototype**: New instance every time bean is requested
     - **Request**: One instance per HTTP request (web applications only)

#### Advanced AOP

187. **What is AOP and how is it implemented in Spring Boot?**
     Aspect-Oriented Programming separates cross-cutting concerns. Spring uses proxy-based AOP with @EnableAspectJAutoProxy.

188. **Explain @Before, @After, @Around, @AfterReturning, @AfterThrowing advices**
     - **@Before**: Executes before method
     - **@After**: Executes after method (finally block)
     - **@Around**: Surrounds method execution
     - **@AfterReturning**: Executes after successful return
     - **@AfterThrowing**: Executes when exception thrown

189. **What is a Pointcut and how do you define it?**
     Expression defining where advice should be applied.
     ```java
     @Pointcut("execution(* com.example.service.*.*(..))")
     public void serviceMethods() {}
     ```

190. **What is a JoinPoint and what data can it provide?**
     Point in program execution where aspect can be applied. Provides method signature, arguments, target object.

191. **How do you create custom annotations and intercept them using AOP?**
     ```java
     @Retention(RetentionPolicy.RUNTIME)
     @Target(ElementType.METHOD)
     public @interface Auditable {
     }
     
     @Around("@annotation(Auditable)")
     public Object audit(ProceedingJoinPoint joinPoint) throws Throwable {
         // Audit logic
         return joinPoint.proceed();
     }
     ```

192. **Real-world use cases of AOP (logging, auditing, security, caching)**
     - **Logging**: Method entry/exit logging
     - **Auditing**: Track data changes
     - **Security**: Method-level authorization
     - **Caching**: Cache method results
     - **Transaction management**: Declarative transactions

#### Advanced JPA & Database

193. **What is the N+1 select problem in JPA? How to fix it?**
     Problem: One query to get entities, then N queries for related entities.
     Solutions: @BatchSize, @Fetch(FetchMode.JOIN), entity graphs, JOIN FETCH in JPQL.

194. **What are entity graphs and how do they help?**
     Define which relationships to fetch in single query, solving N+1 problem.
     ```java
     @NamedEntityGraph(name = "User.posts", attributeNodes = @NamedAttributeNode("posts"))
     ```

195. **When would you use @Query vs derived queries vs Criteria API?**
     - **Derived queries**: Simple queries based on method names
     - **@Query**: Complex custom queries
     - **Criteria API**: Dynamic queries built programmatically

196. **How does optimistic locking work in JPA? @Version annotation?**
     Uses version field to detect concurrent modifications. Throws OptimisticLockException on conflict.

197. **What is pessimistic locking? When to use it?**
     Prevents concurrent access by locking database rows. Use for high-contention scenarios.

198. **How do you handle pagination and sorting in Spring Data JPA?**
     ```java
     Pageable pageable = PageRequest.of(0, 10, Sort.by("name"));
     Page<User> users = userRepository.findAll(pageable);
     ```

199. **What are database transactions? ACID properties?**
     Unit of work that's either fully completed or rolled back.
     ACID: Atomicity, Consistency, Isolation, Durability.

200. **What is connection pooling? HikariCP configuration?**
     Maintains cache of database connections for reuse. HikariCP is default in Spring Boot 2+.

201. **How do you implement database migrations with Flyway/Liquibase?**
     Version-controlled database schema changes. Flyway uses SQL scripts, Liquibase uses XML/YAML/JSON.

202. **What is database indexing? Query optimization strategies?**
     Indexes speed up queries by creating separate data structure. Strategies: proper indexing, query analysis, EXPLAIN plans.

#### Advanced Spring Security

203. **How do you implement OAuth2 and JWT in Spring Boot?**
     Configure OAuth2 resource server, use JWT decoder, implement custom authentication.
     ```java
     @EnableResourceServer
     public class ResourceServerConfig extends ResourceServerConfigurerAdapter {
     }
     ```

204. **What is a stateless session? How does JWT help?**
     Server doesn't store session information. JWT contains all necessary information, enabling stateless authentication.

205. **How do you implement two-factor authentication (2FA)?**
     Combine something you know (password) with something you have (phone, token). Use TOTP libraries like Google Authenticator.

206. **How does CSRF protection work in Spring?**
     Synchronizer token pattern - server generates unique token per session, validates it on state-changing requests.

207. **What is the difference between pre-auth and post-auth filters?**
     - **Pre-auth**: Authentication filters that run before reaching controller
     - **Post-auth**: Authorization filters that run after authentication

208. **How does SecurityFilterChain work in Spring Boot 3+?**
     Replaces WebSecurityConfigurerAdapter, configured as bean with lambda expressions.
     ```java
     @Bean
     public SecurityFilterChain filterChain(HttpSecurity http) throws Exception {
         return http.authorizeHttpRequests(auth -> auth.anyRequest().authenticated())
                   .oauth2ResourceServer(OAuth2ResourceServerConfigurer::jwt)
                   .build();
     }
     ```

209. **What is UserDetailsService and how do you implement it?**
     Interface for loading user-specific data during authentication.
     ```java
     @Service
     public class CustomUserDetailsService implements UserDetailsService {
         @Override
         public UserDetails loadUserByUsername(String username) {
             // Load user from database
             return User.builder().username(username).password(password).authorities(authorities).build();
         }
     }
     ```

210. **How do you implement role-based access control (RBAC)?**
     Assign roles to users, permissions to roles. Use @PreAuthorize, @Secured, or method-level security.

211. **How do you implement method-level security?**
     ```java
     @PreAuthorize("hasRole('ADMIN')")
     public void deleteUser(Long id) {
         userService.delete(id);
     }
     ```

212. **How do you secure microservices communication?**
     - Service-to-service authentication (JWT, mTLS)
     - API Gateway for centralized security
     - Service mesh (Istio) for automatic mTLS

213. **How to implement OAuth authentication in Spring Boot?**
     Configure OAuth2 client, define providers, handle authorization code flow.

#### Microservices Architecture

214. **What is the difference between monolithic and microservices architecture?**
     - **Monolithic**: Single deployable unit, shared database, tight coupling
     - **Microservices**: Multiple independent services, distributed, loose coupling

215. **How do microservices communicate with each other?**
     - **Synchronous**: REST APIs, GraphQL
     - **Asynchronous**: Message queues, event streaming

216. **What is RestTemplate? How to use it?**
     Spring's HTTP client for consuming REST services.
     ```java
     RestTemplate restTemplate = new RestTemplate();
     String result = restTemplate.getForObject("http://example.com/api/users/1", String.class);
     ```

217. **What is an API Gateway? Why is it used?**
     Single entry point for client requests. Handles routing, authentication, rate limiting, request/response transformation.

218. **What is service discovery?**
     Mechanism for services to find and communicate with each other dynamically. Examples: Eureka, Consul, Kubernetes DNS.

219. **How do you implement resilience patterns (Retry, Circuit Breaker, Bulkhead)?**
     - **Retry**: Retry failed requests with backoff
     - **Circuit Breaker**: Stop calling failing service temporarily
     - **Bulkhead**: Isolate resources to prevent cascade failures

220. **What is the Circuit Breaker pattern? Libraries like Hystrix/Resilience4j?**
     Prevents cascade failures by monitoring service calls and opening circuit when failure threshold reached.

221. **How do you implement API rate limiting?**
     Control request rate per client. Algorithms: Token bucket, sliding window. Implementation: Redis, API Gateway.

222. **What happens when one microservice becomes slow? Isolation strategies?**
     Can cause cascade failures. Strategies: timeouts, circuit breakers, bulkhead pattern, asynchronous processing.

223. **How do you handle versioning of REST APIs?**
     - URL versioning: /api/v1/users
     - Header versioning: Accept: application/vnd.api+json;version=1
     - Parameter versioning: /api/users?version=1

224. **How do you implement distributed logging and tracing (ELK, Zipkin)?**
     - **Logging**: Centralized with ELK stack (Elasticsearch, Logstash, Kibana)
     - **Tracing**: Distributed tracing with Zipkin, Jaeger, or Sleuth

225. **What's the difference between sync and async communication?**
     - **Sync**: Immediate response required, blocking
     - **Async**: Response not immediate, non-blocking, better scalability

226. **What is eventual consistency? CAP theorem?**
     - **Eventual Consistency**: System will become consistent over time
     - **CAP Theorem**: Can only guarantee 2 of 3: Consistency, Availability, Partition tolerance

227. **How do you implement saga pattern for distributed transactions?**
     Manages transactions across multiple services using sequence of local transactions with compensation actions.

228. **How do you handle data consistency across microservices?**
     - Event-driven architecture
     - Saga pattern
     - Two-phase commit (not recommended)
     - Eventual consistency

229. **Microservices architecture vs Monolithic architecture**
     - **Microservices**: Independent deployment, technology diversity, complexity
     - **Monolithic**: Simpler development, single deployment, potential bottlenecks

230. **What is producer and consumer applications?**
     - **Producer**: Generates and sends messages/events
     - **Consumer**: Receives and processes messages/events

#### Apache Kafka

231. **What are the core components of Kafka?**
     - **Broker**: Kafka server that stores and serves messages
     - **Topic**: Category or feed name for messages
     - **Partition**: Ordered log within topic
     - **Producer**: Publishes messages to topics
     - **Consumer**: Subscribes to topics and processes messages

232. **What is a Partition in Kafka? How does partitioning work?**
A Partition is a sub-division of a Kafka Topic.

Each partition is an ordered, immutable log of messages.

Messages are written sequentially and each message gets a unique, increasing offset (like an index).

Partitions are the unit of parallelism in Kafka:

More partitions → more consumers can read in parallel → higher throughput.

 **Example**:
A topic user-activity with 3 partitions:

Partition 0: [offset 0 → msg1, offset 1 → msg2, ...]

Partition 1: [offset 0 → msgA, offset 1 → msgB, ...]

Partition 2: [offset 0 → msgX, offset 1 → msgY, ...]  
**How Partitioning Works**  
When a producer sends a message to a Kafka topic, the Kafka partitioner decides which partition the message should go to.

Partition selection rules:

Key-based partitioning (default)

If you provide a message key, Kafka applies a hash function on the key → determines the partition.

Ensures all messages with the same key always go to the same partition → ordering is guaranteed per key.
```java
ProducerRecord<String, String> record = 
    new ProducerRecord<>("user-activity", "user123", "clicked_button");
producer.send(record);
```

Here, "user123" is the key → always mapped to the same partition.

Round-robin (no key)

If you don’t provide a key, messages are distributed round-robin across partitions → balances load.

Custom partitioner

You can implement your own Partitioner class in Java for custom logic.

🔹 Partitioning in Java (Example)
```java
import org.apache.kafka.clients.producer.*;

import java.util.Properties;

public class KafkaPartitioningExample {
    public static void main(String[] args) {
        Properties props = new Properties();
        props.put("bootstrap.servers", "localhost:9092");
        props.put("key.serializer", "org.apache.kafka.common.serialization.StringSerializer");
        props.put("value.serializer", "org.apache.kafka.common.serialization.StringSerializer");

        KafkaProducer<String, String> producer = new KafkaProducer<>(props);

        // With key → ensures messages for same key go to same partition
        ProducerRecord<String, String> keyedRecord =
                new ProducerRecord<>("user-activity", "user123", "Login Event");

        // Without key → round-robin partitioning
        ProducerRecord<String, String> noKeyRecord =
                new ProducerRecord<>("user-activity", "User signed up");

        producer.send(keyedRecord, (metadata, exception) -> {
            if (exception == null) {
                System.out.println("Keyed message sent to partition " + metadata.partition());
            } else {
                exception.printStackTrace();
            }
        });

        producer.send(noKeyRecord);
        producer.close();
    }
}
```
Why Partitioning Matters

Scalability → multiple partitions processed in parallel.

Ordering → ordering is guaranteed only within a partition, not across the entire topic.

Fault tolerance → partitions can be replicated to multiple brokers.

So, Partition = ordered log of messages inside a topic. Partitioning in Java is controlled via keys (deterministic hashing) or round-robin if no key is provided.

233. **What is a Kafka Topic, Producer, Consumer?**
####  Kafka Topic

* A **Topic** is a **named stream of records** (like a category or channel).
* Producers write messages **into a topic**.
* Consumers read messages **from a topic**.
* Topics are divided into **partitions**, and each partition is an ordered log of messages with unique offsets.
* Example: A topic named `orders` could store all order events in an e-commerce app.

---

####  Kafka Producer

* A **Producer** is a client application that **publishes (writes) messages** to Kafka topics.
* Producers can:

  1. Write messages **with a key** → ensures all messages with the same key go to the same partition.
  2. Write messages **without a key** → Kafka distributes them round-robin across partitions.
* Example in Java:

  ```java
  ProducerRecord<String, String> record = 
      new ProducerRecord<>("orders", "order123", "New Order Created");
  producer.send(record);
  ```

---

#### Kafka Consumer

* A **Consumer** is a client application that **subscribes to topics** and reads messages.

* Each message is identified by its **offset** within the partition.

* Consumers can work **individually** or as part of a **Consumer Group**:

  * **Single consumer** → can read all partitions of a topic.
  * **Consumer group** → partitions are distributed among group members for parallel processing.

* Example in Java:

  ```java
  consumer.subscribe(Collections.singletonList("orders"));
  while (true) {
      ConsumerRecords<String, String> records = consumer.poll(Duration.ofMillis(100));
      for (ConsumerRecord<String, String> record : records) {
          System.out.printf("Consumed record: key=%s, value=%s, partition=%d, offset=%d%n",
                            record.key(), record.value(), record.partition(), record.offset());
      }
  }
  ```

---

#### Putting It Together

* **Producer** → sends messages into a **Topic**.
* **Consumer** → subscribes to the topic and processes messages.
* **Topic** → acts as a durable, partitioned, replicated log in Kafka.

 Think of it like **YouTube**:

* A **Topic** = channel (e.g., "Tech Videos").
* A **Producer** = content creator uploading videos.
* A **Consumer** = subscribers watching videos.


234. **What are Consumer Groups? How does rebalancing work?**
     Group of consumers sharing consumption of topic. Rebalancing redistributes partitions when consumers join/leave group.

235. **What if a Kafka consumer keeps retrying endlessly? Dead letter queue?**
     Configure max retry attempts, send failed messages to dead letter topic for manual investigation.

236. **How do you ensure message ordering in Kafka?**
     Messages within same partition maintain order. Use same key for related messages to ensure same partition.

237. **What is Kafka Connect? Use cases?**
     Framework for connecting Kafka with external systems. Use cases: database CDC, log aggregation, data pipeline.

238. **How do you handle exactly-once delivery semantics?**
Excellent question 🚀 — this is one of the most important (and tricky) parts of **Kafka**.

---

#### Message Delivery Semantics

When dealing with distributed systems like Kafka, we talk about **delivery guarantees**:

1. **At most once** → messages may be lost, but never redelivered.
2. **At least once** → no messages are lost, but duplicates may occur.
3. **Exactly once** → every message is delivered **once and only once**.

Kafka’s challenge: handling **exactly once semantics (EOS)** in both **publishing** and **consumption**.

---

#### How Kafka Ensures Exactly-Once Delivery

 1. **Idempotent Producer**

* Kafka provides **idempotent producers** (`enable.idempotence=true`).
* Ensures that retries won’t cause duplicates, even if network errors happen.
* Each producer gets a **Producer ID (PID)** and every message has a **sequence number** → Kafka deduplicates automatically.

```properties
enable.idempotence=true
```

---

 2. **Transactions (Atomic Writes)**

* Kafka supports **transactions** that allow a producer to write to multiple partitions/topics atomically.
* Either **all writes succeed** or **none are visible**.
* Prevents partial updates that could break consistency.

```java
producer.initTransactions();
producer.beginTransaction();

producer.send(new ProducerRecord<>("orders", "order123", "created"));
producer.send(new ProducerRecord<>("order-audit", "order123", "audit entry"));

producer.commitTransaction();  // or abortTransaction() on failure
```

---

 3. **Consumer Offset Management with Transactions**

* Normally, consumers store their offsets in Kafka (`__consumer_offsets` topic).
* With EOS, consumers can commit **both offsets and output records in the same transaction**.
* This guarantees **exactly-once processing**:

  * If the transaction commits → output + offsets are stored.
  * If it aborts → neither is stored, and Kafka retries safely.

---

#### Configuration for Exactly Once

Producer:

```properties
enable.idempotence=true
acks=all
retries=Integer.MAX_VALUE
transactional.id=my-transactional-producer
```

Consumer:

```properties
isolation.level=read_committed
```

---

#### Key Points

* **Idempotence** removes duplicates caused by retries.
* **Transactions** ensure atomicity between producing data and committing offsets.
* **Isolation level** ensures consumers only see committed messages.
* Together, this gives Kafka **exactly-once semantics (EOS)** end-to-end.

---

**Summary:**
To handle exactly-once delivery semantics in Kafka:

1. Use **idempotent producers** (`enable.idempotence=true`).
2. Use **transactions** (`transactional.id` + `beginTransaction/commitTransaction`).
3. Configure consumers with `isolation.level=read_committed`.
----


239. **What is Kafka Streams? When to use it?**
     Library for building stream processing applications. Use for real-time data transformations, aggregations, joins.

240. **How do you monitor Kafka performance?**
     Monitor broker metrics, consumer lag, producer throughput. Tools: JMX, Confluent Control Center, Prometheus.

241. **Explain Kafka and how it handles real-time message processing**
     Distributed streaming platform using publish-subscribe model. Handles real-time processing through partitioned logs, consumer groups, and stream processing APIs.

#### Advanced Testing

242. **What's the difference between unit, integration, and E2E testing?**
     - **Unit**: Test individual components in isolation
     - **Integration**: Test component interactions
     - **E2E**: Test complete user workflows

243. **How do you mock external REST APIs in tests?**
     Use MockWebServer, WireMock, or @MockBean for Spring Boot tests.

244. **What are TestContainers? How to use with Spring Boot?**
     Library providing lightweight, disposable instances of databases, message brokers for testing.
     ```java
     @Testcontainers
     class UserServiceTest {
         @Container
         static PostgreSQLContainer<?> postgres = new PostgreSQLContainer<>("postgres:13");
     }
     ```

245. **How do you write parameterized tests in JUnit 5?**
     ```java
     @ParameterizedTest
     @ValueSource(strings = {"hello", "world"})
     void testWithStringParameter(String argument) {
         assertNotNull(argument);
     }
     ```

246. **What is the role of @DataJpaTest, @WebMvcTest, @SpringBootTest?**
     - **@DataJpaTest**: Tests JPA repositories only
     - **@WebMvcTest**: Tests web layer only
     - **@SpringBootTest**: Loads full application context

247. **How do you implement test data builders and object mothers?**
     Patterns for creating test data. Builder pattern for complex objects, Object Mother for predefined test scenarios.

248. **What is contract testing? Pact framework?**
     Testing interactions between services. Pact enables consumer-driven contracts, ensuring API compatibility.

249. **How do you implement performance testing?**
     Use JMeter, Gatling, or custom load testing. Measure response time, throughput, resource utilization.

250. **What is mutation testing?**
     Testing technique that modifies code to check if tests detect the changes. Measures test quality.

---

## EXPERT LEVEL (5+ Years / Architect Level)

### System Design & Architecture

251. **How do you design a scalable e-commerce system?**
     Use microservices architecture, separate read/write databases, implement caching layers, use CDN, design for horizontal scaling, implement event-driven architecture.

252. **How do you implement distributed caching (Redis, Hazelcast)?**
     Deploy cache cluster, implement cache-aside or write-through patterns, handle cache invalidation, monitor cache hit ratios.

253. **What is CQRS pattern? When to use it?**
     Command Query Responsibility Segregation separates read and write models. Use when read and write requirements differ significantly.

254. **How do you implement event sourcing?**
     Store events instead of current state, rebuild state by replaying events. Enables audit trail, temporal queries, and eventual consistency.

255. **What is database sharding? Strategies?**
     Horizontal partitioning of database across multiple servers. Strategies: range-based, hash-based, directory-based.

256. **How do you design for high availability?**
     Eliminate single points of failure, use redundancy, implement health checks, design for graceful degradation, use circuit breakers.

257. **What is load balancing? Different strategies?**
     Distribute incoming requests across multiple servers. Strategies: round-robin, least connections, weighted round-robin, IP hash.

258. **How do you implement API Gateway patterns?**
     Single entry point handling routing, authentication, rate limiting, request/response transformation, protocol translation.

259. **What is strangler fig pattern for legacy system migration?**
     Gradually replace legacy system by redirecting functionality to new system until legacy system is completely replaced.

260. **How do you design monitoring and alerting systems?**
     Implement metrics collection, log aggregation, distributed tracing, define SLIs/SLOs, set up alerting rules, create dashboards.

261. **How does Redis caching work, and when should it be used?**
     In-memory data structure store. Use for session storage, caching, pub/sub messaging, real-time analytics.

### DevOps & Cloud

262. **How do you containerize a Spring Boot app with Docker?**
     ```dockerfile
     FROM openjdk:17-jre-slim
     COPY target/app.jar app.jar
     EXPOSE 8080
     ENTRYPOINT ["java", "-jar", "/app.jar"]
     ```

263. **What is Docker compose? Multi-stage Docker builds?**
     Docker Compose defines multi-container applications. Multi-stage builds optimize image size by separating build and runtime environments.

264. **How do you create a Jenkins pipeline for Java apps?**
     Use Jenkinsfile with pipeline as code, define stages: checkout, build, test, package, deploy.

265. **What is the difference between blue-green and rolling deployments?**
     - **Blue-Green**: Two identical environments, switch traffic instantly
     - **Rolling**: Gradually replace instances one by one

266. **How do you implement zero-downtime deployment?**
     Use blue-green deployment, rolling updates, health checks, graceful shutdown, load balancer configuration.

267. **What is infrastructure as code? Terraform basics?**
     Define infrastructure using code. Terraform uses HCL to provision and manage infrastructure across multiple cloud providers.

268. **How do you handle secrets management (Vault, K8s secrets)?**
     Use dedicated secret management systems, encrypt at rest and in transit, implement secret rotation, follow principle of least privilege.

269. **What is monitoring and observability? Prometheus, Grafana setup?**
     - **Monitoring**: Collecting metrics and logs
     - **Observability**: Understanding system behavior from outputs
     - **Setup**: Prometheus for metrics, Grafana for visualization

270. **JAR vs WAR files**
     - **JAR**: Java Archive, contains Java classes and resources
     - **WAR**: Web Archive, contains web applications for deployment to servlet containers

271. **Maven vs Gradle**
     - **Maven**: XML-based, convention over configuration, extensive plugin ecosystem
     - **Gradle**: Groovy/Kotlin DSL, flexible, faster incremental builds

272. **Continuous Integration vs Continuous Deployment**
     - **CI**: Automatically build and test code changes
     - **CD**: Automatically deploy tested changes to production

#### Kubernetes & Cloud Native

273. **What is Kubernetes? Pods, Services, Deployments?**
     Container orchestration platform.
     - **Pod**: Smallest deployable unit, contains one or more containers
     - **Service**: Network abstraction for accessing pods
     - **Deployment**: Manages pod replicas and updates

274. **How do you deploy Spring Boot apps on Kubernetes?**
     Create Docker image, define Deployment, Service, ConfigMap, and Ingress manifests.

275. **What is a sidecar container? Use cases?**
     Additional container in pod providing supporting functionality. Use cases: logging, monitoring, service mesh proxy.

276. **How do you handle configuration in K8s (ConfigMaps, Secrets)?**
     - **ConfigMaps**: Non-sensitive configuration data
     - **Secrets**: Sensitive data like passwords, tokens

277. **What is service mesh? Istio basics?**
     Infrastructure layer handling service-to-service communication. Istio provides traffic management, security, observability.

278. **How do you implement autoscaling in K8s?**
     - **HPA**: Horizontal Pod Autoscaler based on CPU/memory
     - **VPA**: Vertical Pod Autoscaler adjusts resource requests
     - **Cluster Autoscaler**: Scales cluster nodes

279. **What is ingress controller?**
     Manages external access to services, provides load balancing, SSL termination, name-based virtual hosting.

280. **How do you implement health checks in K8s?**
     Define liveness and readiness probes in pod specifications.

281. **What is Helm? Chart management?**
     Package manager for Kubernetes. Charts are packages of pre-configured K8s resources.

282. **Cloud-native patterns for Java applications?**
     12-factor app principles, microservices, containerization, service discovery, external configuration, circuit breakers.

#### Performance & Troubleshooting

283. **How do you profile Java applications?**
     Use profiling tools: JProfiler, YourKit, VisualVM, Java Flight Recorder, async-profiler.

284. **How to debug memory leaks?**
     Generate heap dumps, analyze with MAT or VisualVM, identify objects with high retention, check for static collections, unclosed resources.

285. **How to analyze thread dumps?**
     Look for thread states, identify deadlocks, find blocked threads, analyze thread pool usage.

286. **Gateway Timeout vs Service Unavailable - troubleshooting?**
     - **504 Gateway Timeout**: Check upstream service response time, network connectivity
     - **503 Service Unavailable**: Check service health, resource availability, load balancer configuration

287. **How do you optimize database queries?**
     Use EXPLAIN plans, add proper indexes, avoid N+1 queries, optimize JOINs, consider query caching.

288. **How to handle high CPU usage in production?**
     Identify root cause with profiling, check for infinite loops, optimize algorithms, scale horizontally.

289. **What tools do you use for application monitoring?**
     APM tools: New Relic, Datadog, AppDynamics. Open source: Prometheus, Grafana, Jaeger, ELK stack.

290. **How do you implement distributed tracing?**
     Use OpenTracing/OpenTelemetry, instrument code with trace spans, propagate trace context, visualize with Jaeger/Zipkin.

291. **Service Not Found — how to troubleshoot?**
     Check service discovery, DNS resolution, network connectivity, service health, configuration.

292. **How to debug locally & remotely?**
     - **Local**: IDE debugger, unit tests, integration tests
     - **Remote**: Remote debugging ports
