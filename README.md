# Write-a-Java-Program-to-count-the-number-of-words-in-a-string-using-HashMap.

import java.util.HashMap;
import java.util.Scanner;
public class WordCount {
    public static void main(String[] args) {
        String str;
        System.out.print("Enter String: ");
        Scanner sc=new Scanner(System.in);
        str=sc.nextLine();
        String[] split = str.split(" ");
        HashMap<String, Integer> map = new HashMap<String, Integer>();
        for (int i = 0; i < split.length; i++) 
        {
            if (map.containsKey(split[i]))
            {
                int count = map.get(split[i]);
                map.put(split[i], count + 1);
            } 
            else 
            {
                map.put(split[i], 1);
            }
        }
        System.out.println(map);
    }
}
