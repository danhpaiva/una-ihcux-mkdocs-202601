# 🚩 Missão 02: Operação Code Runner (Engenharia de Software via CLI)

Agora que você já domina o terreno (pastas e arquivos), é hora de construir sua primeira estrutura de software profissional. O desafio hoje é provar que você consegue preparar um ambiente de desenvolvimento completo usando apenas o poder do **.NET CLI**.

---

## 🛠️ O Algoritmo da Entrega

### 1. Preparar o Terreno (Repositório)

Crie um novo repositório público no GitHub com o nome:
`una-dotnet-cli-master`

### 2. O Desafio do "Arquiteto de Sistemas"

Esqueça o "Botão Direito > Novo". Siga esta sequência exata no seu terminal:

1. Navegue até sua pasta de projetos (`cd Documentos` ou `cd Desktop`).
2. Crie a pasta do laboratório: `mkdir LabDotnet`.
3. Entre nela: `cd LabDotnet`.
4. **O Grande Salto:** Crie um novo projeto de console chamado "SistemaExpert":
`dotnet new console -n SistemaExpert`
5. Entre na pasta do projeto que o .NET criou: `cd SistemaExpert`.
6. **Compile o projeto:** Execute o comando `dotnet build`.
7. **Rode o programa:** Execute `dotnet run`.

### 3. Registro de Evidência (A "Prova do Crime")

Tire um **print** do seu terminal mostrando:

* O comando `dotnet run` sendo executado.
* A mensagem "Hello, World!" (ou o texto que o template gerou) aparecendo na tela.

### 4. Documentação Técnica (README.md)

No seu repositório, edite o `README.md` com o seguinte template:

```markdown
# 🚀 Minha Primeira Experiência com .NET CLI

Nesta missão, deixei de ser apenas um usuário de pastas e me tornei um desenvolvedor que fala a língua do SDK.

## 🛠️ Comandos de Construção Utilizados
- `dotnet new console`: Para criar a estrutura base do C#.
- `dotnet build`: Para transformar meu código em algo que o PC entende.
- `dotnet run`: Para ver a mágica acontecer.

## 📦 Estrutura Gerada
Arquivos que o .NET criou para mim:
1. `Program.cs`: Onde fica o código.
2. `SistemaExpert.csproj`: As configurações do meu projeto.

## 📸 Evidência de Execução
![Print do terminal rodando o projeto](./minha-evidencia.png)

```

---

## 📂 O que deve conter no seu Repositório?

* **A pasta `SistemaExpert**`: Suba os arquivos `.cs` e `.csproj` (não precisa subir as pastas `bin` e `obj`).
* **minha-evidencia.png**: O print do seu terminal com o `dotnet run`.
* **README.md**: Sua documentação técnica organizada.

---

## 📝 Entrega no Google Classroom

1. Envie o link do repositório `una-dotnet-cli-master`.
2. **Pergunta de Reflexão:** No comentário, responda: *"Qual a diferença visual que você notou entre a pasta que você criou manualmente (mkdir) e a pasta que o comando 'dotnet new' criou?"*

---

## ⚠️ Checklist de Sucesso

!!! check "Critérios de Aceite"
- [ ] O repositório contém o código-fonte C# gerado?
- [ ] A imagem mostra o "Hello World" sendo executado via terminal?
- [ ] O README explica para que serve o comando `dotnet build`?

---

!!! info "Dica de Sênior: O Truque do Explorador"
Quer abrir a pasta do seu projeto no VS Code direto pelo terminal para editar o código? Digite `code .` (isso mesmo, "code" espaço "ponto") dentro da pasta do projeto. Se o VS Code estiver no seu *Path*, ele abrirá instantaneamente!