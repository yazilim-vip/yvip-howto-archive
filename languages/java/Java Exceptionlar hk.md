Java Exceptionlar hk

https://stackoverflow.com/questions/11017304/catching-java-errors

Java'da error'leri consola basarken System.err'e değilde System.out'a bastırılmak istenirse Exception sınıfındaki printStackTrace metodu aşağıdaki şekilde kullanılabilir:
    e.printStackTrace(System.out);

Kaynak: https://stackoverflow.com/questions/23588123/why-does-the-execution-order-between-the-printstacktrace-and-the-other-methods