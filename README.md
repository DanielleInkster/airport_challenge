# Airport Challenge - Week 1 #

## Challenge Description ##
We have a request from a client to write the software to control the flow of planes at an airport. The planes can land and take off provided that the weather is sunny. Occasionally it may be stormy, in which case no planes can land or take off. 

### Here are the user stories that we worked out in collaboration with the client: ###
```
**As an air traffic controller**  
So I can get passengers to a destination 
I want to instruct a plane to land at an airport**

**As an air traffic controller** 
So I can get passengers on the way to their destination 
I want to instruct a plane to take off from an airport and confirm that it is no longer in the airport

**As an air traffic controller** 
To ensure safety 
I want to prevent takeoff when weather is stormy 

**As an air traffic controller**  
To ensure safety 
I want to prevent landing when weather is stormy 

**As an air traffic controller**  
To ensure safety 
I want to prevent landing when the airport is full 

**As the system designer** 
So that the software can be used for many different airports
I would like a default airport capacity that can be overridden as appropriate
```
Your task is to test drive the creation of a set of classes/modules to satisfy all the above user stories. You will need to use a random number generator to set the weather (it is normally sunny but on rare occasions it may be stormy). In your tests, you'll need to use a stub to override random weather to ensure consistent test behaviour.

Your code should defend against edge cases such as inconsistent states of the system ensuring that planes can only take off from airports they are in; planes that are already flying cannot take off and/or be in an airport; planes that are landed cannot land again and must be in an airport, etc.

For overriding random weather behaviour, please read the documentation to learn how to use test doubles: https://www.relishapp.com/rspec/rspec-mocks/docs . There’s an example of using a test double to test a die that’s relevant to testing random weather in the test.

Please create separate files for every class, module and test suite.

In code review we'll be hoping to see:

* All tests passing
* High Test coverage (>95% is good)
* The code is elegant: every class has a clear responsibility, methods are short etc.
* Reviewers will potentially be using this code review rubric. Referring to this rubric in advance will make the challenge somewhat easier. You should be the judge of how much challenge you want this weekend.

======================================

## Technologies
* Ruby 2.6.0
* Rake
* Rspec
* Rubocop 0.71.0
* Simplecov

## How to Install and Run
```bash
> git clone git@github.com:DanielleInkster/airport_challenge.git
> bundle install
> irb
> require './lib/airport.rb'
```
### How to Run Tests
```bash
> rspec # Run the tests to ensure it works
> rubocop # Check code quality
```

### Code Quality

#### Rspec
![Rspec Coverage](work/images/rspec.png)

#### Rubocop
![Rubocop](work/images/rubocop.png)

======================================

## Feature Test ##
![](work/images/Screenshot%202019-09-23%20at%2012.43.05%20AM.png)
![](work/images/Screenshot%202019-09-23%20at%2012.49.45%20AM.png)
![](work/images/Screenshot%202019-09-23%20at%2012.51.18%20AM.png)

