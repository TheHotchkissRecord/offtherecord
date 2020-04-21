# ![Off the Record Banner](https://graphics.thehr.org/newsletter/offtherecord.png)
Off the Record is the Hotchkiss Record's Newsletter, distributed bi-weekly on the off-weeks of the print run to the student body as well as subscribers. 

## Installation
Off the Record is compiled in [`mjml`](https://mjml.io/), using [`node.js`](https://nodejs.org/en/). It is sent as HTML embed within an email. To set up the environment––run
```shell
git clone https://github.com/TheHotchkissRecord/offtherecord.git
```
or use the local GitHub client to clone the repo in your desired directory. Initiate the necessary packages and dependencies:
```shell
npm init -y && npm install mjml
```
```shell
export PATH="$PATH:./node_modules/.bin"
```
(*You might need to [install](https://nodejs.org/en/) node & npm onto your device first.*)

## Documentation
An automaton has been created to automatically create `.mjml` files for Off the Record. Its name is *Henry*. ~~Simply double-click the executable named `henry` from the `offtherecord` folder and Henry will guide you through the necessary steps.~~ To use the most up-to-date version of Henry, clone the [Henry repository](https://github.com/TheHotchkissRecord/henry) and follow the instructions there.

(The old documentation for manually compiling newsletters can still be found [here](https://github.com/TheHotchkissRecord/offtherecord/blob/master/old_documentation.md).)
