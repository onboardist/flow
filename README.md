# ui-flow
Define onboarding flows as DAGs

```javascript
import coachmark from '@onboardist/coachmark';
import callout from '@onboardist/callout';
import hotspot from '@onboardist/hotspot';
import modal from '@onboardist/modal';
import flow from '@onboardist/ui-flow';

// Maybe this?

flow() // Start a new flow
.waitFor('.help-button:click') // On a button click
.waitFor(() => coachmark.show('click-this-button').close) // Show a coachmark and wait for it to be closed
.waitFor(() => hotspot.show('user-name').click) // Show a hotspot and wait for it to be clicked
.waitFor(() => callout.show('user-name').close) // Show a callout and wait for it to be closed



```

# Notes

* [ ] Needs to be usable within a component that has internal flows (callouts, coachmarks) as well as over multiple components working together. As long as it's generic and lightweight enough, that should be fine.
