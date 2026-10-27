<!DOCTYPE html>
<html lang="ku" dir="rtl"><head><meta charset="utf-8"><title>تایپ بکە و سەرکەفتنێ ببینە</title>
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<style>
:root{box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:dark}
*{box-sizing:border-box}[hidden]{display:none!important}
html,body{margin:0;height:100%;background:#0d1b21;color:#eef3f1;font:16px/1.5 Tahoma,'Noto Naskh Arabic',system-ui,-apple-system,Segoe UI,sans-serif;overflow:hidden}
h1,b,.t{font-family:Tahoma,'Noto Naskh Arabic',Georgia,serif;font-weight:700}
#menu{position:absolute;inset:0;overflow:auto;padding:28px 18px 40px;background:radial-gradient(120% 80% at 50% 0,#2b4d62,#0d1b21 72%)}
.wrap{max-width:760px;margin:0 auto;position:relative;z-index:1}#flag{position:fixed;inset:0;width:100%;height:100%;z-index:0}#menu h1,#menu h2,#menu .sub{text-shadow:0 1px 8px #000}
h1{font-size:clamp(36px,8vw,58px);margin:0 0 4px}.sub{color:#a9bcbd;margin:0 0 24px}
h2{font:15px system-ui;color:#a9bcbd;margin:18px 0 8px}
.row{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.card{border:1px solid #ffffff2b;border-radius:14px;padding:14px;background-color:#0b161ca6;color:#eef3f1;text-align:start;font:inherit;cursor:pointer;min-height:84px}
.card.on{border-color:#e9b872;box-shadow:0 0 0 1px #e9b872}
.card b{display:block;font-size:19px;margin-bottom:3px}
.map{background-size:cover;display:flex;align-items:flex-end;min-height:80px;text-shadow:0 1px 6px #000}
.pill{display:inline-block;border:1px solid #ffffff33;border-radius:99px;padding:6px 16px;margin:0 8px 8px 0;background:none;color:#eef3f1;font:inherit;cursor:pointer}
.pill.on{background:#e9b872;color:#1b1a16;border-color:#e9b872}
label{display:inline-flex;align-items:center;gap:10px;margin:0 18px 8px 0}
input[type=color]{width:46px;height:34px;border:2px solid #fff;border-radius:8px;padding:0;background:none;cursor:pointer}
.go{margin-top:26px;width:100%;padding:15px;border:0;border-radius:12px;background:#e9b872;color:#1b1a16;font:600 18px Georgia,serif;cursor:pointer}
button:focus-visible,input:focus-visible{outline:2px solid #fff;outline-offset:2px}
#game{position:absolute;inset:0}canvas{position:absolute;inset:0;width:100%;height:100%}
#hud{position:absolute;top:calc(env(safe-area-inset-top,0px) + 8px);left:8px;right:8px;display:flex;gap:6px;align-items:center;flex-wrap:wrap;font-size:14px}
#hud>*{background:#0b161cb3;backdrop-filter:blur(6px);border-radius:10px;padding:6px 10px}
#hud button{border:1px solid #ffffff2b;color:#fff;font:inherit;cursor:pointer}
#hud input[type=range]{width:90px;vertical-align:middle;accent-color:#e9b872}
#bars{display:flex;gap:8px;align-items:center}.bar{width:80px;height:7px;border-radius:4px;background:#ffffff30;overflow:hidden}.bar i{display:block;height:100%;width:0;background:#e9b872}.bar.r i{background:#8fb4d4}
#panel{position:absolute;left:0;right:0;bottom:0;padding:16px 16px calc(env(safe-area-inset-bottom,0px) + 16px);background:linear-gradient(#0b161c00,#0b161ce6 22%)}
#txt{max-width:820px;margin:0 auto;direction:ltr;text-align:left;font:clamp(20px,2.8vw,28px)/1.55 Georgia,serif;color:#ffffff66;background:#0b161cbf;border-radius:14px;padding:14px 18px;cursor:text}
#txt .d{color:#bfe3c4}#txt .c{color:#1b1a16;background:#e9b872;border-radius:3px}#txt.bad .c{background:#e0675a}
#hint{text-align:center;font-size:13px;color:#cfd9d9;margin-top:8px}
#kb{position:absolute;opacity:0;left:0;bottom:0;width:1px;height:1px}
#end{position:absolute;inset:0;background:#06101699;display:grid;place-items:center;backdrop-filter:blur(4px)}
#end div{background:#12252d;border:1px solid #ffffff2b;border-radius:18px;padding:26px 30px;text-align:center;max-width:90%}
#end h1{font-size:32px}#end button{margin:6px}
#songs{position:fixed;top:56px;left:10px;right:10px;max-width:440px;margin:0 auto;z-index:30;background:#12252df2;border:1px solid #ffffff2b;border-radius:16px;padding:14px;max-height:calc(100% - 70px);overflow:auto;transition:opacity .2s,transform .2s}
#songs.min{opacity:0;pointer-events:none;transform:translateY(-12px)}
#songs a{display:inline-block;margin:0 0 8px 8px;padding:6px 12px;border:1px solid #ffffff33;border-radius:99px;color:#eef3f1;text-decoration:none;font-size:14px}
#songs input{width:100%;padding:9px;border-radius:8px;border:1px solid #ffffff44;background:#0b161c;color:#fff;margin-bottom:8px}
#songs iframe{width:100%;border:0;border-radius:12px;margin-top:8px}.sb{display:flex;justify-content:space-between;align-items:center}
#lv{display:grid;grid-template-columns:repeat(5,1fr);gap:8px}.lvb{padding:10px 0;border-radius:10px;border:1px solid #ffffff33;background:#0b161ca6;color:#fff;font:inherit;cursor:pointer}.lvb.on{background:#e9b872;color:#1b1a16;border-color:#e9b872}#lvi{margin:8px 0 0;color:#cfd9d9}

#menu{font-size:13px}#menu h1{font-size:clamp(24px,6vw,36px)}#menu .sub{font-size:12px;margin-bottom:12px}#menu h2{font-size:12px;margin:8px 0 6px}#menu .card{padding:9px 11px;min-height:60px;font-size:12px;border-radius:12px}#menu .card b{font-size:14px;margin-bottom:2px}#menu .map{min-height:56px}#menu .pill{font-size:12px;padding:4px 11px;margin:0 6px 6px 0}.lvb{padding:6px 0;font-size:12px}#lvi{font-size:12px;margin:6px 0 0}#menu .go{font-size:15px;padding:12px;margin-top:18px}
details{border:1px solid #ffffff22;border-radius:12px;background:#0b161c99;margin:8px 0;padding:0 10px}summary{cursor:pointer;padding:9px 2px;font-size:13px;color:#cfd9d9;list-style:none;display:flex;justify-content:space-between;gap:8px}summary::-webkit-details-marker{display:none}summary b{color:#e9b872;font-size:13px;font-family:inherit;font-weight:600}details[open]{padding-bottom:8px}details[open]>summary{border-bottom:1px solid #ffffff1a;margin-bottom:8px}
#hud{font-size:12px}#hud>*{padding:4px 8px}#hint{font-size:12px}#txt{font-size:clamp(17px,2.3vw,23px)}#songs,#set{font-size:13px}#songs a,#songs .pill,#set .pill{font-size:12px}#end p{font-size:14px}#end h1{font-size:24px}
#set{position:fixed;top:48px;left:10px;right:10px;max-width:420px;margin:0 auto;z-index:30;background:#12252df2;border:1px solid #ffffff2b;border-radius:16px;padding:12px 14px;transition:opacity .2s,transform .2s}#set.min{opacity:0;pointer-events:none;transform:translateY(-12px)}#set label{display:flex;justify-content:space-between;align-items:center;width:100%;margin:8px 0}#set input[type=range]{width:55%;accent-color:#e9b872}
</style></head><body>
<div id="menu"><svg id="flag" aria-hidden="true"></svg><div class="wrap">
<h1>تایپ بکە و سەرکەفتنێ ببینە</h1><p class="sub">چار یاریێن تایپکرنێ، شارێن راستەقینە و مۆسیقایا کوردی.</p>
<details open><summary>یاری <b id="cg"></b></summary><div class="row" id="games"></div></details>
<details><summary>شار <b id="cm"></b></summary><div class="row" id="maps"></div></details>
<details open><summary>شێواز <b id="cmd"></b></summary><div id="md"></div>
<div id="tmw"><span style="color:#a9bcbd">دەم</span><br><span id="tmp"></span> <input type="number" id="tmc" min="5" max="3600" placeholder="چرکە" aria-label="دەم ب چرکان" style="width:80px;padding:4px;border-radius:8px;border:1px solid #ffffff44;background:#0b161c;color:#fff"></div>
<div id="diff"><span style="color:#a9bcbd">خێراهییا نەیار</span><br><span id="dd"></span></div>
<div id="lvw"><div id="lv"></div><p id="lvi"></p></div></details>
<details id="mdlw"><summary>جۆرێ ترومبێلێ <b id="cmo"></b></summary><span id="mdl"></span></details>
<details><summary>ڕەنگ</summary><label id="l1">ڕەنگ <input type="color" id="c1"></label><label id="l2">جل <input type="color" id="c2"></label></details>
<details><summary>وێنەیێ شارێ خۆ</summary><input type="file" id="ph" accept="image/*"> <button class="pill" id="phx">لابرنا وێنەی</button></details>
<details><summary>بەگراوندێ دەستپێکێ <b id="cbg"></b></summary><span id="bgp"></span></details>
<button class="pill" id="sbtn2">♫ ستران و مۆسیقا</button>
<button class="go" id="start">دەستپێکرنا یارییێ</button>
</div></div>
<div id="game" hidden><canvas id="c"></canvas>
<div id="hud"><button id="gear">⚙ سێتینگ</button><span id="st">0.0 چرکە</span><span id="wp">0 ووشە/خولەک</span><span id="ac">100%</span><span id="sc"></span><div id="bars"><span>تو</span><div class="bar"><i id="b1"></i></div><span id="rl">نەیار</span><div class="bar r"><i id="b2"></i></div></div></div>
<div id="set" class="min"><div class="sb"><b>سێتینگ</b><button id="setx" class="pill">داخستن</button></div>
<div id="evw"><label>دەنگێ مەکینەیێ <input type="range" id="ve" min="0" max="1" step=".05" value=".6" aria-label="دەنگێ مەکینەیێ"></label><button id="esb" class="pill"></button></div>
<label>دەنگێ مۆسیقایێ <input type="range" id="mv2" min="0" max="2" step=".05" value="1" aria-label="دەنگێ مۆسیقایێ"></label>
<label>دەنگێ ستران (MP3) <input type="range" id="av" min="0" max="1" step=".05" value="1" aria-label="دەنگێ ستران"></label>
<div><button class="pill" id="sbtn">♫ مۆسیقا و ستران</button><button class="pill" id="rst">دووبارە یاری بکە</button><button class="pill" id="back">زڤڕین بۆ لیستێ</button></div></div>
<div id="panel"><div id="txt"></div><div id="hint">پیتا ڕەنگکری بنڤیسە دا دەست پێ بکەی.</div></div>
<input id="kb" autocomplete="off" autocapitalize="off" autocorrect="off" spellcheck="false" aria-label="جهێ تایپکرنێ">
<div id="end" hidden><div><h1 id="et"></h1><p id="es"></p><button class="pill on" id="nx" hidden>ئاستێ دی</button><button class="pill on" id="again">دووبارە یاری بکە</button><button class="pill" id="menu2">زڤڕین بۆ لیستێ</button></div></div>
</div>
<div id="songs" class="min"><div class="sb"><b>ستران</b><button id="sx" class="pill">داخستن</button></div><h3 style="font-size:15px;margin:6px 0">مۆسیقایا ناڤ یاریێ (ئوفلاین)</h3><div><button class="pill" id="mp">&lsaquo;</button><span id="ml"></span> <button class="pill" id="mn">&rsaquo;</button> <button class="pill on" id="mt">لێدان</button></div><input type="range" id="mv" min="0" max="2" step=".05" value="1" aria-label="دەنگێ مۆسیقایێ"><h3 style="font-size:15px;margin:14px 0 6px">ستران یێن ئوفلاین</h3><p style="font-size:13px;color:#cfd9d9;margin:0 0 8px">فایلێن MP3 جارەکێ زێدە بکە. دێ د یاریێ دا مینن و بێ ئینتەرنێت لێ دهێن.</p><input type="file" id="sg" accept="audio/*" multiple><audio id="au" controls style="width:100%;margin:8px 0"></audio><div id="ol"></div><button class="pill" id="oc">پاکرنا سترانان</button></div>
<script>
const $=s=>document.querySelector(s),SEL={g:0,m:0,d:1,r:1,md:1,bg:0,mo:0,l:1,t:0};
const GN=['پێشبڕکێیا ترومبێلان','سەرکەفتنا پەیژێ','پێشبڕکێیا بایسکلان','پێشبڕکێیا مۆتۆران'],GD=['ترومبێلەکێ هەلبژێرە و د شارێن مەزن دا بەز بچە.','پەیژێن راستەقینە، هەنگاڤێن راستەقینە. بگەهە سەری.','بایسکلا خۆ ڕەنگ بکە و د شاری دا بچە.','مۆتۆرێن بەز ل سەر ڕێکێن شاری.'];
const CITY=[['پاریس','linear-gradient(#7cc8ff,#f3e3c3)'],['تۆکیۆ','linear-gradient(#ffb3d9,#9fb4ff)'],['نیۆیۆرک','linear-gradient(#6db3ff,#c9ced8)'],['ڕیۆ دی ژانێرۆ','linear-gradient(#ffd36b,#4fbf6a)'],['لەندەن','linear-gradient(#a9c3d8,#b86a4f)'],['دوبەی','linear-gradient(#ffcf8a,#e8cf9a)']];
const CLM=[['ڕۆما: پەیژێن ئیسپانی','linear-gradient(#5f9fd8,#d8a673)'],['پاریس: مۆنمارتر','linear-gradient(#3a3f7a,#f7c89c)'],['کیۆتۆ: دەرگەهێن سور','linear-gradient(#bcd0c0,#c9371f)'],['نیۆیۆرک: سەربانێ شەڤێ','linear-gradient(#050a1a,#3a4f7c)']];
const COL=[['#ff5a4d','#2b3a54'],['#ff8a4a','#2b3a54'],['#e63946','#2b3a54'],['#ffb703','#2b3a54']],LB=[['ڕەنگێ ترومبێلێ',''],['جاکێت','پانتۆل'],['ڕەنگێ بایسکلێ','جل'],['ڕەنگێ مۆتۆرێ','جل']];
const CM=['کوپێ','هاچبەک','ئێس یو ڤی','پیکاپ'],DN=['ئارام','ناڤنجی','بەز'],OPP=[2.6,3.6,4.8];
const POOL=(()=>{let s=2026;const R=()=>((s=(s*1664525+1013904223)>>>0)/4294967296),sh=a=>{for(let i=a.length-1;i>0;i--){const j=Math.floor(R()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a},A=w=>(/^[aeiou]/.test(w)?'an ':'a ')+w,
nm=['sam','ali','sara','lina','omar','nora','ahmed','zara','dara','rojin','shirin','kawa','hana'],
ca=['plays in the park','walks to school','reads a book','drinks hot tea','eats bread and cheese','runs in the park','sings a song','cooks dinner','cleans the room','opens the door','draws a picture','washes the car','waits for the bus','plays with a ball','works in the garden','goes to the market','plays with the dog','looks at the sky','visits the city'],
tm=['in the morning','in the evening','at night','after school','every day','on monday','on friday','today'],
pe=['mother','father','brother','sister','friend','teacher','uncle','aunt','grandmother','grandfather'],
ob=['house','tree','book','bag','hat','ball','phone','door','table','chair','bed','cup','clock','lamp','kite'],ve=['car','bike','bus','train','boat'],
aj=['big','small','new','old','red','blue','green','yellow','white','black','nice','good','clean','pretty'],
fd=['bread','rice','milk','tea','cake','soup','cheese','water','juice','apples','bananas','oranges','eggs','tomatoes'],
pl=['park','school','shop','market','river','mountain','beach','city','farm','garden','library'],dy=['monday','tuesday','wednesday','thursday','friday','saturday','sunday'],
an=['dog','cat','horse','cow','sheep','rabbit','duck','bird'],p2=['garden','park','farm','street','room','city'],
aa=['is small','is big','is black','is white','is very nice','sleeps in the sun','is happy today','is hungry'],
wt=['hot','cold','sunny','windy','rainy','nice','very hot','very cold','a good day'],fe=['happy','tired','hungry','ready','fine'],wn=['today','now','at home','at school','in the park'],L=Array.from({length:13},()=>[]),ov=ob.concat(ve);
nm.forEach(n=>{ca.forEach(a=>tm.forEach(t=>L[0].push(`${n} ${a} ${t}.`)));pl.forEach(q=>L[10].push(`${n} and i go to the ${q}.`))});
pe.forEach(q=>{ca.forEach(a=>L[1].push(`my ${q} ${a}.`));pl.forEach(z=>L[6].push(`i go to the ${z} with my ${q}.`))});
ov.forEach(o=>aj.forEach(a=>{L[2].push(`the ${o} is ${a}.`);L[3].push(`i have ${A(a)} ${o}.`)}));ve.forEach(v=>['fast','slow'].forEach(a=>L[2].push(`the ${v} is ${a}.`)));
['like','love','want','need'].forEach(v=>fd.forEach(f=>L[4].push(`i ${v} ${f}.`)));pl.forEach(q=>dy.forEach(d=>L[5].push(`we go to the ${q} on ${d}.`)));
an.forEach(a=>{p2.forEach(q=>L[7].push(`there is ${A(a)} in the ${q}.`));aa.forEach(x=>L[8].push(`the ${a} ${x}.`))});
wt.forEach(w=>L[9].push(`it is ${w} today.`));fe.forEach(f=>wn.forEach(w=>L[11].push(`i am ${f} ${w}.`)));['play','walk','run','sit','read'].forEach(v=>['garden','park','room','house'].forEach(q=>L[12].push(`i like to ${v} in the ${q}.`)));
L.forEach(sh);const out=[];let w=0,i=0;while(w<10000){let y=0;for(const l of L)if(i<l.length){out.push(l[i]);w+=l[i].split(' ').length;y=1}if(!y)break;i++}return out})();
function nextText(m=90){let v=null;try{v=localStorage.getItem('tg_p')}catch(e){}let P=v==null?Math.floor(Math.random()*POOL.length):+v,t='';while(t.length<m){t+=(t?' ':'')+POOL[P%POOL.length];P++}try{localStorage.setItem('tg_p',P%POOL.length)}catch(e){}return t}
try{SEL.l=Math.min(20,Math.max(1,+localStorage.getItem('tg_l')||1));SEL.bg=Math.min(5,+localStorage.getItem('tg_bg')||0)}catch(e){}
const TP=[null,['yesterday i went to the market with my mother and bought some fresh vegetables.','my brother is learning to play the guitar because he wants to join a band.','we are going to visit our grandparents in the village next weekend.','it was raining all morning, so we stayed at home and watched a film.','can you tell me where the nearest bus station is, please?','she usually drinks a cup of coffee before she goes to work.','i have been living in this city for three years and i like it a lot.','the shop closes at six o\'clock, so we must hurry.','last summer we travelled to the mountains and walked by a beautiful river.','if the weather is good tomorrow, we will have a picnic in the park.','my teacher says that reading every day will help me learn english.','the train to the airport leaves in ten minutes, so please run.'],
['Although it was late, we decided to finish the project before going home.','She has been working at the hospital since she graduated from university.','If I had more free time, I would travel around the world and learn new languages.','The film was so exciting that nobody wanted to leave the cinema.','You should drink more water and get enough sleep if you want to feel better.','My cousin, who lives in London, is going to visit us in the spring.','I used to play football every weekend, but now I prefer to go swimming.','The company announced that it would open three new offices next year.','We could not find a table at the restaurant, so we ate at a small cafe nearby.','Learning a language takes patience, but the results are always worth the effort.','He apologised for being late and explained that the traffic had been terrible.','It is important to save some money every month in case of an emergency.'],
['Despite the heavy rain, thousands of people gathered in the square to celebrate the festival.','The new policy has been criticised for failing to address the needs of young families.','Had I known about the delay, I would have booked a different flight.','Scientists are increasingly worried about the impact of plastic waste on marine life.','She managed to persuade her manager to let the team work from home twice a week.','The more you practise typing, the faster and more accurate you become.','Not only did they finish the building on time, but they also stayed under budget.','It is widely believed that regular exercise reduces stress and improves concentration.','The museum, which was founded in 1890, attracts visitors from all over the world.','Whether we like it or not, technology is changing the way we work and communicate.','He was reluctant to accept the offer because it would mean moving abroad.','By the time the ambulance arrived, the injured driver had already been taken to hospital.'],
['The committee\'s decision, though controversial, reflects a genuine attempt to balance economic growth with environmental responsibility.','Rarely have I encountered such a meticulous researcher, whose arguments are as persuasive as they are well documented.','Having weighed the evidence carefully, the jury concluded that the defendant could not have been present at the scene.','The negotiations collapsed because neither side was prepared to make the concessions that a lasting agreement would require.','Her unconventional approach to teaching, which encourages students to question everything, has earned both admiration and criticism.','Were it not for the generous support of local volunteers, the restoration of the old library would have been impossible.','Economists remain divided over whether the recent slowdown is a temporary setback or a sign of deeper structural problems.','In an era of information overload, the ability to distinguish reliable sources from misleading ones is indispensable.','The novel, set against the backdrop of a crumbling empire, explores the fragile boundary between loyalty and betrayal.','Notwithstanding the initial scepticism, the pilot scheme proved remarkably effective in reducing urban congestion.','He spoke with such eloquence that even his fiercest opponents grudgingly acknowledged the force of his argument.','Unless urgent measures are taken, many of the region\'s rarest species will have disappeared within a generation.'],
['The ostensibly innocuous remark, uttered with studied nonchalance, precipitated a rift that would take years to mend.','Inasmuch as language shapes thought, the subtle idiosyncrasies of a dialect may illuminate an entire worldview.','Her prose, at once luminous and unsparing, resists the facile consolations that lesser writers habitually offer.','The treaty\'s ambiguous wording afforded each signatory ample latitude to interpret its obligations to its own advantage.','It would be disingenuous to suggest that the reforms were wholly altruistic; self-interest, as ever, played its part.','Scarcely had the exhibition opened when critics, bewildered by its deliberate austerity, began to question its ambition.','Notwithstanding the exigencies of the moment, the diplomat maintained an equanimity that bordered on the inscrutable.','The philosopher contended that moral intuition, however compelling, cannot be divorced from the contingencies of culture and history.','Meticulously reconstructed from fragmentary manuscripts, the epic offers an unparalleled glimpse into a vanished civilisation.','What began as a modest experiment in cooperative farming gradually burgeoned into a sprawling, self-sustaining community.','Though ephemeral by nature, the fleeting pleasures of everyday life are what render existence tolerable, even luminous.','Her uncharacteristically laconic reply, delivered without so much as a glance, betrayed a profound and carefully concealed disquiet.']],
CEF=['A1','A1','A1','A2','A2','A2','B1','B1','B1','B1','B2','B2','B2','B2','C1','C1','C1','C2','C2','C2'],TO=[[0,'بێ دەم'],[30,'30 چرکە'],[60,'1 خولەک'],[120,'2 خولەک'],[180,'3 خولەک']],BAG=[[],[],[],[],[],[]];
const LV=()=>SEL.md==2?SEL.l:SEL.md==0?(SEL.t>0?9:2):3;
function tierOf(l){return l<=3?0:l<=6?1:l<=10?2:l<=14?3:l<=17?4:5}
function gen(l,min){const t=tierOf(l);if(!t)return nextText(min);let o='';while(o.length<min){if(!BAG[t].length){BAG[t]=TP[t].slice().sort(()=>Math.random()-.5)}o+=(o?' ':'')+BAG[t].pop()}return o}
function mkx(){$('#tmw').hidden=SEL.md!=0;$('#tmp').innerHTML=TO.map(([v,n])=>`<button class="pill ${SEL.t==v?'on':''}" data-t="${v}">${n}</button>`).join('');
$('#lv').innerHTML=Array.from({length:20},(_,i)=>`<button class="lvb ${SEL.l==i+1?'on':''}" data-l="${i+1}">${i+1}</button>`).join('');$('#lvi').textContent=`لیڤل ${SEL.l}: ئاستێ ${CEF[SEL.l-1]}، زەحمەتی ${SEL.l*5}%`}
$('#tmc').oninput=e=>{const v=Math.round(+e.target.value);SEL.t=v>=5?Math.min(3600,v):0;mkx()};
let PH=null;
const sv=(b,g)=>`linear-gradient(#0005,#0005),url("data:image/svg+xml,${encodeURIComponent('<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 600" preserveAspectRatio="xMidYMax slice">'+b+'</svg>')}") center/cover no-repeat,${g}`;
const BG=[['ئالا',''],
['چیا',sv('<circle cx="300" cy="170" r="40" fill="#ffd9a0"/><path d="M0 600V380L90 280L170 390L260 250L400 400V600Z" fill="#2c4a63"/><path d="M0 600V470L120 360L210 480L310 340L400 470V600Z" fill="#183246"/>','linear-gradient(#324f77,#e9a96a)')],
['شار',sv('<g fill="#0a141b"><rect x="10" y="380" width="50" height="220"/><rect x="70" y="310" width="60" height="290"/><rect x="140" y="400" width="50" height="200"/><rect x="200" y="280" width="70" height="320"/><rect x="280" y="360" width="50" height="240"/><rect x="340" y="330" width="60" height="270"/></g><g fill="#ffd27a"><rect x="85" y="330" width="8" height="8"/><rect x="215" y="310" width="8" height="8"/><rect x="355" y="360" width="8" height="8"/><rect x="25" y="410" width="8" height="8"/></g>','linear-gradient(#0b1a33,#5b3b6e)')],
['دەریا',sv('<circle cx="200" cy="330" r="55" fill="#ffcf8a"/><path d="M0 360H400V600H0Z" fill="#1f5a7a"/><path d="M0 420Q100 400 200 420T400 420V600H0Z" fill="#17465f"/>','linear-gradient(#f2a56b,#f7d7a1)')],
['دارستان',sv('<g fill="#13351f"><path d="M40 600L90 330L140 600Z"/><path d="M130 600L190 280L250 600Z"/><path d="M240 600L300 340L360 600Z"/></g><g fill="#0c2415"><path d="M-20 600L30 420L80 600Z"/><path d="M320 600L370 410L420 600Z"/></g>','linear-gradient(#5fa089,#cfe3c0)')],
['ئەستێر',sv('<g fill="#fff"><circle cx="50" cy="60" r="2"/><circle cx="130" cy="140" r="1.5"/><circle cx="220" cy="80" r="2"/><circle cx="310" cy="170" r="1.5"/><circle cx="360" cy="50" r="2"/><circle cx="90" cy="250" r="1.5"/><circle cx="270" cy="280" r="2"/></g><circle cx="320" cy="110" r="26" fill="#f4efd8"/>','linear-gradient(#050a1c,#1a2b55)')]];
function bgSet(){const m=$('#menu');$('#flag').style.display=SEL.bg?'none':'';m.style.background=SEL.bg?BG[SEL.bg][1]:''}
const MD3=['تنێ یاری بکە','دگەل نەیارەکی یاری بکە','لیڤلان'];
function mk(){mkx();const G=SEL.g,ML=G==1?CLM:CITY;$('#games').innerHTML=GN.map((n,i)=>`<button class="card ${G==i?'on':''}" data-g="${i}"><b>${n}</b>${GD[i]}</button>`).join('');
$('#maps').innerHTML=ML.map((a,i)=>`<button class="card map ${SEL.m==i?'on':''}" data-m="${i}" style="background-image:${a[1]}"><b>${a[0]}</b></button>`).join('');
$('#md').innerHTML=MD3.map((n,i)=>`<button class="pill ${SEL.r==i?'on':''}" data-r="${i}">${n}</button>`).join('');
$('#dd').innerHTML=DN.map((n,i)=>`<button class="pill ${SEL.d==i?'on':''}" data-d="${i}">${n}</button>`).join('');$('#diff').hidden=SEL.md!=1;$('#lvw').hidden=SEL.md!=2;$('#cg').textContent=GN[G];$('#cm').textContent=ML[SEL.m][0];$('#cmd').textContent=MD3[SEL.md];$('#cmo').textContent=CM[SEL.mo];
$('#mdl').innerHTML=CM.map((n,i)=>`<button class="pill ${SEL.mo==i?'on':''}" data-o="${i}">${n}</button>`).join('');$('#mdlw').hidden=G!=0;
$('#l1').firstChild.textContent=LB[G][0]+' ';$('#l2').firstChild.textContent=LB[G][1]+' ';$('#l2').hidden=G==0;$('#c1').value=COL[G][0];$('#c2').value=COL[G][1];$('#bgp').innerHTML=BG.map((b,i)=>`<button class="pill ${SEL.bg==i?'on':''}" data-b="${i}">${b[0]}</button>`).join('');$('#cbg').textContent=BG[SEL.bg][0];bgSet()}
$('#menu').onclick=e=>{const b=e.target.closest('[data-g],[data-m],[data-d],[data-r],[data-o],[data-l],[data-t],[data-b]');if(!b)return;const d=b.dataset;if(d.l!=null){SEL.l=+d.l;try{localStorage.setItem('tg_l',SEL.l)}catch(x){}}if(d.t!=null){SEL.t=+d.t;$('#tmc').value=''}if(d.g!=null){SEL.g=+d.g;SEL.m=0}if(d.m!=null)SEL.m=+d.m;if(d.d!=null)SEL.d=+d.d;if(d.r!=null){SEL.md=+d.r;SEL.r=SEL.md>0?1:0}if(d.b!=null){SEL.bg=+d.b;try{localStorage.setItem('tg_bg',d.b)}catch(x){}}if(d.o!=null)SEL.mo=+d.o;mk();if(d.g!=null||d.m!=null||d.o!=null||d.l!=null){const q=b.closest('details');if(q)q.open=false}};
$('#c1').oninput=e=>COL[SEL.g][0]=e.target.value;$('#c2').oninput=e=>COL[SEL.g][1]=e.target.value;
$('#ph').onchange=e=>{const f=e.target.files[0];if(!f)return;const r=new FileReader();r.onload=()=>{const i=new Image();i.onload=()=>PH=i;i.src=r.result};r.readAsDataURL(f)};
$('#phx').onclick=()=>{PH=null;$('#ph').value=''};
mk();
/* ---------- engine sound, songs, flag ---------- */
let ac,EV=.6,ES=0,ef,eg;
function engine(){if(!ac)ac=new(window.AudioContext||window.webkitAudioContext)();ac.resume()}
$('#ve').oninput=e=>{EV=+e.target.value};
const PR=[{c:4,d:7,k:2.2,lp:1800,n:.3},{c:8,d:5,k:1.3,lp:1000,n:.45},{el:1,lp:5000},{c:4,d:10,k:3.4,lp:900,n:.6}],EL=['دەنگێ ئاسایی','دەنگێ V8','دەنگێ کارەبایی','دەنگێ دیزڵ'];
let esp,ER=900,EG=0,erc=900,egc=0,eph=0,eph2=0,enz=0;
function engInit(){esp=ac.createScriptProcessor(2048,0,1);ef=ac.createBiquadFilter();ef.type='lowpass';eg=ac.createGain();esp.connect(ef);ef.connect(eg);eg.connect(ac.destination);
esp.onaudioprocess=e=>{const o=e.outputBuffer.getChannelData(0),sr=ac.sampleRate,P=PR[ES],mc=SEL.g==3,cy=mc?Math.max(1,P.c/4):P.c;ef.frequency.value=P.lp*(mc?1.6:1);
for(let i=0;i<o.length;i++){erc+=(ER-erc)*.0005;egc+=(EG-egc)*.0012;let v;
if(P.el){eph2+=erc/60*5/sr;eph2%=1;v=(Math.sin(6.2832*eph2)+.4*Math.sin(12.566*eph2))*.4}
else{eph+=erc/60*cy/2/sr;if(eph>=1)eph-=1;enz=enz*.6+(Math.random()*2-1)*.4;v=Math.exp(-P.d*eph)*Math.sin(6.2832*eph*P.k+1)*.8+enz*P.n*Math.exp(-12*eph)+Math.sin(6.2832*eph)*.2}
o[i]=Math.max(-1,Math.min(1,v*egc))}}}
function eng(rev,on){if(!ac)return;if(!esp)engInit();const mc=SEL.g==3;ER=(mc?1600:900)+rev*(mc?7500:5200);EG=on?EV*(.3+.7*rev):0}
function esl(){$('#esb').textContent=EL[ES]}$('#esb').onclick=()=>{ES=(ES+1)%4;esl()};esl();
const tgl=()=>$('#songs').classList.toggle('min');$('#sbtn').onclick=tgl;$('#sbtn2').onclick=tgl;$('#sx').onclick=tgl;
const DBo=()=>new Promise((res,rej)=>{const q=indexedDB.open('tg_songs',1);q.onupgradeneeded=()=>q.result.createObjectStore('s',{autoIncrement:true});q.onsuccess=()=>res(q.result);q.onerror=()=>rej()});
let OL=[],oi=0;const au=$('#au');
function oRender(){const box=$('#ol');box.innerHTML='';OL.forEach((x,i)=>{const b=document.createElement('button');b.className='pill'+(i==oi?' on':'');b.textContent='♫ '+x.n.slice(0,22);b.onclick=()=>{oi=i;oPlay()};box.appendChild(b)})}
function oPlay(){if(!OL.length)return;mStop();au.src=OL[oi].u;au.play().catch(()=>{});oRender()}
au.onended=()=>{oi=(oi+1)%OL.length;oPlay()};
async function oSave(fs){try{const d=await DBo(),st=d.transaction('s','readwrite').objectStore('s');st.clear();for(const f of fs)st.add({n:f.name,b:f})}catch(e){}}
async function oLoad(){try{const d=await DBo(),q=d.transaction('s').objectStore('s').getAll();q.onsuccess=()=>{if(q.result.length){OL=q.result.map(x=>({n:x.n,u:URL.createObjectURL(x.b)}));oi=0;oRender()}}}catch(e){}}
$('#sg').onchange=e=>{const fs=[...e.target.files];if(!fs.length)return;OL=fs.map(f=>({n:f.name,u:URL.createObjectURL(f)}));oi=0;oSave(fs);oPlay()};
$('#oc').onclick=async()=>{au.pause();au.removeAttribute('src');OL=[];oRender();try{const d=await DBo();d.transaction('s','readwrite').objectStore('s').clear()}catch(e){}};
oLoad();
const rng=s=>()=>((s=(s*1664525+1013904223)>>>0)/4294967296),MQ=[[0,1,4,5,7,8,10],[0,1,3,5,7,8,10],[0,2,3,5,7,8,11],[0,2,4,5,7,9,11],[0,2,3,5,7,9,10]],MN=['گەڤەند','هەیران','هەلپەرکێ'];
let mgm,mb,mtk=0,mtmr,mpl=0,mi=1,MVl=1,mnb;const KC={};
function mInit(){engine();if(mgm)return;mgm=ac.createGain();mgm.gain.value=MVl;mb=ac.createBiquadFilter();mb.type='lowpass';mb.frequency.value=3400;const L=ac.sampleRate*2,ir=ac.createBuffer(2,L,ac.sampleRate);for(let c=0;c<2;c++){const a=ir.getChannelData(c);for(let i=0;i<L;i++)a[i]=(Math.random()*2-1)*Math.pow(1-i/L,3)}const cv=ac.createConvolver();cv.buffer=ir;const w=ac.createGain();w.gain.value=.45;mb.connect(mgm);mb.connect(cv);cv.connect(w);w.connect(mgm);mgm.connect(ac.destination)}
function pluck(m,t,v,d){const sr=ac.sampleRate;let b=KC[m];if(!b){const N=Math.round(sr/(440*Math.pow(2,(m-69)/12))),len=Math.round(sr*1.6),o=(b=KC[m]=ac.createBuffer(1,len,sr)).getChannelData(0),ring=new Float32Array(N);for(let i=0;i<N;i++)ring[i]=Math.random()*2-1;let p=0;for(let i=0;i<len;i++){const a=ring[p],c=ring[(p+1)%N];o[i]=a;ring[p]=.4975*(a+c);p=(p+1)%N}}
const s=ac.createBufferSource(),g=ac.createGain();s.buffer=b;g.gain.setValueAtTime(v,t);g.gain.exponentialRampToValueAtTime(.001,t+d);s.connect(g);g.connect(mb);s.start(t);s.stop(t+d+.05)}
function msine(m,t,d,v){const o=ac.createOscillator(),e=ac.createGain();o.frequency.value=440*Math.pow(2,(m-69)/12);e.gain.setValueAtTime(0,t);e.gain.linearRampToValueAtTime(v,t+.5);e.gain.linearRampToValueAtTime(0,t+d);o.connect(e);e.connect(mb);o.start(t);o.stop(t+d+.05)}
function mfl(m,t,d,v){const o=ac.createOscillator(),l=ac.createOscillator(),lf=ac.createGain(),e=ac.createGain();o.frequency.value=440*Math.pow(2,(m-69)/12);l.frequency.value=5.5;lf.gain.value=14;l.connect(lf);lf.connect(o.detune);e.gain.setValueAtTime(0,t);e.gain.linearRampToValueAtTime(v,t+.12);e.gain.linearRampToValueAtTime(v*.7,t+d*.7);e.gain.linearRampToValueAtTime(0,t+d);o.connect(e);e.connect(mb);o.start(t);l.start(t);o.stop(t+d+.05);l.stop(t+d+.05)}
function mdrum(t,k){if(!mnb){mnb=ac.createBuffer(1,ac.sampleRate,ac.sampleRate);const a=mnb.getChannelData(0);for(let i=0;i<a.length;i++)a[i]=Math.random()*2-1}const e=ac.createGain();e.connect(mgm);
if(k){const s=ac.createBufferSource(),f=ac.createBiquadFilter();s.buffer=mnb;f.type='highpass';f.frequency.value=2200;s.connect(f);f.connect(e);e.gain.setValueAtTime(.2,t);e.gain.exponentialRampToValueAtTime(.001,t+.09);s.start(t);s.stop(t+.12)}
else{const o=ac.createOscillator();o.frequency.setValueAtTime(150,t);o.frequency.exponentialRampToValueAtTime(48,t+.14);o.connect(e);e.gain.setValueAtTime(.6,t);e.gain.exponentialRampToValueAtTime(.001,t+.3);o.start(t);o.stop(t+.32)}}
function mPlay(id){mi=id;$('#ml').textContent=MN[id%3]+' '+id;if(!ac||!mpl)return;const k=++mtk;clearTimeout(mtmr);const r=rng(id*7919+101),st=id%3,sc=MQ[Math.floor(r()*5)],key=50+Math.floor(r()*7),bt=60/[118,72,138][st]/2,dr=['D.t.D.tt','D...t...','D.tDt.tt'][st];
const dg=d=>key+sc[((d%7)+7)%7]+12*Math.floor(d/7),mk=(a,z)=>{let w=a;const o=[];for(let i=0;i<16;i++){w=Math.max(-2,Math.min(8,w+Math.floor(r()*5)-2));o.push(r()<.2&&i%2?null:w)}o[0]=a;o[15]=z;return o};
const A=mk(0,2),A2=A.slice(0,12).concat(mk(1,0).slice(12)),B=mk(4,3),S=[A,A2,B,A];let n=0;
(function bar(){if(k!==mtk)return;const t=ac.currentTime+.08,q=Math.floor(n/2)%4,sec=S[q],off=(n%2)*8,ro=dg(0)-12;pluck(ro,t,.45,bt*4);pluck(ro+7,t+bt*4,.35,bt*4);msine(ro,t,bt*8.2,.05);
for(let j=0;j<8;j++){const c=dr[j];if(c=='D')mdrum(t+j*bt,0);else if(c=='t')mdrum(t+j*bt,1);const d=sec[off+j];if(d==null)continue;pluck(dg(d)+12,t+j*bt,j%4==0?.5:.36,bt*(j%2?2:3.2));if(st==1&&j%4==0)mfl(dg(d)+12,t+j*bt,bt*3.6,.1);if(q==2)pluck(dg(d)+24,t+j*bt+.01,.14,bt*1.5)}
n++;mtmr=setTimeout(bar,bt*8000-40)})()}
function mStop(){mpl=0;mtk++;clearTimeout(mtmr);$('#mt').textContent='لێدان'}
function mStart(){mInit();if(mpl)return;mpl=1;au.pause();mPlay(mi);$('#mt').textContent='ڕاگرتن'}
$('#mt').onclick=()=>mpl?mStop():mStart();$('#mn').onclick=()=>{mPlay(mi%12+1)};$('#mp').onclick=()=>{mPlay((mi+10)%12+1)};$('#mv').oninput=e=>{MVl=+e.target.value;if(mgm)mgm.gain.value=MVl;$('#mv2').value=MVl};$('#ml').textContent=MN[mi%3]+' '+mi;$('#mv2').oninput=e=>{MVl=+e.target.value;$('#mv').value=MVl;if(mgm)mgm.gain.value=MVl};$('#av').oninput=e=>{au.volume=+e.target.value};$('#gear').onclick=()=>$('#set').classList.toggle('min');$('#setx').onclick=()=>$('#set').classList.add('min');$('#rst').onclick=()=>{$('#set').classList.add('min');begin()};
(function(){let p='';for(let i=0;i<21;i++){const a=i*2*Math.PI/21-Math.PI/2,w=Math.PI/21*.55;for(const [r,q] of [[23,a-w],[41,a],[23,a+w]])p+=(150+r*Math.cos(q)).toFixed(1)+','+(100+r*Math.sin(q)).toFixed(1)+' '}
const f=$('#flag');f.setAttribute('viewBox','0 0 300 200');f.setAttribute('preserveAspectRatio','xMidYMid slice');
f.innerHTML='<rect width="300" height="67" fill="#ed2024"/><rect y="66.5" width="300" height="67" fill="#fff"/><rect y="133" width="300" height="67" fill="#278e43"/><polygon points="'+p+'" fill="#febd11"/><circle cx="150" cy="100" r="25" fill="#febd11"/><rect width="300" height="200" fill="rgba(7,16,20,.5)"/>'})();
/* ---------- helpers ---------- */
const cv=$('#c'),g=cv.getContext('2d'),O='#1f2a44';let W,H,SH;
function rs(){const D=Math.min(devicePixelRatio||1,2);W=innerWidth;H=innerHeight;SH=Math.max(220,H-(W<700?190:170));cv.width=W*D;cv.height=H*D;g.setTransform(D,0,0,D,0,0)}
addEventListener('resize',rs);rs();
const h=i=>Math.abs(Math.sin(i*127.1+3.7)*43758.5453)%1;
function lg(x0,y0,x1,y1,c){const q=g.createLinearGradient(x0,y0,x1,y1);c.forEach((v,i)=>q.addColorStop(i/(c.length-1),v));return q}
function glow(x,y,r,c){const q=g.createRadialGradient(x,y,0,x,y,r);q.addColorStop(0,c);q.addColorStop(1,'rgba(255,200,140,0)');g.fillStyle=q;g.fillRect(x-r,y-r,2*r,2*r)}
function shade(c,f){const n=parseInt(c.slice(1),16),m=f<0?0:255,a=Math.abs(f),p=v=>Math.round(v+(m-v)*a);return`rgb(${p(n>>16)},${p(n>>8&255)},${p(n&255)})`}
function cover(im,x,y,w,hh){const r=Math.max(w/im.width,hh/im.height),iw=w/r,ih=hh/r;g.drawImage(im,(im.width-iw)/2,(im.height-ih)/2,iw,ih,x,y,w,hh)}
function ridge(par,cx,cy,base,amp,cols,sd,hz){g.fillStyle=lg(0,base-amp,0,base+10,cols);g.beginPath();g.moveTo(0,hz);for(let x=0;x<=W;x+=14){const w=x+cx*par;g.lineTo(x,base-amp*(Math.sin(w*.004+sd)*.5+Math.sin(w*.011+sd*2)*.3+.5)+cy)}g.lineTo(W,hz);g.fill()}
function pine(x,y,s,c){g.fillStyle=c;for(let k=0;k<3;k++){const w=s*(.5-k*.1),yy=y-s*.35*k-s*.12;g.beginPath();g.moveTo(x-w,yy);g.lineTo(x,yy-s*.55);g.lineTo(x+w,yy);g.fill()}g.fillRect(x-s*.04,y-s*.12,s*.08,s*.14)}
/* ---------- cartoon pieces ---------- */
function cloud(x,y,s){g.beginPath();[[0,0,22],[24,-9,28],[52,0,22],[26,8,24]].forEach(([a,b,r])=>{g.moveTo(x+(a+r)*s,y+b*s);g.arc(x+a*s,y+b*s,r*s,0,7)});g.strokeStyle=O;g.lineWidth=7;g.stroke();g.fillStyle='#fff';g.fill()}
function bld(x,b,w,ht,c,roof){g.fillStyle=c;g.strokeStyle=O;g.lineWidth=3;g.fillRect(x,b-ht,w,ht);g.strokeRect(x,b-ht,w,ht);g.fillStyle=roof;g.beginPath();g.moveTo(x-4,b-ht);g.lineTo(x+w/2,b-ht-w*.3);g.lineTo(x+w+4,b-ht);g.closePath();g.fill();g.stroke();
g.fillStyle='#fff4b0';for(let a=10;a<w-12;a+=18)for(let q=12;q<ht-10;q+=22)g.fillRect(x+a,b-ht+q,9,12)}
function tree(x,b,s,c){g.fillStyle='#8b5a2b';g.strokeStyle=O;g.lineWidth=3;g.fillRect(x-4*s,b-30*s,8*s,30*s);g.strokeRect(x-4*s,b-30*s,8*s,30*s);g.fillStyle=c;g.beginPath();g.arc(x,b-46*s,22*s,0,7);g.fill();g.stroke()}
const CP=[{s:['#7cc8ff','#e3f5ff'],b:['#f3e3c3','#e8d3a8','#f7ead2'],r:'#5a7fb8',gr:'#8fdc8a',t:'#4cc46a'},{s:['#ffb3d9','#fff1f7'],b:['#9fb4ff','#ff9fc3','#c9b6ff'],r:'#3b3f6b',gr:'#9fe3a6',t:'#ff9ccf'},{s:['#6db3ff','#d8ecff'],b:['#c9ced8','#b8a99c','#e0b89c'],r:'#5d6270',gr:'#a8d89a',t:'#58b868'},{s:['#ffd36b','#fff3c4'],b:['#ff9f7a','#ffd06a','#7fd6c2'],r:'#c7503a',gr:'#6fd17a',t:'#2fb36a'},{s:['#a9c3d8','#e8eef2'],b:['#b86a4f','#9b5a45','#c9a58a'],r:'#4a4f5a',gr:'#6fbf73',t:'#4cc46a'},{s:['#ffcf8a','#fff0d0'],b:['#e8d3a8','#d9b98a','#f0e0c0'],r:'#c9a06a',gr:'#e8cf9a',t:'#58b868'}];
const st3=(c)=>{g.fillStyle=c;g.strokeStyle=O;g.lineWidth=3};
const LM=[(x,b,s)=>{st3('#c9894d');g.beginPath();g.moveTo(x-46*s,b);g.lineTo(x-8*s,b-120*s);g.lineTo(x-3*s,b-200*s);g.lineTo(x,b-235*s);g.lineTo(x+3*s,b-200*s);g.lineTo(x+8*s,b-120*s);g.lineTo(x+46*s,b);g.lineTo(x+22*s,b);g.lineTo(x,b-70*s);g.lineTo(x-22*s,b);g.closePath();g.fill();g.stroke();g.fillRect(x-14*s,b-125*s,28*s,6*s)},
(x,b,s)=>{st3('#7d9be0');g.beginPath();g.moveTo(x-190*s,b);g.lineTo(x,b-190*s);g.lineTo(x+190*s,b);g.closePath();g.fill();g.stroke();g.fillStyle='#fff';g.beginPath();g.moveTo(x-48*s,b-142*s);g.lineTo(x,b-190*s);g.lineTo(x+48*s,b-142*s);g.lineTo(x+24*s,b-132*s);g.lineTo(x,b-150*s);g.lineTo(x-24*s,b-132*s);g.closePath();g.fill();g.stroke();st3('#ff6a3d');g.beginPath();g.moveTo(x+120*s,b);g.lineTo(x+136*s,b-120*s);g.lineTo(x+142*s,b-170*s);g.lineTo(x+148*s,b-120*s);g.lineTo(x+164*s,b);g.closePath();g.fill();g.stroke()},
(x,b,s)=>{st3('#aab4c8');[[30,60],[22,130],[14,190],[6,225]].forEach(([w,t])=>{g.fillRect(x-w*s,b-t*s,2*w*s,t*s);g.strokeRect(x-w*s,b-t*s,2*w*s,t*s)});g.beginPath();g.moveTo(x,b-225*s);g.lineTo(x,b-262*s);g.stroke();st3('#6fc3a0');g.fillRect(x+70*s,b-90*s,14*s,90*s);g.strokeRect(x+70*s,b-90*s,14*s,90*s)},
(x,b,s)=>{st3('#4fbf6a');g.beginPath();g.ellipse(x,b+12*s,160*s,125*s,0,Math.PI,0);g.fill();g.stroke();g.fillStyle='#fff';g.fillRect(x-4*s,b-170*s,8*s,58*s);g.fillRect(x-34*s,b-158*s,68*s,9*s);g.beginPath();g.arc(x,b-176*s,8*s,0,7);g.fill();g.stroke()},
(x,b,s)=>{st3('#d9c18b');g.fillRect(x-20*s,b-180*s,40*s,180*s);g.strokeRect(x-20*s,b-180*s,40*s,180*s);g.beginPath();g.moveTo(x-24*s,b-180*s);g.lineTo(x,b-232*s);g.lineTo(x+24*s,b-180*s);g.closePath();g.fill();g.stroke();g.fillStyle='#fff';g.beginPath();g.arc(x,b-150*s,12*s,0,7);g.fill();g.stroke();g.beginPath();g.arc(x+140*s,b-80*s,70*s,0,7);g.strokeStyle='#e8eef2';g.lineWidth=6;g.stroke()},
(x,b,s)=>{st3('#9fc7e6');g.beginPath();g.moveTo(x-26*s,b);g.lineTo(x-8*s,b-170*s);g.lineTo(x-3*s,b-250*s);g.lineTo(x,b-300*s);g.lineTo(x+3*s,b-250*s);g.lineTo(x+8*s,b-170*s);g.lineTo(x+26*s,b);g.closePath();g.fill();g.stroke();g.strokeStyle='#fff';for(let k=1;k<5;k++){g.beginPath();g.moveTo(x-20*s+k*2*s,b-k*45*s);g.lineTo(x+20*s-k*2*s,b-k*45*s);g.stroke()}}];
/* ---------- vehicles ---------- */
const BP=[null,{b:[[-98,-10],[-102,-40],[-90,-62],[10,-66],[30,-44],[92,-36],[102,-24],[98,-10]],w:[[-82,-46],[-80,-60],[0,-62],[22,-46]]},{b:[[-100,-10],[-102,-50],[-88,-70],[40,-70],[60,-46],[94,-38],[102,-24],[98,-10]],w:[[-82,-48],[-80,-66],[32,-66],[48,-48]]},{b:[[-100,-10],[-102,-38],[-30,-38],[-30,-64],[14,-66],[40,-44],[94,-38],[102,-24],[98,-10]],w:[[-22,-46],[-22,-58],[10,-60],[28,-46]]}];
function poly(a){a.forEach((p,i)=>i?g.lineTo(p[0],p[1]):g.moveTo(p[0],p[1]));g.closePath()}
function wheel(x,y,r,ph,sp){g.fillStyle='#222';g.strokeStyle=O;g.lineWidth=4;g.beginPath();g.arc(x,y,r,0,7);g.fill();g.stroke();g.fillStyle='#fff';g.beginPath();g.arc(x,y,r*.6,0,7);g.fill();g.lineWidth=2;for(let k=0;k<sp;k++){const a=ph+k*6.283/sp;g.beginPath();g.moveTo(x,y);g.lineTo(x+Math.cos(a)*r*.6,y+Math.sin(a)*r*.6);g.stroke()}}
function car(x,y,s,mo,c1,c2,ph){g.save();g.translate(x,y);g.scale(s,s);g.lineJoin='round';
g.fillStyle='rgba(0,0,0,.25)';g.beginPath();g.ellipse(0,2,104,8,0,0,7);g.fill();
g.fillStyle=c1;g.strokeStyle=O;g.lineWidth=4;g.beginPath();
if(!mo){g.moveTo(-99,-10);g.bezierCurveTo(-108,-24,-104,-33,-92,-35);g.lineTo(-68,-40);g.bezierCurveTo(-52,-44,-46,-66,-14,-70);g.bezierCurveTo(10,-72,26,-54,38,-43);g.bezierCurveTo(70,-39,90,-36,100,-27);g.bezierCurveTo(108,-22,106,-12,98,-10);g.closePath()}else poly(BP[mo].b);
g.fill();g.stroke();g.fillStyle=c2;g.fillRect(-98,-22,196,6);g.fillStyle='#bfe9ff';g.beginPath();
if(!mo){g.moveTo(-58,-43);g.bezierCurveTo(-44,-60,-30,-65,-12,-66);g.bezierCurveTo(6,-66,20,-54,30,-43);g.closePath()}else poly(BP[mo].w);
g.fill();g.stroke();g.fillStyle='#fff3a0';g.fillRect(93,-32,9,6);g.fillStyle='#ff5a5a';g.fillRect(-103,-32,6,7);
wheel(-62,-18,21,ph,1);wheel(60,-18,21,ph,1);g.restore()}
function limb(p,w,c){g.lineCap=g.lineJoin='round';g.beginPath();p.forEach((q,i)=>i?g.lineTo(q[0],q[1]):g.moveTo(q[0],q[1]));g.strokeStyle=O;g.lineWidth=w+5;g.stroke();g.strokeStyle=c;g.lineWidth=w;g.stroke()}
function ik2(hx,hy,fx,fy,l){const d=Math.min(Math.hypot(fx-hx,fy-hy),2*l-.5),t=Math.atan2(fy-hy,fx-hx),k=t-Math.acos(d/(2*l));return[hx+Math.cos(k)*l,hy+Math.sin(k)*l]}
function helmet(x,y,c){g.fillStyle=c;g.strokeStyle=O;g.lineWidth=3;g.beginPath();g.arc(x,y,12,0,7);g.fill();g.stroke();g.fillStyle='#223';g.fillRect(x+1,y-4,12,6)}
function bike(x,y,s,c1,cl,ph){g.save();g.translate(x,y);g.scale(s,s);g.fillStyle='rgba(0,0,0,.25)';g.beginPath();g.ellipse(0,2,70,6,0,0,7);g.fill();
wheel(-40,-22,22,ph,8);wheel(42,-22,22,ph,8);const a=ph*.6,pd=[[-4+Math.cos(a)*11,-26+Math.sin(a)*11],[-4-Math.cos(a)*11,-26-Math.sin(a)*11]],hp=[-16,-68],pc=shade(cl,-.35);
limb([hp,ik2(hp[0],hp[1],pd[1][0],pd[1][1],27),pd[1]],9,pc);
limb([[-40,-22],[-4,-26],[26,-62],[-12,-62],[-40,-22]],5,c1);limb([[-4,-26],[-14,-62]],5,c1);limb([[26,-62],[42,-22]],5,c1);limb([[24,-66],[28,-76],[38,-72]],4,'#444');g.fillStyle='#222';g.fillRect(-24,-68,16,5);
limb([hp,ik2(hp[0],hp[1],pd[0][0],pd[0][1],27),pd[0]],9,pc);limb([hp,[12,-102]],16,cl);limb([[10,-98],[24,-84],[36,-72]],7,shade(cl,.2));helmet(17,-113,c1);g.restore()}
function moto(x,y,s,c1,cl,ph){g.save();g.translate(x,y);g.scale(s,s);g.fillStyle='rgba(0,0,0,.25)';g.beginPath();g.ellipse(0,2,80,6,0,0,7);g.fill();
wheel(-46,-22,22,ph,6);wheel(46,-22,22,ph,6);limb([[-46,-22],[-14,-36],[8,-34]],7,'#555');limb([[46,-22],[34,-64]],6,'#999');limb([[-10,-30],[-54,-26]],6,'#888');
g.fillStyle='#444';g.strokeStyle=O;g.lineWidth=3;g.fillRect(-18,-44,34,22);g.strokeRect(-18,-44,34,22);
g.fillStyle=c1;g.beginPath();g.moveTo(-58,-44);g.lineTo(-38,-62);g.lineTo(-6,-60);g.lineTo(-8,-48);g.closePath();g.fill();g.stroke();g.beginPath();g.ellipse(12,-58,24,13,-.15,0,7);g.fill();g.stroke();
g.fillStyle='#222';g.fillRect(-32,-66,30,6);g.fillStyle='#fff3a0';g.beginPath();g.arc(42,-60,6,0,7);g.fill();g.stroke();limb([[34,-64],[26,-74],[14,-74]],4,'#333');
const hp=[-16,-66];limb([hp,ik2(hp[0],hp[1],2,-30,24),[2,-30]],10,shade(cl,-.35));limb([hp,[10,-102]],18,cl);limb([[8,-98],[20,-86],[26,-78]],8,shade(cl,.2));helmet(14,-114,c1);g.restore()}
function veh(G,x,y,s,rival,ph){const c=rival?['#5fb0ff','#2b3a54']:COL[G];if(G==0)car(x,y,s,rival?0:SEL.mo,c[0],shade(c[0],-.3),ph);else if(G==2)bike(x,y,s*.95,c[0],c[1],ph);else moto(x,y,s*.95,c[0],c[1],ph)}
/* ---------- state ---------- */
let S={};
function begin(){S={txt:gen(LV(),Math.max(55,50+LV()*8)),i:0,keys:0,err:0,t0:0,p:0,o:0,u:0,uo:0,tm:0,done:0,win:1,shown:0};
S.timed=SEL.md==0&&SEL.t>0;S.lv=LV();S.N=S.timed?300:Math.round(S.txt.length/4);$('#st').textContent=S.timed?SEL.t+' چرکە':'0.0 چرکە';$('#sc').textContent='خال: 0';$('#end').hidden=1;$('#b2').parentElement.hidden=$('#rl').hidden=!SEL.r;$('#evw').hidden=SEL.g!=0&&SEL.g!=3;
$('#hint').textContent='پیتا ڕەنگکری بنڤیسە دا دەست پێ بکەی.';draw();$('#kb').focus()}
function draw(){const t=S.txt,i=S.i,a=Math.max(0,i-30),z=a+140,e=x=>x.replace(/&/g,'&amp;').replace(/</g,'&lt;');$('#txt').innerHTML=`<span class="d">${e(t.slice(a,i))}</span><span class="c">${t[i]===' '?'&nbsp;':e(t[i]||'')}</span>${e(t.slice(i+1,z))}`}
const nz=c=>({'ي':'ی','ى':'ی','ك':'ک','ڕ':'ر'})[c]||c;
function press(c){if(S.done)return;if(!S.t0){S.t0=performance.now();$('#hint').textContent=SEL.r?'نەیارێ تە ڕێکەفت. بەردەوام بنڤیسە.':'ب ئارامی بنڤیسە.'}
S.keys++;if(nz(c)===nz(S.txt[S.i])){S.i++;S.lt=performance.now();if(S.timed&&S.txt.length-S.i<100)S.txt+=' '+gen(S.lv,100);$('#txt').classList.remove('bad');if(S.i>=S.txt.length){S.done=1;S.win=1}}else{S.err++;$('#txt').classList.add('bad');setTimeout(()=>$('#txt').classList.remove('bad'),140)}draw()}
$('#kb').oninput=e=>{for(const c of e.target.value)press(c);e.target.value=''};
$('#txt').onclick=()=>$('#kb').focus();
function show(){S.shown=1;const sec=S.timed?SEL.t:Math.max(.1,(performance.now()-S.t0)/1000),wpm=Math.round(S.i/5/(sec/60)),acc=S.keys?Math.round(100*(S.keys-S.err)/S.keys):100,sc=Math.max(0,S.i*10-S.err*5),bk=`tg_b_${SEL.g}_${S.timed?SEL.t:0}_${S.lv}`;let bs=0,nw=0;
try{bs=+localStorage.getItem(bk)||0;if(sc>bs){localStorage.setItem(bk,sc);nw=1;bs=sc}}catch(e){}
const lab=SEL.t>=60?SEL.t/60+' خولەک':SEL.t+' چرکە';
$('#et').textContent=S.timed?'دەم ب دوماهیک هات':!SEL.r?'تە یاری ب دوماهیک ئینا':S.win?'تو سەرکەفتی!':'نەیار یێ پێشتر گەهشتی';
$('#es').textContent=(SEL.md==2?`لیڤل ${SEL.l}. `:'')+(S.timed?`ل ماوێ ${lab} دا خالا تە ${sc} بوو. `:`خالا تە ${sc} بوو. `)+`${wpm} ووشە/خولەک، ${acc}% دروستی.`+(S.timed||!SEL.r?(nw?' تۆمارەکێ نوی!':' باشترین خال: '+bs):'');$('#nx').hidden=!(SEL.md==2&&S.win&&SEL.l<20);$('#end').hidden=0}
$('#start').onclick=()=>{engine();$('#menu').hidden=1;$('#game').hidden=0;rs();begin();if(OL.length&&au.paused)oPlay();else mStart()};
$('#again').onclick=begin;$('#nx').onclick=()=>{SEL.l++;try{localStorage.setItem('tg_l',SEL.l)}catch(e){}mk();begin()};$('#menu2').onclick=$('#back').onclick=()=>{$('#game').hidden=1;$('#menu').hidden=0};
/* ---------- race scene (cartoon cities) ---------- */
const RL=6000;
function race(){const G=SEL.g,P=CP[SEL.m],hz=SH*.46,cam=S.p*RL,off=W*.35,rt=SH*.6,rb=SH*.93,sc=Math.min(SH*.0027,W/470),k0=SH/330,gb=hz+(rt-hz)*.62;
g.fillStyle=lg(0,0,0,hz,P.s);g.fillRect(0,0,W,hz+1);
if(PH)cover(PH,0,0,W,gb);else{g.fillStyle='#fff3a0';g.strokeStyle=O;g.lineWidth=3;g.beginPath();g.arc(W*.8,SH*.14,SH*.06,0,7);g.fill();g.stroke();
for(let k=0;k<5;k++){const x=((k*W/4+h(k)*80-cam*.03-S.tm*12)%(W+240)+W+240)%(W+240)-120;cloud(x,SH*(.1+h(k+7)*.18),.7*k0+.2)}}
g.fillStyle=P.gr;g.fillRect(0,gb-2,W,rt-gb+2);
if(!PH){const sp=2400,j0=Math.floor(cam*.12/sp)-1;g.fillStyle=P.gr;g.fillRect(0,hz,W,rt-hz);
for(let k=j0;k<j0+3;k++){const x=k*sp+700-cam*.12;if(x>-350&&x<W+350)LM[SEL.m](x,hz+6,k0)}
for(let k=Math.floor(cam*.35/96)-1;k<(cam*.35+W)/96+2;k++){const w=64+h(k)*34,ht=SH*(.12+h(k+4)*.2);bld(k*96-cam*.35,gb,w,ht,P.b[k%3],P.r)}}
for(let k=Math.floor(cam/170)-1;k<(cam+W)/170+2;k++)tree(k*170+h(k)*60-cam+off,rt-2,k0*1.1,h(k)>.5?P.t:'#4cc46a');
g.fillStyle='#e8e2d0';g.fillRect(0,rt-6,W,6);g.fillStyle='#4b5068';g.fillRect(0,rt,W,rb-rt);g.fillStyle='#fff';const o=-(cam%130);for(let x=o;x<W;x+=130)g.fillRect(x,(rt+rb)/2-3,64,6);
g.fillStyle='#e8e2d0';g.fillRect(0,rb,W,SH-rb);g.fillStyle=O;g.fillRect(0,rt-1,W,3);g.fillRect(0,rb-1,W,3);
const fx=RL+110-cam+off;if(!S.timed&&fx<W+40&&fx>-40){for(let r=0;r<12;r++)for(let c=0;c<2;c++){g.fillStyle=(r+c)%2?'#111':'#fff';g.fillRect(fx+c*14,rt+r*(rb-rt)/12,14,(rb-rt)/12+1)}g.fillStyle='#ff5a5a';g.strokeStyle=O;g.fillRect(fx-4,rt-SH*.2,5,SH*.2);g.fillRect(fx+28,rt-SH*.2,5,SH*.2);g.fillRect(fx-4,rt-SH*.2,37,SH*.06);g.strokeRect(fx-4,rt-SH*.2,37,SH*.06)}
const oy=rt+(rb-rt)*.5,py=SEL.r?rt+(rb-rt)*.9:rt+(rb-rt)*.72,bn=Math.sin(S.tm*16)*1.6;
if(SEL.r)veh(G,S.o*RL-cam+off,oy+(S.t0?bn:0),sc*.93,1,S.o*RL/20);veh(G,off,py+(S.p>.001&&!S.done?bn:0),sc,0,cam/20)}
/* ---------- climb scene (realistic, life-like steps) ---------- */
function walker(hx,hy,s,A,B,sw,jc,pc){g.save();g.translate(hx,hy);g.scale(s,s);g.lineCap=g.lineJoin='round';
const leg=(f,col)=>{let fx=(f[0]-hx)/s,fy=(f[1]-hy)/s,d=Math.min(Math.hypot(fx,fy),51),t=Math.atan2(fy,fx),a=t-Math.acos(d/52),kx=Math.cos(a)*26,ky=Math.sin(a)*26;fx=Math.cos(t)*d;fy=Math.sin(t)*d;
g.strokeStyle=col;g.lineWidth=13;g.beginPath();g.moveTo(0,0);g.lineTo(kx,ky);g.lineTo(fx,fy);g.stroke();g.fillStyle='#f4f4f2';g.beginPath();g.ellipse(fx+6,fy+2,12,5.5,0,0,7);g.fill();g.fillStyle='#37373a';g.fillRect(fx-5,fy+4,22,2.5)};
const arm=(a,col)=>{const ex=Math.sin(a)*19,ey=-40+Math.cos(a)*19,b=a+.5,hx2=ex+Math.sin(b)*17,hy2=ey+Math.cos(b)*17;g.strokeStyle=col;g.lineWidth=10;g.beginPath();g.moveTo(0,-40);g.lineTo(ex,ey);g.lineTo(hx2,hy2);g.stroke();g.fillStyle='#d79c78';g.beginPath();g.arc(hx2,hy2,5,0,7);g.fill()};
leg(A,shade(pc,-.3));g.save();g.rotate(.1);arm(sw*.7,shade(jc,-.3));
g.fillStyle='#2f6f73';g.beginPath();g.roundRect(-26,-44,17,34,5);g.fill();
g.fillStyle=lg(-12,-48,12,0,[jc,shade(jc,-.3)]);g.beginPath();g.roundRect(-13,-48,26,48,8);g.fill();
g.restore();leg(B,pc);g.save();g.rotate(.1);arm(-sw*.7,jc);
g.fillStyle='#d79c78';g.fillRect(0,-56,7,9);g.fillStyle=lg(-9,-76,13,-52,['#f0c19e','#c68a68']);g.beginPath();g.arc(3,-62,12,0,7);g.fill();
g.fillStyle='#2a1b14';g.beginPath();g.arc(1,-64,12.5,Math.PI*.95,Math.PI*1.95);g.lineTo(-8,-60);g.fill();g.fillStyle='#1b1b1b';g.beginPath();g.arc(10,-62,1.7,0,7);g.fill();g.restore();g.restore()}
const STN=[['#d9c3a0','#8a7358','#eddcc0'],['#b9b4ac','#5d5a58','#d5d0c6'],['#8f948c','#3f433f','#b4bab0'],['#7a8796','#2f3844','#a9b6c4']];
function bldg(x,b,w,ht,c,roof,win){g.fillStyle=c;g.fillRect(x,b-ht,w,ht+SH);if(roof){g.fillStyle=roof;g.beginPath();g.moveTo(x-3,b-ht);g.lineTo(x+w*.12,b-ht-w*.22);g.lineTo(x+w*.88,b-ht-w*.22);g.lineTo(x+w+3,b-ht);g.fill()}g.fillStyle=win;for(let a=9;a<w-14;a+=16)for(let q=14;q<ht-8;q+=24)g.fillRect(x+a,b-ht+q,8,13)}
function stp(u,N,SW,SD){const i=Math.floor(u),f=u-i,ef=f*f*(3-2*f),th=k=>Math.min(k,N)*SD,hm=th(i)+(th(i+2)-th(i))*ef,hs=th(i+1);return{ef,hm,hs,cx:(u+1)*SW,cy:-(hm+hs)/2,ev:i%2==0,mx:(i+.5+2*ef)*SW,tx:(i+1.5)*SW}}
function climb(){const m=SEL.m,SW=SH*.13,SD=SH*.06,N=S.N,s=SH*.0033,P=stp(Math.min(S.u,N),N,SW,SD),i=Math.floor(Math.min(S.u,N)),th=k=>Math.min(k,N)*SD;
const cx=P.cx,cy=P.cy,ox=W*.4,oy=SH*.7,X=wx=>wx-cx+ox,Y=wy=>wy-cy+oy,up=-cy,bx=cx;
const sky=[['#5f9fd8','#bfdcf0','#f4e6c8'],['#3a3f7a','#d98aa0','#f7c89c'],['#bcd0c0','#e6eedd','#f0f3e6'],['#050a1a','#16264d','#3a4f7c']][m];
g.fillStyle=lg(0,0,0,SH,sky);g.fillRect(0,0,W,H);
if(PH)cover(PH,0,0,W,SH);else{
if(m==3){for(let k=0;k<90;k++){g.fillStyle=`rgba(255,255,255,${.3+.5*Math.abs(Math.sin(S.tm*.8+k))})`;g.fillRect(h(k)*W,h(k+50)*SH*.7,1.6,1.6)}glow(W*.8,SH*.18,SH*.2,'rgba(220,230,255,.8)');g.fillStyle='#eef2ff';g.beginPath();g.arc(W*.8,SH*.18,SH*.035,0,7);g.fill()}
if(m!=2){const L=m==3?[[.06,'#0f1a33'],[.14,'#16233f']]:[[.08,'#c98d5a'],[.16,'#d8a673']];
if(m==1){glow(W*.3,SH*.7,SH*.7,'rgba(255,210,170,.7)');const ex=W*.68-bx*.05,eb=SH*.9+up*.03;g.fillStyle='#4a3a55';g.beginPath();g.moveTo(ex-40,eb);g.lineTo(ex-6,eb-SH*.5);g.lineTo(ex,eb-SH*.62);g.lineTo(ex+6,eb-SH*.5);g.lineTo(ex+40,eb);g.lineTo(ex+20,eb);g.lineTo(ex,eb-SH*.3);g.lineTo(ex-20,eb);g.fill()}
for(const [par,col] of (m==1?[[.12,'#d8c8ae'],[.2,'#e7d9c0']]:L)){const bs=SH*.95+up*par*.5;for(let k=Math.floor(bx*par/84)-1;k<(bx*par+W)/84+2;k++){const w=58+h(k+par*9)*40,ht=SH*(.22+h(k*3+par*7)*.4),x=k*84-bx*par,c=m==3?col:(m==0?['#c98d5a','#d8a673','#b87a4c','#e3b988'][k&3]:col);bldg(x,bs,w,ht,c,m==1?'#4a5568':null,m==3?(h(k*97)>.4?'rgba(255,214,140,.75)':'rgba(255,214,140,.15)'):'#5a3b28')}}}
else{glow(W*.4,SH*.6,SH*.8,'rgba(255,255,240,.8)');ridge(.04,bx,up*.05,SH*.8,SH*.3,['#9db5a4','#bccdb8','#e0e8d8'],2,SH);ridge(.1,bx,up*.09,SH*.9,SH*.22,['#6f8d78','#8aa591','#b8c8b8'],5,SH);g.fillStyle=lg(0,SH*.8,0,SH*1.2,['#2d4a37','#16281d']);g.fillRect(0,SH*.88+up*.14,W,SH*2);for(let k=Math.floor(bx*.2/36)-1;k<(bx*.2+W)/36+2;k++)pine(k*36-bx*.2,SH*.9+up*.14+8,SH*(.14+h(k)*.1),'#173223')}}
const st=STN[m];
for(let k=i-9;k<=i+14;k++){const top=Y(-th(k));if(m==2&&k%7==4&&k<N){const px=X((k+.5)*SW),gh=SH*.42;g.fillStyle='#c9371f';g.fillRect(px-SH*.2,top-gh,SH*.025,gh);g.fillRect(px+SH*.175,top-gh,SH*.025,gh);g.fillRect(px-SH*.26,top-gh,SH*.52,SH*.03);g.fillStyle='#222';g.fillRect(px-SH*.3,top-gh-SH*.03,SH*.6,SH*.03);g.fillRect(px-SH*.2,top-gh*.8,SH*.4,SH*.02)}}
for(let k=i-9;k<=i+14;k++){const x=X(k*SW),top=Y(-th(k));
g.fillStyle=lg(0,top,0,top+SD*6,[st[0],st[1]]);g.fillRect(x,top,SW+1,SH*2);g.fillStyle=st[2];g.fillRect(x,top,SW+1,Math.max(5,SD*.14));g.fillStyle='rgba(0,0,0,.22)';g.fillRect(x,top+SD*.14,SW,3);g.fillStyle='rgba(0,0,0,.3)';g.fillRect(x,top,3,SH*2);
if(k<N&&h(k*5)>.55){g.fillStyle=m==2?'rgba(80,115,66,.55)':'rgba(0,0,0,.07)';g.fillRect(x+4,top+4,SW*h(k+3)*.6,SD*.3)}
if(k<N&&k%6==3){const lx=x+SW*.5;if(m==0){g.fillStyle='#4f8a47';g.beginPath();g.arc(lx,top-SD*.4,SD*.55,0,7);g.fill();for(let d=0;d<6;d++){g.fillStyle='#e56a9c';g.fillRect(lx-SD*.5+h(k+d)*SD,top-SD*.8+h(k*3+d)*SD*.6,3,3)}}
else if(m!=2){g.strokeStyle=m==1?'#2b2b33':'#8e99a6';g.lineWidth=3;g.beginPath();g.moveTo(lx,top);g.lineTo(lx,top-SD*3);g.stroke();glow(lx,top-SD*3.1,SD*3.5,'rgba(255,214,150,.85)');g.fillStyle='#fff2cf';g.beginPath();g.arc(lx,top-SD*3.1,5,0,7);g.fill()}}}
if(m==1||m==3){g.strokeStyle=m==1?'#23232b':'rgba(190,205,220,.85)';g.lineWidth=3;g.beginPath();g.moveTo(X((i-9)*SW),Y(-th(i-9))-SD*3);for(let k=i-9;k<=i+14;k++){g.lineTo(X(k*SW),Y(-th(k))-SD*3);g.lineTo(X((k+1)*SW),Y(-th(k))-SD*3)}g.stroke()}
const fx=X((N+2)*SW),fy=Y(-N*SD);g.fillStyle='#ddd';g.fillRect(fx,fy-SH*.3,4,SH*.3);g.fillStyle=lg(fx,0,fx+60,0,['#d3232f','#8f1520']);g.beginPath();g.moveTo(fx+4,fy-SH*.3);g.lineTo(fx+66,fy-SH*.26+Math.sin(S.tm*2)*3);g.lineTo(fx+4,fy-SH*.18);g.fill();
const dp=(Q,jc,pc)=>{const M=[X(Q.mx),Y(-Q.hm)-SD*1.3*Math.sin(Math.PI*Q.ef)],T=[X(Q.tx),Y(-Q.hs)];g.fillStyle='rgba(0,0,0,.35)';g.beginPath();g.ellipse(M[0]+8,Y(-Q.hm)+2,16,4,0,0,7);g.fill();g.beginPath();g.ellipse(T[0]+8,Y(-Q.hs)+2,16,4,0,0,7);g.fill();
walker(X(Q.cx),Y(Q.cy)-38*s,s,Q.ev?M:T,Q.ev?T:M,Math.sin(Math.PI*Q.ef)*(Q.ev?1:-1),jc,pc)};
if(SEL.r)dp(stp(Math.min(S.uo,N),N,SW,SD),'#4aa3ff','#26324a');dp(P,COL[1][0],COL[1][1])}
/* ---------- loop ---------- */
let last=0;
function loop(ts){requestAnimationFrame(loop);if($('#game').hidden){last=ts;eng(0,0);return}const dt=Math.min((ts-last)/1000,.05);last=ts;S.tm+=dt;
if(S.timed&&S.t0&&!S.done&&(performance.now()-S.t0)/1000>=SEL.t){S.done=1;S.win=1}const n=S.timed?240:S.txt.length;S.p+=(S.i/n-S.p)*Math.min(1,dt*7);const tg=S.timed?Math.floor(S.i/4):Math.floor(S.i/n*S.N+1e-9);if(S.u<tg)S.u=Math.min(tg,S.u+2.6*dt);
if(SEL.r&&S.t0&&!S.shown){S.o+=OPP[SEL.d]*(SEL.md==2?.7+SEL.l*.06:1)*dt/n;const to=Math.floor(S.o*S.N+1e-9);if(S.uo<to)S.uo=Math.min(to,S.uo+2.6*dt);if(S.o>=1&&!S.done){S.o=1;S.done=1;S.win=0}}
eng(Math.max(0,1-(performance.now()-(S.lt||0))/700),(SEL.g==0||SEL.g==3)&&S.t0&&!S.done&&!S.shown);
if(SEL.g==1)climb();else race();
if(S.done&&!S.shown&&(S.timed||(SEL.g==1?(S.win?S.u>=S.N-.001:S.uo>=S.N-.001):(!S.win||S.p>.985))))show();
if(S.t0&&!S.shown){const s=(performance.now()-S.t0)/1000;$('#st').textContent=(S.timed?Math.max(0,SEL.t-s).toFixed(0):s.toFixed(1))+' چرکە';$('#sc').textContent='خال: '+Math.max(0,S.i*10-S.err*5);$('#wp').textContent=Math.round(S.i/5/(s/60))+' ووشە/خولەک';$('#ac').textContent=Math.round(100*(S.keys-S.err)/S.keys)+'%'}
const bf=S.timed?(S.t0?Math.min(1,(performance.now()-S.t0)/1000/SEL.t):0):(SEL.g==1?S.u/S.N:S.p);$('#b1').style.width=Math.min(100,bf*100)+'%';$('#b2').style.width=S.o*100+'%'}
requestAnimationFrame(loop);
</script></body></html>
