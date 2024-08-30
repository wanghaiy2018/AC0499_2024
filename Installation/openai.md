
Accessing and Using Your OpenAI API Key  Gain an OpenAI API Key:
1.	To do this head to the OpenAI API Dashboard and create/login to an account. (https://platform.openai.com/assistants).
2.	After logging into an account, on the left side of the dashboard select ‘API Keys’.
3.	Next, click ‘Create new secret key’ in the top right corner of the page, from here you can create a name for your key, the project it is used for (if you have multiple keys and projects), and decide the permissions. 
4.	After deciding the settings for your key, click ‘Create secret key’ in the bottom right of the menu. 
5.	This will show your given key, make sure to copy your key and save it in a place of your choosing for later. This will be the only time you can access it. Afterwords, select ‘Done.’

Setting your OpenAI API Key as an Environment Variable:
1.	After obtaining your API key, open the command prompt on your computer. 
2.	Run the following command in the cmd prompt, replacing “<yourkey>” with your API key:	setx OPENAI_API_KEY <yourkey>
3.	To confirm the environment variable was set, run the following command in the cmd prompt, this should repeat your API key back to you:	echo %OPENAI_API_KEY%
4.	After setting the environment variable you will have to restart your computer in order to use it.
Testing if your API Key works:
1.	Run this code in python, it should access your environment variable and write a write a haiku about recursion in programming.


2.	import os
3.	from openai import OpenAI
4.	
5.	client = OpenAI(
6.	    api_key = os.environ.get("OPENAI_API_KEY"),
7.	)
8.	
9.	completion = client.chat.completions.create(
10.	    model="gpt-4o-mini",
11.	    messages=[
12.	        {"role": "system", "content": "You are a helpful assistant."},
13.	        {
14.	            "role": "user",
15.	            "content": "Write a haiku about recursion in programming."
16.	        }
17.	    ]
     
    )
    print(completion.choices[0].message)
