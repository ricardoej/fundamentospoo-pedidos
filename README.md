# Sistema de Pedidos de Restaurante

## Descrição

Neste exercício, você vai criar um sistema para gerenciar diferentes tipos de pedidos em um restaurante utilizando herança em Java. O objetivo é entender como a herança pode ser usada para criar uma hierarquia de classes e compartilhar atributos e métodos comuns, além de implementar funcionalidades específicas para cada tipo de pedido.

Você vai implementar um sistema que gerencia diferentes tipos de pedidos em um restaurante. A classe base será `Pedido`, e haverá três subclasses: `PedidoBebida`, `PedidoComida` e `PedidoSobremesa`. Cada tipo de pedido terá atributos e métodos específicos além dos atributos e métodos comuns definidos na classe `Pedido`.

## Classes a serem implementadas

### Pedido
- **Atributos:**
  - `id` (int)
  - `descricao` (String)
  - `preco` (double)
- **Métodos:**
  - Construtor que inicializa `id`, `descricao` e `preco`
  - Getters e setters para os atributos
  - Método abstrato `calcularValorTotal()` que deve ser implementado pelas subclasses

### PedidoBebida (subclasse de Pedido)
- **Atributos:**
  - `tamanho` (String) // Pequeno, Médio, Grande
- **Métodos:**
  - Construtor que inicializa `id`, `descricao`, `preco` e `tamanho`
  - Getters e setters para o atributo `tamanho`
  - Implementa o método `calcularValorTotal()` para adicionar uma taxa baseada no tamanho da bebida. Se a bebida for pequena, não deve ser adicionado taxa. Se a bebida for médio, adicionar R$2,00 no valor. Se a bebida for grande, adicionar R$3,50 no valor.

### PedidoComida (subclasse de Pedido)
- **Atributos:**
  - `quantidade` (int)
- **Métodos:**
  - Construtor que inicializa `id`, `descricao`, `preco` e `quantidade`
  - Getters e setters para o atributo `quantidade`
  - Implementa o método `calcularValorTotal()` para calcular o valor total baseado na quantidade de comida. O preço da comida é calculado com o preço da comida multiplicado pela quantidade.

### PedidoSobremesa (subclasse de Pedido)
- **Atributos:**
  - `comAdicional` (boolean)
- **Métodos:**
  - Construtor que inicializa `id`, `descricao`, `preco` e `comAdicional`
  - Getters e setters para o atributo `comAdicional`
  - Implementa o método `calcularValorTotal()` para adicionar um valor extra se houver adicional. Se houver adicional, você deve adicionar R$5,00 no preço.

## Passos para implementar

1. **Criar a classe Pedido**
2. **Criar a classe PedidoBebida**
3. **Criar a classe PedidoComida**
4. **Criar a classe PedidoSobremesa**
5. **Criar a classe Main para testar o sistema**

## Objetivo

Entender como a herança permite criar subclasses especializadas e compartilhar comportamento comum através da superclasse, facilitando a reutilização de código e a implementação de funcionalidades específicas para cada tipo de pedido.

## Instruções

1. Implemente todas as classes conforme descrito acima.
2. Compile e execute a classe `Main` para testar o sistema.
3. Verifique se o valor total dos pedidos é calculado corretamente de acordo com as regras específicas de cada tipo de pedido.
