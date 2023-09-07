## Java

* [Download Code](https://github.com/werlen-nevio/Snippets/blob/main/Java/Java.code-snippets)

### Hello World
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### Scanner
```java
import java.util.Scanner;

Scanner ScannerName = new Scanner(System.in);
System.out.println('Question');

String VarName = ScannerName.nextLine();
System.out.println(VarName);
```

### Variables
```java
String name = "John";
int age = 30;
```

### Conditional Statements
```java
if (age >= 18) {
    System.out.println("You are an adult.");
} else {
    System.out.println("You are a minor.");
}
```

### For loop
```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}
```

### While loop
```java
int count = 0;
while (count < 10) {
    System.out.println(count);
    count++;
}
```

### Arrays
```java
int[] myArray = {1, 2, 3, 4, 5};
```

### Array access
```java
int firstElement = myArray[0];
```

### Methods
```java
public static int add(int a, int b) {
    return a + b;
}
```

### File reading
```java
import java.nio.file.*;
String content = Files.readString(Paths.get("file.txt"));
```

### File writing
```java
import java.nio.file.*;
Files.write(Paths.get("output.txt"), "Hello, World!".getBytes());
```

### Exeption Handling
```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Error: Division by zero");
}
```

### Classes and Objects
```java
public class Person {
    String name;
    int age;
}
```

### Object creation
```java
Person person = new Person();
person.name = "Alice";
person.age = 25;
```

### Object methods
```java
public void greet() {
    System.out.println("Hello, my name is " + name);
}
```

### Sorting arrays
```java
import java.util.Arrays;
int[] sortedNumbers = Arrays.copyOf(numbers, numbers.length);
Arrays.sort(sortedNumbers);
```

### List reversal
```java
Collections.reverse(numbersList);
```

### List Length
```java
int listSize = numbersList.size();
```

### List removal
```java
numbersList.remove(3);
```

### List Appending
```java
numbersList.add(6);
```

### List copying
```java
ArrayList<Integer> copiedList = new ArrayList<>(numbersList);
```

### List clearing
```java
numbersList.clear();
```

### String Splitting
```java
String[] words = text.split(", ");
```

### String Formatting
```java
String formattedText = String.format("My name is %s and I am %d years old.", name, age);
```

### Math Operations
```java
int absoluteValue = Math.abs(-5);
```

### Random number generation
```java
import java.util.Random;
Random random = new Random();
int randomNumber = random.nextInt(100);
```

### Date and Time
```java
import java.time.LocalDateTime;
LocalDateTime currentTime = LocalDateTime.now();
```

### HashMap
```java
import java.util.HashMap;
HashMap<String, Integer> scoreMap = new HashMap<>();
```

### Working with Date and Time
```java
import java.time.LocalDate;
LocalDate today = LocalDate.now();
```

### Database connection with JDBC
```java
import java.sql.*;
String url = "jdbc:mysql://localhost:3306/mydb";
String user = "username";
String password = "password";
try (Connection connection = DriverManager.getConnection(url, user, password);
     Statement statement = connection.createStatement()) {
    ResultSet resultSet = statement.executeQuery("SELECT * FROM users");
    while (resultSet.next()) {
        String name = resultSet.getString("name");
        int age = resultSet.getInt("age");
    }
}
```

### Sending email with JavaMail API
```java
import javax.mail.*;
import javax.mail.internet.*;
Properties properties = new Properties();
properties.put("mail.smtp.host", "smtp.example.com");
Session session = Session.getInstance(properties);
MimeMessage message = new MimeMessage(session);
message.setFrom(new InternetAddress("sender@example.com"));
message.addRecipient(Message.RecipientType.TO, new InternetAddress("recipient@example.com"));
message.setSubject("Test Email");
message.setText("This is a test email.");
Transport.send(message);
```

### Working with JSON 
```java
import com.google.gson.*;
JsonObject jsonObject = new JsonObject();
jsonObject.addProperty("name", "Alice");
jsonObject.addProperty("age", 25);
String jsonString = jsonObject.toString();
```

### Handling Date and Time Zones
```java
import java.time.ZoneId;
ZoneId zoneId = ZoneId.of("America/New_York");
```
