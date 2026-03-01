# 📚 Programação e IHC: Lista de Exercícios I

Esta lista de exercício deve:

* Ser realizada em equipes de até **05 alunos**.
* Ser entregue no prazo proposto.
* Ter os algoritmos pedidos escritos em linguagem **C# .NET** do tipo **Console**.
* Ter todos os algoritmos devidamente indentados.
* **Atenção:** Embora o trabalho seja em equipe, todas as entregas na plataforma são **individuais**.

---

## 🍕 Exercício Prático: O "Caos na Cantina"

**Cenário:**
A cantina da universidade lançou um sistema console para agilizar os pedidos. 
Porém, os alunos estão reclamando que o sistema é uma "armadilha":

1. Se você digita algo errado, ele fecha (crash);
2. Se você se arrepende de um item, não tem como voltar;
3. O sistema é "mudo" e não explica o que está acontecendo.

**O Problema (Código Base):**
Atualmente, o sistema é linear e frágil. Se o usuário digitar "dois" em vez de `2`, o programa explode. Se ele escolher o lanche errado, precisa fechar o terminal e começar do zero.

### 🎯 Sua Missão:

Você deve criar uma aplicação console em C# (.NET) que resolva esse fluxo de pedido, aplicando pelo menos **3 Heurísticas de Nielsen** (princípios de design de interface) adaptadas para o terminal.

### Requisitos Técnicos:

1. **Heurística #1 (Visibilidade do Status):** Implemente indicadores que mostrem onde o usuário está.
*Exemplo:* `[Passo 1 de 3] Seleção de Item` ou `[=======] 100% Pedido Processado`.
2. **Heurística #3 (Controle e Liberdade):** O aluno deve conseguir digitar `voltar` em qualquer etapa para corrigir a informação anterior, ou `cancelar` para abortar tudo e limpar a tela.
3. **Heurística #9 (Ajuda e Erros):** O sistema deve ser amigável. Se o aluno digitar um código inexistente, o sistema deve dizer exatamente o que houve:
*"Código 99 não encontrado. Nossos códigos vão de 1 a 10. Tente novamente."*

---

## 📝 O que deve ser entregue:

1. O **código fonte (Program.cs)** funcional e sem erros de compilação.
2. Um **comentário no topo do código** identificando as linhas onde cada heurística foi aplicada.
3. A **URL do seu repositório do GitHub** contendo o código.
* **Nome do repositório:** `ihcux-lista-04`



---

## 💡 Exemplo de Inspiração (O "Pulo do Gato")

Para a **Heurística de Controle e Liberdade**, pensem em usar um laço `while` para cada pergunta. Se a entrada for inválida ou o comando for de "voltar", você não avança para a próxima variável.

**Dica do Professor:** Menos é mais. Não se preocupe com estética visual complexa agora (ASCII Art, etc). Foque na **lógica de interação**. O console pode ser preto e branco, mas a experiência do usuário deve ser clara e segura!

---

**Entregue a URL do seu repositório na plataforma indicada em aula.**