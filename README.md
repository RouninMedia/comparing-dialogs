# Comparing Modals
_Using a custom modal vs. introducing a modal via the native HTML `<dialog>` element._

________

See a comparison of a modal built via the native HTML `<dialog>` element against a custom modal:

- <a href="https://rouninmedia.github.io/comparing-modals/comparing-modals.html" target="_blank">Compare native and custom modals</a>

________
## Analysis:

In the 2020s HTML evolved its own `<dialog>` element, with native functionality built-in to enable the activation of **modals**.

The `<dialog>` element has been available cross-browser since March 2022 - which means, as of the time of writing, it's been reliably available for two years now.

In Web terms, that means `<dialog>` is now pretty well established.

I like that `<dialog>` has its own `::backdrop` pseudo-element in CSS and that a reasonable amount of thought has been given to the element's API, which allows for limited user-control even in the total absence of JavaScript and for a little more control with JavaScript.

But, at the element's current stage of development, I have two main misgivings with activating modals via the native `<dialog>` element and its associated `::backdrop` pseudo-element:

 1. The immediate appearance and disappearance of either or both of the `<dialog>` and the `::backdrop` feels a bit sudden and jarring. It's not as straightforward as you might anticipate to `transition` or `animate` the arrival and departure of the modal - albeit the arrival is easier to animate than the departure. Furthermore, after some initial experimentation, it looks like it might not possible to `transition` or `animate` the fade-in or fade-out of the `::backdrop` pseudo-element at all.
    
 2. More seriously, it's not possible to `click` (or interact in any other way with) the `::backdrop` pseudo-element. Clicking anywhere outside the modal to close it has always felt to me like a natural UX and, because this isn't possible (at present) with the `<dialog>` `::backdrop`, a _Close Button_ must be included within the modal. I have no objecttion to a modal having its own explicit close button, but, to me, for this to be the only way to close the modal definitely feels clunkier.

______

## Conclusions:

As much as I would very much like to use the `<dialog>` element for all my modals, I will, for now, be sticking with a custom modal which allows for:

 - animated fade-in and fade-out of the backdrop
 - click-interaction on the backdrop to close the modal
 - straightforward animated departure of the modal

________

See a comparison of a modal built via the native HTML `<dialog>` element against a custom modal:

- <a href="https://rouninmedia.github.io/comparing-modals/comparing-modals.html" target="_blank">Compare native and custom modals</a>

______

## Sources:

 - https://caniuse.com/dialog
