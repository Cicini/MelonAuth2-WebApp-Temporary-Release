# MelonAuth2-WebApp-Temporary-Release
Temporary Release of MelonAuth2 WebApp, this repository will no longer be updated after the official repository is opened.

## `config.json`

The web app will request `/config.json` during initialization for runtime configurations. You will need to create a `config.json` under web root folder with valid JSON data (or at least handle that GET request with valid response) to make the web app work properly.

Available configurations:

* `api_prefix` **(Required)**

    The URL and base path of your Melon Auth API backend. The web app will prefix the actual API call with this value. For example: if your backend runs at `https://api.example.com` and has a base path `/auth`, then you need to set this value as `"https://api.example.com/auth"`, and the web app will call the verification API as `https://api.example.com/auth/verify/123456`.
   
* `footer_content` (Optional)

    Custom footer content which is displayed at the bottom of the web app. Note that this content will be rendered as unescaped-raw HTML. Be sure to not involving dangerous things.

Example:
```shell script
{
  "api_prefix": "https://api.example.com/auth",
  "footer_content": "<a href='https://github.com/LanguaLab' target='_blank'>© LanguaLab</a>. All rights reserved."
}
```
## How to use
zh-cn: https://cicini.moe/article/1/

## Official Public API
| API URL | APP URL | secretKey | serverName |
| ----------- | ----------- | ----------- | ----------- |
| https://verify.nyaa.cf/api | https://verify.nyaa.cf/ | langualab_public | langualab |

## Unofficial Public API
These contents are provided by third parties, and we do not guarantee that they are safe, please use them as appropriate.
| API URL | APP URL | secretKey | serverName |
| ----------- | ----------- | ----------- | ----------- |
| https://mauth.blingwang.cn/api/ | https://mauth.blingwang.cn/ | MelonAuth_Blw | MelonAuth_Blw |
------------------------------------

如果你想在二级目录中使用此构建，请将js, css, fonts等资源文件放入根目录或手动修改路径即可正常读取.

若想直接构建二级目录版WebApp

构建方法见

https://cicini.moe/article/1/
