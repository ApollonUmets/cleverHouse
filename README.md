# cleverHouse
import java.util.Scanner;

public class Main {
    public static void main(String[] text) {
        Scanner cleverHouse = new Scanner(System.in);

        System.out.println("Введите текущее время, в часас от 0 до 23 :");
        int time = cleverHouse.nextInt();

        System.out.println("Введите текущий день недели");
        String day = cleverHouse.next();

        System.out.println("Укажите включена ли сигнализация : ");
        boolean onOff = cleverHouse.nextBoolean();

        if (( time == 8)  && (!onOff) && (!day.equalsIgnoreCase("Суботта"))
            && (!day.equalsIgnoreCase("Воскресенье"))) {
            System.out.println( "Поднимаю шторы в 8 часов!");

            System.out.println("Поднять шторы, если хозяева дома, сигнализация отключена");
        } else  if ((time == 11) && (!onOff) && ((day.equalsIgnoreCase("Суботта") ||
                (day.equalsIgnoreCase("Воскресенье"))))) {
            System.out.println("Поднять шторы в 11 часов!");

        } else if ((time ==20) && (onOff) && (!day.equalsIgnoreCase("Cуббота")
                && (!day.equalsIgnoreCase("Воскресенье")))) {
            System.out.println("Включить чайник!");
        } else {
            System.out.println("Функция с этими данны не предусмотрина");
        }

    }
}
