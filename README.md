# Construindo-seu-Primeiro-Projeto-L-gico-de-Banco-de-Dados
1. Definição do Banco de Dados
Primeiro, precisamos definir o que queremos armazenar. Vamos criar um banco de dados para gerenciar livros e autores.

2. Estrutura do Banco de Dados
Vamos criar duas tabelas:

Autores
Livros
-- Criação do banco de dados
CREATE DATABASE Biblioteca;

-- Seleciona o banco de dados
USE Biblioteca;

-- Criação da tabela Autores
CREATE TABLE Autores (
    AutorID INT AUTO_INCREMENT PRIMARY KEY,
    Nome VARCHAR(100) NOT NULL,
    Nacionalidade VARCHAR(50),
    DataNascimento DATE
);

-- Criação da tabela Livros
CREATE TABLE Livros (
    LivroID INT AUTO_INCREMENT PRIMARY KEY,
    Titulo VARCHAR(100) NOT NULL,
    AutorID INT,
    AnoPublicacao INT,
    FOREIGN KEY (AutorID) REFERENCES Autores(AutorID)
);
