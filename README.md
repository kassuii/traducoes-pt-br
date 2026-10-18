# Traduções PT-BR

Traduções completas para **português do Brasil** de jogos que não têm versão
oficial em português — ou que têm uma versão oficial abandonada pela metade.

Cada tradução cobre o jogo inteiro: história, diálogos, itens e interface. Não é
só menu.

Feitas por **kassuii**.

---

## Jogos

| Jogo | Textos | Como instalar |
|---|---:|---|
| [Xuan-Yuan Sword VI: The Gate of Firmament](jogos/xuan-yuan-sword-vi.md) | 24.904 | instalador |
| [Little Goody Two Shoes](jogos/little-goody-two-shoes.md) | 16.998 | instalador |
| [Let's School](jogos/lets-school.md) | 12.832 | instalador |
| [Recettear: An Item Shop's Tale](jogos/recettear.md) | 7.631 | instalador |
| [Warcraft III: The Frozen Throne](jogos/warcraft-iii.md) | 5.735 | instalador |
| [Natural Selection 2](jogos/natural-selection-2.md) | 3.666 | instalador |
| [Horticular](jogos/horticular.md) | 1.991 | Oficina Steam ou instalador |
| [Chantelise: A Tale of Two Sisters](jogos/chantelise.md) | 1.397 | instalador |

Os arquivos ficam na página de **[Releases](../../releases)**.

---

## Como instalar

Baixe o `Instalar-Traducao-PT-BR_<jogo>.exe` na página de Releases e clique duas
vezes. Ele acha o jogo sozinho, mostra o que vai fazer e tem botão de
desinstalar.

Se preferir não rodar executável, cada jogo também tem um `.zip` com o mesmo
conteúdo: descompacte e rode o `INSTALAR.bat`.

### O aviso do Windows

Na primeira vez, o Windows provavelmente vai mostrar **"O Windows protegeu o seu
computador"**. Isso acontece com todo executável sem assinatura digital — um
certificado pago que, para uma tradução distribuída de graça, não faz sentido
manter.

Para seguir: **Mais informações → Executar assim mesmo**.

Se preferir não confiar na minha palavra, cada Release traz o **SHA-256** de
todos os arquivos. Confira antes de rodar:

```powershell
Get-FileHash .\Instalar-Traducao-PT-BR_NaturalSelection2.exe -Algorithm SHA256
```

---

## Como funciona

Duas regras valem para todas as traduções daqui:

**1. O pacote nunca contém arquivo do jogo.**

O que você baixa tem só o instalador e os textos em português. Nada de conteúdo
original do jogo — redistribuir isso está fora de questão. Na prática, o
instalador lê o arquivo de idioma da *sua* cópia e escreve o português por cima,
na sua máquina.

Cada projeto tem uma lista branca com `throw`: se um arquivo que não está
explicitamente autorizado tentar entrar no pacote, a montagem falha.

**2. A tradução casa por texto de origem, não por número de linha.**

Se o jogo for atualizado e ganhar textos novos, eles simplesmente ficam em
inglês. Nada vira texto trocado de lugar, e a tradução sobrevive à atualização.

Todo instalador faz backup do arquivo original antes de mexer, e tem
`-Desinstalar` para voltar ao estado de fábrica.

---

## Problemas

Abra uma [issue](../../issues) contando qual jogo, o que aconteceu e, se o
instalador mostrou mensagem de erro, cole o texto dela inteiro.

---

Os nomes dos jogos e suas marcas pertencem aos respectivos donos. Estas são
traduções feitas por fã, sem vínculo com os desenvolvedores, distribuídas de
graça.
