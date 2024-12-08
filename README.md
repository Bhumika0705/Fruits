# Fruits
It will arrange the fruits according to their alphabetical order in  java
public class Fruits {
    public Fruits() {
    }

    static void sortfruits(String[] fruits) {
        int n = fruits.length;

        for(int i = 0; i < n - 1; ++i) {
            int min_index = i;

            for(int j = i + 1; j < n; ++j) {
                if (fruits[j].compareTo(fruits[min_index]) < 0) {
                    min_index = j;
                }
            }

            String temp = fruits[i];
            fruits[i] = fruits[min_index];
            fruits[min_index] = temp;
        }

    }

    public static void main(String[] args) {
        String[] fruits = new String[]{"kiwi", "apple", "papaya", "mango"};
        sortfruits(fruits);
        String[] var2 = fruits;
        int var3 = fruits.length;

        for(int var4 = 0; var4 < var3; ++var4) {
            String val = var2[var4];
            System.out.print(val + " ");
        }

    }
}
