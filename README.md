# Selenium WebDriver 4 with Python - Zero To Hero

**Written by Brian McCarthy**

Comprehensive Selenium WebDriver 4 automation training with Python - from fundamental concepts to advanced automation frameworks. This course teaches you how to build robust, scalable test automation solutions for web applications.

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Languages & Technologies](#languages--technologies)
3. [Project Structure](#project-structure)
4. [Key Methodologies](#key-methodologies)
5. [Core Functions & Components](#core-functions--components)
6. [Code Methodologies Summary](#code-methodologies-summary)
7. [Getting Started Guide](#getting-started-guide)
8. [Tutorial & Examples](#tutorial--examples)
9. [Tips & Best Practices](#tips--best-practices)
10. [Section Index](#section-index)

---

## Overview

This comprehensive guide provides a complete learning path for Selenium WebDriver 4 automation testing with Python. You will progress from Python basics through advanced automation framework implementation, covering everything needed to master web application test automation.

### Key Learning Outcomes:
- Master Python fundamentals and object-oriented programming
- Understand Selenium WebDriver 4 core concepts and APIs
- Learn multiple element locator strategies (XPath, CSS Selectors)
- Implement waits, synchronization, and advanced interactions
- Build enterprise-grade automation frameworks
- Implement data-driven testing approaches
- Create robust logging and reporting infrastructure

---

## Languages & Technologies

**Primary Language:** Python (100%)

### Technology Stack:
- **Selenium WebDriver 4** - Web browser automation
- **Python 3.x** - Programming language
- **Pytest** - Advanced testing framework
- **Unittest** - Python's native testing framework
- **CSV/Excel** - Data-driven testing
- **Logging Module** - Test execution logging
- **Custom Frameworks** - Page Object Model, POM with BaseClass

---

## Project Structure

```
Selenium-Automation-Hero-Python/
│
├── Section 1 - Introduction/
│   └── Course overview and setup
│
├── Section 3 - Understanding Variables And Data Types/
│   └── Python variable types and declarations
│
├── Section 4 - Advanced Data Types/
│   └── Collections, dictionaries, tuples
│
├── Section 5 - Comparison And Boolean Operators/
│   └── Logic and comparison operations
│
├── Section 6 - Program Control Flow/
│   └── If/else, loops, conditionals
│
├── Section 7 - Functions_Methods - Working With Reusable Code/
│   └── Function definition and reusability
│
├── Section 10 - Modules/
│   ├── car.py
│   └── modules_demo2.py
│
├── Section 11 - Working With Files/
│   └── File I/O operations
│
├── Section 12 - How To Inspect Elements On Different Browsers/
│   └── Element inspection techniques
│
├── Section 13 - Selenium WebDriver - Setup And Installation/
│   └── WebDriver installation and configuration
│
├── Section 14 - Selenium WebDriver - Running Tests On Various Browsers/
│   └── Cross-browser testing setup
│
├── Section 15 - Selenium WebDriver - Finding Elements/
│   └── Element locator strategies
│
├── Section 16 - CSS Selectors - Advanced Locators/
│   └── CSS selector patterns and optimization
│
├── Section 17 - Xpath - Advanced Locators/
│   └── XPath syntax and advanced queries
│
├── Section 18 - Selenium WebDriver - Working With Web Elements/
│   └── Element interaction patterns
│
├── Section 19 - Selenium WebDriver - Useful Methods And Properties/
│   └── WebDriver methods and element properties
│
├── Section 20 - Selenium WebDriver - Wait Types/
│   └── Implicit, explicit, and fluent waits
│
├── Section 21 - Selenium WebDriver - Advanced Interactions/
│   └── Actions, keyboard/mouse events
│
├── Section 22 - Selenium WebDriver - File Upload And Download/
│   └── File handling in automation
│
├── Section 23 - Selenium WebDriver - Switch Window And IFrames/
│   └── Window and iframe context switching
│
├── Section 24 - Selenium WebDriver - Working With Actions Class/
│   └── Advanced action chains
│
├── Section 25 - Logging Infrastructure/
│   ├── logging_demo2.py
│   └── custom_logger.py
│
├── Section 26 - Unittest Infrastructure/
│   └── assert_demo.py
│
├── Section 27 - Pytest - Advanced Testing Framework/
│   └── Pytest fixtures and plugins
│
├── Section 28 - Automation Framework - Part 1/
│   └── Framework foundation and base classes
│
├── Section 29 - Automation Framework - Part 2/
│   ├── 5_conftest.py
│   └── 5_webdriverfactory.py
│
├── Section 30 - Automation Framework - Part 3/
│   └── 1_login_page.py
│
├── Section 31 - Automation Framework - Practice Exercise/
│   └── Hands-on framework implementation
│
├── Section 32 - Data Driven Testing/
│   ├── 4_read_data.py
│   └── 4_register_courses_csv_data.py
│
├── Section 33 - Running Complete Test Suite/
│   └── Suite execution and reporting
│
└── README.md
```

---

## Key Methodologies

### 1. **Page Object Model (POM)**
- Encapsulates page elements and interactions
- Maintains separation between test logic and UI elements
- Improves code maintainability and reusability

### 2. **Data-Driven Testing (DDT)**
- Separates test data from test logic
- Enables testing with multiple data sets
- Reduces code duplication

### 3. **Fixture-Based Testing**
- Uses Pytest fixtures for setup/teardown
- Conftest.py manages test configuration
- Enables parameterized and scoped testing

### 4. **Custom Logging Infrastructure**
- Tracks test execution with multiple log levels
- Generates per-method log files
- Improves test debugging and reporting

### 5. **Custom Logger Implementation**
- Dynamic logger initialization
- Automatic filename generation from calling method
- Configurable log formatting and levels

---

## Core Functions & Components

### **Custom Logger Module** (`custom_logger.py`)
```python
import inspect
import logging

def customLogger(logLevel):
    """
    Creates a custom logger with file handler
    
    Args:
        logLevel: Logging level (DEBUG, INFO, WARNING, ERROR, CRITICAL)
    
    Returns:
        Logger instance configured with file handler
    """
    loggerName = inspect.stack()[1][3]  # Get calling method name
    logger = logging.getLogger(loggerName)
    logger.setLevel(logging.DEBUG)
    
    fileHandler = logging.FileHandler("{0}.log".format(loggerName), mode='w')
    fileHandler.setLevel(logLevel)
    
    formatter = logging.Formatter(
        '%(asctime)s - %(name)s - %(levelname)s: %(message)s',
        datefmt='%m/%d/%Y %I:%M:%S %p'
    )
    fileHandler.setFormatter(formatter)
    logger.addHandler(fileHandler)
    
    return logger
```

**Usage Example:**
```python
import logging
import custom_logger as cl

class MyTestClass:
    log = cl.customLogger(logging.DEBUG)
    
    def test_something(self):
        self.log.debug('Starting test')
        self.log.info('Test execution ongoing')
        self.log.error('An error occurred')
```

---

### **CSV Data Reading** (`4_read_data.py`)
```python
import csv

def getCSVData(fileName):
    """
    Reads CSV file and returns data rows
    
    Args:
        fileName: Path to CSV file
    
    Returns:
        List of rows (each row is a list of values)
    """
    rows = []
    dataFile = open(fileName, "r")
    reader = csv.reader(dataFile)
    next(reader)  # Skip headers
    
    for row in reader:
        rows.append(row)
    
    return rows
```

**Usage Example:**
```python
from utilities.read_data import getCSVData

# Data structure: courseName, creditCardNum, expiry, cvv
test_data = getCSVData("testdata.csv")

for data_set in test_data:
    course_name, cc_num, cc_exp, cc_cvv = data_set
    # Use data in test
```

---

### **WebDriver Factory** (`5_webdriverfactory.py`)
```python
from selenium import webdriver

class WebDriverFactory:
    """
    Factory pattern implementation for WebDriver instantiation
    """
    
    def __init__(self, browser):
        self.browser = browser
    
    def getWebDriverInstance(self):
        """
        Creates and configures WebDriver instance
        
        Args:
            None
        
        Returns:
            Configured WebDriver instance
        """
        baseURL = "https://letskodeit.teachable.com/"
        
        if self.browser == "chrome":
            driver = webdriver.Chrome()
        elif self.browser == "firefox":
            driver = webdriver.Firefox()
        elif self.browser == "iexplorer":
            driver = webdriver.Ie()
        else:
            driver = webdriver.Firefox()
        
        # Configuration
        driver.implicitly_wait(3)
        driver.maximize_window()
        driver.get(baseURL)
        
        return driver
```

**Usage Example:**
```python
from base.webdriverfactory import WebDriverFactory

# Create driver
wdf = WebDriverFactory("chrome")
driver = wdf.getWebDriverInstance()

# Use driver
driver.find_element_by_id("element_id").click()

# Cleanup
driver.quit()
```

---

### **Page Object Pattern** (`1_login_page.py`)
```python
from base.selenium_driver import SeleniumDriver
import logging
import custom_logger as cl

class LoginPage(SeleniumDriver):
    """
    Page Object for Login page
    Encapsulates all login-related elements and interactions
    """
    
    log = cl.customLogger(logging.DEBUG)
    
    def __init__(self, driver):
        super().__init__(driver)
        self.driver = driver
    
    # Locators
    _login_link = "Login"
    _email_field = "user_email"
    _password_field = "user_password"
    _login_button = "commit"
    
    def clickLoginLink(self):
        self.elementClick(self._login_link, locatorType="link")
    
    def enterEmail(self, email):
        self.sendKeys(email, self._email_field)
    
    def enterPassword(self, password):
        self.sendKeys(password, self._password_field)
    
    def clickLoginButton(self):
        self.elementClick(self._login_button, locatorType="name")
    
    def login(self, email="", password=""):
        """
        Complete login workflow
        """
        self.clickLoginLink()
        self.enterEmail(email)
        self.enterPassword(password)
        self.clickLoginButton()
    
    def verifyLoginSuccessful(self):
        result = self.isElementPresent(
            "//*[@id='navbar']//span[text()='User Settings']",
            locatorType="xpath"
        )
        return result
    
    def verifyLoginFailed(self):
        result = self.isElementPresent(
            "//div[contains(text(),'Invalid email or password')]",
            locatorType="xpath"
        )
        return result
```

**Usage in Tests:**
```python
from pages.login_page import LoginPage

class TestLogin:
    def test_valid_login(self, driver):
        login_page = LoginPage(driver)
        login_page.login("user@example.com", "password123")
        
        if login_page.verifyLoginSuccessful():
            print("Login test passed!")
        else:
            print("Login test failed!")
```

---

### **Pytest Fixtures & Configuration** (`5_conftest.py`)
```python
import pytest
from selenium import webdriver
from base.webdriverfactory import WebDriverFactory

@pytest.yield_fixture()
def setUp():
    """Method-level setup/teardown"""
    print("Running method level setUp")
    yield
    print("Running method level tearDown")

@pytest.yield_fixture(scope="class")
def oneTimeSetUp(request, browser):
    """Class-level one-time setup"""
    print("Running one time setUp")
    wdf = WebDriverFactory(browser)
    driver = wdf.getWebDriverInstance()
    
    if request.cls is not None:
        request.cls.driver = driver
    
    yield driver
    driver.quit()
    print("Running one time tearDown")

def pytest_addoption(parser):
    """Add custom command-line options"""
    parser.addoption("--browser")
    parser.addoption("--osType", help="Type of operating system")

@pytest.fixture(scope="session")
def browser(request):
    return request.config.getoption("--browser")

@pytest.fixture(scope="session")
def osType(request):
    return request.config.getoption("--osType")
```

**Running Tests with Fixtures:**
```bash
# Run tests with Chrome browser
pytest --browser=chrome

# Run specific test file with Firefox
pytest tests/test_login.py --browser=firefox

# Run with multiple options
pytest --browser=chrome --osType=windows
```

---

### **Data-Driven Testing** (`4_register_courses_csv_data.py`)
```python
from ddt import ddt, data, unpack
import pytest
import unittest

@pytest.mark.usefixtures("oneTimeSetUp", "setUp")
@ddt
class RegisterCoursesCSVDataTests(unittest.TestCase):
    
    @pytest.fixture(autouse=True)
    def objectSetup(self, oneTimeSetUp):
        self.courses = RegisterCoursesPage(self.driver)
    
    @pytest.mark.run(order=1)
    @data(*getCSVData("testdata.csv"))
    @unpack
    def test_invalidEnrollment(self, courseName, ccNum, ccExp, ccCVV):
        """
        Parameterized test - runs once for each CSV row
        """
        self.courses.enterCourseName(courseName)
        self.courses.selectCourseToEnroll(courseName)
        self.courses.enrollCourse(num=ccNum, exp=ccExp, cvv=ccCVV)
        
        result = self.courses.verifyEnrollFailed()
        assert result, "Enrollment verification failed"
```

---

## Code Methodologies Summary

### **1. Object-Oriented Programming (OOP)**
- **Inheritance**: Page classes extend `SeleniumDriver` base class
- **Encapsulation**: Private locators (`_element_name`)
- **Polymorphism**: Overridden methods in child classes
- **Abstraction**: Complex driver operations hidden in base class

### **2. Separation of Concerns**
- **Tests**: Test logic and assertions
- **Pages**: Element locators and interactions
- **Utilities**: Helper functions and data reading
- **Base Classes**: Common driver operations

### **3. Factory Pattern**
- `WebDriverFactory` creates driver instances
- Abstracts driver creation from test code
- Simplifies browser switching

### **4. Fixture Pattern (Pytest)**
- Setup/teardown automation
- Scoped resource management
- Parameterized test execution
- Command-line parameter passing

### **5. Data-Driven Testing**
- External data files (CSV)
- DDT decorators for parameterization
- Reduces test code duplication
- Scalable test data management

---

## Getting Started Guide

### **Step 1: Install Python 3.x**
```bash
# Verify Python installation
python --version
```

### **Step 2: Install Required Packages**
```bash
# Install Selenium WebDriver 4
pip install selenium

# Install Pytest
pip install pytest

# Install Data-Driven Testing library
pip install ddt

# Install all dependencies
pip install -r requirements.txt
```

### **Step 3: Download WebDrivers**

Download drivers matching your browser version:
- **Chrome**: [ChromeDriver](https://chromedriver.chromium.org/)
- **Firefox**: [GeckoDriver](https://github.com/mozilla/geckodriver/releases)
- **IE**: [IEDriver](https://selenium-release.storage.googleapis.com/)

Add drivers to your PATH or specify path in code.

### **Step 4: Clone/Fork Repository**
```bash
git clone https://github.com/BrianGator/Selenium-Automation-Hero-Python.git
cd Selenium-Automation-Hero-Python
```

### **Step 5: Run Your First Test**
```bash
# Navigate to test directory
cd "Section 13 - Selenium WebDriver - Setup And Installation"

# Run a simple test
python test_file.py
```

---

## Tutorial & Examples

### **Example 1: Basic Element Interaction**
```python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

# Initialize driver
driver = webdriver.Chrome()
driver.get("https://example.com")

# Find element by ID
element = driver.find_element(By.ID, "button_id")
element.click()

# Find element by XPath
username_field = driver.find_element(By.XPATH, "//input[@name='username']")
username_field.send_keys("testuser")

# Find element by CSS Selector
submit_btn = driver.find_element(By.CSS_SELECTOR, "button.submit-btn")
submit_btn.click()

driver.quit()
```

### **Example 2: Explicit Wait with Expected Conditions**
```python
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://example.com")

# Wait for element to be clickable (max 10 seconds)
wait = WebDriverWait(driver, 10)
element = wait.until(
    EC.element_to_be_clickable((By.ID, "dynamic_button"))
)
element.click()

# Wait for element to be visible
element = wait.until(
    EC.visibility_of_element_located((By.XPATH, "//div[@class='modal']"))
)

# Wait for element to be present
element = wait.until(
    EC.presence_of_element_located((By.CSS_SELECTOR, ".alert-message"))
)

driver.quit()
```

### **Example 3: Advanced XPath Selectors**
```python
# XPath with text matching
element = driver.find_element(By.XPATH, "//button[text()='Submit']")

# XPath with partial text
element = driver.find_element(By.XPATH, "//button[contains(text(), 'Sub')]")

# XPath with attribute and text
element = driver.find_element(
    By.XPATH, 
    "//input[@type='text' and @name='email']"
)

# XPath with parent-child relationship
element = driver.find_element(By.XPATH, "//div[@class='form']//input[@type='submit']")

# XPath with following sibling
element = driver.find_element(By.XPATH, "//label[text()='Username']/following-sibling::input")
```

### **Example 4: CSS Selector Advanced Usage**
```python
# Direct element selection
element = driver.find_element(By.CSS_SELECTOR, "div.container")

# Child combinator
element = driver.find_element(By.CSS_SELECTOR, "div.form > input.email")

# Descendant combinator
element = driver.find_element(By.CSS_SELECTOR, "div.form input.email")

# Attribute selector
element = driver.find_element(By.CSS_SELECTOR, "input[type='submit']")

# Attribute contains
element = driver.find_element(By.CSS_SELECTOR, "button[class*='primary']")

# Pseudo-class
element = driver.find_element(By.CSS_SELECTOR, "button:first-child")
```

### **Example 5: ActionChains for Complex Interactions**
```python
from selenium.webdriver.common.action_chains import ActionChains

driver = webdriver.Chrome()
driver.get("https://example.com")

action_chains = ActionChains(driver)

# Hover over element
element = driver.find_element(By.ID, "menu_trigger")
action_chains.move_to_element(element).perform()

# Drag and drop
source = driver.find_element(By.ID, "draggable_item")
target = driver.find_element(By.ID, "drop_zone")
action_chains.drag_and_drop(source, target).perform()

# Right-click context menu
element = driver.find_element(By.ID, "context_element")
action_chains.context_click(element).perform()

# Double-click
element = driver.find_element(By.ID, "double_click_element")
action_chains.double_click(element).perform()

# Keyboard actions
action_chains.send_keys("Hello World").perform()
action_chains.key_down(Keys.CONTROL).send_keys('a').key_up(Keys.CONTROL).perform()

driver.quit()
```

### **Example 6: Switch Windows & IFrames**
```python
# Store original window handle
original_window = driver.current_window_handle

# Click link that opens new window
driver.find_element(By.XPATH, "//a[@target='_blank']").click()

# Switch to new window
for window in driver.window_handles:
    if window != original_window:
        driver.switch_to.window(window)
        break

# Perform actions in new window
element = driver.find_element(By.ID, "element_in_new_window")
element.click()

# Close new window and switch back
driver.close()
driver.switch_to.window(original_window)

# Handle IFrames
iframe = driver.find_element(By.TAG_NAME, "iframe")
driver.switch_to.frame(iframe)

# Find element inside iframe
element = driver.find_element(By.ID, "iframe_element")
element.click()

# Switch back to main content
driver.switch_to.default_content()
```

### **Example 7: File Upload & Download**
```python
from selenium.webdriver.common.keys import Keys
import os

driver = webdriver.Chrome()

# File upload
file_input = driver.find_element(By.ID, "file_upload")
file_input.send_keys("/path/to/file.txt")

# Click upload button
driver.find_element(By.ID, "upload_button").click()

# File download
driver.find_element(By.ID, "download_link").click()

# Verify download (check downloads folder)
downloads_path = os.path.expanduser("~/Downloads")
downloaded_files = os.listdir(downloads_path)
assert len(downloaded_files) > 0, "File not downloaded"

driver.quit()
```

### **Example 8: Pytest Test with Fixtures**
```python
import pytest
from selenium import webdriver

@pytest.fixture
def driver():
    """Fixture that provides WebDriver instance"""
    driver = webdriver.Chrome()
    yield driver  # Test executes here
    driver.quit()  # Cleanup

class TestExample:
    def test_page_title(self, driver):
        driver.get("https://example.com")
        assert "Example" in driver.title
    
    def test_element_presence(self, driver):
        driver.get("https://example.com")
        element = driver.find_element(By.ID, "main_content")
        assert element.is_displayed()
```

Run with: `pytest test_file.py`

---

## Tips & Best Practices

### **1. Locator Strategy**
```python
# ✅ DO: Use stable, unique locators
element = driver.find_element(By.ID, "unique_id")
element = driver.find_element(By.NAME, "form_field_name")

# ❌ DON'T: Use index-based or fragile locators
element = driver.find_element(By.XPATH, "//button[3]")  # Breaks with UI changes
element = driver.find_element(By.XPATH, "//div/div/div/button")  # Too nested
```

### **2. Wait Strategy**
```python
# ✅ DO: Use explicit waits
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

wait = WebDriverWait(driver, 10)
element = wait.until(EC.element_to_be_clickable((By.ID, "button")))

# ❌ DON'T: Use sleep
import time
time.sleep(5)  # Hard to maintain, unreliable
```

### **3. Error Handling**
```python
# ✅ DO: Handle specific exceptions
from selenium.common.exceptions import NoSuchElementException, TimeoutException

try:
    element = driver.find_element(By.ID, "element_id")
except NoSuchElementException:
    print("Element not found")
except TimeoutException:
    print("Element took too long to load")

# ❌ DON'T: Catch generic exceptions
try:
    element = driver.find_element(By.ID, "element_id")
except Exception as e:
    print(f"Error: {e}")  # Too broad
```

### **4. Page Object Model**
```python
# ✅ DO: Encapsulate page elements
class LoginPage:
    def __init__(self, driver):
        self.driver = driver
    
    def login(self, username, password):
        self.driver.find_element(By.ID, "username").send_keys(username)
        self.driver.find_element(By.ID, "password").send_keys(password)
        self.driver.find_element(By.ID, "login_btn").click()

# ❌ DON'T: Mix page elements with test logic
def test_login():
    driver.find_element(By.ID, "username").send_keys(username)
    driver.find_element(By.ID, "password").send_keys(password)
    driver.find_element(By.ID, "login_btn").click()
```

### **5. Logging & Reporting**
```python
# ✅ DO: Use structured logging
import logging
logger = logging.getLogger(__name__)

logger.info("Starting test execution")
logger.debug(f"Navigating to URL: {url}")
logger.warning("Element not found, retrying")
logger.error(f"Test failed: {error_message}")

# ❌ DON'T: Use print statements
print("Test started")  # Gets lost in large test runs
```

### **6. Test Independence**
```python
# ✅ DO: Create isolated tests
def test_login_success(driver):
    login_page.login("user@example.com", "password")
    assert login_page.is_logged_in()

def test_login_failure(driver):
    login_page.login("user@example.com", "wrong_password")
    assert login_page.shows_error_message()

# ❌ DON'T: Create dependent tests
def test_1_login(driver):
    login_page.login(...)

def test_2_dashboard(driver):
    # Depends on test_1 passing - fails if run independently
```

### **7. Element Visibility Check**
```python
# ✅ DO: Verify element visibility before interaction
element = driver.find_element(By.ID, "button")
if element.is_displayed() and element.is_enabled():
    element.click()

# ❌ DON'T: Assume element is visible
element = driver.find_element(By.ID, "button")
element.click()  # May fail if element is hidden
```

### **8. Dynamic Content Handling**
```python
# ✅ DO: Wait for dynamic content to load
wait = WebDriverWait(driver, 10)
table_rows = wait.until(
    EC.presence_of_all_elements_located((By.XPATH, "//table/tr"))
)

# ❌ DON'T: Access dynamic content immediately
rows = driver.find_elements(By.XPATH, "//table/tr")  # May be empty
```

### **9. Performance Optimization**
```python
# ✅ DO: Reuse driver instance
# Use fixtures to share driver across tests

# ✅ DO: Use data-driven testing
# Run same test with multiple data sets

# ❌ DON'T: Create new driver for each test
def test_1():
    driver = webdriver.Chrome()  # Slow
    ...
    driver.quit()
```

### **10. Cross-Browser Testing**
```python
# ✅ DO: Use parametrization for multiple browsers
@pytest.mark.parametrize("browser", ["chrome", "firefox", "edge"])
def test_on_multiple_browsers(browser):
    driver = webdriver.Chrome() if browser == "chrome" else None
    ...

# ✅ DO: Use factory for driver creation
wdf = WebDriverFactory(browser_name)
driver = wdf.getWebDriverInstance()
```

---

## Section Index

| Section | Topic | Purpose |
|---------|-------|---------|
| [1](#) | Introduction | Course overview |
| [3](#) | Variables & Data Types | Python fundamentals |
| [4](#) | Advanced Data Types | Collections, lists, tuples |
| [5](#) | Comparison & Boolean Operators | Logic operations |
| [6](#) | Program Control Flow | Conditionals & loops |
| [7](#) | Functions & Methods | Reusable code |
| [10](#) | Modules | Code organization |
| [11](#) | Working With Files | File I/O |
| [12](#) | Inspect Elements | Browser tools |
| [13](#) | WebDriver Setup | Installation & config |
| [14](#) | Running Tests on Browsers | Cross-browser setup |
| [15](#) | Finding Elements | Locator strategies |
| [16](#) | CSS Selectors | Advanced CSS locators |
| [17](#) | XPath | Advanced XPath |
| [18](#) | Working With Elements | Element interactions |
| [19](#) | Useful Methods & Properties | WebDriver API |
| [20](#) | Wait Types | Synchronization |
| [21](#) | Advanced Interactions | ActionChains |
| [22](#) | File Upload & Download | File handling |
| [23](#) | Switch Windows & IFrames | Context switching |
| [24](#) | Working With Actions | Advanced actions |
| [25](#) | Logging Infrastructure | Test logging |
| [26](#) | Unittest Infrastructure | Unittest framework |
| [27](#) | Pytest Framework | Pytest framework |
| [28](#) | Framework - Part 1 | Base structure |
| [29](#) | Framework - Part 2 | Factory & fixtures |
| [30](#) | Framework - Part 3 | Page objects |
| [31](#) | Framework - Practice | Hands-on exercises |
| [32](#) | Data Driven Testing | Parameterized tests |
| [33](#) | Running Complete Test Suite | Suite execution |

---

## Getting Help

- **Documentation**: [Selenium Docs](https://www.selenium.dev/documentation/)
- **Pytest**: [Pytest Docs](https://docs.pytest.org/)
- **Python**: [Python Official Docs](https://docs.python.org/3/)
- **Community**: Stack Overflow, GitHub Issues

---

**Last Updated:** 2026-05-30
**Author:** Brian McCarthy
**License:** Open Source

---

### Resources & Links

- [Selenium WebDriver Documentation](https://www.selenium.dev/documentation/)
- [Python Official Website](https://www.python.org/)
- [Pytest Documentation](https://docs.pytest.org/)
- [ChromeDriver Downloads](https://chromedriver.chromium.org/)
- [Firefox GeckoDriver](https://github.com/mozilla/geckodriver/releases)

---

Happy Testing! 🚀
