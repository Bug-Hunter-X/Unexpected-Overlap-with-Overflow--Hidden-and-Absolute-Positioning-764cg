# CSS Layout Bug: Unexpected Overlap

This repository demonstrates a subtle CSS layout bug involving unexpected element overlap even when using `overflow: hidden` on a parent container.  The issue arises from the interaction of `position: absolute` and `overflow: hidden` in certain scenarios.

## Bug Description

The provided CSS code shows a `div` with class `container` that has `overflow: hidden`. A child `div` with class `content` is absolutely positioned within the `container`. Despite setting `overflow: hidden` on the parent, the child element (`content`) can unexpectedly overlap with elements outside of the container under certain conditions, particularly in some older or less-conformant browsers.

## Bug Reproduction

1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Observe that the `.content` div partially overlaps the border of the `container` div, contradicting the intended behavior of `overflow: hidden`.

## Solution

The solution involves adding `z-index` property to solve this conflict by controlling stack order.  See `bugSolution.css` for the fix.