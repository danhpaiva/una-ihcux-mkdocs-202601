# 🚩 Missão 03: Operação Deep Scan (Heurísticas de UX no Terminal)

Você já sabe criar e rodar. Agora, você vai aprender a **comunicar**. Um software que não diz o que está fazendo deixa o usuário ansioso. Nesta missão, vamos implementar um simulador de varredura de sistema que utiliza a heurística de **Visibilidade do Status**.

---

## 🛠️ O Algoritmo da Entrega

### 1. Evoluindo o Projeto

Não precisamos criar um novo repositório. Use o mesmo `LabDotnet`, mas vamos criar um novo projeto para separar as missões:

1. No terminal, volte para a pasta `LabDotnet`.
2. Crie o novo projeto: `dotnet new console -n ScannerExpert`.
3. Entre na pasta: `cd ScannerExpert`.
4. Abra no VS Code: `code .`.

### 2. Implementando o Status do Sistema

Substitua o conteúdo do `Program.cs` por este código. Note o uso de *loops* e *sleep* para simular o tempo de resposta:

```csharp
using System;
using System.Threading;

// --- IHC: Visibilidade do Status do Sistema ---
Console.Clear();
Console.ForegroundColor = ConsoleColor.Cyan;
Console.WriteLine("=== SISTEMA EXPERT: MÓDULO DE DEEP SCAN ===");
Console.ResetColor();

Console.WriteLine("\nIniciando análise de hardware...");

// Simulando carregamento com feedback visual
string[] fases = { "Verificando CPU...", "Lendo Memória RAM...", "Sincronizando SDK...", "Finalizando..." };

foreach (string fase in fases)
{
    Console.Write($"\r[ANALISANDO] {fase}");
    // Simula um processamento de 1.5 segundos
    Thread.Sleep(1500); 
}

Console.ForegroundColor = ConsoleColor.Green;
Console.WriteLine("\n\n✅ ANALISE CONCLUÍDA COM SUCESSO!");
Console.ResetColor();

Console.WriteLine("-------------------------------------------");
Console.WriteLine("Resultado: Sistema pronto para o deploy.");
Console.WriteLine("-------------------------------------------");

Console.WriteLine("\n[Pressione qualquer tecla para encerrar o log]");
Console.ReadKey();

```

---

## 📸 Registro de Evidência

Tire um **print do terminal no momento em que a análise estiver acontecendo** (mostrando a mensagem de `[ANALISANDO]`). 
Isso prova que seu sistema está informando o status em tempo real.

---

## 📝 Entrega e Reflexão (Google Classroom)

1. Adicione a pasta `ScannerExpert` ao seu repositório `una-dotnet-cli-master`.
2. **Pergunta de Reflexão (IHC):** > "Imagine que o programa demorasse 10 segundos para finalizar, mas ficasse com a tela totalmente em branco, sem as mensagens de '[ANALISANDO]'. 
Como isso afetaria a percepção do usuário? Qual das 10 Heurísticas de Nielsen resolve esse problema?"

---

## ⚠️ Checklist de Sucesso

!!! check "Critérios de Aceite"

* [ ] O repositório contém o novo projeto `ScannerExpert`.
* [ ] O código utiliza `Thread.Sleep` para criar o intervalo de tempo necessário para o feedback.
* [ ] O README foi atualizado mencionando a importância da Visibilidade do Status.

---

!!! info "Dica de Sênior: O caractere mágico `\r`"
No código acima, usamos o `\r` (Carriage Return). 

Ele faz o cursor voltar para o início da linha sem pular para a próxima. 

É assim que criamos barras de progresso e contadores que se atualizam no mesmo lugar no terminal!

