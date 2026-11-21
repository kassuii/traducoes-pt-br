# My Little Blacksmith Shop — tradução PT-BR

**2.533 frases**: menus, configurações, tutorial, o livro-guia, nomes de peças,
metais, armas, armaduras, comidas, construção, as falas dos fregueses, as notas
de atualização e as mensagens de erro.

## Esta tradução não altera nenhum arquivo do jogo

É a única aqui que não precisa mexer em nada. A Unreal Engine carrega qualquer
pacote terminado em `_P` que esteja na pasta `Paks`, e o que está dentro dele
vence o que está no pacote original. Então a tradução é **um arquivo novo**, de
uns 335 KB:

```
MLBSS\Content\Paks\MLBSS-WindowsNoEditor_pt-BR_P.pak
```

O pacote do jogo, de 884 MB, fica intocado — mesmo SHA-256 antes e depois.

Por isso aqui não existe pasta de backup: não há nada para salvar. Desinstalar é
apagar aquele único arquivo.

## Instalar

1. Feche o jogo.
2. Rode o `Instalar-Traducao-PT-BR_MyLittleBlacksmithShop.exe` e clique em
   **Instalar**.

Se o jogo estiver em "Arquivos de Programas", o instalador avisa e mostra o
botão de administrador — sem isso o Windows não deixa gravar.

É instantâneo: um arquivo copiado e conferido.

Se o jogo não abrir em português, vá em **Configurações → idioma** e escolha
Português. O português já era um dos 17 idiomas do jogo; esta tradução só
preenche o que estava faltando.

Seus saves continuam valendo. O inglês continua intacto no mesmo menu.

## O jogo já vinha com 170 frases em português

Tradução oficial, parada no meio do caminho — praticamente só o menu principal.
Essas 170 foram **mantidas**, só tiveram o acento removido para combinar com o
resto, e as outras 2.363 foram traduzidas.

## Por que sem acento

Os textos estão sem acento e sem cedilha de propósito — *Cabeça de martelo*
virou *Cabeca de martelo*.

É para não depender da fonte que o jogo carrega em cada tela: fonte sem a letra
desenhada mostra quadrado ou buraco.

## O que continua em inglês, de propósito

**351 textos**, porque traduzir atrapalharia:

- **nomes de pessoa** — os fregueses, e as sílabas que o jogo sorteia para
  montar nome;
- **metais inventados pelo jogo** — Nobilium, Spiritium, Tenebrium, Celestium,
  Chronosium, Abadonium, Aquanium, Cosmosium, Obsidine, Titaner;
- **siglas** que são iguais em português — FPS, NPC, LAN, XP, UI, Ping;
- **identificadores de conquista da Steam**, identificadores internos e textos
  de teste do programador.

Outros **199** não têm o que traduzir: números, letras soltas e linhas que são
só campos preenchidos pelo jogo (`{Quality} {WeaponName}`).

## Como eu decidi o que era nome e o que era palavra

O jogo vem com 16 idiomas, e vários estão bem traduzidos. Quando uma palavra
solta era ambígua, a escolha dos outros tradutores desempatou — e em três casos
isso evitou um erro que eu teria cometido sozinha:

- **`Elm`** aparece no meio de Cedar, Ash, Fir, Oak e Pine. Parecia madeira, e
  eu ia escrever "Olmo". Mas o chinês **transliterou** ("Ai-er-mu") em vez de
  usar 榆木: é nome de pessoa.
- **`Stey`** parecia nome de gente, cercado de Stewart e Sorina. O chinês pôs
  峭壁 — *penhasco*.
- **`Lorisian Guard`** parecia um soldado. O alemão pôs *Lorisianische
  Parierstange* e o russo *гарда*: é a **guarda da espada**, a peça de metal
  entre a lâmina e o cabo.

E o contrário também: `Titaner`, `Nobilium` e `Obsidine` o chinês traduziu como
liga metálica de verdade (钛合金, 钴铬合金, 黑曜石), mas são metais inventados
pelo jogo e ficaram em inglês, como os outros.

Quando **nenhum** dos 16 idiomas traduziu uma palavra — `Frost`, `Mercy`,
`Envelop` — ela ficou em inglês, com o motivo anotado na tabela.

## O que ele faz com o seu jogo

1. copia um arquivo de 335 KB para `MLBSS\Content\Paks`;
2. confere o SHA-256 do que foi copiado.

É isso. Nenhum arquivo do jogo é lido para ser reescrito, porque nenhum precisa
mudar.

A tabela de texto em português foi montada a partir da tabela em **inglês** do
jogo, com o conteúdo de cada entrada trocado: mesma ordem, mesmas chaves, mesmos
hashes. O casamento é sempre pelo **texto em inglês**, nunca por posição — se o
jogo for atualizado e ganhar texto novo, esse texto aparece em inglês e nada
mais.

## Depois de uma atualização da Steam

Normalmente a tradução continua funcionando: a Steam atualiza os arquivos do
jogo, e o nosso é um arquivo que ela não conhece. Se "Verificar integridade dos
arquivos" apagar o arquivo extra, é só rodar o instalador de novo.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Restaurar` pelo zip.

Ele apaga o arquivo que adicionou — e só se o arquivo for o dele mesmo,
conferido por SHA-256, para não apagar o trabalho de outra pessoa. O jogo volta
a ser exatamente o que a Steam baixou.

## Créditos

Tradução para português do Brasil: **kassuii**.

As 170 frases que o jogo já trazia em português foram mantidas. Os créditos
originais do jogo foram preservados.
