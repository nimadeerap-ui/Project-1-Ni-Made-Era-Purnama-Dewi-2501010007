1. Karakteristik Memori dan Akses Data
• Array O(1): Menggunakan alamat memori yang kontinu (berurutan). Karena ukurannya tetap, komputer dapat menghitung lokasi pasti elemen ke-i secara langsung menggunakan rumus: Alamat_Awal + (indeks * ukuran_data).
• Singly Linked List O(n): Menggunakan memori non-kontinu. Elemen tersebar di berbagai lokasi, sehingga untuk menemukan elemen tertentu, sistem harus menelusuri satu per satu dari head (kepala) melalui pointer hingga mencapai tujuan.

2. Analisis Efisiensi Operasi Manipulasi
Linked List lebih unggul saat sering melakukan penyisipan (insertion) atau penghapusan (deletion) data di awal atau di tengah daftar.
Alasan Teoritis: Pada Array, menyisipkan data menuntut pergeseran (shifting) semua elemen setelahnya, yang memakan waktu O(n). Pada Linked List, Anda hanya perlu mengubah referensi pointer pada node terkait (O(1)) tanpa memindahkan elemen lainnya.

3. Konsep Doubly Linked List
• Anatomi Node: Terdiri dari tiga bagian: Data, pointer Next (menunjuk ke node depan), dan pointer Prev (menunjuk ke node belakang).
• Dampak Memori: Penggunaan memori lebih besar dibandingkan Singly Linked List karena setiap node harus menyimpan satu pointer tambahan (prev).
• Fleksibilitas: Memungkinkan penelusuran dua arah (maju dan mundur), memudahkan operasi seperti menghapus node tertentu tanpa harus mencari pendahulunya dari awal.

4. Mekanisme Circular Linked List
• Perbedaan Teoritis: Pada Linked List biasa, pointer terakhir bernilai null. Pada Circular Linked List, pointer terakhir menunjuk kembali ke head, membentuk lingkaran tanpa ujung.
• Contoh Skenario: Penjadwalan CPU (Round Robin Scheduling) di mana sistem operasi menggilir jatah waktu antar proses secara terus-menerus dalam siklus.

5. Array Dinamis di Python
Saat Python list mencapai kapasitas maksimalnya selama operasi append, mekanisme berikut terjadi:
• Alokasi Baru: Python mengalokasikan blok memori baru yang lebih besar (biasanya sekitar 1.125 x hingga 2x ukuran lama).
• Penyalinan (Copying): Semua elemen dari array lama disalin ke array baru.
• Penghapusan: Array lama dihancurkan untuk membebaskan memori.
• Penyisipan: Elemen baru ditambahkan ke ruang kosong di array baru tersebut.