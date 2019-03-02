#Comandos do Git

git init: 
	- Inicializa o repositório

git status:
	-Da informações sobre o estado do repositório

git add <nome arquivo>: 
	- adiciona o arquivo no estado 'Untracked' no repositório
	- muda o estado do arquivo de 'Modified' para 'Stage'

git commit -m "Mensagem":
	- realiza o commit do repositório passando uma mensagem do que foi feito
	
git log:
	- mostra o todos os commits realizados
	Parâmetros:
		* --author="Nome": filtra os commits pela pessoa que os fez
		* --graph: mostra os commits de forma gráfica

git shortlog:
	- mostra os commits ordenados por autores
	Parâmetros:
		* -sn: mostra a quantidade de commits por autor

git diff:
	- mostra as mudanças feitas nos arquivos
	Parâmetros:
		* --name-only: mostra apenas os nomes dos arquivos modificados

git show <código do commit>:
	- mostra as mudanças feitas naquele commit

git checkout <nome do arquivo>:
	- discarta as mudanças feitas no arquivo no estado 'Modified'

git reset HEAD <nome do arquivo>:
	- retorna um arquivo no modo 'Staged' para o modo 'Modified'
	Parâmetros no lugar no HEAD:
		* --soft: volta o arquivo para o modo 'Staged'
		* --mixed: volta o arquivo para o modo 'Modified'
		* --hard: mata o commit e todas as suas mudanças

git remote add origin <endereço do github>:
	- conecta o repositório a um repositório remoto

git push -u <destino> <branch> ou git push:
	- Envia os arquivos do repositório para o repositório remoto

git clone <link do repositório> <novo nome da pasta>:
	- Clona um repositório remoto para máquina local

##Branchs

git checkout -b <nome branch>:
	- Cria um novo branch

git branch
	- Mostra o branch ativo

git checkout <nome do branch>:
	- Altera o branch ativo

git branch -D <nome do branch>:
	- Deleta o branch

git merge <nome do branch>:
	- Junta o branch ao master pelo método 'merge'
	Merge: o merge cria um commit a mais que é responsavel por juntar os branchs,
	ele também cria uma estrutura ciclíca

git rebase <nome do branch>:
	- Junta o branch ao master pelo método 'rebase'
	Rebase: o rebase exclue os commits do branch, é cria outros correspondentes no master,
	a estrutura criada por ele é linear
