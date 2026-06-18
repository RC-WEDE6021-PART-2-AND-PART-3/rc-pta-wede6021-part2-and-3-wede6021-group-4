# Pastimes — Second-Hand Branded Clothing E-Store

**Module:** WEDE6021POE — Part 3  
**Group:** Group 4  
**Students:** Emihle Zifo (ST10452317) | Mzukisi Tekeni (ST10345918)  
**GitHub:** https://github.com/RC-WEDE6021-PART-2-AND-PART-3/rc-pta-wede6021-part2-and-3-wede6021-group-4

---

## What is Pastimes?

Pastimes is a South African second-hand branded clothing e-store built with PHP, MySQL, HTML, CSS, and JavaScript. It supports four user roles: Guest, Buyer, Seller, and Admin — each with different access and features.

---

## Requirements

- XAMPP (Apache + MySQL)
- PHP 8
- A web browser (Chrome or Firefox recommended)

---


### Open the Website
Go to:
```
http://localhost/pastimes3/loadClothingStore.php to update or create the database
```
then go to:

```
http://localhost/pastimes3/index.php
```

---

## Login Details

### Admin
| Field | Value |
|-------|-------|
| URL | http://localhost/pastimes3/Admin/login.php |
| Email | admin@pastimes.co.za |
| Password | Admin@1234 |

### Buyer
| Field | Value |
|-------|-------|
| URL | http://localhost/pastimes3/login.php |
| Username | lindo |
| Password | password |

### Seller
| Field | Value |
|-------|-------|
| URL | http://localhost/pastimes3/login.php |
| Username | testseller |
| Password | Seller@1234 |

> You can also register a new account at `http://localhost/pastimes3/register.php`

---

## Database Structure

Database name: `pastimes_db`

| Table | Purpose |
|-------|---------|
| tblUser | All user accounts (buyers, sellers, admin) |
| tblClothes | All clothing listings |
| tblOrder | All purchase orders |
| tblMessage | Admin communications and broadcasts |

---

## Folder Structure

```
pastimes3/
├── index.php           — Homepage with stats, categories, product grid
├── category.php        — Browse by category
├── sale.php            — Sale items page
├── about.php           — About page
├── register.php        — User registration
├── login.php           — User login
├── logout.php          — Logout
├── cart.php            — Shopping cart and checkout
├── history.php         — Purchase history report
├── sell.php            — Seller item listing form
├── setup.php           — Database setup (run once)
├── DBConn.php          — Database connection
├── loadClothingStore.php — Sample data seeder
├── Admin/
│   ├── login.php       — Admin login
│   ├── dashboard.php   — Admin dashboard
│   ├── sellers.php     — Seller verification
│   ├── listings.php    — Manage clothing listings
│   ├── orders.php      — Manage orders and delivery status
│   ├── comms.php       — Communications and broadcasts
│   └── users.php       — User management
├── includes/
│   ├── header.php      — Site header and navigation
│   └── footer.php      — Site footer
├── css/
│   └── style.css       — Main stylesheet
├── js/
│   └── script.js       — Dropdown, cart popup, image preview
├── images/             — Category banners and site icons
└── uploads/            — Product photos (requires write permissions)
```

---

## Key Features

- Role-based access for Guest, Buyer, Seller, and Admin
- Shopping cart stored in PHP session
- Checkout displays Order Number and Session Reference
- Purchase history report with totals (printable)
- Seller item listing with photo upload and live preview
- Admin can add, edit, and delete users and clothing listings
- Admin can verify, reject, or suspend seller accounts
- Admin can send direct messages or broadcasts to users
- Passwords stored as bcrypt hashes — never plain text
- All database queries use prepared statements to prevent SQL injection
- Paginated product grid (6 items per page)
- Image lazy loading with fallback placeholder
