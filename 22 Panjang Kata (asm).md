<h1>Panjang Kata</h1>

```
Buatlah program untuk menghitung panjang kata yang diberikan. 
Panjang kata maksimum 20 karakter.
```

Contoh Masukan

```
ilkom
```

Contoh Keluaran

```
5
```

<h2>Code</h2>

```
extern printf
extern scanf
extern fflush
 ;22. panjang kata (asm)
  
  
     global main
section .data
    output      db  "%d", 10, 0
    input       db  "%s", 0
  
section .bss
    string   resb    21
  
section .text
 
main:
  
    push string ;scanf dan di masukin ke sting
    push input
    call scanf
    add esp, 8
     
    cld             ; normalin, ngeclear
    mov al, 0        ;cari karakter
    mov edi, string ; alamat untuk kata yang dibaca
    mov ecx, -1     ;counter maks 21
    repne scasb     ;scan katanya pertehur, teru sscan sampai ketemu null
     
    sub edi, string ; edi dikurangin sama dring awal
    ;edi itu jadi indeks dimana null
    dec edi
     
     
    push edi        ; untuk ngeprint, letak null
    push output     ; masukin ke output
    call printf
    add esp, 8
     
 
;keluar
exit:
    push 0
    call fflush
      
    mov eax, 1
    mov ebx, 0
    int 80h
```
