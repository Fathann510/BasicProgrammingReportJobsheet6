# JOBSHEET 6 - SELECTION 2

**Student Identity:**
* **Name:** Fathan Nur Hidayat
* **NIM:** 26410702084
* **Class / Student Attendance:** 1I / 12

---

## 1: OBJECTIVE

The following are the objectives of the practical work in this chapter:

1. Students can solve problems and case studies using nested selection statements.
2. Students can apply nested selection statements in Java programs.
3. Students can apply the logical operators &&, ||, and ! in selection structures.

---

## 2: LABS & ACTIVITIES

### 2.1 Experiment 1: Nested IF to Check Thesis Exam Requirements.

In this section, students are required to apply a *Nested IF* condition to check thesis exam requirements.

#### 2.1.1 Program Code Java
```java

package Week6;
import java.util.Scanner;

public class NestedThesisExam12 {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
    
        String message;
        System.out.print("Has the student cleared all penalties? (Yes/No): ");
        String noPenalty = input.nextLine().trim();
        
        System.out.print("Enter the number of guidance sessions with Supervisor 1: ");
        int guidanceCount1 = input.nextInt();
        System.out.print("Enter the number of guidance sessions with Supervisor 2: ");
        int guidanceCount2 = input.nextInt();

        if(noPenalty.equalsIgnoreCase("Yes")) {
            if(guidanceCount1 >= 8 && guidanceCount2 >= 4) {
                message = "All requirements met. The student may register for the thesis exam";
            }else if (guidanceCount1 < 8 && guidanceCount2 < 4) {
                message = "Failed! Guidance sessions with Supervisor 1 are below 8 and Supervisor 2 are below 4";
            }else if (guidanceCount1 < 8) {
                message = "Failed! Guidance sessions with Supervisor 1 have not reached 8";
            }else {
                message = "Failed! Guidance sessions with Supervisor 2 have not reached 4";
            }
        }else {
            message = "Failed! The student still has an outstanding penalty";
        }
        System.out.println(message);
        input.close();
    }
}

```

#### 2.1.2 Execution Result / Screenshot Output
The following is an example of the *output* display after the program is run.:

![Experiment1Output](/Experiment1Output.png)

#### 2.1.3 Answers to Questions / Reflection Questions
* **Question 1:** What happens if the student answers "No" to the penalty-clearance question? Why?
  * **Answer:** The process will still proceed to the guidance session, even if you enter the guidance session numbers, the result will still lead to the 'else' section, because the guidance session conditions are only checked when the penalty answer is 'Yes'.
* **Question 2:** Explain the meaning of the following code snippet!
  if (guidanceCount1 >= 8 && guidanceCount2 >= 4) {
  * **Answer:** To check 2 conditions at the same time. If both requirements are met, the code inside the { } will be executed. Both conditions must be True.
* **Question 3:** Describe the full flow of checking the student's requirements from start to finish. Explain
step by step for every condition!
  * **Answer:** The first one, we must enter the penalties, after we enter 'Yes', we are directed to the next statement. We must input the number of guidance session with supervisor 1 & 2.
  * If the requirements of guidance session with supervisor 1 & 2 met, the output will display "All requirements met. The student may register for the thesis exam".
  * If the requirements of guidance sessions with Supervisor 1 are below 8 and Supervisor 2 are below 4, the output will display "Failed! Guidance sessions with Supervisor 1 are below 8 and Supervisor 2 are below 4"
  * If only the required number of guidance sessions with Supervisor 2 is met, but not with Supervisor 1, then the output will display "Failed! Guidance sessions with Supervisor 1 have not reached 8"
  * If only the required number of guidance sessions with Supervisor 1 is met, but not with Supervisor 2, then the output will display "Failed! Guidance sessions with Supervisor 2 have not reached 4"
  * Otherwise if the student hasn't cleared all the penalties, the output will display "Failed! The student still has an outstanding penalty" 
---

### 2.2 Experiment 2: Logical Operators to Determine Campus WiFi Access

Paragraf ini menjelaskan ringkasan Percobaan 2. Percobaan ini berfokus pada penggunaan `switch-case` untuk memilih menu atau opsi berdasarkan nilai yang bersifat spesifik.

#### 2.2.1 Program Code Java
```java

package Week6;
import java.util.Scanner;

public class LogicalOperatorWifi12 {
    public static void main(String[] args) {
     Scanner input = new Scanner(System.in);

     boolean isStudent;
     boolean isLecturer;
     boolean isBlocked;

     System.out.println("--- Wifi Access System ---");
     System.out.print("Is the user a student? (true/false): ");
     isStudent = input.nextBoolean();
     System.out.print("Is the user a lecturer? (true/false): ");
     isLecturer = input.nextBoolean();
     System.out.print("Is the account currently blocked? (true/false): ");
     isBlocked = input.nextBoolean();

     if ((isStudent || isLecturer) && !isBlocked) {
        System.out.println("Wifi Access Granted");
     } else {
        System.out.println("Wifi Access Denied");
     }
     input.close();
 }
}
```
#### 2.2.2 Execution Result / Screenshot Output
The following is an example of the *output* display after the program is run.:


---

## 3: TUGAS MANDIRI

Berikut adalah daftar tugas yang dikerjakan pada Jobsheet ini:

- [x] **Tugas 1:** Mengubah struktur `if-else` menjadi *Ternary Operator*.
- [x] **Tugas 2:** Membuat program berdasarkan *Flowchart* penentuan SKS.
- [ ] **Tugas 3:** Mengimplementasikan studi kasus parkir & antrean.

### 3.1 Implementasi Kode Tugas

```java
// Contoh Kode Program Tugas Mandiri
public class TugasMandiri {
    public static void main(String[] args) {
        int sks = 20;
        String status = (sks <= 24) ? "KRS Valid" : "Melebihi Batas";
        System.out.println(status);
    }
}
```

---

## 4: KESIMPULAN

Tuliskan paragraf kesimpulan di sini. Secara singkat, struktur pemilihan sangat penting digunakan untuk mengatur alur jalannya program (*flow control*) berdasarkan variabel atau pilihan yang ditentukan oleh pengguna.
