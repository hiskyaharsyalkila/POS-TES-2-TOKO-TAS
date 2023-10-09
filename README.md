# POS-TES-2-TOKO-TAS
HISKYA HARSYAL KILA 2309116089


```

#login
def login():
    print("---------------silakan login---------------")
    username= input("Username : ")
    password = input("Password : ")
    

    if username == "hiskya" and password == "12345":
        print("Mantap Saudara")
    else:
      print("Masukkan dengan benar Saudara")
       
if __name__ == "__main__":
    login()

#list toko tas kila
from prettytable import PrettyTable

list_tas = [
    ["1", "Ransel", 169000],
    ["2", "Tote Bag", 105000],
    ["3", "Weekend", 599000],
    ["4", "Sling Bag", 157000],
    ["5", "Duffle Bag", 189000],
    ["6", "Rusksack", 310000],
    ["7", "Wait Bag", 117000],
]

#menu pembeli
def transaksi():
    while True:
      #tampilan
       print("jenis tas yang ada")
       tampilkan_tas()

       #masukkan no tas dan jumlah dibeli
       print("------selamat datang ditoko tas kila------")
       nomor_tas = input("masukkan nomor tas yang mau di beli: ")
       sky = int(input("jumlah tas hanya bisa dibeli 1 kali: "))

       #mencek stok tas
       for Tas in list_tas:
        if Tas[0] == nomor_tas:
            if sky > 1:
               print("jumlah maksimun harus 1 tas saja")
               break
        else:
         #tampilan keseluruhan harga
         for i in range(len(list_tas)):
            if list_tas[i][0] == nomor_tas:
               total_harga = list_tas[i][2] * sky
               print("total harga: Rp", total_harga)
               print("terimakasih sudah berkunjung, silahkan datang kembali")
               return
        #tampilan kembali jika tas salah masuk
        print()

#menu penjual
def create():
   #membuat daftar tas yang baru
   nomor_tas = input("pilih nomor tas: ") 
   nama_tas = input("masukkan nama tas: ")
   harga_tas = int(input("masukkan harga tas: ")) 
   list_tas.append([nomor_tas, nama_tas, harga_tas])
   tampilkan_tas()

def read():
   #membaca tampilan tas yang ada
   tampilkan_tas()

def update():
   #memperbarui daftar tas
    nomor_tas = input("masukkan nomor tas yamg mau di perbarui: ")
    for i in range(len(list_tas)):
        if list_tas[i][0] == nomor_tas:
         nama_tas = input("masukkan nama tas baru: ")
         harga_tas = int(input("masukkan harga tas baru: "))

         #melakukan perbaruan
         list_tas[i][1] = nama_tas
         list_tas[i][2] = harga_tas

         #tampilan terbaru
         tampilkan_tas()
         break
    else:
        print("tas tidak ditemukan")

def delete():
   #menghapus daftar tas yang ada
    nomor_tas = input("masukkan nomor tas yang mau dihapuskan: ")
    for i in range(len(list_tas)):
        if list_tas[i][0] == nomor_tas:
         list_tas.pop(i)
         #tampilan terbaru
         tampilkan_tas()
         break
    else:
       print("tas tidak diketahui")

#tampilan prettytable
def tampilkan_tas():
    table = PrettyTable()
    table.field_names = ["No", "Nama Tas", "Harga Tas"]
    for tas in list_tas:
        table.add_row(tas)
        print(table)

#tampilan pilih role
while True:
    print("-----------------pilih role----------------")
    print("1. penjual", "\n2. pembeli", "\n3. keluar")

    pilih = input("pilih no: ")

    if pilih == "1":
        print("-----------penjual toko tas kila-----------")
        print("1. tambah tas: ", "\n2. lihat tas", "\n3. perbarui tas", "\n4. hapus tas", "\n5. kembali")

        pilihan_penjual = input("pilih no: ")
        if pilihan_penjual == "1":
            create()
        elif pilihan_penjual == "2":
            read()
        elif pilihan_penjual == "3":
            update()
        elif pilihan_penjual == "4":
            delete()
        elif pilihan_penjual == "5":
            continue
        else:
           print("masukkan dengan benar")

    elif pilih == "2":
        print("pembeli")
        transaksi()  
    elif pilih == "3":
        print("akhir dari program")
        break
    else:
        print("masukkan dengan benar")

```

<img width="203" alt="1" src="https://github.com/hiskyaharsyalkila/POS-TES-2-TOKO-TAS/assets/144862428/677b6a99-a02e-4634-8544-40db6bf8e9cc">

<img width="164" alt="2" src="https://github.com/hiskyaharsyalkila/POS-TES-2-TOKO-TAS/assets/144862428/74ecdb49-5c71-4eb4-83c0-401ac67cbd47">

<img width="259" alt="3" src="https://github.com/hiskyaharsyalkila/POS-TES-2-TOKO-TAS/assets/144862428/690cee69-b116-4c6f-a516-ecb0d0913a1e">

```






