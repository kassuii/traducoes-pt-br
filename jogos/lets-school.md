# Let's School — tradução PT-BR

**12.832 textos.** O jogo inteiro: menus, tutoriais, diálogos, DLCs e editor de
mods.

## Instalar

1. Feche o jogo.
2. Rode o `Instalar-Traducao-PT-BR_LetsSchool.exe` e clique em **Instalar**.
3. No jogo: **Configurações → Idioma → "Portugues (Brasil)"**.

## Detalhes

O jogo já vinha com um slot `pt-BR` de fábrica, mas ele estava **praticamente
vazio**: 104 valores preenchidos de 10.875, e o idioma nem aparecia no seletor.

Duas coisas que descobrimos testando, e que explicam por que a instalação é do
jeito que é:

**O jogo esconde idioma com progresso baixo.** Todo idioma listado tem
`Progress >= 0,998` no arquivo `.ini`. O pt-BR vinha com 0,0097 e por isso nunca
aparecia — não era defeito, era regra do jogo.

**Valor vazio não cai para o inglês: mostra a chave, que é em chinês.** O jogo é
da Pathea e as chaves internas são o texto chinês original. Por isso o
instalador preenche o que falta com o **inglês** da sua própria cópia, em vez de
deixar vazio.

Como as chaves são o chinês, algumas traduções saíram do original e não do
inglês — que tem erros. `PlayHouse with [Name]` é 跳房子, ou seja **amarelinha**;
`Sink` é 下沉, **rebaixado**, não "pia".

## Desinstalar

Botão **Desinstalar** na janela. Volta o `pt-BR.json` de fábrica.
