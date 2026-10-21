[index.html](https://github.com/user-attachments/files/33790902/index.html)
# boerne-launch-pad
This is a website for CTE students who would like to start a business in Texas
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Boerne ISD Launch Pad</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,600;12..96,800&family=Atkinson+Hyperlegible:ital,wght@0,400;0,700;1,400&family=JetBrains+Mono:wght@500&display=swap">
<style>
[hidden]{display:none!important}
html{color-scheme:light}
body{margin:0}
img{max-width:100%}
/* Layout: a launch checklist. Left = where you are on the road; right = the step. Plain words first, official words second. */
:root{
  --paper:#F3F6F4; --surface:#FFFFFF; --ink:#13241F; --muted:#4F625C; --line:#D5DFDA;
  --pine:#1F5A4A; --pine-soft:#E2EEE9; --marigold:#E3A51B; --marigold-soft:#FBF0D3; --blue:#2E4A9E; --blue-soft:#E6EBF8;
  --warn:#9A3B12; --warn-soft:#FBE7DD;
  --display:"Bricolage Grotesque", "Segoe UI", system-ui, sans-serif;
  --body:"Atkinson Hyperlegible", "Segoe UI", system-ui, sans-serif;
  --mono:"JetBrains Mono", ui-monospace, Menlo, Consolas, monospace;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --paper:#0F1916; --surface:#16231F; --ink:#E6EFEB; --muted:#9DB2AA; --line:#2A3B36;
  --pine:#7FC7AE; --pine-soft:#1C332C; --marigold:#F2C04E; --marigold-soft:#3A3016; --blue:#9FB4F2; --blue-soft:#1E2742;
  --warn:#F2A07A; --warn-soft:#3A2218; color-scheme:dark}}
:root[data-theme="dark"]{
  --paper:#0F1916; --surface:#16231F; --ink:#E6EFEB; --muted:#9DB2AA; --line:#2A3B36;
  --pine:#7FC7AE; --pine-soft:#1C332C; --marigold:#F2C04E; --marigold-soft:#3A3016; --blue:#9FB4F2; --blue-soft:#1E2742;
  --warn:#F2A07A; --warn-soft:#3A2218; color-scheme:dark}

*{box-sizing:border-box}
body{background:var(--paper);color:var(--ink);font-family:var(--body);font-size:17px;line-height:1.6;
  padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px))}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:10;background:var(--paper)}
.wrap{max-width:1080px;margin:0 auto}
h1,h2,h3{font-family:var(--display);line-height:1.15;text-wrap:balance;margin:0}
h1{font-size:clamp(2.1rem,5vw,3.4rem);font-weight:800;letter-spacing:-.02em}
h2{font-size:clamp(1.6rem,3.2vw,2.2rem);font-weight:800;letter-spacing:-.01em}
h3{font-size:1.2rem;font-weight:600}
p{margin:0}
a{color:var(--blue);text-underline-offset:3px}
a:focus-visible,button:focus-visible,input:focus-visible,select:focus-visible{outline:3px solid var(--marigold);outline-offset:2px;border-radius:4px}
.label{font-family:var(--mono);font-size:.74rem;letter-spacing:.08em;text-transform:uppercase;color:var(--muted)}
.prose{max-width:66ch;display:grid;gap:.9rem}

/* Header + nav */
header.top{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;background:var(--paper);border-bottom:1px solid var(--line)}
.bar{display:flex;align-items:center;gap:1rem;padding-block:.7rem;flex-wrap:wrap}
.brand{font-family:var(--display);font-weight:800;font-size:1.15rem;display:flex;align-items:center;gap:.5rem;color:var(--ink);text-decoration:none}
.brand svg{flex:none}
nav.tabs{display:flex;gap:.25rem;overflow-x:auto;scrollbar-width:none;margin-left:auto;max-width:100%}
nav.tabs::-webkit-scrollbar{display:none}
nav.tabs a{white-space:nowrap;padding:.4rem .75rem;border-radius:999px;color:var(--ink);text-decoration:none;font-size:.95rem}
nav.tabs a:hover{background:var(--pine-soft)}
nav.tabs a[aria-current="page"]{background:var(--pine);color:var(--paper);font-weight:700}

main{padding-block:2rem 4rem}
section.view{display:grid;gap:2rem}
.draft{display:flex;gap:.6rem;align-items:flex-start;background:var(--marigold-soft);border:1px dashed var(--marigold);padding:.7rem 1rem;border-radius:8px;font-size:.92rem}
.draft b{font-family:var(--mono);font-size:.75rem;letter-spacing:.06em;text-transform:uppercase}

/* Home */
.hero{display:grid;grid-template-columns:1.25fr 1fr;gap:2.5rem;align-items:center;padding-block:1rem}
.hero p.lede{font-size:1.2rem;color:var(--muted);max-width:44ch;margin-top:1rem}
.hero .cta{display:flex;gap:.75rem;flex-wrap:wrap;margin-top:1.5rem}
.btn{display:inline-flex;align-items:center;gap:.4rem;padding:.7rem 1.15rem;border-radius:10px;font-weight:700;text-decoration:none;border:2px solid var(--pine);font-family:var(--body);font-size:1rem;cursor:pointer}
.btn.primary{background:var(--pine);color:var(--paper)}
.btn.ghost{color:var(--pine);background:transparent}
.ladder{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:1.25rem;display:grid;gap:.15rem}
.ladder a{display:grid;grid-template-columns:2.2rem 1fr;gap:.6rem;align-items:center;padding:.45rem .4rem;border-radius:8px;color:var(--ink);text-decoration:none}
.ladder a:hover{background:var(--pine-soft)}
.ladder .n{font-family:var(--mono);font-size:.85rem;width:2rem;height:2rem;border-radius:50%;display:grid;place-items:center;border:2px solid var(--pine);color:var(--pine)}
.ladder a.done .n{background:var(--pine);color:var(--paper)}
.three{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem}
.tile{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:1.2rem;display:grid;gap:.5rem;align-content:start}
.tile h3{font-size:1.1rem}
.tile p{color:var(--muted);font-size:.97rem}
.big-def{border-left:4px solid var(--marigold);padding:.2rem 0 .2rem 1.1rem;font-size:1.15rem;max-width:60ch}

/* Roadmap */
.road{display:grid;grid-template-columns:240px 1fr;gap:2rem;align-items:start}
.road-nav{position:sticky;top:calc(env(safe-area-inset-top,0px) + 76px);display:grid;gap:.15rem}
.road-nav button{all:unset;cursor:pointer;display:grid;grid-template-columns:1.9rem 1fr;gap:.5rem;align-items:center;padding:.45rem .5rem;border-radius:8px;font-size:.95rem}
.road-nav button:hover{background:var(--pine-soft)}
.road-nav button[aria-selected="true"]{background:var(--pine-soft);font-weight:700}
.road-nav .n{font-family:var(--mono);font-size:.78rem;width:1.75rem;height:1.75rem;border-radius:50%;display:grid;place-items:center;border:2px solid var(--pine);color:var(--pine)}
.road-nav button.done .n{background:var(--pine);color:var(--paper)}
.step{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:clamp(1.2rem,3vw,2rem);display:grid;gap:1.4rem;min-width:0}
.step-head{display:grid;gap:.4rem}
.step .why{font-size:1.12rem;color:var(--muted);max-width:60ch}
.cols{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem}
.box{border-radius:10px;padding:1rem 1.1rem;display:grid;gap:.6rem;align-content:start;min-width:0}
.box.words{background:var(--blue-soft)}
.box.adult{background:var(--warn-soft)}
.box.adult .label{color:var(--warn)}
.box.example{background:var(--pine-soft)}
.box ul{margin:0;padding-left:1.1rem;display:grid;gap:.35rem}
.chip{display:inline-block;border:1px solid var(--blue);color:var(--blue);background:transparent;border-radius:999px;padding:.1rem .65rem;font-size:.88rem;cursor:pointer;font-family:var(--body);margin:0 .3rem .35rem 0}
.chip:hover{background:var(--blue);color:var(--surface)}
.checklist{display:grid;gap:.5rem;list-style:none;padding:0;margin:0}
.checklist label{display:grid;grid-template-columns:1.3rem 1fr;gap:.6rem;align-items:start;cursor:pointer}
.checklist input{width:1.15rem;height:1.15rem;margin-top:.25rem;accent-color:var(--pine)}
.step-foot{display:flex;justify-content:space-between;gap:1rem;flex-wrap:wrap;border-top:1px solid var(--line);padding-top:1rem}

/* Calculator */
.calc{border:2px solid var(--marigold);border-radius:12px;padding:1.1rem;display:grid;gap:1rem}
.calc-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:.8rem}
.calc label{display:grid;gap:.25rem;font-size:.88rem;color:var(--muted)}
.calc input{font:inherit;font-size:1rem;color:var(--ink);background:var(--paper);border:1px solid var(--line);border-radius:8px;padding:.5rem .6rem;width:100%;font-variant-numeric:tabular-nums}
.calc-out{display:grid;grid-template-columns:repeat(3,1fr);gap:.8rem}
.calc-out div{background:var(--marigold-soft);border-radius:8px;padding:.7rem .8rem}
.calc-out b{display:block;font-family:var(--display);font-size:1.5rem;font-variant-numeric:tabular-nums}
.calc-note{font-size:.95rem}

/* Glossary */
.search{display:flex;gap:.75rem;flex-wrap:wrap;align-items:center}
.search input{flex:1 1 260px;font:inherit;padding:.75rem 1rem;border-radius:10px;border:2px solid var(--line);background:var(--surface);color:var(--ink)}
.gloss{display:grid;grid-template-columns:repeat(2,1fr);gap:1rem}
.term{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:1rem 1.15rem;display:grid;gap:.4rem;align-content:start;scroll-margin-top:100px}
.term.flash{outline:3px solid var(--marigold)}
.term h3{font-size:1.15rem}
.term .also{font-size:.85rem;color:var(--muted)}
.term .ex{font-size:.95rem;color:var(--muted);border-top:1px dashed var(--line);padding-top:.45rem}
.term .ex b{color:var(--ink)}

/* Pathways */
.pick{display:flex;gap:.5rem;flex-wrap:wrap}
.pick button{font:inherit;font-weight:700;padding:.55rem 1rem;border-radius:10px;border:2px solid var(--line);background:var(--surface);color:var(--ink);cursor:pointer}
.pick button[aria-pressed="true"]{border-color:var(--pine);background:var(--pine);color:var(--paper)}
.path{display:grid;gap:1.4rem}
.ideas{display:grid;grid-template-columns:repeat(3,1fr);gap:.8rem}
.idea{background:var(--surface);border:1px solid var(--line);border-radius:10px;padding:.85rem 1rem;display:grid;gap:.25rem;align-content:start}
.idea b{font-family:var(--display);font-weight:600}
.idea span{font-size:.93rem;color:var(--muted)}
.local{border:2px dashed var(--line);border-radius:10px;padding:1rem 1.1rem;display:grid;gap:.4rem;color:var(--muted)}
.local .label{color:var(--marigold)}

/* Rules table */
.tbl-wrap{overflow-x:auto;border:1px solid var(--line);border-radius:12px;background:var(--surface)}
table{border-collapse:collapse;width:100%;min-width:720px;font-size:.96rem}
th,td{text-align:left;vertical-align:top;padding:.85rem 1rem;border-bottom:1px solid var(--line)}
th{font-family:var(--mono);font-size:.74rem;letter-spacing:.07em;text-transform:uppercase;color:var(--muted);font-weight:500}
tr:last-child td{border-bottom:0}
td:first-child{font-weight:700;width:22%}
.pill{display:inline-block;font-family:var(--mono);font-size:.72rem;padding:.12rem .5rem;border-radius:999px;letter-spacing:.04em;white-space:nowrap}
.pill.must{background:var(--warn-soft);color:var(--warn)}
.pill.maybe{background:var(--marigold-soft);color:var(--ink)}
.pill.free{background:var(--pine-soft);color:var(--pine)}

/* Resources */
.res{display:grid;grid-template-columns:repeat(2,1fr);gap:1rem}
.res .tile .label{color:var(--pine)}
.sources{font-size:.9rem;color:var(--muted)}
.sources ol{padding-left:1.2rem;display:grid;gap:.3rem}

/* Teacher */
.practice{display:grid;gap:.9rem;counter-reset:bp}
.practice > div{display:grid;grid-template-columns:2.4rem 1fr;gap:.8rem;background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:1rem}
.practice h3{font-size:1.08rem}
.practice p{color:var(--muted);font-size:.97rem}
.practice .ic{width:2.4rem;height:2.4rem;border-radius:10px;background:var(--pine-soft);display:grid;place-items:center;color:var(--pine)}

footer{border-top:1px solid var(--line);padding-block:1.5rem 2.5rem;font-size:.88rem;color:var(--muted)}

@media (max-width:860px){
  .hero,.road,.cols{grid-template-columns:1fr}
  .three,.ideas{grid-template-columns:1fr 1fr}
  .road-nav{position:static;grid-template-columns:repeat(4,1fr);gap:.3rem}
  .road-nav button{grid-template-columns:1fr;justify-items:center;text-align:center;font-size:.78rem;padding:.4rem .2rem}
  .road-nav button span:last-child{display:none}
  .calc-grid{grid-template-columns:1fr 1fr}
  nav.tabs{margin-left:0}
}
@media (max-width:560px){
  .three,.ideas,.gloss,.res,.calc-out{grid-template-columns:1fr}
  body{font-size:16px}
}
@media (prefers-reduced-motion:no-preference){.term,.step{transition:outline-color .3s}}
</style>
</head>
<body>
<header class="top">
  <div class="wrap bar">
    <a class="brand" href="#home">
      <svg width="26" height="26" viewBox="0 0 26 26" aria-hidden="true"><circle cx="13" cy="13" r="12" fill="none" stroke="currentColor" stroke-width="2"/><path d="M13 5 L18 17 L13 14.5 L8 17 Z" fill="var(--marigold)"/></svg>
      Boerne ISD Launch Pad
    </a>
    <nav class="tabs" aria-label="Sections">
      <a href="#home">Start here</a>
      <a href="#roadmap">The Roadmap</a>
      <a href="#words">Word Bank</a>
      <a href="#pathways">Your Pathway</a>
      <a href="#rules">Texas Rules</a>
      <a href="#help">Get Help</a>
      <a href="#teachers">For Teachers</a>
    </nav>
  </div>
</header>

<main class="wrap">

<!-- HOME -->
<section class="view" id="v-home">
  <div class="hero">
    <div>
      <p class="label">Boerne ISD · Boerne High &amp; Champion High · Grades 9–12</p>
      <h1>You already have a skill someone will pay for.</h1>
      <p class="lede">This is a step-by-step map for turning what you learn in your CTE class into a real, small business. No business words assumed. Every new word is explained the first time you see it.</p>
      <div class="cta">
        <a class="btn primary" href="#roadmap">Start the Roadmap</a>
        <a class="btn ghost" href="#pathways">Find ideas for my pathway</a>
      </div>
    </div>
    <div class="ladder" id="homeLadder" aria-label="The eight steps"></div>
  </div>

  <div class="prose">
    <p class="label">First, two words</p>
    <p class="big-def"><b>Business:</b> anything you do where people give you money in exchange for something they want, like a product (a thing) or a service (work you do for them).</p>
    <p class="big-def"><b>Entrepreneur</b> (on-truh-pruh-NUR): a person who starts their own business and takes on the risk of it. If you mow lawns for money, you are already one.</p>
  </div>

  <div class="three">
    <div class="tile"><p class="label">Step by step</p><h3>Follow the Roadmap</h3><p>Eight steps, in order, from "I have an idea" to "I'm making sales and keeping records." Check things off as you go. Your progress stays on this device.</p></div>
    <div class="tile"><p class="label">Plain language</p><h3>Use the Word Bank</h3><p>Stuck on a word like <i>profit</i> or <i>sole proprietor</i>? Tap any blue word to see what it means, with an example.</p></div>
    <div class="tile"><p class="label">Built for CTE</p><h3>Pick your pathway</h3><p>Ag and FFA, Culinary, Trades, Creative and Tech, or Business and Finance. Each has ideas and rules that fit that kind of work.</p></div>
  </div>

  <div class="draft"><b>Draft</b><span>This is a working draft. Pathway details, local contacts and examples will be added over time. Rules were last checked in October 2026. Always confirm legal and tax rules with an adult, since laws change.</span></div>
</section>

<!-- ROADMAP -->
<section class="view" id="v-roadmap" hidden>
  <div class="prose">
    <p class="label">The Roadmap</p>
    <h2>Eight steps from idea to open for business</h2>
    <p>Do them in order. Most students who struggle skipped Step 2 (talking to customers) and spent money on something nobody wanted.</p>
  </div>
  <div class="road">
    <div class="road-nav" id="roadNav" role="tablist" aria-label="Roadmap steps"></div>
    <div id="stepPanel"></div>
  </div>
</section>

<!-- WORDS -->
<section class="view" id="v-words" hidden>
  <div class="prose">
    <p class="label">Word Bank</p>
    <h2>Business words, in plain English</h2>
    <p>Every word has a simple meaning and a real example. Search, or scroll.</p>
  </div>
  <div class="search">
    <label for="q" class="label">Search</label>
    <input id="q" type="search" placeholder="Try: profit, permit, LLC…" autocomplete="off">
    <span id="qCount" class="label"></span>
  </div>
  <div class="gloss" id="gloss"></div>
</section>

<!-- PATHWAYS -->
<section class="view" id="v-pathways" hidden>
  <div class="prose">
    <p class="label">Your Pathway</p>
    <h2>Business ideas that use what you're learning</h2>
    <p>Choose your CTE pathway to see starter ideas, rules that apply to that kind of work, and student organizations that reward you for it.</p>
  </div>
  <div class="pick" id="pathPick" role="group" aria-label="Choose a pathway"></div>
  <div class="path" id="pathPanel"></div>
</section>

<!-- RULES -->
<section class="view" id="v-rules" hidden>
  <div class="prose">
    <p class="label">Texas Rules</p>
    <h2>What's required, and what's just a good idea</h2>
    <p>Most student businesses start as a <a href="#" data-term="sole proprietor">sole proprietor</a>: just you, no paperwork to "become" a business. But some things do need forms. Because you're under 18, an adult usually has to sign for you.</p>
  </div>
  <div class="tbl-wrap">
    <table>
      <thead><tr><th>The thing</th><th>Do I need it?</th><th>What it means for a student</th><th>Where to go</th></tr></thead>
      <tbody>
        <tr><td>Sales and Use Tax Permit</td><td><span class="pill must">If you sell taxable items</span></td><td>Lets you collect sales tax from customers and send it to the state. It's free. You must be 18 to apply, but a parent or guardian can apply for you. The state rate is 6.25%, and cities and counties add a little more.</td><td><a href="https://comptroller.texas.gov/taxes/permit/" target="_blank" rel="noopener">Texas Comptroller</a></td></tr>
        <tr><td>Assumed Name Certificate (a "DBA")</td><td><span class="pill maybe">If you use a business name</span></td><td>If your business name isn't your own legal name (for example "Maria's Mobile Detailing"), file this with the county clerk. Fees vary by county, often about $15–$25. It lasts up to 10 years. It does not stop someone else from using the same name.</td><td>Your county clerk's office</td></tr>
        <tr><td>Cottage food rules</td><td><span class="pill free">Food made at home</span></td><td>Texas lets you sell many homemade foods without a city or county permit. Since September 1, 2025, the yearly limit is $150,000. You can't ship by mail, and every item needs a label. Some refrigerated foods are now allowed if you follow extra rules.</td><td><a href="https://www.dshs.texas.gov/" target="_blank" rel="noopener">Texas DSHS</a></td></tr>
        <tr><td>Federal tax return</td><td><span class="pill must">If profit is $400+</span></td><td>If you make $400 or more in profit for the year from your own business, you must file a tax return, at any age. You can sign it yourself. You'll likely owe <a href="#" data-term="self-employment tax">self-employment tax</a> even if you owe no income tax.</td><td><a href="https://www.irs.gov/newsroom/when-the-lemonade-stand-makes-bank-young-entrepreneurs-and-taxes" target="_blank" rel="noopener">IRS: young entrepreneurs</a></td></tr>
        <tr><td>Bank account</td><td><span class="pill maybe">Strongly suggested</span></td><td>Keep business money separate from your own money. Most banks require an adult on the account if you're under 18.</td><td>A local bank or credit union</td></tr>
        <tr><td>Contracts and signatures</td><td><span class="pill maybe">Ask an adult</span></td><td>Because you're a minor, many companies won't sign deals with you alone (like renting a booth). Plan on a parent or guardian co-signing.</td><td>Parent, guardian or teacher</td></tr>
        <tr><td>Special licenses</td><td><span class="pill must">Some trades</span></td><td>Some work needs a state license no matter your age, like electrical, plumbing, HVAC, cosmetology on paying clients, or pesticide use. Check before you offer that service.</td><td><a href="https://www.tdlr.texas.gov/" target="_blank" rel="noopener">TDLR</a> and your teacher</td></tr>
        <tr><td>HOA and city rules</td><td><span class="pill maybe">Check locally</span></td><td>Your neighborhood or city may limit signs, traffic, or selling from home. A quick call saves trouble later.</td><td>City hall or your HOA</td></tr>
      </tbody>
    </table>
  </div>
  <div class="local"><p class="label">Add local info</p><p>Boerne is in Kendall County, so assumed name filings go to the Kendall County Clerk. Still to add: the clerk's current fee and address, nearby farmers markets that welcome student vendors, and the city contact for home business questions.</p></div>
</section>

<!-- HELP -->
<section class="view" id="v-help" hidden>
  <div class="prose">
    <p class="label">Get Help</p>
    <h2>Programs and people already helping Texas students</h2>
    <p>You don't have to figure this out alone. These groups exist to help young business owners, and most are free.</p>
  </div>
  <div class="res">
    <div class="tile"><p class="label">Student organization</p><h3>DECA</h3><p>The business and marketing student group. Its competitions include writing a real business plan and pitching it to judges. Texas has one of the biggest DECA associations anywhere.</p><a href="https://www.texasdeca.org/" target="_blank" rel="noopener">Texas DECA</a></div>
    <div class="tile"><p class="label">Student organization</p><h3>FFA and your SAE</h3><p>An "Entrepreneurship SAE" means you own an ag business and take the money risk yourself. FFA gives proficiency awards and scholarships for it in dozens of areas, from beef to landscaping.</p><a href="https://www.texasffa.org/" target="_blank" rel="noopener">Texas FFA</a></div>
    <div class="tile"><p class="label">Free advising</p><h3>Small Business Development Centers (SBDC)</h3><p>Texas has SBDC networks run by universities. They give free one-on-one advice on planning, money and marketing.</p><a href="https://americassbdc.org/find-your-sbdc/" target="_blank" rel="noopener">Find your SBDC</a></div>
    <div class="tile"><p class="label">Free mentor</p><h3>SCORE</h3><p>Volunteer business owners who mentor new entrepreneurs for free. There are chapters across Texas, including South and Central Texas.</p><a href="https://www.score.org/" target="_blank" rel="noopener">SCORE</a></div>
    <div class="tile"><p class="label">School course</p><h3>Entrepreneurship I, II and Practicum</h3><p>Texas updated its high school entrepreneurship courses starting in 2024–25. Ask your counselor whether your school offers them.</p><a href="https://tea.texas.gov/academics/curriculum-standards/teks-review/2023-cte-teks-review" target="_blank" rel="noopener">TEA course standards</a></div>
    <div class="tile"><p class="label">School program</p><h3>INCubatoredu</h3><p>A year-long course used at dozens of Texas high schools. Student teams get a community mentor, test ideas with real customers, and pitch to investors at the end.</p><a href="https://www.uncharted-learning.org/" target="_blank" rel="noopener">Uncharted Learning</a></div>
    <div class="tile"><p class="label">Started in Texas</p><h3>Lemonade Day</h3><p>Began in Houston in 2007. Younger kids run a real stand and learn budgets, profit, and paying back investors. Great for high schoolers to mentor.</p><a href="https://lemonadeday.org/" target="_blank" rel="noopener">Lemonade Day</a></div>
    <div class="tile"><p class="label">Summer</p><h3>University summer camps</h3><p>UT Austin, Texas A&amp;M, Texas Tech, Dallas College and others run business and entrepreneurship camps for high schoolers. Many are free.</p><span class="label" style="text-transform:none;letter-spacing:0">Ask your counselor for this year's list</span></div>
  </div>
  <div class="prose"><p class="label">Right here in Boerne</p></div>
  <div class="res">
    <div class="tile"><p class="label">Boerne ISD pilot</p><h3>Straight to Trades</h3><p>A Boerne ISD pilot at Champion High that pairs trade skills with business and leadership lessons. Students then move into a local incubator to build their own trades company and finish with a pitch competition.</p><a href="https://communityimpact.com/san-antonio/education/straight-to-trades-program-launches-at-boerne-isd-combining-trade-skills-with-entrepreneurship/" target="_blank" rel="noopener">Read about the program</a></div>
    <div class="tile"><p class="label">Local incubator</p><h3>Das GreenHaus</h3><p>A Boerne business incubator: a place that gives new businesses workspace, mentors and support. It partners with Straight to Trades.</p><span class="label" style="text-transform:none;letter-spacing:0">Add link and contact</span></div>
    <div class="tile"><p class="label">Local partners</p><h3>Greater Boerne Chamber &amp; Boerne Kendall County EDC</h3><p>The chamber of commerce (a group of local businesses) and the economic development corporation both help support student entrepreneurship in Boerne.</p><span class="label" style="text-transform:none;letter-spacing:0">Add link and contact</span></div>
  </div>
  <div class="local"><p class="label">Add local info</p><p>Our nearest SBDC office, SCORE chapter, chamber of commerce youth programs, and local business owners willing to mentor.</p></div>
</section>

<!-- TEACHERS -->
<section class="view" id="v-teachers" hidden>
  <div class="prose">
    <p class="label">For Teachers</p>
    <h2>How to use this site, and what research says works</h2>
    <p>Students can work through the Roadmap on their own, but it's built to pair with class time. Each step ends with a checklist that works as an exit ticket or a project milestone.</p>
  </div>
  <div class="practice" id="practice"></div>
  <div class="prose">
    <h3>Suggested pacing</h3>
    <p>One semester: about two weeks per Roadmap step, with Steps 2 and 3 (customers and money) given the most time. A year-long course or a practicum can add a real launch and a public pitch night at the end.</p>
    <h3>How to grow this site</h3>
    <p>Dashed boxes marked <b>Add local info</b> are placeholders. For each pathway, add: local student business examples, which industry certifications help, nearby mentors, and any extra licenses for that field.</p>
  </div>
  <div class="sources" id="sources"></div>
</section>

</main>

<footer>
  <div class="wrap">Boerne ISD Launch Pad is an educational guide, not legal or tax advice. Rules last checked October 2026. Talk with a parent, guardian, or trusted adult before signing anything or filing forms.</div>
</footer>

<script>
(function(){
const store={get(k,d){try{const v=localStorage.getItem(k);return v?JSON.parse(v):d}catch(e){return d}},set(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}}};
const done=store.get('lp-done',{});

/* ---------- Glossary ---------- */
const WORDS=[
["Business","A way of earning money by giving people something they want.","Selling homemade salsa at a farmers market is a business."],
["Entrepreneur","Someone who starts and owns a business and takes on its risk.","A welding student who builds and sells custom fire pits."],
["Product","A thing you make or sell.","Phone cases, bread, a bale of hay."],
["Service","Work you do for someone.","Washing cars, editing videos, fixing small engines."],
["Customer","The person who pays you.","The neighbor who pays you to mow their yard."],
["Target market","The specific group of people most likely to buy from you.","For a prom-photo business: juniors and seniors at nearby schools and their parents."],
["Problem / need","Something people want fixed, made easier, or made better. Good businesses solve one.","\"I don't have time to clean my truck\" is a need a detailing business solves."],
["Value proposition","One sentence that says why a customer should pick you.","\"Fresh tamales, delivered warm to your door on Saturdays.\""],
["Competitor","Another business selling something similar to the same customers.","The car wash down the street competes with your mobile detailing."],
["Market research","Finding out what customers want before you spend money.","Asking 20 classmates what they'd pay for a custom hoodie."],
["Survey","A short list of questions you ask possible customers.","A 5-question Google Form shared with parents in the band booster group."],
["Prototype","A rough first version you can show people.","One sample cutting board to show at a booth before making twenty."],
["Minimum viable product (MVP)","The simplest version that still solves the problem, so you can start selling and learning fast.","Offering just one cookie flavor at first instead of eight."],
["Pivot","Changing your plan based on what you learned.","No one wanted dog sweaters, but lots of people asked for dog-walking. So you switch."],
["Revenue","All the money that comes in from sales, before you pay anything.","Selling 30 plates at $10 each is $300 in revenue."],
["Cost","Money you spend to run the business.","Ingredients, gas, a domain name."],
["Startup costs","One-time money you spend to get going.","A pressure washer you buy once for a cleaning business."],
["Variable cost","A cost that goes up each time you make or sell one more.","Flour and sugar for each batch of cookies."],
["Fixed cost","A cost that stays the same no matter how much you sell.","A $15/month website fee."],
["Profit","The money left after you pay all costs. Revenue minus costs.","$300 revenue minus $120 costs is $180 profit."],
["Loss","When costs are bigger than revenue. You lost money.","Spending $80 on supplies and only selling $50."],
["Margin","How much of each sale you keep as profit, often shown as a percent.","Sell for $10, it cost $4 to make: $6 margin, or 60%."],
["Break-even point","The number of sales you need to pay back all your costs. After that, you make profit.","If your startup cost is $60 and you make $6 on each item, you break even at 10 sales."],
["Pricing","Deciding what to charge. It should cover costs, add profit, and make sense to customers.","Checking what others charge, then pricing a little above your cost plus your time."],
["Budget","A plan for how much money you'll spend and on what.","\"I'll spend $40 on supplies and $10 on flyers this month.\""],
["Cash flow","Money moving in and out over time. You can be profitable and still run out of cash.","You paid for supplies in March but customers don't pay you until April."],
["Inventory","Products you have made or bought but not sold yet.","24 jars of jam on your shelf."],
["Investor","Someone who gives you money to start or grow, expecting to get something back.","Your uncle gives you $200 and you agree to pay him back $220 by summer."],
["Loan","Borrowed money you must pay back, sometimes with extra (interest).","A $100 loan from a parent paid back $20 a week."],
["Interest","Extra money paid for borrowing money.","Borrow $200, pay back $220: the $20 is interest."],
["Business plan","A written description of your business: what you sell, to whom, how, and the numbers.","A 5-page plan you use for a DECA event or to ask for a loan."],
["Pitch","A short, convincing talk about your business, usually to customers, judges or investors.","A 2-minute pitch at a school pitch night."],
["Marketing","Everything you do so customers learn about you and want to buy.","Flyers, Instagram posts, a booth banner, word of mouth."],
["Brand","How people recognize and feel about your business: name, logo, colors, reputation.","A logo and a promise like \"done by Friday or it's free.\""],
["Social media marketing","Using apps like Instagram or TikTok to show your work and reach customers.","Posting before-and-after photos of detailed cars."],
["Sole proprietor","A business owned by one person, with no separate company formed. It's the simplest kind and the default when you just start selling.","You start pet-sitting under your own name. You're a sole proprietor."],
["LLC (Limited Liability Company)","A type of business you register with the state that keeps your personal belongings separate from business debts. Costs money to set up. Most students don't need one at first.","A student landscaping crew that grows big may form an LLC later with an adult's help."],
["Liability","Being legally responsible if something goes wrong.","If your client's car gets scratched while you detail it, you may be liable."],
["Assumed name (DBA)","\"Doing Business As.\" Filing that lets you use a business name that isn't your own name. In Texas, sole proprietors file it with the county clerk.","Filing so you can operate as \"Hill Country Welding Co.\""],
["Permit","Official permission from the government to do something.","A Texas sales tax permit lets you collect sales tax."],
["License","Proof you're allowed to do certain regulated work, often after training or a test.","A cosmetology license to cut hair for pay in a salon."],
["Sales tax","Extra money added to a sale that the business collects and sends to the state.","Selling a $20 shirt and collecting $1.65 more in sales tax."],
["Self-employment tax","Tax for Social Security and Medicare that people who work for themselves pay. It applies once your profit is $400 or more in a year.","On $1,000 of profit, about $141 in self-employment tax."],
["Expense","Any money spent to run the business. Tracking expenses lowers the taxes you owe.","Keeping the receipt for the $30 of clippers you bought."],
["Receipt","Proof of a purchase or a sale.","A photo of the store receipt for your supplies."],
["Records / bookkeeping","Writing down every dollar in and out.","A simple spreadsheet with date, what, money in, money out."],
["Invoice","A bill you send a customer that says what they owe and when.","\"Lawn service, 4 visits, $120, due May 1.\""],
["Contract","A written agreement about what each side will do. Minors usually need an adult to co-sign.","A one-page agreement for a DJ gig with date, hours, and price."],
["Mentor","An experienced person who gives you advice.","A local shop owner who meets with you once a month."],
["Scale / grow","Selling more, reaching more customers, or adding workers.","Going from one booth to three markets a weekend."],
["Social entrepreneur","Someone whose business also helps a cause or community.","A business that donates a meal for every five sold."],
["Spend, save, share","A simple plan for profit: use some, keep some, give some.","From $100 profit: $40 spend, $40 save, $20 donate."]
];
const W=WORDS.map(([t,d,e])=>({t,d,e,id:'w-'+t.toLowerCase().replace(/[^a-z0-9]+/g,'-')}));
const gloss=document.getElementById('gloss'),q=document.getElementById('q'),qc=document.getElementById('qCount');
function drawGloss(){
  const s=q.value.trim().toLowerCase();
  const list=W.filter(w=>!s||w.t.toLowerCase().includes(s)||w.d.toLowerCase().includes(s));
  gloss.innerHTML=list.map(w=>`<article class="term" id="${w.id}"><h3>${w.t}</h3><p>${w.d}</p><p class="ex"><b>Example:</b> ${w.e}</p></article>`).join('')||'<p>No matches. Try a shorter word.</p>';
  qc.textContent=list.length+' of '+W.length+' words';
}
q.addEventListener('input',drawGloss);
function findWord(name){name=name.toLowerCase();return W.find(w=>w.t.toLowerCase()===name)||W.find(w=>w.t.toLowerCase().startsWith(name))}
function openWord(name){
  const w=findWord(name);if(!w)return;
  q.value='';drawGloss();show('words');
  const el=document.getElementById(w.id);
  if(el){el.scrollIntoView({block:'center',behavior:matchMedia('(prefers-reduced-motion: reduce)').matches?'auto':'smooth'});el.classList.add('flash');setTimeout(()=>el.classList.remove('flash'),1800)}
}
document.addEventListener('click',e=>{const t=e.target.closest('[data-term]');if(t){e.preventDefault();openWord(t.dataset.term)}});

/* ---------- Roadmap ---------- */
const STEPS=[
{t:"Find a problem you can solve",s:"Idea",
 why:"Good businesses start with something people already want fixed, not a cool product nobody asked for. Start with what you're good at in your CTE class.",
 words:["Problem / need","Product","Service","Customer"],
 body:"Make three lists: skills you have (from class, hobbies, or a job), problems you notice people complaining about, and people you know who might pay. Where the lists overlap is your idea.",
 ex:"A culinary student notices teachers skip breakfast. Idea: pre-ordered breakfast tacos delivered before first period (with school approval).",
 todo:["Write 10 skills I have","Write 10 problems I hear people complain about","Circle my top 3 ideas where they overlap","Write each idea as one sentence: \"I help ___ by ___.\""],
 adult:"Ask a parent or teacher which idea fits your schedule, transportation and safety."},
{t:"Talk to real customers",s:"Test",
 why:"This is the step most people skip. Before you spend money, find out if people actually want it and what they'd pay.",
 words:["Target market","Market research","Survey","Competitor","Pivot"],
 body:"Pick who your customer is. Talk to at least 15 of them. Ask about their problem, not your idea: \"How do you handle this now? What's annoying about it? What do you pay?\" Look up who else already sells this and their prices.",
 ex:"A student planned to sell car air fresheners. Interviews showed people really wanted interior cleaning. She pivoted and booked six jobs in the first week.",
 todo:["Describe my target market in one sentence","Interview or survey at least 15 people","List 3 competitors and their prices","Decide: keep going, change the idea, or pick a new one"],
 adult:"Interview adults in safe, public places or with a parent nearby. Never share your home address online."},
{t:"Count the money",s:"Money",
 why:"You need to know what it costs to make one, what to charge, and how many you must sell before you're actually earning.",
 words:["Revenue","Cost","Startup costs","Profit","Break-even point","Pricing","Budget"],
 body:"List every cost. Split them into one-time startup costs and costs for each item you sell. Then try prices in the calculator below until the numbers work.",
 calc:true,
 ex:"Custom keychains: $1.50 in materials each, sell for $6. That's $4.50 profit each. A $45 tool set means 10 sales to break even.",
 todo:["List all startup costs","Figure the cost to make one item (or one job)","Choose a price and check it against competitors","Find my break-even number","Write a one-month budget"],
 adult:"If you'll borrow money, even from family, write down how and when you'll pay it back and both sign it."},
{t:"Name it and make it official",s:"Set up",
 why:"Once you sell anything, you're legally a business, called a sole proprietor. A few simple steps make it real and keep you out of trouble.",
 words:["Sole proprietor","Assumed name (DBA)","LLC (Limited Liability Company)","Liability","Brand"],
 body:"Pick a name and check that no one nearby is using it. If the name isn't your own name, an adult can help you file an assumed name certificate at the county clerk. Most students do not need an LLC to start. Open a separate bank account with a parent.",
 ex:"\"Garcia Ag Services\" files an assumed name in its county for about $20 and opens a joint account with a parent.",
 todo:["Pick a business name and check it's not taken locally","Decide if I need an assumed name filing","Open a separate account (with an adult)","Make a simple logo or look"],
 adult:"An adult will need to sign forms and bank paperwork because you're under 18."},
{t:"Check the Texas rules",s:"Rules",
 why:"Some things you sell need a permit, a license, or special labels. Checking now prevents fines later.",
 words:["Permit","License","Sales tax","Contract"],
 body:"Use the Texas Rules page. Ask: Do I sell taxable items (I'll need a sales tax permit)? Is it homemade food (cottage food rules)? Is my trade licensed (electrical, cosmetology, pesticides)? Are there city or HOA limits?",
 ex:"A baker selling cookies at a market doesn't need a city permit under Texas cottage food law, but must label each package correctly.",
 todo:["Read the Texas Rules page","Check if my pathway has special licenses","Ask an adult to apply for a sales tax permit if needed","Write a simple contract template for jobs"],
 adult:"Your parent or guardian applies for a sales tax permit on your behalf. Rules change, so double-check official sites."},
{t:"Start small and sell",s:"Launch",
 why:"Your first version should be small and simple. Sell, learn what customers say, then improve.",
 words:["Minimum viable product (MVP)","Prototype","Marketing","Social media marketing","Value proposition","Pitch"],
 body:"Make a small batch or book a few jobs. Tell people with a clear one-line value proposition. Ask every customer what they liked and what to change.",
 ex:"A graphic design student offers just one thing at first: $25 logo packages for local food trucks. Five sales later, she adds menu design.",
 todo:["Write my one-sentence value proposition","Make a small first batch or book 3 jobs","Post or hand out marketing in 2 places","Collect feedback from every customer"],
 adult:"Get permission before selling at school or on someone's property. Use a parent's help for online payments."},
{t:"Keep records and pay taxes",s:"Records",
 why:"Writing down every dollar shows whether you're really making money, and it lowers the taxes you owe.",
 words:["Records / bookkeeping","Receipt","Expense","Invoice","Self-employment tax","Cash flow"],
 body:"Use one simple spreadsheet: date, what happened, money in, money out. Save every receipt (a photo works). If your profit for the year is $400 or more, you must file a federal tax return, at any age.",
 ex:"A student earns $2,000 detailing and spends $700 on supplies. Profit is $1,300, so he files a return and pays about $184 in self-employment tax.",
 todo:["Set up my money-in, money-out sheet","Save every receipt","Check my total profit each month","Set aside about 15% of profit for taxes"],
 adult:"Have an adult or tax volunteer help with your first tax return."},
{t:"Grow and get help",s:"Grow",
 why:"Every business owner has advisors. Use the free help that already exists for young Texans.",
 words:["Mentor","Scale / grow","Business plan","Investor","Spend, save, share"],
 body:"Find a mentor. Enter your business in DECA or an FFA proficiency award. Decide how to use your profit: spend some, save some, share some. Then decide what's next: more customers, new products, or a bigger goal.",
 ex:"An FFA member's hay business wins a proficiency award, which leads to a scholarship and new customers.",
 todo:["Find one mentor","Look at a DECA or FFA event I could enter","Decide my spend/save/share split","Set one growth goal for next semester"],
 adult:"Mentors should meet you in public places or with a teacher involved."}
];
const nav=document.getElementById('roadNav'),panel=document.getElementById('stepPanel'),ladder=document.getElementById('homeLadder');
let cur=store.get('lp-step',0);
function isDone(i){const s=STEPS[i];return s.todo.every((_,j)=>done[i+'-'+j])}
function drawNav(){
  nav.innerHTML=STEPS.map((s,i)=>`<button role="tab" aria-selected="${i===cur}" class="${isDone(i)?'done':''}" data-i="${i}"><span class="n">${i+1}</span><span>${s.t}</span></button>`).join('');
  ladder.innerHTML='<p class="label" style="padding:0 .4rem .4rem">Your 8 steps</p>'+STEPS.map((s,i)=>`<a href="#roadmap" data-go="${i}" class="${isDone(i)?'done':''}"><span class="n">${i+1}</span><span>${s.t}</span></a>`).join('');
}
function drawStep(){
  const s=STEPS[cur];
  panel.innerHTML=`<article class="step">
   <div class="step-head"><p class="label">Step ${cur+1} of 8 · ${s.s}</p><h2>${s.t}</h2><p class="why">${s.why}</p></div>
   <p class="prose">${s.body}</p>
   ${s.calc?calcHTML():''}
   <div class="cols">
     <div class="box words"><p class="label">Words to know</p><div>${s.words.map(w=>`<button class="chip" data-term="${w}">${w}</button>`).join('')}</div></div>
     <div class="box example"><p class="label">Example</p><p>${s.ex}</p></div>
   </div>
   <div class="cols">
     <div class="box" style="padding-left:0"><p class="label">Do this</p><ul class="checklist">${s.todo.map((t,j)=>`<li><label><input type="checkbox" id="c-${cur}-${j}" data-k="${cur}-${j}" ${done[cur+'-'+j]?'checked':''}><span>${t}</span></label></li>`).join('')}</ul></div>
     <div class="box adult"><p class="label">Ask an adult</p><p>${s.adult}</p></div>
   </div>
   <div class="step-foot">
     ${cur>0?`<button class="btn ghost" data-step="${cur-1}">← Step ${cur}</button>`:'<span></span>'}
     ${cur<7?`<button class="btn primary" data-step="${cur+1}">Step ${cur+2}: ${STEPS[cur+1].t} →</button>`:`<a class="btn primary" href="#help">See who can help →</a>`}
   </div></article>`;
  if(s.calc)wireCalc();
}
function go(i){cur=i;store.set('lp-step',i);drawNav();drawStep()}
nav.addEventListener('click',e=>{const b=e.target.closest('button');if(b)go(+b.dataset.i)});
ladder.addEventListener('click',e=>{const a=e.target.closest('a');if(a)go(+a.dataset.go)});
panel.addEventListener('click',e=>{const b=e.target.closest('[data-step]');if(b){go(+b.dataset.step);document.getElementById('v-roadmap').scrollIntoView()}});
panel.addEventListener('change',e=>{if(e.target.dataset.k){done[e.target.dataset.k]=e.target.checked;store.set('lp-done',done);drawNav()}});

function calcHTML(){return `<div class="calc"><p class="label">Try your numbers</p>
 <div class="calc-grid">
  <label for="cp">Price you charge ($)<input id="cp" type="number" min="0" step="0.5" value="6"></label>
  <label for="cc">Cost to make one ($)<input id="cc" type="number" min="0" step="0.25" value="1.5"></label>
  <label for="cs">Startup costs ($)<input id="cs" type="number" min="0" step="5" value="45"></label>
  <label for="cn">How many you sell<input id="cn" type="number" min="0" step="1" value="30"></label>
 </div>
 <div class="calc-out"><div><span class="label">Profit per item</span><b id="o1"></b></div><div><span class="label">Break-even</span><b id="o2"></b></div><div><span class="label">Total profit</span><b id="o3"></b></div></div>
 <p class="calc-note" id="o4"></p></div>`}
function wireCalc(){
  const $=id=>document.getElementById(id),f=n=>(n<0?'−$':'$')+Math.abs(n).toFixed(2);
  function run(){
    const p=+$('cp').value||0,c=+$('cc').value||0,s=+$('cs').value||0,n=+$('cn').value||0,per=p-c;
    $('o1').textContent=f(per);
    $('o2').textContent=per>0?Math.ceil(s/per)+' sales':'never';
    const tot=per*n-s;$('o3').textContent=f(tot);
    $('o4').textContent=per<=0?'Your price is at or below your cost. Every sale loses money. Raise the price or lower the cost.'
      :tot<0?`You haven't paid back your startup costs yet. Sell ${Math.ceil(s/per)-n} more to break even.`
      :`After paying back your startup costs, you keep ${f(tot)}. Remember: your time is worth something too.`;
  }
  ['cp','cc','cs','cn'].forEach(id=>$(id).addEventListener('input',run));run();
}

/* ---------- Pathways ---------- */
const PATHS=[
{k:"ag",n:"Agriculture / FFA",
 intro:"Ag students already run real businesses through FFA. An Entrepreneurship SAE means you own the project and take the money risk, which is exactly what this Roadmap covers.",
 ideas:[["Show animal breeding","Raise and sell show goats, lambs, or pigs to younger exhibitors."],["Hay and forage","Cut, bale and sell hay to local horse and cattle owners."],["Plant nursery","Grow and sell native Texas plants, herbs, or vegetable starts."],["Eggs and poultry","Sell farm eggs (check egg grading rules for sales beyond the farm)."],["Ag mechanics shop","Build trailers, gates, feeders, or fix equipment."],["Lawn and landscape","Mowing, xeriscaping, and seasonal planting."]],
 rules:["Pesticide or herbicide use for clients needs a Texas Department of Agriculture license.","Selling eggs, meat or raw milk has special rules. Check before selling.","Keep your SAE records in AET. They double as your business records."],
 orgs:"Texas FFA proficiency awards (Entrepreneurship type), Ag Sales CDE, local stock shows and youth auctions."},
{k:"culinary",n:"Culinary / Hospitality",
 intro:"Texas cottage food law is one of the most generous in the country. Many foods made in your home kitchen can be sold without a city or county permit.",
 ideas:[["Baked goods","Cookies, breads, kolaches and cakes for markets and pre-orders."],["Event treats","Custom cupcakes or dessert tables for parties."],["Spice blends and dry mixes","Rubs, pancake mixes, and seasonings."],["Meal prep (check rules)","Some refrigerated foods are now allowed with extra requirements."],["Event helper","Serving or set-up crew for parties and weddings."],["Pop-up at school events","With school approval, sell at games or concerts."]],
 rules:["Cottage food: yearly sales up to $150,000, label every item, sell in Texas only, no shipping.","A food handler card is commonly required for cottage food sellers. Confirm current rules.","Kitchen work outside cottage food rules, like a food truck, needs a health permit."],
 orgs:"FCCLA Entrepreneurship and Culinary events, SkillsUSA Culinary Arts, DECA Hospitality events."},
{k:"trades",n:"Trades",
 intro:"Skilled trades are some of the easiest businesses to start: customers already know they need the work, and you can start with tools you have.",
 ideas:[["Custom welding","Fire pits, signs, BBQ pits, decor and repairs."],["Small engine repair","Mowers, weed eaters and go-karts."],["Mobile detailing","Interior and exterior car cleaning at the customer's home."],["Handyman (light work)","Fence repair, shelves, furniture assembly, painting."],["Woodworking","Cutting boards, benches, custom signs."],["Pressure washing","Driveways, decks and fences."]],
 rules:["Electrical, plumbing and HVAC work for pay require state licensing. Students can't do this work on their own.","Many customers want proof of insurance for work on their property. Ask an adult about coverage.","Use a written contract with price, timeline and what's included."],
 orgs:"Boerne ISD's Straight to Trades pilot at Champion High, SkillsUSA, FFA Ag Mechanics proficiency areas, DECA Entrepreneurship events."},
{k:"creative",n:"Creative / Tech",
 intro:"Creative and tech businesses often need almost no startup money. Your laptop and your portfolio are the business.",
 ideas:[["Graphic design","Logos, menus and flyers for local businesses."],["Photo and video","Senior pictures, sports highlights and event videos."],["Website help","Simple sites for small businesses and clubs."],["Print shop","Custom shirts, stickers and screen printing."],["Tech help","Set up phones, smart TVs and computers for older neighbors."],["Hair, nails and beauty (licensed)","Cosmetology students need a license to serve paying clients."]],
 rules:["Get written permission to use anyone's photo, logo or music. Don't sell other people's characters or brands.","Cosmetology services for pay require a Texas license.","Online payments usually need an adult's account if you're under 18."],
 orgs:"SkillsUSA, BPA, TSA, DECA Marketing events, Texas student media contests."},
{k:"business",n:"Business and Finance",
 intro:"Business and finance students can run their own idea, or help other students run theirs. Your class skills (accounting, marketing, management) are valuable services.",
 ideas:[["School-based store","Run the school store as a real business (DECA certifies these)."],["Marketing for others","Run social media for local shops."],["Bookkeeping helper","Help other student businesses track money."],["Resale business","Buy, clean up and resell sneakers, clothes or electronics."],["Tutoring","Math, test prep or study skills for younger students."],["Event planning","Plan birthday parties or club fundraisers."]],
 rules:["Reselling items usually means collecting sales tax. You'll likely need a sales tax permit through a parent.","Don't give tax or investment advice. That's licensed work.","Keep clear contracts for any client work."],
 orgs:"DECA (Entrepreneurship and School-Based Enterprise), BPA, FBLA, INCubatoredu at participating schools."}
];
let pk=store.get('lp-path','ag');
const pick=document.getElementById('pathPick'),pp=document.getElementById('pathPanel');
function drawPaths(){
  pick.innerHTML=PATHS.map(p=>`<button aria-pressed="${p.k===pk}" data-k="${p.k}">${p.n}</button>`).join('');
  const p=PATHS.find(x=>x.k===pk)||PATHS[0];
  pp.innerHTML=`<p class="prose">${p.intro}</p>
  <div><p class="label" style="margin-bottom:.6rem">Starter ideas</p><div class="ideas">${p.ideas.map(([a,b])=>`<div class="idea"><b>${a}</b><span>${b}</span></div>`).join('')}</div></div>
  <div class="cols">
    <div class="box adult"><p class="label">Rules to watch</p><ul>${p.rules.map(r=>`<li>${r}</li>`).join('')}</ul></div>
    <div class="box example"><p class="label">Compete and get recognized</p><p>${p.orgs}</p></div>
  </div>
  <div class="local"><p class="label">Add local info · ${p.n}</p><p>Student business examples from our school, helpful industry certifications, local mentors in this field, and where to sell nearby.</p></div>`;
}
pick.addEventListener('click',e=>{const b=e.target.closest('button');if(b){pk=b.dataset.k;store.set('lp-path',pk);drawPaths()}});

/* ---------- Teachers ---------- */
const PRACT=[
["Learn by doing","Research on entrepreneurship teaching keeps pointing to hands-on, project-based work over lectures. Students should run something real, even if tiny."],
["Test before you build","Programs like INCubatoredu use a \"lean startup\" approach: guess what customers want, test it fast with real people, then adjust. Step 2 of the Roadmap is built on this."],
["Bring in mentors","Successful Texas programs pair each student team with a community mentor who checks in regularly."],
["Use small real money","Some Texas schools give each team a small amount (one district used $200) to test an idea. Low stakes, real lessons."],
["End with a pitch","A public pitch night with local business judges gives students a real deadline and audience. Some Texas programs award real investment."],
["Make reflection routine","Students learn most when they stop to ask what worked, what didn't, and what they'll change. Use the checklists as reflection prompts."],
["Teach the words first","Students new to business vocabulary disengage fast. Pre-teach a few Word Bank terms per step and use the same words all semester."],
["Connect to CTSOs and SAEs","DECA events, FFA Entrepreneurship SAEs and school-based enterprises give students a reason to keep good records and polish their work."]
];
document.getElementById('practice').innerHTML=PRACT.map(([h,p])=>`<div><span class="ic" aria-hidden="true"><svg width="18" height="18" viewBox="0 0 18 18"><path d="M3 9.5l3.5 3.5L15 4.5" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"/></svg></span><div><h3>${h}</h3><p>${p}</p></div></div>`).join('');
const SRC=[
["Texas Comptroller: Sales tax permit","https://comptroller.texas.gov/taxes/permit/"],
["IRS Tax Tip: Young entrepreneurs and taxes","https://www.irs.gov/newsroom/when-the-lemonade-stand-makes-bank-young-entrepreneurs-and-taxes"],
["TEA: 2023 CTE TEKS review (Entrepreneurship)","https://tea.texas.gov/academics/curriculum-standards/teks-review/2023-cte-teks-review"],
["Texas CTE Resource Center: Entrepreneurship binder","https://www.txcte.org/course-binder/entrepreneurship-0"],
["FARFA: Cottage food law and SB 541","https://farmandranchfreedom.org/cottage-food-law-sb541/"],
["Forrager: Texas SB 541 summary","https://forrager.com/bill/texas-sb-541/"],
["Bexar County Clerk: Assumed name certificate","https://www.bexar.org/DocumentCenter/View/26459/Assumed-Name-Application-for-Certificate-of-Ownership"],
["Dallas Innovates: INCubatoredu in Texas schools","https://dallasinnovates.com/entrepreneurial-mindset-local-schools-giving-young-students-tools-to-create-their-own-businesses/"],
["Community Impact: Student entrepreneurs in Lake Travis/Westlake","https://communityimpact.com/lake-travis-westlake/news/no-minimum-age-trends-show-young-entrepreneurs-on-the-rise-in-the-lake-travis-westlake-area/"],
["Lemonade Day: Houston story","https://houston.lemonadeday.org/city-story"],
["National FFA: Proficiency awards","https://www.ffa.org/participate/awards/proficiencies/"],
["UH Texas Gulf Coast SBDC: Free advising","https://www.sbdc.uh.edu/sbdc/Consulting1.asp"],
["Community Impact: Straight to Trades at Boerne ISD","https://communityimpact.com/san-antonio/education/straight-to-trades-program-launches-at-boerne-isd-combining-trade-skills-with-entrepreneurship/"],
["REGEPE: Best practices in entrepreneurship teaching","https://regepe.emnuvens.com.br/regepe/article/download/2133/564/8812"]
];
document.getElementById('sources').innerHTML='<p class="label">Sources</p><ol>'+SRC.map(([t,u])=>`<li><a href="${u}" target="_blank" rel="noopener">${t}</a></li>`).join('')+'</ol>';

/* ---------- Views ---------- */
const VIEWS=['home','roadmap','words','pathways','rules','help','teachers'];
function show(v){
  if(!VIEWS.includes(v))v='home';
  VIEWS.forEach(x=>document.getElementById('v-'+x).hidden=x!==v);
  document.querySelectorAll('nav.tabs a').forEach(a=>a.getAttribute('href')==='#'+v?a.setAttribute('aria-current','page'):a.removeAttribute('aria-current'));
  try{if(location.hash!=='#'+v)history.replaceState(null,'','#'+v)}catch(e){}
}
document.addEventListener('click',e=>{const a=e.target.closest('a[href^="#"]');if(a&&!a.dataset.term){const v=a.getAttribute('href').slice(1);if(VIEWS.includes(v)){e.preventDefault();show(v);window.scrollTo(0,0)}}});
window.addEventListener('hashchange',()=>show(location.hash.slice(1)));

drawGloss();drawNav();drawStep();drawPaths();
show(location.hash.slice(1)||'home');
})();
</script>
</body>
</html>
