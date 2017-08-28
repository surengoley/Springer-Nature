# Springer-Nature

Assignement_QA this peiece of code is to test the seacrh bar functionality on Spinger.com

package firstTest; import org.openqa.selenium.WebDriver; import org.openqa.selenium.By; import org.openqa.selenium.chrome.ChromeDriver; import org.openqa.selenium.WebElement;

public class springerlink {

public static void main(String[] args) throws Exception {
	
	System.setProperty("webdriver.chrome.driver","C:\\chromedriver.exe");
	WebDriver driver = new ChromeDriver();
	
	driver.get("http://link.springer.com");
	System.out.println("Springer Home page opened");
	WebElement element = driver.findElement(By.name("query"));
	element.sendKeys("Mind");
	System.out.println("Accepted the input string");
    element.submit();
    System.out.println("Displays all articles related to the keyed word");
    Thread.sleep(100);        
    driver.get("http://link.springer.com");
	System.out.println("Springer Home page opened");
	WebElement element1 = driver.findElement(By.name("query"));
	element1.sendKeys("&&&&&&&");
	System.out.println("Accepted invalid  input string");
    element1.submit();
    System.out.println("Displays articles if there any related to the keyed word else displays\n Sorry – we couldn’t find what you are looking for. Why not.. ");
    Thread.sleep(60);
    
    driver.get("http://link.springer.com");
	System.out.println("Springer Home page opened");
	WebElement element2 = driver.findElement(By.name("query"));
	element2.sendKeys(" ");
	System.out.println("No string value entered in search box");
    element2.submit();
    System.out.println("Displays all available articles ");
    Thread.sleep(220);
    
    
    
    driver.quit();
	// TODO Auto-generated method stub

}
}

