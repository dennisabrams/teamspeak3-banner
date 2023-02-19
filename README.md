<a name="readme-top"></a>

<br />

<div align="center">
  <a href="https://www.teamspeak.com/">
    <img src="https://user-images.githubusercontent.com/122950707/217841700-3ab024cb-e9a8-4132-9cf7-ce850a2696f4.png" alt="Logo" width="30%">
  </a>

  <h3 align="center">TeamSpeak 3 Banner</h3>
  <p align="center">
    <!-- Empty for open graph-->
  </p>

  <p align="center">
    A fully customisable TeamSpeak 3 🔊 banner with server & client information.
    <br />
    <br />
    <a href="#demo">View Demo</a>
    ·
    <a href="https://github.com/dennisabrams/teamspeak3-banner/issues">Report Bug</a>
    ·
    <a href="https://github.com/dennisabrams/teamspeak3-banner/issues">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#introduction">Introduction</a>
      <ul>
        <li><a href="#program-explanation">Program Explanation</a></li>
      </ul>
    </li>
    <li><a href="#getting-started">Getting Started</a></li>
    <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#add-banner">Add Banner</a></li>
    </ul>
    <li><a href="#demo">Demo</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

## Introduction

![ts3](https://user-images.githubusercontent.com/122950707/217850954-a10cedcd-ea12-46da-8eb3-12602d8991e0.png)

There are some great TeamSpeak 3 Banner Generators on GitHub, however I didn't find one with much information about the client & server side and the ability to customize the banner with an extern config file. 

My goal was to create a TeamSpeak 3 Banner with some important features:

<ul>
  <li><b>Full Customization</b></li>
  <li><b>Great Design</b></li>
  <li><b>Client sided information</b> <br /><br />
   <table>
  <tr>
    <td>Upload (last min.)</td>
    <td>Download (last min.)</td>
    <td>Nickname</td>
    <td>Online time</td>
    <td>Total connections</td>
    <td>Flag of the country</td>
  </tr> 
</table>
  </li>
  <li><b>Server sided information</b>
      <br /> <br />
   <table>
  <tr>
    <td>Name</td>
    <td>Logo</td>
    <td>Version</td>
    <td>Info text</td>
    <td>Time</td>
    <td>Date</td>
    <td>Active Clients</td>
    <td>Total Clients</td>
    <td>Channels</td>
    <td>Uptime</td>
  </tr>
     </table>
  
  </li>
  

  </ul>

### Program Explanation

The whole project was made with PHP & TS3 PHP Framework. The program connects to the TeamSpeak 3 server, authenticate and spawn an object for the virtual server to get Client- & Server sided information. This is saved in variables, gets rendered on a image that is generated by PHP and outputs a png file.

![php](https://img.shields.io/badge/PHP-7.4.3-777BB3?style=for-the-badge&logo=php&logoColor=white)


## Getting Started

### Prerequisites

* [PHP](https://www.php.net/releases/index.php) 7.x
* [TeamSpeak 3 Server](https://www.teamspeak.com/de/downloads/#server) v3.4.0 (build >= 1536564584) or higher
* [TeamSpeak 3 PHP Framework](https://github.com/planetteamspeak/ts3phpframework)
* HTTP server for example: [Apache](https://httpd.apache.org/download.cgi), [nginx](https://nginx.org/en/download.html)

### Installation

1. Create a new folder `ts3-banner` inside of the root folder of your web server and clone the repo inside of it. Default path: `var/www/html`.
   ```sh
   git clone https://github.com/dennisabrams/teamspeak3-banner.git ts3-banner
   ```
2. Add the path of your TeamSpeak 3 PHP Framework to the `config.php`.
   ```php
   $ts3_libary = "PATH";
   ```
3. Add your serverquery to the `config.php`.
   ```php
   $serverquery_username = 'serveradmin'; // Default serverquery_username: 'serveradmin'
   $serverquery_password = 'PASSWORD';
   $server_ip = '127.0.0.1'; // Set to '127.0.0.1' if the webserver and TS3 server are hosted on the same server (localhost)
   $serverquery_port = '10011'; // Default serverquery_port: '10011'
   $server_port = '9987'; // Default server_port: '9987'
   ```
### Add Banner
 
1. Open TeamSpeak 3 Client and connect to your Server.
2. Right click your server name.
3. Choose _"Edit Virtual Server"_.
4. Add the URL of the Banner.
   ```
   Banner Gfx URL: http://.../ts3-banner/ts3-banner.php
   ```
5. Change the Gfx Interval to 60 so the Banner will reload every minute.
   ```
   Gfx Interval: 60
   ```
   
> The minimum Gfx Interval from TeamSpeak 3 is 60. Sadly it's not 100% accurate so the time on the banner will be not perfectly synced with the minutes.

## Configuration

![ts3-demo](https://user-images.githubusercontent.com/122950707/218219605-79f7879d-a48a-4e16-a41a-88ef030009cb.png)

The TeamSpeak 3 Banner will look similar to this if there are no changes inside the `config.php` file.
* If you don't have any logo, the name of your server will be shown instead.
* Changing the font style & size of the text is possible.
* Positioning of the text is customizable.
* Background can be switched. 3:1 aspect ratio is recommended but not necessary.
* Displaying the server version can be enabled / disabled.
* Locale information for the time and date can be modified.
* Text is editable for translations.

## Demo

You can [join the TeamSpeak Sever](https://projekt-eleven.eu/eleven/redirects/ts3Redirect.php) of my german gaming community [Projekt-Eleven](https://projekt-eleven.eu/) to see the TeamSpeak 3 Banner in action.
<!-- LICENSE -->
## License

Distributed under the MIT License. See [`LICENSE`](https://github.com/dennisabrams/teamspeak3-banner/blob/main/LICENSE) for more information.


<!-- CONTACT -->
## Contact

Dennis Abrams - contact@dennis-abrams.com

Project Link: [https://github.com/dennisabrams/teamspeak3-banner](https://github.com/dennisabrams/teamspeak3-banner)

<p align="right"><a href="#readme-top">back to top ⬆</a></p>
