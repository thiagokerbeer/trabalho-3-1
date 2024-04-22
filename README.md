

Documentação do Projeto CadastroPOO
Introdução
O projeto CadastroPOO implementa um sistema de cadastro de pessoas físicas e jurídicas utilizando programação orientada a objetos (POO) em Java. Este sistema foi atualizado para permitir interação com o usuário através de um menu em modo texto, oferecendo diversas funcionalidades, como inclusão, alteração, exclusão e exibição de dados, além de salvamento e recuperação dos dados em arquivos.

Estrutura do Projeto
A estrutura do projeto consiste nos seguintes elementos:

Classe Pessoa: Representa uma pessoa genérica, com atributos como ID e nome.
Classe PessoaFisica: Herda da classe Pessoa e representa uma pessoa física específica, com atributos adicionais como CPF e idade.
Classe PessoaJuridica: Herda da classe Pessoa e representa uma pessoa jurídica específica, com atributos adicionais como CNPJ.
Classe PessoaFisicaRepo: Gerencia uma lista de pessoas físicas. Possui métodos para inserir, alterar, excluir, obter e exibir pessoas físicas, além de persistir e recuperar os dados em arquivos.
Classe PessoaJuridicaRepo: Gerencia uma lista de pessoas jurídicas, seguindo a mesma estrutura do PessoaFisicaRepo.
Classe CadastroPOO: Classe principal que contém o método main e implementa a interação com o usuário através de um menu em modo texto.
