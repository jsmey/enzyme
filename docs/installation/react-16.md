# Working with React 16

If you are wanting to use enzyme with React 16, but don't already have React 16 and react-dom
installed, you should do so:

```bash
npm i --save react@16 react-dom@16
```

Further, enzyme requires the test utilities addon be installed:

```bash
npm i --save-dev react-test-renderer@16
```

Next, to get started with enzyme, you can simply install it with npm:

```bash
npm i --save-dev enzyme enzyme-react-adapter-16
```

And then you're ready to go!  In your test files you can simply `require` or `import` enzyme:

ES6:
```js
// setup file
import { configure } from 'enzyme';
import Adapter from 'enzyme-adapter-react-16';

configure({ adapter: new Adapter() });
```

```js
// test file
import { shallow, mount, render } from 'enzyme';

const wrapper = shallow(<Foo />);
```

ES5:
<!-- eslint no-var: 0 -->
```js
// setup file
var Enzyme = require('enzyme');
var Adapter = require('enzyme-adapter-react-16');

configure({ adapter: new Adapter() });
```

<!-- eslint no-var: 0 -->
```js
// test file
var enzyme = require('enzyme');

var wrapper = enzyme.shallow(<Foo />);
```