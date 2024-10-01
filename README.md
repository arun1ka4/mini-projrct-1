#Mini Project 1



![minpro drawio](https://github.com/user-attachments/assets/e27a4f58-3cc1-4039-9fa4-bbe7dd9f2bfa)



print("======================================================================")
print("Program Menghitung Gaji Karyawan Berdasarkan Jam Kerja dan Tarif Kerja")
print("NIM Ganjil")
print("======================================================================")
print("  ")

#Registrasi akun
def nama_saya(): #untuk mendefinisikan nama_saya()
    while True: #Melakukan looping
        saya = "nayla lelyanggraheni hutomo"
        no_induk = "2409116061"

        #input nama dan nim (jangan salah)
        Nama = input("Nama Lengkap = ").lower()
        NIM = input("NIM = ")

        if Nama == saya and NIM == no_induk:
            print(" ")
            print(" ")
            print("Selamat Datang", Nama)
            print("NIM anda adalah ", NIM)
            break #menghentikan looping
        else:
            print("Nama atau NIM anda salah, silahkan coba lagi")


    hitung_gaji(Nama, NIM)


#Mengitung gaji Karyawan
def hitung_gaji(Nama, NIM):
    while True: 
        
        print(" ")
        gaji_pokok = int(input("Masukkan gaji anda (tanpa titik) = "))
        print(" ")
        print(" ")

#waktu karyawan bekerja
        print("Berapa lama anda bekerja? (dalam jam)")
        jam = int(input("Waktu bekerja = "))

#penghitungan gaji dan bonus untuk jam kerja lebih dari 160 jam
        print(" ")
        if jam > 160:
            bonus = gaji_pokok * 0.1 
            total_gaji = bonus + gaji_pokok
            print("Total gaji anda sebesar Rp", total_gaji)
            print("Anda mendapat bonus sebesar Rp", bonus)
            print(" ")
            break
#jika jam kerja kurang dari 160 jam
        elif jam > 0:
            print("Total gaji anda sebesar Rp", gaji_pokok)
            print("Kerja lebih baik lagi")
            break
        elif jam == 0:
            print("Malas banget jadi orang")
        else:
            print("kesalahan input gaji, silahkan coba lagi")
            hitung_gaji(Nama, NIM)
        print(" ")
        print(" ")  

    hitung_ulang(Nama, NIM)

#Pengulangan Menghitung Gaji 
def hitung_ulang(Nama, NIM):
    while True:

        print(" ")
        print(" ")
        ulang = input("Apakah anda ingin menghitung gaji? (ya/tidak) = "  ).lower()
        
        if ulang == "ya": #jika ingin melakukan pengulangan menghitung gaji
            hitung_gaji(Nama, NIM)
            break
        elif ulang == "tidak": #jika tidak ingin melakukan pengulangan
            break
        else:
            print("error, silahkan menjawab ya/tidak")


nama_saya()
