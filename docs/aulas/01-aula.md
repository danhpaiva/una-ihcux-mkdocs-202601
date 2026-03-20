# ⚡ Aula 01: Dominando o Terminal (A Linha de Comando)

Esqueça o mouse por alguns minutos. 

Como desenvolvedor, sua produtividade vai saltar de nível quando você aprender a falar diretamente com o sistema operacional. 

O **Terminal** não é coisa de filme de hacker dos anos 90; é a ferramenta de trabalho mais poderosa do seu arsenal.

---

## 🖥️ O que é o Terminal (Prompt de Comando)?

Se a Interface Gráfica (Windows Explorer) é o "painel de controle" com botões e ícones, o **Terminal** é o "motor" por baixo do capô. Nele, enviamos comandos de texto que o sistema executa instantaneamente.

No Windows, temos três opções principais:

1. **CMD (Prompt de Comando):** O clássico, vindo do antigo MS-DOS.
2. **PowerShell:** Uma versão moderna e muito mais poderosa, usada por administradores de sistemas.
3. **Terminal do Windows:** Um aplicativo moderno que agrupa todos os outros em abas (o favorito dos devs).

---

## 📍 O Conceito de "Diretório Atual"

No Windows Explorer, você vê onde está pelas pastas abertas. No Terminal, você vê pelo **Caminho (Path)**.

* `C:\Users\Joao>` significa que você está "dentro" da pasta do usuário João.
* Toda ação que você fizer (criar arquivo, apagar, listar) acontecerá **dentro** dessa pasta, a menos que você mude de lugar.

---

## 🛠️ Comandos de Sobrevivência (O "Be-a-Bá")

Aqui estão os comandos que você usará 90% do tempo. Abra o seu CMD (aperte a tecla `Windows`, digite `cmd` e dê `Enter`) e teste agora:

| Objetivo           | Comando (CMD/PS)           | O que ele faz?                                       |
| ------------------ | -------------------------- | ---------------------------------------------------- |
| **Listar**         | `dir`                      | Mostra todos os arquivos e pastas onde você está.    |
| **Navegar**        | `cd nome_da_pasta`         | Entra em uma pasta específica.                       |
| **Voltar**         | `cd ..`                    | Sai da pasta atual e volta para a "pasta pai".       |
| **Limpar**         | `cls`                      | Limpa toda a bagunça da tela (Clear Screen).         |
| **Criar Pasta**    | `mkdir nome_pasta`         | Cria um novo diretório (Make Directory).             |
| **Mover/Renomear** | `move antigo.txt novo.txt` | Move arquivos ou muda o nome deles.                  |
| **Apagar**         | `del arquivo.txt`          | Deleta um arquivo (Cuidado! Não vai para a lixeira). |

---

## 🚀 Super Poderes do Teclado

Como um desenvolvedor sênior, eu raramente digito o nome inteiro de uma pasta. Use estes atalhos:

* **⇥ Tab (A Tecla Mágica):** Comece a digitar o nome de uma pasta e aperte `Tab`. O terminal autocompleta para você!
* **Seta para Cima (↑):** Recupera o último comando que você digitou. Útil para não repetir trabalho.
* **CTRL + C:** Interrompe um comando que está travado ou rodando em loop.

---

## 🤖 Desafio Prático: Operação "Nuvem Local"

Vamos simular a organização de um projeto real usando apenas o teclado. Siga os passos:

1. Abra o CMD.
2. Digite `cd Desktop` para ir para a sua área de trabalho.
3. Crie uma pasta para a nossa disciplina: `mkdir laboratorios-ihcux`.
4. Entre nela: `cd laboratorios-ihcux`.
5. Crie duas subpastas de uma vez: `mkdir aula01 aula02`.
6. Confirme se elas foram criadas digitando `dir`.

---

## ⚠️ Cuidado: O Poder traz Responsabilidade

!!! danger "Comandos Perigosos"
Evite digitar comandos que você encontrou na internet sem entender o que fazem, especialmente os que envolvem `del /s /q` ou que tentam apagar pastas dentro de `C:\Windows`. O terminal não pergunta "Tem certeza?" como o Windows faz.

---

## 📝 Atividade de Fixação

??? abstract "Exercício 1: O Detetive de Arquivos"
Navegue até a sua pasta de `Documentos` via Terminal e use o comando `dir`. Tente encontrar um arquivo específico e anote o tamanho dele (que aparece ao lado do nome).

??? abstract "Exercício 2: Hierarquia de Pastas"
Crie a seguinte estrutura usando apenas o comando `mkdir` e `cd`:
`Projetos > Exercicios > Logica`.
Depois, tente voltar para a pasta `Projetos` usando apenas um comando (`cd ../..`).

??? abstract "Exercício 3: Versão dos Softwares"
Muitos programas instalados no seu PC só mostram a "cara" no terminal. Tente digitar estes comandos e veja se eles estão instalados (eles devem retornar a versão):
- `dotnet --version`
- `git --version`
- `node -v`

---


## 📝 Entrega no Google Classroom

Crie um repositório público no GitHub com o nome:
`una-ihcux-pratica01`

0. Documente o seu readme com os principais comandos utilizados na aula.
1. Copie a URL do repositório `una-ihcux-pratica01`.
2. Cole no campo da atividade correspondente.

---

!!! tip "Próximos Passos"
Agora que você sabe navegar como um profissional, vamos aprender a integrar o **Git** diretamente com esses comandos. 
Na próxima aula: **Controle de Versão via Linha de Comando!**
