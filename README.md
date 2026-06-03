# Selenium Automation Java Showcase

**Written by Brian McCarthy**

This repository is a complete **Selenium WebDriver 4 Java automation guide** covering Java fundamentals, Selenium locators, WebElements, waits, advanced browser interactions, TestNG, Maven, Page Object Model, API tests, login tests, CI/CD, Git/GitHub, data-driven testing, and framework design from scratch.

All module information is displayed directly on the page. There are **no expandable arrows**, no hidden `<details>` sections, and no click-to-expand content.

---

## Course Content Table of Contents

| # | Module | Details |
|---:|---|---|
| 1 | [Introduction](#module-1---introduction) | Selenium purpose, WebDriver architecture, browser automation value, and framework goals. |
| 2 | [Setup and Configuration](#module-2---setup-and-configuration) | Java, Maven, IDE, Selenium dependencies, TestNG, drivers, and project setup. |
| 3 | [Variables and Data Types](#module-3---variables-and-data-types) | Java variables, strings, numbers, booleans, WebElements, and runtime data. |
| 4 | [Advanced Data Types](#module-4---advanced-data-types) | Arrays, lists, maps, sets, `List<WebElement>`, and structured test data. |
| 5 | [Comparison and Boolean Operators](#module-5---comparison-and-boolean-operators) | Assertions, equality checks, UI state validation, and compound test logic. |
| 6 | [Program Control Flow](#module-6---program-control-flow) | If/else, switch, loops, table iteration, product search, and pagination. |
| 7 | [Reusable Methods](#module-7---reusable-methods) | Methods, parameters, return values, reusable wait/click/type helpers, and utilities. |
| 8 | [Classes and OOP](#module-8---classes-and-oop) | Classes, objects, constructors, inheritance, interfaces, polymorphism, and POM. |
| 9 | [Exception Handling](#module-9---exception-handling) | Selenium exceptions, try/catch, stale elements, timeouts, click interception, and screenshots. |
| 10 | [Modules and Packages](#module-10---modules-and-packages) | Java package layout, Maven folder structure, pages, tests, utils, listeners, and resources. |
| 11 | [Working with Files](#module-11---working-with-files) | Properties, JSON, CSV, Excel, screenshots, downloads, uploads, and file validation. |
| 12 | [Inspecting Elements](#module-12---inspecting-elements) | DevTools, DOM, attributes, dynamic elements, iframes, and locator discovery. |
| 13 | [WebDriver Setup](#module-13---webdriver-setup) | Selenium setup, browser commands, WebDriverManager, Selenium Manager, and driver lifecycle. |
| 14 | [Multiple Browsers](#module-14---multiple-browsers) | Chrome, Firefox, Edge, headless mode, DriverFactory, browser parameters, and cross-browser execution. |
| 15 | [Finding Elements](#module-15---finding-elements) | ID, name, class, tag, link text, CSS, XPath, `findElement`, `findElements`, and scoped lookup. |
| 16 | [CSS Selectors](#module-16---css-selectors) | CSS ID, class, attribute, contains, starts-with, hierarchy, nth-child, and selector quality. |
| 17 | [XPath Locators](#module-17---xpath-locators) | Relative XPath, text, contains, starts-with, axes, parent, ancestor, sibling, and dynamic XPath. |
| 18 | [Working with WebElements](#module-18---working-with-webelements) | Click, type, clear, attributes, text, dropdowns, checkboxes, radio buttons, and state checks. |
| 19 | [Useful WebDriver Methods](#module-19---useful-webdriver-methods) | URL, title, cookies, page source, screenshots, window state, attributes, and broken link checks. |
| 20 | [Wait Types](#module-20---wait-types) | Implicit wait, explicit wait, FluentWait, ExpectedConditions, Ajax waits, and synchronization. |
| 21 | [Advanced Interactions](#module-21---advanced-interactions) | JavaScriptExecutor, scrolling, calendars, tables, autocomplete, dynamic dropdowns, and totals. |
| 22 | [File Upload and Download](#module-22---file-upload-and-download) | Upload with `sendKeys`, Chrome download preferences, file existence checks, and download validation. |
| 23 | [Windows and Iframes](#module-23---windows-and-iframes) | Alerts, prompts, child windows, tabs, iframe switching, nested frames, and focus handling. |
| 24 | [Actions Class](#module-24---actions-class) | Hover, drag-and-drop, right-click, double-click, keyboard actions, and composite user interactions. |
| 25 | [Logging Infrastructure](#module-25---logging-infrastructure) | Log4j2, file logs, console logs, action logs, framework debugging, and CI troubleshooting. |
| 26 | [TestNG Infrastructure](#module-26---testng-infrastructure) | TestNG annotations, groups, XML suites, DataProvider, parameters, listeners, and parallel tests. |
| 27 | [JUnit / Pytest Equivalents](#module-27---junit--pytest-equivalents) | JUnit 5 and TestNG alternatives to Python test frameworks. |
| 28 | [Framework Part 1](#module-28---framework-part-1) | Maven framework start, ecommerce flow, product selection, waits, cart, and checkout. |
| 29 | [Framework Part 2](#module-29---framework-part-2) | Page Object Model, PageFactory, abstract components, page actions, and POM refactoring. |
| 30 | [Framework Part 3](#module-30---framework-part-3) | BaseTest, global config, driver initialization, error tests, groups, and parallel execution. |
| 31 | [Framework Practice Exercise](#module-31---framework-practice-exercise) | End-to-end login, product, cart, checkout, confirmation, and refactoring practice. |
| 32 | [Data-Driven Testing](#module-32---data-driven-testing) | TestNG DataProvider, HashMap, JSON, Excel, CSV, and parameterized tests. |
| 33 | [Running Complete Test Suite](#module-33---running-complete-test-suite) | Maven commands, TestNG XML, smoke/regression suites, headless mode, and reports. |
| 34 | [Git and GitHub](#module-34---git-and-github) | Git config, commits, branches, remotes, push/pull, merge conflicts, and framework versioning. |
| 35 | [Jenkins CI/CD](#module-35---jenkins-cicd) | Jenkins pipeline, Git integration, Maven job, parameters, scheduled runs, artifacts, and reports. |
| 36 | [Conclusion](#module-36---conclusion) | Framework maturity roadmap and recommended next steps. |
| 37 | [API Tests](#api-tests-for-selenium-java-frameworks) | Rest Assured, backend validation, setup data, cleanup, and UI/API hybrid strategy. |
| 38 | [Login Tests](#login-tests-for-selenium-java-frameworks) | Valid login, invalid login, empty fields, locked users, logout, roles, and credential handling. |
| 39 | [Locator Reference Guide](#locator-reference-guide) | Locator priority, examples, anti-patterns, and best practices. |
| 40 | [Framework from Scratch](#building-a-selenium-java-framework-from-scratch) | Required files, folders, dependencies, BaseTest, DriverFactory, Page Objects, utilities, and CI/CD. |
| 41 | [Custom vs Pre-Built Frameworks](#build-from-scratch-vs-pre-built-frameworks) | When to build custom, when to use a starter, and popular Selenium Java framework stacks. |
| 42 | [Top 30 Interview Questions](#top-30-selenium-java-technical-interview-questions) | Selenium Java technical interview questions with code examples. |

---

## Module 1 - Introduction

Selenium WebDriver automates real browser behavior. It validates user workflows such as navigation, search, form submission, shopping cart actions, checkout, file upload, reporting, and error handling.

```java
WebDriver driver = new ChromeDriver();
driver.get("https://example.com");
System.out.println("Title: " + driver.getTitle());
System.out.println("URL: " + driver.getCurrentUrl());
driver.quit();
```

Expected result: Chrome opens, loads the site, prints the title and URL, and closes.

Best practices: keep tests readable, close browser sessions, use explicit waits, and refactor repeated code into framework utilities.

---

## Module 2 - Setup and Configuration

Required tools include Java JDK, Maven, IntelliJ/Eclipse, Selenium WebDriver, TestNG, Chrome/Firefox/Edge, Git, and Jenkins.

```xml
<dependencies>
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.21.0</version>
    </dependency>
    <dependency>
        <groupId>org.testng</groupId>
        <artifactId>testng</artifactId>
        <version>7.10.2</version>
        <scope>test</scope>
    </dependency>
    <dependency>
        <groupId>io.github.bonigarcia</groupId>
        <artifactId>webdrivermanager</artifactId>
        <version>5.8.0</version>
    </dependency>
</dependencies>
```

```java
public class SetupSmokeTest {
    @Test
    public void openBrowserTest() {
        WebDriver driver = new ChromeDriver();
        driver.get("https://example.com");
        Assert.assertEquals(driver.getTitle(), "Example Domain");
        driver.quit();
    }
}
```

Expected result: Maven downloads dependencies and TestNG runs the browser test successfully.

---

## Module 3 - Variables and Data Types

Variables store URLs, expected titles, browser names, timeout values, product names, numeric totals, and element states.

```java
String baseUrl = "https://example.com";
String expectedTitle = "Example Domain";
int timeoutSeconds = 10;
boolean headless = false;

driver.get(baseUrl);
Assert.assertEquals(driver.getTitle(), expectedTitle);
Assert.assertTrue(timeoutSeconds > 0);
Assert.assertFalse(headless);
```

```java
String priceText = "$149.99";
double price = Double.parseDouble(priceText.replace("$", ""));
Assert.assertTrue(price > 0);
```

Expected result: runtime values are stored, parsed, and validated cleanly.

---

## Module 4 - Advanced Data Types

Use arrays, lists, maps, and sets for browsers, users, products, links, table rows, and windows.

```java
List<String> expectedProducts = Arrays.asList("ZARA COAT 3", "ADIDAS ORIGINAL", "IPHONE 13 PRO");
List<WebElement> productCards = driver.findElements(By.cssSelector(".mb-3"));

for (WebElement card : productCards) {
    String productName = card.findElement(By.cssSelector("b")).getText();
    if (expectedProducts.contains(productName)) {
        card.findElement(By.cssSelector("button:last-of-type")).click();
    }
}
```

```java
HashMap<String, String> user = new HashMap<>();
user.put("email", "qa@example.com");
user.put("role", "admin");
Assert.assertEquals(user.get("role"), "admin");
```

Expected result: the framework processes groups of elements and structured test data.

---

## Module 5 - Comparison and Boolean Operators

Boolean logic validates UI state, text, URLs, and test outcomes.

```java
WebElement button = driver.findElement(By.id("login"));
Assert.assertTrue(button.isDisplayed() && button.isEnabled());

String currentUrl = driver.getCurrentUrl();
Assert.assertTrue(currentUrl.contains("dashboard") || currentUrl.contains("products"));
```

Expected result: tests pass only when expected browser or UI conditions are true.

---

## Module 6 - Program Control Flow

Control flow supports searching products, iterating tables, handling pagination, and branching based on conditions.

```java
List<WebElement> products = driver.findElements(By.cssSelector(".product"));
for (WebElement product : products) {
    String name = product.findElement(By.cssSelector(".product-name")).getText();
    if (name.equalsIgnoreCase("Laptop")) {
        product.findElement(By.cssSelector("button.add")).click();
        break;
    }
}
```

```java
boolean itemFound = false;
do {
    List<WebElement> rows = driver.findElements(By.cssSelector("table tbody tr"));
    itemFound = rows.stream().anyMatch(row -> row.getText().contains("Rice"));
    if (!itemFound) {
        driver.findElement(By.cssSelector("[aria-label='Next']")).click();
    }
} while (!itemFound);
```

Expected result: dynamic content is searched until the desired item is found.

---

## Module 7 - Reusable Methods

Reusable methods standardize click, type, wait, and text retrieval.

```java
public class ElementUtils {
    private WebDriver driver;
    private WebDriverWait wait;

    public ElementUtils(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    }

    public WebElement waitForVisible(By locator) {
        return wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
    }

    public void click(By locator) {
        wait.until(ExpectedConditions.elementToBeClickable(locator)).click();
    }

    public void type(By locator, String value) {
        WebElement element = waitForVisible(locator);
        element.clear();
        element.sendKeys(value);
    }
}
```

Expected result: tests use consistent wait-aware interactions.

---

## Module 8 - Classes and OOP

OOP enables reusable framework classes such as Page Objects, BaseTest, DriverFactory, and utilities.

```java
public abstract class AbstractComponent {
    protected WebDriver driver;
    protected WebDriverWait wait;

    public AbstractComponent(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    }

    public void waitForElementToAppear(By locator) {
        wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
    }
}
```

```java
public class ProductCataloguePage extends AbstractComponent {
    private By productsBy = By.cssSelector(".mb-3");

    public ProductCataloguePage(WebDriver driver) {
        super(driver);
    }

    public List<WebElement> getProductList() {
        waitForElementToAppear(productsBy);
        return driver.findElements(productsBy);
    }
}
```

Expected result: shared functionality is inherited by page classes.

---

## Module 9 - Exception Handling

Good exception handling improves debugging without hiding real failures.

```java
public void safeClick(By locator) {
    try {
        WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
        wait.until(ExpectedConditions.elementToBeClickable(locator)).click();
    } catch (ElementClickInterceptedException e) {
        WebElement element = driver.findElement(locator);
        ((JavascriptExecutor) driver).executeScript("arguments[0].click();", element);
    } catch (TimeoutException e) {
        throw new AssertionError("Element was not clickable: " + locator, e);
    }
}
```

```java
public static String captureScreenshot(WebDriver driver, String testName) throws IOException {
    File source = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
    String path = System.getProperty("user.dir") + "/screenshots/" + testName + ".png";
    FileUtils.copyFile(source, new File(path));
    return path;
}
```

Common exceptions: `NoSuchElementException`, `TimeoutException`, `StaleElementReferenceException`, and `ElementClickInterceptedException`.

---

## Module 10 - Modules and Packages

```text
src/test/java/
├── api/
├── base/
├── components/
├── factory/
├── listeners/
├── pages/
├── retry/
├── tests/
└── utils/
```

Expected result: setup, tests, page objects, API helpers, listeners, retry logic, and utilities are separated clearly.

---

## Module 11 - Working with Files

```properties
browser=chrome
baseUrl=https://example.com
headless=false
timeout=10
```

```java
public class ConfigReader {
    private static Properties properties = new Properties();

    static {
        try (FileInputStream input = new FileInputStream("src/test/resources/config.properties")) {
            properties.load(input);
        } catch (IOException e) {
            throw new RuntimeException("Unable to load config file", e);
        }
    }

    public static String get(String key) {
        return System.getProperty(key) != null ? System.getProperty(key) : properties.getProperty(key);
    }
}
```

Expected result: browser, URL, timeout, and environment values are read from configuration.

---

## Module 12 - Inspecting Elements

Inspect ID, name, `data-testid`, `aria-label`, visible text, parent-child relationships, dynamic attributes, and iframe boundaries.

```java
By email = By.id("userEmail");
By field = By.cssSelector("input[type='text']");
By submit = By.cssSelector("button[type='submit']");
By error = By.xpath("//div[contains(@class,'toast') and contains(text(),'Incorrect')]");
```

Best practices: prefer stable IDs and test-specific attributes, avoid absolute XPath, verify uniqueness, and check for iframes.

---

## Module 13 - WebDriver Setup

```java
WebDriver driver = new ChromeDriver();
driver.manage().window().maximize();
driver.get("https://example.com");
driver.navigate().to("https://www.selenium.dev");
driver.navigate().back();
driver.navigate().forward();
driver.navigate().refresh();
driver.quit();
```

```java
ChromeOptions options = new ChromeOptions();
options.addArguments("--start-maximized");
options.addArguments("--disable-notifications");
options.addArguments("--window-size=1920,1080");
WebDriver driver = new ChromeDriver(options);
```

---

## Module 14 - Multiple Browsers

```java
public class DriverFactory {
    public static WebDriver createDriver(String browser, boolean headless) {
        switch (browser.toLowerCase()) {
            case "firefox":
                FirefoxOptions firefox = new FirefoxOptions();
                if (headless) firefox.addArguments("--headless");
                return new FirefoxDriver(firefox);
            case "edge":
                EdgeOptions edge = new EdgeOptions();
                if (headless) edge.addArguments("--headless");
                return new EdgeDriver(edge);
            case "chrome":
            default:
                ChromeOptions chrome = new ChromeOptions();
                if (headless) chrome.addArguments("--headless=new");
                chrome.addArguments("--window-size=1920,1080");
                return new ChromeDriver(chrome);
        }
    }
}
```

```bash
mvn clean test -Dbrowser=chrome
mvn clean test -Dbrowser=firefox
mvn clean test -Dbrowser=edge -Dheadless=true
```

---

## Module 15 - Finding Elements

```java
driver.findElement(By.id("userEmail")).sendKeys("qa@example.com");
driver.findElement(By.name("email")).sendKeys("qa@example.com");
driver.findElement(By.className("login-btn")).click();
driver.findElement(By.linkText("Forgot link")).click();
driver.findElement(By.partialLinkText("Forgot")).click();
driver.findElement(By.tagName("h1")).getText();
driver.findElement(By.cssSelector("button[type='submit']")).click();
driver.findElement(By.xpath("//button[text()='Login']")).click();
```

```java
List<WebElement> links = driver.findElements(By.tagName("a"));
System.out.println("Total links: " + links.size());
```

---

## Module 16 - CSS Selectors

| Selector | Example |
|---|---|
| ID | `#userEmail` |
| Class | `.btn-primary` |
| Attribute | `input[type='text']` |
| Contains | `input[id*='Email']` |
| Starts with | `input[id^='user']` |
| Ends with | `input[id$='Email']` |
| Child | `form button` |
| nth child | `table tr:nth-child(2)` |

```java
By email = By.cssSelector("#userEmail");
By productCards = By.cssSelector("div.mb-3");
By addToCart = By.cssSelector(".card-body button:last-of-type");
By toast = By.cssSelector("#toast-container .toast-message");
```

---

## Module 17 - XPath Locators

| Pattern | Example |
|---|---|
| Attribute | `//input[@id='userEmail']` |
| Text | `//button[text()='Login']` |
| Contains | `//button[contains(text(),'Log')]` |
| Starts with | `//input[starts-with(@id,'user')]` |
| Parent | `//label[text()='Email']/parent::div` |
| Ancestor | `//b[text()='ZARA COAT 3']/ancestor::div[contains(@class,'card-body')]` |
| Following sibling | `//td[text()='Brian']/following-sibling::td/button` |

```java
By addToCartForProduct = By.xpath(
    "//b[text()='ZARA COAT 3']/ancestor::div[contains(@class,'card-body')]//button[contains(text(),'Add To Cart')]"
);
```

---

## Module 18 - Working with WebElements

```java
WebElement email = driver.findElement(By.id("userEmail"));
email.clear();
email.sendKeys("qa@example.com");

Select country = new Select(driver.findElement(By.id("country")));
country.selectByVisibleText("United States");
Assert.assertEquals(country.getFirstSelectedOption().getText(), "United States");

WebElement checkbox = driver.findElement(By.cssSelector("input[type='checkbox']"));
if (!checkbox.isSelected()) {
    checkbox.click();
}
Assert.assertTrue(checkbox.isSelected());
```

---

## Module 19 - Useful WebDriver Methods

```java
driver.get("https://example.com");
String title = driver.getTitle();
String url = driver.getCurrentUrl();
String source = driver.getPageSource();
driver.manage().window().maximize();
driver.manage().deleteAllCookies();
```

```java
driver.manage().addCookie(new Cookie("testMode", "true"));
Cookie cookie = driver.manage().getCookieNamed("testMode");
Assert.assertEquals(cookie.getValue(), "true");
```

---

## Module 20 - Wait Types

```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
WebElement loginButton = wait.until(ExpectedConditions.elementToBeClickable(By.id("login")));
loginButton.click();
```

```java
Wait<WebDriver> fluentWait = new FluentWait<>(driver)
        .withTimeout(Duration.ofSeconds(20))
        .pollingEvery(Duration.ofMillis(500))
        .ignoring(NoSuchElementException.class)
        .ignoring(StaleElementReferenceException.class);

WebElement result = fluentWait.until(d -> d.findElement(By.id("result")));
```

---

## Module 21 - Advanced Interactions

```java
JavascriptExecutor js = (JavascriptExecutor) driver;
WebElement table = driver.findElement(By.cssSelector(".tableFixHead"));
js.executeScript("arguments[0].scrollTop = arguments[0].scrollHeight", table);
```

```java
List<WebElement> amountCells = driver.findElements(By.cssSelector(".tableFixHead td:nth-child(4)"));
int calculatedTotal = amountCells.stream()
        .map(WebElement::getText)
        .mapToInt(Integer::parseInt)
        .sum();
String displayedText = driver.findElement(By.cssSelector(".totalAmount")).getText();
int displayedTotal = Integer.parseInt(displayedText.replaceAll("[^0-9]", ""));
Assert.assertEquals(calculatedTotal, displayedTotal);
```

---

## Module 22 - File Upload and Download

```java
Path uploadFile = Paths.get("src/test/resources/files/upload.xlsx").toAbsolutePath();
WebElement uploadInput = driver.findElement(By.cssSelector("input[type='file']"));
uploadInput.sendKeys(uploadFile.toString());
```

```java
Path downloadDir = Paths.get("downloads").toAbsolutePath();
Map<String, Object> prefs = new HashMap<>();
prefs.put("download.default_directory", downloadDir.toString());
prefs.put("download.prompt_for_download", false);
ChromeOptions options = new ChromeOptions();
options.setExperimentalOption("prefs", prefs);
```

---

## Module 23 - Windows and Iframes

```java
Alert alert = driver.switchTo().alert();
String alertText = alert.getText();
alert.accept();
```

```java
String parentWindow = driver.getWindowHandle();
driver.findElement(By.id("openwindow")).click();
for (String window : driver.getWindowHandles()) {
    if (!window.equals(parentWindow)) {
        driver.switchTo().window(window);
        break;
    }
}
driver.close();
driver.switchTo().window(parentWindow);
```

```java
driver.switchTo().frame("courses-iframe");
driver.findElement(By.linkText("Courses")).click();
driver.switchTo().defaultContent();
```

---

## Module 24 - Actions Class

```java
Actions actions = new Actions(driver);
WebElement menu = driver.findElement(By.id("mousehover"));
actions.moveToElement(menu).perform();
driver.findElement(By.linkText("Top")).click();
```

```java
WebElement source = driver.findElement(By.id("draggable"));
WebElement target = driver.findElement(By.id("droppable"));
new Actions(driver).dragAndDrop(source, target).perform();
```

---

## Module 25 - Logging Infrastructure

```java
private static final Logger logger = LogManager.getLogger(LoginTests.class);
logger.info("Starting login test");
logger.debug("Entering username");
logger.error("Dashboard was not displayed after login");
```

Logs should be archived in CI and should not include sensitive values.

---

## Module 26 - TestNG Infrastructure

```java
public class LoginTests extends BaseTest {
    @BeforeMethod(alwaysRun = true)
    public void openLoginPage() {
        driver.get(ConfigReader.get("baseUrl"));
    }

    @Test(groups = {"smoke", "login"}, priority = 1)
    public void validLoginTest() {
        Assert.assertTrue(true);
    }
}
```

```java
@DataProvider(name = "loginData")
public Object[][] loginData() {
    return new Object[][] {
            {"valid@example.com", "validCredential", true},
            {"invalid@example.com", "invalidCredential", false}
    };
}
```

---

## Module 27 - JUnit / Pytest Equivalents

```java
public class JUnitLoginTest {
    WebDriver driver;

    @BeforeEach
    void setup() {
        driver = new ChromeDriver();
    }

    @Test
    void titleTest() {
        driver.get("https://example.com");
        Assertions.assertEquals("Example Domain", driver.getTitle());
    }

    @AfterEach
    void teardown() {
        driver.quit();
    }
}
```

---

## Module 28 - Framework Part 1

```java
List<WebElement> products = driver.findElements(By.cssSelector(".mb-3"));
WebElement targetProduct = products.stream()
        .filter(product -> product.findElement(By.cssSelector("b")).getText().equals("ZARA COAT 3"))
        .findFirst()
        .orElseThrow(() -> new RuntimeException("Product not found"));

targetProduct.findElement(By.cssSelector("button:last-of-type")).click();
```

---

## Module 29 - Framework Part 2

```java
public class LandingPage extends AbstractComponent {
    WebDriver driver;

    @FindBy(id = "userEmail")
    WebElement userEmail;

    @FindBy(id = "userCredential")
    WebElement userCredential;

    @FindBy(id = "login")
    WebElement loginButton;

    public LandingPage(WebDriver driver) {
        super(driver);
        this.driver = driver;
        PageFactory.initElements(driver, this);
    }

    public ProductCataloguePage loginApplication(String email, String credential) {
        userEmail.sendKeys(email);
        userCredential.sendKeys(credential);
        loginButton.click();
        return new ProductCataloguePage(driver);
    }
}
```

---

## Module 30 - Framework Part 3

```java
public class BaseTest {
    public WebDriver driver;
    public LandingPage landingPage;

    @BeforeMethod(alwaysRun = true)
    public void launchApplication() throws IOException {
        driver = DriverFactory.createDriver(ConfigReader.get("browser"), Boolean.parseBoolean(ConfigReader.get("headless")));
        landingPage = new LandingPage(driver);
        landingPage.goTo();
    }

    @AfterMethod(alwaysRun = true)
    public void tearDown() {
        if (driver != null) driver.quit();
    }
}
```

---

## Module 31 - Framework Practice Exercise

```java
@Test(groups = {"regression", "order"})
public void submitOrderTest() {
    String productName = "ZARA COAT 3";
    ProductCataloguePage productCatalogue = landingPage.loginApplication("user@example.com", "validCredential");
    productCatalogue.addProductToCart(productName);
    CartPage cartPage = productCatalogue.goToCartPage();
    Assert.assertTrue(cartPage.verifyProductDisplay(productName));
    CheckoutPage checkoutPage = cartPage.goToCheckout();
    checkoutPage.selectCountry("India");
    ConfirmationPage confirmationPage = checkoutPage.submitOrder();
    Assert.assertEquals(confirmationPage.getConfirmationMessage(), "THANKYOU FOR THE ORDER.");
}
```

---

## Module 32 - Data-Driven Testing

```java
@DataProvider
public Object[][] getData() {
    HashMap<String, String> user1 = new HashMap<>();
    user1.put("email", "user1@example.com");
    user1.put("credential", "validCredential");
    user1.put("product", "ZARA COAT 3");
    return new Object[][] {{user1}};
}
```

---

## Module 33 - Running Complete Test Suite

```bash
mvn clean test
mvn clean test -Dbrowser=chrome
mvn clean test -Dbrowser=firefox -Dheadless=true
mvn clean test -DsuiteXmlFile=testng.xml
mvn clean test -Dgroups=smoke
```

---

## Module 34 - Git and GitHub

```bash
git init
git status
git add .
git commit -m "Add Selenium Java framework"
git remote add origin https://github.com/BrianGator/Selenium-Automation-Hero-Python-Showcase.git
git push -u origin main
```

```gitignore
target/
reports/
screenshots/
logs/
downloads/
.env
```

---

## Module 35 - Jenkins CI/CD

```groovy
pipeline {
    agent any
    tools {
        maven 'Maven-3.9'
        jdk 'JDK-17'
    }
    stages {
        stage('Checkout') {
            steps { git 'https://github.com/BrianGator/Selenium-Automation-Hero-Python-Showcase.git' }
        }
        stage('Run Tests') {
            steps { sh 'mvn clean test -Dbrowser=chrome -Dheadless=true' }
        }
    }
    post {
        always {
            junit 'target/surefire-reports/*.xml'
            archiveArtifacts artifacts: 'reports/**/*, screenshots/**/*, logs/**/*', allowEmptyArchive: true
        }
    }
}
```

---

## Module 36 - Conclusion

Recommended next steps: Selenium Grid, cloud browser providers, API setup and cleanup, JDBC validation, ExtentReports or Allure, Docker execution, GitHub Actions, and Cucumber BDD.

---

## API Tests for Selenium Java Frameworks

API testing supports UI automation by preparing data, validating backend behavior, and cleaning up records.

```java
@Test(groups = {"api"})
public void getUserProfileTest() {
    given()
        .baseUri("https://api.example.com")
    .when()
        .get("/users/123")
    .then()
        .statusCode(200)
        .body("id", equalTo(123))
        .body("email", containsString("@"));
}
```

```java
String orderId = given()
    .baseUri("https://api.example.com")
    .contentType("application/json")
    .body("{\"productId\":101,\"quantity\":1}")
.when()
    .post("/orders")
.then()
    .statusCode(201)
    .extract()
    .path("id");
```

---

## Login Tests for Selenium Java Frameworks

```java
public class LoginPage {
    private WebDriver driver;
    private By email = By.id("userEmail");
    private By credential = By.id("userCredential");
    private By loginButton = By.id("login");
    private By errorMessage = By.cssSelector(".toast-message");

    public LoginPage(WebDriver driver) {
        this.driver = driver;
    }

    public void login(String userEmail, String userCredential) {
        driver.findElement(email).clear();
        driver.findElement(email).sendKeys(userEmail);
        driver.findElement(credential).clear();
        driver.findElement(credential).sendKeys(userCredential);
        driver.findElement(loginButton).click();
    }
}
```

| Scenario | Expected Result |
|---|---|
| Valid login | User reaches product catalogue/dashboard. |
| Invalid login | Error message appears. |
| Empty fields | Required validation appears. |
| Locked user | Locked account message appears. |
| Logout | User returns to login screen. |
| Role-based login | Correct role-specific features appear. |

---

## Locator Reference Guide

| Priority | Locator | Example | Notes |
|---:|---|---|---|
| 1 | ID | `By.id("userEmail")` | Best when stable and unique. |
| 2 | Test attribute | `By.cssSelector("[data-testid='login']")` | Excellent for automation. |
| 3 | Name | `By.name("email")` | Good for forms. |
| 4 | CSS | `By.cssSelector("button[type='submit']")` | Fast and readable. |
| 5 | XPath | `By.xpath("//button[text()='Login']")` | Good for text and relationships. |
| 6 | Link text | `By.linkText("Forgot Link")` | Good for links. |

Avoid absolute XPath, generated class names, heavy indexes, and locators stored directly in test methods.

---

## Building a Selenium Java Framework from Scratch

```text
selenium-java-framework/
├── pom.xml
├── testng.xml
├── Jenkinsfile
├── README.md
├── .gitignore
├── src/test/java/base/BaseTest.java
├── src/test/java/factory/DriverFactory.java
├── src/test/java/components/AbstractComponent.java
├── src/test/java/pages/LandingPage.java
├── src/test/java/pages/ProductCataloguePage.java
├── src/test/java/pages/CartPage.java
├── src/test/java/pages/CheckoutPage.java
├── src/test/java/tests/SubmitOrderTest.java
├── src/test/java/tests/LoginTest.java
├── src/test/java/api/ApiClient.java
├── src/test/java/listeners/TestListener.java
├── src/test/java/retry/RetryAnalyzer.java
├── src/test/java/utils/ConfigReader.java
├── src/test/java/utils/ElementUtils.java
├── src/test/java/utils/ScreenshotUtils.java
├── src/test/resources/config.properties
├── reports/
├── screenshots/
├── logs/
└── downloads/
```

### Build Steps

1. Create Maven project.
2. Add Selenium, TestNG, WebDriverManager, Rest Assured, Log4j, and reporting dependencies.
3. Create config file.
4. Build ConfigReader.
5. Build DriverFactory.
6. Build BaseTest.
7. Build AbstractComponent.
8. Build Page Objects.
9. Build tests.
10. Add DataProvider support.
11. Add screenshots and listeners.
12. Add API setup/cleanup helper.
13. Add Jenkinsfile.
14. Add GitHub repository and CI job.

---

## Build from Scratch vs Pre-Built Frameworks

| Scenario | Recommendation |
|---|---|
| Learning Selenium | Simple Maven + Selenium + TestNG project. |
| Small smoke suite | Minimal BaseTest + Page Objects. |
| Large enterprise app | Build custom framework. |
| BDD requirement | Cucumber + Selenium Java. |
| Rich reports needed | Serenity BDD, ExtentReports, or Allure. |
| Concise syntax preferred | Selenide. |
| Cloud coverage needed | BrowserStack, Sauce Labs, or LambdaTest templates. |

Build from scratch when repeated complexity requires custom configuration, reporting, data handling, Page Objects, API setup, parallel execution, and CI/CD integration.

---

## Top 30 Selenium Java Technical Interview Questions

1. **What is Selenium WebDriver?** Browser automation API for controlling real browsers.
2. **What is WebDriver architecture?** Test code sends commands through WebDriver to browser drivers.
3. **What is Selenium Grid?** Remote/distributed browser execution.
4. **What locators does Selenium support?** ID, name, class, tag, link text, CSS, XPath.
5. **Best locator?** Stable ID or test-specific attribute.
6. **`findElement` vs `findElements`?** One element/exception vs list/empty list.
7. **Implicit wait?** Global element lookup polling.
8. **Explicit wait?** Condition-specific wait.
9. **FluentWait?** Custom polling and ignored exceptions.
10. **Why avoid `Thread.sleep()`?** Slow and flaky.
11. **How handle dropdowns?** Use `Select` for native select.
12. **How handle dynamic dropdowns?** Type, wait, loop, click match.
13. **How handle checkboxes?** Check `isSelected()` before click.
14. **How handle alerts?** `driver.switchTo().alert()`.
15. **How handle iframes?** `switchTo().frame()` and `defaultContent()`.
16. **How switch windows?** Use window handles.
17. **What is Actions class?** Advanced mouse/keyboard events.
18. **How take screenshots?** `TakesScreenshot`.
19. **What is JavaScriptExecutor?** Executes JS in browser.
20. **What is POM?** Page Object Model separates page logic from tests.
21. **What is PageFactory?** Initializes `@FindBy` elements.
22. **What is TestNG?** Java test framework.
23. **What is DataProvider?** Runs same test with multiple data rows.
24. **How run parallel tests?** TestNG parallel XML + ThreadLocal driver.
25. **Why ThreadLocal?** Isolates driver per thread.
26. **What is ExtentReports?** HTML reporting library.
27. **How run Maven tests?** `mvn clean test`.
28. **How integrate Jenkins?** Pull repo, run Maven, publish reports.
29. **How API supports Selenium?** Setup, validation, cleanup.
30. **What makes framework maintainable?** POM, waits, utilities, data, logging, screenshots, reports, CI/CD.

```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.elementToBeClickable(By.id("login"))).click();
```

```java
File src = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
```

---

## Summary

This README removes all expandable arrows and displays all Selenium Java automation module information directly on the page. It includes expanded module notes, Java code samples, expected results, API testing, login testing, locator guidance, framework-from-scratch details, framework comparison, and top technical interview questions.
