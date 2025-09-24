# Java-Campus-Course-and-Records-Manager-CCRM-
📘 Campus Course & Records Manager (CCRM)

A console-based Java SE application to manage students, courses, enrollments, grades, transcripts, and file operations for an academic institute.
This project demonstrates Java OOP principles, design patterns, exception handling, modern APIs (Streams, Date/Time, NIO.2) and more.

🚀 Features

Student Management: Add, update, list, deactivate students, view transcripts.

Course Management: Add, update, list, deactivate, search/filter by instructor, department, semester.

Enrollment & Grading: Enroll/unenroll students, record marks, compute GPA, generate transcripts.

File Utilities: Import/export CSV-like files, backup/exported data with timestamped folders, recursive file size utility.

CLI Workflow: Menu-driven, uses loops, decision constructs, enums, and polymorphism.

📂 Project Structure
CCRM/
│── src/
│   └── edu/ccrm/
│       ├── cli/        # Console interface (Main.java, Menu.java)
│       ├── config/     # AppConfig (Singleton), builders
│       ├── domain/     # Entities (Person, Student, Instructor, Course, Enrollment, enums)
│       ├── service/    # Services (StudentService, CourseService, EnrollmentService, TranscriptService)
│       ├── io/         # Import/Export, Backup utilities (NIO.2)
│       ├── util/       # Validators, comparators, recursion utilities
│       └── exception/  # Custom exceptions
│
├── screenshots/        # Add your screenshots (JDK setup, Eclipse, running program, exports)
├── test-data/          # Sample CSV import files
├── README.md           # Project overview & documentation
├── USAGE.md            # Example commands & workflows
└── requirements.md     # (Optional) Dependencies or runtime notes

🛠️ Setup & Run
Prerequisites

Java JDK 17+ (check with java -version)

VS Code / Eclipse IDE (Java Extension Pack recommended)

Run from VS Code

Open folder CCRM/ in VS Code.

Open src/edu/ccrm/cli/Main.java.

Click Run ▶️ or use Run → Start Debugging.

Run from Terminal
cd CCRM
javac -d out -sourcepath src src/edu/ccrm/cli/Main.java
java -cp out edu.ccrm.cli.Main


| Syllabus Topic     | Where Implemented                                      |
| ------------------ | ------------------------------------------------------ |
| Encapsulation      | `Student`, `Course` (private fields + getters/setters) |
| Inheritance        | `Person → Student/Instructor`                          |
| Abstraction        | `Person` as abstract class                             |
| Polymorphism       | `TranscriptService` interface with different impls     |
| Nested classes     | `Course.Builder`                                       |
| Interfaces         | `Persistable`, `Searchable<T>`                         |
| Enums              | `Semester`, `Grade`                                    |
| Lambdas & Streams  | Filtering/searching courses, GPA reports               |
| Recursion          | Backup size calculator                                 |
| Singleton          | `AppConfig`                                            |
| Exception handling | Custom exceptions (`DuplicateEnrollmentException`)     |
| Date/Time API      | Enrollment date, backup timestamps                     |
| NIO.2 File API     | Import/Export, Backup service                          |



📖 Java Concepts in README
🔹 Evolution of Java

1995: Java 1.0 released by Sun Microsystems

2004: Java 5 (Generics, Enums, Annotations)

2011: Java 7 (NIO.2, try-with-resources)

2014: Java 8 (Lambdas, Streams, Date/Time API)

2017: Java 9 (Modules, JShell)

2021+: Java 17 LTS, pattern matching, records, sealed classes

🔹 Java Editions
| Edition                  | Use Case                                              |
| ------------------------ | ----------------------------------------------------- |
| **Java ME**              | Mobile devices, embedded systems                      |
| **Java SE**              | Standard Edition, core APIs, desktop apps (used here) |
| **Java EE (Jakarta EE)** | Enterprise apps, web servers, large-scale apps        |

🔹 JDK, JRE, JVM

JDK (Java Development Kit) → Tools + compiler + JRE.

JRE (Java Runtime Environment) → JVM + core libraries.

JVM (Java Virtual Machine) → Executes bytecode, ensures portability.
Flow: .java → (javac) → .class bytecode → (JVM) → Machine code.

🖥️ Installation Guide
Install Java on Windows

Download JDK (17/21) from Oracle
.

Install and set environment variables:

JAVA_HOME = C:\Program Files\Java\jdk-17

Add %JAVA_HOME%\bin to PATH.

Verify:

java -version

Eclipse Setup

Install Eclipse IDE for Java Developers.

Create New Java Project → "CCRM".

Import src/ as source folder.

Run edu.ccrm.cli.Main.

📷 Screenshots to Include

java -version (JDK setup)

Eclipse project setup & run

Program running with menu options

Exported/Backup folder structure

🧪 Sample Usage

See USAGE.md
 for example CSVs, commands, and screenshots of workflow.

⚠️ Notes

Enable assertions when running:

java -ea -cp out edu.ccrm.cli.Main


Backup utility will create timestamped folders inside backup/.

Data import/export works with CSV-like files in test-data/.

🙏 Acknowledgements

Oracle Java Documentation

Effective Java (Joshua Bloch)

Java Tutorials by VIT faculty
