# Cineris Somnia — tradução PT-BR

**2.548 textos**, aplicados em 16.063 lugares do jogo: história, diálogos,
cartas e diários, itens, menus, tela de save e créditos.

## IMPORTANTE: escolha RUSSO na tela de título

O jogo guarda quatro idiomas lado a lado — japonês, inglês, chinês e russo — e
não sobra espaço para um quinto. **O português ocupa o lugar do russo.**

Então, depois de instalar:

> abra o jogo → na tela de título, escolha **RUSSO**

Inglês, japonês e chinês continuam intactos, e trocar de idioma no jogo continua
funcionando normalmente.

## Instalar

1. Feche o Cineris Somnia.
2. Rode o `Instalar-Traducao-PT-BR_CinerisSomnia.exe` e clique em **Instalar**.

Se o jogo estiver em "Arquivos de Programas", o instalador avisa e mostra o
botão de administrador — sem isso o Windows não deixa gravar.

São 150 arquivos para reconstruir: leva alguns minutos e precisa de uns **900 MB
livres** no disco onde o jogo está (400 MB do backup mais os arquivos novos).

Seus saves continuam valendo.

## Três botões são imagem, não texto

No menu de opções, "Aplicar", "Voltar" e "Padrões" não são texto: são desenhos
prontos, um por idioma. Como escrever neles exigiria redesenhar a arte do jogo,
eles passaram a mostrar a versão **inglesa** — *Apply*, *Return* e *Default* —
em vez da russa. O resto do menu está em português.

## Por que sem acento

Os textos estão sem acento e sem cedilha de propósito — *Coracao*, não
*Coração*.

A fonte do jogo não desenha acento em todo lugar: em algumas telas o caractere
sai como quadrado ou buraco. Sem acento fica legível em tudo.

## O que ele faz com o seu jogo

O texto do Cineris Somnia mora espalhado em 150 arquivos (as cenas, o
`resources.assets` e o `sharedassets1.assets`). O instalador:

1. copia os 150 originais para `_original_pt-br`, ao lado do jogo, conferindo o
   SHA-256 de cada um;
2. acha o texto da fatia russa e troca pelo português, casando pelo **texto de
   origem** — nunca por número de linha, para a tradução sobreviver a uma
   atualização;
3. remonta cada arquivo recalculando a tabela interna de objetos;
4. só grava por cima depois de conferir o arquivo novo: ele tem de abrir, o
   último objeto tem de terminar no byte exato do fim, e não pode sobrar texto
   em russo.

Se você já tem a tradução instalada e apagou a pasta de backup, o instalador
reconhece isso e **para**, em vez de guardar o arquivo já traduzido como se
fosse o original.

## Depois de uma atualização da Steam

A Steam substitui os arquivos quando atualiza o jogo, e a tradução some. É só
rodar o instalador de novo. "Verificar integridade dos arquivos" faz a mesma
coisa.

## Desinstalar

Botão **Desinstalar** na janela. Ele devolve os 150 arquivos do backup,
conferindo o SHA-256 de cada um.

A pasta `_original_pt-br` é o seu caminho de volta: se apagar, só dá para
recuperar pela Steam, em "Verificar integridade dos arquivos".

## Créditos

Tradução para português do Brasil: **kassuii**.

Tradução para russo: **Violetta** — e o crédito aqui tem motivo concreto, não é
só cortesia. É o lugar dela no jogo que o português ocupa, e foram as quebras de
linha dela que serviram de molde: cada fala está picada em pedaços do tamanho da
caixa de texto, e o número de pedaços muda de idioma para idioma. O português
foi escrito para caber exatamente nos pedaços que ela deixou. Onde o inglês
ficou ambíguo, a versão russa desempatou.

A tradução chinesa continua creditada dentro do jogo, com o nome do tradutor
preservado. Os créditos originais — autoria, arte, música e vozes — foram
mantidos integralmente, só traduzidos.
