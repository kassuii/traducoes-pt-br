# Recettear: An Item Shop's Tale — tradução PT-BR

**7.631 textos.** O jogo inteiro.

- A história inteira: todos os eventos e cutscenes
- Todos os clientes da loja, com as falas de pechincha
- O catálogo de itens completo: 571 nomes com plural, 1.108 linhas de descrição
  e 33 categorias
- Tutoriais, notícias de preço e lista de inimigos
- Interface e menus

## Instalar

1. Feche o Recettear.
2. Rode o `Instalar-Traducao-PT-BR_Recettear.exe` e clique em **Instalar**.

Leva cerca de um minuto. Seus saves continuam valendo.

## Os nomes dos itens aparecem em três arquivos, e isso importa

O Recettear liga cada inimigo aos itens que ele dropa **pelo nome do item**, e
usa nome de item ou de categoria como chave dos eventos de flutuação de preço.

Traduzir só o catálogo deixaria essas buscas sem encontrar nada: o **drop de
item pararia de funcionar em toda masmorra** e as notícias de preço deixariam
de disparar — sem nenhuma mensagem de erro, sem nada quebrar visivelmente.

Os três arquivos foram traduzidos juntos, e o instalador tira os nomes das
referências da própria tradução do catálogo, então não têm como divergir.
Conferido depois de aplicar: **1.169 referências, 0 órfãs**.

## O que não foi traduzido

13 textos, e nenhum deles aparece em tela:

- 9 linhas de marcador que os próprios desenvolvedores deixaram no arquivo da
  personagem Euria. São a mesma frase em japonês, numerada de 1 a 9, dizendo
  que ela não faz compras. A Carpe Fulgur também não traduziu, porque o jogo
  nunca as mostra.
- 4 nomes de drop que entram pelo catálogo de itens em vez de por linha
  própria. No jogo aparecem em português normalmente.

## Por que sem acento

Os textos estão sem acento de propósito — *Coracao*, não *Coração*.

A fonte do jogo não desenha acento em todo lugar: em algumas telas o caractere
sai como quadrado ou buraco. Sem acento fica legível em tudo.

## O que ele faz com o seu jogo

O `recettear.exe` **confere** o arquivo de índice do jogo e se recusa a abrir
se ele estiver diferente do de fábrica. Por isso o instalador não mexe no
índice: cada arquivo traduzido é gravado no próprio lugar, ocupando exatamente
o mesmo espaço de antes.

(O espaço para o português sai de enxugar os comentários em japonês que os
arquivos trazem e o alinhamento de coluna dos campos numéricos. Nenhum dado do
jogo é perdido.)

Antes de gravar, o instalador guarda os bytes de fábrica de cada arquivo que
vai tocar. Depois de gravar, lê cada um de volta para conferir.

## Desinstalar

Botão **Desinstalar** na janela. Devolve cada arquivo aos bytes de fábrica
guardados na instalação.
