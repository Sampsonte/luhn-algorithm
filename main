def luhn_kontrol(s):
    n = 16    # 16 haneli bir sayı olucağını belirlemiş
    d1 = {}
    d2 = {}
    for i in range(1, n + 1):       # range functionı bir eksiğini aldığı için n + 1 eklemiş
        d2[i] = int(s[i - 1])       
    for i in range(1, n + 1):
        if i % 2 != 0:            #2 ile bölümünden kalan 2 değilse: (yani çift değilse) (456789 sayısındaki 5 7 ve 9 rakamlarını almak için yani)
            d1[i] = 2 * d2[i]        # d1, d2nin iki katı
            if d1[i] > 9:     # d1[i] dokazdan büyükse:
                d1[i] = int(d1[i] / 10) + d1[i] % 10     # d1[i] nin 10a bölümünün tam sayılarıyla 10 ile bölümünün kalanını toplamış
        else:
            d1[i] = d2[i]    # dokuzdan küçükse

    ciftler_toplami = 0    # toplam değirini sıfırlamak için 
    tekler_toplami  = 0
    for i in range(1, n + 1):
        if i % 2 != 0:        # 2 ile bölümünden kalan 2 değilse açıklaması yukarıda var
            tekler_toplami += d1[i] 
        else:
            ciftler_toplami += d1[i]

    toplam = tekler_toplami + ciftler_toplami
    
    kalan = toplam % 10    # kalan toplamın 10 ile bölümünden kalan onu belirlemiş
    if kalan == 0:      
        return True
    else:
        return False     #kalan sıfırsa komutu uygulatmış değilse uygulatmamış

def son_digit_dogrulama(s1):
    n = 16
    d1 = {}
    d2 = {}
    for i in range(1, n + 1):
        d2[i] = int(s1[i - 1])

    for i in range(1 , n):
        d1[i] = d2[n - i]

    for i in range(1 , n):
        if i % 2 != 0:
            d1[i] = 2 * d1[i]                                   # yukardakilerinin hemen hemen aynısı sayılır sadece kısaltılmış halleri     

    for i in range(1 , n):
        if d1[i] > 9: d1[i] -= 9

    toplam = 0
    for i in range(1 , n):
        toplam += d1[i]

    kalan = 9 * toplam % 10

    if kalan == d2[n]:
        return True, kalan
    else:
        return False, -1

print("")

s1 = input("KART NUMARASI GİRİNİZ: ")

print("")

print("luhn_kontrol")

print("")
if luhn_kontrol(s1) == True:
    print(s1 + " - BU KART NUMARASI GEÇERLİDİR.")
else:
    print(s1 + " - BU KART NUMARASI GEÇERLİ DEĞİLDİR.")

print("")

print("son_digit_dogrulama")

print("")
sonuc, sondigit = son_digit_dogrulama(s1)
if sonuc == True:
    print(s1 + " - BU KART NUMARASI GEÇERLİDİR. son digit:", sondigit)
else:
    print(s1 + " - BU KART NUMARASI GEÇERLİ DEĞİLDİR.")

print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")
print("")

cikis = input("ÇIKIŞ YAPMAK İÇİN ENTER'A BASINIZ")
