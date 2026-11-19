<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>আমাদের সেবা</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root{--green:#0B7F47;--green-soft:#E6F4EA;--red-soft:#FCE8E8;--red:#C62828;--blue-soft:#E6EEF9;--blue:#2F6AA3;--purple-soft:#F0EAF9;--purple:#7B4FBF;--bg:#F7F8F7;--card:#FFFFFF;--text:#111;--muted:#5d6b63;--border:#E3E6E4;--mint:#bfe6d0}
  @media (prefers-color-scheme: dark){:root:not([data-theme="light"]){--bg:#101412;--card:#1a201c;--text:#f2f4f3;--muted:#9aa8a0;--border:#2a332e;--green-soft:#173325;--red-soft:#3a1f1f;--blue-soft:#1c2a3d;--purple-soft:#2a2238}}
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{background:var(--bg);color:var(--text);font-family:"Noto Sans Bengali",Inter,system-ui,sans-serif}
  body{min-height:100vh;display:flex;justify-content:center;padding:16px 10px}
  [hidden]{display:none!important}
  a{color:inherit;text-decoration:none}
  .app{width:100%;max-width:380px;background:var(--bg);border:1px solid var(--border);border-radius:28px;overflow:hidden;position:relative;min-height:720px;padding-bottom:72px}
  .view{padding:16px 16px 24px}
  .topbar{display:flex;align-items:center;gap:12px;margin-bottom:16px}
  .back{width:36px;height:36px;border-radius:12px;background:var(--card);border:1px solid var(--border);display:grid;place-items:center;font-size:18px;color:var(--text);flex-shrink:0}
  .topbar h2{font-size:18px;font-weight:700}
  .hero{background:var(--green);color:#fff;border-radius:24px;padding:28px 20px;text-align:center}
  .logo{width:64px;height:64px;margin:0 auto 14px;border-radius:18px;background:rgba(255,255,255,.15);display:grid;place-items:center;font-weight:700;font-size:13px;line-height:1.2}
  .hero h1{font-size:20px;font-weight:700}
  .hero p{font-size:14px;color:var(--mint);margin-top:8px}
  .wallet{background:var(--green);color:#fff;border-radius:24px;padding:22px 20px;margin-bottom:16px}
  .wallet .kicker{font-family:Inter,sans-serif;font-size:13px;color:var(--mint)}
  .wallet .amount{font-family:Inter,sans-serif;font-size:32px;font-weight:700;margin-top:8px}
  .wallet .label{font-size:13px;color:var(--mint);margin-top:6px}
  .grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
  .tile{border-radius:22px;padding:22px 12px 20px;text-align:center;display:flex;flex-direction:column;align-items:center;gap:10px;color:var(--text);transition:transform .15s}
  .tile:active{transform:scale(.97)}
  .tile h3{font-size:16px;font-weight:700}
  .tile small{font-size:13px;color:var(--muted);line-height:1.4}
  .t-green{background:var(--green-soft)} .t-red{background:var(--red-soft)} .t-blue{background:var(--blue-soft)} .t-purple{background:var(--purple-soft)}
  .c-green{color:var(--green)} .c-red{color:var(--red)} .c-blue{color:var(--blue)} .c-purple{color:var(--purple)}
  .svg{width:34px;height:34px;fill:none;stroke:currentColor;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round}
  .sm{width:22px;height:22px}
  .ibox{width:44px;height:44px;border-radius:14px;display:grid;place-items:center;flex-shrink:0}
  .card{background:var(--card);border:1px solid var(--border);border-radius:20px;padding:6px 16px;margin-bottom:12px}
  .card.plain{padding:16px}
  .row{display:flex;align-items:center;gap:12px;padding:14px 0;border-bottom:1px solid var(--border)}
  .row:last-child{border-bottom:none}
  .row .meta{flex:1;min-width:0}
  .row .meta b{display:block;font-size:15px}
  .row .meta span{font-size:13px;color:var(--muted);display:block}
  .chev{color:var(--muted);font-size:20px}
  .muted{font-size:13px;color:var(--muted);line-height:1.5}
  .field{margin:12px 0}
  .field label{display:block;font-size:13px;color:var(--muted);margin-bottom:6px}
  .field input{width:100%;background:var(--bg);border:1px solid var(--border);border-radius:14px;padding:13px 14px;font:inherit;font-size:15px;color:var(--text)}
  .kv{display:flex;justify-content:space-between;font-size:14px;padding:12px 0;border-bottom:1px dashed var(--border)}
  .kv:last-child{border-bottom:none}
  .kv span:last-child{font-weight:600;font-family:Inter,sans-serif}
  .btn{width:100%;background:var(--green);color:#fff;border:none;border-radius:16px;padding:15px;font:inherit;font-size:16px;font-weight:700;margin-top:4px}
  .avatar{width:38px;height:38px;border-radius:50%;display:grid;place-items:center;font-weight:700;font-size:14px;background:var(--green-soft);color:var(--green);flex-shrink:0}
  .bubble{max-width:78%;padding:10px 14px;border-radius:18px;font-size:14px;line-height:1.5;margin-bottom:8px}
  .in{background:var(--card);border:1px solid var(--border);border-top-left-radius:6px}
  .out{background:var(--green);color:#fff;border-top-right-radius:6px;margin-left:auto}
  .time-s{font-size:11px;opacity:.7;margin-top:4px;text-align:right}
  .day{align-self:center;font-size:12px;color:var(--muted);background:var(--card);border-radius:999px;padding:4px 12px;margin:6px 0 10px}
  .composer{display:flex;gap:8px;align-items:center;margin-top:auto;padding-top:12px}
  .composer .input{flex:1;background:var(--card);border:1px solid var(--border);border-radius:999px;padding:12px 16px;font-size:14px;color:var(--muted)}
  .fab{width:44px;height:44px;border-radius:50%;background:var(--green);color:#fff;display:grid;place-items:center;border:none}
  .nav{position:absolute;left:0;right:0;bottom:0;background:var(--card);border-top:1px solid var(--border);display:flex;justify-content:space-around;padding:8px 0 12px}
  .nav a{display:flex;flex-direction:column;align-items:center;gap:3px;font-size:11px;color:var(--muted);padding:4px 10px}
  .nav a.on{color:var(--green);font-weight:600}
</style>
</head>
<body>
<div class="app">

<!-- ===== HOME ===== -->
<section class="view" id="v-home">
  <div class="hero">
    <div class="logo">আমাদের<br>সেবা</div>
    <h1>এক অ্যাপে যোগাযোগ ও লেনদেন</h1>
    <p>বাংলাদেশের মানুষের জন্য একটি ডিজিটাল প্ল্যাটফর্ম</p>
  </div>
  <div style="height:16px"></div>
  <div class="grid">
    <a href="#cat-comm" class="tile t-green"><svg class="c-green svg" viewBox="0 0 24 24"><path d="M21 11.5a8.4 8.4 0 0 1-9 8.4 8.6 8.6 0 0 1-3.8-.9L3 21l1.9-5.1A8.4 8.4 0 1 1 21 11.5z"/></svg><h3>যোগাযোগ</h3><small>চ্যাট, কল, ফাইল</small></a>
    <a href="#cat-bank" class="tile t-red"><svg class="c-red svg" viewBox="0 0 24 24"><rect x="2.5" y="6" width="19" height="13" rx="2.5"/><path d="M2.5 10h19"/><circle cx="16.5" cy="14.5" r="1.3"/></svg><h3>মোবাইল ব্যাংকিং</h3><small>টাকা পাঠানো ও গ্রহণ</small></a>
    <a href="#cat-id" class="tile t-blue"><svg class="c-blue svg" viewBox="0 0 24 24"><path d="M12 3l7.5 3v5.5c0 4.5-3.2 8-7.5 9.5-4.3-1.5-7.5-5-7.5-9.5V6z"/><path d="M9 12l2.2 2.2L15.5 10"/></svg><h3>পরিচয় যাচাই</h3><small>NID, পাসপোর্ট, Face</small></a>
    <a href="#cat-sec" class="tile t-purple"><svg class="c-purple svg" viewBox="0 0 24 24"><path d="M6 11a6 6 0 0 1 12 0v2"/><path d="M4 13.5a8 8 0 0 1 16 0"/><path d="M9 20c.5-1.5 1-3 1-6a2 2 0 0 1 4 0c0 3 .5 5 1.5 6"/></svg><h3>নিরাপত্তা</h3><small>PIN ও বায়োমেট্রিক</small></a>
  </div>
</section>

<!-- ===== WALLET ===== -->
<section class="view" id="v-wallet" hidden>
  <div class="wallet">
    <div class="kicker">Your Digital Financial Hub</div>
    <div class="amount">৳ ২৫,০০০.০০</div>
    <div class="label">নমুনা ওয়ালেট ব্যালেন্স</div>
  </div>
  <div class="grid">
    <a href="#cat-loan" class="tile t-green"><svg class="c-green svg" viewBox="0 0 24 24"><path d="M2 13l4-4 3 2 5-4 4 3 4-2"/><path d="M6 17l3 3h3a2 2 0 0 0 0-4h-2"/></svg><h3>১. লোন সুবিধা</h3><small>ঋণের আবেদন, কিস্তি ও পরিশোধ</small></a>
    <a href="#cat-dps" class="tile t-red"><svg class="c-red svg" viewBox="0 0 24 24"><path d="M4 11c0-3 2.5-5 6-5h4c3.5 0 6 2 6 5v1l2 1v2l-2 .5c-.5 2-2.5 3.5-5 3.5H9l-3-2v-2"/><circle cx="14.5" cy="10" r=".8"/></svg><h3>২. DPS সুবিধা</h3><small>মাসিক সঞ্চয় ও কিস্তি</small></a>
    <a href="#cat-fdr" class="tile t-blue"><svg class="c-blue svg" viewBox="0 0 24 24"><path d="M3 9.5L12 4l9 5.5"/><path d="M5 10v8M9.5 10v8M14.5 10v8M19 10v8M3 20h18"/></svg><h3>৩. FDR সুবিধা</h3><small>নির্দিষ্ট মেয়াদে আমানত</small></a>
    <a href="#cat-mfs" class="tile t-purple"><svg class="c-purple svg" viewBox="0 0 24 24"><path d="M4 8h14l-3-3M20 16H6l3 3"/></svg><h3>৪. অন্যান্য ব্যাংক ও MFS</h3><small>অনুমোদিত সংযোগ ও লেনদেন</small></a>
  </div>
</section>

<!-- ===== CHAT THREAD ===== -->
<section class="view" id="v-thread" hidden>
  <div class="topbar">
    <a class="back" href="#cat-comm">‹</a>
    <div class="avatar">র</div>
    <div style="flex:1"><b style="font-size:15px">রহিম আহমেদ</b><div class="muted" style="color:var(--green)">অনলাইন</div></div>
    <span class="back">📞</span>
  </div>
  <div style="display:flex;flex-direction:column;min-height:460px">
    <div class="day">আজ</div>
    <div class="bubble in">আসসালামু আলাইকুম, কালকের মিটিংটা কখন হবে?<div class="time-s" style="color:var(--muted)">১০:৪০</div></div>
    <div class="bubble out">ওয়ালাইকুম আসসালাম, সকাল ১১টায় হতে পারে।<div class="time-s">১০:৪১ ✓✓</div></div>
    <div class="bubble in">ঠিক আছে, প্রস্তাবনার ফাইলটাও পাঠিয়ে দিন।<div class="time-s" style="color:var(--muted)">১০:৪২</div></div>
    <div class="bubble out">পাঠালাম, দেখে নিন।<div class="time-s">১০:৪২ ✓✓</div></div>
    <div class="composer">
      <button class="back" style="border-radius:50%">＋</button>
      <div class="input">বার্তা লিখুন…</div>
      <button class="fab">➤</button>
    </div>
  </div>
</section>

<!-- ===== DYNAMIC: category + item screens ===== -->
<section class="view" id="v-dyn" hidden></section>

<!-- ===== BOTTOM NAV ===== -->
<nav class="nav" id="nav">
  <a href="#home" data-n="home"><span>⌂</span>হোম</a>
  <a href="#wallet" data-n="wallet"><span>◫</span>ওয়ালেট</a>
  <a href="#cat-comm" data-n="chat"><span>✉</span>চ্যাট</a>
  <a href="#cat-sec" data-n="profile"><span>◎</span>প্রোফাইল</a>
</nav>

</div>
<script>
const P = {
  chat:'<path d="M21 11.5a8.4 8.4 0 0 1-9 8.4 8.6 8.6 0 0 1-3.8-.9L3 21l1.9-5.1A8.4 8.4 0 1 1 21 11.5z"/>',
  call:'<path d="M22 16.9v3a2 2 0 0 1-2.2 2 19.8 19.8 0 0 1-8.6-3.1 19.5 19.5 0 0 1-6-6A19.8 19.8 0 0 1 2.1 4.2 2 2 0 0 1 4.1 2h3a2 2 0 0 1 2 1.7c.1 1 .4 1.9.7 2.8a2 2 0 0 1-.5 2.1L8 9.9a16 16 0 0 0 6 6l1.3-1.3a2 2 0 0 1 2.1-.4c.9.3 1.8.6 2.8.7a2 2 0 0 1 1.7 2z"/>',
  file:'<path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6"/>',
  group:'<path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.9M16 3.1a4 4 0 0 1 0 7.8"/>',
  send:'<path d="M22 2L11 13"/><path d="M22 2l-7 20-4-9-9-4z"/>',
  receive:'<path d="M12 19V5"/><path d="M5 12l7-7 7 7"/>',
  balance:'<path d="M3 9.5L12 4l9 5.5"/><path d="M5 10v8M19 10v8M3 20h18"/>',
  bill:'<path d="M6 2h12v20l-3-2-3 2-3-2-3 2z"/><path d="M9 8h6M9 12h6"/>',
  recharge:'<rect x="6" y="2" width="12" height="20" rx="2"/><path d="M11 18h2"/>',
  nid:'<rect x="3" y="4" width="18" height="16" rx="2"/><path d="M7 9h6M7 13h10"/>',
  passport:'<rect x="5" y="2" width="14" height="20" rx="2"/><circle cx="12" cy="10" r="2.5"/><path d="M9 16h6"/>',
  face:'<circle cx="12" cy="10" r="6"/><path d="M4 21c1.5-4 4.5-6 8-6s6.5 2 8 6"/>',
  pin:'<rect x="5" y="11" width="14" height="10" rx="2"/><path d="M8 11V7a4 4 0 0 1 8 0v4"/>',
  bio:'<path d="M6 11a6 6 0 0 1 12 0v2"/><path d="M4 13.5a8 8 0 0 1 16 0"/><path d="M9 20c.5-1.5 1-3 1-6a2 2 0 0 1 4 0c0 3 .5 5 1.5 6"/>',
  devices:'<rect x="2" y="3" width="20" height="14" rx="2"/><path d="M8 21h8M12 17v4"/>',
  loan:'<path d="M2 13l4-4 3 2 5-4 4 3 4-2"/><path d="M6 17l3 3h3a2 2 0 0 0 0-4h-2"/>',
  emi:'<circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 3"/>',
  repay:'<path d="M4 12h16M12 4l8 8-8 8"/>',
  dps:'<path d="M4 11c0-3 2.5-5 6-5h4c3.5 0 6 2 6 5v1l2 1v2l-2 .5c-.5 2-2.5 3.5-5 3.5H9l-3-2v-2"/>',
  fdr:'<path d="M3 9.5L12 4l9 5.5"/><path d="M5 10v8M9.5 10v8M14.5 10v8M19 10v8M3 20h18"/>',
  matured:'<circle cx="12" cy="12" r="9"/><path d="M8 12l3 3 5-6"/>',
  stmt:'<rect x="4" y="4" width="16" height="16" rx="2"/><path d="M8 9h8M8 13h8M8 17h5"/>',
  addbank:'<path d="M3 9.5L12 4l9 5.5"/><path d="M3 20h18M5 10v8M19 10v8"/>',
  addmfs:'<rect x="5" y="2" width="14" height="20" rx="2"/><path d="M12 6v6M9 9h6"/>',
  cashout:'<path d="M12 5v14"/><path d="M5 12l7 7 7-7"/>',
  addmoney:'<path d="M12 5v14M5 12h14"/>',
  linked:'<path d="M10 13a5 5 0 0 0 7 0l3-3a5 5 0 0 0-7-7l-1 1"/><path d="M14 11a5 5 0 0 0-7 0l-3 3a5 5 0 0 0 7 7l1-1"/>'
};
const CATS = {
 comm:{t:'যোগাযোগ',back:'home',nav:'chat',c:'green',items:[
  {k:'chat',t:'চ্যাট',s:'বন্ধু ও গ্রুপের বার্তা',i:'chat',go:'#thread'},
  {k:'call',t:'কল',s:'ভয়েস ও ভিডিও কল',i:'call',rows:[['সাম্প্রতিক কল','৩টি'],['ভিডিও কল','চালু']],b:'কল করুন'},
  {k:'file',t:'ফাইল',s:'পাঠানো ও গ্রহণকৃত ফাইল',i:'file',rows:[['মোট ফাইল','১২টি'],['মোট আকার','৪.২ MB']],b:'ফাইল পাঠান'},
  {k:'group',t:'গ্রুপ',s:'গ্রুপ তৈরি ও পরিচালনা',i:'group',rows:[['আপনার গ্রুপ','৩টি'],['মোট সদস্য','২৪ জন']],b:'নতুন গ্রুপ'}]},
 bank:{t:'মোবাইল ব্যাংকিং',back:'home',nav:'home',c:'red',items:[
  {k:'send',t:'সেন্ড মানি',s:'মোবাইল নম্বরে টাকা পাঠান',i:'send',f:[['প্রাপকের নম্বর','01XXXXXXXXX'],['পরিমাণ (৳)','৫০০']],rows:[['সেবা চার্জ','৳ ৫.০০']],b:'পাঠান'},
  {k:'cashout',t:'ক্যাশ আউট',s:'এজেন্টের কাছ থেকে টাকা তুলুন',i:'cashout',f:[['এজেন্ট নম্বর',''],['পরিমাণ (৳)','১,০০০']],rows:[['সেবা চার্জ','৳ ১৫.০০']],b:'ক্যাশ আউট করুন'},
  {k:'recharge',t:'রিচার্জ',s:'সব অপারেটরের মোবাইল রিচার্জ',i:'recharge',f:[['মোবাইল নম্বর',''],['পরিমাণ (৳)','১০০']],b:'রিচার্জ করুন'},
  {k:'addmoney',t:'এড মানি',s:'ব্যাংক বা কার্ড থেকে ওয়ালেটে টাকা যোগ করুন',i:'addmoney',f:[['উৎস (ব্যাংক/কার্ড)',''],['পরিমাণ (৳)','৫,০০০']],b:'টাকা যোগ করুন'},
  {k:'loan',t:'লোন',s:'ঋণের আবেদন ও কিস্তি',i:'loan',go:'#cat-loan'},
  {k:'receive',t:'টাকা গ্রহণ',s:'আপনার নম্বরে টাকা নিন',i:'receive',rows:[['আপনার নম্বর','01XXXXXXXXX'],['সর্বশেষ গ্রহণ','৳ ১,২০০']],b:'QR দেখান'},
  {k:'balance',t:'ব্যালেন্স',s:'বর্তমান ওয়ালেট ব্যালেন্স',i:'balance',rows:[['ওয়ালেট','৳ ২৫,০০০'],['আজকের লেনদেন','৳ ৫০০']],b:'স্টেটমেন্ট দেখুন'},
  {k:'bill',t:'বিল পরিশোধ',s:'বিদ্যুৎ, পানি, গ্যাস, ইন্টারনেট',i:'bill',f:[['গ্রাহক নম্বর','']],rows:[['বিলের ধরন','বিদ্যুৎ']],b:'বিল দিন'}]},
 id:{t:'পরিচয় যাচাই',back:'home',nav:'profile',c:'blue',items:[
  {k:'nid',t:'NID যাচাই',s:'জাতীয় পরিচয়পত্র দিয়ে',i:'nid',f:[['NID নম্বর',''],['জন্ম তারিখ','দিন / মাস / বছর']],rows:[['যাচাই অবস্থা','অপেক্ষমাণ']],b:'যাচাই করুন'},
  {k:'passport',t:'পাসপোর্ট যাচাই',s:'পাসপোর্ট নম্বর দিয়ে',i:'passport',f:[['পাসপোর্ট নম্বর',''],['জন্ম তারিখ','দিন / মাস / বছর']],b:'যাচাই করুন'},
  {k:'face',t:'Face যাচাই',s:'মুখ দিয়ে পরিচয় নিশ্চিত করুন',i:'face',rows:[['ক্যামেরা','প্রস্তুত'],['আলো','ভালো']],b:'মুখ স্ক্যান করুন'}]},
 sec:{t:'নিরাপত্তা',back:'home',nav:'profile',c:'purple',items:[
  {k:'pin',t:'PIN পরিবর্তন',s:'লেনদেনের জন্য ৫ সংখ্যার PIN',i:'pin',f:[['বর্তমান PIN',''],['নতুন PIN','']],b:'PIN পরিবর্তন'},
  {k:'bio',t:'বায়োমেট্রিক',s:'আঙুলের ছাপ ও মুখ দিয়ে লগইন',i:'bio',rows:[['আঙুলের ছাপ','চালু'],['মুখ শনাক্তকরণ','বন্ধ']],b:'সেটিং বদলান'},
  {k:'devices',t:'সক্রিয় ডিভাইস',s:'যেসব ফোনে লগইন আছে',i:'devices',rows:[['এই ফোন','সক্রিয়'],['শেষ লগইন','এখনই']],b:'ডিভাইস সরান'}]},
 loan:{t:'লোন সুবিধা',back:'wallet',nav:'wallet',c:'green',items:[
  {k:'apply',t:'লোনের আবেদন',s:'নতুন ঋণের আবেদন করুন',i:'loan',f:[['কত টাকা লাগবে (৳)','২০,০০০'],['মেয়াদ (মাস)','১২']],b:'আবেদন করুন'},
  {k:'emi',t:'কিস্তি',s:'পরবর্তী কিস্তির তথ্য',i:'emi',rows:[['পরবর্তী কিস্তি','৳ ১,৮০০'],['কিস্তির তারিখ','৫ ডিসেম্বর']],b:'কিস্তি দেখুন'},
  {k:'repay',t:'পরিশোধ',s:'বাকি ও পরিশোধের বিবরণ',i:'repay',rows:[['মোট বাকি','৳ ১৮,০০০'],['পরিশোধিত','৳ ২,০০০']],b:'এখন পরিশোধ'}]},
 dps:{t:'DPS সুবিধা',back:'wallet',nav:'wallet',c:'red',items:[
  {k:'open',t:'নতুন DPS',s:'মাসিক সঞ্চয় শুরু করুন',i:'dps',f:[['মাসিক কিস্তি (৳)','১,০০০'],['মেয়াদ (মাস)','১২']],b:'DPS খুলুন'},
  {k:'pay',t:'মাসিক জমা',s:'এই মাসের কিস্তি জমা দিন',i:'emi',rows:[['এই মাসের কিস্তি','৳ ১,০০০'],['স্বয়ংক্রিয় কর্তন','৫ তারিখ']],b:'এখনই জমা দিন'},
  {k:'stmt',t:'বিবরণ',s:'মোট জমা ও পরিপক্কতা',i:'stmt',rows:[['মোট জমা','৳ ৬,০০০'],['পরিপক্কতা','১২ মাস পর']],b:'বিবরণ দেখুন'}]},
 fdr:{t:'FDR সুবিধা',back:'wallet',nav:'wallet',c:'blue',items:[
  {k:'open',t:'নতুন FDR',s:'নির্দিষ্ট মেয়াদে আমানত রাখুন',i:'fdr',f:[['আমানত (৳)','১০,০০০'],['মেয়াদ','৬ মাস']],rows:[['বার্ষিক সুদ','৭.৫০%']],b:'FDR খুলুন'},
  {k:'matured',t:'পরিপক্ক FDR',s:'মেয়াদ শেষের তালিকা',i:'matured',rows:[['পরিপক্ক তারিখ','১৫ মে ২০২৭'],['সুদ','৳ ৩৭৫']],b:'নবায়ন করুন'},
  {k:'stmt',t:'বিবরণ',s:'সব FDR-এর হিসাব',i:'stmt',rows:[['মোট আমানত','৳ ১০,০০০'],['সক্রিয় FDR','১টি']],b:'বিবরণ দেখুন'}]},
 mfs:{t:'অন্যান্য ব্যাংক ও MFS',back:'wallet',nav:'wallet',c:'purple',items:[
  {k:'addbank',t:'ব্যাংক যুক্ত করুন',s:'অনুমোদিত ব্যাংক হিসাব',i:'addbank',f:[['ব্যাংক বেছে নিন',''],['অ্যাকাউন্ট নম্বর','']],b:'যুক্ত করুন'},
  {k:'addmfs',t:'MFS যুক্ত করুন',s:'মোবাইল ফাইন্যান্সিয়াল সার্ভিস',i:'addmfs',f:[['MFS প্রদানকারী',''],['মোবাইল নম্বর','']],b:'যুক্ত করুন'},
  {k:'linked',t:'যুক্ত হিসাব',s:'সব সংযোগের তালিকা',i:'linked',rows:[['যুক্ত ব্যাংক','১টি'],['যুক্ত MFS','১টি']],b:'তালিকা দেখুন'}]}
};
const C_CLS = {green:['var(--green-soft)','var(--green)'],red:['var(--red-soft)','var(--red)'],blue:['var(--blue-soft)','var(--blue)'],purple:['var(--purple-soft)','var(--purple)']};
const CYC = ['green','red','blue','purple'];
const ico = (k,c)=>`<div class="ibox" style="background:${C_CLS[c][0]};color:${C_CLS[c][1]}"><svg class="svg sm" viewBox="0 0 24 24">${P[k]}</svg></div>`;

function renderCat(key){
  const cat = CATS[key];
  const rows = cat.items.map((it,idx)=>{
    const c = CYC[idx%4];
    const href = it.go || `#item-${key}-${it.k}`;
    return `<a href="${href}" class="row">${ico(it.i,c)}<div class="meta"><b>${it.t}</b><span>${it.s}</span></div><span class="chev">›</span></a>`;
  }).join('');
  return `<div class="topbar"><a class="back" href="#${cat.back}">‹</a><h2>${cat.t}</h2></div>
    <div class="card">${rows}</div>`;
}
function renderItem(key,k){
  const cat = CATS[key]; const it = cat.items.find(x=>x.k===k);
  const fields = (it.f||[]).map(([l,v])=>`<div class="field"><label>${l}</label><input value="${v}"></div>`).join('');
  const kv = (it.rows||[]).map(([l,v])=>`<div class="kv"><span class="muted">${l}</span><span>${v}</span></div>`).join('');
  return `<div class="topbar"><a class="back" href="#cat-${key}">‹</a><h2>${it.t}</h2></div>
    <div class="card plain" style="display:flex;gap:12px;align-items:center">${ico(it.i,cat.c)}<div><b style="font-size:15px">${it.t}</b><div class="muted">${it.s}</div></div></div>
    <div class="card plain">${fields}${kv}</div>
    <button class="btn">${it.b}</button>`;
}

function show(){
  const h = location.hash.slice(1) || 'home';
  const dyn = document.getElementById('v-dyn');
  let nav = 'home', mainShow = null;
  if (h === 'home' || h === 'wallet' || h === 'thread') {
    mainShow = 'v-' + h; nav = {home:'home',wallet:'wallet',thread:'chat'}[h];
    dyn.hidden = true;
  } else if (h.startsWith('cat-') && CATS[h.slice(4)]) {
    const key = h.slice(4); nav = CATS[key].nav;
    dyn.innerHTML = renderCat(key); dyn.hidden = false;
  } else if (h.startsWith('item-')) {
    const [, key, k] = h.split('-');
    if (CATS[key] && CATS[key].items.find(x=>x.k===k)) { nav = CATS[key].nav; dyn.innerHTML = renderItem(key,k); dyn.hidden = false; }
  } else { mainShow = 'v-home'; dyn.hidden = true; }
  if (!mainShow && dyn.hidden) mainShow = 'v-home';
  ['v-home','v-wallet','v-thread'].forEach(id => document.getElementById(id).hidden = id !== mainShow);
  if (!dyn.hidden) ['v-home','v-wallet','v-thread'].forEach(id => document.getElementById(id).hidden = true);
  document.querySelectorAll('#nav a').forEach(a => a.classList.toggle('on', a.dataset.n === nav));
  document.getElementById('nav').hidden = (h === 'thread');
  window.scrollTo(0,0);
}
window.addEventListener('hashchange', show);
show();
</script>
</body>
</html>
