# 🎓 Aula 01: O Despertar do Terminal (com C#)

## 1. O que é esse tal de "Console"?

Pense no Console como uma **conversa de WhatsApp** com o seu computador:

* **Você** digita uma mensagem (**Input**).
* O **Computador** processa.
* O **Computador** responde com um texto (**Output**).

Antigamente, não existia mouse. Se você quisesse que o computador fizesse algo, você tinha que saber o nome do comando. Hoje, os melhores programadores do mundo ainda fazem isso porque é **muito mais rápido**.

## 2. Nossa primeira ferramenta: `Console.WriteLine`

No C#, nossa principal forma de "falar" com o usuário é o comando `Console.WriteLine()`.

~~~
Console.WriteLine("Olá, Mundo! Este é o meu primeiro software.");
~~~

Dica: O WriteLine escreve e pula para a linha de baixo. Se você usar apenas Write, ele escreve e fica parado na mesma linha. Parece bobagem, mas é a base para criar interfaces organizadas!

## 3. Lendo o que o usuário diz

Para que o programa não seja um monólogo, precisamos **ouvir**. Para isso, usamos o `Console.ReadLine()`.

~~~
Console.Write("Digite seu nome de usuário: ");
string nome = Console.ReadLine(); // O programa para e espera você digitar algo

Console.WriteLine("Acesso permitido, " + nome + "!");
~~~

## 4. Deixando a "Tela Preta" Profissional

Ninguém gosta de um texto chapado e sem graça. Mesmo no primeiro dia, podemos usar cores para indicar o que está acontecendo. No C#, fazemos isso com o `Console.ForegroundColor`.

### 🚦 O Semáforo do Programador:
* **Verde:** Sucesso.
* **Amarelo:** Atenção / Carregando.
* **Vermelho:** Deu ruim (Erro).

~~~
Console.ForegroundColor = ConsoleColor.Cyan;
Console.WriteLine("--- SISTEMA DE LOGIN ---");
Console.ResetColor(); // Importante: Sempre limpe a cor depois de usar!
~~~

## 5. O Grande Desafio do Dia: "O Oráculo Numérico"

Para fechar nossa primeira aula, vamos criar um pequeno sistema de console que interage com o usuário.

**O que o seu programa deve fazer:**

1.  **Limpar a tela** ao iniciar (`Console.Clear()`).
2.  Mudar a **cor do título** para Amarelo.
3.  **Perguntar** o nome do aluno.
4.  **Pedir** um número de 1 a 10.
5.  **Se o número for 7** (o número da sorte do Oráculo), mostrar uma mensagem em **Verde**.
6.  **Se não**, mostrar uma mensagem em **Vermelho**.

---

## 📝 O que deve ser entregue:

1. O **código fonte (Program.cs)** funcional e sem erros de compilação.
2. A **URL do seu repositório do GitHub** contendo o código.
* **Nome do repositório:** `ihcux-pratica-03`

--- 

## 💡 Por que estamos aprendendo isso?

Toda grande inteligência artificial, todo sistema de banco e todo servidor de jogo roda em interfaces de console. 
Se você aprender a estruturar dados aqui, criar uma interface visual depois será "moleza".
