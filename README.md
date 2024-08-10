*Based on GitHub Release downloads and DockerHub pulls.*

### What is Cryptofolio?

Cryptofolio is an open-source, and self-hosted solution for tracking your cryptocurrency holdings. It features a web interface, an Android mobile app, and a cross-platform desktop application for Windows, macOS, and Linux. These three platforms all work using a RESTful API, which you'd have to host yourself.


### What can it do?

It can provide you with a quick glance at the market, while also keeping track of your assets and their value. It also includes a feature that allows you to share your portfolio in a read-only way with anyone you choose to give the link to. In order to set this up, please go into the "Settings" section of the web interface, enable portfolio sharing, set a PIN code, and use the generated URL to view your assets without having to login. This allows you to share your portfolio with friends, family, or strangers without them being able to modify it.


### How do I set it up? 

If you use DockerHub, then simply follow the instructions on the [page there](https://hub.docker.com/r/xtrendence/cryptofolio).

Use `docker pull xtrendence/cryptofolio:latest` to quickly pull the latest image.

**Initial Username**: admin (the admin account must always have the username "admin")

**Initial Password**: admin

Firstly, download the latest release from the [Releases](https://github.com/aryansingh034/Cryptofolio) section. For the API and website, to ensure you don't get any unfinished code and that everything is compatible, download the "Source code (zip)" file from the Releases section rather than just downloading the source code containing the most recent commits. You'll then have to set up a server on your network using a guide such as [this](https://www.ionos.co.uk/digitalguide/server/tools/xampp-tutorial-create-your-own-local-test-server/) one.

*If you'd rather host it online, you can use a service such as [this](https://www.000webhost.com/free-php-hosting) one in order to get free PHP hosting. Your holdings and such are stored in plaintext, so keep in mind that the hosting provider would be able to see your data. This option is a lot easier though, you'd essentially just have to upload the "api" and "website" folders with whatever storage interface the hosting service provides, and you'd be done.*

Once you've set up a server, extract the content of the ZIP archive you downloaded from the Releases section, and copy-paste the "api" folder to wherever your server's DocumentRoot directory is (usually C:/xampp/htdocs/), and take note of the URL pointing to the "/api/" directory (you'll need to know your server's local IP for this). For example, if you're hosting it on your own network, the URL would look something like:

http://192.168.1.58:8080/api/

Or on port 80:

http://192.168.1.58/api/

If everything is working correctly, opening that URL with a browser should output the following:

```{ "status": "online" }```

You can then copy the "website" folder into the DocumentRoot directory as well. Install the APK file on your Android phone, launch the app, and enter the URL you took note of earlier, and enter "admin" as your password (you can and should change this in the "Settings" page after you first log in).


### Please keep the following points in mind:

- Since the CoinGecko API is used to fetch and utilize market data (such as the price of a cryptocurrency), your IP will most likely be logged by CoinGecko as you'd be making requests to their servers.
- Coin rankings and data might differ from other websites such as CoinMarketCap. Any inaccuracy would be due to CoinGecko's data being wrong or otherwise different.
- Your PIN code for sharing your portfolio is stored in plaintext.
- CoinGecko's API is limited in terms of both functionality, and how often requests can be made. As such, be careful not to refresh **too** often. Any rate limits are temporary though, you won't get banned or anything permanently.

#### Credits

Chart.js: https://www.chartjs.org/

QR Code Styling: https://qr-code-styling.com/

Flatpickr: https://flatpickr.js.org/

#### Website
![Screenshot](https://i.imgur.com/vunbAIz.png)
![Screenshot](https://i.imgur.com/3JbN8Gt.png)
![Screenshot](https://i.imgur.com/aZdlJ3X.png)
![Screenshot](https://i.imgur.com/tWpbWCP.png)
![Screenshot](https://i.imgur.com/fLAvYmZ.png)
![Screenshot](https://i.imgur.com/wMrUWpy.png)
![Screenshot](https://i.imgur.com/KI2tgVi.png)
![Screenshot](https://i.imgur.com/bSWI2wk.png)
![Screenshot](https://i.imgur.com/ojVRJod.png)
![Screenshot](https://i.imgur.com/7pxv2AG.png)
![Screenshot](https://i.imgur.com/WXwarTn.png)
![Screenshot](https://i.imgur.com/54nMKbM.png)
