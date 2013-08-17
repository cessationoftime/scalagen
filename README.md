**Scalagen - Java to Scala conversion**

Scalagen is a Java to Scala conversion tool. It uses a Java based parser for Java sources and provides modular 
transformation of the AST to match Scala idioms. The resulting transformed AST is serialized into Scala format.

Here is a list of example Java sources which have been successfully converted by Scalagen:
https://github.com/mysema/scalagen/tree/master/scalagen/src/test/scala/com/mysema/examples

Scalagen has also been tested on our own projects such as Querydsl, RDFBean, Codegen and some customer projects.

**Usage**

Scalagen provides direct Maven support via a plugin. No need to install,or mess with the POM file, it will be pulled from Maven Central.
You can use it directly via the command line like this

    mvn com.mysema.scalagen:scalagen-maven-plugin_2.10.1:0.3.0:main -DtargetFolder=target/scala
    
and for test sources

    mvn com.mysema.scalagen:scalagen-maven-plugin_2.10.1:0.3.0:test -DtargetFolder=target/scala

The conversion results are to be seen as a starting point for the Java to Scala conversion. 
Some elements are not transformed correctly for various reasons and will need manual intervention.
