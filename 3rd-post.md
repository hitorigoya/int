# アクティブな要素を取得する
これは、現在のブラウジングコンテキストでフォーカスを持っているDOM要素を追跡（または）検索するために使用されます。

```py
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://www.google.com")
driver.find_element(By.CSS_SELECTOR, '[name="q"]').send_keys("webElement")

# Get attribute of current active element
attr = driver.switch_to.active_element.get_attribute("title")
print(attr)
```
