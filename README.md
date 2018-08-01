// برنامه ایی بنویسید که 2 عدد از ورودی خوانده و مجموع، تفریق،ضرب و تقسیم آن را در انواع داده ها نظیر اینتیجر دابل و بایت محاسبه کند

# Session4-Ex13
package com.personal.Ex13;

import java.util.Scanner;

public class Ex13 {

	public static void main(String[] args) {

		Ex13 ex13=new Ex13();
		int Xint=0,Yint=0;
		double Xdouble=0.0,Ydouble=0.0;
		byte Xbyte=0,Ybyte=0;
		int method=0;
		char c;
		String s;
		Scanner sc= new Scanner(System.in);


		
		System.out.println("Enter the two numbers");
		if(sc.hasNextInt()) {
			Xint=sc.nextInt();
			if(sc.hasNextInt()) {
				Yint=sc.nextInt();
				method=1;
				}
						}
		else if (sc.hasNextDouble() ){
			Xdouble=sc.nextDouble();
			if(sc.hasNextDouble()) {
				Ydouble=sc.nextDouble();
				method=2;
				}
						}
		else if (sc.hasNextByte() ){
			Xdouble=sc.nextByte();
			if(sc.hasNextByte()) {
				Ydouble=sc.nextByte();
				method=3;
				}
						}
		
		System.out.println("which operator do you want to exectute for them?");
		
		System.out.println("MULTIPLICATION(*) OR SUM(+) OR MINUS(-) OR DIVISION(/) ");
		s= sc.next();
		c=s.charAt(0);
		
		if (method==1) 
					
		System.out.println("The result is : "+ ex13.INT(Xint,Yint,c));
		
		else if (method==2) 
			
			System.out.println("The result is : "+ ex13.DOUBLE(Xdouble,Ydouble,c));
		else	
			System.out.println("The result is : "+ ex13.BYTE(Xbyte, Ybyte, c));
			
			
	
	}
	
	public int INT(int x,int y, char c) {
		
		if(c=='+')
			return x+y;
		else if(c=='*')
			return x*y;
		else if(c=='/')
			return x/y;
		else if(c=='-')
			return x-y;
	
		else return -1;
		
		
		}
	
public double DOUBLE(double x,double y, char c) {
		
		if(c=='+')
			return x+y;
		else if(c=='*')
			return x*y;
		else if(c=='/')
			return x/y;
		else if(c=='-')
			return x-y;
	
		else return -1;
		
		
		}

public byte BYTE(byte x,byte y, char c) {
	
	if(c=='+')
		return (byte) (x+y);
	else if(c=='*')
		return (byte) (x*y);
	else if(c=='/')
		return (byte) (x/y);
	else if(c=='-')
		return (byte) (x-y);

	else return -1;
	
	
	}

	

}
