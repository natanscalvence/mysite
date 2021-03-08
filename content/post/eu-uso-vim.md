+++
date = 2021-03-07
description = "Como eu melhorei meu fluxo diário de estudos usando apenas o Linux e o Vim."
title = "Como eu melhorei meus estudos usando Linux e Vim."
author = "Natan Gabriel"
+++

Em 2019 quando instalei o Linux pela primeira vez, eu senti o poder que o mesmo tinha, desde uma simples tarefa até as mais complexas. Começei na programação não muito tarde disto, e esta postagem serve justamente para mostrar que um simples Linux com Vim podem se transformar uma máquina poderosa de trabalho, se executado da forma correta.

Antes de tudo, qual distribuição usar? A resposta para isso, na minha opinião é: Aquela que te da conforto de usabilidade. Se você usa o Fedora, Debian ou até mesmo sistemas BSD, se você se sente confortável usando ele e o mesmo lhe serve, é o que vale. Sinceramente, não existe distribuição melhor que a outra já que muitos veem com propósitos diferentes, então não, não adianta sobrepor sua distribuição por cima das outras, e não, você não é superior por usar Kali Linux, Arch Linux, ou Manjaro.

Mas sem enrolação, como eu consegui um método ótimo de estudos com o Vim e o Linux? Arrasta pra cima...

Brincadeiras a parte. Desde que eu comecei a usar Linux, isso no Ubuntu, usei sempre o Gedit. Era um editor de texto padrão na qual eu podia realizar meus códigos e compilar os mesmo através do Terminal. Porém, eu sou uma pessoa muito chata, tanto com editores de texto quanto IDE's, não me sinto bem usando um editor de texto em forma GNU, já que eu perco um certo tempo alterando entre o Terminal e a interface, mesmo que seja um tempo minímo as vezes acabo me confundindo. (Vai pode me chamar de louco, tudo bem).
Foi então rodando alguns vídeos que encontrei dois editores, Emacs e VIM, usei o EMACS e me dei bem até um certo tempo, até perceber o quanto o eshell dele é horrível, e que para usar o shell próprio do sistema eu teria que sair do editor. E então migrei pro VIM e desde então apenas sucesso.

O Linux lhe permite instalar alguns pacotes que já vem por padrão em seu repositório (depende muito da distribuição é claro), entretanto, você pode escolher desde um Vim simples, puro até um Neovim, personalizado e cheio de funcionalidades pra lhe auxiliar. E lembrando que ambos podem ser executados por terminal.

(mas se você ainda deseja algo mais GTK, vai de GVim que é sucesso.)

Quando comecei a usar o VIM percebi o quanto esse editor, por mais que pareça simples pode ser poderoso, e você pode então ficar livre do seu mouse, exatamente, assim que você começa a 'manjar' das teclas, você nem precisa mais de Mouse, além de que keybinds são especificadas apenas para comandos específicos. Inclusive, no final da postagem deixarei os comandos que eu uso no meu Vim.
Além de sua agilidade no processo de escrever códigos, o Linux permite um melhor manuseio com outras ferramentas como o Git, então os comandos acabam sendo muito acessíveis, com apenas uma janela de terminal você apenas lista o seu projeto e da o famoso 'git push origin master'. Uma coisa que eu acho engraçada, é que você consegue fazer tanta coisa por um simples shell, que particulamente nem precisariamos de interface gráfica, muitos projetos como i3-wm, bpswm ou dwm já trazem esse quesito, funcionando apenas como Windows Manager, ou seja, funciona apenas com janelas, e nada mais, o que possibilita ainda mais a produtivo, já que você pode ter até de 3-4 terminais ou janelas abertas e gerenciar tudo por ali. Porém, não recomendo para iniciantes. Sem contar que esses Windows Managers não funcionam em todas as distribuições.

O vim junto ao Linux se configurados de uma forma correta e agradável ao usuário pode sim gerar um trabalho melhorado em comparação a outros sistemas, Unix como o MacOS também conta, já que o estilo de trabalho é parecido. 


Bônus:
___

{{< highlight html >}}

"Essa é a minha configuração de Vim, se desejar, cole e jogue no seu arquivo
.vimrc

runtime! debian.vim

" Vim will load $VIMRUNTIME/defaults.vim if the user does not have a vimrc.
" This happens after /etc/vim/vimrc(.local) are loaded, so it will override
" any settings in these files.
" If you don't want that to happen, uncomment the below line to prevent
" defaults.vim from being loaded.
" let g:skip_defaults_vim = 1

" Uncomment the next line to make Vim more Vi-compatible
" NOTE: debian.vim sets 'nocompatible'.  Setting 'compatible' changes numerous
" options, so any other options should be set AFTER setting 'compatible'.
"set compatible

" Vim5 and later versions support syntax highlighting. Uncommenting the next
" line enables syntax highlighting by default.
if has("syntax")
  syntax on
endif


"Adiciona os números
set number

"Ajusta o padrão do tab
set tabstop=3

"Seta como tema padrão
colorscheme focusedpanic "Caso queira o mesmo tema, basta acessar: 
"https://github.com/tjammer/focusedpanic.vim

"Mapeia a tecla Q para sair como atalho
map! <C-q> <ESC>:quit<CR>

"Mapeia a tecla W para salvar
map! <C-w> <ESC>:w<CR>

"Adiciona a identação automática
set autoindent

"Adiciona procura no código
set incsearch

"Adiciona uma barra de informações no bottom do arquivo
set laststatus=2

"Adiciona uma confirmação de salvar o arquivo
set confirm

"Adiciona o titulo do arquivo
set title

"Ativa o mouse dentro do vim
set mouse=a



{{< /highlight >}}
