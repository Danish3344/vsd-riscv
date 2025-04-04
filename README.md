# vsd-riscv
In the entire task the danish.c the c code 
<details>
<summary><b>Task 1:</b> in this task c based code is compiled using gcc and riscv based on RISCV based lab </summary>

### C Language Based Lab
we should follow the following steps to compile any **.c** file:
1. open terminal. then the following command is :
   ```
   gedit danish.c
   ```
2. This command will open a text editor to type the code. Then type the c code of printing the sum of n number. Once the code is done save the file
3. to compile the c code ,run the following command on the terminal:
   ```
   gcc danish.c
   ```
4. to run the code, run the following command:
   ```
   ./a.out
   ```
### RISCV Based LAB
Follow the given steps:
1.Open the terminal and then run the given command:
  ```
   cat danish.c
  ```
2. to compile the code in riscv64 gcc compiler to get RISCV objdump in -o1 format run  this command:
  ```
  riscv64-unknown-elf-gcc -o1 -mabi=lp64 -march=rv64i -o danish.o danish.c
  ```
3. Open a new tab terminal and then run the given command:
   ```
   riscv64-unknown-elf-objdump -d danish.o
   ```
4. To get main section of data run given command, afterthe ```/main``` to locate main section of the code
   ```
   riscv64-unknown-elf-objdump -d danish.o | less
   ```
5. to get RISCV objdump in -ofast format run the given command in perivous tab:
    ```
    riscv64-unknown-elf-gcc -ofast -mabi=lp64 -march=rv64i -o danish.o danish.c
    ```
6. Open a new tab terminal then run the given command :
    ```
    riscv64-unknown-elf-objdump -d danish.o
    ```
7. To get main section of the data run the given command, After that ```/main``` to locate the main section of the code:
   ```
   riscv64-unknown-elf-objdump -d danish.o | less
