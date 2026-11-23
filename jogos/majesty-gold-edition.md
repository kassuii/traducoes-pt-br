# Majesty Gold Edition — tradução PT-BR

**2.595 textos, escritos em 5.199 lugares do jogo.** O texto dos conselheiros,
as missões e as falas de fim de missão, os prédios e as melhorias, os heróis, os
monstros, os feitiços, os itens, a enciclopédia de dicas inteira, os menus, a
tela de montar partida e as mensagens do jogo.

Inclui a expansão **Northern Expansion**, que vem junto na edição Gold.

Tradução de fã, sem nenhuma ligação com a Cyberlore Studios.

## Não precisa escolher idioma

O Majesty não tem seletor de idioma: o português entra no lugar do inglês e
aparece sozinho quando você abre o jogo.

## Instalar

Rode o `Instalar-Traducao-PT-BR_MajestyGoldEdition.exe` e clique em
**Instalar**. Feche o jogo antes.

Se o jogo estiver em `C:\Arquivos de Programas` — é onde a Steam o coloca —
rode como administrador, senão o Windows não deixa gravar. O instalador testa
isso antes de mexer em qualquer arquivo e avisa.

Leva mais ou menos meio minuto.

## O pacote leva o motor, não o texto do jogo

O texto do Majesty mora dentro de dez arquivos `.cam`: caixas de 1999 com
várias tabelas de texto cada uma, onde cada texto é apontado por uma tabela de
posições. Trocar uma frase por outra de tamanho diferente obriga a remontar a
caixa inteira recalculando essas tabelas.

Então o que vem no download não é texto pronto para copiar por cima: é o
**motor** que faz essa conta na sua máquina, mais a tabela de traduções. O
instalador abre o `.cam` da *sua* cópia, troca os textos, remonta e recalcula.

Antes de gravar por cima, ele abre o arquivo novo **do zero** e exige três
coisas: que a estrutura inteira feche (os dados têm de ser contíguos e acabar no
byte exato do fim), que não tenha sobrado inglês conhecido, e que a cópia para a
pasta do jogo tenha o mesmo SHA-256 do arquivo que acabou de ser conferido.

No fim ele compara **quantos textos escreveu em cada arquivo** com o número
esperado. Se o seu Majesty for outra versão, o número sai diferente e isso
aparece na tela como aviso — em vez de passar calado como se estivesse tudo
certo.

## Como eu sei que o motor está certo

O motor do pacote é uma segunda implementação do formato, em PowerShell. A
primeira, em Python, é a que eu usei para traduzir aqui. Duas implementações do
mesmo formato binário é justo o lugar onde uma pode estar errada sem ninguém
notar.

Por isso a conferência não é "rodou sem erro": o instalador do pacote é rodado
contra uma cópia intocada do jogo e o SHA-256 dos dez arquivos que ele produz é
comparado com os dez arquivos que o Python produziu. Os dez saem **byte a byte
iguais**. Instalar duas vezes deixa tudo igual, e o `-Restaurar` devolve os
originais byte a byte.

## 1.873 textos ficam em inglês, de propósito

Dentro desses mesmos arquivos há texto que não é do jogador:

- nomes de arquivo de arte e de som (`tower_02`, `hb_atk1`)
- comentários que os programadores deixaram nas tabelas, que o jogo nunca mostra
- ids internos de evento (`60 Respawning_Lairs`), que andam em par com o nome de
  verdade — esse sim traduzido
- nomes próprios de pessoa e de lugar do mundo do jogo (Lormidia, Ravenswood,
  Brashnard, Krolm)

Traduzir qualquer um deles não apareceria na tela — ou quebraria a ligação do
jogo com a própria arte.

## Se algum botão aparecer apertado

O Majesty é de 1999 e os botões são arte de tamanho fixo. Em português algumas
palavras ficam mais compridas que em inglês — "RECRUTAR Patrulheiro" contra
"RECRUIT Ranger" — e não dá para saber, lendo os arquivos, se o texto cabe no
botão desenhado.

Se encontrar texto cortado ou saindo do lugar, abra uma
[issue](../../../issues) com um print. Dá para encurtar a frase daquele lugar
sem mexer no resto.

## Sem acentos

Sem acento e sem cedilha, como nas outras traduções daqui. A fonte do jogo é de
1999 e não dá para garantir que ela desenhe "ã" ou "ç": no lugar poderia sair um
quadrado.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Restaurar`.

Na primeira instalação o instalador guarda os dez originais numa pasta
`_original_pt-br` dentro da pasta do jogo (pouco mais de 1 MB). O desinstalar
devolve essa cópia conferindo o SHA-256 de cada arquivo.

Para só conferir, sem escrever nada:

    INSTALAR.bat -Verificar

## Se a Steam atualizar o jogo

Atualização — ou "Verificar integridade dos arquivos" — sobrescreve os `.cam` e
a tradução vai embora. É só rodar o instalador de novo. Saves não são afetados
em nenhum momento: a tradução não toca neles.
