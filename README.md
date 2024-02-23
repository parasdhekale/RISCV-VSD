# Week 1
## Tools installation for RISCV-VSD internship  
System Specification :-   
    1. OS - Ubuntu 20.04  
    2. RAM - 8 GB  
    3. Size - 100 GB HDD  

Install RISC V GNU toolchain, Yosys, iVerilog and GTKWave.  
Status - Completed.  

# Week 2
## Identify Instruction type & 32 bit code 
Instruction 1: add r6, r2, r1  
Type: R-type  
Syntax: add rd,rs1,rs2  
32 bit code : 0000000 r1 r2 000 r6 0110011  

Instruction 2: sub r7, r1, r2  
Type: R-type    
Syntax: sub rd,rs1,rs2      
32 bit code : 0100000 r2 r1 000 r7 0110011  

Instruction 3: and r8, r1, r3  
Type: R-type    
Syntax: and rd,rs1,rs2       
32 bit code : 0000000 r3 r1 111 r8 0110011        

Instruction 4: or r9, r2, r5  
Type: R-type    
Syntax: or rd,rs1,rs2        
32 bit code : 0000000 r5 r2 110 r9 0110011     

Instruction 5: xor r10, r1, r4  
Type: R-type    
Syntax: xor rd,rs1,rs2     
32 bit code : 0000000 r4 rs 100 r10 0110011    

Instruction 6: slt r11, r2, r4  
Type: R-type    
Syntax: slt rd,rs1,rs2      
32 bit code : 0000000 r4 r2 010 r11 0110011     

Instruction 7: addi r12, r4, 5  
Type: I-type   
Syntax: addi rd,rs1,imm       
32 bit code : 00000000101 r4 000 r12 0010011     

Instruction 8: sw r3, r1, 2  
Type: S-type     
Syntax: sw rs1,rs2,imm       
32 bit code : 0000000 r1 r3 010 0010 0100011     

Instruction 9: lw r13, r1, 2  
Type: I-type     
Syntax: lw rd,rs1,imm      
32 bit code : 00000000010 r1 010 r13 0000011     

Instruction 10: beq r0, r0, 15  
Type: B-type     
Syntax: beq rs1,rs2,imm      
32 bit code : 0000000 r0 r0 000 11110 1100011    

Instruction 12: bne r0, r1, 20  
Type:  B-type   
Syntax: bne rs1,rs2,imm      
32 bit code : 0000001 r1 r0 001 01000 1100011       

Instruction 14: sll r15, r1, r2(2)  
Type: R-type     
Syntax: sll rd,rs1,rs2     
32 bit code : 0000000 r2 r1 001 r15 0110011       

Instruction 15: srl r16, r14, r2(2)  
Type: R-type    
Syntax: sr1 rd,rs1,rs2     
32 bit code : 0000000 r2 r14 101 r16 0110011  

## Compile a C code using RISCV GNU Toolchain
Write a sample C code and compile it using gcc.  
![c code](https://github.com/parasdhekale/RISCV-VSD/assets/71093755/492b3881-a40f-4161-a37b-e43f583f2fb2)

Now compile same using riscv gnu toolchain.  
'riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64imac -o sum1ton.o sum1ton.c'   

View the obj file using **riscv64-unknown-elf-objdump -d sum1ton.o | less**    
![obj file](https://github.com/parasdhekale/RISCV-VSD/assets/71093755/93c2de46-02d5-4db9-a72e-be607f89d59a)


