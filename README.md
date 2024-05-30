import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Введите количество тарелок: ");
        float plate = sc.nextFloat();
        System.out.print("Введите количество моющего средства: ");
        float wisher = sc.nextFloat();
        if (wisher > 0 && plate > 0) {
            do {
                System.out.println("осталось: " + wisher);
                wisher -= 0.5;
                plate--;
            }
            while (wisher >= 0 && plate >= 0);
        }
        else if (wisher < 0 || plate < 0)
        {
            System.out.println("Неверно введено число");
        }
        if (wisher == 0)
        {
            System.out.println("Не хватает средства");
        }
        if (plate == 0)
        {
            System.out.println("Мыть нечего");
        }
    }
}
