# BlackJack

1. Given 2 integer values greater than 0, return whichever is closest to 21 without going over 21. If they both go over 21 then return 0.

```java
public class Runner {
	
	public static int blackJack(int cards1, int cards2) {
		if (cards1 > 21 && cards2 > 21) {
			return 0;
		} else if (cards1 > 21 || cards2 > 21) {
			if (cards1 > 21) {
				return cards2;
			}else {
				return cards1;
			}
		} else {
			if ((21 - cards1) < (21 - cards2)) {
				return cards1;
			} else {
				return cards2;
			}
		}
	}

	public static void main(String[] args) {
		System.out.println(blackJack(18,21));
	}

}
```