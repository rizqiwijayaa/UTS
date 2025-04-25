# UTS

### Import Library
```java
import java.util.ArrayList;
import java.util.Scanner;
```
- `ArrayList`: Digunakan untuk menyimpan daftar antrean pasien secara dinamis.
- `Scanner`: Digunakan untuk membaca input dari pengguna lewat konsol.

---

### Deklarasi Kelas
```java
public class HospitalQueueSystemQuestion {
```
- Kelas utama yang menjalankan keseluruhan program.

---

### Variabel Global
```java
private static ArrayList<Patient> patientQueue = new ArrayList<>();
private static Scanner scanner = new Scanner(System.in);
```
- `patientQueue`: Menyimpan antrean pasien berdasarkan prioritas.
- `scanner`: Untuk membaca input dari pengguna.

---

### Fungsi Main (Program Utama)
```java
public static void main(String[] args) {
```
- Titik masuk utama program.

```java
boolean running = true;
System.out.println("Welcome to the Hospital Queue Management System");
```
- Menampilkan pesan awal dan membuat flag agar program terus berjalan.

```java
while (running) {
    displayMenu();
    int choice = getValidIntInput("Enter your choice: ");
```
- Perulangan utama program: menampilkan menu dan membaca pilihan pengguna.

```java
switch (choice) {
    case 1: addPatient(); break;
    case 2: serveNextPatient(); break;
    case 3: displayQueue(); break;
    case 4: updatePriority(); break;
    case 5: searchPatient(); break;
    case 6:
        System.out.println("Thank you for using the system. Goodbye!");
        running = false;
        break;
    default:
        System.out.println("Invalid choice. Please try again.");
}
```
- Mengeksekusi fungsi sesuai pilihan pengguna.

```java
scanner.close();
```
- Menutup objek scanner saat program selesai.

---

### Menampilkan Menu
```java
private static void displayMenu() {
```
- Menampilkan daftar pilihan (menu) ke layar.

---

### Menambah Pasien Baru
```java
private static void addPatient() {
```
- Menerima input data pasien dari pengguna.

```java
Patient newPatient = new Patient(name, age, condition, priority);
```
- Membuat objek pasien baru.

```java
int insertIndex = 0;
while (...) {
    insertIndex++;
}
patientQueue.add(insertIndex, newPatient);
```
- Menentukan posisi pasien dalam antrean berdasarkan prioritas dan menyisipkannya.

---

### Melayani Pasien Berikutnya
```java
private static void serveNextPatient() {
```
- Mengambil dan menampilkan pasien pertama dalam antrean.

---

### Menampilkan Seluruh Antrean
```java
private static void displayQueue() {
```
- Menampilkan seluruh pasien yang ada di antrean saat ini.

---

### Memperbarui Prioritas Pasien
```java
private static void updatePriority() {
```
- Mencari pasien berdasarkan nama, lalu memperbarui prioritasnya dan menempatkan kembali di antrean.

---

### Mencari Pasien
```java
private static void searchPatient() {
```
- Mencari pasien dalam antrean berdasarkan nama, lalu menampilkan data pasien tersebut.

---

### Konversi Angka Prioritas ke Teks
```java
private static String getPriorityText(int priority) {
```
- Mengubah nilai prioritas (angka) menjadi teks yang lebih mudah dibaca.

---

### Validasi Input
```java
private static int getValidIntInput(String prompt)
private static int getValidIntInRange(String prompt, int min, int max)
private static String getValidStringInput(String prompt)
```
- Fungsi bantuan untuk memastikan input pengguna valid:
  - `getValidIntInput`: membaca input bilangan bulat.
  - `getValidIntInRange`: membaca angka dalam rentang tertentu.
  - `getValidStringInput`: membaca string yang tidak kosong.

---

## Kelas `Patient`
```java
class Patient {
    private String name;
    private int age;
    private String condition;
    private int priority;
```
- Menyimpan data masing-masing pasien.

```java
public Patient(...) {...}
```
- Konstruktor untuk membuat objek pasien.

```java
public String getName() { ... }
public int getAge() { ... }
public String getCondition() { ... }
public int getPriority() { ... }
public void setPriority(int priority) { ... }
```
- Getter dan setter untuk mengakses dan mengubah data pasien.

---
