### Task 6 kyu

[Task link](https://www.codewars.com/kata/593e84f16e836ca9a9000054/)

You have to create a function namedone_two (oneTwo for Java or Preloaded.OneTwo for C#) that returns 1 or 2 with equal probabilities. one_two is already defined in a global scope and can be called everywhere.

Your goal is to create a function named one_two_three (oneTwoThree for Java or OneTwoThree for C#) that returns 1, 2 or 3 with equal probabilities using only the one_two function.

Do not try to cheat returning repeating non-random sequences. There is a randomness test especially for this case.




### My solution

```Java

import static preload.Preload.oneTwo;

public class Main {

    public static int oneTwoThree() {
        int a = oneTwo();
        int b = oneTwo();

        if (a == 1 && b == 1)
            return 1;
        if (a == 1 && b == 2)
            return 2;
        if (a == 2 && b == 1)
            return 3;

        return oneTwoThree();
    }

}

```

### Favourite solution from code-wars

```Java

import static preload.Preload.oneTwo;

public class Main {

    public static int oneTwoThree() {
        int count = 0;
        for(int i = 0;i<10;i++){
            count+=oneTwo();
        }
        switch (count){
            case 10:
                return 1;
            case 11:
                return 1;
            case 12:
                return 2;
            case 13:
                return 1;
            case 14:
                return 1;
            case 15:
                return 2;
            case 16:
                return 3;
            case 17:
                return 3;
            case 18:
                return 2;
            case 19:
                return 3;
            case 20:
                return 3;
            default:
                return 0;
        }
    }

}

```

This is crazy, ahah

# Have a nice day!