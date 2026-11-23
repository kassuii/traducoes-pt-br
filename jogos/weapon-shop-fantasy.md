# Weapon Shop Fantasy — tradução PT-BR

**3.864 textos.** O jogo inteiro: a história completa da dívida ao epílogo, as
308 missões, o Livro dos Monstros, os itens, as receitas, as habilidades, as
conquistas, os empregados e a interface toda.

Tradução de fã, sem nenhuma ligação com a INDIECN.

## Importante: deixe o idioma em ENGLISH

O jogo tem quatro idiomas e nenhuma vaga sobrando para o português. Então a
tradução ocupa o lugar do **inglês**.

Depois de instalar, abra o jogo e deixe em **English**. Se você deixar em
chinês ou japonês, o jogo aparece nesses idiomas.

## Instalar

Rode o `Instalar-Traducao-PT-BR_WeaponShopFantasy.exe` e clique em
**Instalar**. Feche o jogo antes — o arquivo de texto fica aberto enquanto ele
roda.

Se o jogo estiver em `C:\Arquivos de Programas`, rode como administrador —
senão o Windows não deixa gravar.

Leva menos de um segundo.

## Precisa ser Windows 10 ou 11

O texto do jogo não é um arquivo de idioma: é um **banco de dados SQLite** de
1 MB, com 16 tabelas, dentro de `StreamingAssets\wsfdata.wsf`.

Para escrever ali o instalador usa o `winsqlite3.dll`, que já vem no Windows 10
e no 11. Nada é baixado, nada é instalado e nenhuma biblioteca vai no pacote.

As 3.864 gravações acontecem **dentro de uma transação só**: ou todas entram, ou
nenhuma entra. Não existe meio caminho onde o jogo fica com metade do texto em
português.

## As 308 missões

Cada missão é pedida por um empregado específico da loja, e o jogo guarda qual.
Foi por isso que dava para acertar o gênero de quem fala em todas elas: o título
da missão da clériga Iona está no feminino porque é ela quem pede, não porque
"missão" seja palavra feminina.

Nos pedidos, o jogo pinta de vermelho o item, o monstro ou a habilidade que você
precisa levar. A tradução mantém a marcação no mesmo lugar e com o **mesmo
nome** que aparece na loja e no Livro dos Monstros — se o pedido diz uma coisa e
a prateleira diz outra, a missão fica impossível de entender.

## Sem acentos

Sem acento e sem cedilha, como nas outras traduções daqui.

## Nada do jogo vem no pacote

O download tem quatro arquivos: o instalador, o leia-me e uma tabela de textos.
Nenhum byte do jogo. A montagem do pacote tem lista branca com `throw`: se
qualquer arquivo a mais tentar entrar, o pacote não é gerado.

A tabela leva o **inglês original ao lado do português**, e ela é a prova de que
o instalador está escrevendo no lugar certo: antes de gravar, ele confere se o
texto que está no banco é exatamente aquele inglês. Se o jogo tiver sido
atualizado e algum texto tiver mudado, ele **para e não escreve nada**.

É assim que a tradução casa por texto de origem, nunca por número de linha.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Desinstalar`.

Na primeira instalação o instalador guarda uma cópia do banco de antes. O
desinstalar devolve essa cópia inteira, byte a byte.

E se você apagar essa cópia, o desinstalar **continua funcionando**: ele escreve
o inglês de volta texto por texto, porque o inglês original também está na
tabela que veio no download. O resultado é idêntico ao arquivo de fábrica.

## Conferir sem mexer em nada

    INSTALAR.bat -Verificar

Abre o banco e conta quantos dos 3.864 textos estão em português, quantos
continuam em inglês e quantos estão diferentes dos dois. Não escreve nada.

## Se a Steam atualizar o jogo

Atualização — ou "Verificar integridade dos arquivos" — sobrescreve o banco e a
tradução vai embora. É só rodar o instalador de novo. Saves não são afetados em
nenhum momento: a tradução não toca neles.
