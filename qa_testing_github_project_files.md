# QA Testing GitHub Project Files

## Folder Structure

**text**
qa-automation-project/
│
├── test\_google\_search.py
├── requirements.txt
├── README.md


**1. test\_google\_search.py**

python
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time

# Open Chrome browser
driver = webdriver.Chrome()

# Open Google
driver.get("https://www.google.com")

# Maximize browser window
driver.maximize\_window()

# Find search box
search\_box = driver.find\_element(By.NAME, "q")

# Type text into search box
search\_box.send\_keys("QA Testing")

# Press Enter
search\_box.send\_keys(Keys.RETURN)

# Wait for page to load
time.sleep(3)

# Print page title
print("Page Title:", driver.title)

# Verify test
if "QA Testing" in driver.title:
    print("Test Passed")
else:
    print("Test Failed")

# Close browser
driver.quit()


**2. requirements.txt**

text
selenium


**3. README.md**

markdown
# QA Automation Testing Project

This is a beginner QA Automation Testing project using Python and Selenium.

## Features
- Opens Google automatically
- Searches for "QA Testing"
- Validates page title
- Prints test result

## Technologies Used
- Python
- Selenium

## How to Run

### Install Selenium

bash
pip install selenium


### Run Project

bash
python test\_google\_search.py


## Expected Output

text
Page Title: QA Testing - Google Search
Test Passed



