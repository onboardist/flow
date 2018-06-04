# ui-flow
Define onboarding flows as DAGs

```javascript
import flow from '@onboardist/ui-flow';

// Maybe this?

flow()
.on({ target: '.btn', action: 'click' }
.run(() => coachmark.show('first-step'))
.waitFor('custom-event')
.run(() => coachmark.show('foo'));


```
