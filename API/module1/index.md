## Module 1

### Description
For this task you have to create API test for Yahoo public API.

The Model should support ability to define values for HTTP request parameters

The tests should contain the following verifications:
- HTTP response code
- HTTP headers

### Project stuff
- Finance model https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/model/Finance.mjs
- Tests https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/tests/finance.test.mjs
- Endpoints descriptions https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/configs/AppConfig.cjs

### Preparation

1. Clone the template project https://git.epam.com/dmytro_kanunik/api-test-with-jest
1. Install dependencies ```npm install```
1. Run tests ```npm test```

### Tasks

##### Task 1
Please pay your attention that Finance models method is used for API calling:
https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/tests/finance.test.mjs#L13

This method is noneffective because the HTTP request parameters were hardcoded.
There is a need to develop a method for Finance model to be able to define the following parameters dynamically:
- company
- region
- interval
- range

##### Task 2

Develop 4 test cases and tests for them to verify that the HTTP response code equals 200 when the following parameters 
are put to Finance.getFinanceData():
- company
- region
- interval
- range

As example:
```
    ...
     let { status } = await Finance.getFinanceData({company:'AAPL'});
    ...
```

##### Task 3

Develop 1 test case and test for it to verify that the HTTP response code equals 422 when an invalid
range is used. 

Use the template https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/tests/finance.test.mjs#L17    


##### Task 4

Develop 1 test case and test for it to verify that the HTTP response code equals 404 when an invalid 
company name is used. 

Use the template https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/tests/finance.test.mjs#L25

##### Task 5

Develop 1 test case and test for it to verify that the HTTP response header "**x-request-id**" contains value that corresponds to the regular expression.

Use the template https://git.epam.com/dmytro_kanunik/api-test-with-jest/-/blob/master/tests/finance.test.mjs#L40

### Documentation

Please, use the following manuals to perform tasks:
- https://jestjs.io/docs/getting-started
- https://www.npmjs.com/package/axios
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Status
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
