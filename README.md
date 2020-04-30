# RDC-Ranorex

### Environment Setup

1. Global Dependencies
    * Make sure you have Ranorex installed on your local machine (https://www.ranorex.com/).

2. Project Dependencies
	* Ensure your Sauce Labs Real Device account has access to the devices specified in the config.yml file.

3. In XCode under your target's `Signing & Capabilities` select your team and make sure `Automatically manage signing` is        checked.

4. Select `Generic iOS Device` in the top left dropdown and choose `Product->Build For->Testing`.

5. After that the `Product` group in the navigator should show a few files:
   * LoanCalc.app
   * LoanCalcTests.xctest
   * LoanCalcUITests.xctest
   Right click on LoanCalc.app and choose `Show in Finder` to get the location of the build.
   Copy `LoanCalc.app` and `LoanCalc-Runner.app` from that folder to your main directory containing your runner.

6. Create a new folder called `Payload`, copy `LoanCalc.app` into it, compress it, and rename the zip `LoanCalc.ipa`. This is    the ipa you'll upload to Sauce Labs. Instructions at https://wiki.saucelabs.com/display/DOCS/Creating+a+Real+Device+Project

7.  Real Device Application Credential
    * Replace the apiKey in runner.sh with your apiKey. This is found under your App Dashboard -> Automated Testing -> Appium 	  -> Setup Instructions

### Running Tests
```
$ ./runner.sh
```

You can view the results of tests and tests in progress under your app dashboard -> Automated Testing -> XCUITest

### Resources

##### [Sauce Labs Documentation](https://wiki.saucelabs.com/)

##### [Stack Overflow](http://stackoverflow.com/)
* A great resource to search for issues not explicitly covered by documentation.
