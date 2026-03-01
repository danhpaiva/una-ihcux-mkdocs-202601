# 🚀 Aula 02: O Poder do .NET CLI (Command Line Interface)

Na aula anterior, aprendemos a navegar nas pastas. Agora, vamos aprender a **construir**. O `dotnet CLI` é a interface de linha de comando que nos permite criar, compilar e rodar aplicações .NET em qualquer sistema (Windows, Linux ou macOS).

Se você pretende trabalhar com Docker, Nuvem (Cloud) ou Automação, dominar esses comandos é obrigatório.

---

## 🛠️ O que é o SDK do .NET?

Para desenvolver, não basta ter o "Runtime" (que apenas executa o app); precisamos do **SDK (Software Development Kit)**. Ele traz o comando `dotnet`, que é o nosso ponto de entrada para tudo.

Imagine o `dotnet` como um mestre de obras: você dá a ordem, e ele chama os compiladores e bibliotecas necessárias para entregar o prédio (seu software) pronto.

---

## 📍 Verificando o Ambiente

Antes de começar, precisamos garantir que o mestre de obras está em casa. No seu terminal, digite:

```bash
dotnet --info

```

Este comando mostra a versão instalada, o sistema operacional e quais "Runtimes" estão presentes. Se aparecer um erro de "comando não encontrado", o SDK não foi instalado corretamente.

---

## 🏗️ Comandos Essenciais do Dia a Dia

Aqui está a sua "colinha" de comandos .NET. Quase todos seguem o padrão: `dotnet [verbo] [argumento]`.

| Objetivo             | Comando                       | O que ele faz?                                                             |
| -------------------- | ----------------------------- | -------------------------------------------------------------------------- |
| **Listar Templates** | `dotnet new list`             | Mostra todos os tipos de projetos que você pode criar (Console, Web, API). |
| **Criar Projeto**    | `dotnet new console -n MyApp` | Cria uma nova aplicação de console na pasta "MyApp".                       |
| **Restaurar**        | `dotnet restore`              | Baixa as bibliotecas (pacotes NuGet) que o projeto precisa.                |
| **Compilar**         | `dotnet build`                | Verifica se há erros no código e gera o executável.                        |
| **Executar**         | `dotnet run`                  | Compila (se necessário) e roda o programa imediatamente.                   |
| **Limpar**           | `dotnet clean`                | Apaga os arquivos temporários da última compilação.                        |

---

## 📂 Entendendo a Estrutura de Arquivos

Ao criar um projeto com `dotnet new console`, dois arquivos principais surgem:

1. **`NomeDoProjeto.csproj`**: O arquivo de "receita". Ele diz quais bibliotecas o projeto usa e qual versão do .NET estamos usando. (É um XML, não mude nada lá a menos que saiba o que está fazendo!).
2. **`Program.cs`**: Onde a mágica acontece. É o seu código-fonte C#.

---

## 🤖 Desafio Prático: Minha Primeira App "Pro"

Vamos criar um projeto do zero, sem tocar no mouse, seguindo o padrão de organização de mercado:

1. Abra o terminal na sua pasta de estudos.
2. Crie uma pasta para o projeto: `mkdir LabDotnet`.
3. Entre nela: `cd LabDotnet`.
4. **Crie o projeto:** `dotnet new console -n OlaMundo`.
5. **Veja o que foi criado:** `dir`.
6. Navegue pra dentro da pasta com o cd OlaMundo.
7. **Execute o código padrão:** `dotnet run`.
* *(Dica: Você verá o clássico "Hello, World!" no terminal).*



---

## 💡 Dica de Sênior: O comando `watch`

Durante o desenvolvimento, é chato ter que digitar `dotnet run` toda vez que você muda uma vírgula no código. Use o **Hot Reload**:

```bash
dotnet watch run

```

O terminal ficará "vigiando" seus arquivos. Assim que você salvar uma alteração no VS Code ou Bloco de Notas, o .NET reinicia a aplicação automaticamente. **Produtividade pura!**

---

## 📝 Atividade de Fixação

??? abstract "Exercício 1: Explorando Templates"
Use o comando `dotnet new list`. Tente identificar qual é o "Short Name" (nome curto) para criar uma **Web API** e para criar um projeto de **Testes Unitários (xUnit)**.

??? abstract "Exercício 2: Mudando a Saída"
Crie um novo projeto de console chamado `Calculadora`, mas desta vez force-o a usar uma versão específica do .NET (se você tiver várias) usando o parâmetro `-f`. Exemplo: `dotnet new console -n Calculadora -f net8.0`.

??? abstract "Exercício 3: O arquivo de Projeto"
Abra o arquivo `.csproj` criado no Exercício 2 usando o comando `notepad Calculadora.csproj` no terminal. Localize a tag `<TargetFramework>` e veja se ela corresponde à versão que você esperava.

---

## 📝 Repositório

Crie um repositório público no GitHub com o nome:
`una-ihcux-pratica02`

0. Suba seu projeto de OlaMundo feito em C#.
1. Copie a URL do repositório `una-ihcux-pratica02`.
2. Cole no campo da atividade correspondente.

Crie um repositório público no GitHub com o nome:
`una-ihcux-calculadorafea`

0. Suba seus arquivos para o seu repositorio.
1. Copie a URL do repositório `una-ihcux-calculadora`.
2. Cole no campo da atividade correspondente.

!!! tip "Próximos Passos"
Agora que você domina o CLI do .NET, o próximo passo é aprender a gerenciar pacotes externos para não precisar "reinventar a roda". Na próxima aula: **Gerenciamento de Pacotes com NuGet via CLI!**