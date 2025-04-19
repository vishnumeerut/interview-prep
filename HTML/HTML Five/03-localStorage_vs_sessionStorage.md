# What is the Difference Between `localStorage` and `sessionStorage`?

Both **`localStorage`** and **`sessionStorage`** are web storage APIs that allow storing data on the client-side (in the browser). However, they have different lifetimes and use cases.

### Key Differences:

1. **Persistence:**
   - **`localStorage`:** Data stored in `localStorage` persists even after the browser is closed or the device is restarted. It remains available until it is explicitly deleted.
   - **`sessionStorage`:** Data stored in `sessionStorage` is temporary and only available for the duration of the page session. It is cleared when the browser tab or window is closed.

2. **Scope:**
   - **`localStorage`:** Data is accessible across different tabs or windows in the same origin (domain). It is shared between all tabs/windows of the same site.
   - **`sessionStorage`:** Data is limited to the tab or window that created it. Other tabs or windows from the same origin cannot access the sessionStorage data.

3. **Storage Size:**
   - Both `localStorage` and `sessionStorage` have a storage limit, but `localStorage` typically allows larger amounts of data (around 5MB per domain).
   - `sessionStorage` also has a similar size limit but is generally considered smaller than `localStorage` because it's meant for temporary data.

4. **Use Cases:**
   - **`localStorage`:** Ideal for storing data that should persist between sessions, such as user preferences, themes, or authentication tokens.
   - **`sessionStorage`:** Suitable for storing temporary data that should not persist once the user leaves the page, such as session-specific information like a shopping cart.

### Example:

#### Using `localStorage`:
```javascript
// Storing data
localStorage.setItem('username', 'JohnDoe');

// Retrieving data
var username = localStorage.getItem('username');
console.log(username);  // Output: JohnDoe

// Removing data
localStorage.removeItem('username');
```
#### Using `sessionStorage`:
```javascript
// Storing data
sessionStorage.setItem('sessionId', 'abc123');

// Retrieving data
var sessionId = sessionStorage.getItem('sessionId');
console.log(sessionId);  // Output: abc123

// Removing data
sessionStorage.removeItem('sessionId');

```
