package okan5;

import java.util.Scanner;

public class okan52 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		// iki veri yarat kilo ve boy
		double kilogirdipound, boygirdiinch;
		final double KILOGRAMS_PER_POUND = 0.45359237; // Constant
		final double METERS_PER_INCH = 0.0254 ; // Constant
		
		
		
		//bmi hesap sonucu icin veri yarat
		double bmisonucu, kilogirdikg, boygirdimetre;
		
		// kullanıcıdan iki deger iste
		Scanner input = new Scanner (System.in);
		System.out.println("Kilonuzu pound giriniz");
		kilogirdipound = input.nextDouble();
		System.out.println("Boyunuzu inch giriniz");
		boygirdiinch = input.nextDouble();
		
		kilogirdikg = kilogirdipound * KILOGRAMS_PER_POUND;
		boygirdimetre = boygirdiinch * METERS_PER_INCH;
		System.out.println("Kilonuz = " + String.format("%.2f",kilogirdikg ) +
				"boyunuz =" + String.format("%2f",boygirdimetre*100)+ "cm");
		
		// bmi hesabı yap
		
			bmisonucu = kilogirdikg / (boygirdimetre * boygirdimetre);
			//bmi sonuca göre mesaj
			
			System.out.println("BMI sonuc=" + bmisonucu);
			if (bmisonucu < 18.5)
				System.out.println("underweight");
			else if (bmisonucu < 25)
				System.out.println("normal");
			else if (bmisonucu < 30 )
				System.out.println("underweight");
			else
				System.out.println("obese");
}
}
