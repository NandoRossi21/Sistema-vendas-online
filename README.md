#Sistema de Vendas Online - Diagrama de Classes
 Descrição:

Este projeto apresenta a modelagem de um sistema de vendas online utilizando UML, com foco em boas práticas de orientação a objetos.

 Conceitos aplicados
Herança (Usuario → Cliente)
Composição (CarrinhoDeCompras → ItemCarrinho)
Associação entre entidades
Enumeração (StatusPedido)
Encapsulamento de regras de negócio
 Principais classes
Usuario
Cliente
CarrinhoDeCompras
ItemCarrinho
Produto
Pedido
FormaDeEnvio
FormaDePagamento
 Regras de negócio importantes
O preço do produto é armazenado no ItemCarrinho para manter histórico
Pedido pode ser orçamento ou venda
Frete baseado no peso total dos produtos
Controle de status via enum


 Possíveis evoluções
Implementação em Java, C# ou Python
Integração com banco de dados
API REST para pedidos
Interface web

 Autor
Fernando 


Implementação em Java

## 💻 Implementação

O projeto foi implementado em Java seguindo os princípios de orientação a objetos, conforme o diagrama de classes.

Principais conceitos aplicados:
- Herança (Usuario → Cliente)
- Composição (CarrinhoDeCompras → ItemCarrinho)
- Encapsulamento de regras de negócio

### Exemplo: Classe Pedido

```java
public class Pedido {
    private String numero;
    private StatusPedido status;
    private boolean ehOrcamento;

    public void confirmarPedido() {
        this.status = StatusPedido.CONFIRMADO;
        this.ehOrcamento = false;
    }
}
