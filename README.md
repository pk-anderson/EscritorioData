#        Loja De Roupa (LOLUCCI BOUTIQUE). 
# Banco de dados relacional para uma Loja de Roupas
# 
#===================================================================
# Levantamento de requisitos
#===================================================================

Temos uma loja de roupas e cosméticos.

As donas desta loja administram funcionários,  clientes e produtos. Por possuirem alguns funcionários, é necessário armarzenar nome, CPF, endereço, telefone, salário, setor de trabalho e sua matrícula que o distingua dos demais dentro da loja. Há uma especialização desta entidade em gerente que exercem maior responsabilidade os demais sendo-lhes atribuído as funções:

    a) Administrar receitas, armazenando no banco os tipos de receita, a data de recebimento, uma pequena descrição da receita e a matrícula do gerente responsável;
    
    b) Administrar despesas, armazendo os tipos de pagamento, datas de pagamento, uma pequena descrição da despesa e a matrícula do gerente responsável;
    
    c) Celebrar contratos, sendo que destes é armazenados o nome da marca contrante, CNPJ da empresa, e-mail e telefone para contato, e a matrícula do gerente responsável.

Os gerentes podem realizar as compras dos produtos que serão comercializados na loja. Para cada compra, será necessário armazenar o tipo de produtos, quantidade dos produtos, valor pago na compra e a data na qual a compra fora realizada. Estas compras realizam alterações na quantidade do número de peças no estoque da loja.

Os funcionários da loja realizam vendas, sendo que para cada venda é necessário armazenar a matrícula do funcionário que realizou a venda, o CPF do cliente, o número de referência do produto, a nota fiscal, número de parcelas, data de pagamento, data da compra, preço do produto e valor pago no final da venda.

As vendas são realizadas para os clientes. Para estes, são armazenados o nome, o cpf, documento de indentidade, endereço, estado de adimplência, produtos que foram comprados, telefone. Para as vendas, são armazenadas a matrícula do funcionário que realizou a venda, o CPF do cliente que comprou, o número de referência dos produtos vendidos, a nota fiscal da venda, o número de parcelas, a data da última parcela que foi paga e a data de vencimento da próxima parcela, o valor total da venda junto com a data de sua realização.

Estas vendas carregam consigo o preço unitáro de cada produto que está sendo comprado pelo cliente e provocam alterações na quantidade do estoque da loja. Este último, por sua vez, armazena os tipos de produtos disponíveis e mostra suas respectivas quantidades.

O estoque contém os produtos disponíveis para serem comercializados na loja e cada produto possui uma referência e um código, além de serem armazenados o nome, preço, classe, descrição e a marca. Os produtos vendidos na loja podem ser peças de roupas ou cosméticos. Para as roupas é preciso armarzenar o tamanho das peças, o tipo das peças e o gênero a qual vestem. Para os cosméticos deve ser armazenado o tipo do produto.

#===================================================================
# Consultas
#===================================================================

1. Lista de todos os funcionários;
2. Lista de quais funcionários são os gerentes;
3. Listas de contratos realizados;
4. Lista de contratos por gerentes que os relizaram;
5. Lista de todas as receitas;
6. Lista de receitas por gerentes que as administrou;
7. Lista de todas as despesas;
8. Lista de despesas por gerente que as administrou;
10. Lista de contratos por empresas contrantes;
11. Lista de todas as vendas que foram realizadas;
12. Lista de vendas realizadas por funcionários;
13. Lista de vendas realizadas com base no cliente;
14. Lista de todos os clientes;
15. Lista de todas as compras;
16. Lista de todas as compras por tipo;
17. Lista dos tipos de produtos disponíveis no estoque;
18. Lista de todos os produtos;
19. Lista de produtos por referência;
20. Lista de produtos por código;
21. Lista de clientes que estão inadimplentes com a loja;

#===================================================================
# Dicionário conceitual de dados
#===================================================================

#Entidades

Entidade Funcionários:

    Entidade principal que armazena informações e relacionamenos mais genéricos sobre os funcionários da loja.
    
    -Atributos:
    
        - Matrícula: armazena o número da matrícula do funcionário dentro da loja;
        
        - Nome: armazena o nome do funcionário;
        
        - CPF: armazena o número do CPF do funcionário;
        
        - Telefone: armazena o telefone do funcionário;
        
        - Endereço: armazena o endereço do funcionário;
        
        - Salário: armazena o valor que o funcionário recebe mensalmente;
       
        - Setor: armazena o setor onde o funcionário trabalho.
        
Entidade Gerente:

    Especialização da entidade funcinário e possue todos os atributos da entidade principal e armazena todas as informações dos gerentes da loja. Não há nenhum atributo específico.
    
Entidade Venda:

    Entidade que armazena as informações das vendas que ocorrem na loja. 
    
    -Atributos:
    
    - Matrícula: armazena a matrícula do funcionário que realizou a venda;
    
    - CPF_do_cliente: armazena o CPF do cliente que realizou uma compra na loja;
    
    - Ref_do_produto: **armazena as referências dos produtos que foram vendidos (OLHAR ISSO AQUI!);**
    
    - Nota_fiscal: armazena o número da nota fiscal que fora emitida naquela venda;
    
    - Parcelas: armazena o número de parcelas da venda, as quais serão pagas pelo cliente;
    
    - Parcela_atual: armazena a data na qual foi paga a parcela mais recente da venda;
    
    - Próxima_parcela: armazena a data do próxima parcela a ser paga pelo cliente;
    
    - Data_da_venda: armazena a data que foi realizada a venda;
    
    - Valor_da_venda: armazena o valor total da venda;
    
    - Preço_do_produto: armazena os preços unitários que compõem a venda. (OLHAR ISSO AQUI!)
    
Entidade Cliente:

    Armazena as informações sobre os clientes que realizaram compras na loja.
    
    - Atributos:
    
    -  Nome: armazena o nome do cliente;
    
    -  CPF: armazena o CPF do cliente;
    
    -  Endereço: armazena o endereço do cliente;
    
    -  Status: armazena o estado de adimplência do cliente com a loja;
    
    -  Telefone: armazena o telefone do cliente;
    
    -  Número_do_RG: armazena o número do documento de registro geral do cliente.
      
Entidade Compra:

    Armazena as informações sobre as compras de produtos para compor o estoque da loja, realizadas pelos gerentes.
    
    - Atributos:
    
    - Tipo_de_produto: armazena o tipo do produto que foi comprado;
    
    - Quantidade: armazena a quantidade de produtos de cada tipo que foram comprados;
    
    - Valor: armazena o valor total da compra realizada;
    
    - Data_da_compra: armazena a data que foi realizada a compra.
    
Entidade Estoque:

    Armazena as informações sobre o estoque de produtos que estão disponíveis na loja.
    
    - Atributos:
    
    - Quantidade: armazena a quantidade de cada produto disponíveis na loja;
    
    - Tipo_de_produto: armazena o tipo de produto disponível na loja.
    
Entidade Produto:

    Entidade geral que armazena as informações sobre os produtos que serão comercializados na loja.
    
    - Atributos:
    
    - Referência: armazena o número de referência do produto;
    
    - Preço: armazena o valor de cada produto;
   
    - Código_do_produto: armazena o código do produto;
    
    - Descrição: armazena uma pequena descrição das características dos produtos;
    
    - Marca: armazena a marca do produto.
    
Entidade Cosmético:

    Especialização da entidade produto que corresponde aos cosméticos que são comercializados na loja.
    
    - Atributos:
    
    - Tipo_do_produto: armazena o tipo de cosmético.
    
Entidade Roupa:

    Especialização da entidade produto que corresponde às roupas que são comercializadas na loja.
    
    - Atributos:
    
    - Tamanho: armazena o tamanho da peça de roupa;
    
    - Tipos_das_peças: armazena o tipo das peças de roupas;
    
    - Gênero: armazena se a roupa é para o gênero masculino, feminino ou unissex.
    
Entidade Receita:

    Armazena as informações das receitas que dão entrada na loja.
    
    - Atributos:
    
    - Tipos_de_receitas: armazena o tipo de receitas da loja;
    
    - Matrícula_do_gerente: armazena a matrícula do gerente que administrou aquela receita;
    
    - Descrição: armazena uma pequena descrição da receita que está entrado em caixa;
    
    - Data_de_recebimento: armazena a data de recebimento da receita.
    
Entidade Despesa:

    Armazena as informações das despesas da loja.
    
    - Atributos:
    
    - Data_de_pagamento: armazena a data de pagamento daquela despesa;
    
    - Matrícula_do_gerente: armazena a matrícula do gerente que administrou aquela despesa;
     
    - Descrição: armazena uma pequena descrição da despesa que está sendo executada;
    
    - Tipo_de_despesa: armazena o tipo de despesa que está sendo execultada.
    
Entidade Contrato:

    Armazena as informações dos contratos que foram celebrados pela loja com fornecedores e demais marcas parceiras do estabelecimento.
    
    - Atributos:
    
    - Nome_da_marca: armazena o nome da marca contratante;
    
    - CNPJ: armazena o CNPJ da marca contratante;
    
    - Matrícula_do_gerente: armazena a matrícula do gerente que celebrou aquele contrato;
    
    - E-mail: armazena o e-mail para contato com a marca contratante;
    
    - Telefone: armazena o telefone para contato com a marca contratante.

#Relacionamentos
    
 
