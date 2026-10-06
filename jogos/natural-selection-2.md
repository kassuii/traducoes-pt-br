# Natural Selection 2 — tradução PT-BR

**3.666 textos.** O jogo inteiro: menus, tutoriais, dicas, navegador de
servidores, Matched Play e cosméticos.

O jogo já tinha um português oficial, mas ele foi abandonado com **19%**
traduzido (691 de 3.675). Esta tradução completa o que faltava e ainda corrige
cinco erros que vinham no arquivo oficial — entre eles um `\n` sem a barra, que
fazia aparecer um "n" solto no meio da frase.

## Instalar

1. Feche o jogo.
2. Rode o `Instalar-Traducao-PT-BR_NaturalSelection2.exe` e clique em
   **Instalar**.
3. No jogo: **Options → Language → Portuguese**. Ele pede para reiniciar o
   cliente; é normal.

Se o jogo estiver em "Arquivos de Programas", o instalador avisa e oferece o
botão de administrador.

## Dá para jogar multiplayer com isso?

**Dá, sem problema nenhum.**

Os servidores do NS2 fazem verificação de consistência dos arquivos, mas ela
cobre `.lua`, `.dds`, `.model`, `.shader`, `.level` e afins. Arquivo `.txt`
**não está na lista**, e os textos do jogo são `.txt`.

Ou seja: traduzir não te derruba de servidor, não afeta ranqueamento e não conta
como trapaça. Isso está no próprio código do jogo, em
`core\lua\ConsistencyConfig.lua`, que a Unknown Worlds distribui aberto.

## O que fica em inglês, e por quê

Alguns rótulos do menu principal — **OPTIONS, SKINS, CREDITS, CUSTOMIZATION,
Weapons, Armors, Shoulder Patches, Exosuits**.

Esses textos estão escritos direto no código Lua (`GUIMenuNavBar.lua`), não no
arquivo de idioma. Nunca passam pela tradução. Duas provas de que não é falha
daqui: o arquivo oficial da Unknown Worlds já trazia `MENU_OPTIONS = "OPÇÕES"` e
a tela continuava em inglês do mesmo jeito.

Traduzir esses rótulos exigiria editar `.lua` — que **está** na verificação de
consistência e quebraria o multiplayer. Por isso ficam como estão.

## Desinstalar

Botão **Desinstalar** na janela. Volta o `ptBR.txt` de fábrica, que o instalador
guarda intocado na primeira execução.
