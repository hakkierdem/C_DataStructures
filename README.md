# C_DataStructures

Temel veri yapılarının C ile, standart kütüphaneye dayanmadan sıfırdan
implementasyonu. Amaç, bellek yönetiminin ve pointer aritmetiğinin veri yapısı
tasarımını nasıl şekillendirdiğini elle görmek.

## İçerik

| Klasör | Yapı | Kapsam |
|---|---|---|
| `Array/` | Dinamik dizi | Büyüme stratejisi, ekleme/silme, indeksleme |
| `LinkedList/` | Bağlı liste | Tek yönlü liste, ekleme/silme, traversal |
| `Stack/` | Yığın | LIFO işlemleri, push/pop/peek |
| `Queue/` | Kuyruk | FIFO işlemleri, enqueue/dequeue |
| `Trees/` | Ağaç | İkili arama ağacı, dolaşma (inorder/preorder/postorder) |

## Derleme

```bash
gcc -Wall -Wextra -std=c11 LinkedList/linkedlist.c -o linkedlist
./linkedlist
```

Her klasör bağımsız derlenebilir; ortak bir build sistemi kullanılmamıştır.

## Notlar

- Her `malloc` çağrısının karşılığında bir `free` bulunur; bellek sızıntısı
  kontrolü için `valgrind` ile doğrulanabilir.
- Hata durumları dönüş değerleriyle bildirilir, çağıran taraf kontrol etmelidir.
- Bu kod üretim amaçlı değil, öğrenme amaçlıdır; kritik uygulamalarda test edilmiş
  kütüphaneleri tercih edin.
