import sentry_sdk
sentry_sdk.init(
    "https://f9af15b45909479d87be73c7035ca40b@o1179766.ingest.sentry.io/6292058",

    # Set traces_sample_rate to 1.0 to capture 100%
    # of transactions for performance monitoring.
    # We recommend adjusting this value in production.
    traces_sample_rate=1.0
)
from selenium import webdriver 
from selenium.webdriver.support.ui import WebDriverWait 
from selenium.webdriver.common.keys import Keys 
from selenium.webdriver.common.by import By 
from selenium.webdriver.support import expected_conditions as EC 
import time 
driver = webdriver.Chrome('/Users/Yassin/chrome.d/chromedriver.exe') 
  
driver.get("https://web.whatsapp.com/") 
wait = WebDriverWait(driver, 600) 
  
target = '"Name of chat"'
string = "Message"
  
x_arg = '//span[contains(@title,' + target + ')]'
group_title = wait.until(EC.presence_of_element_located(( 
    By.XPATH, x_arg))) 
group_title.click() 
inp_xpath = '//div[@class="input"][@dir="auto"][@data-tab="1"]'
input_box = wait.until(EC.presence_of_element_located(( 
    By.XPATH, inp_xpath))) 
for i in range(100): 
    input_box.send_keys(string + Keys.ENTER) 
    time.sleep(1) 
