# Meteor with React and Blaze - Quick and Dirty

## To run this repo
1. Clone this repo
2. Perform step 3 in below section (node_modules are not in repo and have to be added at command line).
3. Run ```meteor``` from project folder.

## To recreate
Refer to http://guide.meteor.com/react.html
1. ```meteor create meteor-with-react_and_blaze_quick_and_dirty```
2. ```cd meteor-with-react_and_blaze_quick_and_dirty```
3. ```meteor npm install --save react react-dom```
4. Added file/react component ```/client/HelloWorld.jsx```
5. Added the following div to ```main.html``` at line 11:

  ```<div id="embeddedReactComponent"></div>```
6. Inserted the following lines into ```main.js``` at line 5:

```
import HelloWorld from './HelloWorld.jsx'
import React from 'react';
import { render } from 'react-dom';

Meteor.startup(() => {
  render(<HelloWorld/>, document.getElementById('embeddedReactComponent'));
});
```
