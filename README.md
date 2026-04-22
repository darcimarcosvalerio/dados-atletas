# Dados dos Atletas - Projeto de Certificação 2

## 📋 Descrição do Projeto

Aplicação JavaScript que recebe informações de um atleta e calcula parâmetros importantes como categoria, IMC e média válida de desempenho. Este projeto foi desenvolvido como parte do Projeto de Certificação 2 de uma competição.

## 🎯 Objetivo

Criar uma classe `Atleta` que:
- Armazena informações do atleta (nome, idade, peso, altura, notas)
- Calcula a categoria baseado na idade
- Calcula o Índice de Massa Corporal (IMC)
- Calcula a média válida das notas (desconsiderando as notas máxima e mínima)
- Fornece métodos para obter todas as informações

## 📚 Especificações

### Classe Atleta

#### Atributos
- `nome`: Nome do atleta
- `idade`: Idade em anos
- `peso`: Peso em kg
- `altura`: Altura em metros
- `notas`: Array de notas obtidas

#### Métodos de Cálculo
- `calculaCategoria()`: Retorna a categoria do atleta baseado na idade
- `calculaIMC()`: Retorna o IMC (peso / altura²)
- `calculaMediaValida()`: Retorna a média válida (excluindo nota máxima e mínima)

#### Métodos de Acesso (Getters)
- `obtemNomeAtleta()`: Retorna o nome
- `obtemIdadeAtleta()`: Retorna a idade
- `obtemPesoAtleta()`: Retorna o peso
- `obtemNotasAtleta()`: Retorna as notas
- `obtemCategoria()`: Retorna a categoria
- `obtemIMC()`: Retorna o IMC
- `obtemMediaValida()`: Retorna a média válida

### Categorias por Idade

| Idade | Categoria |
|-------|-----------|
| 9-11 anos | Infantil |
| 12-13 anos | Juvenil |
| 14-15 anos | Intermediário |
| 16-30 anos | Adulto |
| Outras | Sem categoria |

## 💻 Como Usar

```javascript
// Criar uma instância do atleta
const atleta = new Atleta("Cesar Abascal", 30, 80, 1.70, [10, 9.34, 8.42, 10, 7.88]);

// Acessar as informações
console.log("Nome:", atleta.obtemNomeAtleta());           // Cesar Abascal
console.log("Idade:", atleta.obtemIdadeAtleta());         // 30
console.log("Peso:", atleta.obtemPesoAtleta());           // 80
console.log("Altura:", atleta.altura);                    // 1.7
console.log("Notas:", atleta.obtemNotasAtleta());         // [10, 9.34, 8.42, 10, 7.88]
console.log("Categoria:", atleta.obtemCategoria());       // Adulto
console.log("IMC:", atleta.obtemIMC());                   // 27.68166089965398
console.log("Média válida:", atleta.obtemMediaValida());  // 9.25333333
```

## 📊 Cálculos Realizados

### 1. Categoria
Determinada pela idade do atleta, seguindo as faixas etárias definidas.

### 2. IMC (Índice de Massa Corporal)
```
IMC = peso / (altura × altura)
```

### 3. Média Válida
Remove a nota máxima e a nota mínima do array de notas e calcula a média das notas restantes:
```
Exemplo: notas [10, 9.34, 8.42, 10, 7.88]
Ordenadas: [7.88, 8.42, 9.34, 10, 10]
Sem extremos: [8.42, 9.34, 10]
Média: (8.42 + 9.34 + 10) / 3 = 9.25333333
```

## 🚀 Como Executar

### No Node.js
```bash
node dados-atletas.js
```

### No Navegador
Inclua o arquivo em um HTML:
```html
<script src="dados-atletas.js"></script>
```

## 📝 Exemplo de Saída

```
Nome: Cesar Abascal
Idade: 30
Peso: 80
Altura: 1.7
Notas: 10,9.34,8.42,10,7.88
Categoria: Adulto
IMC: 27.68166089965398
Média válida: 9.25333333
```

## 📁 Estrutura do Repositório

```
notas-atletas/
├── dados-atletas.js    # Arquivo principal com a classe Atleta
├── README.md           # Este arquivo
└── .gitignore         # Arquivos a serem ignorados pelo Git
```

## 🤝 Requisitos

- Node.js (para executar via linha de comando)
- Navegador moderno com suporte a ES6 (para executar no navegador)

## 📚 Conceitos Utilizados

- Programação Orientada a Objetos (OOP)
- Classes e Construtores
- Métodos
- Array e manipulação de dados
- Cálculos matemáticos
- Métodos de acesso (Getters)

## 🎓 Desenvolvido por

Projeto de Certificação - Desenvolvedor

## 📄 Licença

Este projeto é fornecido como material educacional.

---

**Data de Criação**: Abril de 2026
