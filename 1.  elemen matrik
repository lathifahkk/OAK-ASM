#Elemen Matriks
Buatlah program untuk menampilkan nilai elemen matriks sesuai dengan baris dan kolom dari masukan.

Berikut isi dari matriks tersebut, simpan sebagai array double word.

7  11  10   6
5   8   9   2
1   3  12   4

###Contoh Masukan
```
1 2
```
###Contoh Keluaran
```
9
```

###code
```
global main 
extern scanf
extern printf
extern fflush
 
segment .data
    M       dd      7, 11, 10, 6,
            dd      5, 8, 9, 2,
            dd      1, 3, 12, 4
    ncol    dd      4
    sken     db      "%d %d", 0
    prin     db      "%d", 10, 0
 
segment .bss
    a      resd    1
    b       resd    1
    val     resd    1
 
segment .text
    main:
    .read
        push a
        push b
        push sken
        call scanf
        add esp, 12
 
        mov eax, [b]
        mul dword [ncol]
        add eax, [a]
        mov ebx, [M + eax*4]
        mov [val], ebx
 
    .print
        push dword [val]
        push prin
        call printf
        add esp, 8
     
    exit:
        push 0
        call fflush
        add esp, 4
 
        mov eax, 1
        mov ebx, 0
        int 80h
```
