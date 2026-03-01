# 🚩 Missão 04: Operação Escudo Digital (Prevenção de Erros e Robustez)

Um software que "quebra" e mostra uma tela de erro técnica (aquela sopa de letrinhas vermelhas) é o pesadelo de qualquer usuário. 
De acordo com a **5ª Heurística de Nielsen**, o melhor design previne problemas antes mesmo que eles ocorram.

Hoje, você vai construir um sistema que sobrevive à "falha humana".

---

## 🛠️ O Algoritmo da Entrega

### 1. Preparar o Terreno (Novo Repositório)

Crie um novo repositório público no GitHub com o nome:
`una-ihcux-lista04`

### 2. O Desafio do "Sistema Inquebrável"

Siga os comandos no terminal:

1. Navegue até sua pasta de projetos (`cd LabDotnet`).
2. Crie o novo projeto de console:
`dotnet new console -n SistemaRobusto`
3. Entre na pasta: `cd SistemaRobusto`.
4. Abra no VS Code: `code .`.

### 3. Implementando a Prevenção de Erros

Substitua o conteúdo do `Program.cs` por este código. 
Observe como usamos o bloco `try-catch` para capturar o erro antes dele fechar o programa:

```csharp
using System;

// --- IHC: Prevenção de Erros (5ª Heurística de Nielsen) ---
Console.Clear();
Console.WriteLine("=== SISTEMA DE CADASTRO EXPERT ===");

try 
{
    Console.Write("\nDigite sua idade para continuar: ");
    string entrada = Console.ReadLine();

    // Tentativa de conversão (Onde o erro pode acontecer)
    int idade = int.Parse(entrada);

    Console.ForegroundColor = ConsoleColor.Green;
    Console.WriteLine($"\n✅ Acesso liberado! Idade {idade} registrada com sucesso.");
}
catch (FormatException)
{
    // Feedback amigável em vez de um erro técnico
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine("\n[ERRO DE UX]: Você digitou letras em um campo que só aceita números!");
    Console.WriteLine("DICA: Tente novamente inserindo apenas algarismos (ex: 25).");
}
finally
{
    Console.ResetColor();
    Console.WriteLine("\n-------------------------------------------");
    Console.WriteLine("O sistema encerrou a tentativa de operação.");
    Console.WriteLine("Pressione qualquer tecla para sair...");
    Console.ReadKey();
}

```

---

## 📸 Registro de Evidência (A "Prova do Crime")

Desta vez, você precisa de **dois prints**:

1. **Print 01 (Caminho Feliz):** Você digitando um número e o sistema dando sucesso.
2. **Print 02 (Caminho do Erro):** Você digitando letras (ex: "vinte") e o sistema exibindo a mensagem de erro amigável que você programou.

---

## 📂 O que deve conter no seu Repositório?

* **A pasta `SistemaRobusto`**: Arquivos `.cs` e `.csproj`.
* **evidencia-sucesso.png** e **evidencia-erro.png**.
* **README.md**: Explique o que é o `try-catch` e como ele se conecta com a Prevenção de Erros.

---

## 📝 Entrega no Google Classroom

1. Envie o link do repositório `una-ihcux-lista04`.
2. **Pergunta de Reflexão (IHC):** > "Quando o programa 'crasha' e fecha sozinho por um erro de digitação, qual é o sentimento do usuário? Como o tratamento de erros (mensagens amigáveis) ajuda na confiança que o usuário tem no software?"

---

## ⚠️ Checklist de Sucesso

!!! check "Critérios de Aceite"

* [ ] O repositório `una-ihcux-lista04` está público?
* [ ] O código captura o erro de digitação sem fechar o terminal de forma abrupta?
* [ ] As mensagens de erro usam cores (`ConsoleColor`) para destacar o problema?

---

!!! info "Dica de Sênior: O poder do TryParse"
O `try-catch` é excelente, mas desenvolvedores seniores muitas vezes usam o método `int.TryParse()`. 
Ele tenta converter o número e, se não conseguir, ele apenas devolve "falso" em vez de gerar uma exceção. 
É uma forma ainda mais elegante de prevenir erros!