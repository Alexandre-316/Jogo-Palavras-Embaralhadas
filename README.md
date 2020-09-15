# Descrição do trabalho
Jogo das Palavras Embaralhadas:
O objetivo desse exercí­cio é criar um jogo onde partes de sua execução possam ser trocadas. 
O jogo é simples: 
É apresentado ao jogador uma palavra com as letras embaralhadas e o jogador deve tentar adivinhar a palavra correta. O jogo seré¡ jogado no próprio console e a lista de palavras utilizadas pode ser fixa (pelo menos 20).

A classe Scanner pode ser utilizada para ler a entrada do usuário no console. Ela deve ser criada da seguinte forma: Scanner in = new Scanner(System.in); e em seguida metodos como nextLine() ou nextInt() podem ser utilizados para recuperar o que foi digitado pelo usuário.

Passos

O jogo deve possuir os seguintes componentes com as seguintes responsabilidades: 

classe Principal: representa a classe com o metodo main(). Essa classe que é responsável por ler a entrada do usuário e por imprimir as informações no console. Nenhuma outra classe pode imprimir ou ler do console. 

Classe BancoDePalavras: classe que possui um metodo que retorna uma palavra retirada aleatóriamente de uma lista de palavras lida a partir de um arquivo.
 
Classe  Embaralhador: interface que representa classes reponsáveis por receber uma palavra e retornar ela embaralhada. Pelo menos duas implementações deverão ser feitas.
 
Classe FabricaEmbaralhadores: possui um metodo que retorna um embaralhador aleatóriamente. 

Classe MecanicaDoJogo: interface que representa o andamento e a lógica do jogo. Será responsável por ditar o andamento do jogo. Ela que vai dizer se o jogo acabou ou não, se o usuário acertou a palavra ou não,se o usuário pode tentar acertar a palavra novamente e qual foi a pontuaçãoo final do jogador. Pelo menos duas implementações dessa interface devem ser criadas. 

Classe FabricaMecanicaDoJogo: retorna a MecanicaDoJogo que deve ser utilizada. 

A classe Principal deve recuperar a instancia de MecanicaDoJogo de FabricaMecanicaDoJogo e não pode conter nenhuma referência direta a uma das implementações, apenas a interface. 

Da mesma forma, as implementações de MecanicaDoJogo devem recuperar os embaralhadores de FabricaEmbaralhadores e também não pode conter nenhuma referência direta a implementações de Embaralhador, apenas a interface. As implementações de embaralhador devem conter algoritmos para o embaralhamento de palavras. 
As implementações de MecanicaDoJogo devem retratar o andamento do jogo. Quantas tentativas podem ser feitas por palavra; como são computados os pontos; qual embaralhador será utilizado e em que momento; e etc... O importante é que independente do funcionamento, a classe Principal deverá interagir com ele da mesma forma.

