# Little Goody Two Shoes — tradução PT-BR

**16.998 falas.** História, diálogos, menus, itens, tarefas, dicas e tutoriais.

## Instalar

1. Feche o jogo.
2. Rode o `Instalar-Traducao-PT-BR_LittleGoodyTwoShoes.exe` e clique em
   **Instalar**.
3. A instalação leva uns **85 segundos** e precisa de **~7 GB livres** em disco.
   A barra fica andando; é normal.

Não tem passo de selecionar idioma: o jogo **não tem seletor de idioma de
texto** (o "Voice Language" do menu é só a voz). A tradução entra no lugar do
inglês.

## Por que demora e por que precisa de espaço

Todo o jogo está num único arquivo `data.unity3d` de **6,4 GB**, comprimido em
LZ4. Para trocar o texto é preciso remontar esse arquivo.

O instalador renomeia o original para `data.unity3d.original` (renomear no mesmo
disco é instantâneo e não gasta espaço), lê os textos de dentro dele e grava uma
versão nova. Os 6,17 GB que vêm antes do ponto de emenda são copiados byte a
byte **sem descomprimir** — por isso são 85 segundos, e não horas.

## Por que sem acento

A fonte do jogo não tem acento nem cedilha: eles apareceriam como quadrados.

## Detalhe de tradução

As 8 falas que o jogo já trazia em português eram **pt-PT** ("Que estava eu a
pensar") — o estúdio é português. Foram reescritas em pt-BR junto com o resto.

## Desinstalar

Botão **Desinstalar** na janela. Devolve o `data.unity3d` de fábrica, que fica
guardado ao lado durante todo o tempo.
