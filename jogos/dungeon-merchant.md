# Dungeon Merchant — tradução PT-BR

**378 textos**, aplicados em 831 lugares do jogo: menus, tutorial, diálogos,
itens, armas, avisos e as mensagens que o jogo escreve na hora — ouro recebido,
nível do herói, pedidos dos fregueses.

## Instalar

1. Feche o jogo.
2. Rode o `Instalar-Traducao-PT-BR_DungeonMerchant.exe` e clique em
   **Instalar**.

Se o jogo estiver em "Arquivos de Programas", o instalador avisa e mostra o
botão de administrador — sem isso o Windows não deixa gravar.

O jogo não tem menu de idioma: depois de instalar, ele abre em português
direto. Seus saves continuam valendo.

## Por que sem acento

Os textos estão sem acento e sem cedilha de propósito — *Poção* virou *Pocao*.

A fonte do jogo não tem essas letras desenhadas, e letra sem desenho some ou
vira quadrado na tela.

## O que continua em inglês

Os nomes próprios: os heróis, o Jiff, e os pedaços que o jogo sorteia para
montar nome de personagem. Nome de gente não se traduz, e traduzir aqueles
pedaços daria nome sem sentido.

## O texto mora em dois lugares diferentes

E isso muda tudo, porque são dois problemas técnicos distintos.

**293 textos estão nas cenas** — nos componentes de texto da tela. Trocar uma
string ali muda o tamanho do objeto, então a área de dados inteira precisa ser
remontada com o alinhamento certo e a tabela de objetos reescrita. Arquivo
desalinhado não dá mensagem de erro: dá tela em branco.

**85 frases estão dentro do programa** (`Assembly-CSharp.dll`), escritas no meio
do código. Ali a troca é feita **em cima**, com o mesmo número de caracteres e a
sobra virando espaço, para que nenhum endereço interno do arquivo mude de lugar.
Quando a frase é um começo que recebe valor — `"Hero Takes "`, `"COLLECT ("` —
o espaço sobrando vai para a **esquerda**, senão o número apareceria colado na
palavra.

Dessas 85, **65 mudam de texto**; as outras saem iguais ao inglês de propósito.

## Como eu decidi o que podia ser traduzido

Essa é a parte que deu mais trabalho, e é a que importa: no meio do código, uma
frase em inglês pode ser texto de tela ou pode ser **o nome de uma coisa que o
programa usa para se achar**. Trocar a segunda quebra o jogo em silêncio.

Então cada frase foi seguida até **quem consome ela**. Isso barrou 66 textos que
pareciam tradução e não eram: mensagens de depuração, chaves de save, nome de
cena, eixo de controle, parâmetro de animação e identificador de conquista da
Steam.

Nas cenas o critério foi o **componente** que guarda a string: o que está num
componente de texto vai para a tela; a palavra `"Vertical"` guardada no
componente de controle é o eixo do teclado.

## O que ele faz com o seu jogo

1. copia os 14 arquivos originais para `_original_pt-br`, ao lado do jogo,
   conferindo o SHA-256 de cada um;
2. aplica a tradução casando pelo **texto de origem**, nunca por posição;
3. só grava por cima depois de conferir o arquivo novo.

Rodar de novo lê sempre do backup, não de si mesmo — então não tem como a
tradução ser aplicada duas vezes em cima de si.

## Depois de uma atualização da Steam

A Steam substitui os arquivos quando atualiza o jogo, e a tradução some. É só
rodar o instalador de novo: o que continuar igual volta para o português
sozinho, e texto novo fica em inglês.

## Desinstalar

Botão **Desinstalar** na janela, ou `INSTALAR.bat -Restaurar` pelo zip. Ele
devolve os 14 arquivos do backup conferindo o SHA-256 de cada um.

A pasta `_original_pt-br` é o seu caminho de volta: se apagar, só dá para
recuperar pela Steam, em "Verificar integridade dos arquivos".

## Créditos

Tradução para português do Brasil: **kassuii**.

Os créditos originais do jogo foram mantidos integralmente, só traduzidos.
