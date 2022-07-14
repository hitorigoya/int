# 要素から要素を検索
これは、親要素のコンテキスト内で一致する子のWebElementのリストを見つけるために利用されます。 これを実現するために、親WebElementは’findElements’と連鎖して子要素にアクセスします。

```py
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://www.example.com")

# Get element with tag name 'div'
element = driver.find_element(By.TAG_NAME, 'div')

# Get all the elements available with tag name 'p'
elements = element.find_elements(By.TAG_NAME, 'p')
for e in elements:
    print(e.text)
```