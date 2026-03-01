# 🎨 Aula 03: Prototipagem de Baixa Fidelidade com Miro

Na aula anterior, aprendemos a usar o terminal para construir o esqueleto do nosso software. <br>
Agora, vamos aprender a desenhar o **esqueleto da experiência do usuário (UX)**. <br>
Antes de escrever uma única linha de C#, precisamos validar a ideia. É aqui que entra o **Wireframe**.

O Miro é nossa mesa de desenho infinita para criar protótipos de baixa fidelidade (Lo-Fi) de forma colaborativa e rápida.

---

## 🛠️ O que é Baixa Fidelidade (Lo-Fi)?

Um protótipo de baixa fidelidade não se preocupa com cores, fontes perfeitas ou imagens em alta resolução. <br>
Ele foca na **estrutura** e na **funcionalidade**.

Imagine o protótipo como a planta azul de uma casa: você não precisa saber a cor da cortina para saber onde a porta da cozinha deve ficar.

**Por que usar o Miro?**

* **Velocidade:** Arrastar e soltar formas é mais rápido que codar um CSS.
* **Colaboração:** Múltiplas pessoas editando ao mesmo tempo (Pair Design!).
* **Feedback Antecipado:** Errar no Miro custa zero centavos; errar na produção custa o projeto.

---

## 📍 Preparando a Tela de Desenho

Antes de riscar, configure seu ambiente no Miro para ganhar produtividade:

1. **Wireframe Library:** No menu lateral esquerdo, clique em "More apps" (os três pontinhos) e procure por **Wireframes**.
2. **Frames:** Pressione `F` para criar um quadro. Escolha o tamanho (Browser, iPhone, etc.). 
3. Isso mantém seu design organizado.
4. **Grids:** Ative a grade para ajudar a alinhar os componentes.

---

## 🏗️ Elementos Essenciais do Wireframe

Quase todos os protótipos Lo-Fi usam os mesmos componentes básicos. No Miro, você os encontra na barra de ferramentas:

| Elemento                | Representação no Miro  | Uso Comum                                                            |
| ----------------------- | ---------------------- | -------------------------------------------------------------------- |
| **Box (Retângulo)**     | Shape                  | Representa containers, imagens ou seções da página.                  |
| **Placeholder**         | Retângulo com um "X"   | Indica onde ficará uma imagem ou logo (sem precisar da imagem real). |
| **Texto (Lorem Ipsum)** | Text Tool              | Títulos e parágrafos falsos para testar o layout.                    |
| **Botões**              | Rounded Rectangle      | Chamadas para ação (CTA) como "Entrar" ou "Salvar".                  |
| **Input Fields**        | Rectangle (borda fina) | Campos onde o usuário digita (E-mail, Senha).                        |

---

## 📂 Organização com Frames e Setas

Ao criar um protótipo, não desenhe apenas telas isoladas. Desenhe o **fluxo**:

1. **Frames:** Cada tela do seu app deve estar dentro de um Frame nomeado (ex: `Login`, `Dashboard`, `Configurações`).
2. **Conectores (L):** Use setas para ligar um botão de uma tela ao Frame de destino. Isso mostra o "caminho" que o usuário fará.

---

## 🤖 Desafio Prático: Protótipo da Nossa Calculadora

Lembra da Calculadora que fizemos via CLI? Vamos desenhar a versão Web dela no Miro:

1. Crie um novo Board no Miro chamado `Lab-IHC-Calculadora`.
2. Adicione um Frame de **Browser** (Navegador).
3. **Desenhe a Interface:**
* Coloque um título no topo: "Calculadora .NET".
* Crie dois campos de entrada (Inputs) para os números.
* Adicione quatro botões (Soma, Subtração, Multiplicação, Divisão).
* Crie uma área de "Resultado" (um texto em destaque).


4. **Simule o Fluxo:** Crie um segundo Frame que mostra o resultado preenchido e use uma seta conectando o botão de "Soma" a essa nova tela.

---

## 💡 Dica de Sênior: "Don't Make Me Think"

Como desenvolvedores, amamos lógica, mas o usuário odeia ter que pensar. No seu protótipo:

* **Hierarquia Visual:** O botão mais importante deve ser maior ou mais "pesado" visualmente.
* **Consistência:** Se o botão de "Voltar" está na esquerda em uma tela, mantenha-o lá em todas as outras.
* **Dica de Atalho:** No Miro, segure `Alt` e arraste um objeto para duplicá-lo instantaneamente. **Ganhe tempo!**

---

## 📝 Atividade de Fixação

??? abstract "Exercício 1: Explorando a Biblioteca"
Ative a biblioteca de Wireframes do Miro e tente montar um formulário de "Esqueci minha senha" usando apenas os componentes prontos (Input, Button e Icon).

??? abstract "Exercício 2: Criando Navegação"
Crie três telas simples: `Home`, `Perfil` e `Sair`. Use a ferramenta de **Link** do Miro (ou setas) para mostrar como o usuário navega entre elas.

---

## 📝 Entrega do Projeto

Para validar sua participação, siga os passos:

1. No Miro, clique no botão **Share** (canto superior direito).
2. Mude a permissão para "Anyone with the link can **view**".
3. Copie o link do board.
4. Crie um arquivo chamado `PROTOTIPO.md` no seu repositório `una-ihcux-pratica03` (o mesmo da aula passada).
5. Cole o link do Miro dentro desse arquivo Markdown.
6. Dê um `git commit` e `git push`.

!!! tip "Próximos Passos"
Com o protótipo validado, o próximo passo é transformar esse desenho em componentes reais usando HTML/CSS ou Blazor. 
Na próxima aula: **Do Wireframe ao Código - Estruturando a UI!**