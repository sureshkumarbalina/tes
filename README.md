public void allmob() throws InterruptedException
        {
            System.setProperty("webdriver.chrome.driver","C:\\Users\\meghana.ds\\Downloads\\chromedriver_win32//chromedriver.exe");
            WebDriver driver=new ChromeDriver();
            driver.get("https://mobileworld.azurewebsites.net/");
            Thread.sleep(2000);
            driver.findElement(By.xpath("//button[@class='btn btn-warning my-2 my-sm-0']")).click();
            driver.findElement(By.id("username")).sendKeys("Meghana");
            driver.findElement(By.cssSelector("input[type='password']")).sendKeys("hachiko");
            Thread.sleep(2000);
            driver.findElement(By.xpath("//a[@class='btn btn-primary btn-block']")).click();
            Thread.sleep(2000);
            driver.findElement(By.linkText("All Mobiles")).click();
            Thread.sleep(2000);
            driver.findElement(By.linkText("Order")).click();
            Set<String>window=driver.getWindowHandles();  //window handling
            Iterator<String>it=window.iterator(); //parent window to child window
            String parentId=it.next();
            String childId=it.next();
            driver.switchTo().window(childId);
            driver.findElement(By.xpath("//input[@class='form-control']")).sendKeys("Meghana");
            driver.findElement(By.xpath("/html/body/div[1]/div/div[2]/form/div[1]/div[2]/input")).sendKeys("DS");
            driver.findElement(By.xpath("//input[@id='inputEmail']")).sendKeys("meghanads@gmail.com");
            driver.findElement(By.xpath("//input[@type='password']")).sendKeys("meghana");
            driver.findElement(By.id("flexRadioDefault2")).isEnabled();
            driver.findElement(By.xpath("//*[@id=\"myForm\"]/div[3]/div[4]/input")).sendKeys("9035844424");
            driver.findElement(By.xpath("//input[@placeholder='12 Apartment or floor']")).sendKeys("#285 7th cross");
            driver.findElement(By.xpath("//input[@placeholder='Main St']")).sendKeys("Nagaarbhavi");
            driver.findElement(By.id("inputCity")).sendKeys("Banglore");
            WebElement staticDropdown=driver.findElement(By.id("inputState"));
            Select dropdown=new Select(staticDropdown);
            dropdown.selectByIndex(2);
            driver.findElement(By.id("inputZip")).sendKeys("560071");
            driver.findElement(By.xpath("//input[@rel='lenovo']")).click();
            driver.findElement(By.cssSelector("input[placeholder='no of mobiles']")).sendKeys("1");
            WebElement staticDropdow=driver.findElement(By.id("bought"));
            Select dropdow=new Select(staticDropdow);
            dropdow.selectByIndex(1);
            driver.findElement(By.id("gridCheck1")).click();
            driver.findElement(By.xpath("//button[@data-toggle='modal']")).click();
            Thread.sleep(2000);
            driver.findElement(By.linkText("Close")).click();
