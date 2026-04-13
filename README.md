# -10-8-12
<!DOCTYPE html>

<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>迪士尼冒險號 · 16123 號房</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Noto+Serif+TC:wght@600;700&family=Noto+Sans+TC:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root{
  --gold:#F5C842;--gold-dk:#C9A227;--navy:#0B1E3D;--navy-m:#142852;--navy-l:#1E3A6E;
  --sky:#1A6BAA;--ocean:#0D4F8A;--cream:#FFF8EE;--teal:#2EC4B6;--red:#D62828;
  --coral:#FF6B35;--txt-dim:rgba(255,248,238,0.55);
}
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Noto Sans TC',sans-serif;background:var(--navy);color:var(--cream);min-height:100vh;overflow-x:hidden}

/* ── HEADER ── */
header{background:linear-gradient(160deg,#0B1E3D 0%,#142852 40%,#0D4F8A 100%);text-align:center;border-bottom:3px solid var(–gold);position:relative;overflow:hidden}
header::before{content:’’;position:absolute;inset:0;background:url(“data:image/svg+xml,%3Csvg width=‘60’ height=‘60’ viewBox=‘0 0 60 60’ xmlns=‘http://www.w3.org/2000/svg’%3E%3Cg fill=’%23F5C842’ fill-opacity=‘0.04’%3E%3Cpath d=‘M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z’/%3E%3C/g%3E%3C/svg%3E”);pointer-events:none}
.hi{position:relative;z-index:1;padding:26px 20px 18px}
.ship-e{font-size:2.5rem;display:block;margin-bottom:5px;animation:float 3s ease-in-out infinite}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-7px)}}
header h1{font-family:‘Playfair Display’,serif;font-size:clamp(1.6rem,5vw,2.3rem);font-weight:900;color:var(–gold);text-shadow:0 2px 20px rgba(245,200,66,.4)}
header p{font-size:.76rem;color:var(–txt-dim);margin-top:4px;letter-spacing:.1em;text-transform:uppercase}
.room-badge{display:inline-block;margin-top:8px;background:rgba(245,200,66,.18);border:1px solid rgba(245,200,66,.4);border-radius:20px;padding:4px 14px;font-size:.8rem;color:var(–gold);font-weight:700;letter-spacing:.05em}

/* ── NAV ── */
nav{display:flex;background:var(–navy-m);border-bottom:2px solid rgba(245,200,66,.15);overflow-x:auto;scrollbar-width:none;position:sticky;top:0;z-index:100}
nav::-webkit-scrollbar{display:none}
nav button{flex:1;min-width:58px;padding:10px 5px 8px;background:none;border:none;color:var(–txt-dim);font-family:‘Noto Sans TC’,sans-serif;font-size:.66rem;cursor:pointer;border-bottom:3px solid transparent;transition:all .22s;white-space:nowrap;display:flex;flex-direction:column;align-items:center;gap:3px}
nav button .ti{font-size:1.15rem}
nav button.active{color:var(–gold);border-bottom-color:var(–gold);background:rgba(245,200,66,.06)}
nav button:hover:not(.active){color:var(–cream)}

/* ── SECTIONS ── */
section{display:none;padding:16px 13px 50px;animation:fi .28s ease}
section.active{display:block}
@keyframes fi{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}
.sec-title{font-family:‘Playfair Display’,serif;font-size:1.38rem;color:var(–gold);margin-bottom:3px}
.sec-sub{font-size:.73rem;color:var(–txt-dim);margin-bottom:16px;letter-spacing:.04em}

/* ── CARD ── */
.card{background:linear-gradient(135deg,rgba(20,40,82,.95),rgba(13,79,138,.32));border:1px solid rgba(245,200,66,.17);border-radius:13px;margin-bottom:13px;overflow:hidden;transition:border-color .2s,transform .17s;cursor:pointer}
.card:hover{border-color:rgba(245,200,66,.44);transform:translateY(-2px)}
.card-hd{display:flex;align-items:center;gap:11px;padding:13px}
.cbadge{width:46px;height:46px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.4rem;flex-shrink:0}
.ci{flex:1}
.ci h3{font-family:‘Noto Serif TC’,serif;font-size:.9rem;font-weight:700;color:var(–cream);margin-bottom:1px}
.ci p{font-size:.68rem;color:var(–txt-dim)}
.cmeta{display:flex;gap:5px;flex-wrap:wrap;margin-top:4px}
.tag{font-size:.62rem;padding:2px 7px;border-radius:18px;font-weight:500;letter-spacing:.03em}
.tloc{background:rgba(46,196,182,.2);color:#1fffe6;border:1px solid rgba(46,196,182,.3)}
.ttime{background:rgba(245,200,66,.15);color:var(–gold);border:1px solid rgba(245,200,66,.25)}
.ttype{background:rgba(214,40,40,.2);color:#ff8080;border:1px solid rgba(214,40,40,.3)}
.tincl{background:rgba(46,196,182,.15);color:#1fffe6;border:1px solid rgba(46,196,182,.25)}
.tpaid{background:rgba(255,107,53,.15);color:#ffaa70;border:1px solid rgba(255,107,53,.25)}
.thalal{background:rgba(100,200,100,.15);color:#90f090;border:1px solid rgba(100,200,100,.25)}
.tadult{background:rgba(160,80,200,.15);color:#d090ff;border:1px solid rgba(160,80,200,.25)}
.tdeck{background:rgba(30,120,200,.2);color:#80d0ff;border:1px solid rgba(30,120,200,.3)}
.tarr{font-size:.82rem;color:rgba(255,248,238,.3);transition:transform .22s;flex-shrink:0}
.card.open .tarr{transform:rotate(180deg)}
.card-body{display:none;padding:0 13px 13px;border-top:1px solid rgba(245,200,66,.1);animation:fi .2s ease}
.card.open .card-body{display:block}
.cdesc{font-size:.78rem;color:rgba(255,248,238,.82);line-height:1.7;margin:9px 0}
.ctip{background:rgba(245,200,66,.08);border-left:3px solid var(–gold);border-radius:0 7px 7px 0;padding:9px 11px;margin-top:8px}
.ctip p{font-size:.74rem;color:rgba(255,248,238,.85);line-height:1.6}
.ctip strong{color:var(–gold)}

/* ── SCHEDULE TABLE ── */
.sch-table{width:100%;border-collapse:collapse;margin:9px 0;font-size:.72rem}
.sch-table th{background:rgba(245,200,66,.15);color:var(–gold);padding:6px 8px;text-align:left;font-weight:600}
.sch-table td{padding:6px 8px;border-bottom:1px solid rgba(255,255,255,.05);color:rgba(255,248,238,.85);vertical-align:top}
.sch-table tr:last-child td{border-bottom:none}
.sch-note{font-size:.68rem;color:var(–txt-dim);margin-top:5px;font-style:italic}

/* ── MENU ── */
.mh{font-family:‘Playfair Display’,serif;font-size:.85rem;color:var(–gold);margin:9px 0 5px}
.mi{display:flex;justify-content:space-between;align-items:flex-start;padding:6px 0;border-bottom:1px solid rgba(255,255,255,.05)}
.mi:last-child{border-bottom:none}
.min{font-size:.78rem;color:var(–cream);font-weight:500}
.mid{font-size:.68rem;color:var(–txt-dim);margin-top:1px}
.mibadge{font-size:.6rem;padding:2px 5px;border-radius:9px;flex-shrink:0;margin-left:6px;margin-top:2px}
.bv{background:rgba(100,200,100,.2);color:#90f090}
.bh{background:rgba(100,200,100,.2);color:#90f090}
.bs{background:rgba(255,107,53,.2);color:#ffaa70}

/* ── CAT TABS ── */
.cat-tabs{display:flex;gap:6px;overflow-x:auto;scrollbar-width:none;padding-bottom:11px;margin-bottom:4px}
.cat-tabs::-webkit-scrollbar{display:none}
.cbt{flex-shrink:0;padding:6px 11px;background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.1);border-radius:18px;color:rgba(255,248,238,.6);font-size:.74rem;font-family:‘Noto Sans TC’,sans-serif;cursor:pointer;transition:all .2s;white-space:nowrap}
.cbt.active{background:rgba(245,200,66,.15);border-color:var(–gold);color:var(–gold)}
.clist{display:none}
.clist.active{display:block}

/* ── NOTES – LIGHT BG = DARK TEXT, DARK BG = LIGHT TEXT ── */
.ng{margin-bottom:20px}
.ngt{font-family:‘Playfair Display’,serif;font-size:.96rem;color:var(–gold);margin-bottom:8px;display:flex;align-items:center;gap:7px}
.ni{display:flex;gap:8px;align-items:flex-start;border-radius:10px;padding:10px 12px;margin-bottom:6px}
.ni-icon{font-size:1rem;flex-shrink:0;margin-top:1px}

/* dark background cards – light text */
.ni.dark{background:rgba(20,40,82,.8);border:1px solid rgba(255,255,255,.08)}
.ni.dark .ni-text{font-size:.77rem;color:rgba(255,248,238,.85);line-height:1.65}
.ni.dark .ni-text strong{color:var(–cream)}

/* light background variants – dark text (rule #4 fix) */
.ni.alert{background:#ffe8e8;border:1px solid #f8aaaa}
.ni.alert .ni-text{font-size:.77rem;color:#5a0000;line-height:1.65}
.ni.alert .ni-text strong{color:#3a0000;font-weight:700}

.ni.tip{background:#fffbe0;border:1px solid #e8d060}
.ni.tip .ni-text{font-size:.77rem;color:#4a3800;line-height:1.65}
.ni.tip .ni-text strong{color:#2a1e00;font-weight:700}

.ni.info{background:#e4f7f5;border:1px solid #80ddd8}
.ni.info .ni-text{font-size:.77rem;color:#003330;line-height:1.65}
.ni.info .ni-text strong{color:#001c1a;font-weight:700}

.ni.warn{background:#fff0d8;border:1px solid #e8b840}
.ni.warn .ni-text{font-size:.77rem;color:#4a2800;line-height:1.65}
.ni.warn .ni-text strong{color:#2a1200;font-weight:700}

/* remark box */
.rn{margin-top:8px;background:rgba(245,200,66,.07);border-left:3px solid var(–gold);border-radius:0 6px 6px 0;padding:7px 10px;font-size:.71rem;color:rgba(255,248,238,.78);line-height:1.6}

/* prohibited grid */
.proh-grid{display:grid;grid-template-columns:1fr 1fr;gap:6px;margin-top:7px}
.proh-item{background:#ffe8e8;border:1px solid #f8aaaa;border-radius:8px;padding:7px 9px;display:flex;gap:6px;align-items:flex-start}
.proh-item .pi-icon{font-size:1rem;flex-shrink:0}
.proh-item .pi-text{font-size:.7rem;color:#5a0000;font-weight:500;line-height:1.4}

/* ── OVERVIEW / DECK PLAN ── */
.ov-info-grid{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:14px}
.ov-card{background:rgba(20,40,82,.85);border:1px solid rgba(245,200,66,.2);border-radius:12px;padding:13px}
.ov-card .oc-icon{font-size:1.5rem;margin-bottom:5px;display:block}
.ov-card h4{font-family:‘Playfair Display’,serif;font-size:.85rem;color:var(–gold);margin-bottom:5px}
.ov-card p,.ov-card li{font-size:.72rem;color:rgba(255,248,238,.8);line-height:1.6}
.ov-card ul{padding-left:14px}
.ov-card.full{grid-column:1/-1}

/* deck plan SVG table */
.deck-wrap{background:rgba(10,20,50,.9);border:1px solid rgba(245,200,66,.2);border-radius:12px;overflow:hidden;margin-bottom:14px}
.deck-hdr{background:rgba(245,200,66,.12);padding:10px 14px;display:flex;justify-content:space-between;align-items:center}
.deck-hdr h4{font-family:‘Playfair Display’,serif;font-size:.95rem;color:var(–gold)}
.deck-hdr span{font-size:.68rem;color:var(–txt-dim)}
.deck-rows{padding:4px 0}
.deck-row{display:flex;align-items:flex-start;gap:0;border-bottom:1px solid rgba(255,255,255,.05);transition:background .15s}
.deck-row:last-child{border-bottom:none}
.deck-row:hover{background:rgba(245,200,66,.05)}
.deck-num{min-width:52px;padding:9px 8px;text-align:center;font-family:‘Playfair Display’,serif;font-weight:700;font-size:.95rem;border-right:2px solid rgba(245,200,66,.2);flex-shrink:0}
.deck-num.highlight{color:var(–gold)}
.deck-num.myroom{color:#ff80ff;background:rgba(200,50,200,.15)}
.deck-content{padding:8px 10px;flex:1}
.deck-zone{font-size:.7rem;color:var(–gold);font-weight:600;margin-bottom:2px;opacity:.8}
.deck-items{font-size:.7rem;color:rgba(255,248,238,.75);line-height:1.6}
.deck-items .item-pill{display:inline-block;background:rgba(255,255,255,.07);border-radius:4px;padding:1px 5px;margin:1px 2px 1px 0;font-size:.63rem}
.deck-items .item-pill.dining{background:rgba(245,200,66,.12);color:var(–gold)}
.deck-items .item-pill.show{background:rgba(214,40,40,.15);color:#ff8080}
.deck-items .item-pill.shop{background:rgba(80,160,255,.12);color:#80c8ff}
.deck-items .item-pill.ride{background:rgba(100,220,100,.12);color:#90ee90}
.deck-items .item-pill.kids{background:rgba(255,160,50,.12);color:#ffb860}
.deck-items .item-pill.spa{background:rgba(200,100,200,.15);color:#e080e0}
.deck-items .item-pill.myroom{background:rgba(200,50,200,.15);color:#ff80ff;font-weight:700}
.deck-items .item-pill.con{background:rgba(245,200,66,.2);color:var(–gold);font-weight:600}

/* ── CURRENCY ── */
.fx-card{background:linear-gradient(135deg,rgba(20,40,82,.9),rgba(13,79,138,.3));border:1px solid rgba(245,200,66,.25);border-radius:13px;padding:16px;margin-bottom:13px}
.fx-card h3{font-family:‘Playfair Display’,serif;color:var(–gold);font-size:.95rem;margin-bottom:4px}
.fx-card p{font-size:.73rem;color:var(–txt-dim);margin-bottom:11px;line-height:1.6}
.fx-input{padding:9px 11px;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.15);border-radius:9px;color:var(–cream);font-size:.95rem;font-family:‘Noto Sans TC’,sans-serif;outline:none;width:100%}
.fx-input:focus{border-color:var(–gold)}
.fx-sel{padding:9px 11px;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.15);border-radius:9px;color:var(–cream);font-size:.82rem;font-family:‘Noto Sans TC’,sans-serif;outline:none;cursor:pointer;flex-shrink:0}
.fx-sel option{background:#142852}
.fx-results{display:grid;grid-template-columns:1fr 1fr;gap:7px;margin-top:11px}
.fx-res-item{background:rgba(20,40,82,.8);border:1px solid rgba(255,255,255,.08);border-radius:9px;padding:10px 12px}
.fx-res-item .flag{font-size:1.3rem;margin-bottom:2px}
.fx-res-item .cname{font-size:.65rem;color:var(–txt-dim)}
.fx-res-item .cval{font-size:1.05rem;font-weight:700;color:var(–cream);margin-top:2px}
.btn-gold{padding:9px 14px;background:var(–gold);color:#0B1E3D;border:none;border-radius:9px;font-family:‘Noto Sans TC’,sans-serif;font-size:.78rem;font-weight:700;cursor:pointer;transition:background .2s,transform .14s;flex:1;text-align:center}
.btn-gold:hover{background:#e0b330;transform:translateY(-1px)}
.btn-sec{background:rgba(255,255,255,.07);color:var(–cream);border:1px solid rgba(255,255,255,.15)}
.btn-sec:hover{background:rgba(255,255,255,.13)}
.fx-row{display:flex;gap:7px;margin-bottom:9px;align-items:center}
.fx-update{display:flex;gap:7px;flex-wrap:wrap;margin-top:9px}
.fx-status{font-size:.68rem;color:var(–txt-dim);text-align:center;margin-top:5px}
.fx-status.ok{color:var(–teal)}
.fx-status.err{color:#ff8080}

/* manual inputs light bg */
.manual-row{display:flex;align-items:center;gap:8px;margin-bottom:7px}
.manual-lbl{background:#e8f4e8;border:1px solid #80cc80;border-radius:8px;padding:6px 10px;min-width:70px;font-size:.78rem;color:#1a3a1a;font-weight:600;text-align:center}
.manual-input{flex:1;padding:8px 10px;background:#f8fdf8;border:1px solid #80cc80;border-radius:8px;font-size:.9rem;color:#1a3a1a;outline:none;font-family:‘Noto Sans TC’,sans-serif}
.manual-input:focus{border-color:#3a8a3a}
.manual-panel{background:#f0f8f0;border:1px solid #80cc80;border-radius:11px;padding:14px;margin-bottom:10px}
.manual-panel h3{font-size:.9rem;color:#1a3a1a;margin-bottom:3px;font-family:‘Playfair Display’,serif}
.manual-panel p{font-size:.72rem;color:#3a5a3a;margin-bottom:11px;line-height:1.6}
.btn-apply{padding:9px 14px;background:#2a7a2a;color:#fff;border:none;border-radius:9px;font-family:‘Noto Sans TC’,sans-serif;font-size:.8rem;font-weight:700;cursor:pointer;width:100%;margin-top:6px}
.btn-apply:hover{background:#1a6a1a}
.twdlink{display:inline-flex;align-items:center;gap:5px;background:#c00000;color:#fff;border-radius:8px;padding:7px 12px;font-size:.76rem;text-decoration:none;font-weight:600;margin-top:7px;width:100%;justify-content:center}
.twdlink:hover{background:#a00000}

/* translate */
.tr-card{background:linear-gradient(135deg,rgba(20,40,82,.9),rgba(13,79,138,.3));border:1px solid rgba(245,200,66,.25);border-radius:13px;padding:16px;margin-bottom:13px}
.tr-card h3{font-family:‘Playfair Display’,serif;color:var(–gold);font-size:.95rem;margin-bottom:4px}
.tr-card p{font-size:.73rem;color:var(–txt-dim);line-height:1.6;margin-bottom:11px}
.tr-btn{display:flex;align-items:center;gap:8px;background:var(–gold);color:#0B1E3D;border:none;border-radius:10px;padding:10px 14px;font-family:‘Noto Sans TC’,sans-serif;font-size:.8rem;font-weight:700;cursor:pointer;width:100%;justify-content:center;transition:background .2s,transform .14s;text-decoration:none;margin-bottom:6px}
.tr-btn:hover{background:#e0b330;transform:translateY(-1px)}
.tr-btn.sec{background:rgba(255,255,255,.07);color:var(–cream);border:1px solid rgba(255,255,255,.15)}
.tr-btn.sec:hover{background:rgba(255,255,255,.12)}
.phrase-item{display:flex;justify-content:space-between;align-items:center;padding:8px 12px;background:rgba(20,40,82,.7);border:1px solid rgba(255,255,255,.06);border-radius:9px;margin-bottom:5px;cursor:pointer;transition:border-color .2s}
.phrase-item:hover{border-color:rgba(245,200,66,.3)}
.pzh{font-size:.8rem;color:var(–cream);font-weight:500}
.pen{font-size:.68rem;color:var(–txt-dim);margin-top:1px}
.pcopy{font-size:.64rem;color:rgba(245,200,66,.6);padding:3px 6px;background:rgba(245,200,66,.1);border-radius:5px;flex-shrink:0}
.pok{color:var(–teal)}

.divider{border:none;border-top:1px solid rgba(255,255,255,.08);margin:16px 0}
::-webkit-scrollbar{width:4px}
::-webkit-scrollbar-track{background:transparent}
::-webkit-scrollbar-thumb{background:rgba(245,200,66,.3);border-radius:2px}
</style>

</head>
<body>

<header>
  <div class="hi">
    <span class="ship-e">🚢</span>
    <h1>迪士尼冒險號</h1>
    <p>Disney Adventure · 新加坡 · 2026</p>
    <div class="room-badge">🛏️ 房號 16123 · Deck 16 禮賓陽台房</div>
  </div>
</header>

<nav id="mainnav">
  <button class="active" onclick="switchTab('overview')"><span class="ti">🏠</span>概要</button>
  <button onclick="switchTab('shows')"><span class="ti">🎭</span>演出</button>
  <button onclick="switchTab('dining')"><span class="ti">🍽️</span>餐廳</button>
  <button onclick="switchTab('roomsvc')"><span class="ti">🛎️</span>客房點餐</button>
  <button onclick="switchTab('concierge')"><span class="ti">👑</span>禮賓</button>
  <button onclick="switchTab('chars')"><span class="ti">🌟</span>角色見面</button>
  <button onclick="switchTab('shops')"><span class="ti">🛍️</span>商店</button>
  <button onclick="switchTab('notes')"><span class="ti">📋</span>注意</button>
  <button onclick="switchTab('currency')"><span class="ti">💱</span>匯率</button>
  <button onclick="switchTab('translate')"><span class="ti">🌐</span>翻譯</button>
</nav>

<!-- ═══════════════════════════════════
     1. OVERVIEW
═══════════════════════════════════ -->

<section id="overview" class="active">
  <div class="sec-title">🏠 航程概要</div>
  <div class="sec-sub">房號 16123 · Deck 16 禮賓陽台房</div>

  <!-- Key info grid -->

  <div class="ov-info-grid">
    <div class="ov-card">
      <span class="oc-icon">🛏️</span>
      <h4>我的房間</h4>
      <p><strong style="color:var(--gold)">房號：16123</strong><br>Deck 16 · 禮賓陽台房<br>可俯瞰 Wayfinder Bay<br>樓層貼近禮賓廳 (Deck 15)</p>
    </div>
    <div class="ov-card">
      <span class="oc-icon">⚓</span>
      <h4>出發資訊</h4>
      <p>Marina Bay Cruise Centre<br>61 Marina Coastal Dr<br>3夜：週一出發 4PM<br>4夜：週四出發 4PM</p>
    </div>
    <div class="ov-card full">
      <span class="oc-icon">🚌</span>
      <h4>前往港口交通方式</h4>
      <ul>
        <li>🚕 <strong>計程車 / Grab</strong>：從市區約 15–20 分鐘，費用 SGD $20–30（最方便）</li>
        <li>🚇 <strong>MRT</strong>：搭到 Bayfront 站 (CE1/DT16) → 步行或轉 City Direct 巴士約 15 分鐘（費用低）</li>
        <li>🚌 <strong>巴士</strong>：400 路至 Marina South Pier → 步行約 10 分鐘</li>
        <li>✈️ <strong>從樟宜機場</strong>：計程車約 25 分鐘，SGD $30–40</li>
        <li>🅿️ <strong>自駕</strong>：港口附近有停車場，約 SGD $3/小時</li>
      </ul>
    </div>
    <div class="ov-card full">
      <span class="oc-icon">👑</span>
      <h4>禮賓客報到流程</h4>
      <ul>
        <li>📌 建議 <strong>出發前 2 小時</strong>抵達（一般旅客 11AM，禮賓客更早）</li>
        <li>⭐ 禮賓客有<strong>專屬報到通道</strong>，免排一般隊伍，速度快很多</li>
        <li>🏛️ 登船後直接前往 <strong>禮賓廳 (Deck 15)</strong>，禮賓人員協助您完成所有當日預訂</li>
        <li>📱 登船前請先下載 <strong>Disney Navigator App</strong> 並完成線上報到（Online Check-in）</li>
        <li>📄 攜帶：護照、訂房確認信、線上報到完成憑證</li>
        <li>🎭 安全演習後立即開放熱門活動搶訂，請提前想好要訂什麼！</li>
      </ul>
    </div>
  </div>

  <!-- Deck Plan -->

  <div class="deck-wrap">
    <div class="deck-hdr">
      <h4>🗺️ 船層平面圖（Deck Plan）</h4>
      <span>共19層，無第14層</span>
    </div>
    <div class="deck-rows">

```
  <div class="deck-row">
    <div class="deck-num" style="color:#80c8ff">20</div>
    <div class="deck-content">
      <div class="deck-zone">頂層觀景</div>
      <div class="deck-items">
        <span class="item-pill">露天觀景台</span>
        <span class="item-pill show">🦁 煙火秀觀賞區</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#90ee90">19</div>
    <div class="deck-content">
      <div class="deck-zone">⚡ Marvel Landing</div>
      <div class="deck-items">
        <span class="item-pill ride">🎢 Ironcycle Test Run（雲霄飛車）</span>
        <span class="item-pill ride">🏎️ Pym Quantum Racers</span>
        <span class="item-pill ride">🌀 Groot Galaxy Spin</span>
        <span class="item-pill">Tony Stark 無邊際泳池</span>
        <span class="item-pill shop">💈 Marvel Style Studio</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#90ee90">18</div>
    <div class="deck-content">
      <div class="deck-zone">禮賓皇家套房</div>
      <div class="deck-items">
        <span class="item-pill con">❄️ 艾莎皇家套房 18100</span>
        <span class="item-pill con">🌸 安娜皇家套房 18200</span>
        <span class="item-pill spa">💆 Spa 設施延伸</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#F5C842">17</div>
    <div class="deck-content">
      <div class="deck-zone">🧸 Toy Story Place + Lido Deck</div>
      <div class="deck-items">
        <span class="item-pill">Sunnyside 家庭泳池</span>
        <span class="item-pill">Woody & Jessie's 水滑梯</span>
        <span class="item-pill">Flying Saucer 噴水區</span>
        <span class="item-pill dining">🌸 Pixar Market Restaurant（Deck 17 AFT）</span>
        <span class="item-pill dining">🍕 Pizza Planet</span>
        <span class="item-pill dining">🍦 Wheezy's Freezies（免費冰淇淋至午夜）</span>
        <span class="item-pill">Market Bar</span>
      </div>
    </div>
  </div>

  <div class="deck-row" style="background:rgba(180,50,180,.07)">
    <div class="deck-num myroom">16</div>
    <div class="deck-content">
      <div class="deck-zone" style="color:#ff80ff">🌊 Wayfinder Bay + <span style="color:#ff80ff">★ 房號 16123 在此層</span></div>
      <div class="deck-items">
        <span class="item-pill myroom">🏠 16123（禮賓陽台房）</span>
        <span class="item-pill">Wayfinder Bay（莫娜主題池）</span>
        <span class="item-pill">涉水池 + 躺椅區</span>
        <span class="item-pill">Wayfinder Bar</span>
        <span class="item-pill show">🌊 莫娜: 海洋呼喚（戶外舞台）</span>
        <span class="item-pill show">🦁 最佳煙火觀賞位置</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:var(--gold)">15</div>
    <div class="deck-content">
      <div class="deck-zone">👑 禮賓層 + Senses Spa</div>
      <div class="deck-items">
        <span class="item-pill con">🏛️ 禮賓廳（Concierge Lounge）</span>
        <span class="item-pill con">☀️ 禮賓私人露台（含飲品吧）</span>
        <span class="item-pill spa">💆 Senses Spa & Salon</span>
        <span class="item-pill shop">💎 Palace Treasures（禮賓精品）</span>
        <span class="item-pill shop">🌟 3 Wishes（禮賓限定）</span>
        <span class="item-pill">禮賓健身中心</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#80c8ff">13</div>
    <div class="deck-content">
      <div class="deck-zone">禮賓客艙 + 船橋</div>
      <div class="deck-items">
        <span class="item-pill con">禮賓陽台客房</span>
        <span class="item-pill">船橋（不對旅客開放）</span>
      </div>
    </div>
  </div>

  <div class="deck-row" style="background:rgba(80,80,80,.12)">
    <div class="deck-num" style="color:rgba(255,255,255,.25)">14</div>
    <div class="deck-content">
      <div class="deck-zone" style="color:rgba(255,255,255,.3)">（跳過此層 — 亞洲文化中 14 為不吉利數字）</div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#80c8ff">12</div>
    <div class="deck-content">
      <div class="deck-zone">客艙層（安靜）</div>
      <div class="deck-items">
        <span class="item-pill">內部/海景客艙</span>
        <span class="item-pill">無主要公共設施（動感最小層）</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#80c8ff">11</div>
    <div class="deck-content">
      <div class="deck-zone">🏙️ San Fransokyo Street（Big Hero 6）</div>
      <div class="deck-items">
        <span class="item-pill">電玩遊戲區</span>
        <span class="item-pill kids">🎮 Edge（11–14歲少年俱樂部）</span>
        <span class="item-pill kids">🎯 Vibe（青少年俱樂部）</span>
        <span class="item-pill">特色商店</span>
        <span class="item-pill">Hiro Training Zone</span>
        <span class="item-pill">🎬 戲院（電影放映）</span>
        <span class="item-pill dining">🧋 Bewitching Boba & Brews</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#F5C842">10</div>
    <div class="deck-content">
      <div class="deck-zone">🐠 Disney Discovery Reef（Little Mermaid / Nemo / Luca）</div>
      <div class="deck-items">
        <span class="item-pill dining">🇮🇹 Palo Trattoria（付費、成人）</span>
        <span class="item-pill dining">☕ Palo Café（付費）</span>
        <span class="item-pill dining">👾 Mike & Sulley's</span>
        <span class="item-pill dining">🏝️ Stitch's 'Ohana Grill</span>
        <span class="item-pill shop">特色商店</span>
        <span class="item-pill">Reef View 景觀客艙</span>
        <span class="item-pill">Guest Relations 旅客服務 (Deck 6)</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#ff8080">9</div>
    <div class="deck-content">
      <div class="deck-zone">🏰 Town Square（Princess 主題）</div>
      <div class="deck-items">
        <span class="item-pill show">🎭 Walt Disney Theatre（Remember / Disney Seas 演出）</span>
        <span class="item-pill dining">🎨 Animator's Table</span>
        <span class="item-pill shop">👗 Bibbidi Bobbidi Boutique（公主造型）</span>
        <span class="item-pill dining">🔮 Spellbound（酒吧）</span>
        <span class="item-pill dining">🧿 Tiana's Bayou Lounge</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#ff8080">8</div>
    <div class="deck-content">
      <div class="deck-zone">✨ 想像花園（上層）+ Town Square</div>
      <div class="deck-items">
        <span class="item-pill dining">🎬 Hollywood Spotlight Club</span>
        <span class="item-pill">Garden View 陽台客艙</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#ff8080">7</div>
    <div class="deck-content">
      <div class="deck-zone">✨ 想像花園（中層）</div>
      <div class="deck-items">
        <span class="item-pill kids">🎠 Disney Oceaneer Club（3–10歲）</span>
        <span class="item-pill">Garden View 客艙</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#ff8080">6</div>
    <div class="deck-content">
      <div class="deck-zone">🌿 Disney Imagination Garden（核心）</div>
      <div class="deck-items">
        <span class="item-pill show">⭐ Garden Stage（復仇者集結/啟航秀等戶外演出）</span>
        <span class="item-pill">3層高繪本城堡</span>
        <span class="item-pill dining">🍛 Mowgli's Eatery</span>
        <span class="item-pill dining">🌺 Gramma Tala's Kitchen</span>
        <span class="item-pill dining">⚓ Navigator's Club</span>
        <span class="item-pill dining">🌸 Enchanted Summer Restaurant</span>
        <span class="item-pill shop">🌍 World of Disney（旗艦店）</span>
        <span class="item-pill shop">🐻 Duffy & Friends Shop</span>
        <span class="item-pill shop">🌿 National Geographic Store</span>
        <span class="item-pill">Guest Relations（旅客服務）</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:#80c8ff">5</div>
    <div class="deck-content">
      <div class="deck-zone">客艙 + Animator's Palate</div>
      <div class="deck-items">
        <span class="item-pill dining">🎨 Animator's Palate</span>
        <span class="item-pill">內部/海景客艙</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:rgba(255,255,255,.4)">4</div>
    <div class="deck-content">
      <div class="deck-zone">登船甲板 / 旅客服務</div>
      <div class="deck-items">
        <span class="item-pill">登船入口</span>
        <span class="item-pill">醫療中心</span>
        <span class="item-pill">訪客服務</span>
      </div>
    </div>
  </div>

  <div class="deck-row">
    <div class="deck-num" style="color:rgba(255,255,255,.2)">1–3</div>
    <div class="deck-content">
      <div class="deck-zone" style="color:rgba(255,255,255,.3)">工作人員/引擎室（不對旅客開放）</div>
    </div>
  </div>
</div>
```

  </div>

  <div class="ov-card full" style="background:rgba(20,40,82,.85);border:1px solid rgba(245,200,66,.2)">
    <span class="oc-icon">📎</span>
    <h4>官方甲板圖 PDF 下載</h4>
    <p style="margin-bottom:8px">官方完整圖表可下載離線使用：</p>
    <a href="https://disneycruise.disney.go.com/ships/deck-plans/adventure/" target="_blank" style="display:block;background:var(--gold);color:#0B1E3D;text-decoration:none;border-radius:9px;padding:9px 14px;text-align:center;font-weight:700;font-size:.8rem;margin-bottom:6px">🗺️ 官網互動式甲板圖</a>
    <a href="https://dclfan.com/wp-content/uploads/2024/12/disney-adventure-deck-plans.pdf" target="_blank" style="display:block;background:rgba(255,255,255,.08);color:var(--cream);text-decoration:none;border-radius:9px;padding:9px 14px;text-align:center;font-size:.78rem;border:1px solid rgba(255,255,255,.15)">📄 下載 PDF 版甲板圖</a>
  </div>
</section>

<!-- ═══════════════════════════════════
     2. SHOWS
═══════════════════════════════════ -->

<section id="shows">
  <div class="sec-title">🎭 精彩演出</div>
  <div class="sec-sub">點擊展開 · 確切時間以 Navigator App 為準</div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#0D4F8A,#2EC4B6)">⛵</div>
      <div class="ci"><h3>Let's Set Sail（啟航秀）</h3><p>登船首日 · 精靈主持的歡迎派對</p>
        <div class="cmeta"><span class="tag tloc">Deck 6 Garden Stage</span><span class="tag ttime">約20分鐘</span><span class="tag ttype">首日限定</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">神燈精靈（Genie）主持的歡迎秀！一位幸運小客人搓燈瓶召喚精靈。米奇、艾莎、灰姑娘、蒂阿娜、巴斯光年、胡迪、蜘蛛人、M 女士輪番登台，最後倒數啟航！</p>
      <table class="sch-table"><tr><th>時間</th><th>說明</th></tr><tr><td>下午 4:30 前後</td><td>登船首日，船離港前約1小時</td></tr></table>
      <div class="ctip"><p>🌟 帶孩子提早佔位，說不定被選中搓燈！<strong>中間前方</strong>視野最佳。</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#4a2800,#8B5E2A)">☠️</div>
      <div class="ci"><h3>Captain Jack Sparrow & The Siren Queen（傑克船長與海妖女王）</h3><p>加勒比海冒險特技秀</p>
        <div class="cmeta"><span class="tag tloc">Deck 6 Garden Stage</span><span class="tag ttime">約25分鐘</span><span class="tag ttype">冒險特技</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">傑克船長遭遇神秘海妖女王，一場刀光劍影的海盜冒險！充滿幽默與特技，老少皆宜。</p>
      <table class="sch-table"><tr><th>時間</th><th>說明</th></tr><tr><td>傍晚 6:00–8:00 pm</td><td>各海上日，戶外演出受天氣影響</td></tr></table>
      <div class="ctip"><p>🗡️ 前排觀眾可能被「選為船員」！</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#1a3a6e,#2e6fbb)">🤖</div>
      <div class="ci"><h3>Remember（記憶）</h3><p>全球首個 WALL-E 現場演出</p>
        <div class="cmeta"><span class="tag tloc">Deck 9 Walt Disney Theatre</span><span class="tag ttime">約45分鐘</span><span class="tag ttype">百老匯音樂劇</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">冒險號獨家原創音樂劇，WALL-E 協助 EVE 找回失去的記憶，穿越小美人魚、阿拉丁、可可夜總會。精緻偶戲 + 動人音樂，全船最高評價。</p>
      <table class="sch-table"><tr><th>場次</th><th>時間</th><th>日次</th></tr>
        <tr><td>第一場</td><td>晚上 7:30</td><td>3夜：第2夜 / 4夜：第2夜</td></tr>
        <tr><td>第二場</td><td>晚上 9:30</td><td>同日</td></tr></table>
      <div class="ctip"><p>🌟 <strong>禮賓客提前35分鐘入場</strong>（無需排隊），先選最佳位子！兩場都值得看。</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#8B0000,#CC2200)">⚡</div>
      <div class="ci"><h3>Avengers Assemble!（復仇者集結）</h3><p>Marvel 特技大秀 + 死侍首秀</p>
        <div class="cmeta"><span class="tag tloc">Deck 6 Garden Stage</span><span class="tag ttime">約30分鐘</span><span class="tag ttype">特技動作秀</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">Marvel 英雄對抗反派，煙火特效、LED 燈光、與整艘船互動。死侍幽默登場，充分利用露天甲板垂直空間。</p>
      <table class="sch-table"><tr><th>場次</th><th>時間</th></tr><tr><td>黃昏場</td><td>晚上 7:00</td></tr><tr><td>夜間場</td><td>晚上 9:00</td></tr></table>
      <div class="ctip"><p>💡 <strong>看兩場</strong>，每場都有新細節！四面都有驚喜。</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#5a3a00,#C9A227)">🦁</div>
      <div class="ci"><h3>The Lion King: Celebration in the Sky（獅子王天空慶典）</h3><p>世界唯一海上煙火秀</p>
        <div class="cmeta"><span class="tag tloc">Deck 16–20 頂層露天</span><span class="tag ttime">約20分鐘</span><span class="tag ttype">🎆 海上煙火</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">Shah Rukh Khan 旁白，《Circle of Life》《He Lives in You》配樂，在無垠黑色海洋上綻放煙火，世界獨一無二！</p>
      <table class="sch-table"><tr><th>時間</th><th>日次</th><th>位置</th></tr>
        <tr><td>晚上 10:00–10:30</td><td>3夜：第2夜 / 4夜：第3夜</td><td>船尾 Wayfinder Bay 最佳</td></tr></table>
      <p class="sch-note">⚠️ 天氣惡劣可能取消，請以 App 公告為準。</p>
      <div class="ctip"><p>🎆 您的房間 16123 就在 Deck 16 Wayfinder Bay 旁！<strong>從陽台可能就能欣賞</strong>。提前30分鐘佔位，帶薄外套。</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#2a1a6e,#6a3acc)">⭐</div>
      <div class="ci"><h3>Disney Seas the Adventure（迪士尼揚帆冒險）</h3><p>高飛主角歌舞秀</p>
        <div class="cmeta"><span class="tag tloc">Deck 9 Walt Disney Theatre</span><span class="tag ttime">約30分鐘</span><span class="tag ttype">音樂歌舞</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">以高飛為主角，串連莫娜、米格等角色，充滿活力的舞蹈與多彩舞台設計，老少皆宜。</p>
      <table class="sch-table"><tr><th>場次</th><th>時間</th></tr><tr><td>第一場</td><td>晚上 7:30</td></tr><tr><td>第二場</td><td>晚上 9:30</td></tr></table>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#0D4F8A,#2EC4B6)">🌊</div>
      <div class="ci"><h3>Moana: Call of the Sea（海洋呼喚）</h3><p>以真實海洋為背景的戶外演出</p>
        <div class="cmeta"><span class="tag tloc">Deck 16 Wayfinder Bay</span><span class="tag ttime">約20分鐘</span><span class="tag ttype">戶外音樂劇</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">在船尾泳池舞台，莫娜、毛伊現場演唱《How Far I'll Go》，身後就是真實的印度洋。</p>
      <table class="sch-table"><tr><th>時間</th><th>備註</th></tr><tr><td>傍晚 5:30–6:30</td><td>光線最美，Wayfinder Bay 就在您房間樓層！</td></tr></table>
      <div class="ctip"><p>🏠 您的 16123 就在 Deck 16，<strong>距離 Wayfinder Bay 超近</strong>！提前步行即可佔位。</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#2a1a6e,#6a3acc)">🎨</div>
      <div class="ci"><h3>Mickey's Color Spin Dance Party（米奇彩色舞會）</h3><p>全場互動舞蹈派對</p>
        <div class="cmeta"><span class="tag tloc">Deck 6 Garden Stage</span><span class="tag ttime">約20分鐘</span><span class="tag ttype">互動舞蹈</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <table class="sch-table"><tr><th>時間</th></tr><tr><td>下午 4:00–5:00（各海上日）</td></tr></table>
      <div class="ctip"><p>🎵 穿繽紛顏色參加更有趣！帶孩子釋放能量。</p></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#c8dcfc,#6aacff)">🤍</div>
      <div class="ci"><h3>Baymax Super Exercise Expo（大英雄運動嘉年華）</h3><p>大白帶您做操！</p>
        <div class="cmeta"><span class="tag tloc">Deck 11 San Fransokyo</span><span class="tag ttime">約20分鐘</span><span class="tag ttype">互動體驗</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <table class="sch-table"><tr><th>時間</th></tr><tr><td>上午 10:00–11:00（各海上日）</td></tr></table>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#5a3a00,#c48a30)">🧸</div>
      <div class="ci"><h3>Duffy and The Friend Ship（達菲與好朋友）</h3><p>達菲熊的溫馨海上旅行</p>
        <div class="cmeta"><span class="tag tloc">Deck 6 Garden Stage</span><span class="tag ttime">約25分鐘</span><span class="tag ttype">溫馨歌舞</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">達菲熊與雪莉玫、傑拉多尼等好友的溫馨海上旅行，由海鷗 Tippy Blue 帶路。亞洲限定秀。</p>
      <table class="sch-table"><tr><th>時間</th></tr><tr><td>下午 2:00–3:00（各海上日）</td></tr></table>
      <div class="ctip"><p>🐻 帶上達菲玩偶，場地較小提前入座！</p></div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     3. DINING
═══════════════════════════════════ -->

<section id="dining">
  <div class="sec-title">🍽️ 船上餐廳</div>
  <div class="sec-sub">點擊查看完整中英文菜單</div>
  <div class="cat-tabs">
    <button class="cbt active" onclick="switchCat('rot','dining')">🔄 輪替正餐</button>
    <button class="cbt" onclick="switchCat('buf','dining')">🥘 自助餐</button>
    <button class="cbt" onclick="switchCat('qs','dining')">🍔 快餐</button>
    <button class="cbt" onclick="switchCat('prem','dining')">💎 付費高級</button>
    <button class="cbt" onclick="switchCat('bar','dining')">🍹 酒吧茶廊</button>
  </div>

  <div class="clist active" id="dcat-rot">
    <div class="rn" style="margin-bottom:11px">🔄 每晚不同主題餐廳，服務員跟著走，3夜體驗3間。6間餐廳兩兩共用同一套晚餐菜單。</div>

```
<div class="card" onclick="toggleCard(this)">
  <div class="card-hd"><span style="font-size:1.6rem">⚓</span>
    <div class="ci"><h3>Navigator's Club（航海家俱樂部）</h3><p>藝術裝飾風格 · Deck 6</p>
      <div class="cmeta"><span class="tag tdeck">Deck 6</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
  <div class="card-body">
    <div class="mh">🥗 前菜 Starters</div>
    <div class="mi"><div><div class="min">豬肉蝦仁燒賣 Pork & Shrimp Shumai</div><div class="mid">搭配薑汁醬油 / Ginger Soy Sauce</div></div></div>
    <div class="mi"><div><div class="min">青木瓜沙拉 Green Papaya Salad</div><div class="mid">長豆、辣椒、小番茄、椰糖萊姆醬 / Long Beans, Chili, Grape Tomato, Palm Sugar Lime Dressing</div></div><span class="mibadge bv">素食</span></div>
    <div class="mi"><div><div class="min">炸餛飩湯 Wonton Soup</div><div class="mid">軟雞肉餛飩、雞高湯、薑、大白菜、蔥 / Chicken Broth, Ginger, Napa Cabbage, Green Onions</div></div></div>
    <div class="mi"><div><div class="min">海南雞飯 Hainanese Chicken Rice</div><div class="mid">新加坡特色，附薑蔥醬 / With Ginger Sauce</div></div><span class="mibadge bh">清真</span></div>
    <div class="mi"><div><div class="min">玉米芋頭濃湯 Molokai Corn & Taro Chowder</div><div class="mid">玉米粒、蔥 / Cut Yellow Corn, Sliced Green Onions</div></div><span class="mibadge bv">素食</span></div>
    <div class="mh">🍖 主菜 Main Courses</div>
    <div class="mi"><div><div class="min">沙爹雞肉串 Chicken Satay</div><div class="mid">椰子飯、黃瓜、花生醬 / Coconut Rice, Cucumber, Roasted Peanut Dipping</div></div><span class="mibadge bh">清真</span></div>
    <div class="mi"><div><div class="min">烤鮭魚 Seared Verlasso Salmon Filet</div><div class="mid">烤蔬菜、椰奶醬 / Grilled Vegetables, Coconut Sauce</div></div></div>
    <div class="mi"><div><div class="min">皇家奶油雞 Chicken Shahi Korma</div><div class="mid">印度風味咖哩、印度香米 / Indian-style Curry, Basmati Rice</div></div><span class="mibadge bh">清真</span></div>
    <div class="mi"><div><div class="min">辣炒豆腐 Tofu Stir-fry</div><div class="mid">每日輪替醬汁 / Rotating Sauce</div></div><span class="mibadge bv">純素</span></div>
    <div class="mh">🍰 甜點 Desserts</div>
    <div class="mi"><div><div class="min">米奇巧克力塔 Mickey Chocolate Tarte</div><div class="mid">招牌甜點 / Signature Dessert</div></div></div>
    <div class="mi"><div><div class="min">白巧克力麵包布丁 White Chocolate Bread Pudding</div><div class="mid">焦糖醬、香草冰淇淋 / Caramel Sauce, Vanilla Ice Cream</div></div></div>
    <div class="mi"><div><div class="min">兒童菜單 Kids Menu</div><div class="mid">沙拉、烤雞、迷你漢堡、通心麵 / Salad, Chicken, Mini Cheeseburger, Mac & Cheese</div></div></div>
    <div class="rn">💡 與 Hollywood Spotlight Club 共用菜單。米奇、米妮、唐老鴨盛裝互動，帶相機！</div>
  </div>
</div>

<div class="card" onclick="toggleCard(this)">
  <div class="card-hd"><span style="font-size:1.6rem">🎬</span>
    <div class="ci"><h3>Hollywood Spotlight Club（好萊塢聚光燈）</h3><p>黃金好萊塢主題 · Deck 8</p>
      <div class="cmeta"><span class="tag tdeck">Deck 8</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
  <div class="card-body">
    <div class="mh">🌟 特色前菜（與 Navigator's Club 相同菜單，追加以下）</div>
    <div class="mi"><div><div class="min">黃鰭鮪魚孟買咖哩 Yellow Fin Tuna Mumbai Bhel</div><div class="mid">Ceviche 混孟買街頭風 / Ceviche-style with Mumbai Street Food Elements</div></div></div>
    <div class="mi"><div><div class="min">韓式烤牛肉蒸餃 Korean BBQ Beef Steamed Bao</div><div class="mid">醃黃瓜、韓式甜辣醬 / Pickled Cucumber, Gochujang Hoisin Sauce</div></div></div>
    <div class="rn">主菜、甜點同 Navigator's Club。角色盛裝互動表演。</div>
  </div>
</div>

<div class="card" onclick="toggleCard(this)">
  <div class="card-hd"><span style="font-size:1.6rem">🎨</span>
    <div class="ci"><h3>Animator's Palate（動畫師調色盤）</h3><p>Pixar 主題 · 自畫角色出現在螢幕 · Deck 5</p>
      <div class="cmeta"><span class="tag tdeck">Deck 5</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
  <div class="card-body">
    <div class="mh">🥗 前菜 Starters</div>
    <div class="mi"><div><div class="min">叻沙椰奶麵 Laksa Lemak</div><div class="mid">辣椰奶湯底、米粉 / Spicy Coconut Broth, Rice Noodles</div></div><span class="mibadge bh">清真</span></div>
    <div class="mi"><div><div class="min">龍捲壽司 Dragon Roll</div><div class="mid">辣鮪魚、新鮮水鰻、酪梨、鰻魚醬 / Spicy Tuna, Freshwater Eel, Avocado, Unagi Sauce</div></div></div>
    <div class="mi"><div><div class="min">韓式烤牛肉包 Korean BBQ Beef Bao</div><div class="mid">醃黃瓜、韓式甜辣醬 / Pickled Cucumber, Gochujang Hoisin</div></div></div>
    <div class="mi"><div><div class="min">米線湯 Rice Noodle Soup</div><div class="mid">白蘿蔔、黃瓜、胡蘿蔔、雪豆 / Daikon, Cucumber, Carrot, Snow Peas</div></div><span class="mibadge bv">素食</span></div>
    <div class="mi"><div><div class="min">夏威夷玉米芋泥濃湯 Molokai Corn & Taro Chowder</div><div class="mid">玉米、蔥 / Yellow Corn, Green Onions</div></div></div>
    <div class="mi"><div><div class="min">棕櫚心沙拉 Hearts of Palm Salad</div><div class="mid">萊姆芫荽、甜椒、玉米 / Cilantro Lime, Bell Pepper, Popcorn</div></div><span class="mibadge bv">純素</span></div>
    <div class="mh">🍖 主菜 Mains</div>
    <div class="mi"><div><div class="min">果阿豬五花 Goan Pork Belly</div><div class="mid">印度果阿香料、配上馬餅 / Goa-style Spices with Upma Cake</div></div></div>
    <div class="mi"><div><div class="min">烤鮭魚 Seared Verlasso Salmon</div><div class="mid">椰奶醬汁、烤蔬菜 / Coconut Sauce, Grilled Vegetables</div></div></div>
    <div class="mi"><div><div class="min">皇家奶油雞 Chicken Shahi Korma</div><div class="mid">同其他輪替餐廳</div></div><span class="mibadge bh">清真</span></div>
    <div class="mh">🍰 甜點 Desserts</div>
    <div class="mi"><div><div class="min">米奇動畫塔 Animator's Tarte</div><div class="mid">巧克力、卡通裝飾 / Chocolate, Animated Character Decoration</div></div></div>
    <div class="rn">🖊️ 用餐前在餐墊紙繪製角色，看它出現在四周螢幕！</div>
  </div>
</div>

<div class="card" onclick="toggleCard(this)">
  <div class="card-hd"><span style="font-size:1.6rem">🌸</span>
    <div class="ci"><h3>Enchanted Summer / Pixar Market 晚餐（魔法夏日 / Pixar 市場）</h3><p>早午自助、晚間點餐 · Deck 6 & 17</p>
      <div class="cmeta"><span class="tag tdeck">Deck 6 / Deck 17</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
  <div class="card-body">
    <div class="mh">🌙 晚餐（點餐制，共用菜單）</div>
    <div class="mi"><div><div class="min">沙嗲雞肉 Chicken Shahi Korma</div><div class="mid">印度香料咖哩、椰子飯 / Indian Spice Curry, Coconut Rice</div></div><span class="mibadge bh">清真</span></div>
    <div class="mi"><div><div class="min">青木瓜沙拉 Green Papaya Salad</div><div class="mid">長豆、辣椒 / Long Beans, Chili</div></div><span class="mibadge bv">素食</span></div>
    <div class="mi"><div><div class="min">豬肉蝦仁燒賣 Pork & Shrimp Shumai</div><div class="mid">薑汁醬油 / Ginger Soy Sauce</div></div></div>
    <div class="mi"><div><div class="min">泰式羅勒塔 Lemon Thai Basil Tart</div><div class="mid">檸檬凝乳、泰羅勒甘納許、覆盆子醬 / Lemon Curd, Thai Basil Ganache, Raspberry</div></div></div>
    <div class="mi"><div><div class="min">白巧克力麵包布丁 White Chocolate Bread Pudding</div><div class="mid">焦糖醬 / Caramel Sauce</div></div></div>
    <div class="mi"><div><div class="min">兒童菜單 Kids Menu</div><div class="mid">田園沙拉、烤雞餃子、迷你漢堡、火雞肉醬寬麵 / Garden Salad, Chicken Potstickers, Mini Cheeseburger, Turkey Bolognese</div></div></div>
    <div class="rn">Pixar Market 位於 Deck 17，視野更佳；Enchanted Summer 在 Deck 6。菜單每日輪替！</div>
  </div>
</div>

<div class="card" onclick="toggleCard(this)">
  <div class="card-hd"><span style="font-size:1.6rem">🎭</span>
    <div class="ci"><h3>Animator's Table（動畫師餐桌）</h3><p>Pixar 主題 · Deck 9</p>
      <div class="cmeta"><span class="tag tdeck">Deck 9</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
  <div class="card-body">
    <p class="cdesc">與 Animator's Palate 為姊妹餐廳，共用相同菜單，皆有自繪角色在螢幕上出現的互動體驗。</p>
    <div class="rn">菜單同 Animator's Palate（見上方）。</div>
  </div>
</div>
```

  </div>

  <div class="clist" id="dcat-buf">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🥗</span>
        <div class="ci"><h3>Enchanted Summer / Pixar Market 自助早午餐</h3><p>早餐 & 午餐自助，種類豐富 · Deck 6 & 17</p>
          <div class="cmeta"><span class="tag tdeck">Deck 6 / 17</span><span class="tag tincl">✓ 含票價</span><span class="tag thalal">清真選項</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mh">🌅 早餐 Breakfast</div>
        <div class="mi"><div><div class="min">米奇鬆餅 Mickey Waffle</div><div class="mid">經典香草口味 / Classic Vanilla; 偶爾出現肉桂糖吉拿棒版（限量）</div></div></div>
        <div class="mi"><div><div class="min">各式亞洲粥品 Asian Congee</div><div class="mid">薑、皮蛋、豬肉配料 / Ginger, Century Egg, Pork Toppings</div></div></div>
        <div class="mi"><div><div class="min">印度 Idli 蒸糕 Idli</div><div class="mid">搭配各式沾醬 / With Various Chutneys</div></div><span class="mibadge bv">全素</span></div>
        <div class="mi"><div><div class="min">美式早餐區 American Breakfast</div><div class="mid">炒蛋、培根、貝果、麵包 / Scrambled Eggs, Bacon, Bagels</div></div></div>
        <div class="mi"><div><div class="min">各式水果 Fresh Fruit</div><div class="mid">時令水果 / Seasonal Fruits</div></div><span class="mibadge bv">素食</span></div>
        <div class="mh">🌞 午餐 Lunch</div>
        <div class="mi"><div><div class="min">海南雞飯 Hainanese Chicken Rice</div><div class="mid">新加坡特色！ / Singapore Signature</div></div></div>
        <div class="mi"><div><div class="min">海鮮燉飯 Seafood Paella</div><div class="mid">地中海風格 / Mediterranean Style</div></div></div>
        <div class="mi"><div><div class="min">波隆那肉醬筆管麵 Bolognese Penne</div><div class="mid">義式 / Italian Style</div></div></div>
        <div class="mi"><div><div class="min">坦多里烤雞 Tandoori Chicken</div><div class="mid">印度香料醃製 / Indian Spiced</div></div><span class="mibadge bh">清真</span></div>
        <div class="mi"><div><div class="min">椰汁咖哩豬排 Coconut Tonkatsu Curry</div><div class="mid">亞洲風味 / Asian Style</div></div></div>
        <div class="mi"><div><div class="min">法拉費沙拉 Falafel Salad</div><div class="mid">鷹嘴豆炸物、各式沙拉 / Chickpea Fritters with Salad</div></div><span class="mibadge bv">素食</span></div>
        <div class="mi"><div><div class="min">兒童區 Kids Station</div><div class="mid">起司漢堡、麥克起司通心粉、烤腸 / Cheeseburger, Mac & Cheese, Bratwurst</div></div></div>
        <div class="rn">⏰ 菜色每天輪替，過敏或飲食限制請告知服務人員。Pixar Market 視野更佳！</div>
      </div>
    </div>
  </div>

  <div class="clist" id="dcat-qs">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍛</span>
        <div class="ci"><h3>Mowgli's Eatery（毛克利食堂）</h3><p>叢林書主題 · 印度料理 · Deck 6</p>
          <div class="cmeta"><span class="tag tdeck">Deck 6</span><span class="tag tincl">✓ 含票價</span><span class="tag thalal">清真</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">坦多里辣味雞肉提卡 Tandoori Habanero Bhuna Chicken Tikka</div><div class="mid">阿穆爾起司馕餅球 / With Amul Cheese Naan Bombs</div></div><span class="mibadge bh">清真</span></div>
        <div class="mi"><div><div class="min">蔬食咖哩 Vegetable Curry</div><div class="mid">每日輪替 / Daily Rotation</div></div><span class="mibadge bv">全素</span></div>
        <div class="mi"><div><div class="min">印度烤餅包 Naan Wrap</div><div class="mid">各式餡料 / Various Fillings</div></div></div>
        <div class="rn">🌱 全船最佳素食 & 清真快餐選擇！</div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🌺</span>
        <div class="ci"><h3>Gramma Tala's Kitchen（塔拉奶奶廚房）</h3><p>莫娜主題 · 太平洋菜 · Deck 6</p>
          <div class="cmeta"><span class="tag tdeck">Deck 6</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">海南雞飯 Hainanese Chicken Rice</div><div class="mid">新加坡風味高度還原 / Singapore-style</div></div></div>
        <div class="mi"><div><div class="min">Huli Huli 烤雞 Huli Huli Chicken</div><div class="mid">夏威夷蜜汁烤雞 / Hawaiian-style Glazed Chicken</div></div></div>
        <div class="mi"><div><div class="min">四川豆腐 Sichuan Tofu</div><div class="mid">麻辣風格 / Spicy Mala Style</div></div><span class="mibadge bv">素食</span></div>
        <div class="mi"><div><div class="min">夏威夷通心粉沙拉 Hawaiian Macaroni Salad</div><div class="mid">清爽口味 / Refreshing</div></div></div>
        <div class="mi"><div><div class="min">山藥地瓜 Candied Yams</div><div class="mid">蜜汁地瓜 / Glazed Sweet Potato</div></div><span class="mibadge bv">素食</span></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🦸</span>
        <div class="ci"><h3>Cosmic Kebabs（宇宙烤串）</h3><p>Ms Marvel 主題 · 無豬廚房 · Deck 10</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10</span><span class="tag tincl">✓ 含票價</span><span class="tag thalal">無豬廚房</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">各式烤肉串 Assorted Kebabs</div><div class="mid">搭配烤餅、各式醬料 / With Flatbread & Sauces</div></div><span class="mibadge bh">無豬</span></div>
        <div class="mi"><div><div class="min">蔬食烤串 Veggie Kebabs</div><div class="mid">各式蔬菜串 / Assorted Vegetables</div></div><span class="mibadge bv">素食</span></div>
        <div class="mi"><div><div class="min">皮塔餅三明治 Pita Sandwich</div><div class="mid">沙拉、醬料 / Salad, Sauces</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍦</span>
        <div class="ci"><h3>Wheezy's Freezies（玩具總動員冰淇淋）</h3><p>免費軟式冰淇淋至午夜 · Deck 17</p>
          <div class="cmeta"><span class="tag tdeck">Deck 17</span><span class="tag tincl">✓ 免費無限</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">軟式冰淇淋 Soft Serve Ice Cream</div><div class="mid">多種口味，每天到午夜 12 點免費 / Multiple Flavors, Free until Midnight</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍕</span>
        <div class="ci"><h3>Pizza Planet / Stitch's 'Ohana Grill</h3><p>玩具總動員 & Stitch 主題 · Deck 10 & 17</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10/17</span><span class="tag tincl">✓ 含票價</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">各式比薩 Various Pizzas</div><div class="mid">每日口味不同 / Daily Rotation</div></div></div>
        <div class="mi"><div><div class="min">Loco Moco（夏威夷漢堡飯）</div><div class="mid">牛肉漢堡排、米飯、肉汁 / Beef Patty, Rice, Gravy</div></div></div>
        <div class="mi"><div><div class="min">拿坡里番茄義麵 Napolitana Pasta</div><div class="mid">番茄醬、羅勒 / Tomato Sauce, Basil</div></div><span class="mibadge bv">素食</span></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🧋</span>
        <div class="ci"><h3>Bewitching Boba & Brews（魔法珍奶站）</h3><p>Deck 11</p>
          <div class="cmeta"><span class="tag tdeck">Deck 11</span><span class="tag tpaid">部分付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">珍珠奶茶 Bubble Tea</div><div class="mid">多種口味 / Multiple Flavors</div></div></div>
        <div class="mi"><div><div class="min">果昔 Smoothie</div><div class="mid">新鮮水果 / Fresh Fruit</div></div></div>
      </div>
    </div>
  </div>

  <div class="clist" id="dcat-prem">
    <div class="rn" style="margin-bottom:11px">💎 以下需額外付費，建議上船後立即透過 Navigator App 預訂。</div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🇮🇹</span>
        <div class="ci"><h3>Palo Trattoria（帕羅義大利餐廳）</h3><p>成人專屬 · 精緻義大利 · Deck 10</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10</span><span class="tag tpaid">💰 額外付費</span><span class="tag tadult">18+ 成人</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mh">🍝 主要菜色 Menu Highlights</div>
        <div class="mi"><div><div class="min">馬鈴薯麵疙瘩 Potato Gnocchi</div><div class="mid">奶油堅果醬汁 / Creamy Nut Sauce</div></div></div>
        <div class="mi"><div><div class="min">手工義大利麵 Fresh Pasta</div><div class="mid">多種醬汁選擇 / Various Sauces</div></div></div>
        <div class="mi"><div><div class="min">當日海鮮 Fresh Seafood</div><div class="mid">新鮮食材 / Daily Fresh Catch</div></div></div>
        <div class="mi"><div><div class="min">提拉米蘇 Tiramisu</div><div class="mid">傳統義式 / Classic Italian</div></div></div>
        <div class="rn">🌊 船尾絕佳海景，適合特別紀念日。</div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">☕</span>
        <div class="ci"><h3>Palo Café（帕羅咖啡）</h3><p>鵝卵石露台 · Deck 10</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10</span><span class="tag tpaid">💰 額外付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">馬鈴薯麵疙瘩 Potato Gnocchi</div><div class="mid">奶油堅果醬 / Cream & Nut Sauce</div></div></div>
        <div class="mi"><div><div class="min">特調精品咖啡 Specialty Coffee</div><div class="mid">可選迪士尼角色拉花 / Disney Character Latte Art Available</div></div></div>
        <div class="rn">☕ 告知咖啡師想要哪個角色的拉花！在 Pixar Market 用餐時也可點此咖啡。</div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">👾</span>
        <div class="ci"><h3>Mike & Sulley's Flavors of Asia（亞洲風味）</h3><p>怪獸電力公司主題 · Deck 10</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10</span><span class="tag tpaid">部分需付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">各式亞洲小點 Asian Bites</div><div class="mid">每日輪替 / Daily Rotation</div></div></div>
      </div>
    </div>
  </div>

  <div class="clist" id="dcat-bar">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🧿</span>
        <div class="ci"><h3>Tiana's Bayou Lounge（蒂阿娜的沼澤茶廊）</h3><p>公主與青蛙主題 · Deck 9</p>
          <div class="cmeta"><span class="tag tdeck">Deck 9</span><span class="tag tincl">甜點含票價</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">法式甜甜圈 Beignets</div><div class="mid">撒糖粉，Disney郵輪經典 / Powdered Sugar, DCL Classic</div></div></div>
        <div class="mi"><div><div class="min">精品咖啡（角色拉花）Specialty Coffee</div><div class="mid">Disney Character Latte Art</div></div></div>
        <div class="mi"><div><div class="min">無酒精調酒 Mocktails</div><div class="mid">創意莫希托等 / Creative Mocktails</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍺</span>
        <div class="ci"><h3>Buccaneer Bar（海盜酒吧）</h3><p>船長虎克主題 · Deck 10</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10</span><span class="tag tpaid">酒精付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">精釀啤酒 Craft Beer</div></div></div>
        <div class="mi"><div><div class="min">海盜主題雞尾酒 Pirate Cocktails</div></div></div>
        <div class="rn">📺 大螢幕直播體育賽事！</div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🔮</span>
        <div class="ci"><h3>Spellbound（魔法茶室）</h3><p>邪惡皇后主題 · Deck 9</p>
          <div class="cmeta"><span class="tag tdeck">Deck 9</span><span class="tag tpaid">酒精付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">魔法藥水調酒 Magic Potion Cocktails</div><div class="mid">神秘顏色 / Mysterious Colors</div></div></div>
        <div class="mi"><div><div class="min">無酒精版 Non-Alcoholic Version</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍷</span>
        <div class="ci"><h3>Taverna Portorosso（波多羅索酒館）</h3><p>路卡主題 · 海景 · Deck 10</p>
          <div class="cmeta"><span class="tag tdeck">Deck 10</span><span class="tag tpaid">酒精付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">Aperol Spritz 等義式調酒 Italian Cocktails</div></div></div>
        <div class="mi"><div><div class="min">輕食小點 Light Bites</div><div class="mid">義大利麵包、橄欖 / Bread, Olives</div></div></div>
        <div class="rn">🌊 傍晚看夕陽最美！</div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     4. ROOM SERVICE
═══════════════════════════════════ -->

<section id="roomsvc">
  <div class="sec-title">🛎️ 客房點餐</div>
  <div class="sec-sub">24小時服務（最後一晚凌晨1點截止）· 大部分免費</div>
  <div class="rn" style="margin-bottom:13px">📞 <strong>如何點餐</strong>：Navigator App 查看菜單 → 撥打房內電話（0 → 客房服務）<br>🌅 <strong>早餐表單</strong>：填寫後凌晨3點前掛在門外，隔天早上送達<br>🍦 <strong>隱藏菜單</strong>：米奇冰淇淋棒不在菜單上，直接告知工作人員即可！</div>
  <div class="cat-tabs">
    <button class="cbt active" onclick="switchCat('rs-bk','roomsvc')">🌅 早餐</button>
    <button class="cbt" onclick="switchCat('rs-main','roomsvc')">🍔 主食</button>
    <button class="cbt" onclick="switchCat('rs-snack','roomsvc')">🧀 小食甜點</button>
    <button class="cbt" onclick="switchCat('rs-bev','roomsvc')">☕ 飲品</button>
  </div>
  <div class="clist active" id="rscat-rs-bk">
    <div class="rn" style="margin-bottom:9px">🛏️ 早餐表單：睡前填寫掛在門外（凌晨3點前），隔天按選定時段送達。</div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🥐</span>
        <div class="ci"><h3>早餐表單點餐 Continental Breakfast Card</h3><p>前晚掛門外，隔日送達</p><div class="cmeta"><span class="tag tincl">✓ 免費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">各式麵包、土司、牛角麵包 Bread / Toast / Croissant</div><div class="mid">搭配奶油、果醬 / Butter, Jam</div></div></div>
        <div class="mi"><div><div class="min">炒蛋 / 煎蛋 Scrambled / Fried Eggs</div></div></div>
        <div class="mi"><div><div class="min">培根、香腸 Bacon / Sausage</div></div></div>
        <div class="mi"><div><div class="min">各式穀片 & 燕麥粥 Cereals / Oatmeal</div></div></div>
        <div class="mi"><div><div class="min">新鮮水果盤 Fresh Fruit Plate</div></div><span class="mibadge bv">素食</span></div>
        <div class="mi"><div><div class="min">優格 Yogurt</div></div></div>
        <div class="mi"><div><div class="min">咖啡、茶、果汁、牛奶 Coffee / Tea / Juice / Milk</div></div></div>
        <div class="rn">🌟 禮賓套房在最後一天（離船日）可點更豐盛熱食早餐！</div>
      </div>
    </div>
  </div>
  <div class="clist" id="rscat-rs-main">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍔</span>
        <div class="ci"><h3>主食類 Main Dishes</h3><p>24小時隨時可點</p><div class="cmeta"><span class="tag tincl">✓ 大多免費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">起司漢堡 Cheeseburger</div><div class="mid">附薯條 / With Fries</div></div></div>
        <div class="mi"><div><div class="min">雞肉條 Chicken Tenders</div><div class="mid">最人氣！搭配各式醬料 / #1 Most Popular! With Dipping Sauces</div></div></div>
        <div class="mi"><div><div class="min">凱薩沙拉 Caesar Salad</div><div class="mid">帕瑪森起司、脆麵包丁 / Parmesan, Croutons</div></div></div>
        <div class="mi"><div><div class="min">番茄義大利麵 Penne Pasta Marinara</div><div class="mid">番茄醬、羅勒 / Tomato Sauce, Basil</div></div><span class="mibadge bv">素食</span></div>
        <div class="mi"><div><div class="min">奶油濃湯 Cream Soup</div><div class="mid">每日口味不同 / Daily Rotation</div></div></div>
        <div class="mi"><div><div class="min">蔬菜沙拉 Garden Salad</div><div class="mid">各式沙拉醬 / Choice of Dressings</div></div><span class="mibadge bv">素食</span></div>
        <div class="mi"><div><div class="min">薯條 French Fries</div><div class="mid">可單點！深夜宵夜首選 / Order Separately, Great for Late Night!</div></div></div>
      </div>
    </div>
  </div>
  <div class="clist" id="rscat-rs-snack">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🧀</span>
        <div class="ci"><h3>小食與甜點 Snacks & Desserts</h3><div class="cmeta"><span class="tag tincl">✓ 大多免費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">綜合起司拼盤 All Hands on Deck Cheese Plate</div><div class="mid">附餅乾，電影夜首選 / With Crackers, Perfect for Movie Night!</div></div></div>
        <div class="mi"><div><div class="min">牛肉辣翅 Buffalo Wings</div><div class="mid">辣香下酒 / Spicy & Crispy</div></div></div>
        <div class="mi"><div><div class="min">甜點（每日輪替）Daily Dessert</div></div></div>
        <div class="mi"><div><div class="min">🌟 米奇冰淇淋棒（隱藏菜單！）Mickey Premium Ice Cream Bar</div><div class="mid">不在菜單上！直接告知工作人員 / Not on Menu — Just Ask!</div></div></div>
        <div class="rn">🍦 米奇冰淇淋棒是最人氣的「秘密點餐」！</div>
      </div>
    </div>
  </div>
  <div class="clist" id="rscat-rs-bev">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">☕</span>
        <div class="ci"><h3>飲品 Beverages</h3><div class="cmeta"><span class="tag tincl">部分免費</span><span class="tag tpaid">酒精付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mh">✓ 免費 Complimentary</div>
        <div class="mi"><div><div class="min">咖啡（美式、拿鐵等）Coffee</div></div></div>
        <div class="mi"><div><div class="min">各式茶 Tea</div></div></div>
        <div class="mi"><div><div class="min">果汁、牛奶 Juice / Milk</div></div></div>
        <div class="mh">💰 需付費 For a Charge</div>
        <div class="mi"><div><div class="min">濃縮咖啡 Espresso / Cappuccino</div></div><span class="mibadge bs">付費</span></div>
        <div class="mi"><div><div class="min">罐裝汽水 Soda</div></div><span class="mibadge bs">付費</span></div>
        <div class="mi"><div><div class="min">酒精飲品 Alcoholic Beverages</div></div><span class="mibadge bs">付費</span></div>
        <div class="mi"><div><div class="min">包裝零食 Packaged Snacks</div></div><span class="mibadge bs">付費</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     5. CONCIERGE
═══════════════════════════════════ -->

<section id="concierge">
  <div class="sec-title">👑 禮賓專區</div>
  <div class="sec-sub">Concierge Level · 房號 16123 禮賓陽台房住客</div>
  <div class="cat-tabs">
    <button class="cbt active" onclick="switchCat('co-lounge','concierge')">🥂 禮賓廳</button>
    <button class="cbt" onclick="switchCat('co-deck','concierge')">☀️ 私人露台</button>
    <button class="cbt" onclick="switchCat('co-perks','concierge')">⭐ 福利清單</button>
    <button class="cbt" onclick="switchCat('co-food','concierge')">🍽️ 禮賓餐飲</button>
    <button class="cbt" onclick="switchCat('co-spa','concierge')">💆 Spa</button>
  </div>

  <div class="clist active" id="cocat-co-lounge">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#C9A227,#F5C842)">🏛️</div>
        <div class="ci"><h3>禮賓廳（Concierge Lounge）</h3><p>Deck 15 · 全天開放 · 免費飲食供應</p><div class="cmeta"><span class="tag tdeck">Deck 15</span><span class="tag tincl">禮賓客免費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <p class="cdesc">寬敞優雅私人休息室，僅限禮賓客。禮賓服務人員全天在場協助預訂、解答問題。</p>
        <table class="sch-table">
          <tr><th>時段</th><th>供應內容</th></tr>
          <tr><td>7:00–10:30 am</td><td>早餐輕食、咖啡、茶、果汁 / Breakfast Bites, Coffee, Tea, Juice</td></tr>
          <tr><td>12:00–2:00 pm</td><td>午餐輕食、禮賓人員辦公 / Lunch Bites</td></tr>
          <tr><td>5:00–10:00 pm</td><td>🍷 免費啤酒、葡萄酒、烈酒 + 晚餐小點 / Free Beer, Wine, Spirits + Evening Snacks</td></tr>
          <tr><td>全天</td><td>非酒精飲料、Aladdin 廳 Bacha Coffee + TWG 茶 / Coffee & Tea All Day</td></tr>
        </table>
        <div class="ctip"><p>🍿 <strong>免費爆米花地點</strong>：在禮賓廳領取大袋爆米花，可帶入 <strong>Walt Disney Theatre（Deck 9）</strong>看演出！在劇院入口出示禮賓金卡（Gold Key Card）即可在入口補充站領取。晚上 5pm 後的開放吧台也是最受歡迎的福利！</p></div>
      </div>
    </div>
  </div>

  <div class="clist" id="cocat-co-deck">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#0D4F8A,#2EC4B6)">☀️</div>
        <div class="ci"><h3>禮賓私人露台（Concierge Sun Deck）</h3><p>Deck 15 · 無需排隊</p><div class="cmeta"><span class="tag tdeck">Deck 15</span><span class="tag tincl">禮賓客免費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <p class="cdesc">禮賓客專屬戶外甲板，比公共泳池安靜許多。旁邊緊鄰 Senses Spa，是最放鬆的角落。</p>
        <table class="sch-table">
          <tr><th>設施</th><th>說明</th></tr>
          <tr><td>舒適躺椅</td><td>Lounge Chairs · 人少不用搶</td></tr>
          <tr><td>☀️ 免費防曬乳</td><td>Complimentary Sunscreen</td></tr>
          <tr><td>🧊 冰涼毛巾服務</td><td>Chilled Face Cloths</td></tr>
          <tr><td>🍹 露台吧台服務</td><td>飲品點餐服務 / Drinks Available</td></tr>
          <tr><td>🥗 小食供應</td><td>輕食小點，種類輪替 / Light Snacks, Rotating</td></tr>
          <tr><td>♨️ 泡泡浴池（部分設施）</td><td>Hot Tub（視當天設施而定）</td></tr>
        </table>
        <div class="rn">💆 緊鄰 Senses Spa！可先在露台曬太陽，再進 Spa 做護理，是最完美的下午行程。</div>
      </div>
    </div>
  </div>

  <div class="clist" id="cocat-co-perks">
    <div class="ng">
      <div class="ngt">✈️ 出發前優先服務</div>
      <div class="ni tip"><span class="ni-icon">📅</span><div class="ni-text"><strong>130天前優先預訂</strong>：比一般旅客早7天可預訂 Palo 餐廳、Spa、角色合影等熱門活動，幾乎不用擔心搶不到。</div></div>
      <div class="ni tip"><span class="ni-icon">👩‍💼</span><div class="ni-text"><strong>岸上禮賓專員</strong>：出發前130天起可電話或 Email 聯繫，協助規劃行程、預訂。</div></div>
    </div>
    <div class="ng">
      <div class="ngt">🚢 登船 & 船上</div>
      <div class="ni info"><span class="ni-icon">⚡</span><div class="ni-text"><strong>優先登船</strong>：無需等候，直接前往禮賓廳，禮賓人員幫您完成所有當日預訂。</div></div>
      <div class="ni info"><span class="ni-icon">🎬</span><div class="ni-text"><strong>演出提前入場</strong>：開門前35分鐘，禮賓客透過專屬入口提前入座，自由選最佳位子（包括 Remember！）。</div></div>
      <div class="ni tip"><span class="ni-icon">🍿</span><div class="ni-text"><strong>免費爆米花</strong>：禮賓廳領取大袋爆米花帶入 <strong>Deck 9 Walt Disney Theatre</strong>。在劇院補充站出示禮賓金卡（Gold Key Card）也可領取。</div></div>
      <div class="ni tip"><span class="ni-icon">🌐</span><div class="ni-text"><strong>免費 Wi-Fi 100MB+</strong>：部分套房提供無限上網。100MB 對3–4夜已足夠瀏覽社群媒體。</div></div>
      <div class="ni info"><span class="ni-icon">🍽️</span><div class="ni-text"><strong>獨立用餐桌</strong>：輪替餐廳不與他人拼桌，享有完整私人用餐空間。</div></div>
      <div class="ni tip"><span class="ni-icon">🎁</span><div class="ni-text"><strong>升級客房設施</strong>：枕頭菜單（可選硬/軟/記憶枕）、高端盥洗用品、迷你冰箱、每日客房點心、迪士尼主題歡迎禮物。</div></div>
      <div class="ni info"><span class="ni-icon">👋</span><div class="ni-text"><strong>優先離船</strong>：航程結束禮賓客享有優先離船，省去大量等待時間。</div></div>
    </div>
  </div>

  <div class="clist" id="cocat-co-food">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍽️</span>
        <div class="ci"><h3>禮賓廚房（Concierge Kitchen）</h3><p>禮賓套房旅客專屬 · Deck 15</p><div class="cmeta"><span class="tag tdeck">Deck 15</span><span class="tag tincl">禮賓客含費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">麵包凝乳火焰捲 Bread Curd Fire Roll</div><div class="mid">軟烤肉串風格，入口即化 / Soft Kebab Style, Melt-in-Mouth</div></div></div>
        <div class="mi"><div><div class="min">炭烤旁遮普羊肉 Charred Punjabi Raara Lamb</div><div class="mid">辣椒醬搭配嬰兒烤餅 / Chili Coulis with Baby Kulcha</div></div></div>
        <div class="mi"><div><div class="min">味噌醃智利海鱸魚 Miso Glazed Chilean Seabass</div><div class="mid">日式精緻主菜 / Japanese-style Delicate Main</div></div></div>
        <div class="rn">☕ 同時享有 Aladdin 主題廳全天免費 Bacha Coffee 與 TWG 茶！</div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🛍️</span>
        <div class="ci"><h3>禮賓精品商店（Palace Treasures & 3 Wishes）</h3><p>禮賓客限定 · Deck 15</p><div class="cmeta"><span class="tag tdeck">Deck 15</span><span class="tag tadult">禮賓客限定</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">Palace Treasures（皇宮珍寶）</div><div class="mid">高端珠寶、精品奢侈品 / High-end Jewelry & Luxury Goods</div></div></div>
        <div class="mi"><div><div class="min">3 Wishes（三個願望）</div><div class="mid">限定服飾、限量收藏品 / Exclusive Apparel & Collectibles</div></div></div>
      </div>
    </div>
  </div>

  <div class="clist" id="cocat-co-spa">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#5a1a6a,#9a50cc)">💆</div>
        <div class="ci"><h3>Senses Spa & Salon（感官 Spa）</h3><p>Deck 15 · 禮賓優先預約</p><div class="cmeta"><span class="tag tdeck">Deck 15</span><span class="tag tpaid">護理需付費</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <p class="cdesc">禮賓客緊鄰 Deck 15 的 Senses Spa，可享有優先預約（130天前）。Spa 設施包含蒸氣室、蒸汽浴、體驗式蓮蓬頭（experiential showers）及加熱躺椅，部分設施免費，護理療程另計費用。</p>
        <table class="sch-table">
          <tr><th>設施 / Facility</th><th>費用</th></tr>
          <tr><td>蒸氣室 / Steam Room</td><td>隨 Spa 套組或入場費</td></tr>
          <tr><td>體驗式蓮蓬頭 / Experiential Showers</td><td>含在入場費</td></tr>
          <tr><td>加熱躺椅 / Heated Loungers</td><td>含在入場費</td></tr>
          <tr><td>按摩護理 / Massage Treatments</td><td>需另付費 / Additional Charge</td></tr>
          <tr><td>護膚美容 / Facial Treatments</td><td>需另付費 / Additional Charge</td></tr>
          <tr><td>理髮、美髮 / Hair Salon</td><td>需另付費 / Additional Charge</td></tr>
        </table>
        <div class="rn">💡 禮賓客優先預約，建議出發前130天即透過岸上禮賓專員預訂熱門護理項目！</div>
        <div class="ctip"><p>🏖️ <strong>最完美下午組合</strong>：在禮賓露台（Deck 15）曬太陽喝飲料 → 進隔壁 Senses Spa 做護理 → 回禮賓廳享用晚間免費調酒！</p></div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     6. CHARACTER MEET & GREET
═══════════════════════════════════ -->

<section id="chars">
  <div class="sec-title">🌟 角色見面會</div>
  <div class="sec-sub">各主題區域 · 部分需 Navigator App 預約</div>

  <div class="ni alert" style="margin-bottom:12px"><span class="ni-icon">⚠️</span><div class="ni-text"><strong>熱門名額極搶手！</strong>角色合影時段在上船安全演習結束後立即開放，早期航次幾秒內搶完！請提前在 Navigator App 準備好，演習一結束立刻搶訂。</div></div>
  <div class="ni tip" style="margin-bottom:12px"><span class="ni-icon">💡</span><div class="ni-text"><strong>無需預約的角色巡遊</strong>：各區域不定時有角色隨機出現！留意 Deck 6 Town Square 及 Deck 8 Imagination Garden 周邊。</div></div>

  <div class="cat-tabs">
    <button class="cbt active" onclick="switchCat('ch-booking','chars')">📱 預約方式</button>
    <button class="cbt" onclick="switchCat('ch-locs','chars')">📍 各區角色</button>
    <button class="cbt" onclick="switchCat('ch-list','chars')">🎭 角色一覽</button>
  </div>

  <div class="clist active" id="chcat-ch-booking">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#0D4F8A,#2EC4B6)">📱</div>
        <div class="ci"><h3>Navigator App 預約流程</h3><p>登船後立即操作</p></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <table class="sch-table">
          <tr><th>步驟</th><th>說明</th></tr>
          <tr><td>1. 下載 App</td><td>出發前下載 Disney Cruise Line Navigator App</td></tr>
          <tr><td>2. 連接 Wi-Fi</td><td>登船後連接船上 Wi-Fi（免費），App 在區域網路免費使用</td></tr>
          <tr><td>3. 完成安全演習</td><td>Muster Drill（強制參加），完成後系統開放預約</td></tr>
          <tr><td>4. 搶訂！</td><td>立即進入 App → 角色見面 → 選擇角色 & 時段 → 確認</td></tr>
          <tr><td>5. 確認通知</td><td>確認後收到通知，準時前往指定地點</td></tr>
        </table>
        <div class="ctip"><p>⭐ <strong>禮賓客優勢</strong>：您可以在一般旅客的7天前（130天前）就透過岸上禮賓專員預訂角色合影！不用擔心登船當天搶不到。</p></div>
      </div>
    </div>
    <div class="rn">💡 就算沒有預訂到，部分角色會在各區域不定時隨機出現，也有機會合影！不要放棄。</div>
  </div>

  <div class="clist" id="chcat-ch-locs">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🌿</span>
        <div class="ci"><h3>想像花園 Disney Imagination Garden</h3><p>Deck 6 · 主要角色合影區</p><div class="cmeta"><span class="tag tdeck">Deck 6</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <p class="cdesc">船中最熱鬧的角色見面區！繪本城堡前方為主要見面地點，各時段有不同角色出現。</p>
        <div class="mi"><div><div class="min">⛵ 船長米奇 & 米妮（Captain Mickey & Minnie）</div><div class="mid">航海服裝，最受歡迎！</div></div></div>
        <div class="mi"><div><div class="min">🐭 高飛、布魯托（Goofy & Pluto）</div></div></div>
        <div class="mi"><div><div class="min">👸 迪士尼公主（輪替）Disney Princesses</div><div class="mid">白雪公主、茉莉、樂佩、莫娜等輪替出現</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">⚡</span>
        <div class="ci"><h3>Marvel Landing</h3><p>Deck 19 · Marvel 角色</p><div class="cmeta"><span class="tag tdeck">Deck 19</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">🕷️ 蜘蛛人（Spider-Man）</div><div class="mid">感覺像演出，不只是拍照！ / Feels like a Performance</div></div></div>
        <div class="mi"><div><div class="min">🦸 其他復仇者（輪替）Other Avengers</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🏙️</span>
        <div class="ci"><h3>San Fransokyo Street</h3><p>Deck 11 · Big Hero 6</p><div class="cmeta"><span class="tag tdeck">Deck 11</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">🤍 大白（Baymax）</div><div class="mid">亞洲超人氣！隊伍通常很長</div></div></div>
        <div class="mi"><div><div class="min">🔬 小宏（Hiro）</div><div class="mid">不定時出現</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🏴‍☠️</span>
        <div class="ci"><h3>Disney Discovery Reef / 各區</h3><p>Deck 10 & 其他</p><div class="cmeta"><span class="tag tdeck">Deck 10</span></div></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">🏴‍☠️ 傑克船長（Captain Jack Sparrow）</div></div></div>
        <div class="mi"><div><div class="min">🧸 達菲熊 & 好友（Duffy & Friends）</div><div class="mid">亞洲超人氣！通常需要預約</div></div></div>
        <div class="mi"><div><div class="min">🌊 莫娜（Moana）</div><div class="mid">主要在 Wayfinder Bay 附近</div></div></div>
      </div>
    </div>
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><span style="font-size:1.6rem">🍕</span>
        <div class="ci"><h3>餐廳內角色互動</h3><p>輪替晚餐時出現</p></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mi"><div><div class="min">⚓ Navigator's Club / 🎬 Hollywood Spotlight Club</div><div class="mid">米奇、米妮、唐老鴨、黛西著盛裝現場互動表演</div></div></div>
        <div class="rn">🍽️ 輪替晚餐時的角色互動不需要單獨預約，自動安排！</div>
      </div>
    </div>
  </div>

  <div class="clist" id="chcat-ch-list">
    <div class="card" onclick="toggleCard(this)">
      <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#C9A227,#F5C842)">🎭</div>
        <div class="ci"><h3>確認出沒的角色完整清單</h3><p>依 2026 年初旅客回報</p></div><span class="tarr">▼</span></div>
      <div class="card-body">
        <div class="mh">🐭 Disney 經典角色</div>
        <div class="mi"><div><div class="min">船長米奇 & 船長米妮 Captain Mickey & Minnie</div><div class="mid">最受歡迎，優先搶訂</div></div></div>
        <div class="mi"><div><div class="min">唐老鴨 & 黛西 Donald & Daisy</div></div></div>
        <div class="mi"><div><div class="min">高飛 & 布魯托 Goofy & Pluto</div></div></div>
        <div class="mh">👸 迪士尼公主（輪替）</div>
        <div class="mi"><div><div class="min">白雪公主 Snow White</div></div></div>
        <div class="mi"><div><div class="min">茉莉公主 Princess Jasmine</div></div></div>
        <div class="mi"><div><div class="min">樂佩公主 Rapunzel</div></div></div>
        <div class="mi"><div><div class="min">莫娜 Moana</div></div></div>
        <div class="mh">⚡ Marvel</div>
        <div class="mi"><div><div class="min">蜘蛛人 Spider-Man</div><div class="mid">Marvel Landing，感覺像演出！</div></div></div>
        <div class="mh">🌏 亞洲特別角色</div>
        <div class="mi"><div><div class="min">大白 Baymax</div><div class="mid">超人氣！San Fransokyo Street</div></div></div>
        <div class="mi"><div><div class="min">達菲熊 & 好友 Duffy & Friends</div><div class="mid">亞洲版限定，需預約</div></div></div>
        <div class="mh">🏴‍☠️ 其他</div>
        <div class="mi"><div><div class="min">傑克船長 Captain Jack Sparrow</div></div></div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     7. SHOPS
═══════════════════════════════════ -->

<section id="shops">
  <div class="sec-title">🛍️ 船上商店</div>
  <div class="sec-sub">約 1,580 m² 零售空間 · 多款限定商品</div>
  <div class="rn" style="margin-bottom:12px">💡 使用 Navigator App 預約商店入場時段（特別是達菲商店），限定品早去早搶！</div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#CC2200,#FF4422)">🌏</div>
      <div class="ci"><h3>World of Disney（迪士尼世界旗艦店）</h3><p>Deck 6 · 品項最全 · 郵輪首次引進</p>
        <div class="cmeta"><span class="tag tdeck">Deck 6</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <div class="mi"><div><div class="min">冒險號限定服裝 Disney Adventure Exclusive Apparel</div><div class="mid">Spirit Jersey、T恤、雨衣、帽子</div></div></div>
      <div class="mi"><div><div class="min">新加坡天際線系列 Singapore Skyline Collection</div><div class="mid">以新加坡城市景觀設計的獨家周邊</div></div></div>
      <div class="mi"><div><div class="min">各式包款 Bags</div><div class="mid">斜背包、托特包、折疊包（多款設計）</div></div></div>
      <div class="mi"><div><div class="min">文具、馬克杯、鑰匙圈 Stationery / Mugs / Keychains</div></div></div>
      <div class="mi"><div><div class="min">迪士尼徽章（可交換）Disney Pins</div><div class="mid">與服務員交換，免費活動！</div></div></div>
      <div class="rn">🎁 部分商品僅在冒險號有售，回國後找不到！</div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#5a3a00,#c48a30)">🧸</div>
      <div class="ci"><h3>Duffy & Friends Shop（達菲與好朋友商店）</h3><p>Deck 6 · 全球首家海上達菲專賣店</p>
        <div class="cmeta"><span class="tag tdeck">Deck 6</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <div class="mi"><div><div class="min">達菲熊系列娃娃 Duffy Bear Plush</div><div class="mid">冒險號限定航海主題造型 / Exclusive Nautical Design</div></div></div>
      <div class="mi"><div><div class="min">雪莉玫、傑拉多尼等好友 Shellie May / Gelatoni</div><div class="mid">各式好友系列</div></div></div>
      <div class="mi"><div><div class="min">達菲替換服裝 Duffy Costumes</div><div class="mid">可替換的衣服、帽子 / Changeable Outfits & Hats</div></div></div>
      <div class="rn">⚠️ 超受歡迎，<strong>登船第一天就去搶購</strong>！達菲商店與 World of Disney 的達菲商品相似，不必跑兩間。</div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#1a4a2a,#2E7D32)">🌿</div>
      <div class="ci"><h3>National Geographic Store（國家地理商店）</h3><p>Deck 6 · 迪士尼郵輪首次 · 聯名限定</p>
        <div class="cmeta"><span class="tag tdeck">Deck 6</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <div class="mi"><div><div class="min">Disney Adventure × NatGeo 聯名 T恤 & 帽子</div></div></div>
      <div class="mi"><div><div class="min">冒險主題包款 Adventure Bags</div><div class="mid">機能背包、旅行包</div></div></div>
      <div class="mi"><div><div class="min">教育性紀念品 Educational Souvenirs</div><div class="mid">地圖、野生動物主題</div></div></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><span style="font-size:1.6rem">💅</span>
      <div class="ci"><h3>Marvel Style Studio（漫威造型工作室）</h3><p>Deck 19 · 英雄造型體驗</p>
        <div class="cmeta"><span class="tag tdeck">Deck 19</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <div class="mi"><div><div class="min">Marvel 英雄主題髮型 Marvel Hero Hairstyling</div></div></div>
      <div class="mi"><div><div class="min">主題彩妝 Themed Makeup</div><div class="mid">成人 & 兒童均可 / All Ages</div></div></div>
      <div class="mi"><div><div class="min">夜間成人品酒 Adult Beverage Tasting</div><div class="mid">特定時段轉型成人酒吧</div></div></div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><span style="font-size:1.6rem">👗</span>
      <div class="ci"><h3>Bibbidi Bobbidi Boutique（公主造型工作室）</h3><p>Deck 9 Town Square · 兒童公主造型</p>
        <div class="cmeta"><span class="tag tdeck">Deck 9</span><span class="tag kids">兒童 3–12歲</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <p class="cdesc">讓孩子化身為公主、騎士或海盜船長！專業造型師幫忙打扮，包含髮型、服裝及配件。</p>
      <div class="rn">💡 需提前透過 Navigator App 預訂，名額有限！禮賓客可130天前優先預約。</div>
    </div>
  </div>

  <div class="card" onclick="toggleCard(this)">
    <div class="card-hd"><div class="cbadge" style="background:linear-gradient(135deg,#C9A227,#F5C842)">💎</div>
      <div class="ci"><h3>Palace Treasures & 3 Wishes（禮賓精品）</h3><p>Deck 15 · 禮賓客限定</p>
        <div class="cmeta"><span class="tag tdeck">Deck 15</span><span class="tag tadult">禮賓客限定</span></div></div><span class="tarr">▼</span></div>
    <div class="card-body">
      <div class="mi"><div><div class="min">Palace Treasures</div><div class="mid">高端珠寶、奢侈精品 / Jewelry & Luxury Goods</div></div></div>
      <div class="mi"><div><div class="min">3 Wishes</div><div class="mid">禮賓限定服飾、限量收藏品 / Exclusive Apparel & Limited Collectibles</div></div></div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     8. NOTES
═══════════════════════════════════ -->

<section id="notes">
  <div class="sec-title">📋 注意事項</div>
  <div class="sec-sub">出發前必讀 · 入境表格 · 下船流程</div>

  <div class="ng">
    <div class="ngt">📄 新加坡入境表格（SGAC）</div>
    <div class="ni alert"><span class="ni-icon">⚠️</span><div class="ni-text"><strong>必填！入境前3天內提交</strong>：所有外籍旅客（包含孩童）入境新加坡前必須填寫 SG Arrival Card，違者可能被拒絕入境。</div></div>
    <div class="ni info"><span class="ni-icon">📱</span><div class="ni-text"><strong>填寫方式</strong>：至 <strong>eservices.ica.gov.sg</strong> 或下載 MyICA App（iOS / Android）免費填寫，約5–10分鐘完成。</div></div>
    <div class="ni tip"><span class="ni-icon">✅</span><div class="ni-text"><strong>填寫要點</strong>：護照號碼拼寫請與護照完全一致、姓名格式也要吻合、抵達日期（不是出發日）。<br>提交後會收到確認 Email，進關時無需列印（電子版即可）。</div></div>
    <a href="https://www.ica.gov.sg/enter-transit-depart/entering-singapore/sg-arrival-card" target="_blank" style="display:block;background:var(--gold);color:#0B1E3D;text-decoration:none;border-radius:9px;padding:9px 14px;text-align:center;font-weight:700;font-size:.8rem;margin-top:8px">🔗 前往 ICA 官網填寫 SGAC</a>
    <a href="https://eservices.ica.gov.sg/STO1/SGAC" target="_blank" style="display:block;background:rgba(255,255,255,.08);color:var(--cream);text-decoration:none;border-radius:9px;padding:8px 14px;text-align:center;font-size:.76rem;border:1px solid rgba(255,255,255,.15);margin-top:6px">📝 直接前往填表頁面</a>
  </div>

  <div class="ng">
    <div class="ngt">🚢 下船前注意事項</div>
    <div class="ni warn"><span class="ni-icon">🛄</span><div class="ni-text"><strong>下船日行李注意</strong>：下船前一晚（通常晚上10點前）需將大件行李放在門外走廊，貼上行李牌，工作人員會集中處理。<br>隔天早上在港口行李提取區取回。</div></div>
    <div class="ni info"><span class="ni-icon">🌅</span><div class="ni-text"><strong>下船早餐</strong>：3夜航程通常在第4天早上抵港（約7:00 AM）。早餐時間：6:30–8:30 AM，最晚9:00 AM 需離船。</div></div>
    <div class="ni tip"><span class="ni-icon">👑</span><div class="ni-text"><strong>禮賓客優先離船</strong>：享有優先下船，可比一般旅客更早離開，省去等待時間。</div></div>
    <div class="ni dark"><span class="ni-icon">🛃</span><div class="ni-text">下船後在新加坡郵輪中心通過移民局 & 海關檢查，如有攜帶購物品請留意免稅額度（一般為 SGD $500）。</div></div>
  </div>

  <div class="ng">
    <div class="ngt">🚫 禁止攜帶上船物品</div>
    <div class="ni alert"><span class="ni-icon">⛔</span><div class="ni-text"><strong>以下物品嚴禁！被查到可能被拒絕登船或面臨法律責任！</strong></div></div>
    <div class="proh-grid">
      <div class="proh-item"><span class="pi-icon">🔫</span><div class="pi-text">任何武器（槍枝、刀具、彈藥）Weapons</div></div>
      <div class="proh-item"><span class="pi-icon">💊</span><div class="pi-text">非法藥物、大麻 & CBD 製品 Illegal Drugs</div></div>
      <div class="proh-item"><span class="pi-icon">🚬</span><div class="pi-text">電子菸（新加坡法律禁止，罰款可達 SGD $2,000）E-Cigarettes</div></div>
      <div class="proh-item"><span class="pi-icon">🔌</span><div class="pi-text">延長線、插線板（火災危險）Power Strips</div></div>
      <div class="proh-item"><span class="pi-icon">👕</span><div class="pi-text">熨斗、蒸氣熨衣機 Irons / Steamers</div></div>
      <div class="proh-item"><span class="pi-icon">🍷</span><div class="pi-text">自帶酒精（葡萄酒限1瓶）Alcohol</div></div>
      <div class="proh-item"><span class="pi-icon">🍎</span><div class="pi-text">自製食品 & 開封食物 Homemade / Open Food</div></div>
      <div class="proh-item"><span class="pi-icon">🛹</span><div class="pi-text">滑板、直排輪、電動車 Skateboards / E-Scooters</div></div>
      <div class="proh-item"><span class="pi-icon">🏏</span><div class="pi-text">棒球棒、曲棍球棒 Baseball / Hockey Bats</div></div>
      <div class="proh-item"><span class="pi-icon">📡</span><div class="pi-text">無線遙控玩具 / 無人機 Drones / RC Toys</div></div>
      <div class="proh-item"><span class="pi-icon">🌊</span><div class="pi-text">衝浪板、浮板、游泳圈 Surfboards / Pool Noodles</div></div>
      <div class="proh-item"><span class="pi-icon">🎇</span><div class="pi-text">任何煙火 & 爆竹 Fireworks</div></div>
    </div>
    <div class="ni warn" style="margin-top:9px"><span class="ni-icon">⚠️</span><div class="ni-text"><strong>新加坡特別法律</strong>：電子菸在新加坡屬非法物品，攜帶入境可罰款至 SGD $2,000 甚至刑事責任！</div></div>
    <div class="ni info" style="margin-top:6px"><span class="ni-icon">ℹ️</span><div class="ni-text">被沒收的非危險品通常會保管在船上，離船時憑收據取回。</div></div>
  </div>

  <div class="ng">
    <div class="ngt">📅 登船 & 日程</div>
    <div class="ni alert"><span class="ni-icon">⚠️</span><div class="ni-text"><strong>上船後立刻搶訂！</strong>安全演習結束後角色合影、Palo 餐廳等熱門名額立即開放，熱門名額幾秒搶完。提前準備好 Navigator App。</div></div>
    <div class="ni dark"><span class="ni-icon">⚓</span><div class="ni-text" style="color:rgba(255,248,238,.85)"><strong>出發地點</strong>：Marina Bay Cruise Centre，61 Marina Coastal Dr。<strong>禮賓客</strong>建議出發前2小時抵達，享有專屬優先通道。</div></div>
    <div class="ni tip"><span class="ni-icon">📱</span><div class="ni-text"><strong>Navigator App 非常重要！</strong>船上Wi-Fi 連接後，可查看演出時間、預訂角色合影、餐廳預訂、當天活動。免費使用。</div></div>
  </div>

  <div class="ng">
    <div class="ngt">🍽️ 飲食注意</div>
    <div class="ni tip"><span class="ni-icon">✅</span><div class="ni-text"><strong>票價含</strong>：主餐廳、自助餐、快餐、軟式冰淇淋（24小時）。<strong>另計</strong>：Palo 系列、酒精、特殊增值服務。</div></div>
    <div class="ni dark"><span class="ni-icon">🕌</span><div class="ni-text" style="color:rgba(255,248,238,.85)">清真認證肉類於所有桌邊服務餐廳提供。無豬廚房：Cosmic Kebabs。也提供 Jain 嚴格素食（建議提前申請）。</div></div>
    <div class="ni tip"><span class="ni-icon">💡</span><div class="ni-text"><strong>隱藏菜單</strong>：米奇冰淇淋棒不在客房服務菜單上，直接告知工作人員即可！</div></div>
  </div>

  <div class="ng">
    <div class="ngt">💰 費用 & 準備</div>
    <div class="ni tip"><span class="ni-icon">💡</span><div class="ni-text"><strong>小費</strong>：建議每天每人 USD $14.5，通常自動計入帳單。也可主動給現金。</div></div>
    <div class="ni dark"><span class="ni-icon">☀️</span><div class="ni-text" style="color:rgba(255,248,238,.85)">赤道氣候，全年炎熱潮濕！帶好防曬、帽子、涼感衣物。（禮賓露台有免費防曬乳！）</div></div>
    <div class="ni dark"><span class="ni-icon">🌐</span><div class="ni-text" style="color:rgba(255,248,238,.85)">船上 Wi-Fi 需購買套餐（禮賓客有免費額度）。Navigator App 在區域網路中免費。</div></div>
  </div>
</section>

<!-- ═══════════════════════════════════
     9. CURRENCY
═══════════════════════════════════ -->

<section id="currency">
  <div class="sec-title">💱 匯率計算機</div>
  <div class="sec-sub">以台幣為基準手動填入 · 或自動更新</div>

  <div class="fx-card">
    <h3>🔄 匯率更新</h3>
    <p>自動更新（需網路）抓取最新匯率，或手動填入台灣銀行查詢到的匯率。</p>
    <div class="fx-update">
      <button class="btn-gold" onclick="fetchRates()">🌐 自動更新</button>
      <button class="btn-gold btn-sec" onclick="document.getElementById('manual-panel').style.display=document.getElementById('manual-panel').style.display==='none'?'block':'none'">✏️ 手動輸入</button>
    </div>
    <div class="fx-status" id="fx-status">尚未更新 · 使用預設匯率</div>
  </div>

  <!-- Manual panel - light bg, dark text -->

  <div class="manual-panel" id="manual-panel" style="display:none">
    <h3>✏️ 手動輸入匯率（以台幣 TWD 為基準）</h3>
    <p>查詢台灣銀行後填入：1 台幣 = 多少各幣種（建議用即期匯率）</p>
    <div class="manual-row">
      <div class="manual-lbl">🇸🇬 SGD</div>
      <input class="manual-input" id="m-sgd" type="number" step="0.0001" placeholder="1 TWD = ? SGD（約0.042）">
    </div>
    <div class="manual-row">
      <div class="manual-lbl">🇺🇸 USD</div>
      <input class="manual-input" id="m-usd" type="number" step="0.0001" placeholder="1 TWD = ? USD（約0.031）">
    </div>
    <div class="manual-row">
      <div class="manual-lbl">🇯🇵 JPY</div>
      <input class="manual-input" id="m-jpy" type="number" step="0.01" placeholder="1 TWD = ? JPY（約4.6）">
    </div>
    <button class="btn-apply" onclick="applyManual()">✅ 套用匯率</button>
    <a class="twdlink" href="https://rate.bot.com.tw/xrt?Lang=zh-TW" target="_blank">🏦 前往台灣銀行匯率查詢</a>
  </div>

  <div class="fx-card">
    <h3>💰 金額換算</h3>
    <p>輸入金額並選擇幣種，即時查看所有換算結果</p>
    <div class="fx-row">
      <input class="fx-input" id="fx-amount" type="number" placeholder="輸入金額" oninput="calcFX()">
      <select class="fx-sel" id="fx-from" onchange="calcFX()">
        <option value="TWD">🇹🇼 TWD 台幣</option>
        <option value="SGD">🇸🇬 SGD 新幣</option>
        <option value="USD">🇺🇸 USD 美元</option>
        <option value="JPY">🇯🇵 JPY 日幣</option>
      </select>
    </div>
    <div class="fx-results" id="fx-results">
      <div class="fx-res-item"><div class="flag">🇹🇼</div><div class="cname">台幣 TWD</div><div class="cval" id="r-twd">—</div></div>
      <div class="fx-res-item"><div class="flag">🇸🇬</div><div class="cname">新加坡幣 SGD</div><div class="cval" id="r-sgd">—</div></div>
      <div class="fx-res-item"><div class="flag">🇺🇸</div><div class="cname">美元 USD</div><div class="cval" id="r-usd">—</div></div>
      <div class="fx-res-item"><div class="flag">🇯🇵</div><div class="cname">日幣 JPY</div><div class="cval" id="r-jpy">—</div></div>
    </div>
  </div>

  <div class="fx-card">
    <h3>🚢 常見費用快速換算</h3>
    <p>點擊即自動換算</p>
    <div style="display:grid;gap:5px">
      <div class="phrase-item" onclick="quickCalc(14.5,'USD')"><div><div class="pzh">每日小費 USD $14.5／人</div><div class="pen">Daily Gratuity per person</div></div><span class="pcopy">換算</span></div>
      <div class="phrase-item" onclick="quickCalc(958,'USD')"><div><div class="pzh">3夜起始票價 USD $958／2人</div><div class="pen">3-Night minimum fare for 2 guests</div></div><span class="pcopy">換算</span></div>
      <div class="phrase-item" onclick="quickCalc(1318,'USD')"><div><div class="pzh">4夜起始票價 USD $1,318／2人</div><div class="pen">4-Night minimum fare</div></div><span class="pcopy">換算</span></div>
      <div class="phrase-item" onclick="quickCalc(50,'SGD')"><div><div class="pzh">船上消費 SGD $50</div><div class="pen">Onboard spending budget</div></div><span class="pcopy">換算</span></div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════
     10. TRANSLATE
═══════════════════════════════════ -->

<section id="translate">
  <div class="sec-title">🌐 翻譯工具</div>
  <div class="sec-sub">離線翻譯 · 實用英文會話</div>
  <div class="tr-card">
    <h3>📲 Google 翻譯離線使用</h3>
    <p>出發前下載英文語言包，可在無網路下翻譯（包含相機掃描菜單！）</p>
    <a class="tr-btn" href="https://translate.google.com" target="_blank">🌐 開啟 Google 翻譯</a>
    <a class="tr-btn sec" href="https://apps.apple.com/app/google-translate/id414706506" target="_blank">🍎 iOS 版下載</a>
    <a class="tr-btn sec" href="https://play.google.com/store/apps/details?id=com.google.android.apps.translate" target="_blank">📱 Android 版下載</a>
  </div>
  <div class="tr-card">
    <h3>📷 相機翻譯教學</h3>
    <p>Google 翻譯 → 「相機」圖示 → 對準英文菜單 → 自動中文翻譯。建議出發前下載「英文」離線語言包。</p>
  </div>
  <hr class="divider">
  <div class="sec-title" style="font-size:1rem;margin-bottom:3px">💬 實用英文會話</div>
  <div class="sec-sub">點擊複製到剪貼簿</div>
  <div class="phrase-item" onclick="copyPhrase(this,'I have a food allergy. I cannot eat [ingredient].')"><div><div class="pzh">我有食物過敏</div><div class="pen">I have a food allergy. I cannot eat [ingredient].</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Is this dish halal?')"><div><div class="pzh">這是清真的嗎？</div><div class="pen">Is this dish halal?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Do you have a vegetarian option?')"><div><div class="pzh">有素食選項嗎？</div><div class="pen">Do you have a vegetarian option?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'What time does the show start?')"><div><div class="pzh">演出幾點開始？</div><div class="pen">What time does the show start?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Where can I meet [character name]?')"><div><div class="pzh">在哪裡可以和角色合影？</div><div class="pen">Where can I meet [character name]?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Can I get the Mickey ice cream bar delivered to my room?')"><div><div class="pzh">可以叫米奇冰淇淋棒外送到房間嗎？</div><div class="pen">Can I get the Mickey ice cream bar to my room?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'I am a concierge guest. My room number is 16123.')"><div><div class="pzh">我是禮賓客，房號 16123</div><div class="pen">I am a concierge guest. My room number is 16123.</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Where is the Concierge Lounge?')"><div><div class="pzh">禮賓廳在哪裡？</div><div class="pen">Where is the Concierge Lounge?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Where can I get the complimentary popcorn for the theater?')"><div><div class="pzh">可以在哪裡領取免費爆米花？</div><div class="pen">Where can I get the complimentary popcorn for the theater?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'What time does the fireworks show start tonight?')"><div><div class="pzh">今晚煙火秀幾點開始？</div><div class="pen">What time does the fireworks show start tonight?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Please bring the bill.')"><div><div class="pzh">請給我帳單</div><div class="pen">Please bring the bill.</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Is this included in the cruise fare?')"><div><div class="pzh">這含在票價內嗎？</div><div class="pen">Is this included in the cruise fare?</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'I would like to book a character meet and greet.')"><div><div class="pzh">我想預訂角色合影</div><div class="pen">I would like to book a character meet and greet.</div></div><span class="pcopy">複製</span></div>
  <div class="phrase-item" onclick="copyPhrase(this,'Can I book a table at Palo Trattoria for tonight?')"><div><div class="pzh">可以訂今晚 Palo 餐廳嗎？</div><div class="pen">Can I book a table at Palo Trattoria for tonight?</div></div><span class="pcopy">複製</span></div>
  <hr class="divider">
  <div class="tr-card" style="text-align:center;padding:13px">
    <p style="font-size:.72rem;color:var(--txt-dim)">📌 資訊依據 2026年3月實際搭乘報告整理，菜單及演出時間可能隨航次調整，以 Disney Navigator App 公告為準。</p>
  </div>
</section>

<script>
// ── RATES (TWD base fallback) ──
let rates = {TWD:1, SGD:0.0414, USD:0.0308, JPY:4.62};
let ratesUpdated = null;

function switchTab(id){
  document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
  document.querySelectorAll('#mainnav button').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  const tabs=['overview','shows','dining','roomsvc','concierge','chars','shops','notes','currency','translate'];
  const idx=tabs.indexOf(id);
  if(idx>=0) document.querySelectorAll('#mainnav button')[idx].classList.add('active');
  window.scrollTo(0,0);
}

function toggleCard(card){
  const was=card.classList.contains('open');
  card.parentElement.querySelectorAll('.card.open').forEach(c=>c.classList.remove('open'));
  if(!was) card.classList.add('open');
}

function switchCat(cat, section){
  let fullId;
  if(section==='roomsvc') fullId='rscat-'+cat;
  else if(section==='concierge') fullId='cocat-'+cat;
  else if(section==='chars') fullId='chcat-'+cat;
  else fullId='dcat-'+cat;
  const sec=document.getElementById(section);
  sec.querySelectorAll('.clist').forEach(l=>l.classList.remove('active'));
  sec.querySelectorAll('.cbt').forEach(b=>b.classList.remove('active'));
  const tgt=document.getElementById(fullId);
  if(tgt) tgt.classList.add('active');
  if(event&&event.target) event.target.classList.add('active');
}

// ── CURRENCY ──
async function fetchRates(){
  const st=document.getElementById('fx-status');
  st.textContent='正在更新…'; st.className='fx-status';
  try{
    const r=await fetch('https://api.exchangerate-api.com/v4/latest/TWD');
    if(!r.ok) throw new Error();
    const d=await r.json();
    rates.SGD=d.rates.SGD||rates.SGD;
    rates.USD=d.rates.USD||rates.USD;
    rates.JPY=d.rates.JPY||rates.JPY;
    ratesUpdated=new Date();
    st.textContent='✅ 已更新：'+ratesUpdated.toLocaleString('zh-TW'); st.className='fx-status ok';
    calcFX();
  }catch(e){
    try{
      const r2=await fetch('https://open.er-api.com/v6/latest/TWD');
      const d2=await r2.json();
      rates.SGD=d2.rates.SGD||rates.SGD;
      rates.USD=d2.rates.USD||rates.USD;
      rates.JPY=d2.rates.JPY||rates.JPY;
      ratesUpdated=new Date();
      st.textContent='✅ 已更新：'+ratesUpdated.toLocaleString('zh-TW'); st.className='fx-status ok';
      calcFX();
    }catch(e2){
      st.textContent='❌ 更新失敗，請使用手動輸入'; st.className='fx-status err';
    }
  }
}

function applyManual(){
  const s=parseFloat(document.getElementById('m-sgd').value);
  const u=parseFloat(document.getElementById('m-usd').value);
  const j=parseFloat(document.getElementById('m-jpy').value);
  if(s>0) rates.SGD=s;
  if(u>0) rates.USD=u;
  if(j>0) rates.JPY=j;
  document.getElementById('fx-status').textContent='✅ 手動匯率已套用（以 TWD 台幣為基準）';
  document.getElementById('fx-status').className='fx-status ok';
  document.getElementById('manual-panel').style.display='none';
  calcFX();
}

function toTWD(amount,from){
  if(from==='TWD') return amount;
  return amount/rates[from];
}
function fmt(n,curr){
  if(curr==='JPY') return Math.round(n).toLocaleString();
  if(curr==='TWD') return n.toFixed(0);
  return n.toFixed(2);
}
function calcFX(){
  const amt=parseFloat(document.getElementById('fx-amount').value);
  const from=document.getElementById('fx-from').value;
  if(isNaN(amt)||amt<=0){
    ['twd','sgd','usd','jpy'].forEach(c=>document.getElementById('r-'+c).textContent='—');
    return;
  }
  const inTWD=toTWD(amt,from);
  document.getElementById('r-twd').textContent='NT$ '+fmt(inTWD,'TWD');
  document.getElementById('r-sgd').textContent='S$ '+fmt(inTWD*rates.SGD,'SGD');
  document.getElementById('r-usd').textContent='$ '+fmt(inTWD*rates.USD,'USD');
  document.getElementById('r-jpy').textContent='¥ '+fmt(inTWD*rates.JPY,'JPY');
}
function quickCalc(amount, currency){
  document.getElementById('fx-amount').value=amount;
  document.getElementById('fx-from').value=currency;
  switchTab('currency');
  calcFX();
}

function copyPhrase(el,text){
  navigator.clipboard.writeText(text).then(()=>{
    const btn=el.querySelector('.pcopy');
    btn.textContent='✓ 已複製'; btn.classList.add('pok');
    setTimeout(()=>{btn.textContent='複製'; btn.classList.remove('pok')},2000);
  }).catch(()=>{
    const ta=document.createElement('textarea');
    ta.value=text; document.body.appendChild(ta); ta.select(); document.execCommand('copy'); document.body.removeChild(ta);
    const btn=el.querySelector('.pcopy');
    btn.textContent='✓ 已複製'; btn.classList.add('pok');
    setTimeout(()=>{btn.textContent='複製'; btn.classList.remove('pok')},2000);
  });
}
</script>

</body>
</html>
