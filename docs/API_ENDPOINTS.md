# ⚡ Convex API Functions

## 📦 Cakes Domain

### `cakes:listAvailable`
* **Type:** 🔵 Query (Fetch)
* **Description:** Get all cakes where inventory is > 0.
* **Args:** * `flavor` (optional string): Filter by category.
* **Returns:** Array of Cake Objects.

### `cakes:updateStock`
* **Type:** 🔴 Mutation (Change)
* **Description:** Manually adjust inventory (Admin only).
* **Args:**
    * `cakeId`: id('cakes')
    * `newCount`: number
* **Returns:** void

---

## 🛒 Orders Domain

### `orders:create`
* **Type:** 🔴 Mutation (Change)
* **Description:** Places a new order and decrements cake inventory.
* **Args:**
    * `cakeId`: id('cakes')
    * `qty`: number
    * `customerDetails`: Object
* **Logic:**
    * Check if stock exists.
    * Throw error if stock is too low.
    * Subtract `qty` from `cakes.inventory`.
    * Insert into `orders` table.

### `orders:dashboardStats`
* **Type:** 🔵 Query (Fetch)
* **Description:** Aggregates total revenue and pending orders.
* **Args:** None.
* **Returns:** Object `{ totalRevenue, pendingCount }`
