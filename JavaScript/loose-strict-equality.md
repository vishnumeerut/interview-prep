### 🔄 Difference between `==` and `===` in JavaScript

| Operator | Name            | Compares            | Type Coercion | Example        | Result  |
|----------|-----------------|---------------------|----------------|----------------|---------|
| `==`     | Loose Equality  | Values              | ✅ Yes         | `'5' == 5`     | `true`  |
| `===`    | Strict Equality | Values + Types      | ❌ No          | `'5' === 5`    | `false` |

---

### ✅ Summary:
- `==` → Converts operands to same type before comparing.
- `===` → Compares both **value and type** without conversion.
- **Recommended:** Always use `===` to avoid unexpected bugs.

