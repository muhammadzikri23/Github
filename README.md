 \\ PENJELASAN KODE \\

```java
import java.util.ArrayList ; // mengimpor ArrayList dari java untuk menyimpan daftar pesanan
 import java.util.Scanner; = \//mengimpor Scanner untuk membaca input dari  pengguna 
public class KafeMenu // untuk menyatakan kelas Kafe menu
public static void main(String[] args) // metode ( main) yang akan di eksekusi sat program  di jalankan
Scanner user = new Scanner(System.in); // untuk membuat objek Scanner untuk menerima input 
String[] menuNama //   menampilkan Array yang berisi daftar nam menu di Kafe
int[] menuHarga //  menampilkan Array yang berisi harga setiap menu 
ArrayList<String> pesananNama = new ArrayList<>(); // menyimpan nama menu yang di pesan
ArrayList<Integer> pesananJumlah = new ArrayList<>(); // menyimpan jumlah pesanan
ArrayList<Integer> pesananHarga = new ArrayList<>(); // menyimpan harga pesanan
boolean isRunning // true = menentukan program tetap berjalan atau tidak
for (int i = 0; i < menuNama.length; i++) // menampilkan Looping untuk mencetak menu beserta harganya
while (isRunning)  // Menampilkan Looping utama program selama isRuning bernilai true
System.out.println("Pilih opsi berikut:"); 
System.out.println("1. Tambah Pesanan"); // menampilkan opsi unutk menambhakan pesanan
System.out.println("2. Lihat Daftar Pesanan"); // menampilkan daftar pesanan yang telah di buat
System.out.println("3. Hitung Total Biaya"); // menampilkan total biaya pesanan
System.out.println("4. Selesai"); // memberikan opsi u ntuk keluar dari program
System.out.print("Masukkan pilihan Anda: "); // meminta input dari pengguna
int pilihan = user.nextInt(); // membaca input angka 
user.nextLine(); // membersihkan input agar tidak bermasalah saat membaca string selanjutnya
if (pilihan == 1)  // memilih opsi pertama
System.out.print("Masukkan nomor menu yang ingin dipesan: ");// meminta pengguna memasukkan nomor menu yang ingin dipesan
int nomorMenu = user.nextInt(); // membaca nomor menu yang dimasukkan pengguna
if (nomorMenu < 1 || nomorMenu > menuNama.length) // memeriksa apakah nomor menu yang dimasukkan valid           
System.out.println("Nomor menu tidak valid.");// Jika nomor tidak valid, tampilkan pesan kesalahan
continue; // kembali ke awal loop unutk meminta input lagi
int jumlah = user.nextInt();// membaca jumlah pesanan dari pengguna
if (jumlah <= 0) // memeriksa apakah jumlah pesanan valid
System.out.println("Jumlah pesanan harus lebih dari 0."); // jika jumlah tidak valid ,tampilkan pesanan kesalahan
continue; // kembali ke awal loop
pesananNama.add(menuNama[nomorMenu - 1]);// menambahkan nama menu ke dalam daftar pesanan
pesananJumlah.add(jumlah);//menambahkan jumlah pesanan ke daftar
pesananHarga.add(menuHarga[nomorMenu - 1]);// menambahkan harga menu yang di pesan ke daftar
 System.out.println(""); // menampilkan pesan bahwa pesanan berhasil di tambahkan
 else if (pilihan == 2) // mengecek apakah pengguna memilih opsi"Lihat daftar Pesanan "
 System.out.println("\n=== Daftar Pesanan ===");// menampilkan judul daftar pesanan
 if (pesananNama.isEmpty()) // mengecek apakah belum ada pesanan yang ditambahkan
 System.out.println("Belum ada pesanan.");// Jika daftar pesanan kosong , tampilkan pesanan 
 for (int i = 0; i < pesananNama.size(); i++) // Loop untuk menampilkan setiap pesanan yang ada dalam daftar
 System.out.println((i + 1) + ". " + pesananNama.get(i) + " x" + pesananJumlah.get(i));// menampilkan nomor, nama menu, dan jumlah pesanan
 else if (pilihan == 3) // mengecek apakah pengguna memilih opsi "Hitung Total Biaya"
 int total = 0; // Inisialisasi variabel total untuk menyimpan total harga pesanan
 for (int i = 0; i < pesananNama.size(); i++) //Loop untuk menghitung total harga pesanan
 total += pesananJumlah.get(i) * pesananHarga.get(i);// menjumlahkan harga dari setiap pesanan
System.out.println("\n=== Total Biaya ===");//menampilkan judul untuk total biaya
ystem.out.println("Total yang harus dibayar: Rp" + total);// menampilkan total biaya yang harus di bayar
else if (pilihan == 4) // mengecek apakah pengguna memilih opso "keluar"
System.out.println("Terima kasih telah berkunjung ke kafe kami!")// menampilkan pesan perpisahan
isRunning = false;// mengubah isRunning menjadi false agar loop utama berhenti , sehingga program akan selesai.
            

                    
