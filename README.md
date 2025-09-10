# Níveis de Linguagens em Ordem Decrescente: Foi criado um código que imprime a frase "Hello world" nas linguagens de programação. Do Baixo ao Alto Nivel

## 1 - Assembly 
✅ Código Assembly 64 bits para imprimir "hello world"
section .data
    msg db 'hello world', 0xA  ; A mensagem a ser exibida com quebra de linha
    len equ $ - msg            ; Calcula o comprimento da mensagem

section .text
    global _start              ; Ponto de entrada

_start:
    ; sys_write (syscall número 1)
    mov rax, 1                 ; syscall: sys_write
    mov rdi, 1                 ; file descriptor 1: saída padrão (stdout)
    mov rsi, msg               ; endereço da mensagem
    mov rdx, len               ; comprimento da mensagem
    syscall

    ; sys_exit (syscall número 60)
    mov rax, 60                ; syscall: sys_exit
    xor rdi, rdi               ; código de saída 0
    syscall
💻 Como compilar e rodar (em Linux)
Salve o código como, por exemplo, hello.asm.

Compile com NASM e o linker do ld:

nasm -f elf64 hello.asm -o hello.o
ld hello.o -o hello
Execute:

./hello
Você verá a saída:

hello world
## 2 - Cobol
✅ Código COBOL para imprimir "hello world"
       IDENTIFICATION DIVISION.
       PROGRAM-ID. HelloWorld.

       PROCEDURE DIVISION.
           DISPLAY "hello world".
           STOP RUN.
💻 Como compilar e executar com GnuCOBOL (em Linux, macOS ou Windows com GnuCOBOL)
Salve o código em um arquivo chamado hello.cob.

Compile usando o GnuCOBOL:

cobc -x hello.cob
Execute o programa:

./hello
Você verá a saída:

hello world
## 3 - Pascal
✅ Código Pascal para imprimir "hello world"
program HelloWorld;

begin
  writeln('hello world');
end.
💻 Como compilar e executar com Free Pascal (FPC)
Salve o código em um arquivo, por exemplo, hello.pas.

Compile com o Free Pascal:

fpc hello.pas
Execute o programa:

./hello
Saída esperada:

hello world
## 4 - Java 
✅ Código Java para imprimir "hello world"
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("hello world");
    }
}
💻 Como compilar e executar (usando terminal/console)
Salve o código em um arquivo chamado HelloWorld.java (o nome do arquivo deve ser o mesmo da classe pública).

Compile o programa com o javac:

javac HelloWorld.java
Execute o programa com o java:

java HelloWorld
Saída esperada:

hello world

## 5 - C
✅ C
#include <stdio.h>

int main() {
    printf("hello world\n");
    return 0;
}
💻 Compilar e rodar (Linux/macOS/WSL):
gcc hello.c -o hello
./hello
## 6 - C#
✅ C++
#include <iostream>

int main() {
    std::cout << "hello world" << std::endl;
    return 0;
}
💻 Compilar e rodar:
g++ hello.cpp -o hello
./hello
## 7 - C++
✅ C#
using System;

class HelloWorld {
    static void Main() {
        Console.WriteLine("hello world");
    }
}
💻 Compilar e rodar com .NET SDK:
Crie um arquivo chamado HelloWorld.cs.

Compile:

csc HelloWorld.cs
Execute:

./HelloWorld
Ou, com o .NET CLI moderno (Linux/Windows/macOS):

dotnet new console -o HelloApp
cd HelloApp
dotnet run
## 8 - Java Script
✅ JavaScript (console – ambiente Node.js ou navegador)
console.log("hello world");
💻 Executar no navegador:
Abra o navegador (Chrome, Firefox, etc.).

Pressione F12 para abrir o console do desenvolvedor.

Cole o código:

console.log("hello world");
Pressione Enter e verá:

hello world
💻 Executar com Node.js (no terminal)
Crie um arquivo chamado hello.js com o conteúdo:

console.log("hello world");
Execute com o Node.js:

node hello.js
## 9 - Python
✅ Python
print("hello world")
💻 Como executar
✅ No terminal:
Crie um arquivo chamado hello.py com o conteúdo acima.

Execute com o Python:

python hello.py
✅ Ou diretamente no terminal/interpreter:
Basta digitar:
