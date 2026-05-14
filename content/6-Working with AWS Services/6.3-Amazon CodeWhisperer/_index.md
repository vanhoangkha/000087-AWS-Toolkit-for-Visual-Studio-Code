---
title: "Amazon CodeWhisperer"
date: 2024-01-01
weight: 3
chapter: false
pre: "<b>6.3</b>"
---

#### Using CodeWhisperer to Write Code Faster

CodeWhisperer can be used as a powerful automatic tool to significantly reduce keystrokes when writing each line or block of code. To use CodeWhisperer this way, simply write code as you normally would. CodeWhisperer will provide automatic suggestions as you type. Accept suggestions when they are helpful and skip them when they are not. In my experience, using CodeWhisperer in this way alone has reduced my keystrokes by 50% or more.

#### Generating Functions Automatically

In programming, creating functions that can automatically generate content from signatures is an important part of the software development process. Skilled programmers often use clear, descriptive names for their functions and parameters. If you adhere to this practice in your own programming, CodeWhisperer will have enough context to implement many functions for you.

When you enter the function signature below, CodeWhisperer will generate the function body for you.

**User Input (JavaScript):**

```javascript
function standardDeviation(numbers)
```

**Result:**

```javascript
function standardDeviation(numbers) {
  let mean = numbers.reduce((a, b) => a + b) / numbers.length;
  let variance =
    numbers.reduce((a, b) => a + Math.pow(b - mean, 2)) / numbers.length;
  return Math.sqrt(variance);
}
```

#### Creating Functions from Comments

Sometimes, a good function signature alone is not enough to convey the desired behavior of a function. In those cases, you can use a detailed code comment as a hint for CodeWhisperer. I recommend using your language's documentation comment syntax when employing this technique.

**User Input (JavaScript):**

```javascript
/**
 * Given a list that contains some numbers and strings, format them into a string
 * in which the numbers are prepended with "#" and the strings are wrapped in
 * double quotes.
 */
```

**Result:**

```javascript
/**
 * Given a list that contains some numbers and strings, format them into a string
 * in which the numbers are prepended with "#" and the strings are wrapped in
 * double quotes.
 */
function formatList(list) {
  return list
    .map((item) => {
      if (typeof item === "number") {
        return `#${item}`;
      } else {
        return `"${item}"`;
      }
    })
    .join(", ");
}
```

That's how you can use CodeWhisperer to automatically generate functions or from descriptive comments in your code.

---

#### Creating Classes

You can create complete or partial classes from a single comment in the code. This comment should describe the main properties and behaviors of the class. Usually, simple descriptions suffice.

User Input (TypeScript):

```typescript
/**
 * A folder with a name, children, and an optional parent folder. A child cannot be added
 * twice.
 */
```

Result:

After writing the above comment, CodeWhisperer provides various suggestions, including the following implementation, along with documentation comments for each method!

```typescript
/**
 * A folder with a name, children, and an optional parent folder. A child cannot be added
 * twice.
 */
export class Folder {
  name: string;
  children: Folder[];
  parent?: Folder;

  constructor(name: string, parent?: Folder) {
    this.name = name;
    this.children = [];
    this.parent = parent;
  }

  /**
   * Add a child to the folder.
   * @param child The child to add.
   * @returns True if the child was added, false if the child is already in the list.
   */
  addChild(child: Folder): boolean {
    if (this.children.includes(child)) {
      return false;
    }
    this.children.push(child);
    child.parent = this;
    return true;
  }

  /**
   * Remove a child from the folder.
   * @param child The child to remove.
   * @returns True if the child was removed, false if it is not in the list.
   */
  removeChild(child: Folder): boolean {
    const index = this.children.indexOf(child);
    if (index === -1) {
      return false;
    }
    this.children.splice(index, 1);
    child.parent = undefined;
    return true;
  }
}
```

You can see that based on the comment, the implementation code is generated, including documentation comments for each method.

---

#### Implementing Algorithms with CodeWhisperer

CodeWhisperer allows you to implement famous algorithms easily. Just specify which algorithm you want to apply to a specific programming problem, and it will fulfill the request.

#### User Input (JavaScript):

```javascript
const actors = [ ... ];

// Sort actors by age using the merge sort algorithm.
```

#### Result:

```javascript
const actors = [ ... ];

// Sort actors by age using the merge sort algorithm.
function mergeSort(arr) {
  if (arr.length < 2) {
    return arr;
  }

  const middle = Math.floor(arr.length / 2);
  const left = arr.slice(0, middle);
  const right = arr.slice(middle);

  return merge(mergeSort(left), mergeSort(right));
}

function merge(left, right) {
  const result = [];

  while (left.length && right.length) {
    if (left[0].age < right[0].age) {
      result.push(left.shift());
    } else {
      result.push(right.shift());
    }
  }

  while (left.length) {
    result.push(left.shift());
  }

  while (right.length) {
    result.push(right.shift());
  }

  return result;
}

console.log(mergeSort(actors));
```

Thank you for using CodeWhisperer to implement this algorithm!

---

#### Enhancing Writing Unit Tests

CodeWhisperer helps speed up the process of writing unit tests. Not only does it have the ability to implement logic for most of the unit tests I request, but it often suggests tests for edge cases that I hadn't even thought of.

When I want CodeWhisperer to implement a unit test, I start by stating the condition I'm testing and the expected result as in the example below.

```javascript
describe("Folder.addChild()", () => {
  it("when adding an existing folder should not add duplicate", () => {
    const folder = new Folder("root");
    const child = new Folder("child");
    folder.addChild(child);
    folder.addChild(child);
    expect(folder.children.length).toBe(1);
  });
});
```

After writing one or two tests, CodeWhisperer has the ability to suggest additional tests without specific requests.

**Tip:** You'll notice that my test descriptions include 1) the function I'm testing, 2) the condition I'm testing, and 3) the result I expect. Following this three-part pattern is a great way to ensure that CodeWhisperer has the necessary context to implement high-quality test logic.

---

#### Generating Sample Data with Code Whisper

One interesting discovery I've had is that Code Whisperer can generate fake data—or actually any code with repeating patterns. For example, given the list below, I only entered the first "user"

 object as an example, and Code Whisperer continued the pattern in a useful way.

#### User Input (JavaScript):

```javascript
const fakeUsers = [
  { name: "User 1", id: "user1" },
JavaScript
```

#### Result:

```javascript
const fakeUsers = [
  { name: "User 1", id: "user1" },
  { name: "User 2", id: "user2" },
  { name: "User 3", id: "user3" },  
  { name: "User 4", id: "user4" },
  { name: "User 5", id: "user5" },
  { name: "User 6", id: "user6" }
]
JavaScript
```

It also works to generate random but believable values like the names seen below.

#### User Input (JavaScript):

```javascript
const fakeUsers = [
  { name: "Sally", id: "user1" },
JavaScript
```

#### Result:

```javascript
const fakeUsers = [
  { name: "Sally", id: "user1" },
  { name: "Bob", id: "user2" },
  { name: "Joe", id: "user3" },
  { name: "Jane", id: "user4" },
  { name: "Jill", id: "user5" },
  { name: "Jack", id: "user6" }
]
```

