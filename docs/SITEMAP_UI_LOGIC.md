# 🗺️ App Sitemap & UI Logic

## 🚦 Route Overview
| Route | Platform | Access | Screen Name |
| :--- | :--- | :--- | :--- |
| `/` | Web | Public | Landing Page |
| `/menu` | Web/Mobile | Public | Menu Grid |
| `/admin/orders` | Web | **Protected (Admin)** | Kitchen Dashboard |

---

## 📱 Screen Specifications

### 1. Menu Grid
* **Route:** `/menu`
* **Params:** `?flavor=chocolate` (Optional filter)
* **Data Requirements:** List of available cakes (inventory > 0).

**Key Components:**
* `FilterBar`
    * *Function:* Updates URL params on click.
* `CakeCard`
    * *Function:* Displays image/price. Contains "Add to Cart" button.
* `CartFloatingButton`
    * *Condition:* Only visible if cart has items.

### 2. Kitchen Dashboard
* **Route:** `/admin/orders`
* **Access:** Requires `role === 'admin'`
* **Data Requirements:** Real-time stream of active orders.

**Key Components:**
* `OrderKanbanBoard`
    * *Function:* Drag and drop orders to change status.
* `InventoryAlert`
    * *Condition:* Shows when any cake stock < 5.
