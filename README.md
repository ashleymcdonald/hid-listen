# hidlisten

Originally forked from https://github.com/zvecr/hid-listen due to repository being readonly / project abandoned.

> Library for acquiring debugging information from usb hid devices

[![npm version](https://badge.fury.io/js/hidlisten.svg)](https://badge.fury.io/js/hidlisten)

NodeJS implementation of <https://www.pjrc.com/teensy/hid_listen.html>.

## Install

```shell
$ npm install hidlisten
```

## Usage

```js
const HIDListen = require('hidlisten');

const inst = new HIDListen();
inst.on('connect', () => {
    console.log('Listening:');
});
inst.on('disconnect', () => {
    console.log('Device disconnected.');
    console.log('Waiting for new device:');
});
inst.on('data', (data) => {
    console.log(data);
});
```
