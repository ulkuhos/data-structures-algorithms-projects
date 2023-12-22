# Proje 1: Insertion Sort ve Selection Sort

## Insertion Sort

``` 
[22,27,16,2,18,6] -> Insertion Sort
```
**Soru 1- Yukarı verilen dizinin Insertion sort türüne göre aşamalarını yazınız.**
*Yanıt:*
```
   Adım 1: [22,27,16,2,18,6]   // 22, 27'den küçük olduğu için sıralama yapıldı
   Adım 2: [22,16,27,2,18,6]   // 27 ile 16 yer değişti
   Adım 3: [16,22,27,2,18,6]   // 22 ile 16 yer değişti

   Adım 4: [16,22,2,27,18,6]   // 27 ile 2 yer değişti
   Adım 5: [16,2,22,27,18,6]   // 22 ile 2 yer değişti
   Adım 6: [2,16,22,27,18,6]   // 16 ile 2 yer değişti
   
   Adım 7: [2,16,22,18,27,6]   // 27 ile 18 yer değişti
   Adım 8: [2,16,18,22,27,6]   // 22 ile 18 yer değişti

   Adım 9: [2,16,18,22,6,27]   // 27 ile 6 yer değişti
   Adım 10: [2,16,18,6,22,27]  // 22 ile 6 yer değişti
   Adım 11: [2,16,6,18,22,27]  // 18 ile 6 yer değişti
   Adım 12: [2,6,16,18,22,27]  // 16 ile 6 yer değişti
```

**Soru 2- Big-O gösterimini yazınız.**
*Yanıt:*
```Big-O: İşlemler n'den 1'e kadar gideceği için, 1'den n'e kadar olan sayilarin toplami sonucu verecektir. n tane değer için yapılacak işlem n+(n-1)+(n-2)+(n-3)+.........+1 dir  
             n.(n+1)/2 :Bu işlemlerin toplamı sonucundan (n^2+n)/2 denklemini buluruz.
           = n^2       :Bu denklemi donime eden değer n^2 olduğu için Big-O Notation-> O(n^2)
```

**Soru 3- Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız.**
**Average case: Aradığımız sayının ortada olması**
**Worst case: Aradığımız sayının sonda olması**
**Best case: Aradığımız sayının dizinin en başında olması.**
*Yanıt:* 
```
Time Complexity: 18 sayisi-aradığımız sayı dizinin ortasında. Bu yüzden, Average Case uygundur.
```

## Selection Sort 

```
[7,3,5,8,2,9,4,15,6] -> dizisinin Selection Sort'a göre ilk 4 adımını yazınız.
```
**Soru 1- Yukarı verilen dizinin Insertion sort türüne göre aşamalarını yazınız.**
*Yanıt:*
```
İlk 4 adımı:
    Adım 1: [2,3,5,8,7,9,4,15,6]
    Adım 2: [2,3,4,8,7,9,5,15,6]
    Adım 3: [2,3,4,5,7,9,8,15,6]
    Adım 4: [2,3,4,5,6,9,8,15,7]
Devamı:
    Adım 5: [2,3,4,5,6,7,8,15,9]
    Adım 6: [2,3,4,5,6,7,8,9,15]
```

***

# Proje 2:Merge Sort

## Merge Sort
```
[16,21,11,8,12,22] -> Merge Sort
```
Soru 1 : Yukarıdaki dizinin Merge Sort türüne göre aşamalarını yazınız.
*Yanıt:*
```
Adım 1:   [16,21,11]           -             [8,12,22]
Adım 2:  [16,21] - [11]                    [8,12] - [22]
Adım 3:  [16]-[21]-[11]                    [8]-[12]-[22]
Adım 4:  [16,21] - [11]                    [8,12] - [22]
Adım 5:   [11,16,21]                         [8,12,22]
Adım 6:                 [8,11,12,16,21,22]
```

Soru 2 :Big-O gösterimini yazınız.
*Yanıt:*
```
Big-O gosterimi : O(nlogn) olacaktir.
```

***

# Proje 3: Binary Search Tree 

## Binary Search Tree
```
[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] -> Binary-Search-Tree
```
Soru 1 :Yukardaki dizinin Binary-Search-Tree aşamalarını yazınız.
Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.
*Yanıt:*
```
**Root x = 6 olarak alalım.**
        6
      /   \ 
     5     7
    /       \
   1         8
  / \         \
 0   3         9
    / \      
   2   4    
```
Sırasıyla dizini inclelediğimizde;

```
Adım 1: "7" > 6 old.için root'un sağında "7" bulunur.
Adım 2: "5" < 6 old.için root'un solunda "5" bulunur.
Adım 3: "1" < 5 ve 6 old.için "1" root'un soluna eklenir.
Adım 4: "8" > 6 old.için "8" root'un sağına eklenir.
Adım 5: 1< "3" <5<6 old.için "3" root'un soluna ama 1'in sağına eklenir.
Adım 6: "0" < 1<5<6 old.için "0" root'un soluna eklenir.
Adım 7: "9" > 6 old.için "9" root'un sağına eklenir.
Adım 8: 1<3< "4" <5<6 old.için "4" root'un soluna eklenir.
Adım 9: 1< "2" <3<5<6 old.için "2" root'un soluna eklenir.
```