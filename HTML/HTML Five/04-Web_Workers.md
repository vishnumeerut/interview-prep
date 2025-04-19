# What are Web Workers in HTML5?

Web Workers are a feature in HTML5 that allows web pages to run JavaScript code in the background, separate from the main UI thread. This enables non-blocking operations, improving performance and user experience by keeping the user interface responsive while performing computationally intensive tasks.

### Key Features of Web Workers:
- **Multithreading:** Web Workers allow JavaScript to run in parallel threads, offloading heavy computations from the main thread.

- **Asynchronous Execution:** Web Workers can execute scripts asynchronously, meaning they do not block the main thread or affect the user interface.

- **Isolation:** Workers operate in isolation, meaning they cannot directly manipulate the DOM. They communicate with the main thread using a messaging system.

### How Web Workers Work:

1. **Main Thread:** The main thread (UI thread) runs the normal JavaScript code.
2. **Web Worker Thread:** A separate thread is created to perform tasks in the background without interrupting the main thread.

### Creating a Web Worker:

#### Example: Creating and Using a Web Worker
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Web Worker Example</title>
</head>
<body>
    <h1>Web Worker Example</h1>
    <button id="startWorker">Start Worker</button>
    <div id="result"></div>

    <script>
        document.getElementById('startWorker').addEventListener('click', function() {
            // Create a new Web Worker
            const worker = new Worker('worker.js');

            // Send data to the worker
            worker.postMessage('Hello Worker');

            // Receive messages from the worker
            worker.onmessage = function(event) {
                document.getElementById('result').innerText = 'Worker says: ' + event.data;
            };
        });
    </script>
</body>
</html>
