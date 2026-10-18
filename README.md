

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SILSILA | Flowers That Stay</title>
<meta name="description" content="Discover thoughtfully arranged artificial flowers and beautiful gifts at SILSILA.">
<meta name="theme-color" content="#f8f5ed">

<style>
:root{
  --cream:#f8f5ed;--sage:#a9b9a2;--green:#34483d;
  --pink:#e7b9b0;--ink:#26342c;--white:#fffdf8;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth;scroll-padding-top:90px}
body{margin:0;background:var(--cream);color:var(--ink);font-family:Arial,sans-serif}
body.loading{overflow:hidden}
button,input{font:inherit}
button,a{-webkit-tap-highlight-color:transparent}
a{color:inherit;text-decoration:none}
button{cursor:pointer}
img{max-width:100%}

/* LOADING FLOWER */
#loader{
 position:fixed;inset:0;z-index:9999;background:var(--cream);
 display:grid;place-items:center;
 transition:opacity .45s,visibility .45s;
}
#loader.done{opacity:0;visibility:hidden;pointer-events:none}
.loader-inner{text-align:center}
.flower{
 width:70px;height:70px;margin:auto;position:relative;
 animation:spin 1.3s linear infinite;
}
.petal{
 position:absolute;width:19px;height:31px;
 left:25px;top:4px;border-radius:100% 100% 45% 45%;
 background:var(--sage);transform-origin:10px 31px;
 box-shadow:0 0 13px #a9b9a277;
}
.petal:nth-child(2){transform:rotate(45deg)}
.petal:nth-child(3){transform:rotate(90deg)}
.petal:nth-child(4){transform:rotate(135deg)}
.petal:nth-child(5){transform:rotate(180deg)}
.petal:nth-child(6){transform:rotate(225deg)}
.petal:nth-child(7){transform:rotate(270deg)}
.petal:nth-child(8){transform:rotate(315deg)}
.flower:after{
 content:"";position:absolute;width:12px;height:12px;border-radius:50%;
 background:#d6ad6b;top:29px;left:29px;
 box-shadow:0 0 15px #d6ad6b99;
}
.loader-name{font:25px Georgia,serif;letter-spacing:8px;margin-top:25px}
.loader-caption{font-size:10px;letter-spacing:3px;margin-top:12px;color:#6e786f}
@keyframes spin{to{transform:rotate(360deg)}}

/* HEADER */
.announcement{text-align:center;background:var(--green);color:white;padding:10px;font-size:10px;letter-spacing:2px}
header{position:sticky;top:0;z-index:50;background:#f8f5edf2;backdrop-filter:blur(12px);border-bottom:1px solid #dedfd4}
.nav{max-width:1250px;margin:auto;display:flex;align-items:center;justify-content:space-between;padding:18px 5%;gap:20px}
.brand{font:26px Georgia,serif;letter-spacing:6px}
.navlinks{display:flex;gap:25px;font-size:12px}
.navlinks a:hover{color:#82947c}
.pill{border:1px solid var(--green);border-radius:30px;padding:11px 17px;background:transparent;color:var(--green)}
.menu-toggle{display:none}

/* HERO */
.hero{max-width:1250px;margin:auto;padding:65px 5%;display:grid;grid-template-columns:1fr 1fr;gap:40px;align-items:center}
.eyebrow{text-transform:uppercase;font-size:10px;letter-spacing:3px;color:#6e786f}
h1,h2,h3,p{margin-top:0}
h1{font:clamp(49px,6.5vw,83px)/1.02 Georgia,serif;font-weight:400;margin:22px 0}
h1 em{color:#788e72}
.hero p,.muted{color:#6e786f;line-height:1.9;font-size:14px}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:25px}
.primary{display:inline-block;background:var(--green);color:white;padding:14px 22px;border:1px solid var(--green);border-radius:30px}
.primary:hover{background:#506a57}
.secondary{display:inline-block;border:1px solid var(--green);padding:14px 22px;border-radius:30px}
.hero-art{
 min-height:440px;border-radius:48% 48% 16px 16px;
 background:radial-gradient(circle at 50% 40%,#fff9ed 0,#e7e9da 40%,#e8cfc5 100%);
 display:grid;place-items:center;position:relative;overflow:hidden;
}
.hero-flower{font-size:clamp(130px,20vw,220px);filter:drop-shadow(0 20px 20px #34483d20);animation:float 4s ease-in-out infinite}
.art-label{position:absolute;bottom:23px;right:20px;background:#fffdf0dd;border-radius:30px;padding:13px 17px;font:italic 14px Georgia,serif}
@keyframes float{50%{transform:translateY(-10px) rotate(4deg)}}
.marquee{text-align:center;background:#e7eadf;padding:17px;font:italic 17px Georgia,serif;letter-spacing:1px}

/* PRODUCTS */
.section{max-width:1250px;margin:auto;padding:75px 5%}
.section-title{font:clamp(32px,4vw,48px) Georgia,serif;font-weight:400;margin:12px 0}
.section-head{display:flex;justify-content:space-between;align-items:end;gap:20px;margin-bottom:25px}
.tools{display:flex;gap:12px;margin:25px 0;flex-wrap:wrap}
.tools input,.tools select{background:var(--white);border:1px solid #dedfd4;padding:13px 16px;border-radius:30px;color:var(--ink)}
.tools input{flex:1;min-width:180px}
.filters{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:25px}
.filter{background:transparent;border:1px solid #dedfd4;border-radius:30px;padding:9px 14px;font-size:11px}
.filter.active{background:var(--green);color:white}
.products{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:19px}
.card{background:var(--white);border:1px solid #e9e7de;border-radius:12px;overflow:hidden;transition:transform .25s,box-shadow .25s}
.card:hover{transform:translateY(-5px);box-shadow:0 15px 30px #34483d15}
.photo{aspect-ratio:4/4.3;display:grid;place-items:center;background:linear-gradient(145deg,#f0e8d9,#e0e8db);overflow:hidden}
.photo img{width:100%;height:100%;object-fit:cover}
.emoji{font-size:85px}
.card-body{padding:16px}
.tag{font-size:9px;letter-spacing:2px;text-transform:uppercase;color:#788578}
.card h3{font:21px Georgia,serif;font-weight:400;margin:10px 0}
.description{font-size:12px;line-height:1.7;color:#6e786f;min-height:38px}
.price{font-weight:bold;margin:14px 0}
.add{width:100%;padding:11px;border:1px solid var(--green);border-radius:30px;background:transparent;color:var(--green)}
.add:hover{background:var(--green);color:white}
.empty{grid-column:1/-1;text-align:center;padding:35px;color:#6e786f}

/* STORY */
.story{display:grid;grid-template-columns:1fr 1fr;gap:45px;align-items:center}
.story-art{min-height:300px;display:grid;place-items:center;border-radius:14px;background:linear-gradient(135deg,#dbe4d4,#f1d6cd);font-size:110px}
.story p{font-size:14px;line-height:1.9;color:#6e786f}
.banner{padding:35px;background:#e9ede3;border-radius:18px;display:flex;justify-content:space-between;align-items:center;gap:20px}
.banner h2{font:clamp(28px,4vw,42px) Georgia,serif;font-weight:400;margin:12px 0}
.banner p{max-width:530px;font-size:13px;line-height:1.8;color:#6e786f}
.banner-art{font-size:80px}

/* FOOTER */
footer{background:var(--green);color:var(--cream);padding:35px 5%;display:flex;justify-content:space-between;align-items:center;gap:20px;flex-wrap:wrap}
footer .brand{margin-bottom:9px}
footer small{font-size:11px;opacity:.8;line-height:2}

/* CART */
.overlay{position:fixed;inset:0;background:#17251dcc;z-index:100;display:none;justify-content:flex-end}
.overlay.show{display:flex}
.drawer{width:min(440px,100%);height:100%;overflow:auto;background:var(--cream);padding:24px}
.drawer-head{display:flex;justify-content:space-between;align-items:center}
.drawer-head h2{font:32px Georgia,serif;font-weight:400}
.close{background:transparent;border:0;font-size:28px}
.cart-row{padding:16px 0;border-bottom:1px solid #dedfd4;display:flex;justify-content:space-between;gap:15px}
.qty{display:flex;gap:10px;align-items:center;margin-top:10px}
.qty button{width:28px;height:28px;border:1px solid #dedfd4;background:white;border-radius:50%}
.total{display:flex;justify-content:space-between;padding:20px 0;font-size:19px}
.checkout{width:100%;text-align:center}
.hint{font-size:11px;line-height:1.7;color:#6e786f;margin-top:12px}
.toast{position:fixed;bottom:20px;left:50%;transform:translateX(-50%);background:var(--green);color:white;padding:13px 20px;border-radius:30px;z-index:200;display:none;font-size:13px;max-width:90%;text-align:center}
.toast.show{display:block}

@media(max-width:850px){
 .products{grid-template-columns:repeat(2,minmax(0,1fr))}
 .hero{gap:25px}.hero-art{min-height:340px}
 .navlinks{gap:13px}
}
@media(max-width:580px){
 .nav{padding:14px 5%;gap:10px}
 .brand{font-size:21px;letter-spacing:4px}
 .navlinks{display:none}
 .hero{grid-template-columns:1fr;padding:35px 5%;gap:25px}
 .hero-art{grid-row:1;min-height:280px}
 .hero-copy{text-align:center}
 .hero-copy .actions{justify-content:center}
 .section{padding:52px 5%}
 .section-head{display:block}
 .products{gap:11px}
 .photo{aspect-ratio:4/4.4}
 .emoji{font-size:65px}
 .card-body{padding:11px}
 .card h3{font-size:17px}
 .description{font-size:11px}
 .story{grid-template-columns:1fr;gap:25px}
 .story-art{min-height:220px}
 .banner{padding:25px;align-items:flex-start}
 .banner-art{font-size:48px}
}
@media(prefers-reduced-motion:reduce){
 *,*::before,*::after{animation-duration:.01ms!important;scroll-behavior:auto!important}
}
</style>
</head>

<body class="loading">

<div id="loader" aria-label="Loading SILSILA">
 <div class="loader-inner">
  <div class="flower" aria-hidden="true">
   <span class="petal"></span><span class="petal"></span>
   <span class="petal"></span><span class="petal"></span>
   <span class="petal"></span><span class="petal"></span>
   <span class="petal"></span><span class="petal"></span>
  </div>
  <div class="loader-name">SILSILA</div>
  <div class="loader-caption">A LITTLE BEAUTY IS BLOOMING</div>
 </div>
</div>

<div class="announcement">A LITTLE JOY, DELIVERED IN BLOOM ✿</div>

<header>
 <nav class="nav">
  <a class="brand" href="#home">SILSILA</a>
  <div class="navlinks">
   <a href="#shop">Shop</a><a href="#story">Our Story</a><a href="#behind">Behind the Blooms</a>
  </div>
  <button class="pill" onclick="openCart()">Bag (<span id="bagcount">0</span>)</button>
 </nav>
</header>

<main id="home">
 <section class="hero">
  <div class="hero-copy">
   <div class="eyebrow">Flowers for your everyday spaces</div>
   <h1>Let beauty<br>stay a little<br><em>longer.</em></h1>
   <p>Thoughtfully chosen artificial blooms for corners that need a little softness, tables that bring everyone together, and gifts that keep on giving.</p>
   <div class="actions">
    <a class="primary" href="#shop">Explore the collection ↗</a>
    <a class="secondary" href="#story">Our story</a>
   </div>
  </div>
  <div class="hero-art">
   <div class="hero-flower">💐</div>
   <div class="art-label">Made to make you smile</div>
  </div>
 </section>

 <div class="marquee">Soft petals · thoughtful details · little moments of wonder</div>

 <section class="section" id="shop">
  <div class="section-head">
   <div><div class="eyebrow">The collection</div><h2 class="section-title">Find your kind of bloom</h2><p class="muted">Small details, lovely spaces. Pick a favourite.</p></div>
   <button class="pill" onclick="openCart()">View bag ↗</button>
  </div>
  <div class="tools">
   <input id="search" type="search" placeholder="Search flowers..." aria-label="Search products">
   <select id="sort" aria-label="Sort products">
    <option value="featured">Sort: Featured</option>
    <option value="low">Price: low to high</option>
    <option value="high">Price: high to low</option>
    <option value="az">Name: A to Z</option>
   </select>
  </div>
  <div class="filters" id="filters"></div>
  <div class="products" id="products"></div>
 </section>

 <section class="section" id="story">
  <div class="story">
   <div class="story-art">🌷🌿</div>
   <div>
    <div class="eyebrow">A little about us</div>
    <h2 class="section-title">Some things deserve to stay.</h2>
    <p>SILSILA is about the little connections that make a place feel like yours — a bloom on your desk, colour on a quiet shelf, or a thoughtful gift for someone special.</p>
    <p>Every piece is chosen with care. Make it yours, style it your way, and let it become part of your everyday story.</p>
    <a href="#shop" class="secondary">Find your bloom</a>
   </div>
  </div>
 </section>

 <section class="section" id="behind">
  <div class="banner">
   <div>
    <div class="eyebrow">Behind the blooms</div>
    <h2>Come along for the making.</h2>
    <p>Discover new arrivals, styling ideas and little peeks behind SILSILA. Follow our journey on Instagram.</p>
    <a id="instaLink" class="primary" href="https://instagram.com/" target="_blank" rel="noopener noreferrer">Follow our journey ↗</a>
   </div>
   <div class="banner-art">🌼</div>
  </div>
 </section>
</main>

<footer>
 <div><div class="brand">SILSILA</div><small>Flowers that stay, moments that bloom.</small></div>
 <div><a href="#shop">Shop</a> · <a href="#story">Our story</a><br><small>© <span id="year"></span> SILSILA</small></div>
</footer>

<div class="overlay" id="cartOverlay" onclick="if(event.target===this)closeCart()">
 <aside class="drawer" role="dialog" aria-modal="true" aria-label="Shopping bag">
  <div class="drawer-head"><h2>Your bag</h2><button class="close" onclick="closeCart()" aria-label="Close bag">×</button></div>
  <p class="hint">A few lovely things, all in one place.</p>
  <div id="cartitems"></div>
  <div class="total"><span>Total</span><strong id="carttotal">₹0</strong></div>
  <label class="hint">Your name (optional)
   <input id="buyername" placeholder="Name" style="display:block;width:100%;margin:7px 0 14px;padding:12px;border:1px solid #dedfd4;border-radius:10px;background:#fffdf8">
  </label>
  <label class="hint">Delivery area / notes (optional)
   <input id="buyernote" placeholder="Your area and any notes" style="display:block;width:100%;margin:7px 0 14px;padding:12px;border:1px solid #dedfd4;border-radius:10px;background:#fffdf8">
  </label>
  <button class="primary checkout" onclick="checkout()">Order via WhatsApp ↗</button>
  <p class="hint">WhatsApp opens with your order details. Review and send the message there.</p>
 </aside>
</div>
<div class="toast" id="toast" role="status" aria-live="polite"></div>

<script>
"use strict";

/* EDIT THIS NUMBER: country code + number, digits only.
   Example India: 919876543210 */
const WHATSAPP_NUMBER = "918016845559";

const seed = [
 {id:1,name:"Blush Garden Rose",size:"Approx. 30 cm stem",price:199,cat:"Everyday blooms",emoji:"🌹",desc:"Soft blush petals for a gentle touch."},
 {id:2,name:"Wildflower Meadow",size:"Small bunch · approx. 20 cm",price:249,cat:"Bundles & gifts",emoji:"💐",desc:"A cheerful mix for your favourite corner."},
 {id:3,name:"Ivory Lily Stem",size:"Approx. 45 cm stem",price:179,cat:"Statement stems",emoji:"🌼",desc:"Clean, calm and effortlessly elegant."},
 {id:4,name:"Peach Peony",size:"Approx. 25 cm bloom",price:229,cat:"Everyday blooms",emoji:"🌸",desc:"Full petals with a warm peach tone."},
 {id:5,name:"Eucalyptus Sprig",size:"Approx. 35 cm stem",price:129,cat:"Statement stems",emoji:"🌿",desc:"A little green to soften your space."},
 {id:6,name:"Spring Gift Bundle",size:"Set of 3 stems",price:399,cat:"Bundles & gifts",emoji:"🪻",desc:"A ready-to-gift trio of spring-inspired blooms."},
 {id:7,name:"Sunny Daisy Stem",size:"Approx. 28 cm stem",price:149,cat:"Seasonal",emoji:"🌼",desc:"A small pop of happy sunshine."},
 {id:8,name:"Lavender Dream",size:"Approx. 32 cm stem",price:169,cat:"Seasonal",emoji:"🪻",desc:"Gentle lavender tones for a peaceful nook."}
];

let products = seed.map(p=>({...p}));
let cart = {};
let category = "All";
let toastTimer;

const $ = id => document.getElementById(id);
const money = n => "₹" + Number(n).toLocaleString("en-IN");
const safe = s => String(s ?? "").replace(/[&<>"']/g,c=>({
 "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"
}[c]));

function showToast(message){
 const t=$("toast");
 t.textContent=message;
 t.classList.add("show");
 clearTimeout(toastTimer);
 toastTimer=setTimeout(()=>t.classList.remove("show"),2500);
}

function renderFilters(){
 const cats=["All",...new Set(products.map(p=>p.cat))];
 if(!cats.includes(category))category="All";
 $("filters").innerHTML=cats.map(c=>
  `<button class="filter ${category===c?"active":""}" data-category="${safe(c)}">${safe(c)}</button>`
 ).join("");
}

function renderProducts(){
 renderFilters();
 const query=$("search").value.trim().toLowerCase();
 let list=products.filter(p=>
  (category==="All"||p.cat===category) &&
  (p.name+" "+p.cat+" "+p.desc).toLowerCase().includes(query)
 );
 const sort=$("sort").value;
 if(sort==="low")list.sort((a,b)=>a.price-b.price);
 if(sort==="high")list.sort((a,b)=>b.price-a.price);
 if(sort==="az")list.sort((a,b)=>a.name.localeCompare(b.name));

 $("products").innerHTML=list.length?list.map(p=>`
  <article class="card">
   <div class="photo"><span class="emoji" aria-hidden="true">${safe(p.emoji)}</span></div>
   <div class="card-body">
    <div class="tag">${safe(p.cat)}</div>
    <h3>${safe(p.name)}</h3>
    <div class="description">${safe(p.size)}<br>${safe(p.desc)}</div>
    <div class="price">${money(p.price)}</div>
    <button class="add" data-add="${p.id}">＋ Add to bag</button>
   </div>
  </article>`).join(""):'<div class="empty">No blooms found. Try another search. 🌷</div>';
}

function addToCart(id){
 cart[id]=(cart[id]||0)+1;
 renderCart();
 showToast("Added to your bag ✿");
}
function changeQty(id,delta){
 cart[id]=(cart[id]||0)+delta;
 if(cart[id]<=0)delete cart[id];
 renderCart();
}
function renderCart(){
 const count=Object.values(cart).reduce((a,b)=>a+b,0);
 let total=0;
 $("bagcount").textContent=count;
 const rows=Object.entries(cart).filter(([,q])=>q>0).map(([id,q])=>{
  const p=products.find(x=>x.id===Number(id));
  if(!p)return "";
  total+=p.price*q;
  return `<div class="cart-row">
   <div><strong>${safe(p.name)}</strong><div class="hint">${money(p.price)} each</div>
   <div class="qty"><button data-qty="${id}" data-delta="-1" aria-label="Remove one">−</button><span>${q}</span><button data-qty="${id}" data-delta="1" aria-label="Add one">+</button></div></div>
   <strong>${money(p.price*q)}</strong>
  </div>`;
 }).join("");
 $("cartitems").innerHTML=rows||'<p class="empty">Your bag is waiting for its first bloom 🌷</p>';
 $("carttotal").textContent=money(total);
}
function openCart(){
 $("cartOverlay").classList.add("show");
 document.body.style.overflow="hidden";
 renderCart();
}
function closeCart(){
 $("cartOverlay").classList.remove("show");
 document.body.style.overflow="";
}
function checkout(){
 const items=Object.entries(cart).filter(([,q])=>q>0).map(([id,q])=>{
  const p=products.find(x=>x.id===Number(id));
  return p?{p,q}:null;
 }).filter(Boolean);
 if(!items.length){showToast("Add a bloom to your bag first");return}
 if(!/^\d{10,15}$/.test(WHATSAPP_NUMBER)){
  showToast("Please set a valid WhatsApp number in the code.");
  return;
 }
 const total=items.reduce((sum,x)=>sum+x.p.price*x.q,0);
 const lines=items.map(x=>`${x.p.name} | Qty ${x.q} | ${money(x.p.price*x.q)}`);
 const msg=`Hello SILSILA! I'd like to place an order:\n\n${lines.join("\n")}\n\nTotal: ${money(total)}\nName: ${$("buyername").value.trim()||"Not provided"}\nDelivery area / notes: ${$("buyernote").value.trim()||"Not provided"}\n\nPlease confirm availability and delivery details.`;
 window.open("https://wa.me/"+WHATSAPP_NUMBER+"?text="+encodeURIComponent(msg),"_blank","noopener,noreferrer");
}

/* Product buttons and filters */
$("filters").addEventListener("click",e=>{
 const b=e.target.closest("[data-category]");
 if(!b)return;
 category=b.dataset.category;
 renderProducts();
});
$("products").addEventListener("click",e=>{
 const b=e.target.closest("[data-add]");
 if(b)addToCart(Number(b.dataset.add));
});
$("cartitems").addEventListener("click",e=>{
 const b=e.target.closest("[data-qty]");
 if(b)changeQty(Number(b.dataset.qty),Number(b.dataset.delta));
});
$("search").addEventListener("input",renderProducts);
$("sort").addEventListener("change",renderProducts);
$("year").textContent=new Date().getFullYear();

/* Change this to your actual Instagram profile */
const INSTAGRAM_URL="https://instagram.com/";
$("instaLink").href=INSTAGRAM_URL;

/* Show the site after a short animated intro */
function hideLoader(){
 $("loader").classList.add("done");
 document.body.classList.remove("loading");
}
window.addEventListener("load",()=>setTimeout(hideLoader,1000));
setTimeout(hideLoader,2500);

/* Escape closes the bag */
document.addEventListener("keydown",e=>{
 if(e.key==="Escape")closeCart();
});

renderProducts();
renderCart();
</script>
</body>
</html>
