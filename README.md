# Lights Out

Este projeto é um jogo de lógica/puzzle chamado "Lights Out", desenvolvido utilizando React. O objetivo do jogo é apagar todas as luzes do tabuleiro.

## O Jogo

**Lights Out** é um jogo de lógica/puzzle jogado em uma grade de luzes individuais, que podem estar acesas ou apagadas. O puzzle é vencido quando todas as luzes são apagadas.

Você pode clicar em uma célula para alternar essa luz — mas isso também alterna a luz acima, à esquerda, à direita e abaixo dela. (Células na borda ou no canto não alternam tantas luzes, pois faltam alguns vizinhos).

## Código

Este jogo será construído a partir de três componentes:

### Design dos Componentes

- **App**: Como de costume, este é um componente muito simples. Ele apenas renderiza o componente `Board`.
- **Board**: O componente mais sofisticado. Ele manterá o estado que representa a grade de memória de verdadeiro/falso para luzes acesas/apagadas. Como o estado do tabuleiro vive aqui, é aqui que as chamadas `setState()` precisarão ser feitas — e, portanto, todas as funções que chamam `setState()`.
- **Cell**: Um componente mais simples. Ele simplesmente renderizará uma `<div>`, onde as classes CSS indicarão se esta célula está acesa ou apagada. Este é o que o usuário clica — mas precisará chamar uma função que recebe do `Board`, pois isso precisará atualizar o estado.

Quando o jogo é vencido, o tabuleiro não deve ser mostrado, mas uma simples mensagem "Você Venceu" deve aparecer em seu lugar.

Uma pequena quantidade de código é fornecida, mas há muitos lugares onde você precisará escrever código para tornar o jogo funcional.

## Estudo Adicional

### Propriedades Padrão

Adicione propriedades padrão para os tamanhos do tabuleiro e a probabilidade de uma luz no tabuleiro inicial estar acesa ou apagada.

### Melhorar o CSS

O CSS fornecido é suficiente para visualizar o jogo funcionando, mas pode ser melhorado de várias maneiras: melhores cores, formas arredondadas ou animações CSS podem torná-lo mais agradável.

### Garantir que um Jogo Seja Vencível

Dependendo do tamanho do seu tabuleiro, algumas configurações iniciais de luzes acesas/apagadas podem não ser realmente solucionáveis — o que é bastante cruel para seus usuários.

É relativamente difícil decidir se qualquer tabuleiro dado é solucionável (aqui está uma [leitura leve sobre este tópico](https://ida.mtholyoke.edu/xmlui/bitstream/handle/10166/693/375.pdf?sequence=1&isAllowed=y)) — mas há um truque simples para garantir que um tabuleiro inicial que você dá a um jogador seja solucionável.

Descubra como fazer isso.
