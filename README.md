Automating the Facebook login or registration page for a script or bot can be done using tools like Selenium or Puppeteer, which allow programmatic interaction with web pages. However, it's important to understand the terms of service of Facebook. Automating actions such as login or registration on Facebook may violate their policies, especially if used for spammy or unethical behavior, so be sure you comply with their rules.
package com.fb;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import java.util.Scanner;

public class Emni {

	public static void main(String[] args) throws InterruptedException 
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("Please enter the Email/Phone Number");
		String un=sc.next();
		System.out.println("Enter the Password");
		String pw=sc.next();
		WebDriver driver=new ChromeDriver();
		driver.get("https://www.facebook.com/");
		driver.findElement(By.name("email")).sendKeys(un);
		
		driver.findElement(By.id("pass")).sendKeys(pw);
		driver.findElement(By.name("login")).click();
	

	}

}
