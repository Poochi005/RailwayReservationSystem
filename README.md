# Railway Reservation System

**Java Internship Project** – DLK Technologies (17 June 2026 – 17 July 2026)
**Intern:** Mahalakshmi T (Reg. No. 510423104303), B.E. CSE, Arunai Engineering College

## Abstract
A console-based Java application that lets passengers search trains, book and cancel tickets,
and check PNR status. Data (trains, bookings, PNR counter) is saved to disk, so it persists
between runs.

## Features
1. View all trains / search by source and destination
2. Book tickets (validation: age, seat limit 1–6, no past dates, seat availability)
3. Cancel tickets (seats are released, 80% refund)
4. PNR status check and list of all bookings
5. Data persistence using file handling

## Java concepts used (from the 30-day syllabus)
| Concept | Where |
|---|---|
| Classes, Encapsulation, Constructors | `model/Train`, `model/Booking` |
| Packages & access modifiers | `railway.model`, `.service`, `.util`, `.exception` |
| Exception handling (custom exception) | `ReservationException` |
| Collections & Generics | `LinkedHashMap`, `List`, `DataStore.load<T>` |
| File handling (serialization) | `util/DataStore` |
| Multithreading / synchronization | `synchronized book()` and `cancel()` |
| Control statements, Strings, I/O | `Main` menu with `switch` |

## Project structure
```
src/railway/Main.java
src/railway/model/{Train,Booking}.java
src/railway/service/ReservationService.java
src/railway/exception/ReservationException.java
src/railway/util/DataStore.java
```

## Run
Requires JDK 17+.
```
./build.sh
```
or
```
mkdir out && javac -d out $(find src -name "*.java") && java -cp out railway.Main
```

## Future enhancements
JDBC + MySQL storage (Day 19), Swing GUI (Day 20), Spring Boot REST API (Day 25).
