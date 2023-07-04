Task 1 - GitHub
Task Description
Manage GitHub scripts and documents
![Task 1 Screenshot](task1_screenshot.png)

Task Preparation
Create a folder named "Devasc_Skills" in the DEVASC virtual machine.
Start a Git repository in the "Devasc_Skills" folder.

Task Implementation
Created a local repository using the git init command.
Created a GitHub repository named "Devasc_Skills_DO".
Connected the local repository to the GitHub repository using git remote add origin https://github.com/davidoluwaseun/Devasc_Skills_DO.
Uploaded the local files to GitHub after each task using appropriate Git commands.

Task Troubleshooting
No major issues encountered during the implementation.

Task Verification
Screenshot: GitHub Repository

# GitHub


Task 2: Ansible
Task Description
![Task 2 Screenshot](task2_screenshot.png)

Task Preparation
[...]

Task Implementation
[...]

Task Troubleshooting
[...]

Task Verification
[...]


# Ansible



Task 3: Docker
Task Description
[...]

Task Preparation
[...]

Task Implementation
[...]

Task Troubleshooting
[...]

Task Verification
[...]


# Docker





Task 4: Jenkins
Task Description
[...]

Task Preparation
[...]

Task Implementation
[...]

Task Troubleshooting
[...]

Task Verification
[...]


# Jenkins






Task 5: restconf
Task Description
[...]

Task Preparation
[...]

Task Implementation
[...]

Task Troubleshooting
[...]

Task Verification
[...]


# restconf



Task 6: Webex
Task Description
Manage GitHub scripts and documents
![Task 6 Screenshot](task6_screenshot.png)

Task Preparation
To perform this task, I did the the following:

create a Webex Teams account
Webex Teams access token
Installed Python on the system
Installed requested library(pip install requests)

Task Implementation
The following steps were taken:

Imported the necessary libraries:
python
Copy code
import requests
Defined the Webex Teams API endpoint and access token:
python
Copy code
api_url = "https://api.ciscospark.com/v1"
access_token = "YmU5NjZjMGYtMDI5Ni00YWRmLThjZWUtMjc5Y2M2OTVlYzJiNGFlMzhlNmMtZTVh_PF84_58476986-544b-4c19-b57f-0d76391b2077"
Created a Webex Teams space using the API:

def create_space():
    url = api_url + "/rooms"
    headers = {
        "Authorization": "Bearer " + access_token,
        "Content-Type": "application/json"
    }
    data = {
        "title": "devasc_skills_DO",
        "type": "group"
    }
    response = requests.post(url, headers=headers, json=data)
    if response.status_code == 200:
        space_id = response.json().get("id")
        print("Space created successfully with ID:", space_id)
        return space_id
    else:
        print("Failed to create space")
        return None

Added members to the space:


def add_members(space_id):
    url = api_url + "/memberships"
    headers = {
        "Authorization": "Bearer " + access_token,
        "Content-Type": "application/json"
    }
    emails = ["<your-email>", "yvan.rooseleer@biasc.be"]
    for email in emails:
        data = {
            "roomId": space_id,
            "personEmail": email
        }
        response = requests.post(url, headers=headers, json=data)
        if response.status_code == 200:
            print("Member added successfully:", email)
        else:
            print("Failed to add member:", email)
Sent a message to the space:

def send_message(space_id):
    url = api_url + "/messages"
    headers = {
        "Authorization": "Bearer " + access_token,
        "Content-Type": "application/json"
    }
    data = {
        "roomId": space_id,
        "text": "Here are my screenshots of devasc skills-based exam"
    }
    response = requests.post(url, headers=headers, json=data)
    if response.status_code == 200:
        print("Message sent successfully")
    else:
        print("Failed to send message")
Main function to run the script:

def main():
    space_id = create_space()
    if space_id:
        add_members(space_id)
        send_message(space_id)

if __name__ == "__main__":
    main()

Task Troubleshooting
The following problem was encountered:

The email address davidoluwaseun2000@yahoo.com could not be added as a member. 

Task Verification
The quality of the task result can be verified by checking the following:

Successful creation of the Webex Teams space with the assigned space ID.
Successful addition of the member yvan.rooseleer@biasc.be to the space.

# Webex




Task 7: Bash
Task Description
Manage GitHub scripts and documents
![Task 7 Screenshot](task7_screenshot.png)

Task Preparation
To perform this task, you need to ensure the following:

Have access to a network device that supports RESTCONF API.
Install cURL on your Linux machine (if not already installed) using the package manager for your distribution.

Task Implementation
To implement the RESTCONF API calls in Bash, I followed these steps:

Create a bash script file.
Define the necessary variables, such as the IP address of the host, RESTCONF credentials, data format, and interface details.
Construct the REST API URLs for PUT and GET requests.
Set the headers and authentication for the requests.
Prepare the payload data for the PUT request.
Make the PUT request using cURL and capture the status code.
Make the GET request using cURL and capture the status code and interface information.
Output the results.

Task Troubleshooting
Following troubleshooting steps:

I checked the connectivity to the host and ensure it is reachable from your Linux machine.
I verify the correctness of the RESTCONF credentials and API URLs.
Ensure cURL is installed and accessible from the command line.
Validate the payload data format and structure for the PUT request.
Inspect any error messages or status codes returned by the API calls for debugging.

Task Verification
Verified the quality of the result, follow these steps:

Run the bash script.
Check the generated check_restconf_api.txt file for the output.
Ensure that the output includes the current date, start and end markers, status codes, and interface information.
Compare the obtained results with the expected behavior of the RESTCONF API.








# Filtering DNAC Response Data

Task 10: Filtering DNAC Response Data
Description: Filtering DNAC Response Data

**Task Preparation**
To perform this task, I needed:
A virtual DEVASC virtual machine with an internet connection.
Access to a Python execution environment.

**Task Implementation**
I Copied the provided sample script to my Python execution environment.
I replace the XXXXXXXX placeholders in the script with suitable parameters, variables, keys, names, or code as instructed in the comments.
Run the script.
The script uses the DNAC API to retrieve network device information and filters the response data based on certain conditions. It then prints the filtered data to the console.

**Task Troubleshooting**
While implementing this task, the following problems was encountered:

(i) Incorrect credentials: I make sure to provide the correct username and password for DNAC authentication.
(ii) Network connectivity issues: I ensure that your virtual machine has an internet connection to communicate with the DNAC server.

**Task Verification**
To verify the quality of the result, I check if the script produces the expected output similar to the provided "DNAC OUTPUT TASK 10" in the task description. 
Successful execution of the script.
