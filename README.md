#        Loja De Roupa (LOLUCCI BOUTIQUE). 
# Banco de dados relacional para uma Loja de Roupas
# 
Temos uma loja de roupas e cosméticos. 
As donas desta loja administram funcionários,  clientes e produtos. Por possuirem alguns funcionários, é necessário armarzenar nome, CPF, endereço, telefone, salário, setor de trabalho e sua matrícula que o distingua dos demais dentro da loja. Há uma especialização desta entidade em gerente que exercem maior responsabilidade os demais sendo-lhes atribuído as funções:

    a) Administrar receitas, armazenando no banco os tipos de receita e a data de recebimentos;
    
    b) Administrar despesas, armazendo os tipos de pagamento e datas de pagamento, e investimentos realizados para a manutenção e melhoria da qualidade do atendimento no espaço;
    
    c) Celebrar contratos, sendo que destes é armazenados o nome da marca contrante, CNPJ da empresa, e-mail e telefone para contato.
Os gerentes podem realizar as compras dos produtos que serão comercializados na loja. Para cada compra, será necessário armazenar o tipo de produtos, quantidade dos produtos, valor pago na compra e a data na qual a compra fora realizada. Estas compras realizam alterações na quantidade do número de peças no estoque da loja.

Os funcionários da loja realizam vendas, sendo que para cada venda é necessário armazenar a matrícula do funcionário que realizou a venda, o CPF do cliente, o número de referência do produto, a nota fiscal, número de parcelas, data de pagamento, data da compra, preço do produto e valor pago no final da venda.

As vendas são realizadas para os clientes. Para estes, são armazenados o nome, o cpf, documento de indentidade, endereço, estado de adimplência, produtos que foram comprados, telefone.

Estas vendas carregam consigo o preço unitáro de cada produto que está sendo comprado pelo cliente e provocam alterações na quantidade do estoque da loja. Esta última, por sua vez, armazena os tipos de produtos disponíveis e mostra suas respectivas quantidades.

O estoque contém os produtos disponíveis para serem comercializados na loja e cada produto possui uma referência e um código, além de serem armazenados o nome, preço, classe, descrição e a marca. Os produtos vendidos na loja podem ser peças de roupas ou cosméticos. Para as roupas é preciso armarzenar o tamanho das peças, o tipo das peças e o gênero a qual vestem. Para os cosméticos deve ser armazenado o tipo do produto.
