# AUTOMATING WHATSAPP USING SELENIUM

from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.common.exceptions import NoSuchElementException
import time


options = webdriver.ChromeOptions()
# To Bypass QRCode
options.add_argument('--user-data-dir=C:\\Users\\Levi Ackerman\\AppData\\Local\Google\\Chrome\\User Data\\Default')
options.add_argument('--profile-directory=Default')

PATH = 'C:\Program Files (x86)/chromedriver.exe'
browser = webdriver.Chrome(PATH, options=options)
browser.get('https://web.whatsapp.com/')

# Time for browser to load up
time.sleep(20)


while True: # Loop To to check for unread messages repeatedly
    try:
        # To check for unread messages
        unreadMsgs = browser.find_element_by_class_name('_31gEB')
        unreadMsgs.click()
        time.sleep(5)

        # Message Box
        message_box = browser.find_element_by_xpath("//*[@id='main']/footer/div[1]/div[2]")
        time.sleep(1)
        message_box.send_keys("Hi, I'm busy right now and will reply ASAP. BTW this is an automated message!" "  "  "こんにちは、私は今忙しいのでできるだけ早く返信します。ところでこれは自動メッセージです！ ")
        time.sleep(1)

        # Message send button
        send_button = browser.find_element_by_xpath("//*[@id='main']/footer/div[1]/div[3]/button")
        time.sleep(1)
        send_button.click()

    except Exception as e:
        pass

# NOTE : THIS CODE WILL ALSO REPLY TO GROUP MESSAGES
# YOU CAN DIFFERENTIATE BETWEEN GROUP MESSAGE AND PRIAVTE MESSAGE BY KEEPING THE GROUPS ON MUTE AND USING THE MUTE ICON.
