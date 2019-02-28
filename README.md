# Heroku Accounts

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

Helps use multiple accounts on Heroku.

## Installation

    $ heroku plugins:install heroku-accounts

## Usage

To add accounts:

    $ heroku accounts:add personal
    Enter your Heroku credentials.
    Email: david@heroku.com
    Password: ******

To add single sign-on (SSO) accounts:

    $ heroku accounts:add work --sso
    Enter your organization name: my-company-name
    Opening browser for login... done
    Enter your access token (typing will be hidden): **********************************

To switch to a different account:

    $ heroku accounts:set personal

To list accounts:

    $ heroku accounts
    * personal
    work

To find current account:

    $ heroku accounts:current
    personal

To remove an account:

    $ heroku accounts:remove personal
    Account removed: personal


If you want to position yourself with the account faster, simply add it to your zshrc or .bashrc, to make it even easier, I’ve added the following aliases to my ~/.zshrc (or ~/.bashrc):

```
# Heroku
alias hp='heroku accounts:set personal'
alias hw='heroku accounts:set work'
```
