# CSCI-201-MIPS-Preliminary-Project
#program:Project 0
    .data
    out_string:            .asciiz "Hello @02921255\n"
    out_string2:           .asciiz "Hello @02921255"
    .text 
main:
    li $v0, 4              # calls code 
    li $v0, 5              # N - 02921255 % 11 = 3
    la $a0, out_string     #loads string
    li $t0, 0              #$t0=how many loops
loop:
    beq $t0,$s0,exit       #condition statement for if $t0 not=to 0
    syscall                #prints out_string
    addi $t0,$t0,1         #adds to $t0
    j loop                 #returns to start of program
exit:
    lam $a0, out_string2
    syscall

    li $v0
    syscall                #exits 
