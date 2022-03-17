# **Binary Search Three Project**

## Binary Search Tree Nedir?

İkili ağaçların (Binary Tree) özel bir hali olan ikili arama ağaçlarında, düğümlerde duran bilgilerin birbirine göre küçüklük büyüklük ilişkisi bulunmalıdır. Örneğin tam sayılardan(integer) oluşan veriler tutulacaksa bu verilerin aralarında küçük-büyük ilişkisi bulunmaktadır.

İkili arama ağacı, her düğümün solundaki koldan ulaşılabilecek bütün verilerin düğümün değerinden küçük, sağ kolundan ulaşılabilecek verilerin değerinin o düğümün değerinden büyük olmasını şart koşar.

---

## Binary Search Tree Nasıl Çalışır?

Ağacın üzerinde duran verilerin özel bir şekilde sıralı bulunması gerekir. Buna göre herhangi bir değeri arayan kişi ağacın kök değerine bakarak aşağıdaki 3 eylemden birisini yapar:

1. Aranan sayı kökteki değere eşittir -> aranan değer bulunmuştur
2. Aranan sayı kökteki değerden küçüktür -> Kökün sol kolu takip edilir
3. Aranan sayı kökteki deüerden büyüktür -> Kökün sağ kolu takip edilir

---

## Patika Binary Search Tree Projesi


### [7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary Search Tree mantığına göre görsel olarak aşama aşama gösterilmesi gerekmektedir. Buna göre:


* Adım 1

Root değerini 7 olarak kabul edersek dizi içerisinde sonraki indisteki değerin root değerimizden büyük ya da küçük olmasına göre soluna veya sağına yerleştireceğiz.

5 değeri 7 değerinden küçük olduğu için root değerimizin solunda ilk branchi oluşturur.

```
            7
           /
          5

```
---
* Adım 2

Sıradaki indisteki 1 değeri root değeri 7'den ve branch değeri 5'ten küçük. Dolayısıyla 5'in solundan yeni bir subtree oluşturur.

```
            7
           /
          5
         /
        1  

```
---
* Adım 3

8 değeri root değerimiz 7'den büyük olduğu için sağ tarafa bir branch eklenmesi sağlar.

```
            7
           / \
          5   8 
         /
        1  

```
---
* Adım 4

Sıradaki indisteki 3 değeri root değeri 7'den ve 5'ten küçük olduğu için sola, branchteki 1 değerinden büyük olduğu için 1 kendi altında yeni bir branch oluşturur.

```
            7
           / \
          5   8 
         /
        1 
         \
          3

```
---
* Adım 5

Sıradaki indisteki 6 değeri root değeri 7'den küçük fakat alt ağaç node'u 5'ten büyük olduğu için, 5 değerinin sağına yeni bir branch ekler.


```
            7
           / \
          5   8 
         / \
        1   6
         \
          3

```
---
* Adım 6

Sıradaki indisteki 0 değeri root değeri 7'den ve solundaki nodeların tümünden daha küçük olduğu için 1 değerinin solunda yeni bir branch oluşturur.

```
            7
           / \
          5   8 
         / \
        1   6
      /   \
     0     3

```
---
* Adım 7

Sıradaki indisteki 9 değeri root değeri olan 7'den ve alt ağaç branchi olan 8'den büyük olduğu için 8 değerinin sağına yeni bir branch oluşturur.

```
            7
           / \
          5   8 
         / \   \
        1   6   9
      /   \
     0     3

```
---
* Adım 9
---
Sıradaki indisteki 4 değeri root değerinden ve alt branch node'u olan 5'ten küçük fakat 1'den büyüktür. Dolayısıyla 1'in sağına doğru branch yapar, fakat Binary Three'de her bir node'a ancak ikili bağlantı kurulabildiği için 3 değerinin olduğu node'un sağına doğru alt branch oluşturur.

```
            7
           / \
          5   8 
         / \   \
        1   6   9
      /   \
     0     3
            \
             4

```
---
* Adım 10

Sıradaki indisteki 2 değeri ise Adım 9'da bahsedildiği noktaya gelip 3 değerinin soluna bir alt branch oluşturur. Bu aynı zamanda dizimizin Binary Search Three mantığına göre diziliminin son halidir.

```
            7
           / \
          5   8 
         / \   \
        1   6   9
      /   \
     0     3
          /  \
         2    4

```

---

## Kaynakça

[Medium Veri Yappıları - Binary Search Three Nedir?](https://tsafaelmali.medium.com/binary-search-tree-nedir-2e6fb0621d9)


