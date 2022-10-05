<h2 align="center"> Problemas e Soluções - GIT </h2>
<div align="justify">
:construction: Neste repositório estão os erros e as soluções que aprendi durante o uso do Git.

- <b> Erro encontrado: </b>  
<code>! [rejected]        master -> master (fetc h first) </code> <br>
<code> error: failed to push some refs to 'git@github.com:abc/abc.git'"</code> [...]

- <b> Solução #1 - Melhor encontrada: </b> <i>Digitar os seguintes comandos abaixo:</i><br> 
<code> git fetch origin master:tmp </code> ➡️ <code> git rebase tmp </code> ➡️<code> git push origin HEAD:master </code> ➡️ <code> git branch -D tmp </code>

- <b> Solução #2 - Cuidado! * </b> <i>Digitar o seguinte comando abaixo:</i><br>
<code>git push origin master --force</code>

 <i> * Se alguém construído em cima de sua história original enquanto você está rebasing, a ponta do ramo no controle remoto pode avançar com seu compromisso, e cegamente empurrando com -- force perderá seu trabalho.</i>
 </div>
 
##
