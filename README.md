Download Link: https://assignmentchef.com/product/solved-coursework-assignment-2
<br>
<p class="ui header product-top-header" title="Coursework assignment 2 Solution"><strong>Introduction</strong>This is Coursework assignment 2 (of 2 coursework assignments in total) for 2016–2017. Part (A) asks that you demonstrate an understanding of parsing with String.split(), writing to and reading from a file and serialization. Part (B) looks at String.format() and the Comparator interface in the context of a client/server system.

<strong>IMPORTANT NOTE:</strong> Please use the most recent version of Java, Java 8.

<strong>Electronic files you should have:</strong>Part A

• TextQuestion.java• TextQuestionUtils.java• testquestions.txt

Part B

• Client.java• ClientGUI.java• CourseworkComparator.java• History.java• ServerUtils.java• Student.java• StudentFileReader.java• StudentServer.java• StudentServerEngine.java• TotalComparator.java• marks.txt

<strong>What you should hand in: very important</strong>At the end of each section there is a list of files to be handed in – <strong>please note the</strong><strong>handing-in requirements supersede the generic University of London instructions.</strong>Please ensure that you hand in <strong>electronic versions</strong> of your .java files since you cannot gain any marks without handing them in. Class files are not needed, and any student handing in only a class file will <strong>not</strong> receive any marks for that part of the coursework assignment, <strong>so please be careful about what you upload as you could fail if you submit incorrectly.</strong>There is one mark allocated for handing in uncompressed files – that is, students who hand in zipped or .tar files or any other form of compressed files can only score 49/50 marks.There is one mark allocated for handing in files that are <strong>not</strong> contained in a directory;

students who upload their files in a directory can only achieve 49/50 marks.Please put your name and student number as a comment at the top of each .java file that you hand in.

<strong>The examiners intend to compile and run your Java programs; for this reason, </strong><strong>programs that do not compile will not receive any marks.</strong>

Your are asked to give your classes certain names; please follow these instructions carefully. Make sure there is no conflict between your file name and class names.Remember that if you give your files names that are different from the names of your classes (e.g. cwk1-partA.java file name versus TextQuestionUtils (class name) your  program will not compile because of the conflict between the file name and the class name.Students who hand in files containing their java classes that cannot be compiled (e.g. PDFs) will not be given any marks for that part of the coursework assignment.

<strong>List interface</strong>You will note that in the files you have been given, ArrayLists are declared to be of type List, as are methods that return an ArrayList. List is an interface:<a href="https://docs.oracle.com/javase/7/docs/api/java/util/List.html" target="_blank" rel="nofollow noopener">http://docs.oracle.com/javase/7/docs/api/java/util/List.html</a>

<em>Explanation below, modified from Effective Java, 2nd edition by Joshua Bloch</em>You should use interfaces rather than classes as parameter types. More generally, you should favour the use of interfaces rather than classes to refer to objects. If appropriate interface types exist, then parameters, return values, variables and fields should all be declared using interface types.

Get in the habit of typing this:

// Good – uses interface as type

List&lt;Subscriber subscribers = new ArrayList&lt;Subscriber();rather than this:

// Bad – uses class as type!

ArrayList&lt;Subscriber subscribers = new ArrayList&lt;Subscriber();

If you get into the habit of using interfaces as types, your program will be much more flexible. If you decide that you want to switch implementations, all you have to do is change the class name in the constructor.

For example, the first declaration could be changed to read:List&lt;Subscriber subscribers = new LinkedList&lt;Subscriber(); and all of the surrounding code would continue to work. The surrounding code was unaware of the old implementation type, so it would be oblivious to the change.

<strong>Part A</strong>Consider the <em>TextQuestionUtils class</em>. The output of the completed class should be:

<em>/******* parsed from text file testquestions.txt *******/</em><em>Is it true that event sources (such as a JButton) can be only</em><em>be registered with one event handler? no</em><em>What is the class that all exceptions sub-class?</em><em>java.lang.Exception</em><em>Should Swing applications directly call the paintComponent()</em><em>method? no</em><em>Java has two types of stream; chain is one, what is the other?</em><em>connection</em><em>Is a child class serializable if the parent class is? yes</em><em>How many areas does BorderLayoutManager have? 5</em><em>/******* parsed from text file written by</em><em>TextQuestionUtil.writeToFile() *******/</em><em>Is it true that event sources (such as a JButton) can be only</em><em>be registered with one event handler? no</em><em>What is the class that all exceptions sub-class?</em><em>java.lang.Exception</em><em>Should Swing applications directly call the paintComponent()</em><em>method? no</em><em>Java has two types of stream; chain is one, what is the other?</em><em>connection</em><em>Is a child class serializable if the parent class is? yes</em><em>How many areas does BorderLayoutManager have? 5</em><em>/******* deserialised from a file *******/</em><em>Is it true that event sources (such as a JButton) can only be</em><em>registered with one event handler? no</em><em>What is the class that all exceptions sub-class?</em><em>java.lang.Exception</em><em>Should Swing applications directly call the paintComponent()</em><em>method? no</em><em>Java has two types of stream; chain is one, what is the other?</em><em>connection</em><em>Is a child class serializable if the parent class is? yes</em><em>How many areas does BorderLayoutManager have? 5</em>You are tasked with completing the methods in the TextQuestionUtils class such that the output in your revised class is the same as that above. Please do not change the method headings, the main method or the test() method as you complete the following tasks:

1. You are given the heading of the serializeToFile(String, List&lt;TextQuestion) method. Complete the method. In your answer make sure that the method does what the comments written above the heading say it will do. [7 marks]

2. You are given the heading of the deserializeFromFile(String) method.Complete the method. In your answer make sure that the method does what the comments written above the heading say it will do. [7 marks]

3. The readFromFile(String) method uses a method called parseQuestion(String) to parse a String to a TextQuestion object using String.split(). Complete the parseQuestion(String) method. In your answer make sure that the method does what the comments written above the heading say it will do. [7 marks]

4. You are given the heading of the writeToFile(String, List&lt;TextQuestion) method. Complete the method. In your answer make sure that the methoddoes what the comments written above the heading say it will do. [7 marks

<strong>Reading for Part A</strong>Note that in the list below, the ‘Subject guide’ refers to volume 2, and HFJ refers to Head First Java• Subject guide, Chapter 2, Sections 2.2, 2.11 and HFJ 275–78 (static utility classes)• Subject guide, Chapter 3, Sections 3.2, 3.3, 3.5, 3.6 and HFJ 319–26 and 329–33 (handling exceptions)• Subject guide, Chapter 5, Sections 5.3 and HFJ 447, 452–54 and 458–59 (files,parsing with String.split(), streams including BufferedReader and BufferedWriter)• Subject guide Chapter 6, sections 6.2, 6.3, 6.4 and HFJ 431–38 and 441–43(serialization)

<strong>Deliverable for Part A</strong>• An electronic copy of your revised class: TextQuestionUtils.javaPlease put your name and student number as a comment at the top of your Java file.

<strong>Part B</strong><strong>Testing the ClientGUI</strong>You should compile and run the ClientGUI.java file. To do this you will need to first compile and start the StudentServer.java. You can run both programs from the shell (cmd.exe), but you will need to open the shell twice, once to get the StudentServer started and another to run the ClientGUI. Note that the ClientGUI has been hard-coded to connect to a local host.

When you start the ClientGUI class you should see a simple GUI with a JButton, a scrollable JTextArea and a JTextField. When you click on the ‘Connect’ button, if you see the message ‘ERROR: Connection refused: connect’, and you have the StudentServer class running, it may be that you need to tell your firewall to allow java through it. If this is the case you will have to restart the StudentServer and the ClientGUI once you have adjusted your firewall. Whenever you disconnect from the ClientGUI you will have to restart the StudentServer from the shell (cmd.exe) as the server is single-threaded and dies once the client has disconnected.

What you should see when you run the ClientGUI is the following, on the JTextArea:

<em>Welcome to the Student Results Server. Available commands:</em><em>SHOW ALL show all student results</em><em>SORT EXAM sort student results by exam mark</em><em>SORT CWK sort student results by coursework mark</em><em>SORT GRADE sort student results by grade</em><em>SORT TOTAL sort student results by total (final) mark</em><em>GRADE &lt;grade show all students that achieved a grade of &lt;grade</em><em>SEARCH &lt;name show all students that have &lt;term in their name</em><em>SHOW HELP show this help</em>Enter each of the listed commands to test the ClientGUI. You will note that the Student class has five instance variables: name, exam, cwk, total and grade. The constructor takes three of the values of the instance variables from the user, and then calls methods to work out the value of the total and grade instance variables. The Student class implements the rule that a student passes a module if they have achieved a mark of at least 35 in the coursework and exam components, with a weighted average mark of both components (the total field) of 40 or more. Student objects therefore have five fields that can be searched for in a list of Student objects, and that a list of Student objects can be sorted by.

The ClientGUI has commands to sort the List of Student objects by EXAM (the int exam field), by CWK (the int cwk field), by GRADE (the String grade field) and by TOTAL (the int total field).You will notice that two of the SORT commands do not work. Consider theStudentServerEngine class. It has a sort(String) method (see below), where twostatements have been commented out because the methods that they call in turn rely on Comparator classes that have not been written yet.

<em>private String sort(String sortBy) {</em><em>switch (sortBy.toLowerCase()) {</em><em>case “cwk”: return sortByCoursework();</em><em>case “total”: return sortByTotal();</em><em>//case “exam”: return sortByExam();</em><em>//case “grade”: return sortByGrade();</em><em>default: return “I don’t know how to sort by that!”;</em><em>}</em><em>}</em>

Please complete the following tasks:<em></em>1. The Student class has a basic toString() method. Write an improved <em>toString() using String.format() to set out the fields of the class in a readable way. [5 marks]</em>

2. Write the ExamComparator class. Once you have written the class, remove the comment marks (“//”) from the appropriate statement in the sort(String) method of the StudentServerEngine class and run the ClientGUI to test your new Comparator. [7 marks]<em>3</em>. Write the GradeComparator class. Once you have written the class, remove the comment marks (“//”) from the appropriate statement in the sort(String) method of the StudentServerEngine class and run the ClientGUI to test your new Comparator. [8 marks]

<strong>Reading for Part B</strong><em>• </em>Head First Java pp.294–97 for more about String.format()• <a href="https://docs.oracle.com/javase/7/docs/api/java/lang/String.ht" target="_blank" rel="nofollow noopener">http://docs.oracle.com/javase/7/docs/api/java/lang/String.ht</a><em>ml (scroll down or</em>search to find a description of the String.format() method).<em>• </em>Chapter 7 of Volume 2 of the CO2220 subject guide, pp.63–66 (clients andservers).<em>• </em>Head First Java pp. 473–85 (clients and servers)<em>• You are expected to do some research to help you complete Questions 2–4 butsee:</em><a href="https://stackoverflow.com/questions/7117044/how-to-use-java-comparator-properly" target="_blank" rel="nofollow noopener">http://stackoverflow.com/questions/7117044/how-to-use-java-comparator-properly</a><em><a href="https://docs.oracle.com/javase/7/docs/api/java/util/Comparator.html" target="_blank" rel="nofollow noopener">https://docs.oracle.com/javase/7/docs/api/java/util/Comparator.html</a></em>

<strong>Deliverables for Part B</strong><em></em>Please submit an electronic copy of the following:<em>• </em>Student.java (with revised toString() method)• ExamComparator.java• GradeComparator.java<em></em>Please put your name and student number as a comment at the top of your Java files.