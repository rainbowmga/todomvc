# The Temelpa Take-Home Assignment

Please create a private fork of this repo, complete the steps, and once you
are finished, send a link to your repo to us.

# The Assignment

In this repo, you're given an incomplete version of
[TodoMVC](https://todomvc.com/). The assignment is to first finish
it, and then add a few extensions on top of the TodoMVC. What
exists in the repository was taken from a boilerplate implementation,
if you want to radically refactor the code go right ahead.

The following are the objectives you'll need to complete to finish the
take-home.

### Step 1: Finish The Implementation

The repo starts you off with implmentations of the individual components without
implementing global state management. Additionally, there may or may not be
small bugs in the components' implementation. So don't assume that you don't
need to modify the components. Your goal is to finish the TodoMVC implementation,
you may look at existing implementations (of course excluding their source code)
to see what you'll need to do.

As part of the implementations you'll need to retrieve and set the state of the
todo list from the backend api. Take a look at `src/pages/api/index.ts` to see how
the API is constructed.

Once you're done, the implementation should behave exactly the same way as the other
TodoMVC implementations you've seen with the addition that state is persisted through
the backend.

### Step 2: Add Search Functionality

Remove the downward chevron '⌄' with and replace it with a button that toggles
search mode. In search mode, rather the main input field is used to filter
through each todo by title (instead of creating new todos).

The specific matching algorithm is up to you, whether you use prefix matching,
substring matching, or some other way of identifying if a todo and search
term matches.

You should change the visual elements accordingly so that a user who has never
used this app can intuitively understand how to use it. For starters, the input
field shouldn't say "What Needs To Be Done" when empty in search mode.

### Step 3: Add Keyboard Shortcuts

Add the following keyboard shortcuts into the implementation:

1. Users can press `/` to open search mode and begin searching.
2. Users can press `n` to open input mode and begin writing a new todo.
3. Users can press the up arrow, or down arrow key to select and step through the
   currently visible todos in the todolist. Inside a selected todo:

- Users can press space to toggle if the todo is completed or active
- While selected, the todo should not be filtered invisible even if the user
  changes the status, only after deselecting the todo should the filter
  take affect.
- Users can press enter to toggle edit mode and change the todo's title

4. As much as possible, pressing `Esc` should do something intuitive -- I.E. undo, remove.
5. As much as possible, pressing `Enter` should do something intuitive -- I.E. insert, complete.

Like in step 2, you should change the visual elements accordingly so that a novice user
can understand how these features work. Take a look at
[this blog post](https://knock.app/blog/how-to-design-great-keyboard-shortcuts)
if you want some ideas on how to visually show keyboard shortcuts.

### Step 4: Undo/Redo

Add two buttons at the footer to allow the user to undo or redo any change the user has made. `Ctrl + z`
and `Ctrl + Shift + z` should also undo and redo.

## Assumptions

We expect you to work as if this task was a normal project at work. So please write
your code in a way that fits your intuitive notion of operating within best practices.
Additionally, you should at the very least have a different commmit for each individual step,
Ideally, more as you go through process of completing the take-home. Also we like
to see your thought process and fixes as you make changes. So don't be afraid of
committing code that you later edit. No need to squash those commits.

Many parts of the assignment is intentionally ambiguious. If you have a question, definitely
reach out. But for many of these ambiguiuties, we want to see how you independently make
software design decisions.
