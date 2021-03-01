#        Loja De Roupa (LOLUCCI BOUTIQUE). 
# Banco de dados relacional para uma Loja de Roupas
# =================================================
#               Entidades:
# =================================================

1. Clientes
    # Nome
    # CPF (CHAVE)
    # Identidade
    # Endereço
    # Tel/Cel
    # Produtos 
    # Status
2.  Venda
    # CPF Cliente (CHAVE)
    # Ref Produto (CHAVE)
    # Nota Fiscal (CHAVE*)
    # Valor Pago
    # Preço Produto
    # Parcelas
    # Data de Compra
    # Data do Parcela
3.  Sócias
    # Nome
    # CPF (CHAVE)
    # Endereço
    # Telefone 
4. Estoque
    # Referencia (CHAVE)
    # Nome
    # Preço
    # Marca
    # Quantidade
    # Tipo
5. Funcionários
    # Nome
    # CPF (CHAVE)
    # Telefone
    # Salário
    # Endereço
6. Receitas
    # Pagamentos em espécie
    # Cartão de crédto ou débito
    # Cheque
    # Promissória(Carnê)   
7. Despesas
    # Contas de água e luz
    # Salários
    # Compra de mercadoria
    # Aluguel
8. Contratos
    # (.....)
9. Roupas
    # tamanho
    # tipo das peças
    # gênero
10. Comésticos
    # tipo do produto
    # (......)
# =================================================

Temos uma loja de Roupas e cosméticos. Uma loja de Roupas possui as donas/socias, funcionarios,  clientes e produtos. Ambos as 
sócias dessa loja possui o mesmo cargo chefe. O cadastro dos funcionários é composto pelo nome, cpf, telefone, seguido pelo salário a receber
e o endereço residencial. O cadastro de cada cliente é composto pelo seu nome, sobrenome, cpf, identidade, endereço que servirá tanto para entrega do produto quanto para cobrança, os produtos que o cliente compra na loja também são inseridos e um numero para contato. A loja também possui produtos, estes podendo variar de tipos entre peças de roupa e cosméticos, além dos tipos, cada produto possui uma referencia, nome, preço e marca. Cada produto comprado deverá ser associado ao comprador(cliente) que armazenará o CPF do cliente, a referencia do produto, nota fiscal, valor pago, parcelamento e data de compra. O banco de dados servirá para armazenar toda a movimentação de caixa da loja, guardando informações correspondentes às receitas e despesas que ali ocorrem, inclui-se aqui, os contratos realizados de representação comercial de determinada marca de roupa.

# =================================================
#               * = Possibilidade
# =================================================
    
