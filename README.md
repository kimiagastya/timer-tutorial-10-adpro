# Reflection
## Result of Execution<br>
![Result of Execution](img/Result_of_Execution.png)
<br>
Dalam kode ini, "hey hey" di-print sebelum "howdy!" dan "done!" karena fungsi `main` menjalankan perintah print "hey hey" terlebih dahulu yang dilanjutkan dengan menjalankan dua perintah print yang ada pada queue di executor.
<br>
## Multiple Spawn<br>
![Multiple Spawn](img/Multiple_Spawn.png)
## Removing Statement: `drop(spawner);`<br>
![Removing Statement](img/Removing_drop_spawner.png)
## Putting it in again<br>
![Put Again](img/Put_again.png)
<br>
Saat menjalankan multiple spawn, seluruh task yang di-spawn akan dijalankan bersamaan. Dalam kode, terdapat timer yang menunggu 2 detik sebelum dicetaknya semua string "done". Maka dari itu, program akan mencetak semua string "howdy" terlebih dahulu lalu kemudian dilanjutkan dengan mencetak seluruh string "done". <br>
Saat statement `drop(spawner)` dihapus, program akan bekerja seperti biasanya, tetapi program tidak akan selesai karena `drop(spawner)` bertujuan untuk memberi tahu program bahwa tidak akan ada lagi tugas yang ditambahkan kepada executor. Maka, ketika `drop(spawner)` dihapus, program akan tetap menunggu datangnya tugas baru.