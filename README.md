# Advprog Module 10 Tutorial Part 1 - Timer
Hadyan Fachri\
2306245030\
Advprog A

## Reflection
**Add such a sentence (you need to modify the text) right after the spawner.spawn (...);  
Take a look at what happened. Capture the result of your execution. 
Put it in your Readme.md, with some explanation why the result is as such.**

![alt text](image.png)
Setelah saya menambahkan pesan setelah spawner, terlihat bahwa pesan `Fachri's Computer: hey hey not bad :/` muncul terlebih dahulu. Ini karena pesan tersebut dieksekusi langsung di fungsi `main`, sebelum `executor.run()` dijalankan.

Future yang berisi `howdy!!!` dan `done!!!` hanya mulai dijalankan saat `executor.run()` dipanggil. `howdy!!!` dieksekusi lebih dulu saat task pertama kali diproses. Kemudian, karena ada `await Timer::new(...)`, task akan tertunda (Pending) selama **2 detik**. Setelah waktu habis, executor melanjutkan task tersebut dan mencetak `done!!!`.