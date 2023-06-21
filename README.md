- 👋 Hi, I’m @Sss0006666789002
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Sss0006666789002/Sss0006666789002 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from selenium import webdriver

# Set the path to the appropriate WebDriver for your mobile browser
driver_path = '/path/to/chromedriver'

# Set the desired number of tabs to open
num_tabs = 100

# Configure the options for mobile emulation
mobile_emulation = {
    "deviceMetrics": {"width": 360, "height": 640, "pixelRatio": 3.0},
    "userAgent": "Mozilla/5.0 (Linux; Android 11; Pixel 4) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.81 Mobile Safari/537.36",
}

# Configure the Chrome options
chrome_options = webdriver.ChromeOptions()
chrome_options.add_experimental_option("mobileEmulation", mobile_emulation)

# Open the browser with the specified options
driver = webdriver.Chrome(executable_path=driver_path, options=chrome_options)

# Open multiple tabs
for _ in range(num_tabs):
    driver.execute_script("window.open('https://www.youtube.com');")

# Close the browser when finished
driver.quit()
