# StringClass
Repo to Study String Class Methods



public class StringClassMain {

	public static void main(String[] args) {
		
		//ways to create a string
		
		String word = "Life";// string literal
		String word1 = new String("Cloud");// new String

		System.out.println(word);
		System.out.println(word1);
		System.out.println("converting char array into String---------------------------------------");
		//converting char array into String
		char arr[] = {'h','o','m','e'};
		
		String ch = new String(arr);
		
		System.out.println(ch);
		System.out.println("to lower case---------------------------------------");
		//to lower case		
		System.out.println(ch.toLowerCase());
		
		System.out.println("to upper case	---------------------------------------");
		//to upper case		
		System.out.println(ch.toUpperCase());
		
		System.out.println("get char at index in String	---------------------------------------");
		//get char at index in String		
		System.out.println(ch.charAt(0));// h is the first char in ch
		
		System.out.println("if starts with	 h---------------------------------------");
		//if starts with	 h
		System.out.println(ch.startsWith("h"));//true
		
		System.out.println("if starts with	 h at specific index---------------------------------------");
		//if starts with	 h at specific index
		System.out.println(ch.startsWith("h",1));//false, the second char is "o"
		
		System.out.println("if ends with	 h at specific index---------------------------------------");
		//if ends with	 h at specific index
		System.out.println(ch.endsWith("e"));//true
		
		System.out.println("comparison using compareTo()---------------------------------------");
		//comparison using compareTo(), 0 is equal  != 0 is different
		String w = "Flag1";
		String v = "Flag";
		String x = "Flag1";
		String z = "flag";
		
		System.out.println(w.compareTo(v));//0
		System.out.println(w.compareTo(z));//-1 in this case lower or upper case is important
		System.out.println(w.compareTo(x));//-1
		
		System.out.println("comparison using compareToIgnoreCase()---------------------------------------");
		//comparison using compareToIgnoreCase()
		System.out.println(w.compareToIgnoreCase("flag"));//1 in this case lower or upper case is not important

		
		System.out.println("comparison using equals---------------------------------------");
		//comparison using equals
		System.out.println(w.equals(v));
		System.out.println(w.equals("flag"));//false, in this case lower or upper case is important
		System.out.println(w.equals(x));//false
		
		System.out.println("comparison using equalsIgnoreCase---------------------------------------");
		//comparison using equalsIgnoreCase
		System.out.println(w.equalsIgnoreCase("flag"));//true, in this case lower or upper case is not important
		
		System.out.println("returning hash code---------------------------------------");
		//hash code
		System.out.println(w.hashCode());
		
		System.out.println("returning index of character---------------------------------------");

		String text = "ABCADU";
		System.out.println(text.indexOf("U")); //5,  if value != 0 the value not exist
		
		System.out.println("returning index of character from specific index---------------------");

		String text1 = "ABCADU";
		System.out.println(text1.indexOf("A",1)); // 3

		
		System.out.println("get interval substring---------------------");

		String text2 = "CORONEL";
		System.out.println(text2.substring(1, 4)); // ORO, the second index is not included
		
		System.out.println("get substring starting by index---------------------");

		String text3 = "ABRAHAM";
		System.out.println(text3.substring(2)); //RAHAM
		
		
		System.out.println("if contains substring---------------------");

		String text4 = "hunting";
		System.out.println(text4.contains("hun")); //true, lower and upper case matter
		
		System.out.println("replace all---------------------");

		String text5 = "ABRAHAM";
		System.out.println(text5.replaceAll("A", "a")); //aBRaHaM
		
		System.out.println("split---------------------");

		String s = "Welcome to CUBA";
		String[] wordsg = s.split(" ");
		
		for (String string : wordsg) {
			System.out.println(string);
		}
		//or
		System.out.println(Arrays.toString(wordsg));
		
		System.out.println("trim---------------------");

		String ss = "   Welcome to CUBA  ";//delete white sapeces before and after string
		System.out.println(ss.trim());
		
		
		System.out.println("from string to char array---------------------");

		String sd = "Welcome to CUBA";
		System.out.println(Arrays.toString(sd.toCharArray()));

	}

}
