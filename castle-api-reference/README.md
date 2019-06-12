# Castle API Reference Postman Collection

This collection replicates the [API Reference documentation](https://castle.io/docs/api_reference) on Castle's website.

This collection serves as an example to showcase Postman's documentation feature for a collection. With a few clicks, documentation for this collection (with saved examples included) [was published to a public endpoint](https://documenter.getpostman.com/view/7520859/S1TbTv4e).

## Instructions for Use

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/b4beebc4889fde9730aa#?env%5BAPI%20Reference%20Collection%5D=W3sia2V5IjoiY2FzdGxlX2FwaV9zZWNyZXQiLCJ2YWx1ZSI6Im51bGwiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InVzZXJfaWQiLCJ2YWx1ZSI6IjEiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InVzZXJfZW1haWwiLCJ2YWx1ZSI6InVzZXIxQGNhc3RsZS5pbyIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoicmVnaXN0ZXJlZF9hdCIsInZhbHVlIjoiMTU2MDI5MDQ5MjI5MSIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiZGV2aWNlX3Rva2VuIiwidmFsdWUiOiJudWxsIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJjbGllbnRfaWQiLCJ2YWx1ZSI6Im51bGwiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im9yaWdpbl9pcF9hZGRyZXNzIiwidmFsdWUiOiJudWxsIiwiZW5hYmxlZCI6dHJ1ZX1d)

To use this collection, please download the [API Reference Collection Environment File](https://github.com/castle/postman/blob/master/castle-environments/API%20Reference%20Collection.postman_environment.json) which can be found in the `/castle-environments` folder of this repository.

After downloading the `.json` environment file, import the environment into your Postman application. You will then need to set the `castle_api_secret` environment variable to your Castle API secret. 

Some of the requests will require a `device_token` parameter to be set. You may set this manually if you have a specific device to check, or you can alternatively use the first request "Authenticate a User Login" to retrieve a device token. The test script for that first request will automatically pop[ulate the `device_token` parameter.