![image1](/img/image.png)
Output dihasilkan seperti di atas karena program melakukan println terlebih dahulu pada "hey hey" lalu melakukan drop spawner dan menjalankan executor untuk mengerjakan tasknya, sehingga async task selalu berjalan setelah println "hey hey".

# Adding multiple spawner
![image3](/img/image3.png)
Menambahkan multiple spawner akan membuat executor menjalankan 3 asynchronous tasks secara bersamaan, menghasilkan sebuah output yang tidak dapat diprediksi karena sifatnya yang concurrent.

# Removing drop spawner
![image2](/img/image2.png)
Menghilangkan drop spawner membuat executor terus menunggu task berikutnya dari spawner, sehingga program terus berjalan karena queue yang dibuat oleh spawner tidak ditutup.