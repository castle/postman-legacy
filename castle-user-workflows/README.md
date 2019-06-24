# Castle User Workflows Postman Collection

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/076a6c2af9bf37ff74e1#?env%5BAPI%20Reference%20Collection%5D=W3sia2V5IjoiY2FzdGxlX2FwaV9zZWNyZXQiLCJ2YWx1ZSI6Im51bGwiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InVzZXJfaWQiLCJ2YWx1ZSI6IjEiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6InVzZXJfZW1haWwiLCJ2YWx1ZSI6InVzZXIxQGNhc3RsZS5pbyIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoicmVnaXN0ZXJlZF9hdCIsInZhbHVlIjoiMTU2MDI5MDQ5MjI5MSIsImVuYWJsZWQiOnRydWV9LHsia2V5IjoiZGV2aWNlX3Rva2VuIiwidmFsdWUiOiJudWxsIiwiZW5hYmxlZCI6dHJ1ZX0seyJrZXkiOiJjbGllbnRfaWQiLCJ2YWx1ZSI6Im51bGwiLCJlbmFibGVkIjp0cnVlfSx7ImtleSI6Im9yaWdpbl9pcF9hZGRyZXNzIiwidmFsdWUiOiJudWxsIiwiZW5hYmxlZCI6dHJ1ZX1d)

This collection includes several scenarios that showcase abilities of the Castle product.

The requests in a folder are designed to be run in order, including sub-folders. The reason for this ordering is that some of the user workflows are designed to make the Castle API respond in specific ways. One example is when Castle returns a `challenge` verdict (rather than `allow`) once authentication requests begins to deviate from a user's normal authentication context patterns. The requests use pre-request scripts and update environment variables via test scripts in order to create this context and elicit the expected responses from the Castle API.

This means that with all sub-folders expanded, the requests are designed to run from top to bottom in order for all tests to pass. The collection still needs some work to elicit expected Castle responses 100% of the time - sometimes `allow` verdicts are expected to be `challenge` by the tests. If you run the collection and you get failures in the tests, try running it again and submit a PR to update the collection sequence or data in order to make improvements.

## Instructions for Use

To use this collection, please download the [API Reference Collection Environment File](https://github.com/castle/postman/blob/master/castle-environments/API%20Reference%20Collection.postman_environment.json) which can be found in the `/castle-environments` folder of this repository.

After downloading the `.json` environment file, import the environment into your Postman application. You will then need to set the `castle_api_secret` environment variable to your Castle API secret. 

### Running the Entire Collection

The Postman Collection Runner may be used to run the entire collection in this folder. All requests will execute from top-bottom, and tests are designed to pass when the collection is run in this order. Be sure to select your previously-defined Castle API environment when you open the collection runner. 

## Included Examples
- User Authenticates with Castle for First Time
- User's Device is Revoked
- Castle Challenges Anomaly Behavior
  - Challenge is Completed
  - Challenge is Failed

Each of the examples above contains multiple requests to demonstrate Castle functionality. Each request contains any necessary authentication configuration, pre-request scripts, and tests to validate that the Castle API has returned the expected responses.
