## Belajar Exception pada python
### Dengan menggunakan block try except

1. Pertama kita buat sebuah folder bernama `13-exception` dan didalamnya kita buat file bernama `Praktikum.py` , `filedemo.txt` dan `filedemo2.txt`, untuk penamaan folder dan file itu sesuai kesukaan kalian.
      
      ![File](https://user-images.githubusercontent.com/115931631/209066021-1a5ac0fd-92db-4527-bc1a-0fa68c256a03.png) 
   
2. Sekarang mari kita buka file `Praktikum.py` lalu inputkan codingan sebagai berikut :
      
        try:
            # membuat variable_1
            variable_1 = "Ini variable 1"
            # menampilkan variable yang salah
            print(variable1)  # seharusnya variable_1
            # memberitahu kesalahn pemanggilan variable dengan exception
        except NameError as variable1:
            print(variable1)

   ! Kita melakukan penanganan kesalahan NameError
    lalu run dengan cara ketik `python Praktikum.py` di terminal

    Maka hasilnya sebagai berikut :
    
    ![yang k 1](https://user-images.githubusercontent.com/115931631/209065831-e6bfed1e-01aa-4e9e-a547-ff595d025745.png)
    
3. Masih difile yang sama yaitu `Praktikum.py` lalu inputkan codingan sebagai berikut :

          try:
              # membuat variable_1
              variable_1 = "Ini variable 1"
              # menampilkan variable yang salah
              print(variable1)  # seharusnya variable_1
              # memberitahu kesalahn pemanggilan variable dengan exception
          except NameError as variable1:
             print(variable1)

  ! Jangan lupa untuk mengcomment codingan sebelumnya atau kalian boleh hapus agar kita fokus di contoh kedua yaitu FileNotFoundError

   lalu run dengan cara ketik `python Praktikum.py` di terminal

   Maka hasilnya sebagai berikut :
    
   ![yang k 2](https://user-images.githubusercontent.com/115931631/209066389-9d139b7b-6931-4501-b487-086c7ba689bb.png)
   
4. Masih difile yang sama yaitu `Praktikum.py` lalu inputkan codingan sebagai berikut :
       
       try:
            # parameter x digunakan untuk membuat file
            f1 = open('filedemo2.txt', 'x')
            # menulis kata di filedemo2.tt
            f1.write("Halo semuanya ini filedemo2 yang baru dibuat")
            print(f1.read())
            # jika filedemo2.txt sudah ada maka dilempar ke exception dibawah ini
        except FileExistsError:
            raise FileExistsError("File dengan nama filedemo2 sudah ada.")
      
  ! Jangan lupa untuk mengcomment codingan sebelumnya atau kalian boleh hapus agar kita fokus di contoh kedua yaitu FileExistError

   lalu run dengan cara ketik `python Praktikum.py` di terminal

   Maka hasilnya sebagai berikut :
 
  ![yang k 3](https://user-images.githubusercontent.com/115931631/209066997-abeb6413-73e5-4e0c-af6b-db3ca6424094.png)

   disini error bahwa file tersebut sudah ada, seperti yang kita lihat filedemo2 sudah kita buat diawal. jadi kita tidak boleh membuat file dengan nama yang sama dalam satu folder
   
5. Masih difile yang sama yaitu `Praktikum.py` lalu inputkan codingan sebagai berikut :

        # menginput nim, fungsi input() selalu berupa string untuk type data
        nim = input ("Masukkan NIM")
        # jika nim bukan interger tipe datanya maka membangkitkan error 
        if not type(nim) is int:
            # menangani bahwa nim wajib integer
            raise TypeError('Mohon maaf ni yee sebelumnya ... nim kudu integer ')
        else:
            print(nim)
            
  ! Jangan lupa untuk mengcomment codingan sebelumnya atau kalian boleh hapus agar kita fokus di contoh keempat yaitu TypeError

   lalu run dengan cara ketik `python Praktikum.py` di terminal

   Maka hasilnya sebagai berikut :

   ![hasil nya](https://user-images.githubusercontent.com/115931631/209067587-8bfd065e-4214-4a8e-ae61-6420fe7ee5fb.png)

   Baik disini errornya berupa type yaitu bahwa nim itu harus integer, karena fungsi input selalu mengembalikan type data string, jika kalian tidak ingin eror kalian bisa convert nim trsebut ke integer dngn cara berikut => nim = int(input("Masukan NIM : "))

#### Baik Teman teman kurang lebih seperti itu dalam belajar exception pada python
#### di repository ini kita memang sengaja membuat kesalahan agar bisa mengetes exception dengan try except, Untuk kali ini kita hanya belajar beberapa saja dari exception.
#### Terima kasih
