# DNA-pattern
I  have dna pattern in java
dna pattern:


import java.io.*; 
class Main { 
static void printUpperHalf(String str) 
{ 
	char first, second; 
	int pos = 0; 
	for (int i = 1; i <= 4; i++) { 
		first = str.charAt(pos); 
		second = str.charAt(pos+1); 
		pos += 2; 
		
		for (int j = 4 - i; j >= 1; j--) 
			System.out.print(" "); 
		System.out.print(first); 
		for (int j = 1; j < i; j++) 
			System.out.print("  "); 
		System.out.println(second); 
	} 
} 
static void printLowerHalf(String str) 
{ 
	char first, second; 
	int pos = 0; 
	for (int i = 1; i <= 4; i++) { 

		first = str.charAt(pos); 
		second = str.charAt(pos+1); 
		pos += 2; 
		
		for (int j = 1; j < i; j++) 
			System.out.print(" "); 
		System.out.print(first); 
		for (int j = 4 - i; j >= 1; j--) 
			System.out.print("  "); 
		System.out.println(second); 
	} 
} 
static void printDNA(String str[], int n) 
{ 
	for (int i = 0; i < n; i++) { 

		int x = i % 6; 
		if (x % 2 == 0) 
			printUpperHalf(str[x]); 
		else
			printLowerHalf(str[x]); 
	} 
} 
public static void main (String[] args) { 
	int n = 8; 

	String DNA[] = { "********", "********", "********", 
				"********", "********", "********" }; 
	printDNA(DNA, n); 
			
	} 
}


