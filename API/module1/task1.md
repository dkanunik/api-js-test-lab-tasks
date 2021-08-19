# Module 1

## Task 1

### Description
For this task you have to create API test for Yahoo public API.

The Model should support ability to define values for HTTP request parameters

The tests should contain the following verifications:
- HTTP response code
- HTTP headers

### Preparation
1. Clone the template project https://github.com/dkanunik/api-test-with-jest
1. Install dependencies ```npm install```

### Project stuff
- Finance model https://github.com/dkanunik/api-with-jest-simple/blob/main/model/FinanceModel.mjs
- Tests https://github.com/dkanunik/api-with-jest-simple/blob/main/tests/finance.test.mjs
- Endpoints descriptions https://github.com/dkanunik/api-with-jest-simple/blob/main/configs/AppConfig.cjs

### Specification
Please pay your attention that Finance models method is used for API calling:
https://github.com/dkanunik/api-test-with-jest/-/blob/master/tests/finance.test.mjs#L13

This method is noneffective because the HTTP request parameters were hardcoded.
There is a need to develop a method for Finance model to be able to define the following parameters dynamically:
- company
- region
- interval
- range

### Test run
``` npm test```

### Expected result
```
As a FinanceModel API user
    I have to get HTTP response code
        200 for a valid range
        422 for a invalid range
        404 for a nonexistent company
    
    I have to get values for response headers
        content-type
        x-request-id
```

### Documentation
Please, use the following manuals to perform tasks:
- https://jestjs.io/docs/getting-started
- https://www.npmjs.com/package/axios
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Status
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
