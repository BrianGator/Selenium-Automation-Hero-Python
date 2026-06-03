# Selenium Automation Java Showcase

**Written by Brian McCarthy**

This repository is a comprehensive **Selenium WebDriver 4 automation framework guide using Java, TestNG, Maven, API testing, login testing, CI/CD, Page Object Model, data-driven testing, logging, reporting, and framework design from scratch**.

The course structure is adapted from the O'Reilly course outline for **Selenium WebDriver 4 with Python - Zero To Hero** and translated into a Java Selenium automation learning path. The original outline covers Selenium WebDriver setup, programming fundamentals, locators, WebElements, waits, advanced interactions, file upload/download, windows/iframes, logging, testing frameworks, automation framework design, data-driven testing, Git/GitHub, and Jenkins CI/CD. This README keeps that same module progression but provides **Java Selenium examples**.

---

## Course Content Table of Contents

| Module # | Module Name | Module Details |
|---:|---|---|
| 1 | [Introduction](#module-1---introduction) | Selenium purpose, WebDriver architecture, browser automation value, QA automation career context, and framework goals. |
| 2 | [Setup and Configuration](#module-2---setup-and-configuration) | Java JDK, IDE, Maven, browser drivers, Selenium dependencies, project setup, and first runnable test environment. |
| 3 | [Understanding Variables and Data Types](#module-3---understanding-variables-and-data-types) | Java variables, primitives, strings, booleans, object references, arithmetic, precedence, formatting, and test data values. |
| 4 | [Advanced Data Types](#module-4---advanced-data-types) | Arrays, lists, maps, sets, collections, test data containers, locator maps, and data structures used in test automation. |
| 5 | [Comparison and Boolean Operators](#module-5---comparison-and-boolean-operators) | Equality, relational operators, boolean logic, compound conditions, validation logic, and assertion decision-making. |
| 6 | [Program Control Flow](#module-6---program-control-flow) | `if`, `else`, `switch`, `for`, enhanced `for`, `while`, break/continue, and test branching patterns. |
| 7 | [Functions/Methods - Reusable Code](#module-7---functionsmethods---reusable-code) | Java methods, parameters, return values, reusable helper methods, generic actions, waits, and utility design. |
| 8 | [Classes and Object-Oriented Programming](#module-8---classes-and-object-oriented-programming) | Classes, objects, constructors, encapsulation, inheritance, interfaces, polymorphism, and Page Object Model foundations. |
| 9 | [Exception Handling](#module-9---exception-handling) | `try/catch/finally`, Selenium exceptions, stale elements, timeouts, no such element, custom errors, and screenshot-on-failure handling. |
| 10 | [Modules and Packages](#module-10---modules-and-packages) | Java packages, Maven modules, page/test/util package organization, imports, reusable libraries, and framework structure. |
| 11 | [Working with Files](#module-11---working-with-files) | Reading properties files, CSV data, JSON data, screenshots, downloads, file validation, and test evidence. |
| 12 | [Inspecting Elements on Different Browsers](#module-12---inspecting-elements-on-different-browsers) | Chrome DevTools, Edge/Firefox inspection, DOM basics, element attributes, accessibility, dynamic elements, and locator discovery. |
| 13 | [Selenium WebDriver Setup and Installation](#module-13---selenium-webdriver-setup-and-installation) | Selenium 4 dependency setup, WebDriverManager, Chrome/Firefox/Edge setup, driver lifecycle, and first Java WebDriver script. |
| 14 | [Running Tests on Various Browsers](#module-14---running-tests-on-various-browsers) | Chrome, Firefox, Edge, Safari concepts, cross-browser execution, driver factory, headless mode, and browser parameterization. |
| 15 | [Finding Elements](#module-15---finding-elements) | ID, name, class name, link text, partial link text, tag name, CSS, XPath, `findElement`, `findElements`, and dynamic IDs. |
| 16 | [CSS Selectors - Advanced Locators](#module-16---css-selectors---advanced-locators) | CSS IDs, classes, attributes, contains, starts/ends patterns, child nodes, hierarchy, nth-child, and locator quality. |
| 17 | [XPath - Advanced Locators](#module-17---xpath---advanced-locators) | Absolute vs relative XPath, text, contains, starts-with, axes, parent/sibling, dynamic XPath, and XPath best practices. |
| 18 | [Working with WebElements](#module-18---working-with-webelements) | Click, type, clear, get text, get attributes, enabled/disabled state, checkboxes, radio buttons, dropdowns, hidden elements, and element lists. |
| 19 | [Useful WebDriver Methods and Properties](#module-19---useful-webdriver-methods-and-properties) | URL, title, page source, window size, element presence, generic element methods, reusable find/wait methods, and dynamic XPath helpers. |
| 20 | [Selenium Wait Types](#module-20---selenium-wait-types) | Implicit waits, explicit waits, FluentWait, expected conditions, polling, timeouts, and synchronization strategy. |
| 21 | [Advanced Interactions](#module-21---advanced-interactions) | Calendars, autocomplete, dynamic dropdowns, screenshots, JavaScriptExecutor, scrolling, browser size, and complex UI flows. |
| 22 | [File Upload and Download](#module-22---file-upload-and-download) | Native file upload with `sendKeys`, download folder configuration, downloaded file validation, and system dialog limitations. |
| 23 | [Switch Windows and Iframes](#module-23---switch-windows-and-iframes) | Window handles, tab switching, iframe switching, JavaScript popups, alerts, confirms, prompts, and focus management. |
| 24 | [Actions Class](#module-24---actions-class) | Mouse hover, drag-and-drop, sliders, right-click, double-click, keyboard actions, composite actions, and user-like interaction. |
| 25 | [Logging Infrastructure](#module-25---logging-infrastructure) | Log4j2 setup, console logs, file logs, patterns, custom logger utility, debugging, and CI-friendly logging. |
| 26 | [TestNG Infrastructure](#module-26---testng-infrastructure) | TestNG annotations, assertions, suite XML, groups, parameters, DataProvider, listeners, reports, and parallel tests. |
| 27 | [JUnit / Pytest Equivalent Concepts for Java](#module-27---junit--pytest-equivalent-concepts-for-java) | Java alternatives to Python testing frameworks: JUnit 5, TestNG, assertions, lifecycle hooks, tags, parameterized tests, and runner selection. |
| 28 | [Automation Framework - Part 1](#module-28---automation-framework---part-1) | Framework folder structure, Maven setup, BaseTest, DriverFactory, configuration, Page Objects, and first framework test. |
| 29 | [Automation Framework - Part 2](#module-29---automation-framework---part-2) | Custom driver methods, reusable waits, navigation helpers, page utilities, screenshot utility, and robust element handling. |
| 30 | [Automation Framework - Part 3](#module-30---automation-framework---part-3) | Reporting, listeners, retry analyzer, environment config, browser config, parallel execution, and CI integration. |
| 31 | [Framework Practice Exercise](#module-31---framework-practice-exercise) | End-to-end registration/course/login flow, dynamic iframe handling, page classes, test class implementation, and refactoring. |
| 32 | [Data-Driven Testing](#module-32---data-driven-testing) | TestNG DataProvider, CSV, Excel, JSON, multiple datasets, parameterized browser/login tests, and test data utilities. |
| 33 | [Running the Complete Test Suite](#module-33---running-the-complete-test-suite) | Running smoke/regression suites, browser-specific suites, Maven commands, TestNG XML, suite navigation, and local execution flow. |
| 34 | [Git and GitHub Version Control](#module-34---git-and-github-version-control) | Git installation, staging, commits, branches, merge conflicts, GitHub remotes, clone, pull, push, and framework versioning. |
| 35 | [Continuous Integration with Jenkins](#module-35---continuous-integration-with-jenkins) | Jenkins setup, plugins, Git integration, Maven jobs, scheduled builds, secure credentials, reports, and remote build execution. |
| 36 | [Conclusion and Next Steps](#module-36---conclusion-and-next-steps) | Recommended next steps, portfolio improvements, interview preparation, CI/CD expansion, cloud grids, API integration, and framework maturity. |
| 37 | [API Tests for Selenium Java Frameworks](#api-tests-for-selenium-java-frameworks) | Rest Assured setup, GET/POST/PUT/DELETE, authentication, API setup/cleanup, schema-style checks, and backend validation. |
| 38 | [Login Tests for Selenium Java Frameworks](#login-tests-for-selenium-java-frameworks) | Valid login, invalid login, empty fields, locked users, logout, role validation, session validation, and secure credentials. |
| 39 | [Locator Reference Guide](#locator-reference-guide) | ID, name, CSS, XPath, link text, class name, tag name, accessibility notes, dynamic locator guidance, and anti-patterns. |
| 40 | [Building a Selenium Java Framework from Scratch](#building-a-selenium-java-framework-from-scratch) | Required files, folders, dependencies, step-by-step framework build, BaseTest, DriverFactory, Page Objects, utilities, and CI-ready structure. |
| 41 | [Build from Scratch vs Pre-Built Frameworks](#build-from-scratch-vs-pre-built-frameworks) | When custom frameworks are needed, when starter templates are better, popular framework choices, and scenario-based recommendations. |
| 42 | [Top 30 Selenium Java Technical Interview Questions](#top-30-selenium-java-technical-interview-questions) | Java Selenium interview Q&A with code examples covering WebDriver, waits, locators, POM, TestNG, Maven, API, Jenkins, and frameworks. |

---

## Module 1 - Introduction

Selenium WebDriver is a browser automation tool used to validate web applications through real browser interactions. It can open pages, find elements, click, type, select options, handle windows/iframes, execute JavaScript, capture screenshots, and validate user-facing behavior.

<details>
<summary>Click to expand Module 1 details, code, and expected result</summary>

### Topics Covered

- Why Selenium is used in QA automation.
- Selenium WebDriver architecture.
- Browser driver role.
- Difference between manual testing and automated browser testing.
- Where Selenium fits in regression, smoke, and CI/CD pipelines.

### Java Example

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class FirstSeleniumTest {
    public static void main(String[] args) {
        WebDriver driver = new ChromeDriver();
        driver.get("https://example.com");
        System.out.println(driver.getTitle());
        driver.quit();
    }
}
```

### Expected Result

- Chrome opens.
- Browser navigates to `https://example.com`.
- Page title prints to the console.
- Browser closes cleanly.

</details>

---

## Module 2 - Setup and Configuration

This module establishes the Java Selenium environment. A stable setup includes Java JDK, Maven, an IDE, browser drivers or Selenium Manager, TestNG or JUnit, and project dependencies.

<details>
<summary>Click to expand Module 2 details, code, and expected result</summary>

### Required Software

| Tool | Purpose |
|---|---|
| Java JDK 17+ | Runs Java code and test frameworks |
| IntelliJ IDEA / Eclipse | IDE for writing tests |
| Maven | Dependency and build management |
| Selenium WebDriver 4 | Browser automation API |
| TestNG | Test framework used for suites, groups, DataProvider, listeners, and reports |
| Chrome / Firefox / Edge | Browsers used for execution |
| Git | Version control |
| Jenkins | CI/CD execution |

### Maven `pom.xml`

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

### Expected Result

`mvn test` compiles the project, downloads dependencies, and runs TestNG tests.

</details>

---

## Module 3 - Understanding Variables and Data Types

Variables store test data, URLs, expected results, locator strings, credentials, and runtime values. Java is statically typed, so each variable must have a declared type.

<details>
<summary>Click to expand Module 3 details, code, and expected result</summary>

```java
String baseUrl = "https://example.com";
String expectedTitle = "Example Domain";
int timeoutSeconds = 10;
boolean headless = false;

driver.get(baseUrl);
String actualTitle = driver.getTitle();
Assert.assertEquals(actualTitle, expectedTitle);
```

### Expected Result

- `baseUrl` drives navigation.
- `actualTitle` stores runtime browser output.
- Test passes if the actual page title matches `Example Domain`.

### Automation Usage

- `String`: URLs, usernames, passwords, locator text.
- `int`: timeout values, counts, retry attempts.
- `boolean`: feature flags, pass/fail conditions, headless mode.
- `double`: price validation, totals, calculations.

</details>

---

## Module 4 - Advanced Data Types

Advanced data structures organize multiple values for test execution: login data, locator groups, product names, expected messages, and API payloads.

<details>
<summary>Click to expand Module 4 details, code, and expected result</summary>

```java
List<String> browsers = Arrays.asList("chrome", "firefox", "edge");
Map<String, String> user = new HashMap<>();
user.put("email", "qa@example.com");
user.put("password", "Password123");

for (String browser : browsers) {
    System.out.println("Run tests on: " + browser);
}
```

### Expected Output

```text
Run tests on: chrome
Run tests on: firefox
Run tests on: edge
```

### Framework Use Cases

- `List<WebElement>` for element collections.
- `Map<String, String>` for environment settings.
- `Object[][]` for TestNG DataProvider data.
- POJO classes for test users, products, orders, and API payloads.

</details>

---

## Module 5 - Comparison and Boolean Operators

Comparison and boolean operators are essential for assertions and branching test behavior.

<details>
<summary>Click to expand Module 5 details, code, and expected result</summary>

```java
boolean loginButtonDisplayed = driver.findElement(By.id("login")).isDisplayed();
boolean loginButtonEnabled = driver.findElement(By.id("login")).isEnabled();

Assert.assertTrue(loginButtonDisplayed && loginButtonEnabled,
        "Login button should be visible and enabled");
```

### Expected Result

The test passes only when the login button is both visible and enabled.

### Common Operators

| Operator | Meaning |
|---|---|
| `==` | Equal for primitive values |
| `.equals()` | Equal for object/string values |
| `!=` | Not equal |
| `>` `<` `>=` `<=` | Numeric comparison |
| `&&` | AND |
| `||` | OR |
| `!` | NOT |

</details>

---

## Module 6 - Program Control Flow

Control flow allows tests and utilities to make decisions and repeat operations.

<details>
<summary>Click to expand Module 6 details, code, and expected result</summary>

```java
List<WebElement> products = driver.findElements(By.cssSelector(".product-name"));
String targetProduct = "Laptop";

for (WebElement product : products) {
    if (product.getText().equalsIgnoreCase(targetProduct)) {
        product.click();
        break;
    }
}
```

### Expected Result

The test loops through product names and clicks the product matching `Laptop`.

### Automation Use Cases

- Loop through search results.
- Select dropdown options dynamically.
- Retry a condition.
- Branch based on browser, environment, or user role.
- Stop iteration when the target element is found.

</details>

---

## Module 7 - Functions/Methods - Reusable Code

Reusable methods reduce duplication and make tests easier to maintain.

<details>
<summary>Click to expand Module 7 details, code, and expected result</summary>

```java
public WebElement waitForVisible(By locator, int seconds) {
    WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(seconds));
    return wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
}

public void type(By locator, String value) {
    WebElement element = waitForVisible(locator, 10);
    element.clear();
    element.sendKeys(value);
}
```

### Expected Result

Test classes can call `type(By.id("email"), "qa@example.com")` instead of repeating wait, clear, and sendKeys logic.

</details>

---

## Module 8 - Classes and Object-Oriented Programming

OOP is the foundation of maintainable Selenium frameworks. Page Objects, BaseTest, DriverFactory, and utility classes all rely on classes and objects.

<details>
<summary>Click to expand Module 8 details, code, and expected result</summary>

```java
public class LoginPage {
    private WebDriver driver;
    private By email = By.id("email");
    private By password = By.id("password");
    private By loginButton = By.id("login");

    public LoginPage(WebDriver driver) {
        this.driver = driver;
    }

    public void login(String userEmail, String userPassword) {
        driver.findElement(email).sendKeys(userEmail);
        driver.findElement(password).sendKeys(userPassword);
        driver.findElement(loginButton).click();
    }
}
```

### Expected Result

The test can instantiate `LoginPage` and call `login()` instead of managing raw locators in the test class.

</details>

---

## Module 9 - Exception Handling

Selenium tests must handle timing, stale elements, missing elements, unexpected alerts, and invalid states.

<details>
<summary>Click to expand Module 9 details, code, and expected result</summary>

```java
try {
    driver.findElement(By.id("dashboard")).click();
} catch (NoSuchElementException e) {
    System.out.println("Dashboard element was not found: " + e.getMessage());
    throw e;
} catch (StaleElementReferenceException e) {
    System.out.println("Element became stale. Re-locating element.");
    driver.findElement(By.id("dashboard")).click();
}
```

### Expected Result

The framework logs useful failure context and can retry safe stale-element operations.

### Common Selenium Exceptions

- `NoSuchElementException`
- `TimeoutException`
- `StaleElementReferenceException`
- `ElementClickInterceptedException`
- `NoSuchFrameException`
- `NoSuchWindowException`

</details>

---

## Module 10 - Modules and Packages

Java packages organize code by responsibility.

<details>
<summary>Click to expand Module 10 details, code, and expected result</summary>

```text
src/test/java/
├── base/
│   └── BaseTest.java
├── pages/
│   ├── LoginPage.java
│   └── DashboardPage.java
├── tests/
│   └── LoginTests.java
├── utils/
│   ├── ConfigReader.java
│   ├── WaitUtils.java
│   └── ScreenshotUtils.java
└── api/
    └── UserApiClient.java
```

### Expected Result

The framework separates test setup, page objects, utilities, tests, and API helpers.

</details>

---

## Module 11 - Working with Files

Files are used for configuration, test data, screenshots, downloads, logs, and reports.

<details>
<summary>Click to expand Module 11 details, code, and expected result</summary>

```java
Properties properties = new Properties();
try (FileInputStream file = new FileInputStream("src/test/resources/config.properties")) {
    properties.load(file);
}
String baseUrl = properties.getProperty("baseUrl");
String browser = properties.getProperty("browser");
```

### Expected Result

The framework reads runtime configuration from a properties file instead of hardcoding values in tests.

### Example `config.properties`

```properties
baseUrl=https://example.com
browser=chrome
headless=false
```

</details>

---

## Module 12 - Inspecting Elements on Different Browsers

Inspection helps identify stable locators. Chrome, Edge, Firefox, and Safari provide DevTools for inspecting the DOM.

<details>
<summary>Click to expand Module 12 details, locator examples, and expected result</summary>

### What to Inspect

- `id`
- `name`
- `class`
- `type`
- `href`
- `aria-label`
- visible text
- parent/child relationship
- dynamic attributes
- iframe boundaries

### Locator Example

```java
By emailInput = By.id("email");
By submitButton = By.cssSelector("button[type='submit']");
By forgotPassword = By.linkText("Forgot Password?");
```

### Expected Result

The selected locators uniquely identify elements and remain stable across test runs.

</details>

---

## Module 13 - Selenium WebDriver Setup and Installation

Selenium 4 can manage drivers automatically through Selenium Manager, but many frameworks still use WebDriverManager for explicit driver management.

<details>
<summary>Click to expand Module 13 details, code, and expected result</summary>

```java
import io.github.bonigarcia.wdm.WebDriverManager;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class DriverSetup {
    public static WebDriver createChromeDriver() {
        WebDriverManager.chromedriver().setup();
        return new ChromeDriver();
    }
}
```

### Expected Result

ChromeDriver is resolved and launched without manually downloading driver executables.

</details>

---

## Module 14 - Running Tests on Various Browsers

Cross-browser testing validates that the application behaves correctly in different browsers.

<details>
<summary>Click to expand Module 14 details, code, and expected result</summary>

```java
public WebDriver createDriver(String browser) {
    switch (browser.toLowerCase()) {
        case "firefox":
            return new FirefoxDriver();
        case "edge":
            return new EdgeDriver();
        case "chrome":
        default:
            return new ChromeDriver();
    }
}
```

### TestNG Parameter Example

```xml
<parameter name="browser" value="chrome"/>
```

```java
@Parameters("browser")
@BeforeMethod
public void setup(String browser) {
    driver = createDriver(browser);
}
```

### Expected Result

The same test suite can run against Chrome, Firefox, or Edge based on suite configuration.

</details>

---

## Module 15 - Finding Elements

Finding elements is the core of Selenium WebDriver automation.

<details>
<summary>Click to expand Module 15 details, code, and expected result</summary>

```java
driver.findElement(By.id("email")).sendKeys("qa@example.com");
driver.findElement(By.name("password")).sendKeys("Password123");
driver.findElement(By.linkText("Login")).click();

List<WebElement> links = driver.findElements(By.tagName("a"));
System.out.println("Total links: " + links.size());
```

### Expected Result

- Email and password fields receive text.
- Login link or button is clicked.
- Link count is printed.

</details>

---

## Module 16 - CSS Selectors - Advanced Locators

CSS selectors are fast, readable, and useful for stable locator design.

<details>
<summary>Click to expand Module 16 details, code, and expected result</summary>

```java
By byId = By.cssSelector("#email");
By byClass = By.cssSelector(".btn-primary");
By byAttribute = By.cssSelector("input[name='password']");
By contains = By.cssSelector("input[id*='user']");
By startsWith = By.cssSelector("input[id^='user']");
By child = By.cssSelector("form#loginForm button[type='submit']");
```

### Expected Result

CSS selectors locate elements using IDs, classes, attributes, partial values, and hierarchy.

</details>

---

## Module 17 - XPath - Advanced Locators

XPath is powerful for dynamic relationships, text, parent/child traversal, and sibling navigation.

<details>
<summary>Click to expand Module 17 details, code, and expected result</summary>

```java
By relative = By.xpath("//input[@id='email']");
By text = By.xpath("//button[text()='Login']");
By contains = By.xpath("//button[contains(text(),'Log')]");
By startsWith = By.xpath("//input[starts-with(@id,'user')]");
By parent = By.xpath("//label[text()='Email']/parent::div//input");
By sibling = By.xpath("//td[text()='Brian']/following-sibling::td/button");
```

### Expected Result

XPath finds elements by exact text, partial text, dynamic attributes, parent nodes, and sibling nodes.

### Best Practice

Prefer short relative XPath over absolute XPath.

</details>

---

## Module 18 - Working with WebElements

WebElements represent elements located on a page. Selenium can click, type, clear, read text, check state, and interact with controls.

<details>
<summary>Click to expand Module 18 details, code, and expected result</summary>

```java
WebElement email = driver.findElement(By.id("email"));
email.clear();
email.sendKeys("qa@example.com");

WebElement rememberMe = driver.findElement(By.id("remember"));
if (!rememberMe.isSelected()) {
    rememberMe.click();
}

Select country = new Select(driver.findElement(By.id("country")));
country.selectByVisibleText("United States");
```

### Expected Result

The email field is populated, the checkbox is selected, and the dropdown selects `United States`.

</details>

---

## Module 19 - Useful WebDriver Methods and Properties

WebDriver and WebElement methods help validate page state and build utilities.

<details>
<summary>Click to expand Module 19 details, code, and expected result</summary>

```java
String currentUrl = driver.getCurrentUrl();
String title = driver.getTitle();
String text = driver.findElement(By.cssSelector("h1")).getText();
String href = driver.findElement(By.linkText("Docs")).getAttribute("href");

Assert.assertTrue(currentUrl.contains("example"));
Assert.assertNotNull(title);
Assert.assertFalse(text.isEmpty());
Assert.assertTrue(href.startsWith("https"));
```

### Expected Result

The test validates URL, title, heading text, and link attribute values.

</details>

---

## Module 20 - Selenium Wait Types

Waits solve synchronization problems caused by slow pages, Ajax calls, animations, and dynamic rendering.

<details>
<summary>Click to expand Module 20 details, code, and expected result</summary>

### Explicit Wait

```java
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
WebElement button = wait.until(ExpectedConditions.elementToBeClickable(By.id("submit")));
button.click();
```

### Fluent Wait

```java
Wait<WebDriver> fluentWait = new FluentWait<>(driver)
        .withTimeout(Duration.ofSeconds(20))
        .pollingEvery(Duration.ofMillis(500))
        .ignoring(NoSuchElementException.class);

WebElement result = fluentWait.until(d -> d.findElement(By.id("result")));
```

### Expected Result

The test waits until the element is ready instead of failing immediately or relying on hard sleeps.

</details>

---

## Module 21 - Advanced Interactions

Advanced interactions cover real-world widgets and browser features.

<details>
<summary>Click to expand Module 21 details, code, and expected result</summary>

### JavaScript Scroll

```java
JavascriptExecutor js = (JavascriptExecutor) driver;
WebElement element = driver.findElement(By.id("footer"));
js.executeScript("arguments[0].scrollIntoView(true);", element);
```

### Screenshot

```java
File source = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
Files.copy(source.toPath(), Paths.get("screenshots/home.png"), StandardCopyOption.REPLACE_EXISTING);
```

### Autocomplete

```java
driver.findElement(By.id("search")).sendKeys("Selenium");
WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(10));
wait.until(ExpectedConditions.visibilityOfElementLocated(By.cssSelector(".suggestion")));
driver.findElement(By.xpath("//li[contains(text(),'Selenium WebDriver')]")).click();
```

### Expected Result

The test scrolls to elements, captures screenshots, and selects dynamic autocomplete suggestions.

</details>

---

## Module 22 - File Upload and Download

File upload usually uses `sendKeys()` on an `<input type='file'>`. Downloads require browser preferences and file validation.

<details>
<summary>Click to expand Module 22 details, code, and expected result</summary>

### Upload

```java
WebElement upload = driver.findElement(By.cssSelector("input[type='file']"));
upload.sendKeys(Paths.get("src/test/resources/sample.pdf").toAbsolutePath().toString());
```

### Chrome Download Folder

```java
Map<String, Object> prefs = new HashMap<>();
prefs.put("download.default_directory", Paths.get("downloads").toAbsolutePath().toString());
ChromeOptions options = new ChromeOptions();
options.setExperimentalOption("prefs", prefs);
WebDriver driver = new ChromeDriver(options);
```

### Expected Result

The file is uploaded successfully or downloaded into the configured folder.

</details>

---

## Module 23 - Switch Windows and Iframes

Modern apps often use tabs, windows, iframes, and JavaScript alerts.

<details>
<summary>Click to expand Module 23 details, code, and expected result</summary>

### Window Switching

```java
String parent = driver.getWindowHandle();
driver.findElement(By.id("openWindow")).click();

for (String handle : driver.getWindowHandles()) {
    if (!handle.equals(parent)) {
        driver.switchTo().window(handle);
        break;
    }
}

Assert.assertTrue(driver.getTitle().contains("New Window"));
driver.close();
driver.switchTo().window(parent);
```

### Iframe Switching

```java
driver.switchTo().frame("payment-frame");
driver.findElement(By.id("cardNumber")).sendKeys("4111111111111111");
driver.switchTo().defaultContent();
```

### Alert Handling

```java
Alert alert = driver.switchTo().alert();
Assert.assertTrue(alert.getText().contains("Are you sure"));
alert.accept();
```

### Expected Result

The test manages browser focus across windows, frames, and alerts.

</details>

---

## Module 24 - Actions Class

The `Actions` class simulates advanced keyboard and mouse behavior.

<details>
<summary>Click to expand Module 24 details, code, and expected result</summary>

```java
Actions actions = new Actions(driver);

WebElement menu = driver.findElement(By.id("productsMenu"));
actions.moveToElement(menu).perform();

driver.findElement(By.linkText("Laptops")).click();
```

### Drag and Drop

```java
WebElement source = driver.findElement(By.id("source"));
WebElement target = driver.findElement(By.id("target"));
new Actions(driver).dragAndDrop(source, target).perform();
```

### Expected Result

Hover menus open, drag-and-drop executes, sliders move, and keyboard/mouse interactions behave like a user action.

</details>

---

## Module 25 - Logging Infrastructure

Logging provides traceability for debugging local and CI failures.

<details>
<summary>Click to expand Module 25 details, code, and expected result</summary>

### Log4j2 Dependency

```xml
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-core</artifactId>
    <version>2.23.1</version>
</dependency>
<dependency>
    <groupId>org.apache.logging.log4j</groupId>
    <artifactId>log4j-api</artifactId>
    <version>2.23.1</version>
</dependency>
```

### Logger Usage

```java
private static final Logger logger = LogManager.getLogger(LoginTests.class);

logger.info("Starting login test");
logger.debug("Entering username");
logger.error("Login failed");
```

### Expected Result

Logs are printed to console and/or file, helping identify where a test failed.

</details>

---

## Module 26 - TestNG Infrastructure

TestNG provides annotations, assertions, test suites, parameters, DataProvider, listeners, grouping, and parallel execution.

<details>
<summary>Click to expand Module 26 details, code, and expected result</summary>

```java
public class LoginTests extends BaseTest {
    @BeforeMethod
    public void openLoginPage() {
        driver.get(config.getBaseUrl() + "/login");
    }

    @Test(groups = {"smoke", "login"})
    public void validLoginTest() {
        Assert.assertTrue(true);
    }

    @AfterMethod
    public void cleanup() {
        driver.manage().deleteAllCookies();
    }
}
```

### Expected Result

TestNG runs setup before each test, executes grouped tests, and performs cleanup after each test.

</details>

---

## Module 27 - JUnit / Pytest Equivalent Concepts for Java

The referenced course uses Python testing frameworks. In Java Selenium, the equivalent frameworks are typically **TestNG** and **JUnit 5**.

<details>
<summary>Click to expand Module 27 details, code, and expected result</summary>

### JUnit 5 Example

```java
import org.junit.jupiter.api.*;

public class JUnitLoginTests {
    @BeforeEach
    void setup() {
        System.out.println("Setup driver");
    }

    @Test
    void validLoginTest() {
        Assertions.assertTrue(true);
    }

    @AfterEach
    void teardown() {
        System.out.println("Quit driver");
    }
}
```

### When to Use TestNG vs JUnit

| Framework | Best Use |
|---|---|
| TestNG | Enterprise Selenium suites, XML suites, groups, DataProvider, parallel runs |
| JUnit 5 | Modern Java unit/integration tests, Spring projects, clean annotation model |

</details>

---

## Module 28 - Automation Framework - Part 1

Framework Part 1 establishes the framework foundation.

<details>
<summary>Click to expand Module 28 details, files, code, and expected result</summary>

### Starter Structure

```text
selenium-java-framework/
├── pom.xml
├── testng.xml
├── src/test/java/base/BaseTest.java
├── src/test/java/factory/DriverFactory.java
├── src/test/java/pages/LoginPage.java
├── src/test/java/tests/LoginTests.java
├── src/test/java/utils/ConfigReader.java
└── src/test/resources/config.properties
```

### BaseTest

```java
public class BaseTest {
    protected WebDriver driver;

    @BeforeMethod
    public void setUp() {
        driver = DriverFactory.createDriver(ConfigReader.get("browser"));
        driver.manage().window().maximize();
        driver.get(ConfigReader.get("baseUrl"));
    }

    @AfterMethod
    public void tearDown() {
        if (driver != null) driver.quit();
    }
}
```

### Expected Result

Every test starts with a configured browser and closes the browser after execution.

</details>

---

## Module 29 - Automation Framework - Part 2

Framework Part 2 adds custom wrappers and utility methods.

<details>
<summary>Click to expand Module 29 details, code, and expected result</summary>

```java
public class ElementUtils {
    private WebDriver driver;
    private WebDriverWait wait;

    public ElementUtils(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(10));
    }

    public void click(By locator) {
        wait.until(ExpectedConditions.elementToBeClickable(locator)).click();
    }

    public void type(By locator, String value) {
        WebElement element = wait.until(ExpectedConditions.visibilityOfElementLocated(locator));
        element.clear();
        element.sendKeys(value);
    }
}
```

### Expected Result

Page Objects can use `ElementUtils` for consistent waits and interactions.

</details>

---

## Module 30 - Automation Framework - Part 3

Framework Part 3 adds listeners, reporting, retries, and CI readiness.

<details>
<summary>Click to expand Module 30 details, code, and expected result</summary>

### Screenshot Listener

```java
public class TestListener implements ITestListener {
    @Override
    public void onTestFailure(ITestResult result) {
        Object instance = result.getInstance();
        WebDriver driver = ((BaseTest) instance).driver;
        File screenshot = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
        System.out.println("Captured screenshot for: " + result.getName());
    }
}
```

### Retry Analyzer

```java
public class RetryAnalyzer implements IRetryAnalyzer {
    private int count = 0;
    private static final int maxRetry = 1;

    public boolean retry(ITestResult result) {
        if (count < maxRetry) {
            count++;
            return true;
        }
        return false;
    }
}
```

### Expected Result

Failures capture evidence and unstable tests can be retried in a controlled way.

</details>

---

## Module 31 - Framework Practice Exercise

This module combines page classes, test classes, waits, locators, data, navigation, and iframe handling into a working scenario.

<details>
<summary>Click to expand Module 31 details, code, and expected result</summary>

```java
@Test
public void registerForCourseTest() {
    LoginPage loginPage = new LoginPage(driver);
    DashboardPage dashboard = loginPage.login("student@example.com", "Password123");
    CoursesPage courses = dashboard.openCourses();
    courses.searchCourse("Selenium WebDriver");
    courses.selectCourse("Selenium WebDriver 4 Java");
    Assert.assertTrue(courses.isRegistrationConfirmationDisplayed());
}
```

### Expected Result

The test logs in, navigates to courses, searches for a Selenium course, registers, and validates confirmation.

</details>

---

## Module 32 - Data-Driven Testing

Data-driven testing runs the same test with multiple data sets.

<details>
<summary>Click to expand Module 32 details, code, and expected result</summary>

```java
@DataProvider(name = "loginData")
public Object[][] loginData() {
    return new Object[][] {
            {"valid@example.com", "Password123", true},
            {"locked@example.com", "Password123", false},
            {"bad@example.com", "wrong", false}
    };
}

@Test(dataProvider = "loginData")
public void loginDataDrivenTest(String email, String password, boolean expectedSuccess) {
    LoginPage loginPage = new LoginPage(driver);
    boolean actualSuccess = loginPage.loginAndReturnStatus(email, password);
    Assert.assertEquals(actualSuccess, expectedSuccess);
}
```

### Expected Result

TestNG runs the login test once for each row of data.

</details>

---

## Module 33 - Running the Complete Test Suite

Complete suite execution should support smoke, regression, browser-specific, and environment-specific runs.

<details>
<summary>Click to expand Module 33 details, commands, and expected result</summary>

```bash
mvn clean test
mvn clean test -Dbrowser=chrome
mvn clean test -DsuiteXmlFile=testng-smoke.xml
mvn clean test -Denv=qa -Dbrowser=firefox
```

### TestNG Suite

```xml
<suite name="Regression Suite" parallel="tests" thread-count="2">
    <test name="Chrome Tests">
        <parameter name="browser" value="chrome"/>
        <classes>
            <class name="tests.LoginTests"/>
        </classes>
    </test>
</suite>
```

### Expected Result

Maven runs the selected suite and generates Surefire/TestNG reports.

</details>

---

## Module 34 - Git and GitHub Version Control

Git protects framework history and supports collaboration.

<details>
<summary>Click to expand Module 34 details, commands, and expected result</summary>

```bash
git init
git status
git add .
git commit -m "Add Selenium Java framework"
git branch -M main
git remote add origin https://github.com/BrianGator/Selenium-Automation-Hero-Python-Showcase.git
git push -u origin main
```

### Branch Workflow

```bash
git checkout -b feature/login-tests
git add .
git commit -m "Add login tests"
git checkout main
git merge feature/login-tests
```

### Expected Result

Framework changes are version-controlled and can be integrated with Jenkins/GitHub Actions.

</details>

---

## Module 35 - Continuous Integration with Jenkins

Jenkins runs automated Selenium suites after code changes, on schedules, or before releases.

<details>
<summary>Click to expand Module 35 details, pipeline code, and expected result</summary>

```groovy
pipeline {
    agent any

    tools {
        maven 'Maven-3.9'
        jdk 'JDK-17'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/BrianGator/Selenium-Automation-Hero-Python-Showcase.git'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'mvn clean test -Dbrowser=chrome'
            }
        }
    }

    post {
        always {
            junit 'target/surefire-reports/*.xml'
            archiveArtifacts artifacts: 'screenshots/**/*, logs/**/*, target/surefire-reports/**/*', allowEmptyArchive: true
        }
    }
}
```

### Expected Result

Jenkins checks out the repo, runs tests with Maven, publishes JUnit results, and archives screenshots/logs/reports.

</details>

---

## Module 36 - Conclusion and Next Steps

After completing the modules, the framework should be expanded with cloud execution, API setup/cleanup, database validation, visual testing, and CI/CD maturity.

<details>
<summary>Click to expand Module 36 recommendations</summary>

### Recommended Next Steps

- Add Selenium Grid or cloud execution.
- Add Rest Assured API tests.
- Add role-based login coverage.
- Add Allure or ExtentReports.
- Add GitHub Actions in addition to Jenkins.
- Add Docker execution.
- Add contract/API tests for backend workflows.
- Add performance smoke checks for key pages.

</details>

---

## API Tests for Selenium Java Frameworks

API testing complements Selenium UI testing by validating backend behavior and preparing/cleaning test data.

### Rest Assured Dependency

```xml
<dependency>
    <groupId>io.rest-assured</groupId>
    <artifactId>rest-assured</artifactId>
    <version>5.4.0</version>
    <scope>test</scope>
</dependency>
```

### GET API Test

```java
import org.testng.annotations.Test;
import static io.restassured.RestAssured.*;
import static org.hamcrest.Matchers.*;

public class UserApiTests {
    @Test
    public void getUserProfileTest() {
        given()
            .baseUri("https://api.example.com")
            .header("Authorization", "Bearer token")
        .when()
            .get("/users/123")
        .then()
            .statusCode(200)
            .body("id", equalTo(123))
            .body("email", containsString("@"));
    }
}
```

### POST API Setup for Selenium UI Test

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

### Expected Result

- API tests validate backend behavior quickly.
- UI tests can start with prepared data instead of manual setup.
- Cleanup APIs remove records created during automated tests.

---

## Login Tests for Selenium Java Frameworks

Login testing validates authentication, access control, error handling, and session behavior.

### Login Page Object

```java
public class LoginPage {
    private WebDriver driver;
    private By email = By.id("email");
    private By password = By.id("password");
    private By loginButton = By.cssSelector("button[type='submit']");
    private By errorMessage = By.cssSelector(".alert-danger");

    public LoginPage(WebDriver driver) {
        this.driver = driver;
    }

    public void login(String userEmail, String userPassword) {
        driver.findElement(email).clear();
        driver.findElement(email).sendKeys(userEmail);
        driver.findElement(password).clear();
        driver.findElement(password).sendKeys(userPassword);
        driver.findElement(loginButton).click();
    }

    public String getErrorMessage() {
        return driver.findElement(errorMessage).getText();
    }
}
```

### Valid Login Test

```java
@Test(groups = {"smoke", "login"})
public void validLoginTest() {
    LoginPage loginPage = new LoginPage(driver);
    loginPage.login(System.getenv("TEST_USER_EMAIL"), System.getenv("TEST_USER_PASSWORD"));
    Assert.assertTrue(driver.getCurrentUrl().contains("dashboard"));
}
```

### Invalid Login Test

```java
@Test(groups = {"login"})
public void invalidLoginTest() {
    LoginPage loginPage = new LoginPage(driver);
    loginPage.login("bad@example.com", "wrong-password");
    Assert.assertTrue(loginPage.getErrorMessage().contains("Invalid"));
}
```

### Login Coverage Checklist

| Scenario | Expected Result |
|---|---|
| Valid credentials | Dashboard loads |
| Invalid password | Error message appears |
| Empty username/password | Required field validation appears |
| Locked user | Locked user message appears |
| Logout | User returns to login page |
| Expired session | User is redirected to login |
| Role-based login | User sees correct menu/features |

---

## Locator Reference Guide

| Locator | Example | Best Use |
|---|---|---|
| ID | `By.id("email")` | Best locator when stable and unique |
| Name | `By.name("password")` | Good for forms |
| CSS | `By.cssSelector("button[type='submit']")` | Fast and readable for attributes/classes |
| XPath | `By.xpath("//button[text()='Login']")` | Useful for text and DOM relationships |
| Link text | `By.linkText("Login")` | Exact anchor text |
| Partial link text | `By.partialLinkText("Log")` | Partial anchor text |
| Class name | `By.className("btn-primary")` | Use carefully; often not unique |
| Tag name | `By.tagName("a")` | Useful for lists/counts |

### Locator Best Practices

- Prefer stable IDs and test-specific attributes.
- Prefer CSS for readable attribute and hierarchy selectors.
- Use XPath for text, parent/sibling, and complex DOM traversal.
- Avoid absolute XPath.
- Avoid brittle generated classes.
- Avoid indexes unless the UI is intentionally ordered and stable.
- Always verify a locator is unique before using it in framework code.

---

## Building a Selenium Java Framework from Scratch

A custom Selenium framework is useful when tests need reusable setup, consistent waits, Page Objects, reports, logging, data management, CI/CD, and cross-browser execution.

### Required Files and Folders

```text
selenium-java-framework/
├── pom.xml
├── testng.xml
├── README.md
├── .gitignore
├── Jenkinsfile
├── src/test/java/base/BaseTest.java
├── src/test/java/factory/DriverFactory.java
├── src/test/java/pages/LoginPage.java
├── src/test/java/pages/DashboardPage.java
├── src/test/java/tests/LoginTests.java
├── src/test/java/tests/ApiTests.java
├── src/test/java/utils/ConfigReader.java
├── src/test/java/utils/ElementUtils.java
├── src/test/java/utils/ScreenshotUtils.java
├── src/test/java/listeners/TestListener.java
├── src/test/resources/config.properties
├── src/test/resources/testdata/login-data.csv
├── screenshots/
├── logs/
└── reports/
```

### Step-by-Step Build

1. Create Maven project.
2. Add Selenium, TestNG, WebDriverManager, Rest Assured, and Log4j dependencies.
3. Create `config.properties`.
4. Build `ConfigReader`.
5. Build `DriverFactory`.
6. Build `BaseTest`.
7. Build Page Object classes.
8. Build utility classes for waits, screenshots, JavaScript, and data.
9. Add TestNG tests.
10. Add DataProvider tests.
11. Add listeners and reporting.
12. Add API setup/cleanup tests.
13. Add Jenkinsfile.
14. Add GitHub repository and CI trigger.

### DriverFactory Example

```java
public class DriverFactory {
    public static WebDriver createDriver(String browser) {
        switch (browser.toLowerCase()) {
            case "firefox": return new FirefoxDriver();
            case "edge": return new EdgeDriver();
            case "chrome":
            default: return new ChromeDriver();
        }
    }
}
```

### Best Practices

- Keep tests readable and business-focused.
- Keep locators inside Page Objects.
- Keep reusable waits inside utility classes.
- Keep credentials out of source code.
- Run smoke tests on every pull request.
- Use API calls for setup and cleanup when possible.
- Capture screenshots and logs on failure.
- Avoid over-engineering before repeated needs are clear.

---

## Build from Scratch vs Pre-Built Frameworks

### Build from Scratch When

| Scenario | Why Custom Framework Helps |
|---|---|
| Enterprise application | Needs custom reporting, environments, users, roles, and workflows |
| Large regression suite | Needs reusable Page Objects, parallel execution, tagging, and CI/CD |
| Complex login/security | Needs role-based login, session handling, and secure credentials |
| UI + API hybrid testing | Needs backend setup/cleanup and UI validation together |
| Team collaboration | Needs shared standards, folder structure, naming, and framework rules |

### Use Pre-Built or Simple Framework When

| Scenario | Better Choice |
|---|---|
| Learning Selenium | Simple Java + Selenium + TestNG project |
| Small smoke suite | Minimal Page Objects and Maven are enough |
| Existing company standard | Use the team’s established framework |
| Fast prototype | Use Selenium IDE export, simple TestNG, or a starter template |
| BDD requirements | Use Cucumber + Selenium + Java |

### Popular Selenium Java Framework Options

| Framework / Stack | Best Scenario |
|---|---|
| Selenium + TestNG + Maven | Most common Java QA automation framework style |
| Selenium + JUnit 5 + Maven/Gradle | Java engineering teams and Spring projects |
| Selenium + Cucumber + Java | BDD acceptance testing with Gherkin scenarios |
| Selenium Grid | Distributed local browser execution |
| Selenide | Concise Selenium wrapper with built-in waits |
| Serenity BDD | Rich reporting and BDD-friendly framework |
| WebDriverIO / Playwright | Consider for modern JS/TS teams or newer web-first tooling |
| Cloud grids: BrowserStack/Sauce Labs/LambdaTest | Cross-browser/cross-platform execution without maintaining infrastructure |

### Decision Rule

Build a custom framework only when repeated project complexity justifies it. For small projects, use the simplest structure that supports the tests.

---

## Top 30 Selenium Java Technical Interview Questions

### 1. What is Selenium WebDriver?

Selenium WebDriver is an API for automating browsers through real browser drivers such as ChromeDriver, GeckoDriver, and EdgeDriver.

```java
WebDriver driver = new ChromeDriver();
driver.get("https://example.com");
driver.quit();
```

### 2. What is the difference between Selenium WebDriver and Selenium IDE?

WebDriver is code-based browser automation. Selenium IDE is record-and-playback automation, better for quick prototypes than scalable frameworks.

### 3. What is the WebDriver architecture?

Test code sends commands through WebDriver APIs to a browser driver, which controls the browser and returns results.

### 4. What locator strategies does Selenium support?

ID, name, class name, tag name, link text, partial link text, CSS selector, and XPath.

### 5. Which locator is best?

Stable unique ID or test-specific attribute is usually best. CSS is generally preferred for readable attribute locators. XPath is useful for text and DOM relationships.

### 6. What is the difference between `findElement` and `findElements`?

`findElement` returns one element or throws `NoSuchElementException`. `findElements` returns a list and returns an empty list if none are found.

```java
WebElement button = driver.findElement(By.id("submit"));
List<WebElement> links = driver.findElements(By.tagName("a"));
```

### 7. What is an implicit wait?

An implicit wait tells WebDriver to poll for elements for a configured time before throwing `NoSuchElementException`.

```java
driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
```

### 8. What is an explicit wait?

Explicit wait waits for a specific condition.

```java
new WebDriverWait(driver, Duration.ofSeconds(10))
    .until(ExpectedConditions.elementToBeClickable(By.id("login")));
```

### 9. What is FluentWait?

FluentWait customizes timeout, polling interval, and ignored exceptions.

### 10. Why avoid `Thread.sleep()`?

It creates fixed delays and causes slow/flaky tests. Use explicit waits instead.

### 11. What is Page Object Model?

POM stores locators and actions in page classes so tests are readable and maintainable.

### 12. What is PageFactory?

PageFactory initializes WebElements annotated with `@FindBy`. It is useful but many modern frameworks prefer explicit `By` locators for control.

### 13. How do you handle dropdowns?

Use Selenium `Select` for native `<select>` elements.

```java
Select select = new Select(driver.findElement(By.id("country")));
select.selectByVisibleText("United States");
```

### 14. How do you handle alerts?

```java
Alert alert = driver.switchTo().alert();
alert.accept();
```

### 15. How do you switch windows?

Use `getWindowHandles()` and `switchTo().window(handle)`.

### 16. How do you switch iframes?

```java
driver.switchTo().frame("frameName");
driver.switchTo().defaultContent();
```

### 17. How do you take screenshots?

```java
File src = ((TakesScreenshot) driver).getScreenshotAs(OutputType.FILE);
```

### 18. How do you execute JavaScript?

```java
((JavascriptExecutor) driver).executeScript("window.scrollTo(0, document.body.scrollHeight)");
```

### 19. What is the Actions class used for?

Mouse hover, drag-and-drop, double-click, right-click, keyboard shortcuts, and sliders.

### 20. How do you upload files?

Use `sendKeys()` with an absolute file path on an `<input type='file'>`.

### 21. How do you validate downloaded files?

Configure the download folder, trigger download, wait for the file, and assert the file exists.

### 22. What is TestNG?

TestNG is a Java testing framework that supports annotations, assertions, XML suites, groups, parameters, DataProvider, listeners, and parallel execution.

### 23. What is DataProvider?

DataProvider runs the same test with multiple sets of data.

### 24. How do you run tests in parallel?

Use TestNG XML with `parallel` and `thread-count`, and ensure each thread has its own WebDriver instance.

### 25. Why use ThreadLocal WebDriver?

ThreadLocal isolates WebDriver per thread during parallel execution.

```java
private static ThreadLocal<WebDriver> driver = new ThreadLocal<>();
```

### 26. What is Maven used for?

Maven manages dependencies, builds code, and runs tests through plugins such as Surefire.

### 27. How do you integrate Selenium with Jenkins?

Configure Jenkins to check out code and run `mvn clean test`, then publish reports and artifacts.

### 28. How can API testing support Selenium tests?

API calls can create test data, validate backend state, authenticate users, and clean up records.

### 29. What login scenarios should be automated?

Valid login, invalid login, empty fields, locked user, logout, session timeout, and role-based access.

### 30. What makes a Selenium framework maintainable?

Clear folder structure, Page Objects, reusable utilities, explicit waits, config management, logging, reporting, CI/CD, clean data handling, and readable test names.

---

## Summary

This README provides a complete Java Selenium WebDriver automation learning path and framework guide based on a 36-module Selenium WebDriver course outline. It includes Java examples, expected results, locator guidance, API testing, login testing, framework design, pre-built framework comparisons, CI/CD, and top technical interview questions.
