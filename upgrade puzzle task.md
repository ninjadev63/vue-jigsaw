# Task

We need an upgrade to an existing jigsaw puzzle game functionallity.
The game is built in JavaScript and is integrated into and called from a Vue component in Nuxt.

We need to add a few new features:

# New features

## Scrolling bar for puzzle pieces

Add a boolean parameter, `useScrollingPieceBar`, to the constructor for the `Puzzle` class. If `false`, the puzzle game should work as now.

If `true`, 
 - The puzzle game should have all the initial pieces in a horisontal band sitting inside and at the bottom of the `forPuzzle` container. 
 - All the pieces should be in a single row and should (if necessary) scoll outside the `forPuzzle` container.
 - The user shall be able to drag the pieces from the scrolling bar and drop them in on the main board.
 - The scrolling bar should work with scrolling gestures and touch.
 - The scrolling bar should not display scrollbars, and should scroll solely by using scrolling gestures and touch.

## Show only edge pieces
At the top of the page in `JigsawPuzzle.vue` a button should flip on and off whether to only show edge pieces in the scrolling bar. The initial state should be that all pieces are shown.

## Show image as background
At the top of the page in `JigsawPuzzle.vue` a button should flip on and off whether to show the completed image (greyed out) as a background on the main board. The initial state should be that the image is not shown.

# Demo

To see an example of how the new features should work, see https://www.loom.com/share/c9297ff7cb9c485ab881c5f73da7b7bc?sid=1570f01f-690a-4333-b392-d9aede423fe4 


# How to see the current code / functionality

The code is in a github repository, https://github.com/mkelk/vue-jigsaw and can be seen there. It can be cloned and run locally to see the current functionality. See the README in the repository for how to do this.


# Delivery

The delivery should be a new branch in the repository containing the changes needed to implement the new features. The code should be able to be run locally using `npm run dev`.

# Proposal

Please provide

- a fixed price offer
- a timeline for delivery
- a short note on why you are well suited to do the job
