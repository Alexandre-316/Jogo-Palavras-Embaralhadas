# Descri��o do trabalho
Jogo das Palavras Embaralhadas:
O objetivo desse exerc�cio � criar um jogo onde partes de sua execu��o possam ser trocadas. 
O jogo � simples: 
� apresentado ao jogador uma palavra com as letras embaralhadas e o jogador deve tentar adivinhar a palavra correta. O jogo ser� jogado no pr�prio console e a lista de palavras utilizadas pode ser fixa (pelo menos 20).

A classe Scanner pode ser utilizada para ler a entrada do usu�rio no console. Ela deve ser criada da seguinte forma: Scanner in = new Scanner(System.in); e em seguida metodos como nextLine() ou nextInt() podem ser utilizados para recuperar o que foi digitado pelo usu�rio.

Passos

O jogo deve possuir os seguintes componentes com as seguintes responsabilidades: 

classe Principal: representa a classe com o metodo main(). Essa classe que � respons�vel por ler a entrada do usu�rio e por imprimir as informa��es no console. Nenhuma outra classe pode imprimir ou ler do console. 

Classe BancoDePalavras: classe que possui um metodo que retorna uma palavra retirada aleat�riamente de uma lista de palavras lida a partir de um arquivo.
 
Classe  Embaralhador: interface que representa classes repons�veis por receber uma palavra e retornar ela embaralhada. Pelo menos duas implementa��es dever�o ser feitas.
 
Classe FabricaEmbaralhadores: possui um metodo que retorna um embaralhador aleat�riamente. 

Classe MecanicaDoJogo: interface que representa o andamento e a l�gica do jogo. Ser� respons�vel por ditar o andamento do jogo. Ela que vai dizer se o jogo acabou ou n�o, se o usu�rio acertou a palavra ou n�o,se o usu�rio pode tentar acertar a palavra novamente e qual foi a pontua��oo final do jogador. Pelo menos duas implementa��es dessa interface devem ser criadas. 

Classe FabricaMecanicaDoJogo: retorna a MecanicaDoJogo que deve ser utilizada. 

A classe Principal deve recuperar a instancia de MecanicaDoJogo de FabricaMecanicaDoJogo e n�o pode conter nenhuma refer�ncia direta a uma das implementa��es, apenas a interface. 

Da mesma forma, as implementa��es de MecanicaDoJogo devem recuperar os embaralhadores de FabricaEmbaralhadores e tamb�m n�o pode conter nenhuma refer�ncia direta a implementa��es de Embaralhador, apenas a interface. As implementa��es de embaralhador devem conter algoritmos para o embaralhamento de palavras. 
As implementa��es de MecanicaDoJogo devem retratar o andamento do jogo. Quantas tentativas podem ser feitas por palavra; como s�o computados os pontos; qual embaralhador ser� utilizado e em que momento; e etc... O importante � que independente do funcionamento, a classe Principal dever� interagir com ele da mesma forma.

