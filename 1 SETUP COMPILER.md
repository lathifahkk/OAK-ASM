<h1>
Lab: Setup ASM
</h1> 


<h2>Setup</h2>

```
https://auriza.github.io/posts/setup-asm-x86/
```

<h2>Instruksi x86</h2>

```
https://github.com/auriza/x86/blob/master/instruction.md#set-instruksi
```

<h2>Geany</h2>

Tambahkan di menu Build -> Set Build Commands -> Build:

```
yasm "%f" -f elf32 -g dwarf2 -l "%e".lst && gcc -o "%e" -m32 "%e".o
```


<h2>Online Compiler</h2>

```
https://www.tutorialspoint.com/compile_yasm_online.php
```
```
Project --> Compile Options --> yasm -f elf *.asm; gcc -m32 -o demo *.o
```
