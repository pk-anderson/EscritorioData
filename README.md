# EscritorioData
Banco de dados relacional para um escritório de advocacia
Entidades:
	                                
	Advogados                			

	Especialidades
		Civil			
		Criminal
		Tributário						
		
	Funcionários					
		Secretários;
		Estagiários;
		
	Clientes
		PF;
		PJ;


	Processos

	

	Consultoria
Temos um escritório. Um escritório possui advogados. Cada advogado possui um secretário e estagiários. 
Os advogados são especialistas em somente uma área de atuação. Seu cadastro no escritório é composto pelo seu nome, numero de inscrição na ordem,
CPF, email, telefone. Cada advogado é responsável por uma pasta de processos.
Os funcionarios do ambiente podem ser secretários ou estagiários. O cadastro dos secretários, é necessário que se tenha o seu nome, cpf, telefone para contato, NIT e salário.
Cada secretario trabalha para um advogado e é responsável por atender os clientes e marcar as consultas. Os estagiarios, são cadastrados com o números da sua inscrição
na ordem, nome, cpf, matricula e periodo no curso. 
Para os clientes será necessário o nome e telefone para contato. Os clientes podem ser possoas físicas ou empresas. Para as PF será necessário CPF, endereço
residencial. Para as empresas será necessário o CNPJ, o nome do representante, endereço da sede. Cada cliente pode estar conectado a um processo ou a uma consultoria.
Por sua vez, cada processo possui por um número e os honorários que advirão daquele, e está relacionado a um cliente e ao seu advogado especialista.
A consultoria, por sua vez, além dos relacionamentos de praxe, possui os valor da consulta e o horário que fora realizada.

