# python-proje1
1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]


l = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
def flatten(xs):
    res = []
    def loop(ys):
        for i in ys:
            if isinstance(i, list):
                loop(i)
            else:
                res.append(i)
    loop(xs)
    return res
flatten(l)

[1, 'a', 'cat', 2, 3, 'dog', 4, 5]



2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]


l =[[1, 2], [3, 4], [5, 6, 7]]
l=l[::-1]

for i in range(len(l)):
    (l[i])=(l[i])[::-1]
print(l)

[[7, 6, 5], [4, 3], [2, 1]]
