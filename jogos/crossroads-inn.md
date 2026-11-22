# Crossroads Inn — tradução PT-BR

**7.973 textos.** O jogo inteiro: campanha, modo livre, diálogos, legendas das
cutscenes, menus, receitas, construções, missões e enciclopédia.

Tradução de fã, sem nenhuma ligação com a Kraken Unleashed ou a Klabater.

## Importante: escolha RUSSO nas opções

A lista de idiomas é fixa dentro do executável do jogo — não dá para
acrescentar "português" nela. Então o português ocupa o lugar de um idioma que
já existe, e o escolhido foi o **russo**.

Depois de instalar:

**Options → Language → RUSSKIY**

O botão continua escrito com as letras russas. É só o nome do botão: o jogo
inteiro aparece em português. Os outros seis idiomas continuam intactos.

## Instalar

Rode o `Instalar-Traducao-PT-BR_CrossroadsInn.exe` e clique em **Instalar**.

Se o jogo estiver em `C:\Arquivos de Programas`, rode como administrador —
senão o Windows não deixa gravar.

Leva uns 15 segundos. O jogo cresce meio megabyte.

## Sem backup de 13 GB

Todo o texto do jogo mora dentro de `Bin\Project.pak`, um arquivo único de
**13,3 GB** com 22.696 arquivos dentro. Copiar isso para fazer backup seria
pedir 13 GB de disco emprestados para trocar meio mega de texto.

Não é o que o instalador faz. Ele escreve o arquivo em português **no fim** do
pak e regrava **12 bytes** do índice, para a fatia russa passar a apontar para
o arquivo novo. O arquivo russo original continua inteiro lá dentro — só não
tem mais ninguém apontando para ele.

Por isso o backup são duas linhas de texto, e **desinstalar devolve o pak byte
a byte**, exatamente como a Steam baixou.

Prefira o botão **Desinstalar** a "Verificar integridade dos arquivos": a
verificação da Steam baixa os 13,3 GB de novo.

## As 173 legendas que o inglês não tem

As cutscenes da campanha são legendadas — mas o arquivo de textos em inglês não
tem nenhuma dessas legendas. Elas existem só na fatia russa, com nomes de chave
próprios. Sem elas, as cutscenes rodariam **mudas** em português.

Então o instalador não só troca texto: ele também **acrescenta** as 173
legendas, uma por uma, com os mesmos nomes de chave e na mesma ordem que o
russo usa.

## O evento Dia da Lua

As 422 falas do evento de namorados não estão no arquivo de textos: estão num
arquivo solto, `Scenarios\valentines.scenario`, onde cada fala carrega as
próprias traduções — francês, alemão e polonês — uma atrás da outra.

Não havia vaga de russo ali. Então o instalador **acrescenta** uma quarta
tradução em cada uma das 422 falas, e não mexe nas três que o jogo já trazia:
quem joga em francês, alemão ou polonês não vê diferença nenhuma. Fora os
pedaços acrescentados, o arquivo continua byte a byte o que a Steam baixou.

Antes de gravar, o instalador confere o SHA-256 do arquivo do jogo e o do
arquivo que ele mesmo montou. Se qualquer um dos dois não bater — jogo
atualizado, mod, arquivo mexido — ele **não toca no arquivo** e deixa só o
evento em inglês; o resto da tradução entra normalmente.

## Sem acentos

Sem acento e sem cedilha, como nas outras traduções daqui.

## Nada do jogo vem no pacote

O arquivo em português é montado **na sua máquina**, a partir da sua própria
cópia do jogo. O que vem no download são duas tabelas com a chave, o português
e um **resumo SHA-256** do texto original — nunca o texto original.

Isso também é o que faz a tradução sobreviver a uma atualização: cada frase é
casada pela chave e pelo resumo, nunca por número de linha. Se a Steam mudar
uma frase, aquela linha fica em inglês e o instalador diz na tela quantas
ficaram de fora.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Restaurar`. Devolve os 12
bytes do índice, corta do fim do pak o pedaço acrescentado e põe o arquivo do
evento de volta — os dois conferidos por SHA-256 depois de voltar.
