<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Quest Belajar</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Lilita+One&family=Nunito:wght@500;700;800&display=swap">
<style>
:root{--bg:#8fd0f7;--card:#fffdf4;--tx:#10222b;--mut:#5d6b6f;--pri:#0f7c8c;--ok:#2f9e44;--bad:#e03e3e;--hi:#ffcf33;--line:#10222b;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#10222b;--card:#18323d;--tx:#f3efe0;--mut:#9db3b8;--pri:#5ec4e8;--ok:#8fd14f;--bad:#ff6b5b;--hi:#ffcf33;--line:#f3efe0}}
:root[data-theme="dark"]{--bg:#10222b;--card:#18323d;--tx:#f3efe0;--mut:#9db3b8;--pri:#5ec4e8;--ok:#8fd14f;--bad:#ff6b5b;--hi:#ffcf33;--line:#f3efe0}
*{box-sizing:border-box}html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--tx);font-family:Nunito,system-ui,sans-serif;font-weight:700;line-height:1.5}
h1,h2,h3{font-family:'Lilita One',Impact,sans-serif;font-weight:400;margin:0;letter-spacing:.5px}
main{max-width:760px;margin:0 auto;padding:16px}
.top{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-bottom:16px}
.top h1{font-size:28px}
.xp{min-width:130px;text-align:right;font-size:13px}.xp b{font-family:'Lilita One';font-size:16px;font-weight:400}
.bar{height:14px;border:2px solid var(--line);border-radius:8px;background:var(--card);overflow:hidden}
.bar i{display:block;height:100%;background:var(--bad);transition:width .4s}
.bar.xpb i{background:var(--hi)}.bar.tm i{background:var(--pri);transition:width 1s linear}.bar.sm{height:8px}
.card{background:var(--card);border:2px solid var(--line);border-radius:14px;padding:16px;box-shadow:4px 4px 0 var(--line)}
.chips{display:flex;gap:8px;flex-wrap:wrap;margin:8px 0 18px}
button{font:inherit;color:inherit;cursor:pointer}
.chip{border:2px solid var(--line);background:var(--card);border-radius:999px;padding:6px 14px}
.chip[aria-pressed=true]{background:var(--hi);color:#10222b}
.modes{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:14px}
.mode{text-align:left;border:2px solid var(--line);background:var(--card);border-radius:14px;padding:16px;box-shadow:4px 4px 0 var(--line)}
.mode:hover{transform:translate(-2px,-2px);box-shadow:6px 6px 0 var(--line)}
.mode h3{font-size:21px}.mode small{color:var(--mut);display:block;margin-top:4px}.mode .em{font-size:34px}
.btn{border:2px solid var(--line);background:var(--pri);color:#fff;border-radius:10px;padding:9px 18px;box-shadow:3px 3px 0 var(--line)}
:root[data-theme="dark"] .btn,.btn.ghost{color:var(--tx)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]) .btn{color:#10222b}}
.btn.ghost{background:var(--card)}.btn:active{transform:translate(2px,2px);box-shadow:1px 1px 0 var(--line)}
button:focus-visible{outline:3px solid var(--hi);outline-offset:2px}
.row{display:flex;justify-content:space-between;align-items:center;gap:10px;margin-bottom:10px}
.boss{text-align:center;margin:6px 0 12px}.boss .em{font-size:72px;line-height:1;display:inline-block}
.boss .em.hit{animation:hit .35s}@keyframes hit{0%,100%{transform:translateX(0)}25%{transform:translateX(-12px) rotate(-6deg)}75%{transform:translateX(12px) rotate(6deg)}}
.opt{display:block;width:100%;text-align:left;margin:8px 0;padding:11px 14px;border:2px solid var(--line);border-radius:10px;background:var(--card)}
.opt:hover:not(:disabled){background:var(--hi);color:#10222b}
.opt.ok{background:var(--ok);color:#10222b}.opt.no{background:var(--bad);color:#10222b}
.fb{margin-top:10px;padding:12px;border-radius:10px;border:2px dashed var(--line)}
.fc{min-height:190px;display:flex;align-items:center;justify-content:center;text-align:center;font-size:22px;padding:20px;width:100%;border:2px solid var(--line);border-radius:14px;background:var(--card);box-shadow:4px 4px 0 var(--line)}
.fc.back{background:var(--hi);color:#10222b}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px}
.tile{min-height:78px;padding:6px;font-size:14px;border:2px solid var(--line);border-radius:10px;background:var(--card)}
.tile.sel{background:var(--hi);color:#10222b}.tile.done{background:var(--ok);color:#10222b;opacity:.75}.tile.shake{animation:hit .3s;background:var(--bad)}
.boxes{display:flex;gap:8px;margin:10px 0}.boxes div{flex:1;text-align:center;border:2px solid var(--line);border-radius:8px;padding:4px;font-size:13px;background:var(--card)}
.back-link{margin-bottom:12px}
.mm{display:grid;gap:12px}.mm .card h3{font-size:19px;margin-bottom:4px}.mm p{margin:0;color:var(--mut)}
.v{display:none}.v.on{display:block}
.res{text-align:center}.res .em{font-size:64px}
/* ---------- Animasi ---------- */
.v.on{animation:vin .35s ease backwards}@keyframes vin{from{opacity:0;transform:translateY(14px)}}
.top h1{display:inline-block;animation:drop .7s cubic-bezier(.3,1.6,.5,1) backwards}@keyframes drop{from{opacity:0;transform:translateY(-22px) rotate(-4deg)}}
.mode{animation:pop .5s cubic-bezier(.3,1.5,.5,1) backwards;transition:transform .15s,box-shadow .15s}
.mode:nth-child(2){animation-delay:.08s}.mode:nth-child(3){animation-delay:.16s}.mode:nth-child(4){animation-delay:.24s}
@keyframes pop{from{opacity:0;transform:scale(.85) translateY(16px)}}
.mode .em{display:inline-block}.mode:hover:not(:disabled) .em{animation:wob .6s}
@keyframes wob{25%{transform:rotate(-14deg) scale(1.2)}75%{transform:rotate(14deg) scale(1.2)}}
.mode:disabled:hover{transform:none;box-shadow:4px 4px 0 var(--line)}
.chip{transition:background .2s,transform .15s}.chip:hover{transform:translateY(-2px)}.chip[aria-pressed=true]{animation:pulse .35s}
@keyframes pulse{50%{transform:scale(1.12)}}
.btn{transition:transform .12s,box-shadow .12s}.btn:hover:not(:active){transform:translateY(-2px);box-shadow:3px 5px 0 var(--line)}
.xp.lvup{animation:pulse .7s 2}
.boss{position:relative}.boss .em{animation:float 2.4s ease-in-out infinite}
@keyframes float{50%{transform:translateY(-8px)}}
.boss .em.die{animation:die .9s forwards}@keyframes die{to{transform:scale(0) rotate(540deg);opacity:0}}
.card.lose{animation:hit .5s}
.dmg{position:absolute;left:58%;top:0;font-family:'Lilita One';font-size:30px;pointer-events:none;animation:up .9s ease-out forwards}
@keyframes up{to{transform:translateY(-56px) scale(1.3);opacity:0}}
#hs,#cb{display:inline-block}#hs.hit{animation:hit .4s}
.cbp{display:inline-block;animation:combo .5s}@keyframes combo{0%{transform:scale(1.8) rotate(-8deg)}100%{transform:none}}
.bar.tm.low i{background:var(--bad)}.bar.tm.low{animation:pulse .5s infinite}
.opt{animation:slide .35s backwards;transition:background .15s,transform .15s}.opt:hover:not(:disabled){transform:translateX(4px)}
.opt:nth-child(2){animation-delay:.07s}.opt:nth-child(3){animation-delay:.14s}.opt:nth-child(4){animation-delay:.21s}
@keyframes slide{from{opacity:0;transform:translateY(10px)}}
.opt.ok{animation:okpop .45s}@keyframes okpop{40%{transform:scale(1.04)}}
.opt.no{animation:hit .35s}
.fb{animation:slide .3s backwards}
.fc.new{animation:cardin .35s}@keyframes cardin{from{opacity:0;transform:translateX(40px) rotate(3deg)}}
.fc.fl{animation:flip .4s}@keyframes flip{from{transform:rotateY(90deg)}}
.tile{animation:pop .4s calc(var(--d,0)*1s) backwards;transition:background .2s,transform .15s}
.tile:hover:not(.done){transform:translateY(-2px)}
.tile.done{animation:okpop .45s}.tile.shake{animation:hit .3s}
.res .em{display:inline-block;animation:bounce .9s}@keyframes bounce{0%{transform:scale(0)}50%{transform:scale(1.3) rotate(8deg)}100%{transform:none}}
.cf{position:fixed;top:-14px;width:10px;height:14px;z-index:9;pointer-events:none;animation:fall 1.9s ease-in forwards}
@keyframes fall{to{transform:translate(var(--dx),105vh) rotate(var(--r))}}
/* ---------- Gaya ala Roblox ---------- */
body{background-image:radial-gradient(circle,rgba(255,255,255,.35) 3px,transparent 4px);background-size:34px 34px}
.top{background:#232527;color:#fff;padding:8px 12px;border:2px solid var(--line);border-radius:6px;box-shadow:4px 4px 0 var(--line)}
.top h1{color:#fff;text-shadow:0 3px 0 #0f7c8c}
.coin{border:2px solid #ffcf33;border-radius:6px;padding:2px 10px;font-family:'Lilita One';font-size:16px;color:#ffcf33}.coin.bump{animation:pulse .4s}
.card,.mode,.opt,.btn,.tile,.fc,.chip,.fb,.bar{border-radius:6px}
.btn{background:#00b06f;color:#fff;text-shadow:0 2px 0 rgba(0,0,0,.3)}
.mode:nth-child(1){border-bottom:7px solid #e2231a}.mode:nth-child(2){border-bottom:7px solid #0d69ac}.mode:nth-child(3){border-bottom:7px solid #00b06f}.mode:nth-child(4){border-bottom:7px solid #f58a1f}
.lobby,.arena{display:flex;align-items:flex-end;gap:14px;padding:12px 16px 0;background:linear-gradient(#bfe6fb 75%,#5aa24a 75%);border:2px solid var(--line);border-radius:6px;color:#10222b}
.lobby{margin:0 0 14px;min-height:120px}.arena{margin:6px 0 12px;padding-bottom:0}.arena .boss{flex:1;margin:0 0 8px}
.bubble{background:#fff;border:2px solid #10222b;border-radius:6px;padding:8px 12px;margin-bottom:50px}
#lobby,.pl{width:56px;flex:none;padding-bottom:6px}
.noob{position:relative;width:44px;height:84px;margin:0 auto;animation:bob 1s ease-in-out infinite;cursor:pointer}
.noob i{position:absolute;display:block;border:2px solid #10222b;transform-origin:50% 0}
.noob .h{left:11px;top:0;width:22px;height:22px;background:#f5cd2f;border-radius:4px}
.noob .h::before{content:'';position:absolute;left:3px;top:6px;width:3px;height:3px;background:#000;box-shadow:9px 0 #000}
.noob .h::after{content:'';position:absolute;left:4px;top:11px;width:9px;height:4px;border-bottom:2px solid #000;border-radius:0 0 8px 8px}
.noob .t{left:6px;top:24px;width:32px;height:28px;background:#0d69ac}
.noob .a1,.noob .a2{top:24px;width:12px;height:28px;background:#f5cd2f}.noob .a1{left:-6px}.noob .a2{left:38px}
.noob .l1,.noob .l2{top:54px;width:16px;height:28px;background:#a3c86b}.noob .l1{left:6px}.noob .l2{left:22px}
#lobby .a2{animation:wave .5s infinite alternate}@keyframes wave{to{transform:rotate(150deg)}}
@keyframes bob{50%{transform:translateY(-3px)}}
.noob.jump{animation:jump .5s}@keyframes jump{40%{transform:translateY(-34px)}}
.noob.atk{animation:atk .6s}@keyframes atk{40%{transform:translate(70px,-12px)}}
.noob.oof{animation:oof .6s}@keyframes oof{30%{transform:rotate(-80deg) translateY(10px)}}
.noob.cheer{animation:jump .5s 3}
.noob.dead{animation:dead .5s forwards}@keyframes dead{to{transform:rotate(90deg) translate(-18px,0)}}
.toast{position:fixed;right:12px;top:calc(12px + env(safe-area-inset-top,0px));background:#232527;color:#fff;border:2px solid #fff;border-radius:6px;padding:10px 14px;z-index:10;animation:tin .4s,tout .4s 2.8s forwards}
@keyframes tin{from{transform:translateX(120%)}}@keyframes tout{to{transform:translateX(120%);opacity:0}}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
</style>
</head>
<body>
<main>
<div class="top">
  <h1>Quest Belajar</h1><div class="coin">🪙 <b id="cn">0</b></div>
  <div class="xp"><div>Level <b id="lv">1</b> · <span id="xpt">0</span> XP</div><div class="bar xpb sm" style="margin-top:4px"><i id="xpb" style="width:0"></i></div></div>
</div>

<section id="v-home" class="v on">
  <div class="lobby"><div id="lobby"></div><div class="bubble">Halo, Pemain! Pilih quest dan kalahkan boss!</div></div>
  <p style="margin:0">Pilih mata pelajaran, lalu pilih cara bermain. Setiap permainan memakai metode belajar yang sudah terbukti.</p>
  <div class="chips" id="chips"></div>
  <div class="modes">
    <button class="mode" onclick="startBattle(cat)"><div class="em">🐉</div><h3>Boss Battle</h3><small>Jawab soal untuk mengurangi darah boss. Metode: Active Recall</small></button>
    <button class="mode" onclick="startCards()"><div class="em">🗂️</div><h3>Kartu Kilat</h3><small>Kartu istilah dengan sistem kotak Leitner. Metode: Spaced Repetition</small></button>
    <button class="mode" onclick="startMatch()"><div class="em">🧩</div><h3>Pasangkan</h3><small>Cocokkan istilah dengan artinya. Metode: Elaborasi</small></button>
    <button class="mode" id="rev" onclick="startBattle('review')"><div class="em">🔁</div><h3>Remedial</h3><small id="revn">Ulangi soal yang pernah salah. Metode: Error-based Review</small></button>
  </div>
  <p style="margin:18px 0 0"><button class="btn ghost" onclick="show('metode')">Lihat metode belajar</button></p>
</section>

<section id="v-battle" class="v"></section>
<section id="v-cards" class="v"></section>
<section id="v-match" class="v"></section>

<section id="v-metode" class="v">
  <button class="btn ghost back-link" onclick="show('home')">Kembali ke menu</button>
  <h2 style="margin-bottom:12px">Metode belajar di balik game</h2>
  <div class="mm">
    <div class="card"><h3>Active Recall (Boss Battle)</h3><p>Menjawab soal tanpa melihat catatan memaksa otak mengambil ingatan. Cara ini membuat ingatan lebih kuat daripada hanya membaca ulang.</p></div>
    <div class="card"><h3>Umpan balik instan</h3><p>Setiap jawaban langsung disertai penjelasan, jadi kesalahan segera dikoreksi sebelum menjadi kebiasaan.</p></div>
    <div class="card"><h3>Spaced Repetition (Kartu Kilat)</h3><p>Kartu yang sudah hafal naik ke kotak berikutnya dan muncul lebih jarang. Kartu yang lupa kembali ke kotak 1 dan muncul lebih sering.</p></div>
    <div class="card"><h3>Elaborasi (Pasangkan)</h3><p>Menghubungkan istilah dengan maknanya membangun pemahaman, bukan sekadar hafalan.</p></div>
    <div class="card"><h3>Error-based Review (Remedial)</h3><p>Soal yang salah disimpan otomatis. Menjawabnya benar di mode Remedial akan menghapusnya dari daftar.</p></div>
    <div class="card"><h3>Gamifikasi</h3><p>XP, level, combo, dan boss memberi alasan untuk kembali belajar setiap hari. Belajar singkat tapi rutin lebih efektif daripada sekali lama.</p></div>
  </div>
</section>
</main>

<script>
const CATS={mat:{n:'Matematika',e:'🐉',b:'Naga Angka'},ipa:{n:'IPA',e:'👾',b:'Monster Sains'},idn:{n:'Bahasa Indonesia',e:'🧙',b:'Penyihir Kata'},review:{n:'Remedial',e:'👹',b:'Boss Remedial'}};
const Q={
mat:[
{q:'Hasil dari 7 × 8 adalah ...',o:['54','56','64','48'],a:1,e:'7 × 8 = 56. Ingat urutan 5-6-7-8: 56 = 7 × 8.'},
{q:'Hasil dari 3/4 + 1/4 adalah ...',o:['1','4/8','1/2','3/16'],a:0,e:'Penyebut sama, jadi jumlahkan pembilangnya: 4/4 = 1.'},
{q:'Keliling persegi dengan sisi 9 cm adalah ...',o:['18 cm','36 cm','81 cm','27 cm'],a:1,e:'Keliling persegi = 4 × sisi = 4 × 9 = 36 cm.'},
{q:'25% dari 200 adalah ...',o:['25','50','75','40'],a:1,e:'25% = 1/4. Seperempat dari 200 adalah 50.'},
{q:'Luas segitiga dengan alas 10 dan tinggi 6 adalah ...',o:['60','30','16','36'],a:1,e:'Luas = ½ × alas × tinggi = ½ × 10 × 6 = 30.'},
{q:'Akar kuadrat dari 144 adalah ...',o:['14','12','11','13'],a:1,e:'12 × 12 = 144, jadi √144 = 12.'}],
ipa:[
{q:'Gas yang diserap tumbuhan saat fotosintesis adalah ...',o:['Oksigen','Nitrogen','Karbon dioksida','Hidrogen'],a:2,e:'Tumbuhan menyerap CO₂ dan air, lalu menghasilkan glukosa dan oksigen.'},
{q:'Planet yang paling dekat dengan Matahari adalah ...',o:['Venus','Bumi','Merkurius','Mars'],a:2,e:'Urutan dari Matahari: Merkurius, Venus, Bumi, Mars, dst.'},
{q:'Rumus kimia air adalah ...',o:['CO₂','H₂O','O₂','NaCl'],a:1,e:'Satu molekul air terdiri dari 2 atom hidrogen dan 1 atom oksigen.'},
{q:'Perubahan wujud dari cair menjadi gas disebut ...',o:['Membeku','Menguap','Mengembun','Menyublim'],a:1,e:'Cair → gas = menguap. Gas → cair = mengembun.'},
{q:'Organ yang memompa darah ke seluruh tubuh adalah ...',o:['Paru-paru','Hati','Jantung','Ginjal'],a:2,e:'Jantung memompa darah lewat pembuluh darah ke seluruh tubuh.'},
{q:'Satuan gaya dalam SI adalah ...',o:['Joule','Newton','Watt','Pascal'],a:1,e:'Gaya diukur dalam Newton (N). Joule untuk energi, Watt untuk daya.'}],
idn:[
{q:'Sinonim kata "pandai" adalah ...',o:['Bodoh','Cerdas','Malas','Lambat'],a:1,e:'Sinonim berarti sama maknanya. Pandai = cerdas.'},
{q:'Antonim kata "rajin" adalah ...',o:['Giat','Tekun','Malas','Ulet'],a:2,e:'Antonim berarti berlawanan makna. Rajin lawan katanya malas.'},
{q:'Penulisan kata baku yang benar adalah ...',o:['Apotik','Apotek','Apotick','Apotk'],a:1,e:'Bentuk baku menurut KBBI: apotek.'},
{q:'Kata "tulis" diberi awalan me- menjadi ...',o:['Mentulis','Menulis','Menullis','Memtulis'],a:1,e:'Huruf t di awal kata luluh saat diberi me-, sehingga menjadi menulis.'},
{q:'"Dia bagaikan singa di medan perang." Majas kalimat ini adalah ...',o:['Metafora','Simile','Hiperbola','Ironi'],a:1,e:'Simile membandingkan secara eksplisit memakai kata seperti, bagaikan, atau bak.'},
{q:'Gagasan pokok paragraf biasanya terdapat pada ...',o:['Kalimat utama','Judul buku','Kalimat penjelas','Kalimat terakhir saja'],a:0,e:'Kalimat utama memuat gagasan pokok. Kalimat penjelas hanya mendukungnya.'}]
};
const P={
mat:[['Persegi','Bangun dengan 4 sisi sama panjang'],['Keliling','Jumlah panjang semua sisi'],['Luas','Besar daerah di dalam bangun'],['Pecahan','Bagian dari suatu keseluruhan'],['Bilangan prima','Hanya habis dibagi 1 dan dirinya sendiri'],['Diameter','Dua kali jari-jari lingkaran']],
ipa:[['Fotosintesis','Tumbuhan membuat makanan dengan bantuan cahaya'],['Gravitasi','Gaya tarik ke pusat bumi'],['Herbivora','Hewan pemakan tumbuhan'],['Evaporasi','Air berubah menjadi uap'],['Atom','Partikel penyusun materi'],['Ekosistem','Hubungan makhluk hidup dengan lingkungannya']],
idn:[['Sinonim','Kata yang maknanya sama'],['Antonim','Kata yang maknanya berlawanan'],['Metafora','Perbandingan langsung tanpa kata seperti'],['Kalimat utama','Kalimat berisi gagasan pokok'],['Prefiks','Imbuhan di awal kata'],['Paragraf','Kumpulan kalimat dengan satu gagasan']]
};
const ALL=[];for(const c in Q)Q[c].forEach((q,i)=>{q.id=c+i;ALL.push(q)});
let S={xp:0,wrong:[],box:{},coins:0,bd:{}};
try{const r=localStorage.getItem('quest-belajar');if(r)S=Object.assign(S,JSON.parse(r))}catch(e){}
function save(){try{localStorage.setItem('quest-belajar',JSON.stringify(S))}catch(e){}}
const $=s=>document.querySelector(s);
const shuf=a=>{a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a};
let cat='mat',timer=null;

function stats(){$('#cn').textContent=S.coins;$('#lv').textContent=Math.floor(S.xp/100)+1;$('#xpt').textContent=S.xp;$('#xpb').style.width=(S.xp%100)+'%';
  const n=S.wrong.length;$('#revn').textContent=n?`${n} soal menunggu diulang. Metode: Error-based Review`:'Belum ada soal salah. Main Boss Battle dulu.';$('#rev').disabled=!n;$('#rev').style.opacity=n?1:.55}
function addXP(n){const o=Math.floor(S.xp/100);S.xp+=n;save();stats();
  if(Math.floor(S.xp/100)>o){const x=$('.xp');x.classList.remove('lvup');void x.offsetWidth;x.classList.add('lvup');confetti();toast('🏅 Naik ke Level '+(Math.floor(S.xp/100)+1)+'!')}}
function confetti(){if(matchMedia('(prefers-reduced-motion:reduce)').matches)return;const cs=['#ffcf33','#0f7c8c','#2f9e44','#e03e3e','#5ec4e8'];
  for(let i=0;i<40;i++){const s=document.createElement('i');s.className='cf';s.style.cssText=`left:${Math.random()*100}vw;background:${cs[i%5]};animation-delay:${Math.random()*.4}s;--dx:${(Math.random()-.5)*160}px;--r:${Math.random()*720}deg`;document.body.appendChild(s);s.addEventListener('animationend',()=>s.remove())}}
function fly(t,c){const s=document.createElement('b');s.className='dmg';s.textContent=t;s.style.color=c;$('.boss').appendChild(s);setTimeout(()=>s.remove(),900)}
function show(v){clearInterval(timer);document.querySelectorAll('.v').forEach(e=>e.classList.remove('on'));$('#v-'+v).classList.add('on');if(v==='home')stats()}
$('#chips').innerHTML=['mat','ipa','idn'].map(c=>`<button class="chip" data-c="${c}" aria-pressed="${c===cat}">${CATS[c].n}</button>`).join('');
$('#chips').onclick=e=>{const c=e.target.dataset.c;if(!c)return;cat=c;document.querySelectorAll('.chip').forEach(b=>b.setAttribute('aria-pressed',b.dataset.c===c))};

/* ---------- Boss Battle ---------- */
let B;
function startBattle(c){
  const src=c==='review'?ALL.filter(q=>S.wrong.includes(q.id)):Q[c];
  B={c,src,hp:100,me:3,combo:0,pool:shuf(src),i:0,t:15,q:null,over:false};
  $('#v-battle').innerHTML=`<button class="btn ghost back-link" onclick="show('home')">Kembali ke menu</button>
  <div class="card"><div class="row"><div id="hs" aria-label="Nyawa"></div><div id="cb"></div></div>
  <div class="arena"><div class="pl">${NOOB}</div><div class="boss"><div class="em" id="be">${CATS[c].e}</div><div style="margin:4px 0">${CATS[c].b} · <span id="hpn">100</span> HP</div><div class="bar"><i id="bhp" style="width:100%"></i></div></div></div>
  <div class="bar tm sm"><i id="tm" style="width:100%"></i></div>
  <h3 id="bq" style="margin:14px 0 6px;font-size:21px"></h3><div id="bo"></div><div id="fb"></div></div>`;
  show('battle');nextQ();
}
function nextQ(){
  if(B.i>=B.pool.length){B.pool=shuf(B.src);B.i=0}
  const q=B.q=B.pool[B.i++];B.opts=shuf(q.o.map((t,k)=>({t,k})));B.t=15;B.locked=false;
  $('#bq').textContent=q.q;$('#fb').innerHTML='';$('#tm').style.width='100%';$('#tm').parentNode.classList.remove('low');
  $('#bo').innerHTML=B.opts.map((o,j)=>`<button class="opt" onclick="answer(${j})">${o.t}</button>`).join('');
  $('#hs').textContent='❤️'.repeat(B.me)+'🖤'.repeat(3-B.me);$('#cb').innerHTML=B.combo>1?`<span class="cbp">Combo x${B.combo} 🔥</span>`:'';
  clearInterval(timer);timer=setInterval(()=>{B.t--;$('#tm').style.width=(B.t/15*100)+'%';$('#tm').parentNode.classList.toggle('low',B.t<=5);if(B.t<=0)answer(-1)},1000);
}
function answer(j){
  if(B.locked)return;B.locked=true;clearInterval(timer);
  const q=B.q,ok=j>=0&&B.opts[j].k===q.a,btns=document.querySelectorAll('.opt');
  btns.forEach((b,x)=>{b.disabled=true;if(B.opts[x].k===q.a)b.classList.add('ok');else if(x===j)b.classList.add('no')});
  let msg;
  if(ok){const d=20+Math.min(B.combo,3)*5;B.hp=Math.max(0,B.hp-d);B.combo++;S.wrong=S.wrong.filter(id=>id!==q.id);
    $('#be').classList.remove('hit');void $('#be').offsetWidth;$('#be').classList.add(B.hp<=0?'die':'hit');fly('-'+d,'var(--bad)');act('atk');gain(5+Math.min(B.combo,3));beep(880);if(B.combo>=3)badge('c3','Combo Master, 3 jawaban beruntun!');msg=`✅ Tepat! Boss kehilangan ${d} HP.`}
  else{B.me--;B.combo=0;const h=$('#hs');h.classList.remove('hit');void h.offsetWidth;h.classList.add('hit');if(B.me<=0)$('#v-battle .card').classList.add('lose');act(B.me<=0?'dead':'oof');beep(150,.3,'sawtooth');if(!S.wrong.includes(q.id))S.wrong.push(q.id);msg=j<0?'⏰ Waktu habis! Kamu kehilangan 1 nyawa.':'❌ Belum tepat. Kamu kehilangan 1 nyawa.'}
  save();$('#bhp').style.width=B.hp+'%';$('#hpn').textContent=B.hp;$('#hs').textContent='❤️'.repeat(B.me)+'🖤'.repeat(3-B.me);
  const end=B.hp<=0||B.me<=0;
  $('#fb').innerHTML=`<div class="fb"><div>${msg}</div><div style="color:var(--mut);margin:4px 0 10px">Penjelasan: ${q.e}</div><button class="btn" onclick="${end?'endBattle()':'nextQ()'}">${end?'Lihat hasil':'Soal berikutnya'}</button></div>`;
}
function endBattle(){
  const win=B.hp<=0,xp=win?50+B.me*10:10;addXP(xp);if(win){confetti();gain(20);badge('win','Boss Slayer, kalahkan boss pertamamu!');beep(660,.15);setTimeout(()=>beep(990,.3),150)}
  $('#v-battle').innerHTML=`<div class="card res"><div class="em">${win?'🏆':'💀'}</div><h2>${win?'Boss dikalahkan!':'Kamu kalah kali ini'}</h2>
  <p>+${xp} XP. ${win?'Soal yang salah tadi disimpan di Remedial untuk diulang.':'Soal yang salah tersimpan di Remedial. Ulangi untuk menguatkan ingatan.'}</p>
  <p style="margin-top:14px"><button class="btn" onclick="startBattle('${B.c}')">Main lagi</button> <button class="btn ghost" onclick="show('home')">Menu</button></p></div>`;
}

/* ---------- Kartu Kilat (Leitner) ---------- */
let C;
function startCards(){C={c:cat,cur:-1,flip:false,n:0,anim:'new'};$('#v-cards').innerHTML=`<button class="btn ghost back-link" onclick="show('home')">Kembali ke menu</button><div id="cw"></div>`;show('cards');nextCard()}
const bk=(c,i)=>S.box[c+i]||1;
function nextCard(){
  const cards=P[C.c].map((p,i)=>({i,b:bk(C.c,i)+Math.random()*1.5})).sort((a,b)=>a.b-b.b).filter(x=>x.i!==C.cur);
  C.cur=cards[0].i;C.flip=false;C.anim='new';drawCard();
}
function drawCard(){
  const an=C.anim||'';C.anim='';const p=P[C.c][C.cur],cnt=[1,2,3].map(b=>P[C.c].filter((_,i)=>bk(C.c,i)===b).length);
  $('#cw').innerHTML=`<p style="margin:0 0 6px">Ingat artinya dulu, lalu klik kartu untuk melihat jawaban.</p>
  <div class="boxes"><div>Kotak 1 (sering) · ${cnt[0]}</div><div>Kotak 2 · ${cnt[1]}</div><div>Kotak 3 (jarang) · ${cnt[2]}</div></div>
  <button class="fc ${C.flip?'back':''} ${an}" onclick="C.flip=true;C.anim='fl';drawCard()">${C.flip?p[1]:p[0]}</button>
  <div class="row" style="margin-top:14px;justify-content:center">${C.flip?`<button class="btn ghost" onclick="rate(0)">Belum hafal</button><button class="btn" onclick="rate(1)">Hafal</button>`:''}</div>`;
}
function rate(ok){const k=C.c+C.cur;S.box[k]=ok?Math.min(3,bk(C.c,C.cur)+1):1;if(ok&&++C.n%5===0)addXP(10);save();nextCard()}

/* ---------- Pasangkan ---------- */
let M;
function startMatch(){
  const pairs=shuf(P[cat].map((p,i)=>({p,i})));
  M={tiles:shuf(pairs.flatMap(x=>[{id:x.i,t:x.p[0],k:'t'},{id:x.i,t:x.p[1],k:'d'}])),sel:null,done:0,moves:0,lock:false};
  $('#v-match').innerHTML=`<button class="btn ghost back-link" onclick="show('home')">Kembali ke menu</button>
  <div class="card"><div class="row"><b>Pasangkan istilah dengan artinya</b><span id="mv">Langkah: 0</span></div><div class="grid" id="mg"></div><div id="mr"></div></div>`;
  $('#mg').innerHTML=M.tiles.map((t,x)=>`<button class="tile" style="--d:${x*.04}" onclick="pick(${x})">${t.t}</button>`).join('');show('match');
}
function pick(x){
  if(M.lock)return;const el=document.querySelectorAll('.tile')[x];if(el.classList.contains('done')||M.sel===x)return;
  if(M.sel===null){M.sel=x;el.classList.add('sel');return}
  const a=M.tiles[M.sel],b=M.tiles[x],ea=document.querySelectorAll('.tile')[M.sel];M.moves++;$('#mv').textContent='Langkah: '+M.moves;
  if(a.id===b.id&&a.k!==b.k){ea.className=el.className='tile done';M.sel=null;
    if(++M.done===M.tiles.length/2){addXP(Math.max(20,60-M.moves*3));confetti();gain(10);$('#mr').innerHTML=`<div class="fb res" style="margin-top:12px"><div class="em">🎉</div><p>Selesai dalam ${M.moves} langkah!</p><button class="btn" onclick="startMatch()">Main lagi</button></div>`}}
  else{M.lock=true;ea.classList.remove('sel');ea.classList.add('shake');el.classList.add('shake');
    setTimeout(()=>{ea.className=el.className='tile';M.sel=null;M.lock=false},450)}
}
const NOOB='<div class="noob"><i class="h"></i><i class="t"></i><i class="a1"></i><i class="a2"></i><i class="l1"></i><i class="l2"></i></div>';
$('#lobby').innerHTML=NOOB;$('#lobby .noob').onclick=e=>{act('jump',e.currentTarget);beep(500,.1)};
let AC;function beep(f,d=.12,t='square'){try{AC=AC||new(window.AudioContext||window.webkitAudioContext)();const o=AC.createOscillator(),g=AC.createGain();o.type=t;o.frequency.value=f;g.gain.setValueAtTime(.05,AC.currentTime);g.gain.exponentialRampToValueAtTime(.001,AC.currentTime+d);o.connect(g);g.connect(AC.destination);o.start();o.stop(AC.currentTime+d)}catch(e){}}
function act(c,el){el=el||$('.pl .noob');if(!el)return;el.classList.remove('atk','oof','jump','cheer');void el.offsetWidth;el.classList.add(c);
  if(c!=='dead')el.addEventListener('animationend',e=>{if(e.target===el)el.classList.remove(c)},{once:true})}
function gain(n){S.coins+=n;save();$('#cn').textContent=S.coins;const c=$('.coin');c.classList.remove('bump');void c.offsetWidth;c.classList.add('bump')}
function toast(t){const d=document.createElement('div');d.className='toast';d.textContent=t;document.body.appendChild(d);setTimeout(()=>d.remove(),3300);beep(520,.1);setTimeout(()=>beep(780,.2),110)}
function badge(id,t){if(S.bd[id])return;S.bd[id]=1;save();toast('🏅 Badge: '+t)}
stats();
</script>
</body>
</html>
