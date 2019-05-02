# sop-exer-comando-terminal-shell-script
Exercicio1
``````````````````````````````````````````````
echo"Ana Carolina Knop"
``````````````````````````````````````````````
Exercício 2
``````````````````````````````````````````````
echo "Ana Carolina Knop" > cliente01.txt
less cliente01.txt
``````````````````````````````````````````````
Exercício 3
``````````````````````````````````````````````
[root@localhost ~]# echo "Joinville" >> cliente01.txt
[root@localhost ~]# less cliente01.txt
``````````````````````````````````````````````
Exercício 04
``````````````````````````````````````````````
[root@localhost ~]# mkdir clientes
[root@localhost ~]# ls
cliente01.txt  clientes       dos            hello.c
``````````````````````````````````````````````
Exercício 05

``````````````````````````````````````````````
[root@localhost ~]# mv ~/cliente01.txt clientes
[root@localhost ~]# cd clientes
[root@localhost clientes]# ls
cliente01.txt
``````````````````````````````````````````````
Exercício 06

``````````````````````````````````````````````
[root@localhost clientes]# cp cliente01.txt cliente01.txt.bkp
[root@localhost clientes]# ls
cliente01.txt      cliente01.txt.bkp
``````````````````````````````````````````````
Exercício 07
``````````````````````````````````````````````
[root@localhost clientes]# rm cliente01.txt
[root@localhost clientes]# ls
cliente01.txt.bkp
``````````````````````````````````````````````
Exercício 08

``````````````````````````````````````````````
[root@localhost ~]# vi cliente.script
[root@localhost ~]# #!/usr/bash
[root@localhost ~]# echo "Ana Carolina Knop"
[root@localhost ~]# echo "Ana Carolina Knop" > cliente01.txt
[root@localhost ~]# echo "Joinville" >> cliente01.txt
[root@localhost ~]# mkdir clientes
[root@localhost ~]# mv ~/cliente01.txt clientes
[root@localhost ~]# cp cliente01.txt cliente01.txt.bkp
[root@localhost ~]# rm cliente01.txt
``````````````````````````````````````````````
Exercício 09

``````````````````````````````````````````````
[root@localhost ~]# chmod 777 script.shell
``````````````````````````````````````````````
Exercício 10

``````````````````````````````````````````````
 Quando utiliza o comando echo|cal>hoje.txt, gera um arquivo tipo txt com nome "hoje" onde
	tem uma tabela com o mês igual o do horário da máquina. O less permite a
	visualização do arquivo sem alterá-lo.
``````````````````````````````````````````````
Exercício 11

``````````````````````````````````````````````
[root@localhost ~]# wget https://gist.githubusercontent.com/leandersonandre/c8cba982f42262591be628e5397d1c3f/raw/bd13a3e13823708e477f99f9285f845b292714c6/cidades_sc.txt.
``````````````````````````````````````````````
Exercício 12
``````````````````````````````````````````````
[root@localhost ~]# grep Balneario cidades sc.txt
	apresentou o resultado da busca por cidades que possuem Balneario no nome:
	Balneario Camburiu;
	Balneario Barra do Sul;
	Balneario Barra Velha;
	Balneario Itajuba;
  ``````````````````````````````````````````````
  Exercício 13
  ``````````````````````````````````````````````
 [root@localhost ~]#  grep balneario cidades_sc.txt não encontrou nenhuma cidade pois o "b" é minúsculo e o programa é case sensitive.
 ``````````````````````````````````````````````
 Exercício 14
 
``````````````````````````````````````````````
  [root@localhost ~]#  grep "do sul", não encontrou nenhuma cidade não se deve usar aspas para procurar.
 ``````````````````````````````````````````````
Exercício 15

``````````````````````````````````````````````
[root@localhost ~]#  cat cidades_sc.txt | grep Balneario

	Retornou as cidades:
	Balneario Camburiu;
	Balneario Barra do Sul;
	Balneario Barra Velha;
	Balneario Itajuba;
  ``````````````````````````````````````````````
  Exercício 16
  ``````````````````````````````````````````````
 [root@localhost ~]#  vi balneario.txt
	Balneario Camburiu;
	Balneario Barra do Sul;
	Balneario Barra Velha;
	Balneario Itajuba;
  ``````````````````````````````````````````````
  Exercício 17
  ``````````````````````````````````````````````
  [root@localhost ~]# gzip balneario.txt renomeou para balneario.txt.gz,
	utilizei gzip pois o tar nao funcionou
  ``````````````````````````````````````````````
  Exercício 18
  ``````````````````````````````````````````````
  gzip -d balneario.txt.gz  descompactou para balneario.txt
  
``````````````````````````````````````````````
  _______________________________________________________________________________
  Exercícios Shell Script
  Exercício 01
  
``````````````````````````````````````````````
  [root@localhost ~]# echo "Informe Seu Nome "
	[root@localhost ~]# read nome
	[root@localhost ~]# echo "Seu nome é: $nome "
``````````````````````````````````````````````
Exercício 02
``````````````````````````````````````````````
  [root@localhost ~]#  echo "Digite um numero:"
	[root@localhost ~]# #read x
	[root@localhost ~]# echo "Digite outro numero:"
	[root@localhost ~]# read z
	[root@localhost ~]# y=$(($x*$z))
	[root@localhost ~]# echo "Seu resultado $y"
  ``````````````````````````````````````````````
  Exercício 03
``````````````````````````````````````````````
  [root@localhost ~]# echo "Digite um numero: "
	[root@localhost ~]# read x
	[root@localhost ~]# if [ $x -gt 0 ]; then
   [root@localhost ~]#   #echo "maior que 0"
	[root@localhost ~]# elif [ $x -lt 0 ]; then
   [root@localhost ~]#     #echo "menor que zero"
	[root@localhost ~]# else
   [root@localhost ~]#     #echo "igual zero"
	[root@localhost ~]# fi
``````````````````````````````````````````````
Exercício 04

``````````````````````````````````````````````
Numero: 2
	2x0 = 1
	2x1 = 2
	...
	2x10 = 20
 ``````````````````````````````````````````````
 Exercício 05
 
``````````````````````````````````````````````
[root@localhost ~]#  #!/usr/bash
	[root@localhost ~]# echo "1: Calendrio"
	[root@localhost ~]# echo "2: Listas de arquivos do diretrio"
	[root@localhost ~]# read x
	[root@localhost ~]# if [ $x -eq 1 ]; then
    [root@localhost ~]#    echo|cal
	[root@localhost ~]# elif [ $x -eq 2 ]; then
   [root@localhost ~]#     mkdir Documentos
   [root@localhost ~]#     cd Documentos
    [root@localhost ~]#    echo "  " > arquivo1.txt
    [root@localhost ~]#    echo "  " > arquivo2.txt
     [root@localhost ~]#   ls
[root@localhost ~]#	else
   [root@localhost ~]#     echo "Voce digitou  errado"
	fi
