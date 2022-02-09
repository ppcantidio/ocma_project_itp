## Introdução
Esta aplicação tem como objetivo a implementação de um bot que funcione como um barco-pesqueiro em um jogo de simulação gerenciado pelo OCMA - Órgão de Controle do Meio Ambiente. Neste jogo, diversos barcos são lançados em meio a uma área de pesca com 3 espécies de peixe presentes: Robalo, Cioba e Tainha, cada um com um valor diferente no mercado, e com uma limitação do barco de somente capacitar 10 kg de peixe. Caso o pescador deseje continuar pescando deve ir ao porto mais próximo vender sua carga ou pagar multa por cada kg de peixe em excesso em seu barco. Por fim, vence o barco que alcançar o saldo máximo (R$10.000), ou tiver o maior saldo ao final de um número máximo de rodadas.

O intuito desta aplicação é portanto não somente programar um simples barco de pesca, como também criar o melhor método e algoritmo capaz de analisar e identificar as melhores ações para o bot, para que desta forma ele tenha a melhor performance e ganhe o jogo. Partindo deste princípio, foi pensado então diversas estratégias para alcançar tal objetivo. 

A priori, o bot busca armazenar os dados fornecidos pelo OCMA, de forma que possamos fazer comparações futuras, guardando o mapa da área de pesca, a posição dos bots adversários e do meu bot em matrizes distintas. Em seguida, são feitas diversas comparações condicionais, que irão definir a ação do bot, partindo como prioridade o bot verificar se está com estoque para pescar, já que comporta somente até 10kg de peixe, e caso contrário buscará um porto para vender sua carga. 
Caso esteja em condição de pescar, ele verifica o melhor ponto de pesca para se dirigir, partindo como prioridade os peixes com maior valor (Robalo > Cioba > Tainha). Caso ele passe por todas estas verificações e esteja acima de um ponto de pesca, ele então lança o comando de pescar. Ele repetirá essas ações todos os turnos até que um vencedor seja definido.

## Como rodar
### Para gerar os arquivos executaveis:

Windows:
```sh
mingw32-make.exe
```
Linux:
```sh
make
```
### Para dar inicio ao jogo:

Windows:
```sh
mingw32-make.exe run
```
Linux:
```sh
make run
```
