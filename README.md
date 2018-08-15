# Puppeteer With Mocha

## Summary

This project uses [Puppeteer](https://developers.google.com/web/tools/puppeteer/) to automate the testing of Adobe DTM implementation.

[Mocha](https://mochajs.org/) testing framework is used to run the tests.

[Chai](http://www.chaijs.com/) assertion lirary is used. We are using expect in a BDD format.

The following are tested:

    √ _satellite object exist
    √ DTM is initialized
    √ DTM library name exist
    √ DTM Analytics tool is loaded
    √ DTM Visitor ID services tool is loaded
    √ Userzoom feedback button displayed (also takes a screenshot if UserZoom is present under test/screenshots)

## Requirements

You will need node.js and npm install on your machine.

## Intall 

```
npm install
```

## Run test

```
npm test --url=valid_url
```

## Test ouputs

### All Success

```
Validate the DTM implementation for URL https://www.example.com
    √ _satellite object exist
    √ DTM is initialized
    √ DTM library name exist
    √ DTM Analytics tool is loaded
    √ DTM Visitor ID services tool is loaded
    √ Userzoom feedback button displayed (315ms)
```

  6 passing (4s)


### With failures

```
Validate the DTM implementation for URL https://www.example.com
    √ _satellite object exist
    √ DTM is initialized
    √ DTM library name exist
    √ DTM Analytics tool is loaded
    √ DTM Visitor ID services tool is loaded
    1) Userzoom feedback button displayed


  5 passing (3s)
  1 failing

  1) Validate the DTM implementation for URL https://www.examle.com
       Userzoom feedback button displayed:
     AssertionError: expected [] not to be empty
      at Context.<anonymous> (test\puppeteer1.js:72:26)
      at <anonymous>
      at process._tickCallback (internal/process/next_tick.js:188:7)



npm ERR! Test failed.  See above for more details.
```