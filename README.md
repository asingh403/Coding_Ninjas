# Coding_Ninjas
Arranging Numbers


package SelenuimSession;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

/**
 * 
 * @author ASHUTOSH SINGH
 *
 */

public class AmazonClick {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.setProperty("webdriver.chrome.driver", 
                 "C:/chromedriver_win32/chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.amazon.in/");

		WebElement ele = driver.findElement(By.id("nav-link-shopall"));
		WebElement ele1 = driver.findElement(By.xpath("//*[@id=\"nav-flyout-
                                   shopAll\"]/div[2]/span[1]/span"));
		performClick(ele,ele1,driver);
		
	}
	
	/**
	 * The below method was created for genral purpose utility to pass the params as well as          
         *  the driver 
	 * @param ele
	 * @param ele1
	 * @param driver
	 */
		public static void performClick(WebElement ele,WebElement ele1,WebDriver driver) {
		Actions act=new Actions(driver);
		act.moveToElement(ele).perform();
		act.moveToElement(ele1).perform();

                //How to optimize the below web element ,please advice me.
		WebElement ele2 = driver.findElement(By.xpath("//*[@id=\"nav-flyout-
                                  shopAll\"]/div[3]/div[1]/div[1]/div/a[4]/span[1]"));
		ele2.click();
		
		
		}	

	}
