# Protractor Notes


#### command to run tests
````
grunt protractor:singlerun --specs=test/e2e/config/buildings.spec.js
````

### 8/28/2017
>```
Error: No selenium server jar found at /home/rjperri/Development/sl-beacon/sl-beacon-ui/node_modules/protractor/selenium/selenium-server-standalone-2.52.0.jar. Run 'webdriver-manager update' to download binaries
```
tried running this statement, didn't work
```
node ./node_modules/grunt-protractor-runner/scripts/webdriver-manager-update
```
Tried what cameron said, to uncomment  the line directConnect:true
New error:
```
Error message: Could not find chromedriver at /home/rjperri/Development/sl-beacon/sl-beacon-ui/node_modules/protractor/selenium/chromedriver_2.27. Run 'webdriver-manager update' to download binaries.
```

### 8/29/2017
> added this to package.json
```json
"scripts": {
    "webdriver-update": "webdriver-manager update"
}
```
ran
```
sudo npm install
```
then ran
```
npm run webdriver-update
```
[src](https://stackoverflow.com/a/42453067/3842570)
Result: same error :(
I think the issue is that no **selenium** folder is being created in the **protractor** folder in node\_modules
The command did install it in _ /sl-beacon/sl-beacon-ui/node\_modules/protractor/node\_modules/webdriver-manager/selenium _
so maybe if I point the protractor.config.js to look at that direcrory?
**Success** well at least the test started up, now a new error

> New Error
```
Error: /home/rjperri/Development/sl-beacon/sl-beacon-ui/test/e2e/api/beacon.api.js:97
            var auth = utils.createAuthenticationString(person.userName, person.password);
                ^^^^
SyntaxError: Unexpected identifier
```
fixed this error removing that line from the beacon.api.js file

> New Error
```
No specs found
```
this was cause by add adding a '\' to the run test command
right now I'm using the selenium web driver instead of the chrome driver

> Now I'm trying to run honor-code.spec.js
New Error:
```
Message:
    Failed: common.createStudent is not a function
  Stack:
    TypeError: common.createStudent is not a function
```
Looks like _createStudent_ was taken out of _common_ so maybe try using _createEnrolledStudent_ in _faker.api_

### 8/30/2017
