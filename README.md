<!DOCTYPE html>

<html lang="zh-TW">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Disney Adventure 探險號 禮賓旅客指南</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { background: #08111f; color: #e8dcc8; font-family: 'Lato', sans-serif; }
  .app { min-height: 100vh; background: linear-gradient(160deg, #08111f 0%, #0c1a30 60%, #08111f 100%); }

/* HEADER */
.header {
background: linear-gradient(180deg, #060e1c 0%, #0f1e3a 100%);
border-bottom: 1px solid #1e3060;
padding: 14px 18px 10px;
text-align: center;
position: sticky; top: 0; z-index: 100;
box-shadow: 0 2px 20px rgba(0,0,0,0.5);
}
.header-title {
font-family: ‘Cinzel’, serif;
font-size: 17px; font-weight: 700; color: #f0d060;
letter-spacing: 2px;
text-shadow: 0 0 24px rgba(240,208,96,0.5);
}
.header-sub { font-size: 11px; color: #7090cc; letter-spacing: 1.5px; margin-top: 2px; }
.room-badge {
display: inline-block;
background: linear-gradient(135deg, #b8872a, #f0d060);
color: #060e1c; font-size: 10px; font-weight: 700;
padding: 2px 12px; border-radius: 20px; margin-top: 5px; letter-spacing: 1px;
}

/* NAV */
.nav-scroll {
display: flex; overflow-x: auto; gap: 6px;
padding: 10px 14px;
background: #090f1e; border-bottom: 1px solid #152040;
scrollbar-width: none;
}
.nav-scroll::-webkit-scrollbar { display: none; }
.nav-btn {
flex-shrink: 0;
background: #101c34; border: 1px solid #1e3060; color: #7090cc;
border-radius: 20px; padding: 6px 13px; font-size: 11px;
cursor: pointer; white-space: nowrap;
transition: all 0.2s; font-family: ‘Lato’, sans-serif;
}
.nav-btn.active, .nav-btn:hover {
background: linear-gradient(135deg, #1a3060, #2548a0);
border-color: #3a60c0; color: #f0d060;
}

/* CONTENT */
.content { padding: 14px; max-width: 500px; margin: 0 auto; }
.section { display: none; }
.section.active { display: block; }

/* CARDS & TYPOGRAPHY */
.section-title {
font-family: ‘Cinzel’, serif;
font-size: 15px; color: #f0d060;
border-bottom: 1px solid #1e3060;
padding-bottom: 8px; margin-bottom: 14px; letter-spacing: 1px;
}
.card { background: #0e1828; border: 1px solid #182848; border-radius: 12px; padding: 13px; margin-bottom: 10px; }
.card-title { font-size: 13px; font-weight: 700; color: #c8b070; margin-bottom: 7px; }
.card-body { font-size: 12px; color: #8eaacf; line-height: 1.75; }

/* TAGS */
.tag {
display: inline-block;
background: #121e38; color: #6888c0; border: 1px solid #1e3060;
font-size: 10px; padding: 2px 8px; border-radius: 12px; margin: 2px;
}
.tag-gold { background: #1e1600; color: #f0d060; border-color: #4a3800; }
.tag-green { background: #081808; color: #50c870; border-color: #183828; }

/* MESSAGE BOXES */
.warn-box {
background: #221200; border: 1px solid #702808;
border-radius: 8px; padding: 10px 13px;
font-size: 12px; color: #e09060; margin: 8px 0; line-height: 1.7;
}
.info-box {
background: #00101e; border: 1px solid #183860;
border-radius: 8px; padding: 10px 13px;
font-size: 12px; color: #60a0e0; margin: 8px 0; line-height: 1.7;
}
.gold-box {
background: #120e00; border: 1px solid #483200;
border-radius: 8px; padding: 10px 13px;
font-size: 12px; color: #f0d060; margin: 8px 0; line-height: 1.7;
}

/* SCHEDULE */
.schedule-row {
display: flex; justify-content: space-between; align-items: center;
padding: 7px 0; border-bottom: 1px solid #131f34; font-size: 12px;
}
.schedule-row:last-child { border-bottom: none; }
.time-badge {
background: #152040; color: #70a8f0;
padding: 2px 8px; border-radius: 8px;
font-size: 11px; font-weight: 700; flex-shrink: 0;
}

/* MENU ITEMS */
.menu-item {
display: flex; justify-content: space-between;
padding: 7px 0; border-bottom: 1px dashed #131f34; font-size: 12px;
}
.menu-item:last-child { border-bottom: none; }
.menu-item-name { color: #c0d0e8; flex: 1; }
.menu-item-en { color: #485870; font-size: 10px; }
.menu-item-price { color: #f0d060; flex-shrink: 0; margin-left: 8px; }
.menu-item-price.paid { color: #e08060; }
.menu-item-price.free { color: #60c870; }

/* DECK MAP */
.deck-map {
background: #050d1a; border: 1px solid #152040;
border-radius: 12px; padding: 14px;
font-size: 11px; color: #7090cc;
}
.deck-row {
display: flex; align-items: flex-start;
padding: 8px 0; border-bottom: 1px solid #0a1428; gap: 10px;
}
.deck-row:last-child { border-bottom: none; }
.deck-num {
background: #152040; color: #70a8f0;
width: 34px; height: 34px; border-radius: 8px;
display: flex; align-items: center; justify-content: center;
font-weight: 700; font-size: 13px; flex-shrink: 0; margin-top: 2px;
}
.deck-num.hl { background: linear-gradient(135deg, #b8872a, #f0d060); color: #060e1c; }
.deck-info { flex: 1; }
.deck-name { color: #c8b070; font-weight: 700; font-size: 12px; margin-bottom: 2px; }
.deck-locs { color: #485870; font-size: 10px; line-height: 1.6; }

/* CURRENCY */
.currency-input {
background: #0e1828; border: 1px solid #1e3060;
border-radius: 8px; padding: 10px 13px;
color: #e8dcc8; font-size: 15px; font-family: ‘Lato’, sans-serif;
width: 100%; outline: none; margin: 4px 0 10px;
}
.currency-input:focus { border-color: #3a60c0; }
.currency-result {
background: #09152a; border: 1px solid #152848;
border-radius: 8px; padding: 10px 13px; margin: 5px 0;
display: flex; justify-content: space-between; align-items: center;
}
.currency-label { font-size: 11px; color: #6080b8; }
.currency-value { font-size: 15px; color: #f0d060; font-weight: 700; }
.rate-row {
display: flex; gap: 8px; align-items: center;
padding: 6px 0; border-bottom: 1px solid #131f34; font-size: 12px;
}
.rate-label { color: #6080b8; flex: 1; }
.rate-input {
background: #09152a; border: 1px solid #1e3060;
border-radius: 6px; padding: 4px 8px;
color: #f0d060; font-size: 12px; width: 80px;
outline: none; text-align: right;
}
.flex-row { display: flex; gap: 8px; align-items: center; }
.flex-row .currency-input { margin-bottom: 0; }

/* LINK BUTTONS */
.link-btn {
display: block; width: 100%;
background: linear-gradient(135deg, #182858, #203878);
border: 1px solid #3060b0; color: #a0c0f0;
font-size: 13px; font-weight: 700; padding: 13px;
border-radius: 10px; cursor: pointer; margin-bottom: 8px;
font-family: ‘Lato’, sans-serif; letter-spacing: 1px;
text-decoration: none; text-align: center; transition: all 0.2s;
}
.link-btn:hover { background: linear-gradient(135deg, #203878, #2a4898); }
.link-btn-green { background: linear-gradient(135deg, #102818, #183820); border-color: #306840; color: #80e090; }
.link-btn-green:hover { background: linear-gradient(135deg, #183820, #204828); }
.link-btn-blue { background: linear-gradient(135deg, #101828, #182438); border-color: #2848a0; color: #80a8f0; }
.link-btn-blue:hover { background: linear-gradient(135deg, #182438, #202e48); }

/* ACCORDION */
.accordion-btn {
width: 100%; background: #101c34; border: 1px solid #1e3060;
color: #c8b070; font-size: 12px; font-weight: 700;
padding: 11px 13px; border-radius: 8px;
cursor: pointer; text-align: left; margin-bottom: 3px;
font-family: ‘Lato’, sans-serif;
display: flex; justify-content: space-between; align-items: center;
transition: all 0.2s;
}
.accordion-btn:hover { background: #182848; }
.accordion-arrow { font-size: 10px; color: #4060a0; flex-shrink: 0; }
.accordion-content {
background: #090f1e; border: 1px solid #152040;
border-radius: 8px; padding: 12px 13px; margin-bottom: 8px;
display: none;
}
.accordion-content.open { display: block; }

/* STEPS */
.step { display: flex; gap: 10px; padding: 6px 0; font-size: 12px; }
.step-num {
background: linear-gradient(135deg, #b8872a, #f0d060);
color: #060e1c; width: 22px; height: 22px; border-radius: 50%;
display: flex; align-items: center; justify-content: center;
font-weight: 700; font-size: 11px; flex-shrink: 0;
}
.step-text { color: #8eaacf; line-height: 1.65; }

/* CONCIERGE */
.conc-cat {
background: linear-gradient(135deg, #120e00, #161200);
border: 1px solid #483200; border-radius: 10px;
padding: 11px 13px; margin-bottom: 10px;
}
.conc-cat-title {
font-family: ‘Cinzel’, serif; font-size: 12px;
color: #f0d060; margin-bottom: 8px;
}
.conc-item {
font-size: 11px; color: #c8b070; padding: 4px 0;
border-bottom: 1px solid #1e1800; line-height: 1.6;
}
.conc-item:last-child { border-bottom: none; }

/* FORBIDDEN / TIPS LISTS */
.forbidden-item {
font-size: 12px; color: #d07060; padding: 5px 0;
border-bottom: 1px solid #1e0808; line-height: 1.6;
}
.forbidden-item:last-child { border-bottom: none; }
.tips-item {
font-size: 12px; color: #70c880; padding: 5px 0;
border-bottom: 1px solid #081808; line-height: 1.6;
}
.tips-item:last-child { border-bottom: none; }

/* UTILITIES */
.mb8 { margin-bottom: 8px; }
.mb10 { margin-bottom: 10px; }
.mb12 { margin-bottom: 12px; }
.mb14 { margin-bottom: 14px; }
.mt8 { margin-top: 8px; }
.mt4 { margin-top: 4px; }
.small-label { font-size: 11px; color: #405080; margin-bottom: 4px; }
.bottom-pad { height: 24px; }
.edit-btn {
background: #152040; border: 1px solid #1e3060; color: #70a8f0;
font-size: 11px; padding: 4px 10px; border-radius: 8px; cursor: pointer;
font-family: ‘Lato’, sans-serif;
}
.rate-value { color: #f0d060; font-size: 13px; font-weight: 700; }
.card-title-row { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; }
.schedule-name { color: #90b0d0; font-size: 11px; margin-left: 10px; }
</style>

</head>
<body>
<div class="app">

  <!-- HEADER -->

  <div class="header">
    <div class="header-title">✦ Disney Adventure ✦</div>
    <div class="header-sub">探險號 · 新加坡 Marina Bay · 禮賓旅客專屬</div>
    <div class="room-badge">房號 16123 · Concierge Inside · 第16甲板</div>
  </div>

  <!-- NAV -->

  <div class="nav-scroll" id="navScroll"></div>

  <!-- CONTENT -->

  <div class="content" id="appContent"></div>

</div>

<script>
// ===================== DATA =====================

const NAV_ITEMS = [
  { id:"deck",       icon:"🗺️", label:"甲板平面圖" },
  { id:"shows",      icon:"🎭", label:"秀/表演" },
  { id:"restaurants",icon:"🍽️", label:"餐廳" },
  { id:"shops",      icon:"🛍️", label:"商店" },
  { id:"roomservice",icon:"🛎️", label:"客房點餐" },
  { id:"concierge",  icon:"👑", label:"禮賓服務" },
  { id:"activities", icon:"🎢", label:"遊樂設施" },
  { id:"translate",  icon:"🌐", label:"離線翻譯" },
  { id:"currency",   icon:"💱", label:"匯率換算" },
  { id:"notes",      icon:"📋", label:"注意事項" },
];

const DECK_DATA = [
  { num:19, hl:false, name:"第19甲板 — Marvel Landing", locs:"Ironcycle Test Run（過山車，最長海上過山車）・Pym Quantum Racers（蟻人賽車）・Groot Galaxy Spin（旋轉設施）・Marvel Style Studio（漫威造型體驗）・Marvel角色見面" },
  { num:18, hl:false, name:"第18甲板", locs:"Infinity Pool（Iron Man主題景觀游泳池）・Infinity Bar" },
  { num:17, hl:false, name:"第17甲板 — Toy Story Place", locs:"Sunnyside Family Pool（家庭主泳池）・Woody & Jessie's Wild Slides（水滑道）・Flying Saucer Splash Zone・Toy Story Splash Pad・戶外大螢幕・Pizza Planet・Wheezy's Freezies（霜淇淋）" },
  { num:16, hl:true,  name:"第16甲板 ★ 你的房間 & Wayfinder Bay", locs:"房號 16123（禮賓內艙房）· Wayfinder Bay（Moana主題水池＋表演廣場）・Wayfinder Bar・Moana: Call of the Sea舞台" },
  { num:15, hl:false, name:"第15甲板 — 禮賓私人甲板", locs:"禮賓專屬 Opulence Spa & Fitness・禮賓私人戶外日光浴甲板（僅房卡可進入）" },
  { num:13, hl:false, name:"第13甲板", locs:"客艙甲板（無公共設施）" },
  { num:12, hl:false, name:"第12甲板", locs:"客艙甲板" },
  { num:11, hl:false, name:"第11甲板 — San Fransokyo Street", locs:"Big Hero 6主題街道・Baymax Cinemas（4銀幕電影院）・Big Hero Arcade・Hiro Training Zone・Edge（青少年11-14歲）・Vibe（青少年14-17歲）・Duffy & Friends Shop（全球首間郵輪版）・National Geographic Shop・Alley Cat Cafe" },
  { num:10, hl:false, name:"第10甲板 — Discovery Reef + 成人餐廳", locs:"Discovery Reef（小美人魚/海底主題開放露台）・Treasures Untold商店・Stitch's 'Ohana Grill・Cosmic Kebabs・Bewitching Boba & Brews・Mike & Sulley's Flavors of Asia（付費）・Palo Trattoria（付費，第10-11層）" },
  { num:9,  hl:false, name:"第9甲板 — Town Square（下層）", locs:"Walt Disney Theatre（主劇院：Remember / Disney Seas The Adventure）・Bibbidi Bobbidi Boutique・Oceaneer Club（3-10歲兒童俱樂部）" },
  { num:8,  hl:false, name:"第8甲板 — Town Square（中層）", locs:"Hollywood Spotlight Club（輪替餐廳/下午茶）・D Lounge・多功能活動空間" },
  { num:7,  hl:false, name:"第7甲板 — Imagination Garden上層", locs:"角色見面廣場・Gramma Tala's Kitchen（Moana主題）・Mowgli's Eatery（Jungle Book主題）" },
  { num:6,  hl:false, name:"第6甲板 — Imagination Garden下層 / Garden Stage", locs:"Garden Stage三層挑高LED主舞台（Let's Set Sail・Avengers Assemble!・Duffy秀・Captain Jack秀・Baymax Expo）・Buccaneer Bar・Tiana's Bayou Lounge" },
  { num:5,  hl:false, name:"第5甲板 — Town Square主層", locs:"World of Disney（主店）・World of Disney Too・Art of Disney・Diamonds and Wishes（珠寶）・Palo Café・Taverna Portorosso・Spellbound雞尾酒吧・輪替主餐廳（Navigator's Club・Animator's Palate・Pixar Market・Animator's Table・Enchanted Summer）" },
  { num:2,  hl:false, name:"第2甲板 — 碼頭層", locs:"上/下船出入口・Marina Bay Cruise Centre新加坡" },
];

const SHOWS_DATA = [
  {
    title:"🚢 Let's Set Sail 出航派對",
    loc:"第6-8甲板 Garden Stage（Imagination Garden）", dur:"約45分鐘",
    desc:"登船當日舉行的出航慶典，在探險號中央廣場Garden Stage舉行。米奇、米妮與各迪士尼角色登場帶動氣氛。注意：探險號沒有傳統頂層甲板出航儀式，改在室內/半戶外廣場舉行，全航次會舉行多場。",
    tip:"禮賓旅客可先在貴賓室享用歡迎輕食，再下來參與出航派對。",
    schedule:[{time:"登船日下午（出發前）",name:"Let's Set Sail派對（多場）"}]
  },
  {
    title:"🦸 Avengers Assemble!",
    loc:"第6-8甲板 Garden Stage（三層挑高LED螢幕）", dur:"約40分鐘",
    desc:"探險號最強表演！Marvel英雄（蜘蛛人、鋼鐵人、美國隊長、黑豹、雷神、猩紅女巫）對決反派（洛基、紅骷髏、任務大師）。壓軸由Deadpool登場跳Bye Bye Bye！有高空特技、吊鋼絲、煙火特效，視覺震撼度極高。",
    tip:"通常每晚兩個場次，提前30分鐘佔位。禮賓旅客享優先座位。",
    schedule:[{time:"每航次各晚",name:"Avengers Assemble!（場次一）"},{time:"同晚稍後",name:"Avengers Assemble!（場次二）"}]
  },
  {
    title:"🐻 Duffy and The Friend Ship",
    loc:"第6-8甲板 Garden Stage", dur:"約35分鐘",
    desc:"Duffy熊與友人（ShellieMay、Gelatoni、StellaLou、CookieAnn、'Olu Mel、LinaBell）的溫馨航海音樂劇，由海鷗Tippy Blue引導。Duffy家族首次登上迪士尼郵輪的全新表演！",
    schedule:[{time:"每航次各晚（多場）",name:"Duffy and The Friend Ship"}]
  },
  {
    title:"🏴‍☠️ Captain Jack Sparrow & The Siren Queen",
    loc:"第6-8甲板 Garden Stage", dur:"約35分鐘",
    desc:"傑克船長與謎樣海妖女王的奪寶冒險！設有觀眾互動環節，以及一隻會噴墨汁的巨型章魚特效道具，充滿海盜幽默。",
    schedule:[{time:"每航次各晚（多場）",name:"Captain Jack Sparrow"}]
  },
  {
    title:"🤖 Baymax Super Exercise Expo",
    loc:"第6-8甲板 Garden Stage", dur:"約30分鐘",
    desc:"與大白（Baymax）一起做健康體操！充滿歡笑的全家互動節目，老少咸宜。Baymax會帶全場一起做各種搞笑但實用的健康動作。",
    schedule:[{time:"每日早/午排程",name:"Baymax Super Exercise Expo"}]
  },
  {
    title:"🌺 Moana: Call of the Sea",
    loc:"第16甲板 Wayfinder Bay（水池旁戶外舞台）", dur:"約30分鐘",
    desc:"以真實大海為背景的Moana主題現場秀，結合音樂、舞蹈與精彩布偶藝術，水池會成為表演舞台的一部分。非常壯觀。Disney提醒空間有限，請提早就座。",
    tip:"你的房間16123就在第16甲板，步行幾步即可到達Wayfinder Bay！晚場加上海風格外夢幻。",
    schedule:[{time:"每日排程（查Navigator App）",name:"Moana: Call of the Sea"}]
  },
  {
    title:"🎭 Remember & Disney Seas The Adventure",
    loc:"第9甲板 Walt Disney Theatre（室內主劇院）", dur:"約50分鐘",
    desc:"兩齣迪士尼郵輪原創的百老匯級製作：「Remember」以瓦力（Wall-E）與Eve為主角的感人愛情故事；「Disney Seas The Adventure」為迪士尼郵輪特製航海冒險秀，兩齣輪替演出。",
    tip:"劇院需入場，提前20分鐘排隊。禮賓旅客享優先座位。",
    schedule:[{time:"每晚（輪替）",name:"查Navigator App確認當日劇目"}]
  },
  {
    title:"🦁 The Lion King: Celebration in the Sky",
    loc:"戶外甲板（夜間煙火秀）", dur:"約15分鐘",
    desc:"全球唯一在郵輪上施放煙火的表演！以獅子王為主題，由寶萊塢巨星Shah Rukh Khan旁白，在探險號開放甲板欣賞夜空煙火。",
    tip:"注意：4晚航程通常含此秀，3晚航程可能不包含，請查詢行程確認。",
    schedule:[{time:"4晚航程某夜（天氣良好時）",name:"Lion King Fireworks"}]
  },
  {
    title:"🎨 Mickey's Color Spin Dance Party",
    loc:"第6-8甲板 Garden Stage", dur:"約30分鐘",
    desc:"米奇主題全家歌舞互動派對，搭配繽紛色彩特效，全場跟著迪士尼角色一起歡舞。",
    schedule:[{time:"每日排程",name:"Mickey's Color Spin Dance Party"}]
  },
];

const RESTS_DATA = [
  {
    name:"Navigator's Club 航海家俱樂部", deck:"第5甲板", type:"輪替主餐廳 A組", cat:"精緻西式",
    desc:"6間輪替餐廳中A組之一，與Animator's Palate和Pixar Market同組輪替。以航海探險為主題，充滿復古航海裝飾風格。",
    menu:[{zh:"龍蝦濃湯",en:"Lobster Bisque",price:"—"},{zh:"慢燉牛短肋",en:"Braised Short Rib",price:"—"},{zh:"烤鮭魚",en:"Roasted Salmon",price:"—"},{zh:"巧克力慕斯",en:"Chocolate Mousse",price:"—"}]
  },
  {
    name:"Animator's Palate 動畫家調色盤", deck:"第5甲板", type:"輪替主餐廳 A組", cat:"互動主題",
    desc:"迪士尼招牌互動餐廳，牆面螢幕隨用餐播放動畫。A組輪替（與Navigator's Club和Pixar Market同組）。探險號有Palate和Table兩間同主題餐廳分屬A/B兩組。",
    menu:[{zh:"奶油玉米湯",en:"Cream Corn Soup",price:"—"},{zh:"義式燉飯",en:"Risotto",price:"—"},{zh:"炙烤牛排",en:"Grilled Sirloin",price:"—"},{zh:"提拉米蘇",en:"Tiramisu",price:"—"}]
  },
  {
    name:"Pixar Market 皮克斯市集", deck:"第5甲板", type:"輪替主餐廳 A組（早/午自助）", cat:"Pixar主題",
    desc:"A組輪替餐廳，以《超人特攻隊》《怪獸大學》《腦筋急轉彎》《青春養成記》為主題。早/午為自助形式，晚餐為輪替主餐廳。探險號獨有設計。",
    menu:[{zh:"早午自助（亞洲/西式）",en:"Buffet",price:"免費"},{zh:"晚餐輪替主菜",en:"Rotational Dinner",price:"—"}]
  },
  {
    name:"Hollywood Spotlight Club 好萊塢聚光燈", deck:"第8甲板", type:"輪替主餐廳 B組", cat:"好萊塢黃金年代",
    desc:"B組輪替餐廳，以1920-50年代好萊塢電影海報裝飾風格為主題，提供精緻西式料理。另外也是「Royal Society for Friendship and Tea」下午茶體驗的場地（需額外付費）。",
    menu:[{zh:"紐約客牛排",en:"NY Strip Steak",price:"—"},{zh:"香煎海鱸",en:"Pan-Seared Sea Bass",price:"—"},{zh:"奶油蝦義大利麵",en:"Shrimp Pasta",price:"—"},{zh:"紐約芝士蛋糕",en:"NY Cheesecake",price:"—"}]
  },
  {
    name:"Animator's Table", deck:"第5甲板", type:"輪替主餐廳 B組", cat:"動畫主題",
    desc:"Animator's Palate的姊妹餐廳，B組輪替（與Hollywood Spotlight Club和Enchanted Summer同組）。同樣以動畫為主題但菜單有所不同。",
    menu:[{zh:"鮮蝦雞尾酒",en:"Shrimp Cocktail",price:"—"},{zh:"雞胸佐蘑菇醬",en:"Chicken with Mushroom Sauce",price:"—"},{zh:"時蔬燉飯",en:"Vegetable Risotto",price:"—"},{zh:"草莓芝士蛋糕",en:"Strawberry Cheesecake",price:"—"}]
  },
  {
    name:"Enchanted Summer 魔法夏日", deck:"第5甲板", type:"輪替主餐廳 B組（早/午自助）", cat:"迪士尼公主主題",
    desc:"B組輪替餐廳，以迪士尼公主為主題。早/午自助，晚餐輪替。與Hollywood Spotlight Club和Animator's Table同組。",
    menu:[{zh:"早午自助（含亞洲/西式）",en:"Buffet",price:"免費"},{zh:"晚餐輪替主菜",en:"Rotational Dinner",price:"—"}]
  },
  {
    name:"Palo Trattoria 帕洛義式餐廳", deck:"第10-11甲板（船尾）", type:"★ 需付費預訂・成人限定(18+)", cat:"頂級義式料理",
    desc:"迪士尼郵輪經典成人餐廳Palo的探險號版本。以皮克斯《Luca》天文夢境為靈感，閃爍星座月光裝飾令人驚艷，橫跨兩層。菜色以精緻義式料理聞名，探險號特有的特調干邑可購買收藏。強烈建議禮賓旅客出發前120天即預訂。",
    menu:[{zh:"海鮮拼盤（龍蝦/蝦/貽貝/燻鮭魚）",en:"Seafood Antipasto",price:"套餐含"},{zh:"茄子捲佐瑞可達起司",en:"Rollatini Melanzane",price:"套餐含"},{zh:"帕瑪森雞胸佐番茄羅勒",en:"Parmesan Chicken Breast",price:"套餐含"},{zh:"黃鰭吞拿魚Crudo",en:"Yellowfin Crudo",price:"套餐含"},{zh:"提拉米蘇",en:"Tiramisu",price:"套餐含"}]
  },
  {
    name:"Mike & Sulley's – Flavors of Asia", deck:"第10甲板（船尾）", type:"★ 需付費預訂", cat:"亞洲高端多元料理",
    desc:"以《怪獸電力公司》為主題的高端亞洲美食體驗，提供四種形式：日式鐵板燒・主廚Omakase套餐・壽司刺身吧・戶外全服務日式牛排館。對亞洲料理愛好者是必試體驗。",
    menu:[{zh:"主廚Omakase套餐",en:"Chef's Omakase",price:"付費"},{zh:"鐵板燒（含海鮮/和牛）",en:"Teppanyaki",price:"付費"},{zh:"壽司/刺身拼盤",en:"Sushi & Sashimi",price:"付費"}]
  },
  {
    name:"Gramma Tala's Kitchen", deck:"第7甲板 Imagination Garden", type:"免費快餐", cat:"Moana主題・太平洋島嶼料理",
    desc:"以Moana奶奶Tala命名的快餐站，提供太平洋島嶼風格輕食，有室內及戶外座位，緊鄰Garden Stage廣場，看表演前後可順道用餐。",
    menu:[{zh:"島嶼風烤雞",en:"Island Grilled Chicken",price:"免費"},{zh:"椰香飯",en:"Coconut Rice",price:"免費"},{zh:"熱帶水果沙拉",en:"Tropical Fruit Salad",price:"免費"}]
  },
  {
    name:"Mowgli's Eatery", deck:"第7甲板 Imagination Garden", type:"免費快餐", cat:"Jungle Book主題・印度料理",
    desc:"以《森林王子》毛克利為主題的印度風味快餐站，緊鄰Gramma Tala's Kitchen，同處Imagination Garden廣場。",
    menu:[{zh:"印度烤雞串（Tikka）",en:"Chicken Tikka",price:"免費"},{zh:"薄餅/咖哩",en:"Naan/Curry",price:"免費"}]
  },
  {
    name:"Pizza Planet", deck:"第17甲板 Toy Story Place", type:"免費快餐", cat:"Toy Story主題",
    desc:"《玩具總動員》主題披薩快餐站，全日供應各式現烤披薩，位於水上樂園區旁，玩水後補充體力最方便。",
    menu:[{zh:"每日特製披薩",en:"Daily Specialty Pizza",price:"免費"},{zh:"芝士披薩",en:"Cheese Pizza",price:"免費"}]
  },
  {
    name:"Wheezy's Freezies", deck:"第17甲板 Toy Story Place", type:"免費", cat:"冰品甜點",
    desc:"以《玩具總動員》Wheezy企鵝命名的霜淇淋站，全日免費供應多口味軟式霜淇淋。",
    menu:[{zh:"軟式霜淇淋（多口味）",en:"Soft Serve Ice Cream",price:"免費"}]
  },
  {
    name:"Stitch's 'Ohana Grill", deck:"第10甲板 Discovery Reef", type:"免費快餐", cat:"Lilo & Stitch主題・夏威夷風味",
    desc:"以《星際寶貝》史迪奇命名的夏威夷風烤肉輕食站，位於海底主題的Discovery Reef戶外區。",
    menu:[{zh:"夏威夷風烤肉串",en:"Hawaiian BBQ",price:"免費"},{zh:"炸薯條",en:"Fries",price:"免費"}]
  },
  {
    name:"Cosmic Kebabs", deck:"第10甲板 Discovery Reef", type:"免費快餐", cat:"Ms. Marvel主題",
    desc:"以《驚奇少女》Ms. Marvel為主題的烤串小食站，多元風格串燒快餐。",
    menu:[{zh:"多元烤串",en:"Assorted Kebabs",price:"免費"}]
  },
  {
    name:"Bewitching Boba & Brews", deck:"第10甲板 Discovery Reef", type:"部分付費", cat:"小美人魚主題・珍珠奶茶",
    desc:"以《小美人魚》為主題的珍珠奶茶咖啡廳，提供多種特調波霸飲品，部分需額外付費。",
    menu:[{zh:"珍珠奶茶（多口味）",en:"Bubble Tea",price:"部分付費"},{zh:"魔法特調",en:"Specialty Drinks",price:"付費"}]
  },
  {
    name:"Palo Café", deck:"第5甲板 Town Square", type:"部分付費", cat:"Luca主題・精品咖啡",
    desc:"Palo Trattoria的咖啡輕食附設空間，提供精品咖啡、糕點及輕食，氣氛優雅適合早晨或下午茶。",
    menu:[{zh:"濃縮咖啡/拿鐵",en:"Espresso/Latte",price:"部分付費"},{zh:"糕點/可頌",en:"Pastry/Croissant",price:"部分付費"}]
  },
];

const SHOPS_DATA = [
  {name:"World of Disney 迪士尼世界（主店）", deck:"第5甲板 Town Square", icon:"🏰", desc:"船上最大迪士尼商品旗艦店，販售角色商品、服飾、玩具，及探險號限定「航海主題」紀念品（只在此店才有）。"},
  {name:"World of Disney Too（副店）", deck:"第5甲板 Town Square", icon:"🎪", desc:"主店旁的副店，Duffy & Friends、大雄6、迪士尼公主、Marvel等各系列均有，最後一刻採購首選。"},
  {name:"Art of Disney 迪士尼藝術", deck:"第5甲板 Town Square", icon:"🎨", desc:"限量版版畫、藝術瓷器及高端藝術收藏品，送禮或自用的紀念逸品。"},
  {name:"Diamonds and Wishes 鑽石與願望", deck:"第5甲板 Town Square", icon:"💎", desc:"船上最高端珠寶精品店，精緻珠寶首飾及名牌手錶，適合紀念特殊場合或航行中的小奢華。"},
  {name:"Treasures Untold 未知珍寶", deck:"第10甲板 Discovery Reef", icon:"🐚", desc:"以小美人魚珍寶閣為靈感的精品店，販售高端迪士尼商品，以及新加坡本地藝術家Danielle Tay的探險號限定設計系列，獨家商品。"},
  {name:"Duffy & Friends Shop", deck:"第11甲板 San Fransokyo Street", icon:"🐻", desc:"全球首間登上迪士尼郵輪的Duffy專賣店！Duffy、ShellieMay、Gelatoni、StellaLou、CookieAnn、'Olu Mel、LinaBell全系列商品。Duffy迷絕對不能錯過！"},
  {name:"National Geographic Shop", deck:"第11甲板 San Fransokyo Street", icon:"🌏", desc:"National Geographic旗下探索主題商品，含攝影書、旅行配件及自然科學紀念品。"},
  {name:"Bibbidi Bobbidi Boutique 魔法美麗坊", deck:"第9甲板 Town Square", icon:"✨", desc:"3-12歲兒童公主/騎士造型體驗，提供妝扮、服裝、髮型設計，名額有限需提前預約，建議禮賓管家協助。"},
  {name:"Marvel Style Studio 漫威造型工作室", deck:"第19甲板 Marvel Landing", icon:"🦸", desc:"鋼鐵人、蜘蛛人、驚奇隊長等英雄造型體驗，成人與兒童均可，特定時段轉為成人限定（18+）場次。"},
];

const RS_MENU = [
  {zh:"米奇形狀鬆餅",en:"Mickey-Shaped Waffles",price:"免費"},
  {zh:"法式吐司",en:"French Toast",price:"免費"},
  {zh:"美式炒蛋培根",en:"Scrambled Eggs & Bacon",price:"免費"},
  {zh:"國際芝士拼盤",en:"International Cheese Plate",price:"免費"},
  {zh:"雞肉雲吞麵湯",en:"Chicken Wonton Noodle Soup",price:"免費"},
  {zh:"波隆那肉醬筆管麵",en:"Pennette Bolognaise",price:"免費"},
  {zh:"Caesar沙拉",en:"Caesar Salad",price:"免費"},
  {zh:"總匯三明治",en:"Club Sandwich",price:"免費"},
  {zh:"牛肉漢堡",en:"Beef Burger",price:"免費"},
  {zh:"炸薯條",en:"French Fries",price:"免費"},
  {zh:"水果拼盤",en:"Fresh Fruit Platter",price:"免費"},
  {zh:"巧克力熔岩蛋糕",en:"Chocolate Lava Cake",price:"免費"},
  {zh:"咖啡/熱可可/茶",en:"Coffee / Hot Choc / Tea",price:"免費"},
  {zh:"罐裝汽水・果汁",en:"Soda / Juice",price:"免費"},
  {zh:"瓶裝礦泉水",en:"Bottled Water",price:"免費"},
  {zh:"葡萄酒（紅/白）",en:"Wine (Red/White)",price:"另計"},
  {zh:"特調雞尾酒",en:"Cocktails",price:"另計"},
];

const CONC_DATA = [
  {
    cat:"🛎️ 禮賓管家服務",
    items:[
      "出發前130天起可聯繫岸上禮賓專員（Shore-side Concierge），協助預訂Palo Trattoria及Mike & Sulley's等付費餐廳",
      "出發前120天可預訂水療、Bibbidi Bobbidi Boutique等特殊體驗（早於一般旅客的75天）",
      "登船後管家全日電話待命，協助一切船上需求",
      "代辦：特殊慶典佈置、生日驚喜、特殊餐點需求",
      "無需到客服中心排隊，所有問題在禮賓貴賓室直接處理",
    ]
  },
  {
    cat:"🏖️ 禮賓專屬私人空間（第15甲板）",
    items:[
      "Opulence Spa & Fitness：禮賓專屬健身中心及水療設施（一般旅客需使用Senses Spa，禮賓旅客有獨立空間）",
      "禮賓私人戶外日光浴甲板（僅持禮賓房卡可刷卡進入）",
      "私人甲板配備舒適躺椅、遮陽傘、免費防曬乳、冰鎮毛巾",
    ]
  },
  {
    cat:"🍾 禮賓貴賓室 Concierge Lounge",
    items:[
      "開放時間：每日 07:00 – 22:00",
      "全日供應：輕食開胃小食、咖啡/茶/果汁/汽水/礦泉水（免費）",
      "礦泉水及汽水可自由帶回客房冰箱，完全免費",
      "每日 17:00–22:00 歡樂時光：免費啤酒、葡萄酒及精選雞尾酒",
      "配備高端咖啡機（可點製各式濃縮咖啡/拿鐵）",
    ]
  },
  {
    cat:"🎭 優先體驗禮遇",
    items:[
      "登船日：專屬優先通道（無需與一般旅客排隊）",
      "登船日享用禮賓專屬歡迎午餐",
      "Garden Stage及Walt Disney Theatre優先座位",
      "角色見面優先排隊資格",
      "下船：優先先行離船",
    ]
  },
  {
    cat:"🎁 客艙特別禮遇",
    items:[
      "客艙：Frette埃及棉床單・Elemis高端洗浴用品",
      "枕頭菜單可選（鵝絨/記憶泡棉/恆溫/防鼾/絲質等）",
      "登船歡迎禮（水果籃或特別小禮）",
      "每晚睡前床頭餅乾/巧克力驚喜",
      "最後一晚通常有Don Ducky Williams限量版版畫禮品",
      "特殊慶典佈置（生日/紀念日）請出發前聯繫禮賓管家預訂",
    ]
  },
];

const ACT_DATA = [
  {
    name:"🎢 Ironcycle Test Run（過山車）", deck:"第19甲板 Marvel Landing", warn:true,
    warnText:"⚠️ 安全提醒：搭乘Ironcycle前，請僅帶房卡（Key to the World Card）！錢包、手機、手錶、零錢等任何貴重物品請先回客艙鎖好。這是在30英尺高空環繞船頂的高速過山車，物品極易飛出或遭竊。行前把貴重物品存入客艙保險箱！",
    desc:"迪士尼郵輪史上第一座過山車，目前全球最長的海上過山車（820英尺/250公尺）！模擬鋼鐵人Ironcycle原型車，在第19甲板高速環繞。"
  },
  {name:"🐜 Pym Quantum Racers", deck:"第19甲板 Marvel Landing", warn:false, desc:"蟻人主題縮小版賽車，高度限制較低，適合較小的孩子也能體驗的Marvel設施。"},
  {name:"🌿 Groot Galaxy Spin", deck:"第19甲板 Marvel Landing", warn:false, desc:"嬰兒Groot主題旋轉飛行設施，類似樂園的「小飛象」，全家老少均適合。"},
  {name:"💧 Woody & Jessie's Wild Slides", deck:"第17甲板 Toy Story Place", warn:false, desc:"Toy Story主題雙水滑道，探險號沒有傳統AquaDuck，改以這對滑道取代。家庭友好，身高要求較低。"},
  {name:"🌊 Sunnyside Family Pool", deck:"第17甲板 Toy Story Place", warn:false, desc:"Toy Story主題的主家庭泳池，周邊多個熱水Jacuzzi。旁有兩面大螢幕全日播映迪士尼電影，Pizza Planet和Wheezy's Freezies近在咫尺。"},
  {name:"♾️ Infinity Pool", deck:"第18甲板（Iron Man主題）", warn:false, desc:"以鋼鐵人Tony Stark家為靈感的景觀游泳池，360度海景壯觀。旁有Infinity Bar提供飲品。以成人氛圍為主但無嚴格年齡限制。"},
  {name:"🌺 Wayfinder Bay 水池（你樓層！）", deck:"第16甲板（你的房間同層）", warn:false, desc:"Moana主題戶外水池兼表演廣場，表演時水池變舞台。非表演時段可靜靜游泳，旁有Wayfinder Bar。你住16甲板走幾步就到！"},
  {name:"🤖 Hiro Training Zone", deck:"第11甲板 San Fransokyo Street", warn:false, desc:"大雄6中Hiro設計的沉浸式模擬訓練，最多4人一組，在高科技地板上奔跑閃避格擋，體能與趣味兼備。"},
  {name:"🎮 Big Hero Arcade", deck:"第11甲板 San Fransokyo Street", warn:false, desc:"大型電玩遊藝廳，各式街機遊戲，部分需額外付費。適合青少年及玩家。"},
  {name:"🎬 Baymax Cinemas", deck:"第11甲板 San Fransokyo Street", warn:false, desc:"4銀幕船上電影院，從早上7點到午夜播放迪士尼/皮克斯/Marvel/Lucasfilm電影，免費入場。旁有Alley Cat Cafe賣爆米花。"},
  {name:"💆 Opulence Spa（禮賓專屬）", deck:"第15甲板", warn:false, desc:"僅禮賓旅客可使用的專屬水療及健身中心。一般旅客需去另一間Senses Spa，你有獨享的私人設施。建議出發前120天預訂按摩療程。"},
  {name:"👧 Oceaneer Club 海洋探索俱樂部", deck:"第9甲板 Town Square", warn:false, desc:"3-10歲兒童的免費托管遊樂天地，主題區域含Fairytale Hall（公主）、Andy's Toy Box（玩具總動員）、Marvel WEB Workshop（漫威）等，專業迪士尼員工全程陪伴。"},
];

const FORBIDDEN = [
  "超額酒精（每人限帶2瓶750ml葡萄酒/香檳上船）",
  "電熱鍋・電磁爐・電熱水壺等電熱器具",
  "明火裝置（蠟燭受限）・大型爆竹/煙火",
  "非法藥物",
  "槍枝・超規格刀具",
  "寵物（認證服務犬除外）",
  "電動平衡車・滑板・電動滑板車",
  "外帶大量生鮮食材（新加坡海關規定）",
  "超額現金（請注意海關申報）",
];

const TIPS = [
  "護照有效期至少6個月（從抵達新加坡日起算）",
  "需填寫新加坡SG Arrival Card（見下方連結，出發前3天內線上完成）",
  "Key to the World Card（房卡）= 房門鑰匙+消費卡+禮賓區通行證，請妥善保管",
  "搭乘Ironcycle等遊樂設施前，貴重物品請先鎖回房間，僅帶房卡",
  "Navigator App = 每日行程/秀的時間表，船上Wi-Fi下免費使用",
  "所有消費綁定房卡，可到禮賓貴賓室查詢帳單明細",
  "全程在海上不停靠港口，船時以新加坡時間（SGT, UTC+8）為準",
  "禮賓旅客享優先登船通道，提早到Marina Bay Cruise Centre報到",
  "小費：一般服務已含入票價，但禮賓管家額外給予小費是慣例",
  "船上Wi-Fi速度有限且費用高，建議事先下載好離線地圖及翻譯語言包",
];

// ===================== HELPERS =====================

function e(tag, cls, html, attrs) {
  const el = document.createElement(tag);
  if (cls) el.className = cls;
  if (html !== undefined) el.innerHTML = html;
  if (attrs) Object.entries(attrs).forEach(([k,v]) => el.setAttribute(k, v));
  return el;
}

function box(type, text) {
  return e('div', type + '-box', text);
}

function tag(label, extra) {
  return e('span', 'tag' + (extra ? ' ' + extra : ''), label);
}

function accordion(titleText, buildContent) {
  const wrap = document.createDocumentFragment();
  const btn = e('button', 'accordion-btn');
  const sp = e('span', '', titleText);
  sp.style.flex = '1';
  sp.style.marginRight = '8px';
  const arr = e('span', 'accordion-arrow', '▼');
  btn.appendChild(sp);
  btn.appendChild(arr);
  const content = e('div', 'accordion-content');
  buildContent(content);
  btn.addEventListener('click', () => {
    const open = content.classList.toggle('open');
    arr.textContent = open ? '▲' : '▼';
  });
  const frag = document.createDocumentFragment();
  frag.appendChild(btn);
  frag.appendChild(content);
  return frag;
}

function menuItems(items) {
  const wrap = e('div');
  items.forEach(m => {
    const row = e('div', 'menu-item');
    const left = e('div');
    left.appendChild(e('div', 'menu-item-name', m.zh));
    left.appendChild(e('div', 'menu-item-en', m.en));
    const priceClass = m.price === '付費' ? 'menu-item-price paid' : m.price === '免費' ? 'menu-item-price free' : 'menu-item-price';
    const right = e('div', priceClass, m.price);
    row.appendChild(left);
    row.appendChild(right);
    wrap.appendChild(row);
  });
  return wrap;
}

function step(num, text) {
  const d = e('div', 'step');
  d.appendChild(e('div', 'step-num', String(num)));
  d.appendChild(e('div', 'step-text', text));
  return d;
}

// ===================== SECTION BUILDERS =====================

function buildDeck() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🗺️ 甲板平面圖'));
  sec.appendChild(box('gold', '⭐ 你的房間：第16甲板・房號 16123（禮賓內艙房 Concierge Inside）'));
  sec.appendChild(box('info', 'ℹ️ 探險號共19個甲板，跳過第14甲板（亞洲文化忌諱，13層後直跳15）。7大主題區域分布如下：Imagination Garden（6-8層）・Town Square（5-9）・Discovery Reef（10）・San Fransokyo Street（11）・Wayfinder Bay（16）・Toy Story Place（17）・Marvel Landing（19）'));
  const map = e('div', 'deck-map');
  DECK_DATA.forEach(d => {
    const row = e('div', 'deck-row');
    const num = e('div', d.hl ? 'deck-num hl' : 'deck-num', String(d.num));
    const info = e('div', 'deck-info');
    info.appendChild(e('div', 'deck-name', d.name));
    info.appendChild(e('div', 'deck-locs', d.locs));
    row.appendChild(num);
    row.appendChild(info);
    map.appendChild(row);
  });
  sec.appendChild(map);
  return sec;
}

function buildShows() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🎭 秀與表演'));
  const ib = e('div', 'info-box');
  ib.innerHTML = '📍 主舞台：Garden Stage（第6-8甲板 Imagination Garden，三層挑高LED螢幕）<br>📍 劇院：Walt Disney Theatre（第9甲板）<br>📍 水池舞台：Wayfinder Bay（第16甲板，你房間同層！）';
  sec.appendChild(ib);
  sec.appendChild(box('warn', '⚠️ 詳細每日時間表請查 Disney Cruise Line Navigator App（船上Wi-Fi下免費使用）'));

  SHOWS_DATA.forEach(s => {
    sec.appendChild(accordion(s.title, cont => {
      const tags = e('div', 'mb8');
      tags.appendChild(tag('📍 ' + s.loc));
      if (s.dur) tags.appendChild(tag('⏱ ' + s.dur));
      cont.appendChild(tags);
      cont.appendChild(e('div', 'card-body mb8', s.desc));
      if (s.tip) cont.appendChild(box('gold', '💡 ' + s.tip));
      if (s.schedule && s.schedule.length) {
        cont.appendChild(e('div', 'small-label mt8', '📅 時間參考'));
        s.schedule.forEach(t => {
          const row = e('div', 'schedule-row');
          row.appendChild(e('span', 'time-badge', t.time));
          row.appendChild(e('span', 'schedule-name', t.name));
          cont.appendChild(row);
        });
      }
    }));
  });
  return sec;
}

function buildRestaurants() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🍽️ 餐廳總覽'));
  sec.appendChild(box('info', '🔄 輪替制：探險號有6間輪替主餐廳分A、B兩組（各3間）。你被隨機分配到其中一組，每晚去不同餐廳，服務員跟著你換桌。3-4晚航程只能體驗一組3間。'));
  sec.appendChild(box('gold', "⭐ 付費成人餐廳：Palo Trattoria & Mike & Sulley's。禮賓旅客可出發前120天預訂，強烈建議盡早！"));

  RESTS_DATA.forEach(r => {
    sec.appendChild(accordion(r.name, cont => {
      const tags = e('div', 'mb8');
      tags.appendChild(tag('📍 ' + r.deck));
      let tagCls = '';
      if (r.type.includes('付費')) tagCls = 'tag-gold';
      else if (r.type.includes('免費')) tagCls = 'tag-green';
      tags.appendChild(tag(r.type, tagCls));
      tags.appendChild(tag(r.cat));
      cont.appendChild(tags);
      cont.appendChild(e('div', 'card-body mb10', r.desc));
      cont.appendChild(e('div', 'small-label', '📖 菜單（代表性品項）'));
      cont.appendChild(menuItems(r.menu));
    }));
  });
  return sec;
}

function buildShops() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🛍️ 船上商店'));
  sec.appendChild(box('warn', '⚠️ 注意：探險號全程在海上不靠港，商店按正常時間開放。Duffy系列及限定商品建議盡早購買以免售罄。'));
  sec.appendChild(box('info', '💳 付款：房卡刷卡 / 現金（美金或新加坡幣）'));
  SHOPS_DATA.forEach(s => {
    const card = e('div', 'card');
    card.appendChild(e('div', 'card-title', s.icon + ' ' + s.name));
    card.appendChild(tag('📍 ' + s.deck));
    const body = e('div', 'card-body mt8', s.desc);
    card.appendChild(body);
    sec.appendChild(card);
  });
  return sec;
}

function buildRoomService() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🛎️ 客房點餐（24小時）'));
  const gb = e('div', 'gold-box mb12');
  gb.appendChild(e('div', '', '📞 點餐步驟'));
  gb.querySelector('div').style.cssText = 'font-weight:700;margin-bottom:7px';
  gb.appendChild(step(1, '拿起客房電話，撥「Room Service」或房內說明的分機號碼。'));
  gb.appendChild(step(2, '告知房號 16123 及所需品項（英文或中文均可）。'));
  gb.appendChild(step(3, '確認預計送達時間，通常30-45分鐘內送到。'));
  gb.appendChild(step(4, '大部分項目免費，酒精飲品另計（刷房卡）。'));
  sec.appendChild(gb);
  sec.appendChild(box('info', 'ℹ️ 禮賓旅客可另洽管家追加點輪替主餐廳主菜送至房間。'));
  sec.appendChild(e('div', 'small-label', '🍴 客房菜單（部分實際品項）'));
  sec.appendChild(menuItems(RS_MENU));
  return sec;
}

function buildConcierge() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '👑 禮賓服務總覽'));
  sec.appendChild(box('gold', '你入住「禮賓內艙房（Concierge Family Inside）」，享有迪士尼郵輪最高階服務禮遇。以下分類列出所有禮賓特權。'));
  CONC_DATA.forEach(c => {
    const cat = e('div', 'conc-cat');
    cat.appendChild(e('div', 'conc-cat-title', c.cat));
    c.items.forEach(item => cat.appendChild(e('div', 'conc-item', '✦ ' + item)));
    sec.appendChild(cat);
  });
  return sec;
}

function buildActivities() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🎢 遊樂設施'));
  ACT_DATA.forEach(a => {
    const card = e('div', 'card');
    card.appendChild(e('div', 'card-title', a.name));
    card.appendChild(tag('📍 ' + a.deck));
    if (a.warn) {
      const wb = e('div', 'warn-box mt8', a.warnText);
      card.appendChild(wb);
    }
    card.appendChild(e('div', 'card-body mt8', a.desc));
    sec.appendChild(card);
  });
  return sec;
}

function buildTranslate() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '🌐 Google 離線翻譯'));
  const card1 = e('div', 'card');
  card1.appendChild(e('div', 'card-title', '📥 下載 Google 翻譯 App'));
  const links = [
    {href:'https://translate.google.com', cls:'link-btn', text:'🌐 開啟 Google 翻譯'},
    {href:'https://apps.apple.com/app/google-translate/id414706506', cls:'link-btn link-btn-green', text:'🍎 App Store 下載（iOS）'},
    {href:'https://play.google.com/store/apps/details?id=com.google.android.apps.translate', cls:'link-btn link-btn-blue', text:'🤖 Google Play 下載（Android）'},
  ];
  links.forEach(l => {
    const a = e('a', l.cls, l.text, {href: l.href, target:'_blank', rel:'noreferrer'});
    card1.appendChild(a);
  });
  sec.appendChild(card1);

  const card2 = e('div', 'card');
  card2.appendChild(e('div', 'card-title', '📖 離線語言包設定步驟'));
  [
    '開啟 Google 翻譯 App，點右上角「⋮」或設定齒輪。',
    '選「離線翻譯」（Offline Translation）。',
    '下載「英文」「日文」「中文（繁體）」語言包（各約30-50MB）。',
    '下載完成，海上無網路也可使用文字翻譯。',
    '「拍照翻譯」（相機對著菜單）離線同樣支援！',
  ].forEach((t, i) => card2.appendChild(step(i+1, t)));
  sec.appendChild(card2);
  sec.appendChild(box('gold', '💡 請在有Wi-Fi時完成下載！船上Wi-Fi費用高且速度慢，不適合大量下載。'));
  sec.appendChild(box('info', '🗣️ 探險號員工均能以英文服務。遇複雜需求可找禮賓管家協助翻譯。'));
  return sec;
}

function buildCurrency() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '💱 匯率換算'));

  const CURR = [
    {code:"USD", name:"美元", flag:"🇺🇸"},
    {code:"SGD", name:"新加坡幣", flag:"🇸🇬"},
    {code:"JPY", name:"日圓", flag:"🇯🇵"},
    {code:"TWD", name:"台幣", flag:"🇹🇼"},
  ];
  let rates = {USD:1, SGD:1.35, JPY:152, TWD:32.5};
  let fromCurr = 'USD';
  let editingRates = false;

  // Card 1: calculator
  const card1 = e('div', 'card');
  card1.appendChild(e('div', 'card-title', '金額輸入'));

  const row = e('div', 'flex-row');
  const amtInput = e('input', 'currency-input', undefined, {type:'number', placeholder:'輸入金額', value:'100'});
  amtInput.style.flex = '2';
  amtInput.style.margin = '0';

  const fromSel = e('select', 'currency-input');
  fromSel.style.flex = '1';
  fromSel.style.padding = '10px 6px';
  fromSel.style.margin = '0';
  CURR.forEach(c => {
    const opt = document.createElement('option');
    opt.value = c.code;
    opt.textContent = c.flag + ' ' + c.code;
    fromSel.appendChild(opt);
  });
  row.appendChild(amtInput);
  row.appendChild(fromSel);
  card1.appendChild(row);

  const resultsDiv = e('div', 'mt8');
  card1.appendChild(resultsDiv);
  sec.appendChild(card1);

  function updateResults() {
    resultsDiv.innerHTML = '';
    const parsed = parseFloat(amtInput.value) || 0;
    const inUSD = parsed / rates[fromCurr];
    CURR.filter(c => c.code !== fromCurr).forEach(c => {
      const res = e('div', 'currency-result');
      res.appendChild(e('span', 'currency-label', c.flag + ' ' + c.name + ' (' + c.code + ')'));
      const val = inUSD * rates[c.code];
      const fmt = c.code === 'JPY'
        ? Math.round(val).toLocaleString('zh-TW')
        : val.toLocaleString('zh-TW', {minimumFractionDigits:2, maximumFractionDigits:2});
      res.appendChild(e('span', 'currency-value', fmt));
      resultsDiv.appendChild(res);
    });
  }

  amtInput.addEventListener('input', updateResults);
  fromSel.addEventListener('change', () => { fromCurr = fromSel.value; updateResults(); });
  updateResults();

  // Card 2: rate editor
  const card2 = e('div', 'card');
  const titleRow = e('div', 'card-title-row');
  titleRow.appendChild(e('div', 'card-title', '⚙️ 手動調整匯率（1 USD = ?）'));
  const editBtn = e('button', 'edit-btn', '編輯');
  titleRow.appendChild(editBtn);
  card2.appendChild(titleRow);

  const ratesDiv = e('div');
  card2.appendChild(ratesDiv);
  card2.appendChild(box('info', '💡 船上商店以美元計價，找零可能為新加坡幣。出發前查詢最新匯率後更新此頁。'));
  sec.appendChild(card2);

  function renderRates() {
    ratesDiv.innerHTML = '';
    CURR.filter(c => c.code !== 'USD').forEach(c => {
      const row2 = e('div', 'rate-row');
      row2.appendChild(e('span', 'rate-label', c.flag + ' 1 USD = ? ' + c.code));
      if (editingRates) {
        const inp = e('input', 'rate-input', undefined, {type:'number', value: String(rates[c.code])});
        inp.addEventListener('input', () => {
          rates[c.code] = parseFloat(inp.value) || 1;
          updateResults();
        });
        row2.appendChild(inp);
      } else {
        row2.appendChild(e('span', 'rate-value', String(rates[c.code])));
      }
      ratesDiv.appendChild(row2);
    });
  }

  editBtn.addEventListener('click', () => {
    editingRates = !editingRates;
    editBtn.textContent = editingRates ? '完成' : '編輯';
    renderRates();
  });
  renderRates();

  return sec;
}

function buildNotes() {
  const sec = e('div');
  sec.appendChild(e('div', 'section-title', '📋 注意事項'));

  const card1 = e('div', 'card');
  card1.appendChild(e('div', 'card-title', '🚫 禁止攜帶上船物品'));
  FORBIDDEN.forEach(item => card1.appendChild(e('div', 'forbidden-item', '✗ ' + item)));
  sec.appendChild(card1);

  const card2 = e('div', 'card');
  card2.appendChild(e('div', 'card-title', '✅ 重要旅行提醒'));
  TIPS.forEach(tip => card2.appendChild(e('div', 'tips-item', '✓ ' + tip)));
  sec.appendChild(card2);

  const card3 = e('div', 'card');
  card3.appendChild(e('div', 'card-title', '🔗 重要連結'));
  [
    {href:'https://www.ica.gov.sg/enter-transit-depart/entering-singapore/sg-arrival-card', cls:'link-btn', text:'🇸🇬 新加坡 SG Arrival Card 填寫入口'},
    {href:'https://disneycruise.disney.go.com/ships/adventure/', cls:'link-btn link-btn-green', text:'🚢 Disney Adventure 官方介紹'},
    {href:'https://disneycruise.disney.go.com/ships/deck-plans/adventure/', cls:'link-btn link-btn-blue', text:'🗺️ 官方甲板圖 PDF 下載'},
  ].forEach(l => {
    card3.appendChild(e('a', l.cls, l.text, {href:l.href, target:'_blank', rel:'noreferrer'}));
  });
  card3.appendChild(box('warn', '⚠️ SG Arrival Card 每位旅客需個別填寫，出發前3天內線上完成，無需列印。'));
  sec.appendChild(card3);

  return sec;
}

// ===================== SECTION MAP =====================

const SECTION_BUILDERS = {
  deck:        buildDeck,
  shows:       buildShows,
  restaurants: buildRestaurants,
  shops:       buildShops,
  roomservice: buildRoomService,
  concierge:   buildConcierge,
  activities:  buildActivities,
  translate:   buildTranslate,
  currency:    buildCurrency,
  notes:       buildNotes,
};

// ===================== APP INIT =====================

let activeSection = 'deck';
const sectionCache = {};
const navScroll = document.getElementById('navScroll');
const appContent = document.getElementById('appContent');

function showSection(id) {
  activeSection = id;

  // Update nav buttons
  navScroll.querySelectorAll('.nav-btn').forEach(btn => {
    btn.classList.toggle('active', btn.dataset.id === id);
  });

  // Build section if not cached
  if (!sectionCache[id]) {
    sectionCache[id] = SECTION_BUILDERS[id]();
  }

  // Swap content
  appContent.innerHTML = '';
  appContent.appendChild(sectionCache[id]);
  const pad = document.createElement('div');
  pad.className = 'bottom-pad';
  appContent.appendChild(pad);
  window.scrollTo(0, 0);
}

// Build nav buttons
NAV_ITEMS.forEach(n => {
  const btn = document.createElement('button');
  btn.className = 'nav-btn';
  btn.dataset.id = n.id;
  btn.textContent = n.icon + ' ' + n.label;
  btn.addEventListener('click', () => showSection(n.id));
  navScroll.appendChild(btn);
});

// Show initial section
showSection('deck');
</script>

</body>
</html>