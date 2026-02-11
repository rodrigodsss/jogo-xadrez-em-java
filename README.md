#♟️ Chess Engine em Java

Arquitetura em Camadas | Check & Checkmate | Console Application


📌 Visão Geral

Este projeto implementa um motor de xadrez em Java, executado via console, com foco em:

Programação Orientada a Objetos

Modelagem de domínio

Separação de responsabilidades

Validação robusta de regras

Controle consistente de estado

A aplicação simula regras reais do jogo incluindo check e checkmate, utilizando abordagem de simulação reversível de movimentos.

🧠 Destaque Técnico

O sistema implementa:

✔ Controle de turno (WHITE / BLACK)

✔ Validação de jogadas legais

✔ Prevenção de movimentos inválidos

✔ Impedimento de jogadas que deixam o próprio rei em CHECK

✔ Captura de peças

✔ Destaque visual de movimentos possíveis

✔ Detecção automática de CHECK

✔ Algoritmo completo de CHECKMATE via simulação

🔎 Estratégia para Checkmate

O algoritmo:

Detecta se o rei está sob ataque.

Itera sobre todos os movimentos possíveis do jogador.

Simula cada jogada (makeMove).

Reverte o estado (undoMove).

Confirma se existe saída legal.

Caso contrário → CHECKMATE.

Essa abordagem demonstra controle rigoroso de estado e modelagem consistente de regras de negócio.

🏗️ Arquitetura do Projeto
src/
 ├── application/
 │   ├── Program.java
 │   └── UI.java
 │
 ├── Chess/
 │   ├── ChessMatch.java
 │   ├── ChessPiece.java
 │   ├── ChessPosition.java
 │   ├── ChessException.java
 │   ├── Color.java
 │   └── pieces/
 │       ├── King.java
 │       └── Rook.java
 │
 └── boardgame/
     ├── Board.java
     ├── Piece.java
     ├── Position.java
     └── BoardException.java

Separação de Camadas
Camada	Responsabilidade
boardgame	Infraestrutura genérica de tabuleiro
Chess	Regras de negócio do xadrez
application	Interface e fluxo de execução

Essa arquitetura permite fácil extensão para novas peças e regras sem comprometer o design.

⚙️ Tecnologias Utilizadas

Java 17+

Programação Orientada a Objetos

Estruturas de Dados (Matriz)

Tratamento de Exceções

GitHub Actions (CI)

Arquitetura modular

▶️ Como Executar
Build Limpo
javac -d bin (Get-ChildItem -Recurse -Filter *.java src | ForEach-Object FullName)

Executar
java -cp bin application.Program

🎮 Como Jogar

Digite as posições no formato:

Source: e2
Target: e4


Formato válido:

[a-h][1-8]


Exemplo:

Source: c2
Target: c3


O sistema retorna mensagens claras em caso de erro de regra.

📈 Evoluções Futuras

Implementação de todas as peças

Promoção de peão

Roque

En passant

Testes automatizados (JUnit)

CI avançado

Interface gráfica (JavaFX)

🎯 Competências Demonstradas

Este projeto evidencia:

Modelagem de regras complexas

Pensamento algorítmico

Arquitetura limpa

Controle consistente de estado

Aplicação sólida de OOP

Engenharia de software estruturada

👨‍💻 Autor

Rodrigo Silva
QA Engineer | DevOps | Engenharia de Software

Projeto desenvolvido como exercício de arquitetura e modelagem de domínio em Java.
