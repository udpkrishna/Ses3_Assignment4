package AssignmentPack;

public class Ses3Assignment4 {

	int x;
	int y;
	int res;
	String str1;

	public void getNum(int l, int b) {
		x = l;
		y = b;
	}

	public int operation(String str) {
		str1 = str;
		switch (str) {
		case "+":
			res = x + y;
			break;
		case "-":
			res = x - y;
			break;
		case "*":
			res = x * y;
			break;
		case "/":
			res = x / y;
			break;
		default:
			System.out.println("Enter the right operator...");

		}
		return res;
	}

	public void dispNum() {
		System.out.println(
				"Enter no. is " + x + " and " + y + " operation performed is " + str1 + " and result is " + res);
	}

}

Tester package:
package Testerpack;

import java.util.Scanner;

import AssignmentPack.Ses3Assignment4;

public class TestSes3Assignment4 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Ses3Assignment4 v1 = new Ses3Assignment4();

		System.out.println("Enter the first no:");
		Scanner s1 = new Scanner(System.in);
		int l = s1.nextInt();

		System.out.println("Enter the secong no:");
		Scanner s2 = new Scanner(System.in);
		int b = s2.nextInt();

		v1.getNum(l, b);

		System.out.println("Enter the operation to be performated as (+,-,*,/_): ");
		Scanner s3 = new Scanner(System.in);
		String str = s3.nextLine();
		v1.operation(str);

		v1.dispNum();
	}

}

