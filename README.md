# cert-bot

Tool for generate letsencrypt-cert (SSL cert)

## Steps 
1. Run command ```docker-compose run --rm app certonly --manual --preferred-challenges dns"```
2. You will see input prompt ```Enter email address (used for urgent renewal and security notices)``` and enter your subcribe email
3. In ```Read the Terms of Service``` select Y
4. Enter the domain like ```*.example.co.th``` and we will get challenge key. Please copy the challenge key to DNS provider. For example, we got ```IYTkRppMiNGWD_iHlJLYrj145IvPSmP5jIY44D9XnIg``` and I go to cloudflare and search TXT _acme-challenge in DNS. Copy paste challenge key to content.
![Screen Shot 2565-10-19 at 09 50 20](https://user-images.githubusercontent.com/8089883/196586093-bc7fd45e-3578-458f-b7f5-633f092ad766.png)

5. Enter continue step in terminal
6. Finish, we will see successfully received certificate and path where you get cert.
7. Cert will place in folder ```cert-data/live/example.co.th/```
