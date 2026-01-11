docker run -d -p 1566:1566   --name pansou-and-pancheck  -e SEARCH_API_URL=http://192.168.50.50:1514   -e CHECK_API_URL=http://192.168.50.50:7024/api/v1/links/check   silent7897/pansou-and-pancheck:latest

SEARCH_API_URL：你的pansou服务地址
CHECK_API_URL：你的pancheck服务校验接口地址

https://github.com/fish2018/pansou
https://github.com/fish2018/pansou-web
https://github.com/Lampon/PanCheck
