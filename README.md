---

# 🚀 **About This Package**

This package provides a set of lightweight, type-safe, and developer-friendly React hooks that simplify making API requests in your frontend applications. It removes the repeated boilerplate developers write **every single time** they call an API:

* Fetching
* Error handling
* Status checking
* Zod validation
* Managing loading, success, and failure states

Instead of writing the same conditional checks across components, the package delivers one consistent, predictable API response format.

---

# 🌟 **Why Developers Need This**

### 🧱 1. Eliminates repeated boilerplate

Normally, developers must check:

```ts
if (response.ok) { ... }
else if (status === 404) { ... }
else if (status === 500) { ... }
```

And then parse JSON, validate shape, handle errors, track loading state…

Your hook does *all* of this in one place.

---

### 🛡️ 2. One unified API response structure

Every hook (`useGet`, `usePost`, `usePut`, `usePatch`, `useDelete`) returns:

* `data`
* `isValid`
* `status`
* `loading`
* `message`
* `error`

No matter which HTTP method is used, the developer always receives the **same stable structure**.

This makes API handling extremely predictable.

---

### 🎯 3. Built-in Zod validation

API responses are often inconsistent.
Developers don’t always trust backend data.

Your package lets them provide a Zod schema:

```ts
useGet("/api/user", userSchema)
```

And ensures:

* The response matches expected shape
* Invalid data is caught early
* TypeScript automatically infers the validated type

This is a huge upgrade in safety and reliability.

---

### ⚡ 4. Method-specific hooks for simplicity

Developers don’t need to configure anything:

```ts
useGet("/api/users")
usePost("/api/users", body)
usePut("/api/users/5", body)
useDelete("/api/users/5")
```

Each one internally uses the same core logic, so it is consistent, reliable, and easy to understand.

---

### 📦 5. Zero configuration needed

Just install the package and call the hooks.
No provider, no setup, no context — nothing.

Perfect for:

* React
* Next.js
* Vite
* CRA
* Any React environment

---

### 🧩 6. Centralized, maintainable logic

Instead of spreading error handlers and status checks across dozens of components, you keep everything in one place:

✔ One main engine (`useApiGuard`)
✔ Each method wrapper calls the same logic
✔ Easy to update, scale, and maintain

This improves code consistency across the entire team.

---

### 🧪 7. Clean cancellation & request safety

Your core hook:

* Uses `AbortController`
* Prevents memory leaks
* Avoids state updates on unmounted components

This is the correct, modern way to handle fetch in React.

---

# ❤️ **In Short: What This Package Gives Developers**

* Much cleaner code
* Less repetitive API logic
* Strong runtime validation
* Strong TypeScript inference
* Unified error structure
* Faster development
* Fewer bugs
* Better DX (Developer Experience)

This package essentially becomes a **tiny, elegant, developer-friendly abstraction layer** on top of fetch — perfect for modern React apps.

---
