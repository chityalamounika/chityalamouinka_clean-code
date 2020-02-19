# chityalamouinka_clean-code


//SimpleInterest

public class SimpleInterest
{
	float simpleInterestCalculator(float principle,float time,float rateOfInterest)
	{
		return ((principle*time*rateOfInterest)/100);
	}
}

//CompoundInterest
public class CompoundInterest
{
	double compoundInterestCalculator(float principle,float time,float rateOfInterest)
	{
		return (principle*Math.pow(1+(rateOfInterest/100),time));
	}
}

//EstimateConstructioncost

public class EstimateConstructionCost
{
	double calculateCost(int choice,float area)
	{
		double result=0;
		if(choice==1)
		{
			result=1200*area;
		}
		else if(choice==2)
		{
			result=1500*area;
		}
		else if(choice==3)
		{
			result=1800*area;
		}
		else if(choice==4)
		{
			result=2500*area;
		}
		return result;
	}
}

//Interest

import java.util.*;
public class Interest
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter 0 if you want to calculate Simple Interest and 1 if you want to calculate Compound Interest");
		int choice=sc.nextInt();
		float principle=0,time=0,rateOfInterest=0,n=0;
		if(choice==0 || choice==1)
		{
			System.out.println("Enter Principle");
			 principle=sc.nextFloat();
			System.out.println("Enter Time");
			 time=sc.nextFloat();
			System.out.println("Enter Rate Of Interest");
			 rateOfInterest=sc.nextFloat();
			
		}
		if(choice==0)
		{
			SimpleInterest simpleInterestObject=new SimpleInterest();
			float simpleInterestResult=simpleInterestObject.simpleInterestCalculator(principle,time,rateOfInterest);
			System.out.println("Result of simple interest is : "+simpleInterestResult);
		}
		if(choice==1)
		{
			CompoundInterest compoundInterestObject=new CompoundInterest();
			double compoundInterestResult=compoundInterestObject.compoundInterestCalculator(principle,time,rateOfInterest);
			System.out.println("Result of compound interest is : "+compoundInterestResult);
		}
		
		
//ConstructionDetails:

import java.util.*;
class ConstructionDetails
{
	public static void main(String args[])
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Menu for Material standards : ");
		System.out.println("1->Standard Materials");
		System.out.println("2->Above Standard Materials");
		System.out.println("3->High Standard Materials");
		System.out.println("4->High Standard Materials and fully automated home");
		System.out.println("Enter your choice");
		int choice = sc.nextInt();
		System.out.println("Enter total area of house(square feets)");
		float area=sc.nextFloat();
		EstimateConstructionCost object=new EstimateConstructionCost();
		double result=object.calculateCost(choice,area);
		System.out.println("Total cost : "+result);
	}
}
