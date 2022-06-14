# Lions Rails 6 Issue Ticketing

## Description
This repository is used as an issue ticketing system to track and organise possible issues while testing the Lion's Rails App after upgrading to `rails 6.1.6` and `ruby 2.7.6`.

## Rails 6.1.6 Setup Instructions 
1. Run `git switch master`
2. Run `git pull`
3. Run `git switch rails-upgrade/rails-6-testing`
4. Run `rbenv install 2.7.6`
5. Run `rbenv exec bundle install --path .bundle`
6. Run `rbenv exec bundle exec rails s` to start the server

## Setting up the database
Make sure to use the last database dump(13062022) when testing to help identify data discrepancies
1. Download the latest database dump from the Google Drive
2. Run `gunzip < your_backup_file.sql.gz | psql lions_rails_dev`
3. Run `bundle exec rails db:migrate`

## Rails Testing Procedure (Full Scale Test [But not limited to])
- Read Only Check
- CUD Check
- Check Related Pages
### Notes:
- All Buttons Work Correctly
- All Pages load Correctly
- Check for errors/deprecation warnings in the console
- Check data consistency with staging
- etc.

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
