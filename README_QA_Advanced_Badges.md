# ♟️ Chess Engine --- QA-Oriented Architecture

![Build](https://github.com/rodrigodsss/Jogo-Xadrez-Em-Java/actions/workflows/build.yml/badge.svg)
![Java](https://img.shields.io/badge/Java-17-orange?logo=java)
![Architecture](https://img.shields.io/badge/architecture-layered-blue)
![Focus](https://img.shields.io/badge/focus-QA%20Automation-critical)
![Status](https://img.shields.io/badge/status-active-success)
![License](https://img.shields.io/badge/license-MIT-blue)

------------------------------------------------------------------------

## 📌 Sobre o Projeto

Este projeto implementa um **motor de xadrez em Java (console)** com
foco em qualidade, validação de regras e arquitetura modular.

Mais do que um jogo, trata-se de um exercício prático de engenharia
orientada à qualidade, aplicando:

-   Programação Orientada a Objetos
-   Modelagem de domínio
-   Separação de responsabilidades
-   Controle rigoroso de estado
-   Validação robusta de regras

------------------------------------------------------------------------

## 🎯 Perspectiva de QA Automation

O projeto foi estruturado considerando princípios fundamentais de QA:

-   ✔ Validação de entradas
-   ✔ Tratamento de exceções
-   ✔ Integridade de estado da aplicação
-   ✔ Prevenção de regressões lógicas
-   ✔ Simulação de cenários críticos
-   ✔ Bloqueio de jogadas inválidas
-   ✔ Proteção contra "self-check"

------------------------------------------------------------------------

## 🧠 Algoritmo de Checkmate

A detecção de checkmate utiliza simulação reversível:

1.  Detecta se o rei está em CHECK.
2.  Itera sobre todos os movimentos possíveis.
3.  Simula cada jogada.
4.  Reverte o estado.
5.  Verifica se existe saída válida.
6.  Caso não exista → CHECKMATE.

Essa abordagem demonstra pensamento analítico, controle transacional e
validação de regras críticas.

------------------------------------------------------------------------

## 🏗️ Arquitetura

    src/
     ├── application/   → Interface e fluxo
     ├── Chess/         → Engine de regras
     └── boardgame/     → Infraestrutura genérica

### Separação de Camadas

  Camada        Responsabilidade
  ------------- ---------------------------------
  boardgame     Estrutura genérica de tabuleiro
  Chess         Regras de negócio
  application   Interface e execução

------------------------------------------------------------------------

## ⚙️ Tecnologias

-   Java 17+
-   OOP
-   Estruturas de Dados (Matriz)
-   Tratamento de Exceções
-   GitHub Actions (CI)
-   Arquitetura em Camadas

------------------------------------------------------------------------

## ▶️ Execução

### Compilar

``` bash
javac -d bin (Get-ChildItem -Recurse -Filter *.java src | ForEach-Object FullName)
```

### Executar

``` bash
java -cp bin application.Program
```

------------------------------------------------------------------------

## 🔬 Competências Demonstradas

-   Modelagem de regras complexas
-   Pensamento algorítmico
-   Controle consistente de estado
-   Arquitetura organizada
-   Engenharia orientada à qualidade

------------------------------------------------------------------------

## 🚀 Próximos Passos

-   Implementar testes automatizados (JUnit)
-   Adicionar cobertura de código
-   Integrar Codecov
-   Integrar SonarCloud
-   Criar cenários BDD

------------------------------------------------------------------------

## 👨‍💻 Autor

Rodrigo Silva\
QA Engineer \| DevOps \| Engenharia de Software
