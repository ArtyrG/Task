# Task
package www;

public class Strings {

	public static void main(String[] args) {

		// String s = new String();
		//
		// s = "1";
		//
		// String ss = new String("asd");
		//
		// String s2 = s;
		//
		// s = s.concat("2");
		//
		// System.out.println(s);

		// String x = "Java";
		// x.concat(" tJavar");
		// System.out.println(x);
		// System.out.println(x.concat(" tJavadsf"));
		//
		// x = x.toUpperCase();
		// System.out.println(x);
		//
		// String s1 = "1";
		// String s2 = "1вв"; // пуул
		//
		// String s3 = new Strung("32вы"); // и в пуул и объект
		//
		// s2 = s2.intern(); // ссылку на пуул принуждает
		//
		// System.out.println(s1 == s2);

		String s = "1234567abc";

		System.out.println(s.charAt(3));

		System.out.println(s.concat("xcfv"));

		System.out.println(s.equalsIgnoreCase("1234567ABC")); // забивает на регистр
																
		System.out.println(s.equals("1234567ABC"));

		System.out.println(s.length());

		System.out.println(s.replace('c', 'C')); // меняем один символ
		System.out.println(s.replace("abc", "ABC")); // меняем символы

		System.out.println(s.substring(0, 6)); // выводит первые 6 символов не включаю 6 символ
												 

		System.out.println(s.toString()); // объект в виде строки

		System.out.println(s.toLowerCase()); // в верхний регистр

		String s2 = "   xxx   ";
		System.out.println(s2);
		System.out.println(s2.trim() + "yyy"); // trim убирает пробелы в начале и конце
												 

		char c = '2';
		int i = c;
		System.out.println(i);
		System.out.println(s.indexOf(i)); // ищет символ и возращает индекс
		System.out.println(s.indexOf("56"));
		System.out.println(s.indexOf("56", 0));
		System.out.println(s.indexOf("56", 5));

		System.out.println(s.endsWith("abc")); // есть ли в конце abc

		System.out.println(s.startsWith("345", 2)); // 345 начинается ли строка с 345 с 2 символа
		
		String s3 = "123:456:234:6:";
		String[] sub = s3.split(":");
		for (String x : sub) {
			System.out.println(x); ///123 456 234 6
		}
		
		
		StringBuilder sBuilder; // меняет строку!!!
		StringBuffer sBuffer;
				
		sBuilder = new StringBuilder("Builder");
		sBuilder.append(s);			// добавляет s меняя строку
		System.out.println(sBuilder);
		
		
		long startString = System.currentTimeMillis();
		String ss = "";
		for(int j = 0; j < 10000; j++){
			ss += j;
		}
		System.out.println(System.currentTimeMillis() - startString);
		
		long startStringBulder = System.currentTimeMillis();
		StringBuilder sb = new StringBuilder();
		for (int j = 0; j < 100000; j++) {
			sb.append(j);
		}
		System.out.println(System.currentTimeMillis() - startStringBulder);
		
	}

}
