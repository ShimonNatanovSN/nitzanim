מחרוזות - חלק 1:
import java.util.Scanner;
public class StringPart1 {
	public static void main(String[] args) {
		//מתודה סטטית המקבלת מחרוזת ומחזירה מחרוזת זהה לחלוטין שרק שכל אות במחרוזת המקורית שהיא אות קטנה תהפוך לגדולה ולהפך 
		Scanner in = new Scanner(System.in);
		
		String str = "abc@@  ABC";
		String tmp="";
		
		// לולאה שעוברת על כל תו במחרוזת
		for(int i = 0; i < str.length(); i++) {
			char ch = str.charAt(i);
			
			// אם התו הוא אות קטנה - הופכים לגדולה
			if(ch >= 'a' && ch <= 'z') {
				tmp += (char)(ch - 32); // הפרש בין אות קטנה לגדולה הוא 32
			}
			// אם התו הוא אות גדולה - הופכים לקטנה  
			else if(ch >= 'A' && ch <= 'Z') {
				tmp += (char)(ch + 32); // מוסיפים 32 כדי להפוך לקטנה
			}
			// אם התו אינו אות - משאירים כמו שהוא
			else {
				tmp += ch;
			}
		}
		
		System.out.println("Original string: " + str);
		System.out.println("Modified string: " + tmp);
		
		
	}
}
