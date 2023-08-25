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
   UML => 6.07 association(aggregation, composition)
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
          singleton instance, to avoid this add a method `readresolve`
