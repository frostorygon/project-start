# 🗄️ Data Schema (Models)

### `cakes` Table
| Field | Type | Description |
| :--- | :--- | :--- |
| `name` | string | Name of the cake (e.g., "Chocolate Lava") |
| `price` | number | Price in cents (e.g., 2500 = $25.00) |
| `inventory` | number | Current stock available |
| `flavor` | string | Primary flavor category |
| `isGlutenFree`| boolean | **Optional.** Defaults to false. |

### `orders` Table
| Field | Type | Description |
| :--- | :--- | :--- |
| `cakeId` | id('cakes') | **Relation.** Links to `cakes` table. |
| `customerName` | string | Name of the person ordering |
| `qty` | number | Number of cakes ordered |
| `status` | string | Union: "pending" \| "baking" \| "ready" |
