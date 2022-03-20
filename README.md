# Scala



Notes-:
Repl -: Recent evaluation print loop
val is immutable
var is mutable
for help use 
:help
ctrl + d #to exit

```
>>  sbt
>>  sbt console or start scala


scala> def max(x: Int,y: Int): Int=if (x>y) x else y
max: (x: Int, y: Int)Int

scala> max(5,7)
res2: Int = 7

scala> def say(name: String)=println(s"Hello $name")
say: (name: String)Unit

scala> say("Priyanshu")
Hello Priyanshu

scala> deg say(name: String){
     | println(s"Hello $name)
<console>:2: error: unclosed string literal
       println(s"Hello $name)
                            ^

scala> deg say(name: String){
     | println(s"Hello $name")
     | }
<console>:12: error: not found: value deg
       deg say(name: String){
       ^
<console>:12: error: not found: value name
       deg say(name: String){
               ^
<console>:13: error: not found: value name
       println(s"Hello $name")
                        ^

scala> def say(name: String) {println(s"Hello $name")
     | }
say: (name: String)Unit

scala>

scala> say("Sing")
Hello Sing

scala> a=10
<console>:11: error: not found: value a
       a=10
       ^
<console>:12: error: not found: value a
       val $ires0 = a
                    ^

scala> val a=10
a: Int = 10

scala> val b=20
b: Int = 20

scala> if (a>b) println(s"Max is $a") else println(s"Max is $b")
Max is 20

scala> def add(a:Int,b:Int){
     | result=a+b}
<console>:14: error: not found: value result
       result=a+b}
       ^

scala> def add(a:Int,b:Int){
     | val result=a+b}
add: (a: Int, b: Int)Unit

scala> add(5,6)

scala> def add(a:Int,b:Int){
     | val result=a+b
     | result
     | {
     | }
     |
     |
[warn] Canceling execution...
java.lang.InterruptedException
        at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.reportInterruptAfterWait(Unknown Source)
        at java.util.concurrent.locks.AbstractQueuedSynchronizer$ConditionObject.awaitNanos(Unknown Source)
        at java.util.concurrent.LinkedBlockingQueue.poll(Unknown Source)
        at sbt.internal.util.Terminal$proxyInputStream$.poll$1(Terminal.scala:675)
        at sbt.internal.util.Terminal$proxyInputStream$.read(Terminal.scala:681)
        at jline.console.ConsoleReader$1.read(ConsoleReader.java:227)
        at jline.internal.NonBlockingInputStream.read(NonBlockingInputStream.java:245)
        at jline.internal.InputStreamReader.read(InputStreamReader.java:258)
        at jline.internal.InputStreamReader.read(InputStreamReader.java:195)
        at jline.console.ConsoleReader.readCharacter(ConsoleReader.java:2180)
        at jline.console.ConsoleReader.readCharacter(ConsoleReader.java:2170)
        at jline.console.ConsoleReader.readBinding(ConsoleReader.java:2255)
        at jline.console.ConsoleReader.readLine(ConsoleReader.java:2496)
        at jline.console.ConsoleReader.readLine(ConsoleReader.java:2407)
        at jline.console.ConsoleReader.readLine(ConsoleReader.java:2395)
        at scala.tools.nsc.interpreter.jline.InteractiveReader.readOneLine(JLineReader.scala:63)
        at scala.tools.nsc.interpreter.InteractiveReader.readLine(InteractiveReader.scala:45)
        at scala.tools.nsc.interpreter.InteractiveReader.readLine$(InteractiveReader.scala:42)
        at scala.tools.nsc.interpreter.jline.InteractiveReader.readLine(JLineReader.scala:31)
        at scala.tools.nsc.interpreter.ILoop.interpretStartingWith(ILoop.scala:875)
        at scala.tools.nsc.interpreter.ILoop.interpretStartingWith(ILoop.scala:883)
        at scala.tools.nsc.interpreter.ILoop.interpretStartingWith(ILoop.scala:883)
        at scala.tools.nsc.interpreter.ILoop.interpretStartingWith(ILoop.scala:883)
        at scala.tools.nsc.interpreter.ILoop.interpretStartingWith(ILoop.scala:883)
        at scala.tools.nsc.interpreter.ILoop.interpretStartingWith(ILoop.scala:883)
        at scala.tools.nsc.interpreter.ILoop.command(ILoop.scala:733)
        at scala.tools.nsc.interpreter.ILoop.processLine(ILoop.scala:435)
        at scala.tools.nsc.interpreter.ILoop.loop(ILoop.scala:456)
        at scala.tools.nsc.interpreter.ILoop.process(ILoop.scala:1048)
        at xsbt.ConsoleBridge.run(ConsoleBridge.scala:75)
        at sbt.internal.inc.AnalyzingCompiler.console(AnalyzingCompiler.scala:208)
        at sbt.Console.console0$1(Console.scala:64)
        at sbt.Console.$anonfun$apply$5(Console.scala:74)
        at sbt.Run$.executeSuccess(Run.scala:186)
        at sbt.Console.$anonfun$apply$4(Console.scala:74)
        at sbt.internal.util.Terminal.withRawInput(Terminal.scala:145)
        at sbt.internal.util.Terminal.withRawInput$(Terminal.scala:143)
        at sbt.internal.util.Terminal$ProxyTerminal$.withRawInput(Terminal.scala:384)
        at sbt.Console.$anonfun$apply$3(Console.scala:74)
        at sbt.internal.util.Terminal$TerminalImpl.withRawOutput(Terminal.scala:975)
        at sbt.internal.util.Terminal$ProxyTerminal$.withRawOutput(Terminal.scala:423)
        at sbt.Console.apply(Console.scala:71)
        at sbt.Console.apply(Console.scala:49)
        at sbt.Console.apply(Console.scala:41)
        at sbt.Defaults$.$anonfun$consoleTask$1(Defaults.scala:2232)
        at sbt.Defaults$.$anonfun$consoleTask$1$adapted(Defaults.scala:2218)
        at scala.Function1.$anonfun$compose$1(Function1.scala:49)
        at sbt.internal.util.$tilde$greater.$anonfun$$u2219$1(TypeFunctions.scala:62)
        at sbt.std.Transform$$anon$4.work(Transform.scala:68)
        at sbt.Execute.$anonfun$submit$2(Execute.scala:282)
        at sbt.internal.util.ErrorHandling$.wideConvert(ErrorHandling.scala:23)
        at sbt.Execute.work(Execute.scala:291)
        at sbt.Execute.$anonfun$submit$1(Execute.scala:282)
        at sbt.ConcurrentRestrictions$$anon$4.$anonfun$submitValid$1(ConcurrentRestrictions.scala:265)
        at sbt.CompletionService$$anon$2.call(CompletionService.scala:64)
        at java.util.concurrent.FutureTask.run(Unknown Source)
        at java.util.concurrent.Executors$RunnableAdapter.call(Unknown Source)
        at java.util.concurrent.FutureTask.run(Unknown Source)
        at java.util.concurrent.ThreadPoolExecutor.runWorker(Unknown Source)
        at java.util.concurrent.ThreadPoolExecutor$Worker.run(Unknown Source)
        at java.lang.Thread.run(Unknown Source)

That entry seems to have slain the compiler.  Shall I replay
your session? I can re-run each line except the last one.
[y/n]
You must enter y or n.
That entry seems to have slain the compiler.  Shall I replay
your session? I can re-run each line except the last one.
[y/n]
Abandoning crashed session.

scala>

scala> def add(a:Int,b:Int){
     | val result=a+b
     | result
     | }
<console>:15: warning: multiline expressions might require enclosing parentheses; a value can be silently discarded when Unit is expected
       result
       ^
<console>:15: warning: a pure expression does nothing in statement position
       result
       ^
add: (a: Int, b: Int)Unit

scala> add(5,6)

scala>  def add(a:Int,b:Int){
     |      | val result=a+b
<console>:2: error: ';' expected but 'val' found.
            | val result=a+b
              ^

scala>      | result
<console>:12: error: not found: value result
        result
        ^

scala> def add(a:Int,b:Int)={
     | val result=a+b
     | }
add: (a: Int, b: Int)Unit

scala> add(5,6)

scala> val sum=add(5,6)
sum: Unit = ()

scala> sum

scala> def add(a:Int,b:Int)={
     | val result=a+b
     | result
     | }
add: (a: Int, b: Int)Int

scala> add(4,5)
res12: Int = 9

scala> def SAD(a:Int,b:Int): (Int,Int)={
     | val sum=a+b
     | val diff=a-b
     | (sum,diff)
     | }
SAD: (a: Int, b: Int)(Int, Int)

scala> val res=SAD(10,5)
res: (Int, Int) = (15,5)

scala> res._1
res13: Int = 15

scala> res._2
res14: Int = 5

scala> val (sm,df)=SAD(10,5)
sm: Int = 15
df: Int = 5

scala> val (a,b,c)=(0,'a',1)
a: Int = 0
b: Char = a
c: Int = 1

scala> a
res15: Int = 0

scala> b
res16: Char = a

scala> val x=1+2
x: Int = 3

scala> 1.+(2)
res17: Int = 3

scala> val s="Hello"
s: String = Hello

scala> s.charAt(1)
res18: Char = e

scala> s.charAt 1
<console>:1: error: ';' expected but integer literal found.
       s.charAt 1
                ^

scala> s charAt 1
res19: Char = e

scala> list(1,2,3).map(_*2)
<console>:12: error: not found: value list
       list(1,2,3).map(_*2)
       ^

scala> List(1,2,3).map(_*2)
res21: List[Int] = List(2, 4, 6)

scala> println("Hello")
Hello

scala> println "Hello"
<console>:1: error: ';' expected but string literal found.
       println "Hello"
               ^

scala> System.out.println "Hello"
<console>:1: error: ';' expected but string literal found.
       System.out.println "Hello"
                          ^

scala> System.out println "Hello"
Hello

scala> val args=Array("Pk","Singh")
args: Array[String] = Array(Pk, Singh)

scala> val args=Array(1,2,3,4,5)
args: Array[Int] = Array(1, 2, 3, 4, 5)

scala> args[0]
<console>:1: error: identifier expected but integer literal found.
       args[0]
            ^

scala> args._1
<console>:13: error: value _1 is not a member of Array[Int]
       args._1
            ^

scala> ags(0)
<console>:12: error: not found: value ags
       ags(0)
       ^

scala> args(0)
res26: Int = 1

scala> LocalDate.now()
<console>:12: error: not found: value LocalDate
       LocalDate.now()
       ^

scala> import java.time._
import java.time._

scala> LocalDate.now()
res28: java.time.LocalDate = 2022-03-18

scala> now()
<console>:15: error: not found: value now
       now()
       ^

scala> args(0)="Priyanshu"
<console>:16: error: type mismatch;
 found   : String("Priyanshu")
 required: Int
       args(0)="Priyanshu"
               ^

scala> args
res31: Array[Int] = Array(1, 2, 3, 4, 5)

scala> args(0)=10

scala> args
res33: Array[Int] = Array(10, 2, 3, 4, 5)

scala> type(args)
<console>:1: error: identifier expected but '(' found.
       type(args)
           ^

scala> args.update(1,12)

scala> args
res35: Array[Int] = Array(10, 12, 3, 4, 5)

scala> val lis=List(1,2,3)
lis: List[Int] = List(1, 2, 3)

scala> lis
res36: List[Int] = List(1, 2, 3)

scala> lis.apply(0)
res37: Int = 1

scala> lis(0)
res38: Int = 1

scala> lis(0)=2
<console>:16: error: value update is not a member of List[Int]
       lis(0)=2
       ^

scala> val arr2=Array(1,2,3)
arr2: Array[Int] = Array(1, 2, 3)

scala> val arr2=Array[Int](1,2,3)
arr2: Array[Int] = Array(1, 2, 3)

scala> arr2.size
res40: Int = 3

scala> +
<console>:15: error: not found: value +
       +
       ^

scala> :help
All commands can be abbreviated, e.g., :he instead of :help.
:completions <string>    output completions for the given string
:edit <id>|<line>        edit history
:help [command]          print this summary or command-specific help
:history [num]           show the history (optional num is commands to show)
:h? <string>             search the history
:imports [name name ...] show import history, identifying sources of names
:implicits [-v]          show the implicits in scope
:javap <path|class>      disassemble a file or class name
:line <id>|<line>        place line(s) at the end of history
:load <path>             interpret lines in a file
:paste [-raw] [path]     enter paste mode or paste a file
:power                   enable power user mode
:quit                    exit the interpreter
:replay [options]        reset the repl and replay all previous commands
:require <path>          add a jar to the classpath
:reset [options]         reset the repl to its initial state, forgetting all session entries
:save <path>             save replayable session to a file
:sh <command line>       run a shell command (result is implicitly => List[String])
:settings <options>      update compiler options, if possible; see reset
:silent                  disable/enable automatic printing of results
:type [-v] <expr>        display the type of an expression without evaluating it
:kind [-v] <type>        display the kind of a type. see also :help kind
:warnings                show the suppressed warnings from the most recent line which had any

scala> Nil
res42: scala.collection.immutable.Nil.type = List()

scala> Nil.::(1).::(2)
res43: List[Int] = List(2, 1)

scala> l1=List(1,2,3)
<console>:14: error: not found: value l1
       l1=List(1,2,3)
       ^
<console>:15: error: not found: value l1
       val $ires1 = l1
                    ^

scala> val l1=List(1,2,3)
l1: List[Int] = List(1, 2, 3)

scala> val l2=List(4,5,6)
l2: List[Int] = List(4, 5, 6)

scala> l1:::l2
res44: List[Int] = List(1, 2, 3, 4, 5, 6)

scala> l2:::l1
res45: List[Int] = List(4, 5, 6, 1, 2, 3)

scala> val arr1: Seq[Int]=Array(1,2,3)
arr1: Seq[Int] = WrappedArray(1, 2, 3)

scala> l1(0)=12
<console>:16: error: value update is not a member of List[Int]
       l1(0)=12
       ^

scala>  Vector(1,2,3)
res47: scala.collection.immutable.Vector[Int] = Vector(1, 2, 3)

scala> Sets(List(1,2,3,1,2,3,454))
<console>:15: error: not found: value Sets
       Sets(List(1,2,3,1,2,3,454))
       ^

scala> Set(List(1,2,3,1,2,3,454))
res49: scala.collection.immutable.Set[List[Int]] = Set(List(1, 2, 3, 1, 2, 3, 454))

scala>  List(1,2,3,1,2,3,454)
res50: List[Int] = List(1, 2, 3, 1, 2, 3, 454)

scala> lis= List(1,2,3,1,2,3,454)
<console>:15: error: reassignment to val
       lis= List(1,2,3,1,2,3,454)
          ^

scala> val lis= List(1,2,3,1,2,3,454)
lis: List[Int] = List(1, 2, 3, 1, 2, 3, 454)

scala> Set(lis)
res51: scala.collection.immutable.Set[List[Int]] = Set(List(1, 2, 3, 1, 2, 3, 454))

scala> Set(1,23,4,1,2,343,54)
res52: scala.collection.immutable.Set[Int] = Set(1, 343, 2, 54, 23, 4)

scala> new Array[String](3)
res53: Array[String] = Array(null, null, null)

scala> new Array[String](2)
res54: Array[String] = Array(null, null)

scala> new Array[String](10)
res55: Array[String] = Array(null, null, null, null, null, null, null, null, null, null)

scala> map('a'->1)
<console>:15: error: not found: value map
       map('a'->1)
       ^

scala> Map('a'->1)
res57: scala.collection.immutable.Map[Char,Int] = Map(a -> 1)

scala> a
res58: Int = 0

scala> var m1=Map('a'->1)
m1: scala.collection.immutable.Map[Char,Int] = Map(a -> 1)

scala> m1
res59: scala.collection.immutable.Map[Char,Int] = Map(a -> 1)

scala> m1(a)
<console>:17: error: type mismatch;
 found   : Int
 required: Char
       m1(a)
          ^

scala> "hello"->43
res61: (String, Int) = (hello,43)

scala> "hello".->55
<console>:1: error: ';' expected but integer literal found.
       "hello".->55
                 ^

scala> "hello".->(55)
res62: (String, Int) = (hello,55)

scala> var String="hello"
String: String = hello

scala> String.reverse
res63: String = olleh

scala> val mapToRiches=Map(1->"One",2->"Two",3->"Three")
mapToRiches: scala.collection.immutable.Map[Int,String] = Map(1 -> One, 2 -> Two, 3 -> Three)

scala> for((step,instructions)<-mapToRiches){
     | println(s"Step $step - $instructions")
     | }
Step 1 - One
Step 2 - Two
Step 3 - Three

scala>

scala> cd
<console>:15: error: not found: value cd
       cd
       ^

scala> import scala.io.Source
import scala.io.Source

scala> for(line<-Source.fromFile("file.txt").getLines()){
     | println(line)
     | }
Unity in Diversity means unity among people who has certain differences. These differences may be related to there place of leaving, their culture, their religion, and their class. If you are leaving in India you can see different cultures are leaving in a different part of the country with language change is common someplace it changes after every 50km, It may be a small change or large change. In some cultures, people take the bear and some not but they are leaving and working together for their professional point of view. The best thing about unity in diversity is that we are learning something new like there food, If north Indian leaves with south Indian guy then there definitely share there food like the south have dosa and the north one have samosa and so on.
```
### Class
```
scala> class A{
     | val x=10
     | val y=x*2
     | def timesY(a:Int):Int=a*y
     | }
defined class A

scala> val A=new A
A: A = A@a6bdb57

scala> A.x
res0: Int = 10

scala> A.y
res1: Int = 20

scala> A.timesY(4)
res2: Int = 80
```

### FileWrite
```
scala> import java.io._

scala> class WriteOutput(writer: PrintWriter){
     | def write(s:String): Unit=writer.println(s)
     | }
// defined class WriteOutput
scala> val out1=new WriteOutput(ex1)
val out1: WriteOutput = WriteOutput@7574d4ad

scala> out1.write("Hello")

scala> out1.write("to")

scala> out1.write("you")

scala> ex1.close()
```
### if-else(no ternary)
```
scala>  if(a>b){println(a)}else{println(b)}
10
```
### Try-catch
```
scala> try{
     | require(a,"A should be true")
     | a
     | } catch{ case ex: IllegalArgumentException=>0}
val res1: AnyVal = 0
```
### For
```
scala> for (i<-1 to 10) println(i*i)
1
4
9
16
25
36
49
64
81
100

scala> (1 to 10).foreach(i=> println(i*i))
1
4
9
16
25
36
49
64
81
100

scala> for {
     | i<-1 to 3
     | j<-1 to 3
     | }{ println(i*j)}
1
2
3
2
4
6
3
6
9

scala> for (i<-1 to 10) yield i*i
val res2: IndexedSeq[Int] = Vector(1, 4, 9, 16, 25, 36, 49, 64, 81, 100)

scala> (1 to 3).flatMap(i=>(1 to 3).map(j=>i*3))
val res3: IndexedSeq[Int] = Vector(3, 3, 3, 6, 6, 6, 9, 9, 9)

scala> for {
     | v1<- 1 to 3
     | v2<- 4 to 6
     | v3<- 7 to 9
     | } yield v1+v2+v3
val res4: IndexedSeq[Int] = Vector(12, 13, 14, 13, 14, 15, 14, 15, 16, 13, 14, 15, 14, 15, 16, 15, 16, 17, 14, 15, 16, 15, 16, 17, 16, 17, 18)
```

### Mathc- Case Similar to Switch Case
```

scala> val x=1
val x: Int = 1

scala> x match{
     | case 1=> println("One")
     | case 2=> println("Two")
     | case 3=> println("Three")
     | case _=>  println("Something else")
     | }
One

scala> val res=x match{
     | case 1=> "one"
     | case 2=> "two"
     | case _=> "Something else"
     | }
val res: String = one

scala> val n = -1
scala> n match{
     | case 0=> "Zero"
     | case v if v>0 => "positive"
     | case v => "negative"
     | }
val res5: String = negative
```
### String interpotation
![img](https://user-images.githubusercontent.com/55645997/159112220-86d9c2c6-266e-488b-b135-6e44745d5eae.jpeg)

### Higher Order Function
```
scala> val nums=(1 to 10).toList
val nums: List[Int] = List(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)

scala> nums.map(x=>x*x)
val res0: List[Int] = List(1, 4, 9, 16, 25, 36, 49, 64, 81, 100)

scala> nums.filter(x=>x%2==0)
val res1: List[Int] = List(2, 4, 6, 8, 10)

scala> nums.span(x=>x%4!=0)
val res2: (List[Int], List[Int]) = (List(1, 2, 3),List(4, 5, 6, 7, 8, 9, 10))

scala> nums.partition(x=>x%4!=0)
val res3: (List[Int], List[Int]) = (List(1, 2, 3, 5, 6, 7, 9, 10),List(4, 8))

scala> nums.partition(x=>x%4!=0)(1)
val res4: List[Int] = List(4, 8)

scala> val res=nums.reduce((x,y)=>x max y)
val res: Int = 10

scala> nums.reduce((x:Int,y:Int)=>x+y)
val res5: Int = 55

```

### Partial app
```
scala> val num3=(a: Int,b: Int,c: Int)=>a+b+c
val num3: (Int, Int, Int) => Int = Lambda$1611/2101881246@17810908

scala> val add=num3(6,(_:Int),3)
val add: Int => Int = Lambda$1623/1218021867@6d97a357

scala> add
val res6: Int => Int = Lambda$1623/1218021867@6d97a357

scala> add(2)
val res7: Int = 11
```
