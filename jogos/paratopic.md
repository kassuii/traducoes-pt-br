# Paratopic — tradução PT-BR

**607 falas**, em 12 cenas: o jogo inteiro — diálogos, escolhas, menu, opções e
as dicas de controle.

O Paratopic não tem save: ele foi feito para ser jogado de uma vez só, em cerca
de uma hora.

## IMPORTANTE: escolha PORTUGUÊS no menu de opções

O jogo monta o caminho de cada pacote de texto a partir do **nome** do idioma.
Criar um idioma novo exigiria mexer na tabela de recursos do jogo; ocupar uma
vaga que já existe troca só o conteúdo, que é a parte segura. **O português
ocupa o lugar do japonês.**

Depois de instalar:

> abra o jogo → **Opções** → **Idioma** → clique até aparecer
> **"Idioma: Portugues"**

O inglês fica intocado — e o instalador prova que ficou, a cada arquivo que
grava. Quem quiser jogar em inglês só escolhe inglês no mesmo menu, a qualquer
hora.

## Instalar

1. Feche o Paratopic.
2. Rode o `Instalar-Traducao-PT-BR_Paratopic.exe` e clique em **Instalar**.

Se o jogo estiver em "Arquivos de Programas", o instalador avisa e mostra o
botão de administrador — sem isso o Windows não deixa gravar.

O instalador acha o jogo sozinho (na Steam a pasta se chama `ParatopicAM001`).

## Por que sem acento

Os textos estão sem acento e sem cedilha de propósito — *Coracao*, não
*Coração*.

A fonte do jogo não tem essas letras desenhadas, e letra sem desenho some ou
vira quadrado na tela.

## Um detalhe que não é defeito da tradução

No menu de Opções, a linha do tamanho da janela aparece como **"Em janela:
1920x1080"**, repetindo a palavra.

Isso é um engano do próprio Paratopic: esse item procura o texto errado na
tabela — pede a chave da palavra "em janela" em vez da chave de "resolução". Em
inglês ele também mostra *"Windowed: 1920x1080"*. Consertar aquilo seria mexer
no programa do jogo, não na tradução, então ficou como o original.

## O que ele faz com o seu jogo

A fala do Paratopic não mora no diálogo: o grafo de diálogo guarda só **chaves**
(os 457 campos foram conferidos um por um, e nenhum tem texto). A fala mora em
pacotes XML, um por cena e por idioma, gravados dentro do
`sharedassets0.assets`:

```xml
<entry name="P17_0"><text>A Loja do Leite?</text></entry>
```

O instalador:

1. copia os originais para `_original_pt-br`, ao lado do jogo;
2. monta o XML em português a partir do **XML inglês da sua própria cópia**, com
   o conteúdo de cada fala trocado, casando pela **chave** de cada entrada —
   nunca por posição;
3. remonta o arquivo recalculando a tabela interna de objetos;
4. só grava por cima depois de conferir o arquivo novo: ele tem de abrir, ter a
   mesma tabela de objetos, cada objeto começando no alinhamento certo, o
   cabeçalho batendo com o tamanho real, cada pacote voltando exatamente como
   foi gravado — e o inglês intocado.

Arquivo desalinhado não dá mensagem de erro: dá tela em branco. É por isso que a
conferência vem antes da gravação, e não depois.

## Como ele sabe que já passou por ali

Rodar o instalador duas vezes não pode guardar um arquivo já traduzido como se
fosse o original. Para saber se a vaga do japonês já é nossa, ele procura lá
dentro uma **frase da tradução** — com 12 caracteres ou mais, e diferente do
inglês.

Procurar "tem caractere não-ASCII" não funcionaria, e esse foi o primeiro erro:
o pacote de fontes japonês é ASCII puro no original.

## Depois de uma atualização da Steam

A Steam substitui os arquivos quando atualiza o jogo, e a tradução some. É só
rodar o instalador de novo. "Verificar integridade dos arquivos" faz a mesma
coisa.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Restaurar` pelo zip. Ele
devolve os arquivos do backup conferindo o SHA-256 de cada um.

A pasta `_original_pt-br` é o seu caminho de volta: se apagar, só dá para
recuperar pela Steam.

## Créditos

Tradução para português do Brasil: **kassuii**.

Os créditos originais do jogo — autoria, arte e música — foram mantidos
integralmente, só traduzidos.
