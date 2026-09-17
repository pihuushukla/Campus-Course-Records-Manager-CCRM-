## Pihu Shukla(24BCY10148)

# Campus Course & Records Manager (CCRM)

It is basically a simple Java console application I made to manage students, courses, and enrollments. The project has a modular structure: one package for the CLI, one for domain models, one for services, one for utilities, while users of the system can add students/courses, list students/courses, perform student enrollment in courses, view enrollments, and do file backup. Its implementation relies on object-oriented principles, following a layered architecture; hence, the code will be clean and well-organized and easy to extend, for example, by integrating databases using JDBC.

# Project Structure

```
CCRM-Java-Project
 ├─ edu/
 │   └─ ccrm/
 │       ├─ cli/
 │       │   └─ MainMenu.java
 │       ├─ config/
 │       │   └─ AppConfig.java
 │       ├─ domain/
 │       │   ├─ Course.java
 │       │   ├─ CourseCode.java
 │       │   ├─ Enrollment.java
 │       │   ├─ Grade.java
 │       │   ├─ Instructor.java
 │       │   ├─ Person.java
 │       │   ├─ Semester.java
 │       │   └─ Student.java
 │       ├─ service/
 |       |       ├─ StudentService.java
 │       |       ├─ CourseService.java
 │       |       └─ EnrollmentService.java
 │       └─ util/
 │           └─ FileUtil.java
 ├─ screenshots/
 └─ README.md  
 
 ```

# setup & Running

# Requirements
- JDK 17 (or higher version)
- VS Code (with Java Extension Pack) / Eclipse ide
  
<img width="1596" height="650" alt="downloading java" src="https://github.com/user-attachments/assets/89fc05dc-ec24-4e25-8343-55b6c4619bb6" />

# Steps to run
1. open the folder `JavaVITyarthiProject` in VS Code.  
2. Navigate to the file: 
        edu.ccrm/cli/MainMenu.java
3. Run the program. The menu-driven CLI will appear in the terminal.

# Java editions
| Edition               |    Use Case |

| Java SE               | Standard Edition (desktop/console apps)  |
| Java EE (Jakarta EE)  | Enterprise Edition (web apps, servers)   |
| Java ME               | Micro Edition (mobile, embeded devices) |

# JDK, JRE, jvm
- JVM: Java Virtual Machine –   executes `.class` bytecode  
- JRE: Java Runtime Environment –   JVM + libraries (for running programs)  
- JDK: Java Development Kit –   JRE + compiler + tools (for developement)  

# Installation (windows Example)
1. Download JDK from [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. Install and set `JAVA_HOME` enviornment variable.  
3. Verify installation:
        java -version
        javac -version

<img width="962" height="340" alt="java version" src="https://github.com/user-attachments/assets/ad638c89-1763-4680-b41b-13e3987cffe2" />

 # Mapping of syllabus Topics → Code
 

```
| Topic           |  Where used |

| Encapsulation   | `Student.java` (private fields + getters/setters) |

| Inheritance     | `Person → Student, Instructor` |

| Abstraction     | `Person.java` (abstract class with abstract method) |

| Polymorphism    | `printProfile()` overrided in Student/Instructor |

| Immutable class | `CourseCode.java` |

| Nested class    | `Course.Builder` (static nested class) |

| Enum            | `Grade.java`, `Semester.java` |

| Lambda & Stream | `courses.forEach(System.out::println)` in `MainMenu.java`   |

| singleton       | `AppConfig.java` |

| Builder pattern | `Course.Builder` |

| Exceptions      | `tryBackup()` in `MainMenu.java` |

| Custom exception | (to be added later, e.g., `MaxCreditLimitException`) |

| File I/O (NIO.2) | `FileUtil.java` |

| recursion       | `folderSize()` in `FileUtil.java` |

| Date/Time api   | `admissionDate` in `Student.java` |

| Assertions      | `assert credits > 0 : "Credits must be positive";|
```
        
# Eclipse setup 
1. File → New → Java project  
2. Name project: `CCRM-Java-Project`  
3. copy source files into `edu/ccrm/...`  
4. Run `MainMenu.java`  

<img width="1091" height="544" alt="Eclipse setup" src="https://github.com/user-attachments/assets/9fcde42a-8ada-43e5-8eca-51d1d988a09a" />
<img width="638" height="679" alt="eclipse install" src="https://github.com/user-attachments/assets/b3600da8-d4b1-4d50-a061-5c6f06a9da54" />


# Assertions
In code:
```java
assert credits > 0 : "Credits must be positive";

Run with assertions enabled:
        java -ea edu.ccrm.cli.MainMenu

             or 
# Compile all java files with package structure
        javac -d . $(find edu -name "*.java")

# Run the main program
        java edu.ccrm.cli.MainMenu
