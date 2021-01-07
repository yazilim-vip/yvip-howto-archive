# PostConstruct Annotation
- because when the constructor is called, the bean is not yet initialized - i.e. no dependencies are injected. In the **@PostConstruct** method the bean is fully initialized and you can use the dependencies.

- because this is the contract that guarantees that this method will be invoked only once in the bean lifecycle. It may happen (though unlikely) that a bean is instantiated multiple times by the container in its internal working, but it guarantees that @PostConstruct will be invoked only once.

Reference: https://stackoverflow.com/questions/3406555/why-use-postconstruct