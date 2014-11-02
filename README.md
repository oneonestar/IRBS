# Intranet Room Booking System (IRBS)
PolyU COMP2011 Assignment 4 (Mini-Project)

##File structure
 - db/  database files, ant will copy the files to the destination during build
 - lib/ libraries used by the program
 - PartA/ the documentations required in part A
 - src/ the java source files
 - build.xml ant build file

##Build
This project is using Apache Ant for automating building. It contains different targets as folow:
 - clean: delete the existing build, docs and dist directory
 - compile: compile all java files into class files including testing files output to build/. It will also copy the database files in db/ into build/
 - compileDebug: do the same thing as compile except using -debug option for compilation
 - doc: generate the javadoc in doc/
 - jar: create a jar file in dist/ and copy the files from db/ to dist/
 - run: execute the file using the jar
 - test: run the JUnit test cases
 - all: jar + run

##Testing
The database files included some entries for testing purpose, you may login the system using the folloing accounts:
User: abc001 Password:cba001
User: abc002 Password:cba002
User: abc003 Password:cba003

#Additional information
The system do not support file saving function. Closing the program compeletely will discard all the booking records made during the process.
The password of the users are in SHA-256 hashed format.
