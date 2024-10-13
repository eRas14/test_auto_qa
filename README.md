# Автотест для проверки наличия футера и кнопки-виджета на странице "Компания"
Автотест написанный на Python с использованием библиотеки Selenium. Тест проверяет наличие элемента футера и кнопки-виджета/

```from selenium import webdriver
from selenium.webdriver.common.by import By

#Поиск футера и кнопки-виджета на странице "Компания" https://only.digital/company

browser = webdriver.Firefox()
browser.implicitly_wait(2)

browser.get("https://only.digital/company")

#Поиск элемента футер по тегнейму
try:
    browser.find_element(By.TAG_NAME, "footer") 
    print("Элемент footer присуствует на странице")
except:
    print("Элемент footer не найден на странице")

#Поиск кнопки виджета по классау
try:
    browser.find_element(By.CLASS_NAME, "kUMIZv") 
    print("Кнопка виджет присуствует на странице")
except:
    print("Кнопка виджет не найдена на странице")


browser.quit()
