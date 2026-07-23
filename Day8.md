# JavaScript Asynchronous Programming

## 1. Synchronous vs Asynchronous

### Synchronous (Sync)

In synchronous programming, code executes **one line at a time**. The next line waits until the current line finishes.

### Example

```javascript
console.log("Start");
console.log("Processing...");
console.log("End");
```

### Output

```
Start
Processing...
End
```

**Characteristics**
- Executes sequentially.
- Each task blocks the next task.
- Simple to understand.
- Slow if a task takes a long time.

---

### Asynchronous (Async)

In asynchronous programming, long-running tasks (API calls, timers, file operations, etc.) execute in the background while the rest of the program continues.

### Example

```javascript
console.log("Start");

setTimeout(() => {
    console.log("Task Completed");
}, 2000);

console.log("End");
```

### Output

```
Start
End
Task Completed
```

**Characteristics**
- Non-blocking execution.
- Improves performance.
- Used for network requests, file reading, timers, etc.

---

# 2. Callback

A **callback** is a function passed as an argument to another function. It is executed after a task is completed.

### Syntax

```javascript
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function bye() {
    console.log("Goodbye!");
}

greet("Rohan", bye);
```

### Output

```
Hello Rohan
Goodbye!
```

### Why use callbacks?

- Handle asynchronous operations.
- Execute code after a task finishes.

### Problem: Callback Hell

When callbacks are nested repeatedly, the code becomes difficult to read and maintain.

```javascript
login(function () {
    getUser(function () {
        getPosts(function () {
            getComments(function () {
                console.log("Done");
            });
        });
    });
});
```

This deeply nested structure is called **Callback Hell**.

---

# 3. Promises

A **Promise** is an object that represents the eventual completion (or failure) of an asynchronous operation.

A Promise has three states:

- Pending
- Fulfilled
- Rejected

### Creating a Promise

```javascript
const promise = new Promise((resolve, reject) => {

    let success = true;

    if (success)
        resolve("Task Completed");
    else
        reject("Task Failed");

});
```

### Consuming a Promise

```javascript
promise
.then(result => {
    console.log(result);
})
.catch(error => {
    console.log(error);
});
```

### Output

```
Task Completed
```

### Advantages

- Avoids callback hell.
- Easier to read.
- Better error handling using `.catch()`.

---

# 4. Async / Await

`async` and `await` are built on top of Promises. They make asynchronous code look like synchronous code.

### Example

```javascript
function fetchData() {

    return new Promise(resolve => {

        setTimeout(() => {
            resolve("Data Received");
        }, 2000);

    });

}

async function displayData() {

    console.log("Loading...");

    const result = await fetchData();

    console.log(result);

}

displayData();
```

### Output

```
Loading...
Data Received
```

### Rules

- `await` can only be used inside an `async` function.
- `await` pauses only the async function, not the entire program.

### Error Handling

```javascript
async function example() {

    try {

        const result = await fetchData();
        console.log(result);

    } catch (error) {

        console.log(error);

    }

}
```

---

# Flow of Asynchronous Programming

```
Synchronous
      │
      ▼
Callbacks
      │
      ▼
Callback Hell ❌
      │
      ▼
Promises
      │
      ▼
Async / Await ✅
```

---

# Comparison

| Feature | Callback | Promise | Async/Await |
|---------|----------|----------|-------------|
| Easy to Read | ❌ | ✅ | ⭐⭐⭐ |
| Error Handling | Difficult | Good | Excellent |
| Callback Hell | Yes | No | No |
| Uses | Older JavaScript | Modern JavaScript | Latest & Recommended |

---

# When to Use

### Use Callbacks
- Simple event handling
- Small asynchronous tasks

### Use Promises
- API requests
- Database operations
- File handling

### Use Async/Await (Recommended)
- Most modern JavaScript applications
- Fetching APIs
- Node.js backend development
- React, Angular, Vue applications

---

# Summary

- **Synchronous:** Executes one statement after another.
- **Asynchronous:** Executes long tasks in the background.
- **Callback:** Function passed into another function and executed later.
- **Promise:** Represents the result of an asynchronous operation.
- **Async/Await:** Simplifies Promise-based code and improves readability.

> **Tip:** In modern JavaScript, prefer **async/await** for most asynchronous code because it is cleaner, easier to understand, and provides better error handling.