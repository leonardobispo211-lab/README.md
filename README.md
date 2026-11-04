# Carteira de Investimentos 
Programa em C (terminal) que simula uma carteira de investimentos acessíveis, suportando múltiplos ativos simultâneos com persistência de dados.

**Tema:** inclusão financeira (ODS 8.10 da ONU).  
**Foco:** structs, modularização e manipulação de arquivos (I/O).

## 1. Descrição do projeto

O projeto consiste em um sistema de gerenciamento e simulação de uma carteira de investimentos, desenvolvido em linguagem C e executado pelo terminal. O usuário pode cadastrar ativos, consultar a composição da carteira, acompanhar valores e rentabilidade e visualizar simulações educativas de possíveis rendimentos ao longo do tempo.

As informações cadastradas são armazenadas em arquivo texto, permitindo que a carteira seja recuperada em uma próxima execução do programa. A proposta também busca contribuir para a inclusão financeira, apresentando conceitos como juros compostos, risco e rentabilidade de forma simples e acessível, em alinhamento à meta ODS 8.10 da ONU.

## 2. Público-alvo

O sistema é destinado principalmente a pessoas que desejam aprender conceitos básicos de investimentos e organização financeira, especialmente estudantes, iniciantes no mercado financeiro e usuários que procuram uma ferramenta simples para acompanhar uma carteira simulada.

Não substitui plataformas de corretoras nem oferece recomendações financeiras. As taxas utilizadas no simulador são estimativas educativas.

## 3. Funcionalidades do sistema

- **Cadastrar ativos:** registra nome, categoria, quantidade, preço de compra e preço atual.
- **Listar ativos:** exibe os ativos cadastrados na carteira e seus respectivos dados.
- **Calcular valor total:** soma o valor atual de todos os ativos, considerando suas quantidades.
- **Calcular rentabilidade geral:** apresenta a variação percentual entre o valor total de compra e o valor atual da carteira.
- **Ordenar por rentabilidade:** organiza os ativos da maior para a menor rentabilidade.
- **Simulador educativo:** projeta a evolução do valor da carteira em 12 meses, utilizando três taxas mensais ilustrativas associadas a diferentes níveis de risco.
- **Relatório final:** apresenta a composição da carteira ordenada, o resumo financeiro e uma explicação sobre inclusão financeira e ODS 8.10.
- **Salvar e carregar dados:** grava os ativos em `data/carteira.txt` e recupera os dados na inicialização do programa.

## 4. Tecnologias utilizadas no desenvolvimento

- **Linguagem C:** implementação da lógica e das funcionalidades do sistema.
- **GCC (GNU Compiler Collection):** compilação do código-fonte.
- **Biblioteca padrão de C (`stdio.h`):** entrada e saída de dados pelo terminal e manipulação de arquivos.
- **Arquivos texto (`.txt`):** persistência dos dados da carteira, com campos separados por ponto e vírgula.
- **Structs e modularização:** organização dos dados dos ativos e separação do programa em módulos e arquivos de cabeçalho.

## 5. Requisitos mínimos para execução

- Computador com sistema operacional Windows, Linux ou macOS.
- Compilador C instalado (GCC recomendado).
- Terminal ou prompt de comando para executar a compilação e o programa.
- Permissão de leitura e escrita na pasta do projeto, especialmente na pasta `data/`.
- Espaço em disco suficiente para os arquivos do projeto e para o arquivo de dados.

## 6. Instruções para execução

### 6.1. Preparar o projeto

1. Extraia os arquivos do projeto para uma pasta.
2. Abra o terminal nessa pasta, na raiz do projeto (a pasta que contém `Src`, `include` e `data`).
3. Verifique se o GCC está instalado:

```bash
gcc --version
```

### 6.2. Compilar

No terminal, execute:

```bash
gcc -Wall -Wextra -Iinclude Src/main.c Src/funcoes.c Src/modulo.c -o programa
```

> Observação: os nomes das pastas e arquivos devem respeitar as letras maiúsculas e minúsculas em sistemas que diferenciam maiúsculas de minúsculas, como Linux.

### 6.3. Executar

No Linux ou macOS:

```bash
./programa
```

No Windows (Prompt de Comando):

```bat
programa.exe
```

### 6.4. Utilizar o sistema

Siga as opções apresentadas no menu do terminal. Cadastre os ativos e utilize as opções de consulta, cálculo, ordenação, simulação e relatório. Ao escolher **Sair**, o sistema tenta salvar os dados em `data/carteira.txt`.

Mantenha a pasta `data/` no mesmo diretório de execução do programa para que a leitura e a gravação dos dados funcionem corretamente.

## 7. Desenvolvedores

- Amauri Aquino
- Daniel Carlos Silva
- Dion Dalton Ferreira
- Leandro de Souza Gregorio
- Leonardo Aparecido Rezende Bispo
- Nathan Henrique Silva de Melo

## Estrutura de pastas e arquivos

O projeto utiliza uma arquitetura modular:

- `Src/main.c`: loop do menu principal e chamadas de execução.
- `Src/funcoes.c`: lógica de negócio, cálculos e interações no terminal.
- `Src/modulo.c`: operações de persistência, incluindo leitura e gravação de arquivos.
- `include/funcoes.h`: definição da `struct Ativo`, constantes e protótipos das funções de negócio.
- `include/modulo.h`: protótipos das operações de arquivo.
- `data/carteira.txt`: arquivo de dados persistente, utilizando `;` como separador.

## Compilação

Com o terminal aberto na raiz do projeto, utilize:

```bash
gcc -Wall -Wextra -Iinclude Src/main.c Src/funcoes.c Src/modulo.c -o programa
```
