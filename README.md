.dados

.macro finalizarPrograma
li $v 0, 10
syscall
.end_macro

.macro printf
.data
msg: .asciiz %str
.text
li $v 0,4
la $a 0, msg
syscall

.end_macro

.text
.globl principal

principal:
printf{"ola mundo"}
finalizarPrograma

