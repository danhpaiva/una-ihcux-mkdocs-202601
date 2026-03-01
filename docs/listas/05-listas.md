# 🚩 05: Operação Global Exchange (O Grand Finale)

Chegou a hora de consolidar seus conhecimentos. 
Você vai construir um **Conversor de Moedas** que não apenas faz contas, mas entrega uma experiência de usuário (UX) de alto nível no terminal. 
O foco aqui é a **Robustez** e o **Feedback Realista**.

---

## 🛠️ O Algoritmo da Entrega

### 1. Preparar o Terreno (Repositório Final)

Crie o último repositório desta jornada no GitHub:
`una-ihcux-lista05`

### 2. O Desafio do "Sistema Financeiro"

Siga os comandos:

1. Navegue até sua pasta de projetos (`cd LabDotnet`).
2. Crie o projeto: `dotnet new console -n ConversorExpert`.
3. Entre na pasta: `cd ConversorExpert`.
4. Abra no VS Code: `code .`.

### 3. O Código Mestre

Substitua o conteúdo do `Program.cs` por este sistema completo:

```csharp
using System;
using System.Threading;

// --- PROJETO FINAL: IHC & UX NO CONSOLE ---
Console.Clear();
Console.ForegroundColor = ConsoleColor.Yellow;
Console.WriteLine("===========================================");
Console.WriteLine("       GLOBAL EXCHANGE - CONVERSOR v1.0    ");
Console.WriteLine("===========================================");
Console.ResetColor();

try 
{
    // --- Entrada de Dados (UX de Instrução) ---
    Console.Write("\nDigite o valor em REAIS (R$): ");
    string entrada = Console.ReadLine();
    double valorReais = double.Parse(entrada);

    Console.Write("Digite a cotação do DÓLAR hoje (ex: 5,20): ");
    double cotacaoDolar = double.Parse(Console.ReadLine());

    // --- Heurística 01: Visibilidade do Status ---
    Console.WriteLine("\n[SISTEMA]: Conectando ao Banco Central...");
    Thread.Sleep(1000);
    Console.Write("[SISTEMA]: Calculando taxas");
    for(int i = 0; i < 3; i++) { Thread.Sleep(500); Console.Write("."); }
    
    // --- Lógica de Negócio ---
    double resultado = valorReais / cotacaoDolar;

    // --- Heurística 08: Estética e Design Minimalista ---
    Console.ForegroundColor = ConsoleColor.Green;
    Console.WriteLine("\n\n-------------------------------------------");
    Console.WriteLine($"VALOR CONVERTIDO: $ {resultado:F2} (Dólares)");
    Console.WriteLine("-------------------------------------------");
    Console.ResetColor();
}
catch (Exception)
{
    // --- Heurística 05: Prevenção de Erros ---
    Console.BackgroundColor = ConsoleColor.Red;
    Console.ForegroundColor = ConsoleColor.White;
    Console.WriteLine("\n\n [ERRO CRÍTICO] ");
    Console.ResetColor();
    Console.WriteLine("Entrada inválida! Use apenas números e vírgula para decimais.");
}
finally
{
    Console.WriteLine("\nObrigado por usar o Global Exchange. Volte sempre!");
    Console.WriteLine("Pressione qualquer tecla para finalizar...");
    Console.ReadKey();
}

```

---

## 📸 Registro de Evidência

Tire um **print** do terminal mostrando uma **conversão feita com sucesso**. 
O print deve mostrar as mensagens de carregamento ("Conectando ao Banco Central...") e o resultado final formatado.

---

## 📂 Estrutura do Repositório

* **A pasta `ConversorExpert**`: Código fonte completo.
* **evidencia-final.png**: Print do sistema funcionando.
* **README.md**: Um resumo de todas as heurísticas que você aplicou (Status, Prevenção de Erros e Estética).

---

## 📝 Entrega no Google Classroom

1. Envie o link do repositório `una-ihcux-lista05`.
2. **Reflexão de Encerramento:** > "Após passar por essas 4 missões, como a sua visão sobre 'apenas escrever código' mudou ao considerar a experiência de quem vai usar o seu programa?"

---

## ⚠️ Checklist de Sucesso

!!! check "Critérios de Aceite"

* [ ] O sistema utiliza `Thread.Sleep` para dar visibilidade de status?
* [ ] O sistema utiliza `try-catch` para evitar o fechamento por erro de digitação?
* [ ] O valor final é exibido com apenas duas casas decimais (`:F2`)?
* [ ] O README está organizado e profissional?

---

!!! info "Dica de Sênior: A Evolução Contínua"
Em um cenário real, você não "fixaria" a cotação via teclado, mas sim consumiria uma **API de Economia** para pegar o valor do dólar em tempo real. 
Você acabou de dar o primeiro passo para criar sistemas que o mercado realmente utiliza!