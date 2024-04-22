import java.io.*;
import java.util.*;

public class CadastroPOO {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        PessoaFisicaRepo repoFisica = new PessoaFisicaRepo();
        PessoaJuridicaRepo repoJuridica = new PessoaJuridicaRepo();

        int opcao;
        do {
            System.out.println("\n=== Menu ===");
            System.out.println("1. Incluir");
            System.out.println("2. Alterar");
            System.out.println("3. Excluir");
            System.out.println("4. Exibir pelo ID");
            System.out.println("5. Exibir todos");
            System.out.println("6. Salvar dados");
            System.out.println("7. Recuperar dados");
            System.out.println("0. Finalizar");
            System.out.print("Escolha uma opção: ");
            opcao = scanner.nextInt();
            scanner.nextLine(); // Limpar o buffer do scanner

            switch (opcao) {
                case 1:
                    System.out.println("\n1. Incluir");
                    System.out.println("1. Pessoa Física");
                    System.out.println("2. Pessoa Jurídica");
                    System.out.print("Escolha o tipo (1 ou 2): ");
                    int tipo = scanner.nextInt();
                    scanner.nextLine(); // Limpar o buffer do scanner
                    if (tipo == 1) {
                        incluirPessoa(scanner, repoFisica);
                    } else if (tipo == 2) {
                        incluirPessoa(scanner, repoJuridica);
                    } else {
                        System.out.println("Opção inválida!");
                    }
                    break;
                case 2:
                    // Implementar a opção de alterar
                    break;
                case 3:
                    // Implementar a opção de excluir
                    break;
                case 4:
                    // Implementar a opção de exibir pelo ID
                    break;
                case 5:
                    // Implementar a opção de exibir todos
                    break;
                case 6:
                    // Implementar a opção de salvar dados
                    break;
                case 7:
                    // Implementar a opção de recuperar dados
                    break;
                case 0:
                    System.out.println("Finalizando o programa...");
                    break;
                default:
                    System.out.println("Opção inválida!");
            }
        } while (opcao != 0);

        scanner.close();
    }

    private static void incluirPessoa(Scanner scanner, PessoaFisicaRepo repo) {
        System.out.println("Digite o ID:");
        int id = scanner.nextInt();
        scanner.nextLine(); // Limpar o buffer do scanner
        System.out.println("Digite o nome:");
        String nome = scanner.nextLine();
        System.out.println("Digite o CPF:");
        String cpf = scanner.nextLine();
        System.out.println("Digite a idade:");
        int idade = scanner.nextInt();
        scanner.nextLine(); // Limpar o buffer do scanner

        PessoaFisica pessoa = new PessoaFisica(id, nome, cpf, idade);
        repo.inserir(pessoa);
        System.out.println("Pessoa física incluída com sucesso!");
    }

    // Métodos para incluir, alterar, excluir, exibir pelo ID, exibir todos, salvar dados, recuperar dados
}
