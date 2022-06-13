# Lions Rails 6 Issue Ticketing

## Description
This repository is used as an issue ticketing system to track and organise possible issues while testing the Lion's Rails App after upgrading to `rails 6.1.6` and `ruby 2.7.6`.

## Rails 6.1.6 Setup Instructions 
1. Run `git switch master`
2. Run `git pull`
3. Run `git switch rails-upgrade/rails-6.1.6`
4. Run `rbenv install 2.7.6`
5. Run `rbenv exec bundle install --path .bundle`
6. Run `rbenv exec bundle exec rails s` to start the server

## Issue Submission Guidelines
- When submitting issues please follow the following guidelines:
```
## Issue Description (Unexpected Behaviour)
- What kind of error occured? Please provide a short succinct description.
- Can you isolate the error to a specific commit (`git bisect`)? 
- Is it caused by rails upgrade or is it an exisiting error?

## Expected Behaviour
- What should've happened instead? What is the correct output? 
- You can `git switch` to the master branch and compare outputs.

## Steps to Reproduce the Error
1. Step 1 do this
2. Step 2 do this...

## Screenshots / Other Information
- Please provide any other helpful information such as Screenshots
```
