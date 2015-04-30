# LiveCode-MiniTest
Mini Test is a small, easy to use testing toolkit for LiveCode. It can be used in both GUI scripts and server scripts. Thanks to LiveCode's messaging, it can be used to test GUI applications as well as commands and handlers.

## How It Works
Mini Test consists of a set of handlers which you can use to create automated test scripts. There are at least three scripts needed to run a MiniTest test script. The test script itself, MiniTest, and the stacks or scripts being tested (and any sub-stacks they may include.)

## Testing with Mini Test
There are two levels of tests in MiniTest. The highest level is a Test Run which may contain individual tests or Test Files. The lower level is a Test File which contains a individual tests. (A Test File cannot be included in a Test File). Actually, MiniTest is quite flexible and is happy with any number of test runs and test files in a single script. It is also happy to process only Test Runs (without Test Files) and only Test Files (without Test Runs).

A Mini Test script is written by simply interspersing Mini Tests commands in your testing code.

An indivdual test consist of four elements:


## Mini Test Handlers
Mini Test consists of the handlers listed below. The name of all the Mini Test the handlers is pre-fixed with "MT." which should practically reduce the chance to nil of a Mini Test handler having the same name as one of your handlers.

###MT.setTestReport pTestReporter
This command prepares Mini Test to run in "GUI mode". It requires the name of a LiveCode Field to be supplied for it to use to report the test results. For example, if you want Mini Test to display it's result in a Field called "Mini Test Report", you would use:
```
MT.setTestReport "Mini Test Report"
```

### MT.startTestRun
This command prepares Mini Test to perform a test run.
```
MT.startTestRun
```

### MT.startTestFile pTestFileName
This command informs Mini Test that a new test file is starting. You need to provide a name for the test file to Mini Test.
```
MT.startTestFile "My First Mini Test File"
```

### MT.startTest pTestName
This command signfies the start of an individual test. A name is required so that Mini Test can report which test fails (if any do). 
