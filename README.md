# Trabalho-Elias
Composição de nota

1.	O que é a gerência de configuração?
Gerência de Configuração de Software (GCS) é um conjunto de atividades de apoio que permite a absorção controlada das mudanças inerentes ao desenvolvimento de software, mantendo a estabilidade na evolução do projeto.
2.	O que são itens de configuração?
São todas as alterações nos produtos de trabalho identificados. Uma entidade dentro de uma configuração que satisfaz uma função de uso final e que pode ser identificada de forma única em uma determinada baseline. Um item de configuração pode agregar vários produtos de trabalho, mas deve ser tratado como uma entidade singular pelo processo Gerência de Configuração.

3.	De acordo com o MPS.BR, quais os resultados esperados para o processo de gerência de configuração?
GCO 1. Um Sistema de Gerência de Configuração é estabelecido e mantido; 
GCO 2. Os itens de configuração são identificados com base em critérios estabelecidos; 
GCO 3. Os itens de configuração sujeitos a um controle formal são colocados sob baseline; 
GCO 4. A situação dos itens de configuração e das baselines é registrada ao longo do tempo e disponibilizada; 
GCO 5. Modificações em itens de configuração são controladas; 
GCO 6. O armazenamento, o manuseio e a liberação de itens de configuração e baselines são controlados; 
GCO 7. Auditorias de configuração são realizadas objetivamente para assegurar que as baselines e os itens de configuração estejam íntegros, completos e consistentes. 


4.	Como se dá o processo de gerência de configuração (exemplifique e indique softwares/ferramentas que auxiliem esse tipo de gerência)?
Mudanças durante o desenvolvimento são inevitáveis; o entendimento dos usuários sobre suas necessidades muda, o ambiente no qual o sistema vai operar muda, a legislação muda, os requisitos mudam. Com tantas mudanças assim, é necessária alguma forma de gerenciamento para que o desenvolvimento não fique caótico.
Tipo de Ferramenta	Open Source	Comercial
Controle de Versão	•	Mercurial
•	Git
•	Subversion
•	CVS
•	Team Foundation Server - Microsoft
•	Team Concert - IBM/Rational
•	ClearCase
•	StarTeam
•	Perforce
•	BitKeeper

Controle de Mudança	•	Trac
•	Redmine
•	Mantis
•	Bugzilla
•	JIRA
•	FogBUGZ
•	CaliberRM
•	Perforce

Integração Contínua	•	Jenkins | Jenkins
•	Bitten
•	SCons
•	Ant
•	Maven
•	CruiseControl
•	Gump
•	TinderBox
•	AntHill Pro
•	FinalBuilder
•	BuildForge



5.	GitHub
1.	O que é e qual sua função?
GitHub é uma plataforma de código de hospedagem para controle de versão e colaboração. Ele permite que você e outros trabalham juntos em projetos de qualquer lugar. Resumindo, você poderá usar gratuitamente o github para hospedar seus projetos pessoais. Além disso, quase todos os projetos/frameworks/bibliotecas sobre desenvolvimento open source estão no github, e você pode acompanhá-los através de novas versões, contribuir informando bugs ou até mesmo enviando código e correções. Se você é desenvolvedor e ainda não tem github, você está atrasado e essa é a hora de correr atrás do prejuízo.

2.	Guia de uso (tutorial passo-a-passo) (Instalação/configuração, criar conta, postar arquivos.... comandos básicos)

Instalando o Git para Windows
No site oficial do Git (http://git-scm.com/) há links para download para Windows, Mac e Linux. Clique no link do Windows.
 

Na próxima tela clique no arquivo com a descrição "Full installer for official Git for Windows" (o nome do arquivo pode variar dependendo da versão mais recente).
 

Na tela seguinte clique novamente no nome do arquivo para iniciar o download.
Execute o arquivo baixado e vá dando "Next" até a tela "Select Components". Nesta tela eu escolho as opções como na imagem:

 

Em especial eu marco a opção "Windows Explorer integration" > "Context menu entries", assim eu consigo abrir o prompt de comandos do Git (Git Bash) em qualquer pasta, basta clicar com o botão direito e "Git Bash Here". A última opção também é interessante, porque ele instala uma fonte melhorzinha para o prompt de comandos.
Nota: O Git para Windows vem com um prompt de comandos próprio (o Git Bash), que além dos comandos git também fornece alguns comandos Unix que podem ser bem úteis (além de ser bem mais bonitinho que o prompt de comandos padrão do Windows).
Na próxima tela, eu escolho a opção mais conservadora: "Use Git Bash only".
 

Esta opção permite usar o git e os outros comandos Unix apenas pelo Git Bash.
A segunda opção permite usar o Git também pelo prompt padrão do Windows, mas não os comandos Unix. Já a terceira permite usar todos os comandos pelo prompt do Windows, mas alguns comandos do Windows serão substituídos por comandos Unix que tem o mesmo nome (como find e sort).
Outra configuração importante: quebra de linhas.

 
Windows e sistemas Unix (Linux, Mac) possuem formatos diferentes de quebra de linha em arquivos texto. Se você escreve um código com quebras de linha no formato Windows, outra pessoa pode ter problemas ao abrir o mesmo arquivo em um Linux, e vice-versa. Esta opção permite normalizar isso.
A primeira opção converte os arquivos para padrão Windows quando os arquivos chegam para você, e convertem para padrão Unix quando você os comita no repositório. A segunda não faz nenhuma conversão quando os arquivos chegam, mas convertem para padrão Unix quando você comita. Já a terceira opção não faz nenhuma conversão.
Eu opto pela segunda, pois prefiro manter tudo no padrão Unix (já que qualquer bom editor de código consegue ler arquivos no padrão Unix mesmo estando em Windows).
Feito isso, "Next", "Finish" e o Git está instalado.

Criando um repositório e comitando
Crie uma pasta, botão direito nela e "Git Bash Here".

 

Antes de mais nada, informe ao Git os seus dados, que irão identificar seus commits. Digite os comandos:
git config --global user.name "Nome Sobrenome"
git config --global user.email "seu_email@email.com"

Dica: para copiar e colar comandos no Git Bash, clique com o botão direito na barra de título da janela e na opção "Editar" você tem as opções de marcar, copiar, colar.
Agora vamos inicializar um repositório Git nesta pasta que estamos.
git init
 

Viu esse (master) que apareceu na linha de comando? Ele indica que você está em um repositório Git, na branch master. Xique, hein?
Vamos adicionar um arquivo neste repositório que está vazio e comitá-lo. Veja a sequência de comandos:
touch teste.txt
git add .
git commit -m "Primeiro commit"
Primeiro criamos um arquivo teste.txt vazio. Depois adicionamos todos os novos arquivos (no caso só o teste.txt) ao índice do repositório, e por último comitamos todos os arquivos que estão no índice e foram modificados.

 Compartilhando no GitHub
Legal, você tem um repositório Git na sua máquina, mas que tal compartilhar seus códigos noGitHub e usufruir de tudo que essa comunidade tem para oferecer?

 Preparação Inicial
Vá em http://github.com e clique em "Pricing and signup" e depois "Create an free account" para criar sua conta gratuita.
Tendo cadastrado e logado em sua conta, agora você precisa de uma chave SSH para poder começar a comitar. No Git Bash digite:
ssh-keygen -t rsa -C "seu_email@email.com"
Informe no comando seu e-mail cadastrado no GitHub. Dê Enter na próxima pergunta (sobre o arquivo a ser criado - vamos deixar o padrão).
A próxima pergunta vai te pedir uma senha (passphrase). Invente uma senha e a informe. Ele vai pedir uma confirmação. Digite a senha novamente e Enter. Digite agora:
notepad ~/.ssh/id_rsa.pub
para abrir no Bloco de Notas o arquivo que foi criado.
Agora no GitHub, vá em "Account Settings" e depois "SSH Public Keys". Clique "Add another public key". Informe um título para identificar o computador onde a a chave foi gerada e no campo "Key" cole todo o conteúdo do arquivo id_rsa.pub (que você abriu no Bloco de Notas).
 
Tome cuidado de copiar e colar todo o conteúdo do arquivo, começando por "ssh-rsa ..." até o seu e-mail (incluindo ele, como na imagem). Clique em "Add Key".
Vamos testar pra ver se essa bagaça deu certo. No Git Bash digite:
ssh -T git@github.com
Ele vai perguntar se você tem certeza que quer conectar bla bla bla (yes/no). Digite yes e Enter. Na próxima pergunta (Enter passphrase...) informe sua senha (a que você escolheu ao criar a chave SSH).
Se você receber uma mensagem do tipo:
Hi doug2k1! You've successfully authenticated, but GitHub does not provide shell access.
Então tudo deu certo!



Criando o primeiro repositório remoto
No GitHub vamos criar um novo repositório (botão "New Repository" no seu dashboard). Informe um nome preferencialmente sem espaços e caracteres especiais, caso contrário o GitHub vai remover esses caracteres.
 


Você cairá na página do seu repositório, que por enquanto ainda não tem arquivos.
Importante! Se o e-mail informado ao Git no início do passo 2 não for o mesmo usado para se cadastrar no GitHub, refaça o comando informando o e-mail cadastrado. Assim o GitHub vai poder ligar os commits à sua conta.
No Git Bash (na pasta do seu repositório local) digite:
git remote add origin git@github.com:seu_login/nome_do_repositorio.git
Note que seu_login/nome_do_repositorio deve ser digitado como aparece na URL do seu repositório, no exemplo:
https://github.com/doug2k1/projeto_tutorial
Agora para atualizar o GitHub com o que está no seu repositório local, digite:
git push origin master
Informe a sua senha (da chave SSH) quando pedido.
Recarregue a página do seu repositório e agora, ao invés da mensagem inicial, você verá seus commits e arquivos.
 
3.	Criar um conta e postar um ou mais documentos (informar o endereço da sua conta no trabalho)
 

 


 

4.	Fazer alterações no(s) documento(s) e envia-lo novamente ao repositório (capturar "print" da tela e postar no trabalho)
