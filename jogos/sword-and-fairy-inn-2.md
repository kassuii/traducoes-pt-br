# Sword and Fairy Inn 2 — tradução PT-BR

**10.507 frases, em 11.218 das 11.585 linhas de texto do jogo.** A história e as
falas dos personagens, os menus e as configurações, o tutorial, o cardápio, os
pratos, os ingredientes, as receitas, a mobília, as lojas, os fregueses, as
missões, a enciclopédia, as conquistas, as dicas de carregamento e os créditos.

仙剑客栈2 / *Sword and Fairy Inn 2*, da Softstar. Tradução de fã, sem nenhuma
ligação com a desenvolvedora.

## Jogue com o jogo em inglês

O jogo tem três idiomas: chinês simplificado, chinês tradicional e inglês.
Português não está na lista, e idioma novo não se acrescenta por fora.

Então esta tradução ocupa a **fatia do inglês**: com ela instalada, quem joga em
inglês vê português. Os dois chineses continuam intactos.

A fatia do inglês foi a escolhida porque é a mais completa — o chinês
simplificado tem 1.533 linhas de menos, já que o chinês é o idioma de origem e
várias linhas lá são preenchidas de outro jeito.

Para voltar ao inglês de verdade, desinstale.

## Esta tradução não altera nenhum arquivo do jogo

A Unreal Engine carrega qualquer pacote terminado em `_P` que esteja na pasta
`Paks`, e o que está dentro dele vence o que está nos pacotes originais. Então a
tradução é **um arquivo novo**, de 1,7 MB:

```
palinn2\Content\Paks\pakchunk99-WindowsNoEditor_pt-BR_P.pak
```

Os dez pacotes do jogo ficam intocados — o maior tem 2,3 GB, mesmo SHA-256
antes e depois.

Por isso aqui não existe pasta de backup: não há nada para salvar. Desinstalar é
apagar aquele único arquivo.

## Instalar

1. Feche o jogo.
2. Rode o `Instalar-Traducao-PT-BR_SwordAndFairyInn2.exe` e clique em
   **Instalar**.
3. Abra o jogo com o idioma em **inglês**.

Se o jogo estiver em "Arquivos de Programas" — é onde a Steam o coloca —, o
instalador avisa e mostra o botão de administrador, senão o Windows não deixa
gravar.

É instantâneo: um arquivo copiado e conferido por SHA-256.

Seus saves continuam valendo. A tradução não toca neles em nenhum momento.

## O formato do pacote foi escrito do zero

O texto do jogo mora em `Game.locres`, dentro de pacotes `.pak` da Unreal
Engine, versão 11 do formato. Não havia ferramenta aqui para ler nem para
escrever nenhum dos dois, então os dois foram implementados.

A prova de que o modelo do formato está certo não é "abriu sem erro": é
**remontar e comparar**. Os dez pacotes do jogo, com cerca de 37.800 arquivos
dentro, foram lidos e remontados byte a byte iguais aos originais; os três
`Game.locres` também. Um campo entendido errado em formato binário não dá erro —
dá texto que desaparece da tela sem avisar.

O pacote entregue é montado na hora em que o zip é fechado, e aí reaberto do
zero: um script abre o `.pak` gravado, confere que dentro dele existe **um
arquivo só**, relê o `Game.locres` de dentro e compara, chave por chave, com a
tabela em inglês do jogo — mesmos espaços de nome, mesma ordem, mesmos hashes de
origem — exigindo em cada uma exatamente o texto que a tabela de tradução manda.

## Por que sem acento

Os textos estão sem acento e sem cedilha de propósito — *Ninho de Pássaro* virou
*Ninho de Passaro*, *coração* virou *coracao*.

É para não depender da fonte que o jogo carrega em cada tela: fonte sem a letra
desenhada mostra quadrado ou buraco. A verificação do pacote reforça isso por
caractere — nenhuma letra que não exista no inglês do jogo passa.

## O que continua em inglês, de propósito

**367 linhas, de 277 textos diferentes**, porque traduzir atrapalharia ou não há
o que traduzir:

- **nomes de pessoa e de lugar** do mundo do jogo — Chonglou, Fa Tian, Feng Du,
  Bai Moqing, Gu Hanjiang;
- **palavras iguais em português** — Bonsai, Ginseng, Cordyceps, Auto;
- **siglas e rótulos curtos** — `HP:`, `CUL:`, `CONT`;
- **risadas e interjeições** — `Ah!`, `Haha...`, `ARRRGH!`;
- **números, letras soltas** e linhas que são só pontuação ou só um campo que o
  jogo preenche na hora (`<Red22>{{Menu.27}}</>?`).

## Os botões da tela de título não são texto

Os cinco botões da tela inicial — jogo novo, carregar, contabilidade, batalha
online e sair — continuam como estavam. Eles não passam pela tabela de texto: são
imagem desenhada. Não estão no `Game.locres` nem como texto dentro do
executável.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Restaurar` pelo zip.

Ele apaga o arquivo que adicionou — e só se o arquivo for o dele mesmo,
conferido por SHA-256, para não apagar o trabalho de outra pessoa. O jogo volta a
ser exatamente o que a Steam baixou, com o inglês original de volta.

Para só conferir, sem escrever nada:

    INSTALAR.bat -Verificar

## Depois de uma atualização da Steam

Normalmente a tradução continua funcionando: a Steam atualiza os arquivos do
jogo, e o nosso é um arquivo que ela não conhece. Se "Verificar integridade dos
arquivos" apagar o arquivo extra, é só rodar o instalador de novo.

Se o jogo ganhar texto novo, esse texto aparece em inglês e nada mais: o
casamento é sempre pelo **texto em inglês**, nunca por posição.

## Créditos

Tradução para português do Brasil: **kassuii**.

Os créditos originais do jogo foram preservados.
