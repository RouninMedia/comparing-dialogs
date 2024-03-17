# Comparing Modals
_Using a custom modal vs. introducing a modal via the native HTML `<dialog>` element._

________

See a comparison of a modal built via the native HTML `<dialog>` element against a custom modal:

- <a href="https://rouninmedia.github.io/comparing-modals/comparing-modals.html" target="_blank">Compare native and custom modals</a>

________

In the 2020s HTML evolved its own `<dialog>` element, with native functionality built-in to enable the activation of **modals**.

The `<dialog>` element has been available cross-browser since March 2022 - which means, as of the time of writing, it's been reliably available for two years now.

In Web terms, that means `<dialog>` is now pretty well established.

I like that `<dialog>` has its own `::backdrop` pseudo-element in CSS and that a reasonable amount of thought has been given to the element's API, which allows for limited user-control even in the total absence of JavaScript and for a little more control with JavaScript.

But, at the element's current stage of development, I have two main misgivings with using the native `<dialog>` element to activate modals:

 1. It's not as straightforward as you might anticipate to `transition` or `animate` the arrival or departure of the modal - and it looks like it's not possible to to `transition` or `animate` the fade-in or fade-out of the `::backdrop` pseudo-element at all. The immediate appearance and disappearance of the `::backdrop` feels a bit sudden and jarring.
 2. It's not possible to `click` (or interact in any other way with) the `::backdrop` pseudo-element. Clicking anywhere outside the modal to close it has always felt to me like a natural UX and, because this isn't possible (at present) with the `<dialog>` `::backdrop`, a _Close Button_ must be included within the modal. I have no objecttion to a modal having its own explicit close button, but, to me, for this to be the only way to close the modal feels clunkier.


______

## Sources:

 - https://caniuse.com/dialog
