Berikut adalah penjelasan lengkap tentang script:

1. **Class `Ticket`**: Ini adalah class yang mewakili tiket. Class ini memiliki beberapa atribut, yaitu `destination` (tujuan tiket), `price` (harga tiket), dan `isBooked` (status pemesanan tiket). Terdapat juga beberapa method, antara lain:
   - Constructor `Ticket(String destination, double price)`: Membuat objek tiket dengan tujuan dan harga yang ditentukan. Inisialisasi `isBooked` dengan `false`.
   - Method `getDestination()`: Mengembalikan tujuan tiket.
   - Method `getPrice()`: Mengembalikan harga tiket.
   - Method `isBooked()`: Mengembalikan status pemesanan tiket.
   - Method `bookTicket()`: Mengubah status pemesanan tiket menjadi terpesan (`true`).
   - Method `cancelBooking()`: Mengubah status pemesanan tiket menjadi tidak terpesan (`false`).
   - Method `toString()`: Method override untuk mencetak informasi tiket.

2. **Class `TicketingSystem`**: Ini adalah class yang mewakili sistem pemesanan tiket. Class ini memiliki atribut `tickets` (array tiket) dan beberapa method, antara lain:
   - Constructor `TicketingSystem(int capacity)`: Membuat objek sistem pemesanan tiket dengan kapasitas yang ditentukan.
   - Method `addTicket(Ticket ticket, int index)`: Menambahkan tiket ke dalam sistem pada indeks yang ditentukan.
   - Method `getTickets()`: Mengembalikan array tiket dalam sistem.
   - Method `bookTicket(int index)`: Memesan tiket pada indeks yang ditentukan. Jika tiket belum terpesan, mengubah status pemesanan tiket menjadi terpesan dan mengembalikan tiket tersebut. Jika tiket sudah terpesan, mengembalikan `null`.
   - Method `cancelBooking(int index)`: Membatalkan pemesanan tiket pada indeks yang ditentukan.

3. **Class `FlightTicket`**: Ini adalah subclass dari `Ticket` yang mewakili tiket pesawat. Class ini memiliki tambahan atribut `airline` (maskapai) dan method `toString()` yang telah di-override untuk mencetak informasi tiket pesawat.

4. **Class `Main`**: Ini adalah class utama yang berisi method `main` sebagai entry point program. Di dalam method `main`, langkah-langkah berikut dilakukan:
   - Membuat objek tiket menggunakan constructor `Ticket` dan `FlightTicket`.
   - Membuat objek sistem pemesanan tiket menggunakan constructor `TicketingSystem`.
   - Menambahkan tiket ke dalam sistem menggunakan method `addTicket`.
   - Mencetak semua tiket dalam sistem menggunakan for-each loop dan anonymous class untuk mencetak informasi tiket.
   - Memesan tiket menggunakan method `bookTicket` dan menangani kasus jika tiket sudah terpesan.
   - Membatalkan pemesanan tiket menggunakan method `cancelBooking`.
   - Mencetak semua tiket dalam sistem setelah perubahan.
   - Menggunakan try-catch untuk menangani exception `ArrayIndexOutOfBoundsException` ketika mencoba membatalkan pemesanan tiket dengan indeks yang tidak valid.
   - Menggunakan custom annotation `@Deprecated` pada variabel `ticketPrice`.


Nama :Kembang Prima Rossari
NIM : V3922025
Kelas : TI-D
