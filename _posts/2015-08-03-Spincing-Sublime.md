---
layout: post
title: Melhorando o Sublime!
---

Já faz um tempinho... Desculpem-me por isso. Muito trabalho para fazer... :pensive: Vou tentar fazer 2 posts para compensar. (Já que quebrei minha promessa inicial) Eles serão posts rápidos (com alguma coisinha que aprendi durante essas semanas)

<div style="text-align:center"><img src="/images/guilty_dog.gif" width="300" height="170"></div>

Semana passada (na verdade, fazem duas semanas, eu acho) Eu estava lendo um [post](http://devblog.avdi.org/2015/07/08/ruby-is-defined-by-terrible-tools/) do Avdi Grimm, sobre as ferramentas que são usadas para programar em Ruby.

Não quero discutir o post, mas ele me fez ficar pensando no quanto eu sofro usando o Sublime para programar. Instalei o RUbyMine (a licensa academica), mas eu não tive a mesma agilidade que eu tenho com o Sublime e eu estou com vários problemas para fazer a troca.

No fim o que eu fiz foi: comecei a melhorar um pouco meu Sublime. Para aqueles que não conhece o [Sublime](http://www.sublimetext.com/) é um editor de texto para 'codar'. Existem os amantes e os que odeiam e eu ainda gosto dele. E ele é grátis, só fica te enchendo o saco para comprar a licensa de vez em quando.

Você pode 'tunar' o Sublime instalando pacotes nele. A primeira coisa a fazer é instalar o [Package Control](https://packagecontrol.io/installation). É bem simples e fácinho. Eu uso esses pacotes: [All Autocomplete](https://packagecontrol.io/packages/All%20Autocomplete), [GitGutter](https://packagecontrol.io/packages/GitGutter) and the [Rails Casts Colour](https://packagecontrol.io/packages/RailsCasts%20Colour%20Scheme). Eu também uso umas configuração muito legais para me ajudar. E aí eu li o post do Avdi Grimm e só isso não pareceu o suficiente. Eu queria algo que me impedisse de adicionar um estilo fora do padrão da comunidade no meu código. Algo que me ajudasse a achar aquela maldita vírgula que eu escrevi a mais e quebrava todo o meu código. Descobri depois que eu queria a ajuda do rubocop no meu Sublime.

<div style="text-align:center"><img src="/images/bug-dance.gif" width="300" height="170"></div>

[Rubocop](https://github.com/bbatsov/rubocop) é ua gem que analisa o seu código  de acordo com o [Ruby Style  Guide](https://github.com/bbatsov/ruby-style-guide). Depois da instalação da gem você pode executá-la através do seu terminal e voilà! Ele mostrará todas as 'ofensas' que você cometeu ao programar.
Ele é beeem chato. Se você estava acostumado a programar como se não houvesse amanhã, ele vai te impedir (ou pelo menos te atormentar mostrando os seus erros). É bem fácil configurar um novo arquivo `yml` para alterar o seu comportamento normal (afinal um número maior de caracteres sempre é bem-vindo).

Eu não queria ficar rodando esse comando toda vez no console. Poderia até ser feito junto do RSpec, mas não... Então eu descobri o [Sublime Linter](https://packagecontrol.io/packages/SublimeLinter). Eu não sabia o que a palavra 'linter' significava e de acordo com a wikipédia:

> In computer programming, lint was the name originally given to a particular program that flagged some suspicious and non-portable constructs (likely to be bugs) in C language source code.
> The term is now applied generically to tools that flag suspicious usage in software written in any computer language. The term lint-like behavior is sometimes applied to the process of flagging suspicious language usage.
> Lint-like tools generally perform static analysis of source code.

<div style="text-align:center"><img src="/images/police.gif" width="300" height="170"></div>

Bem o que eu queria :relaxed: mas, ele não funciona sozinho. Da documentação:

> SublimeLinter does not do the linting itself; it acts as a host for linting plugins.
> The linting plugins themselves usually do not perform linting either; they just act as a bridge between the code you type in Sublime Text and the actual linter.

O Linter pode ser usado para várias linguagens, e você pode instalar quantos plugins de linter quiser!

"Programar é dificil. Estamos sujeitos a cometer erros. A grande vantagem de se usar o SublimeLinter é que o seu código será 'linted' enquanto você digita (antes de salvar) e qualquer erro será destacado imediatamente, o que é muito mais fácil do que salvar o arquivo, mudar para um terminal, rodar o linter, ler a lista de erros, e depois voltar para o Sublime para encontrar os erros nos arquivos!"

<div style="text-align:center"><img src="/images/omg.gif" width="300" height="250"></div>

Se você usa o eclipse ou algum outro editor mais poderoso, você está me julgando agora... Eu sei... Mas eu não ligo. É uma das coisas que o post menciona, não seja preguiçoso e o leia.

Agora, vamos adicionar o [SublimeLinter-ruby](https://packagecontrol.io/packages/SublimeLinter-ruby) e o [SublimeLinter-rubocop](https://packagecontrol.io/packages/SublimeLinter-rubocop) para ver a magia acontecer. Você vai precisar configurar o ruby path em Preferences -> Package Settings -> Sublime Linter -> Settings - Default.

Aqui vai o meu exemplo:

```
"paths": {
            "linux": ["~/.rvm/rubies/ruby-2.1.3/bin/ruby"],
            "osx": [],
            "windows": []
        },
```

Você também vai precisar instalar a gem do rubocop. Você pode instalar na pasta onde ficam todos os seus projetos. Agora esteja pronto para ver as 'ofensas' que você cometeu no código em amarelo e códigos 'quebrados' em vermelho. 

![Image of rubocop offenses](/images/rubocop-linter.png)
