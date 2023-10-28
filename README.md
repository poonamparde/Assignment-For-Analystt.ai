# Assignment-For-Analystt.ai
Assignment 
import requests

# Get your API key from Beeper
API_KEY = "YOUR_API_KEY"

# Create a request to send a message
request = requests.post(
    "https://api.beeper.com/v1/linkedin/messages/send",
    headers={
        "Authorization": "Bearer {}".format(API_KEY),
    },
    json={
        "recipient": "RECIPIENT_LINKEDIN_URL",
        "subject": "Message subject",
        "body": "Message body",
    },
)

# Check the response status code
if request.status_code == 200:
    print("Message sent successfully")
else:
    print("Error sending message: {}".format(request.content))
