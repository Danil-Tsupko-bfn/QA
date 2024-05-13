import pytest
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

def test_login_button_and_footer_existence():
    chrome_options = webdriver.ChromeOptions()
    chrome_options.add_argument("--start-maximized")
    driver = webdriver.Chrome(options=chrome_options)
    
    driver.get("https://uaserials.pro/")
    
    try:
        login_button = WebDriverWait(driver, 10).until(
            EC.presence_of_element_located((By.CLASS_NAME, "js-login"))
        )
        
        assert login_button is not None
        
        footer = driver.find_element(By.CLASS_NAME, "footer")
        assert footer is not None
        
    finally:
        driver.quit()

test_login_button_and_footer_existence()
