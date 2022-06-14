# LamBot
LamBot is a bot creation guide to automate booking/reservation system. This bot is powered by AWS Lambda and Python Selenium
This bot is a cloud bot using severless AWS Lambda with Headless Chrome Webdriver along with Selenium
# Requirements

 - AWS Lambda
 - Selenium
 - Python 3.7
 - Linux
 - Docker

# Installation

 - Create ZIP file for Lambda Layer
	
	Clone the repo
    ```
    chmod +x chrome_headless_lambda_layer.sh
    ./chrome_headless_lambda_layer.sh
    ```
    
 - AWS Lambda Configuration
	
	Create a new lambda function 
	```
	Create a new lambda function on your AWS Lambda dashboard
	Select python 3.7 as runtime
	Select x86_64 as architecture
	Leave the rest as default value
	```

	Upload layer
	```
	Go to layers menu on the main AWS Lambda dashboard
	Create a new layer
	Select "Upload a .zip file"
	Upload the zip file created from the previous script
	Select python 3.8 as compatible runtimes
	Leave the rest as default/empty
	```

	Configure layer for lambda function
	```
	Go to your lambda function details
	Scroll down and click on 'add a layer'
	Select custom layers
	Select the recently uploaded layers
	```
	Now it is time to upload your Selenium bot script ! (You can upload the test_script.py for testing)
	```
	Upload using Zip file
	OR
	Copy paste your code in the editor!
	And finally deploy your code !
	```


# Troubleshoot

 - If you encounter ``Task timed out after 3.01 seconds`` error, it is usually related to the memory of your lambda function
 
	 To change your memory allocation, go to ``configuration`` > ``General Configuration`` > ``Edit``

	And then update your memory accordingly
