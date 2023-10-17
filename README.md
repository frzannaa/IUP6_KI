# IUP6_KI
- Farzana Afifah Razak 5025201130
- Rahel Ceclia Purba 5025201155
- Selomita Zhafirah 5025201120
- Shafina Chaerunisa 5025201129
- Muhammad Fadli Azhar 5025201157

This project is a foundational component of a Django-based web application that serves various functions, including user authentication, file uploads with encryption, and data retrieval. 

# Disclaimer
This is the final version of our project and the old one had a lot of modifications to it so we decided to move it here instead, to see the old progress you can see it here > https://github.com/seraaaz/Assignment1_IS_Group

## Django Imports and Setup:
The code starts by importing essential Django modules. Django is a popular Python web framework, and these modules provide crucial functionalities for web development. `EncryptionAlgo` is set to "ARC4," which indicates that the application uses the ARC4 encryption algorithm for securing user data. It's worth noting that the ARC4 algorithm, while historically widely used, has known security vulnerabilities, and its usage should be reviewed for modern security standards.

## User Authentication:
The `login_view` function is responsible for handling user authentication. It processes POST requests, extracting the submitted username and password. It then utilizes Django's built-in functions, `authenticate` and `login`, to verify the user's credentials. If the authentication is successful, the user is logged in, and they are redirected to their profile page. In the case of authentication failure, an error message is displayed to inform the user of the issue.

## File Downloads:
The `download_data` function is designed to allow authenticated users to download specific files associated with their profiles. The function takes a `file_type` parameter, which determines which type of file the user wants to download. Depending on the `file_type`, the code retrieves the corresponding file from the user's profile (e.g., ID card image, medical info file, or fingerprint image). It then constructs a downloadable response and serves the file to the user. This feature is valuable for users who need to access their uploaded data or documents.

## File Upload and Encryption:
The `upload_data` function handles the process of uploading user data. Users can submit various forms, including user information, personal info, medical info, and biometric data. The code first validates the submitted forms to ensure the data is correctly formatted and complies with the application's requirements. After validation, it saves the user's data in the database. Importantly, the code encrypts certain uploaded files, such as the ID card image, medical info file, and fingerprint image, using the "ARC4" algorithm before saving them. The use of encryption is a critical security measure to protect sensitive user information from unauthorized access.

## Profile Page:
The `profile` function serves as a secure profile page accessible only to authenticated users. It retrieves the user's data, personal info, medical info, and biometric data from the database and renders these details on the profile page. This feature allows users to view their own information conveniently and securely.

## URL Routing:
The code leverages Django's URL routing to direct incoming requests to the appropriate views. This routing system ensures that the user's request is directed to the correct function or view within the application.

## Imported Modules and Classes:
The code imports various forms and models from application-specific modules. These forms and models define the structure and validation rules for the data that users submit. Additionally, the code imports a `cryptoHasher` class from an external module, for handling encryption and decryption processes. This separation of concerns follows good software engineering practices.

## Exception Handling and Feedback:
The code includes mechanisms for handling errors and providing feedback to users. When form validation fails, error messages are generated using Django's `messages` framework. This feedback is vital for user experience, ensuring that users receive clear and actionable information when they make mistakes while submitting data.

## File Management and Storage:
The code employs Django's file storage mechanisms, particularly `default_storage`, for managing and storing user-uploaded files. This ensures that files are stored securely and can be easily retrieved when needed. The code also demonstrates file path manipulation to access, encrypt, and delete files as necessary. Proper file management is crucial for maintaining a well-organized and secure data storage system.

## Performance Logging:
In addition to its functional aspects, the code logs the time taken for the upload process. Logging is a valuable practice for monitoring the application's performance. In this case, it helps measure the time it takes to process and encrypt user-uploaded files. It is crucial for optimizing the application's efficiency.



## Running Time Analysis

![S__10502313](https://github.com/frzannaa/IUP6_KI/assets/100435004/60e1e63b-3f83-47cd-b1d3-dc1b76aeda63)


The running time analysis in the provided log indicates the time intervals between different log entries. Here's a breakdown of the time intervals between specific events:

1. Time Interval from the first request to the second request: 10 seconds
2. Time Interval from the second request to the file operation section: Approximately 1 minute and 34 seconds
3. Time Interval from the start of the file operations to the delta time measurement: Approximately 1 minute and 12 seconds
4. Delta Time Measurement: 1.019479 seconds
5. Time Interval from the delta time measurement to the third request: Approximately 1 minute and 53 seconds


# Web Screenshots

Login Page
![Login page](https://github.com/frzannaa/IUP6_KI/assets/100435004/f9429f97-c58c-4b01-b239-c186e7d55747)

Form Page
![form page](https://github.com/frzannaa/IUP6_KI/assets/100435004/30d73c5d-c578-4d70-b186-d4494c94a697)

Saved Successfully page
![Saved successfully page](https://github.com/frzannaa/IUP6_KI/assets/100435004/a1136a80-53da-4085-a869-f95dbe22acc4)

Profile Page
![profile page](https://github.com/frzannaa/IUP6_KI/assets/100435004/cf4e3a03-d716-40e1-9629-7ad9a75a2ecf)

Downloadable Contents
![downloaded content](https://github.com/frzannaa/IUP6_KI/assets/100435004/46d3f88a-8006-4100-80af-153834c5e969)

Database page
![database](https://github.com/frzannaa/IUP6_KI/assets/100435004/5122fd97-1e69-4d30-b018-5589d966822f)

