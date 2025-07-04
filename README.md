import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        String userPlay;
        int numberGuess = random.nextInt(100);
        int numberUser;


        System.out.print("\nO jogo é simples !\neu irei gerar um número aleatório entre 0 e 100\ne você terá de advinhar qual é. ");
        System.out.print("\n");
        do {
            System.out.print("\nJogar ? ");
            userPlay = scanner.nextLine();

            if (userPlay.trim().equalsIgnoreCase("Sim")){
                System.out.print("\nVAMOS COMEÇAR !");
                System.out.print("\n");
            } else {
                System.out.print("\nPrograma Encerrado.");
                break;
            }

            System.out.print("\nDigite um Número: ");
            numberUser = Integer.parseInt(scanner.nextLine());
            System.out.print("\n");
            if (numberUser == numberGuess){
                System.out.print("Número Digitado: " + numberUser);
                System.out.print("\n");
                System.out.print("\nNúmero Gerado: " + numberGuess);
                System.out.print("\n");
                System.out.print("\nSucesso !\nVocê Acertou em Cheio");
                System.out.print("\n");
                } else {
                System.out.print("Número Digitado: " + numberUser);
                System.out.print("\n");
                System.out.print("\nNúmero Gerado: " + numberGuess);
                System.out.print("\n");
                System.out.print("\nNão Foi Dessa Vez\nMais Sorte na Próxima.");
                System.out.print("\n");
            }
        }while (!userPlay.trim().equalsIgnoreCase("Não"));

    }
}
