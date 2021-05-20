# Praktikum-GUI
modul 2

1. 
# Menggunakan Variable
angka = 10

# Param 1 : Maksimal
for i in range(angka) :
    print("Angka Ke : ")
    print(i)

# Param 2 : Minim, Maks
for i in range(angka, 20) :
    print("Angka Ke : ")
    print(i)

# Param 3 : Minim, Maks, Lompatan(decre,incre)
for i in range(angka, 1, -1) :
    print("Angka Ke : ")
    print(i)

#Array
array = [1,2,3,4]
for i in array :
    print(i, end = ' ') 
    
    2. IF
    x = False
y = True

#if..else
if x != True :
    print('print')
else:
    print('tidak print')

#if..else if..else
if x != False :
    print('print c')
elif y != False :
    print('print y')

#if(..and..)..else
if x != True and y == False :
    print('print')
else:
    print('tidak print') 
    
    
    3. TryExcept.py
    # Try..except
try :
    a = int(input('masukkan nilai a: '))
    b = int(input('masukkan nilai b: '))
    c = a / b
    print(f"{a} / {b} = {c}")

except ZeroDivisionError as e :
    print('Error : Tidak boleh bagi 0')

#Try..except..finnaly
f = ''

try :
    f = open('contoh.txt', 'r')
    lines = f.readlines()
    for line in lines :
        print(line, end='\n')
except IOError as e :
    print('ERROR: File Hilang')

finally:
   if f:
     f.close()
 4  Modul 2/While.py 
@@ -0,0 +1,4 @@
i = 1
while i < 10 :
    print(i, end =' ')
    i += 1
    
    
    4. function.py
    
    #Parameter untuk inheritance
class Titik(object) :
    #constructor
    def __init__(self, x = 0, y = 0):\
        # self adalah this
        self.x = x
        self.y = y

    def pindah(self, x, y):
        self.x = x
        self.y = y

    def cetak(self):
        print(f'{self.x},{self.y}')

#buat object
titik = Titik()
titik.cetak()
titik.pindah(5,10)
titik.cetak()

5. fungsi
#fungsi Global
def kali (a,b) :
    c = a * b
    return c
    z = kali(10,5)
    print(z)

#fungsi globals
def cetakBonus(daftar=[]) :
    #fungsi lokal
    def hitungBonus(gaji) :
        if gaji < 5000000 :
            bonus = 0.05 * gaji
        elif 5000000 <= gaji < 7500000 :
            bonus = 0.10 * gaji
        else :
            bonus = 0.15 * gaji
        return bonus
    for nama, gaji in daftar :
        b = hitungBonus(gaji)
        print(f'{nama}\t: {gaji}, {b} ')
data = [
    ('Ucok', 4000000),
    ('Budi', 6000000),
    ('Wagi', 8000000),
]
cetakBonus(data)
hitungBonus(data)

6
#fungsi lambda

maks = lambda  a,b : a if a > b else b
print(maks(25, 20))

same = lambda a : True if a == 25 else False
print(same(20))


    
