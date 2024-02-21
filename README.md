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
32 bit code : 0100000 rs2 rs1 000 rd 0110011  

Instruction 3: and r8, r1, r3  
Type: R-type    
Syntax: and rd,rs1,rs2       
32 bit code : 0000000 rs2 rs1 111 rd 0110011        

Instruction 4: or r9, r2, r5  
Type: R-type    
Syntax: or rd,rs1,rs2        
32 bit code : 0000000 rs2 rs1 110 rd 0110011     

Instruction 5: xor r10, r1, r4  
Type: R-type    
Syntax: xor rd,rs1,rs2     
32 bit code : 0000000 rs2 rs1 100 rd 0110011    

Instruction 6: slt r11, r2, r4  
Type: R-type    
Syntax: slt rd,rs1,rs2      
32 bit code : 0000000 rs2 rs1 010 rd 0110011     

Instruction 7: addi r12, r4, 5  
Type: I-type   
Syntax: addi rd,rs1,imm       
32 bit code : imm[11:0] rs1 000 rd 0010011     

Instruction 8: sw r3, r1, 2  
Type: S-type     
Syntax: sw rs1,rs2,imm       
32 bit code : imm[11:5] rs2 rs1 010 imm[4:0] 0100011     

Instruction 9: lw r13, r1, 2  
Type: I-type     
Syntax: lw rd,rs1,imm      
32 bit code : imm[11:0] rs1 010 rd 0000011     

Instruction 10: beq r0, r0, 15  
Type: B-type     
Syntax: beq rs1,rs2,imm      
32 bit code : imm[12|10:5] rs2 rs1 000 imm[4:1|11] 1100011    

Instruction 12: bne r0, r1, 20  
Type:  B-type   
Syntax: bne rs1,rs2,imm      
32 bit code : imm[12|10:5] rs2 rs1 001 imm[4:1|11] 1100011       

Instruction 14: sll r15, r1, r2(2)  
Type: R-type     
Syntax: sll rd,rs1,rs2     
32 bit code : 0000000 rs2 rs1 001 rd 0110011       

Instruction 15: srl r16, r14, r2(2)  
Type: R-type    
Syntax: sr1 rd,rs1,rs2     
32 bit code : 0000000 rs2 rs1 101 rd 0110011     
