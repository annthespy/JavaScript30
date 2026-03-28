# JavaScript30 Notes

## Day 1 - Drum Kit

### Key Concepts

**Event Listeners**
- `window.addEventListener('keydown', callback)` - listen for keyboard events
- `e.keyCode` - get the numeric code of the pressed key (e.g., 65 = "A")

**DOM Selection with Attribute Selectors**
- `document.querySelector(`audio[data-key="${e.keyCode}"]`)` - select element by data attribute
- `querySelectorAll('.key')` - select multiple elements

**Audio API**
- `audio.play()` - play the sound
- `audio.currentTime = 0` - reset playback position (allows rapid re-triggering)

**CSS Class Manipulation**
- `element.classList.add('playing')` - add a class
- `element.classList.remove('playing')` - remove a class

**Transition Events**
- `transitionend` event fires when a CSS transition completes
- `e.propertyName` - which CSS property finished transitioning (e.g., 'transform')
- Multiple properties transitioning = multiple `transitionend` events

**Event Delegation**
- Attach listener to parent instead of each child
- Events bubble up from child to parent
- `e.target` still refers to the actual element that triggered the event
- Benefits: fewer listeners, works with dynamically added elements

**Guard Clauses**
- `if (!element) return;` - early exit pattern to handle null/missing elements
