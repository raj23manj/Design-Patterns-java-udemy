# Design-Patterns

1) DRY(Do not repeat yourself)
2) Kiss (keep it simple and stupid)
3) Yagni (you aren;t going to need it)
4) Slap (single level of abstraction)
5) Delegation Principle
6) SOLID 
   - single responsibility
   - open for extension closed for modification
   - Liskov substitution principle
   - Interface seggregation
   - Dependency Inversion
7) UML & Sequence Diagram: 
   ##### UML
   - UML => 6.07 association(aggregation, composition)
          example => 1) Teacher teaches a subject(teacher without teacing anything cannot exisit) this is assosition
                     2) A department can have teacher, a teacher can exisit without a department, this is aggregation
                     3) A Department must have a department manager, if there is no department then no manager, this is composition  
9) ### Design Patterns

      #### Structural Patterns
      
        - Prototype pattern
          create only one object and clone it and give
        - Builder pattern
          has a director -> concrete builder -> interface(abstract class) -> entity
        - Factory Design Pattern(class/method)
          files DB.java(method), FactoryDesignPattern, DatabaseFactory
        - Singleton pattern
          make constructor private, access instace using a getter. When Singleton class implements serialiseable, when seriliasing and deserialising we will get two
          singleton instance, to avoid this add a method `readresolve`. 
          Using reflection api we can get the constructor of the class and get a new instance, to avoid this we can use a Enum singleton, but serializatoin problem
          discused above will exisits, and no classes can inherit from this ENUM. If there is private variables with getters and setters in Enum class that won't get
          serialized. 
          To handle exception while object creation use static block, this is ideal way of creating a singleton instance. This way the instance gets created at class
          loading
          We can create lazy singleton, meaning create the singlenton instance only when we need it and not before, there is issue in multithreaded env, and threads can
          create multiple instances to avoid this, we can make the method as `synchronised`
