# H Crafts — Website (Frontend + Backend)

## যা আছে
- `public/` — ফ্রন্টএন্ড: index.html, admin.html, CSS, JS, প্রোডাক্ট ছবি, লোগো
- `server/` — ব্যাকএন্ড: Node.js + Express সার্ভার
  - `server/data/products.json` — প্রোডাক্ট ক্যাটালগ (এডিট করে নতুন প্রোডাক্ট যোগ করা যাবে)
  - `server/data/orders.json` — ওয়েবসাইট থেকে আসা অর্ডার রিকোয়েস্ট জমা হয় এখানে

## কীভাবে নিজের কম্পিউটারে চালাবেন
```
cd server
npm install
npm start
```
এরপর ব্রাউজারে যান: `http://localhost:3000`

অ্যাডমিন প্যানেল (অর্ডার দেখার জন্য): `http://localhost:3000/admin.html`
ডিফল্ট admin key: `hcrafts123` — এটা `server/index.js` ফাইলে বা `ADMIN_KEY` এনভায়রনমেন্ট ভ্যারিয়েবল দিয়ে বদলে নিন।

## কীভাবে প্রোডাক্ট যোগ/এডিট করবেন
`server/data/products.json` ফাইলে একটা নতুন অবজেক্ট যোগ করুন (id, name, category, price, image, description, badge)। ছবি রাখুন `public/assets/images/` ফোল্ডারে।

## লাইভ হোস্ট করার উপায়
এটা একটা সাধারণ Node.js + Express অ্যাপ, তাই যেকোনো Node hosting-এ ডিপ্লয় করা যাবে:
- **Render.com** / **Railway.app** — ফ্রি টিয়ারে শুরু করা যায়, GitHub রিপো কানেক্ট করলেই অটো-ডিপ্লয় হয়
- **A2 Hosting / Hostinger VPS** (বাংলাদেশে জনপ্রিয়) — Node.js সাপোর্ট থাকলে চলবে
- ডোমেইন থাকলে সেটা সার্ভারের IP-তে পয়েন্ট করে দিলেই হবে

ডিপ্লয়ের সময় `npm install` আর `npm start` রান করতে হবে (start command: `node index.js`, port env var `PORT`)।

## গুরুত্বপূর্ণ নোট
- `orders.json`-এ অর্ডার ফাইলে জমা হয়, তাই এটা ডেটাবেজ নয় — বড় স্কেলে গেলে MongoDB/PostgreSQL-এ সরানো ভালো। ছোট ব্যবসার জন্য এটা যথেষ্ট।
- WhatsApp বাটন ও লিংক ইতিমধ্যে আপনার নম্বর (+880 1972-403066) দিয়ে সেট করা আছে।
- Facebook পেজের লিংক এখনো placeholder (`facebook.com`) — আসল পেজ লিংক দিলে `public/index.html`-এ বসিয়ে দেওয়া যাবে।
