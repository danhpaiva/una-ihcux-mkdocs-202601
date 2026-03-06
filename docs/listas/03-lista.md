# 🚩 Missão 03: Operação Deep Scan (Heurísticas de UX no Terminal)

Você já sabe criar e rodar. 
Agora, você vai aprender a **comunicar**. 

A 1ª Heurística de Nielsen (**Visibilidade do Status do Sistema**) diz que o software deve sempre manter o usuário informado sobre o que está acontecendo, através de feedback apropriado e em tempo razoável.

Nesta missão, vamos implementar um simulador de varredura de sistema que utiliza essa heurística para evitar que o usuário ache que o programa "travou".

---

## 🛠️ O Algoritmo da Entrega

### 1. Preparar o Terreno (Novo Repositório)

Desta vez, crie um novo repositório público no GitHub com o nome:
`una-ihcux-lista03`

### 2. O Desafio do "Scanner de Sistema"

Siga a sequência no seu terminal:

1. Navegue até sua pasta de projetos (`cd LabDotnet`)
2. Crie o novo projeto de console:
`dotnet new console -n ScannerExpert`
3. Entre na pasta: `cd ScannerExpert`
4. Abra no VS Code: `code .`

### 3. Implementando a Visibilidade de Status

Substitua o conteúdo do `Program.cs` por este código. 
Note o uso de *loops* e o comando `Thread.Sleep` para simular o tempo de processamento:

```csharp
using System;
using System.Threading;

// --- UX / IHC: Visibilidade do Status do Sistema ---
Console.Clear();
Console.ForegroundColor = ConsoleColor.Cyan;
Console.WriteLine("=== SISTEMA EXPERT: MÓDULO DE DEEP SCAN ===");
Console.ResetColor();

Console.WriteLine("\nIniciando análise de hardware...");

// Lista de tarefas para simular o progresso
string[] fases = { 
    "Verificando CPU...", 
    "Lendo Memória RAM...", 
    "Sincronizando SDK...", 
    "Validando Permissões...",
    "Finalizando..." 
};

foreach (string fase in fases)
{
    // O caractere \r faz o cursor voltar ao início da linha sem pular para a próxima
    Console.Write($"\r[PROCESSANDO] {fase}   ");
    
    // Simula um processamento de 1.5 segundos (1500 milissegundos)
    Thread.Sleep(1500); 
}

Console.ForegroundColor = ConsoleColor.Green;
Console.WriteLine("\n\n✅ ANÁLISE CONCLUÍDA COM SUCESSO!");
Console.ResetColor();

Console.WriteLine("-------------------------------------------");
Console.WriteLine("Resultado: Sistema pronto para o deploy.");
Console.WriteLine("-------------------------------------------");

Console.WriteLine("\n[Pressione qualquer tecla para encerrar o log]");
Console.ReadKey();

```

---

## 📸 Registro de Evidência (A "Prova do Crime")

Tire um **print do terminal no momento em que a análise estiver acontecendo** (mostrando a mensagem de `[PROCESSANDO]`). 

Isso prova que seu sistema está informando o status em tempo real conforme a heurística de Nielsen.

---

## 📂 O que deve conter no seu Repositório?

* **A pasta `ScannerExpert**`: Arquivos `.cs` e `.csproj`.
* **minha-evidencia.png**: O print do terminal durante o "carregamento".
* **README.md**: Documentação explicando que este projeto aplica a **1ª Heurística de Nielsen**.

---

## 📝 Entrega no Google Classroom

1. Envie o link do repositório `una-ihcux-lista03`.
2. **Pergunta de Reflexão (IHC):** > "Se o programa demorasse 10 segundos para finalizar, mas ficasse com a tela totalmente parada (em branco), sem as mensagens de '[PROCESSANDO]', o que o usuário provavelmente pensaria? 
Como a visibilidade de status melhora a Experiência do Usuário (UX)?"

---

## ⚠️ Checklist de Sucesso

!!! check "Critérios de Aceite"

* [ ] O repositório `una-ihcux-lista03` foi criado corretamente?
* [ ] O código utiliza `Thread.Sleep` para criar o intervalo de tempo necessário para o feedback?
* [ ] O print mostra o programa no meio do processo de "varredura"?

---

!!! info "Dica de Sênior: O segredo do feedback visual"
No código acima, usamos o `\r` (Carriage Return). 
Ele é um "truque" de interface CLI que permite que a mesma linha seja sobrescrita. 
Sem ele, o terminal ficaria poluído com várias linhas repetidas. 
Pequenos detalhes técnicos fazem uma grande diferença na **UX do Desenvolvedor**!
