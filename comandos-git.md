COMANDOS GIT
git add . - adiciona todas alterações
git add file.txt - adiciona file.txt
git status - vê estado dos commits
git status -s - status resumido
git status --short - status resumido
git commit -a - commit direto, sem passar por stagging
git commit -m "Mensagem" - commit passando pelo stagging com mensagem de alteração
git commit -amend - adiciona alterações no commit anterior
git push origin master - envia as alterações para o repositório na branch master
git push - ||
git pull origin - baixa commits do repositório remoto
git pull - ||
git fetch origin - atualiza as referências com um repositório remoto (busca branches etc)
git fetch - ||
git rm <nome_do_arquivo> - remove determinado arquivo do repositório local
git branch <nome_da_branch> - cria nova branch com o nome desejado
git branch - lista as branches disponíveis no repositório local
git checkout <nome_da_branch> - navega para aquela branch
git checkout -b <nome_da_branch> - cria nova branch e já faz checkout nela
git push --set-upstream origin new-branch - faz push da nova branch e suas alterações
git push -u origin <nome_da_branch> - faz push da branch (nova ou não) e suas alterações
git checkout - - o git checkout - te leva a branch que você estava trabalhando antes de trocar de branch
git branch -d <nome_da_branch> - remove branch do repositorio local
git push --delete origin <nome_da_branch> - remove do repositório online a branch desejada
git merge <nome_da_branch> - faz merge com a branch desejada
git merge <nome_da_branch> -no-ff - faz merge com a branch deseja no modo 3-way
git pull --rebase - força rebase ao fazer pull
git rebase <nome_da_branch> - reaplica todos os commits na branch desejada
git rebase master -i - mostra lista de commits e posso alterar ela para mudar o histórico e tudo, muito foda
git log - mostra lista de commits
git log --oneline - mostra historico de commits em uma linha por commit
git log --abbrev-commit - ||
git log --color - mostra historico de commits e tenta colorir o output
git log --graph - mostra historico em um grafico das branchs em modo texto
git log --pretty - mostra historico e permite que sejam utilizados place holders para as informações dos commits
git tag <versao> - cria uma tag com a versao desejada
git checkout <versao> - "travo" para usar aquele commit em específico
git push origin --tags - além do push normal eu preciso fazer push das tags também, para acrescentar uma tag no que foi commitado
git checkout --ours <arquivo_conflito> - adiciona conteúdo sem modificação que conflitou
git checkout --theirs <arquivo_conflito> - adiciona conteúdo em conflito na branch atual que estou
git merge -abort - cancela um merge que eu havia feito
git reset --mixed - altera o staging e o repositório, mantém o working dir intacto. É o padrão e é útil nos casos que queremos desfazer partes das alterações e criar um novo commit em seguida
git reset --soft - similar ao mixed, mas mantém o staging como está
git reset --hard - desfaz tudo a partir de um commit específico
git revert - não modifica histórico de commits, mas cria um novo commit com o inverso do commit desejado, ou seja, o resultado final é o commit anterior
git reset HEAD~1 --hard - descarta e elimina as alterações do último commit
git checkout HEAD~2 - move o HEAD para dois commits anteriores
git revert <hash> - reverte as alterações de um commit específico e cria um novo commit
git reset HEAD~2 <arquivo> - restaura para o staging as alterações do arquivo desejado em dois commits atrás
git checkout -- <arquivo> - recupera diretamente no working dir o arquivo desejado
git add --patch - vejo linha por linha da alteração e consigo selecionar o que quero adicionar ao commit
git clone <repo> --depth - quero o clone a partir de X commits