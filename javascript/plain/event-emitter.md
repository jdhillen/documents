[Event Emitter](https://dev.to/tunaxor/the-beautiful-thing-called-eventemitter-23ei)
===

[Source Code for Event Emitter](https://gist.github.com/mudge/5830382)

```javascript
const EventEmitter = require('events');

const ee = new EventEmitter();

ee.on('dog', () => console.log('dog'));
ee.on('dog', (name, color, race) => console.log('dog', name, color, race));

ee.emit('dog');
// dog
// dog undefined undefined undefined

ee.emit('dog', 'Fig', 'brown', 'chihuahua');
// dog
// dog Fig brown chihuahua
```
