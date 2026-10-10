<!doctype html>
<html lang="en"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>GD Arena — Hinglish Placement Coach</title>
<style>
:root{--bg:#f5f6fb;--fg:#151823;--card:#fff;--mut:#586074;--ac:#4f46e5;--acf:#fff;--ac2:#e5e7ff;--bd:#e1e4ee;--ok:#15803d;--er:#b91c1c;--wn:#b45309;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0e1017;--fg:#eceef6;--card:#171a24;--mut:#9aa3b8;--ac:#818cf8;--acf:#10121a;--ac2:#252a4a;--bd:#2a2f40;--ok:#4ade80;--er:#f87171;--wn:#fbbf24}}
:root[data-theme="dark"]{--bg:#0e1017;--fg:#eceef6;--card:#171a24;--mut:#9aa3b8;--ac:#818cf8;--acf:#10121a;--ac2:#252a4a;--bd:#2a2f40;--ok:#4ade80;--er:#f87171;--wn:#fbbf24}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*,*:before,*:after{box-sizing:inherit}
body{margin:0;background:var(--bg);color:var(--fg);font:16px/1.55 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
main{max-width:1060px;margin:0 auto;padding:16px}
h1,h2,h3{line-height:1.2;margin:.2em 0 .5em}
.card{background:var(--card);border:1px solid var(--bd);border-radius:14px;padding:18px;margin-bottom:14px}
.hero{padding:34px 22px;text-align:center;background:linear-gradient(135deg,var(--ac2),var(--card))}
.hero h1{font-size:clamp(1.9rem,5vw,3rem)}
.sm{font-size:.86rem;color:var(--mut)}
button{font:inherit;font-weight:600;border:0;border-radius:10px;padding:10px 16px;background:var(--ac);color:var(--acf);cursor:pointer}
button.sec{background:var(--ac2);color:var(--fg)}button.danger{background:var(--er);color:#fff}
button:disabled{opacity:.45;cursor:not-allowed}
button.big{font-size:1.15rem;padding:14px 28px}
:focus-visible{outline:3px solid var(--ac);outline-offset:2px}
input[type=text],textarea,select{width:100%;font:inherit;padding:9px 11px;border-radius:10px;border:1px solid var(--bd);background:var(--bg);color:var(--fg)}
fieldset{border:1px solid var(--bd);border-radius:12px;margin:0 0 14px;padding:12px}
legend{font-weight:700;padding:0 6px}
.opt{display:flex;gap:9px;align-items:flex-start;padding:5px 2px}
.opt input{margin-top:5px}
.grid{display:grid;gap:12px;grid-template-columns:repeat(auto-fit,minmax(210px,1fr))}
.chip{display:inline-block;background:var(--ac2);border-radius:99px;padding:4px 12px;font-weight:600;font-size:.9rem}
.badge{display:inline-block;border-radius:6px;padding:1px 8px;font-size:.78rem;font-weight:700}
.badge.d{background:#fde68a;color:#78350f}
.err{background:color-mix(in srgb,var(--er) 14%,transparent);border:1px solid var(--er);padding:9px 12px;border-radius:10px;margin:8px 0}
.note{background:var(--ac2);padding:10px 14px;border-radius:10px}
.rh{display:flex;justify-content:space-between;gap:14px;align-items:center;flex-wrap:wrap}
.tm{min-width:150px;text-align:right}.tm span{font:700 1.8rem ui-monospace,monospace}
.bar{height:6px;border-radius:9px;background:var(--bd);overflow:hidden}.bar i{display:block;height:100%;width:100%;background:var(--ac)}
.pg{display:flex;gap:10px;overflow-x:auto;padding:2px 2px 12px}
.av{flex:0 0 132px;text-align:center;background:var(--card);border:2px solid var(--bd);border-radius:14px;padding:10px 6px;display:flex;flex-direction:column;gap:2px;align-items:center}
.av.on{border-color:var(--ok);box-shadow:0 0 0 4px color-mix(in srgb,var(--ok) 25%,transparent)}
.ac{width:52px;height:52px;border-radius:50%;color:#fff;font:700 1.4rem/52px system-ui;text-align:center}
.sp{min-height:1.2em;font-size:.8rem;color:var(--ok);font-weight:700}
.cols{display:grid;gap:14px;grid-template-columns:1.3fr 1fr}
@media(max-width:800px){.cols{grid-template-columns:1fr}}
.tr{max-height:52vh;min-height:200px;overflow-y:auto}
.tn{padding:7px 10px;border-radius:10px;margin-bottom:7px;background:var(--bg)}
.tn.me{background:var(--ac2)}.tn b{font-size:.88rem}.tn .sm{margin-left:6px}
.tn.int{opacity:.65;font-style:italic}
.btns{display:flex;flex-wrap:wrap;gap:8px;margin-top:10px}
blockquote{margin:6px 0;padding:6px 12px;border-left:4px solid var(--ac);background:var(--bg);border-radius:0 8px 8px 0}
table{width:100%;border-collapse:collapse}th,td{text-align:left;padding:7px 8px;border-bottom:1px solid var(--bd)}
.pill{border-radius:99px;padding:2px 10px;font-size:.78rem;font-weight:700;color:#fff}
.Strength{background:var(--ok)}.Needs{background:var(--wn)}.Ins{background:#64748b}
.top{display:flex;justify-content:space-between;align-items:center;gap:8px}
.logo{font-weight:800;font-size:1.1rem}
ul{padding-left:20px}
</style></head>
<body>
<main id="app"></main>
<script>
const $=s=>document.querySelector(s),app=$('#app');
const esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const sleep=ms=>new Promise(r=>setTimeout(r,ms));
const wc=t=>t.trim()?t.trim().split(/\s+/).length:0;
const TOPICS=["Should AI replace some human jobs?","Social media: benefits and risks","Online education versus classroom education","Should college attendance be mandatory?","Is work experience more important than academic marks?","Climate change and individual responsibility","Technology in everyday life"];
const PS=[
{id:'assertive',name:'Arjun',label:'Dominating Speaker',d:'Speaks quickly and often, keeps contributing',color:'#dc2626',pitch:.8,rate:1.08},
{id:'data',name:'Meera',label:'Data-Driven Speaker',d:'Evidence, examples, careful logic',color:'#0284c7',pitch:1.2,rate:.97},
{id:'quiet',name:'Kabir',label:'Quiet Contributor',d:'Speaks less, short thoughtful points',color:'#059669',pitch:1,rate:.9},
{id:'challenger',name:'Zoya',label:'Respectful Challenger',d:'Questions assumptions, counterarguments',color:'#d97706',pitch:1.3,rate:1.03},
{id:'distract',name:'Rohan',label:'Distractible Speaker',d:'Drifts off-topic, can be redirected',color:'#7c3aed',pitch:.95,rate:1.14}];
const MOD={id:'mod',name:'Moderator',label:'Moderator',color:'#334155',pitch:1,rate:.95},ME={id:'me',name:'You',label:'Student',color:'#4f46e5'};
const L={en:{
assertive:["I'll be direct: on this topic, the benefits clearly outweigh the downsides if we plan properly.","Let me push back a little. We can't treat this as optional, because it already shapes real decisions.","Here's my stand: waiting is the riskiest option, so we need action now."],
data:["Let's separate claims from evidence. We'd want comparisons across groups, not just anecdotes.","A concrete example helps: look at how one college or company handled this, then check if it generalises. I won't quote numbers I can't verify.","Logically, correlation isn't causation here. We should define what success looks like first."],
quiet:["Just one thought: the people affected most are often the ones we forget to ask.","Briefly, balance matters more than extremes.","I'd add that skills and attitude matter as much as the system itself."],
challenger:["Respectfully, are we assuming too much? Does this work the same way for everyone?","That's fair, but what's the counterargument? Who might lose out?","I'd question that premise. What would change your mind?"],
distract:["Sorry, slightly random, but this reminds me of my cousin's startup. Anyway, I think change is inevitable.","Oh, like how phones changed exams? Okay, back to the topic: students adapt quickly.","Wait, did anyone watch that match last night? Right, sorry. I think it depends on the context."]},
hi:{
assertive:["Seedhi baat: is topic par fayde nuksaan se zyada hain, bas sahi planning chahiye.","Main thoda disagree karunga. Isko optional maan lena ab possible nahi hai.","Mera stand clear hai: ruk jaana sabse risky option hai."],
data:["Claims aur evidence alag rakhte hain. Sirf kisse nahi, comparison chahiye.","Ek example lo: ek college ya company ne ise kaise handle kiya, phir dekho sab par lagu hota hai ya nahi. Main wo numbers nahi bolunga jo verify nahi hain.","Correlation aur causation same nahi hain. Pehle define karo ki success kya hai."],
quiet:["Bas ek baat: jo log sabse zyada affect hote hain, unse hum kam poochte hain.","Chhota sa point: balance extreme se behtar hai.","Skills aur attitude bhi system jitne hi zaroori hain."],
challenger:["Respectfully, kya hum zyada assume kar rahe hain? Kya ye sab par ek jaise kaam karta hai?","Theek hai, par counterargument kya hai? Kiska nuksaan ho sakta hai?","Main is premise par sawal uthaunga. Aapko kaunsi baat mana sakti hai?"],
distract:["Sorry, thoda random, par mere cousin ka startup yaad aa gaya. Khair, change inevitable hai.","Arre jaise phones ne exams badal diye? Okay, wapas topic par: students jaldi adapt karte hain.","Wait, kal ka match kisne dekha? Sorry, mujhe lagta hai context par depend karta hai."]}};
const CL={en:["To close: this needs balance, evidence and empathy.","My closing view: act thoughtfully and keep listening to each other.","Finally, I'd say clear goals matter more than the tools we choose."],hi:["Closing mein: balance, evidence aur empathy teeno zaroori hain.","Mera closing view: soch samajhkar kaam karo aur ek doosre ko suno.","Aakhir mein, clear goals tools se zyada zaroori hain."]};
const ML={en:{welcome:t=>`Welcome! I'm your moderator. Everyone else on this panel is an AI participant. Today's topic: ${t}.`,rules:d=>`Rules: one speaker at a time, stay on topic, be respectful. Use the microphone or type your turn. We have ${d} minutes.`,open:t=>`Let's begin. Please share your opening view.`,redirect:()=>"Let's bring this back to the topic.",final:()=>"We're moving to the final round. Each participant, please give a brief closing statement.",conclude:()=>"Thank you all. That concludes the group discussion. Preparing your report now."},
hi:{welcome:t=>`Welcome! Main aapka moderator hoon. Panel ke baaki sabhi participants AI hain. Aaj ka topic: ${t}.`,rules:d=>`Rules: ek time par ek speaker, topic par raho, respect rakho. Mic use karo ya type karo. Humare paas ${d} minute hain.`,open:t=>`Chaliye shuru karte hain. Apna opening view share kijiye.`,redirect:()=>"Chaliye, wapas topic par aate hain.",final:()=>"Ab final round. Har participant ek chhota closing statement dein.",conclude:()=>"Dhanyavaad. GD yahan khatam hoti hai. Aapki report taiyaar ho rahi hai."}};
const SR=window.SpeechRecognition||window.webkitSpeechRecognition;
const S={view:'landing',st:'SETUP',cfg:{topic:TOPICS[0],custom:'',useCustom:false,panel:['assertive','data','challenger'],dur:3,lang:'en',pause:2.5,wait:1,vi:false},turns:[],tok:0,used:{},rr:0,buf:'',interim:'',mic:SR?'idle':'unavailable',micWanted:!!SR,err:'',failed:null,speaker:null,speaking:false,act:0,vcache:[]};
const ml=(k,...a)=>ML[S.cfg.lang][k](...a);

/* storage */
function ld(){try{return JSON.parse(localStorage.getItem('gd.s')||'[]')}catch(e){console.warn(e);return[]}}
function sv(a){try{localStorage.setItem('gd.s',JSON.stringify(a));return true}catch(e){console.warn(e);return false}}

/* speech output */
function voices(){try{return(speechSynthesis.getVoices()||[]).filter(v=>/^(en|hi)/i.test(v.lang))}catch(e){return[]}}
function voiceFor(p){const v=voices();if(v.length<2)return null;const order=[MOD,...(S.panelP||[])];return v[Math.max(0,order.findIndex(o=>o.id===p.id))%v.length]}
function cancelSpeech(){try{window.speechSynthesis&&speechSynthesis.cancel()}catch(e){console.warn(e)}}
function speak(p,text){return new Promise(res=>{
 if(S.muted||!('speechSynthesis' in window)){setTimeout(res,Math.min(5000,400+text.length*28));return}
 const u=new SpeechSynthesisUtterance(text),v=voiceFor(p);if(v)u.voice=v;u.lang=v?v.lang:'en-IN';u.pitch=p.pitch;u.rate=p.rate;
 let done=false;const f=()=>{if(!done){done=true;res()}};
 u.onend=f;u.onerror=e=>{if(e.error!=='interrupted'&&e.error!=='canceled')setErr('Speech output failed ('+e.error+'). The text is still shown.');f()};
 setTimeout(f,text.length*95+4000);
 try{speechSynthesis.speak(u)}catch(e){setErr('Speech output is unavailable: '+e.message);f()}})}

/* speech input */
function stopRec(){clearTimeout(S.sil);const r=S.rec;S.rec=null;if(r){r.onend=null;r.onresult=null;try{r.abort()}catch(e){console.warn(e)}}if(S.mic==='listening')S.mic='idle'}
function startRec(){
 if(!SR){S.mic='unavailable';upd();return}
 if(S.rec||(S.st!=='LISTENING'&&!(S.st==='AI_SPEAKING'&&S.cfg.vi))||!S.micWanted)return;
 const r=new SR();r.lang='en-IN';r.continuous=true;r.interimResults=true;
 r.onstart=()=>{S.mic='listening';upd()};
 r.onresult=e=>{if(S.st==='AI_SPEAKING'&&S.cfg.vi)interrupt();let it='';for(let i=e.resultIndex;i<e.results.length;i++){const R=e.results[i];if(R.isFinal){const t=R[0].transcript.trim();if(t&&!S.buf.endsWith(t))S.buf=(S.buf+' '+t).trim()}else it+=R[0].transcript}
  S.interim=it;S.act=Date.now();clearTimeout(S.sil);S.sil=setTimeout(()=>{if(S.buf&&S.st==='LISTENING')submit()},S.cfg.pause*1000);upd()};
 r.onerror=e=>{if(e.error==='not-allowed'||e.error==='service-not-allowed'){S.micWanted=false;S.mic='unavailable';setErr("Microphone access was denied. Allow it in your browser's site settings and press Start mic, or type your turn below.")}
  else if(e.error==='no-speech'||e.error==='aborted'){S.mic='idle'}
  else{S.micWanted=false;S.mic='idle';setErr('Speech recognition failed ('+e.error+'). Press Start mic to retry, or type your turn.')}upd()};
 r.onend=()=>{S.rec=null;if(S.mic==='listening')S.mic='idle';if(S.micWanted&&(S.st==='LISTENING'||(S.st==='AI_SPEAKING'&&S.cfg.vi)))setTimeout(startRec,250);upd()};
 S.rec=r;try{r.start()}catch(e){S.rec=null;setErr('Could not start the microphone: '+e.message)}}

/* transcript */
function addTurn(p,text,extra){
 text=text.replace(/\s+/g,' ').trim();if(!text)return null;
 const last=S.turns[S.turns.length-1];if(last&&last.id===p.id&&last.text===text)return null;
 const t={n:S.turns.length+1,id:p.id,name:p.name,role:p.label,text,ts:Date.now(),phase:S.phase,...extra};S.turns.push(t);return t}

/* demo AI engine (scripted — NOT live AI) */
const withTimeout=(pr,ms)=>Promise.race([pr,new Promise((_,j)=>setTimeout(()=>j(new Error('timed out')),ms))]);
async function gen(p,kind,first){
 await sleep(450+Math.random()*500);const lg=S.cfg.lang;
 const u=S.used[p.id]||(S.used[p.id]=new Set());let ix=[0,1,2].filter(i=>!u.has(i));if(!ix.length){u.clear();ix=[0,1,2]}
 const k=ix[Math.floor(Math.random()*ix.length)];u.add(k);
 if(kind==='close')return CL[lg][(k+PS.indexOf(p))%3];
 let line=L[lg][p.id][k],pre='';
 const mine=[...S.turns].reverse().find(t=>t.id==='me'),prev=[...S.turns].reverse().find(t=>t.id!=='me'&&t.id!=='mod'&&t.id!==p.id&&!t.interrupted);
 if(first&&mine&&Math.random()<.6)pre=(lg==='hi'?'Aapne kaha tha "':'You said "')+mine.text.split(' ').slice(0,7).join(' ')+(lg==='hi'?'..." — ':'..." — ');
 else if(prev&&Math.random()<.85)pre=prev.name+(p.id==='challenger'?(lg==='hi'?', respectfully main isse agree nahi hoon: ':', respectfully, I see it differently: '):lg==='hi'?', isi baat ko aage badhaun toh: ':', building on that: ');
 return pre+line}
const kws=()=>S.topic.toLowerCase().split(/[^a-z]+/).filter(w=>w.length>3&&!['should','that','with','what','more','than','versus','some'].includes(w));
const hits=t=>kws().filter(k=>t.toLowerCase().includes(k)).length;

/* run a queue of spoken turns, sequentially, cancellable */
async function run(items,tok,mode){
 for(let i=0;i<items.length;i++){
  if(tok!==S.tok)return false;const it=items[i];let text=it.text;
  if(!text){if(mode==='reply'){S.st='PROCESSING';S.speaker=null;upd()}
   for(let a=0;a<2&&!text;a++){try{text=await withTimeout(gen(it.p,it.kind,i===0),8000)}catch(e){if(a===1){
     if(tok!==S.tok)return false;
     if(mode==='close')break;
     S.failed={items:items.slice(i)};S.st='LISTENING';S.speaker=null;setErr('The AI response failed ('+e.message+'). Your transcript is safe. Retry, keep speaking, or end the discussion.');startRec();return false}}}
   if(!text)continue}
  if(tok!==S.tok)return false;
  S.st=mode==='reply'?'AI_SPEAKING':mode==='close'?'CLOSING':'OPENING';S.speaker=it.p.id;S.speaking=true;
  addTurn(it.p,text);upd();
  if(S.cfg.vi)startRec();
  await speak(it.p,text);S.speaking=false;
  if(tok!==S.tok)return false;S.speaker=null}
 return true}
async function reply(){
 const tok=++S.tok,me=S.turns[S.turns.length-1],P=S.panelP,items=[];
 await sleep(S.cfg.wait*1000);if(tok!==S.tok)return;
 if(wc(me.text)>=5&&!hits(me.text))items.push({p:MOD,text:ml('redirect')});
 const n=P.length>3&&Math.random()<.5?3:2,pick=[],dom=P.find(p=>p.id==='assertive');if(dom)pick.push(dom);
 while(pick.length<n){const p=P[S.rr++%P.length];if(p.id==='quiet'&&S.rr%2)continue;if(!pick.includes(p))pick.push(p)}
 pick.forEach(p=>{items.push({p,kind:'reply'});if(p.id==='distract'&&Math.random()<.5)items.push({p:MOD,text:ml('redirect')})});if(dom&&Math.random()<.5)items.push({p:dom,kind:'reply'});
 await afterRun(items,tok)}
async function afterRun(items,tok){
 const ok=await run(items,tok,'reply');
 if(ok&&tok===S.tok&&S.st!=='CLOSING'&&S.st!=='COMPLETED'){S.st='LISTENING';S.speaker=null;S.act=Date.now();upd();startRec()}}

/* flow */
function submit(){
 if(S.st!=='LISTENING')return;
 const t=(S.buf+' '+($('#ti')?$('#ti').value:'')).replace(/\s+/g,' ').trim();
 if(!t){setErr('Nothing to submit yet. Speak or type something first.');return}
 clearErr();stopRec();S.buf='';S.interim='';$('#ti').value='';
 const turn=addTurn(ME,t);S.st='PROCESSING';upd();if(turn)reply()}
function interrupt(){
 if(S.st!=='AI_SPEAKING'&&S.st!=='PROCESSING')return;
 S.tok++;cancelSpeech();const last=S.turns[S.turns.length-1];
 if(S.speaking&&last&&last.id!=='me')last.interrupted=true;
 S.speaking=false;S.speaker=null;S.st='LISTENING';S.act=Date.now();upd();startRec()}
async function startGD(){
 S.view='room';S.st='OPENING';S.phase='OPENING';S.turns=[];S.used={};S.rr=0;S.endAt=null;S.warned=false;S.buf='';S.interim='';S.err='';S.failed=null;S.started=Date.now();
 render();const tok=++S.tok;
 const ok=await run([{p:MOD,text:ml('welcome',S.topic)},{p:MOD,text:ml('rules',S.cfg.dur)},{p:MOD,text:ml('open',S.topic)}],tok,'open');
 if(!ok||tok!==S.tok)return;
 S.phase='DISCUSSION';S.st='LISTENING';S.endAt=Date.now()+S.cfg.dur*60000;S.act=Date.now();S.openAt=Date.now()+15000;upd();startRec()}
async function beginClosing(){
 if(S.st==='CLOSING'||S.st==='COMPLETED'||S.st==='OPENING')return;
 const tok=++S.tok;stopRec();cancelSpeech();
 const last=S.turns[S.turns.length-1];if(S.speaking&&last&&last.id!=='me')last.interrupted=true;
 S.speaking=false;S.speaker=null;S.st='CLOSING';S.phase='CLOSING';S.failed=null;clearErr();upd();
 const ok=await run([{p:MOD,text:ml('final')},...S.panelP.map(p=>({p,kind:'close'})),{p:MOD,text:ml('conclude')}],tok,'close');
 if(tok!==S.tok)return;complete()}
function complete(){
 S.st='COMPLETED';S.speaker=null;S.ended=Date.now();S.rep=buildReport();
 const all=ld();all.unshift({id:S.rep.id,rep:S.rep,turns:S.turns});S.rep.saved=sv(all.slice(0,10));
 S.view='report';render()}
function setErr(m){S.err=m;upd()}function clearErr(){S.err='';S.failed=null}
function aiStarts(){const P=S.panelP,p=P.find(x=>x.id==='assertive')||P[0];stopRec();S.st='PROCESSING';upd();afterRun([{p,kind:'reply'}],++S.tok)}
function modNote(){const tok=++S.tok;stopRec();const s=Math.round(Math.max(30000,S.cfg.dur*15000)/1000);afterRun([{p:MOD,text:S.cfg.lang==='hi'?`Time check: lagbhag ${s} second bache hain. Apne final points wrap up kijiye, phir closing round hoga.`:`Time check: about ${s} seconds left. Please wrap up your key points; the closing round comes next.`}],tok)}

/* report */
function buildReport(){
 const T=S.turns,tot=T.filter(t=>!t.interrupted),all=tot.reduce((a,t)=>a+wc(t.text),0),sp={};
 [MOD,...S.panelP,ME].forEach(p=>sp[p.id]={name:p.name,role:p.label,turns:0,words:0});
 tot.forEach(t=>{if(sp[t.id]){sp[t.id].turns++;sp[t.id].words+=wc(t.text)}});
 const stats=Object.values(sp).map(s=>({...s,share:all?Math.round(1000*s.words/all)/10:0,estSec:Math.round(s.words/2.5)}));
 const fb=feedback().map(o=>{const tn=o.turn&&T.find(t=>t.n===o.turn);
  if(o.quote&&!(tn&&tn.text.includes(o.quote)))return{...o,rating:'Insufficient evidence',quote:'',turn:null,expl:'The supporting quotation could not be verified against the transcript, so no judgement is made.'};return o});
 return{id:'s'+Date.now(),topic:S.topic,dur:S.cfg.dur,lang:S.cfg.lang,elapsed:Math.round((S.ended-S.started)/1000),panel:S.panelP.length,stats,fb,all,date:new Date().toLocaleString(),
  meTurns:T.filter(t=>t.id==='me').length,meWords:sp.me.words}}
const sents=t=>t.split(/(?<=[.!?])\s+/).map(s=>s.trim()).filter(Boolean);
const cut=s=>s.slice(0,160);
function feedback(){
 const T=S.turns,me=T.filter(t=>t.id==='me'),mw=me.reduce((a,t)=>a+wc(t.text),0),out=[];
 const add=(cat,rating,expl,turn,quote,sug)=>out.push({cat,rating,expl,turn:turn?turn.n:null,quote:quote||'',sug});
 const ins=(cat,why)=>add(cat,'Insufficient evidence',why,null,'','Speak at least 2–3 turns of 2–3 sentences each so this can be assessed.');
 const cats=["Starting the discussion (discussion start karne ki ability)","Quality and relevance of ideas","Logical reasoning and examples","Building on other participants' points","Listening and responding appropriately","Handling interruptions","Staying on topic","Ending with a clear conclusion"];
 if(!me.length){cats.forEach(c=>ins(c,'You did not speak during this session, so there is nothing to assess.'));return out}
 const longest=t=>sents(t.text).sort((a,b)=>b.length-a.length)[0];
 const first=me[0],before=T.filter(t=>t.n<first.n&&t.id!=='mod').length;
 add(cats[0],before===0?'Strength':'Needs work',`Your first turn was #${first.n}, after ${before} turn(s) by AI participants (the moderator is not counted).`,first,cut(sents(first.text)[0]),before?'Try to give the first substantive view right after the moderator opens, with a one-line position.':'Keep leading with a clear one-line position.');
 const few=c=>ins(c,`Only ${mw} word(s) were spoken in total, which is not enough to judge this fairly.`);
 if(mw<15)cats.slice(1).forEach(few);
 else{
  const best=[...me].sort((a,b)=>hits(b.text)-hits(a.text))[0];
  hits(best.text)?add(cats[1],'Strength','At least one turn used key words from the topic, suggesting relevant ideas.',best,cut(sents(best.text).find(s=>hits(s))||sents(best.text)[0]),'Add one more distinct idea per turn rather than repeating the same one.')
   :add(cats[1],'Needs work','No key words from the topic appeared in your turns, so relevance is unclear.',best,cut(longest(best)),'Name the topic or its key terms explicitly in your first sentence.');
  const R=/\b(because|for example|for instance|such as|e\.g\.|therefore|since|isliye|kyunki|jaise|udaharan)\b/i;
  const rt=me.find(t=>R.test(t.text));
  rt?add(cats[2],'Strength','You gave a reason or example.',rt,cut(sents(rt.text).find(s=>R.test(s))||sents(rt.text)[0]),'Follow each claim with one concrete example from college, work or daily life.')
   :add(cats[2],'Needs work','No reasoning words or examples were detected in your turns.',me[0],cut(longest(me[0])),'Use the pattern: claim, because, for example.');
  const names=S.panelP.map(p=>p.name).join('|'),B=new RegExp('\\b('+names+'|you said|you mentioned|agree|disagree|aapne|sahi kaha)\\b','i');
  const bt=me.find(t=>B.test(t.text));
  bt?add(cats[3],'Strength','You referred to or reacted to another speaker.',bt,cut(sents(bt.text).find(s=>B.test(s))||sents(bt.text)[0]),'Name the speaker, then agree, extend or counter their point.')
   :add(cats[3],'Needs work','No explicit reference to another speaker was detected.',me[me.length-1],cut(sents(me[me.length-1].text)[0]),'Try: "Building on Meera\'s point about evidence, I would add…"');
  let lt=null,lp=null;
  me.forEach(t=>{if(lt)return;const p=[...T].reverse().find(x=>x.n<t.n&&x.id!=='me'&&x.id!=='mod'&&!x.interrupted);
   if(p){const w=new Set(p.text.toLowerCase().match(/[a-z]{5,}/g)||[]);if((t.text.toLowerCase().match(/[a-z]{5,}/g)||[]).filter(x=>w.has(x)).length>=2){lt=t;lp=p}}});
  const anyAI=me.some(t=>T.some(x=>x.n<t.n&&x.id!=='me'&&x.id!=='mod'));
  lt?add(cats[4],'Strength',`Your turn #${lt.n} shared several words with ${lp.name}'s previous point, suggesting you responded to it.`,lt,cut(sents(lt.text)[0]),'Keep paraphrasing the previous speaker before adding your view.')
   :anyAI?add(cats[4],'Needs work','Your turns shared little wording with the AI speaker just before you.',me[me.length-1],cut(sents(me[me.length-1].text)[0]),'Open with a one-line paraphrase of what the last speaker said.')
   :ins(cats[4],'No AI participant had spoken before your turns.');
  const ii=T.findIndex(t=>t.interrupted),nx=ii>=0?T.slice(ii+1).find(t=>t.id==='me'):null;
  nx?add(cats[5],hits(nx.text)?'Strength':'Needs work',`You interrupted ${T[ii].name} (turn #${T[ii].n}) and continued in turn #${nx.n}.`,nx,cut(sents(nx.text)[0]),'After taking the floor, acknowledge the interrupted point briefly, then make yours.')
   :ins(cats[5],'No AI speaker was interrupted in this session.');
  const on=me.filter(t=>hits(t.text)).length,ratio=on/me.length,ot=ratio>=.5?me.find(t=>hits(t.text)):me.find(t=>!hits(t.text));
  add(cats[6],ratio>=.5?'Strength':'Needs work',`${on} of ${me.length} of your turns used key topic words.`,ot,cut(sents(ot.text)[0]),'Tie each point back to the topic in one phrase.');
  const lm=me[me.length-1],C=/\b(in conclusion|to sum|overall|finally|to conclude|in short|ant mein|toh nishkarsh)\b/i,cs=sents(lm.text);
  C.test(lm.text)?add(cats[7],'Strength','Your last turn contained a concluding phrase.',lm,cut(cs.find(s=>C.test(s))||cs[cs.length-1]),'Keep your conclusion to two sentences: position plus reason.')
   :add(cats[7],'Needs work','Your last turn had no clear concluding signal.',lm,cut(cs[cs.length-1]),'Finish with "In conclusion, I believe… because…".')}
 return out}

/* views */
function go(v){S.view=v;render();window.scrollTo(0,0)}
function vLanding(){const h=ld();return `<div class="top"><span class="logo">🎙️ GD Arena</span><button class="sec" id="th" aria-label="Toggle theme">Theme</button></div>
<section class="card hero"><h1>GD Arena — Hinglish Placement Coach</h1><p>Practise group discussions out loud with 3–5 AI participants and a moderator, then get a transcript-linked report.</p><p>Campus placement GD ki practice: mic se bolo, AI participants ko suno, aur specific feedback pao.</p>
<button class="big" data-go="setup">Start a GD</button><p class="sm">Best in desktop Chrome or Edge (microphone). Other browsers can use the typing fallback.</p></section>
<section class="card"><h2>How it works</h2><div class="grid"><div><b>1. Create GD room</b><br>Topic chuno (ya apna custom topic), 3–5 AI participants aur moderator set karo.</div><div><b>2. Mic se bolo</b><br>Speech live text mein badalti hai (live captions). Mic na chale to type karo.</div><div><b>3. AI participants discuss karte hain</b><br>Wo aap par aur ek-doosre par respond karte hain, awaaz mein, ek time par ek. Aap kabhi bhi interrupt kar sakte ho.</div><div><b>4. Report</b><br>Kisne kitna bola, start karna, ideas, building on others, conclusion. Har point transcript ke exact quote se linked.</div></div></section>
<section class="card"><h2>Topics</h2><ul>${TOPICS.map(t=>`<li>${esc(t)}</li>`).join('')}<li>Or enter your own custom topic</li></ul></section>
<section class="card note"><b>All other speakers are AI (aapke alawa sab participants aur moderator AI hain).</b> Every participant and the moderator are AI personas. This build runs in <span class="badge d">DEMO MODE</span>: replies are clearly scripted, not live generative AI.</section>
<section class="card"><h2>Privacy</h2><p class="sm">Your microphone is used only while listening, through your browser's speech recognition (the browser vendor's service may process audio). No audio is recorded or stored by this app. Transcripts and reports are saved only in this browser and you can delete them any time.</p></section>
${h.length?`<section class="card"><h2>Previous sessions</h2>${h.map(x=>`<div class="top" style="border-bottom:1px solid var(--bd);padding:8px 0"><span>${esc(x.rep.topic)}<br><span class="sm">${esc(x.rep.date)} · ${x.rep.meWords} words spoken</span></span><span><button class="sec" data-open="${x.id}">Open</button> <button class="danger" data-del="${x.id}" aria-label="Delete session">Delete</button></span></div>`).join('')}</section>`:''}`}
function vSetup(){const c=S.cfg;return `<div class="top"><span class="logo">🎙️ GD Arena</span><button class="sec" data-go="landing">← Home</button></div><section class="card"><h2>Set up your GD</h2>
<fieldset><legend>Topic</legend>${TOPICS.map((t,i)=>`<label class="opt"><input type="radio" name="tp" value="${i}" ${!c.useCustom&&c.topic===t?'checked':''}>${esc(t)}</label>`).join('')}
<label class="opt"><input type="radio" name="tp" value="c" ${c.useCustom?'checked':''}>Custom topic</label>
<input type="text" id="ct" maxlength="200" aria-label="Custom topic" placeholder="Type your own topic (5–120 characters)" value="${esc(c.custom)}"></fieldset>
<fieldset><legend>AI participants (choose 3–5; the moderator is extra)</legend>${PS.map(p=>`<label class="opt"><input type="checkbox" name="pp" value="${p.id}" ${c.panel.includes(p.id)?'checked':''}><span><b>${p.name}</b> · ${p.label}<br><span class="sm">${p.d}</span></span></label>`).join('')}</fieldset>
<div class="grid"><label>Duration<select id="du">${[1,2,3,5,8].map(d=>`<option value="${d}" ${c.dur===d?'selected':''}>${d} min</option>`).join('')}</select></label>
<label>Language<select id="lg"><option value="en" ${c.lang==='en'?'selected':''}>English</option><option value="hi" ${c.lang==='hi'?'selected':''}>Hinglish</option></select></label>
<label>Pause before auto-submit<select id="pa">${[1.5,2.5,4].map(d=>`<option value="${d}" ${c.pause===d?'selected':''}>${d}s of silence</option>`).join('')}</select></label>
<label>AI waits before replying<select id="wa">${[0.5,1,2.5].map(d=>`<option value="${d}" ${c.wait===d?'selected':''}>${d}s</option>`).join('')}</select></label></div>
<label class="opt"><input type="checkbox" id="vi" ${c.vi?'checked':''}>Interrupt the AI by speaking (use headphones, otherwise the AI's own voice can trigger it). The Interrupt button always works.</label>
<p class="sm"><b>Browser check:</b> ${SR?'✅ Speech recognition supported (microphone permission is requested when the GD starts).':'⚠️ Speech recognition is not supported here. You can still take part by typing.'} ${'speechSynthesis' in window?'✅ Speech output supported.':'⚠️ Speech output unsupported; replies show as text only.'}</p>
<div id="er" class="err" role="alert" hidden></div><div class="btns"><button id="rv">Review &amp; continue</button></div></section>`}
function vConfirm(){const c=S.cfg,v=voices().length;return `<section class="card"><h2>Confirm your GD</h2><ul><li><b>Topic:</b> ${esc(S.topic)}</li><li><b>Duration:</b> ${c.dur} min</li><li><b>AI participants:</b> ${S.panelP.map(p=>p.name+' ('+p.label+')').join(', ')} + Moderator</li><li><b>Language:</b> ${c.lang==='hi'?'Hinglish':'English'}</li></ul>
<p class="note"><b>Everyone except you is AI.</b> DEMO MODE: replies are scripted, not live AI.</p>
<p class="sm">${v>=2?`${v} usable browser voices found; participants get different voices.`:v===1?'Only one voice is available, so participants differ by speech rate and pitch only.':'No speech voices detected; replies will be shown as text.'}</p>
<div class="btns"><button class="sec" data-go="setup">← Back to setup</button><button class="big" id="go">Start discussion</button></div></section>`}
function vRoom(){return `<header class="rh card"><div><b>${esc(S.topic)}</b><div class="sm">${S.cfg.lang==='hi'?'Hinglish':'English'} · <span class="badge d">DEMO MODE: scripted replies, not live AI</span> · All other speakers are AI</div></div><div class="tm"><span id="tm">${fmt(S.cfg.dur*60000)}</span><div class="bar"><i id="pb"></i></div></div></header>
<div class="pg">${[MOD,...S.panelP,ME].map(p=>`<div class="av" id="av-${p.id}"><div class="ac" style="background:${p.color}">${p.name[0]}</div><b>${p.name}</b><span class="sm">${p.id==='me'?'You (student)':p.id==='mod'?'Moderator (AI)':p.label+' · AI'}</span><span class="sp" id="sp-${p.id}"></span></div>`).join('')}</div>
<div class="cols"><section class="card"><h3>Live transcript</h3><div id="tr" class="tr" aria-live="polite"></div></section>
<section class="card"><div id="stat" class="chip" role="status"></div><div id="er" class="err" role="alert" hidden></div><div id="nudge" class="sm"></div>
<label for="ti">Your turn (speak, or type here)</label><textarea id="ti" rows="3" maxlength="1500"></textarea><div id="im" class="sm" aria-live="polite"></div>
<div class="btns"><button id="bm" class="sec"></button><button id="bs">Submit turn</button><button id="bi" class="sec">✋ Interrupt AI</button><button id="bv" class="sec">🔊 Voice on</button><button id="be" class="danger">End discussion</button></div>
<p class="sm">Auto-submits after a pause in speech; use Submit turn if that is unreliable.</p></section></div>`}
const fmt=ms=>{const s=Math.ceil(ms/1000);return String(Math.floor(s/60)).padStart(2,'0')+':'+String(s%60).padStart(2,'0')};
function upd(){
 if(S.view!=='room'||!$('#stat'))return;const st=S.st;
 $('#stat').textContent=({OPENING:'Moderator opening…',LISTENING:'Your turn',PROCESSING:'Panel is thinking…',AI_SPEAKING:'AI speaking…',CLOSING:'Closing round…',COMPLETED:'Completed'}[st]||st)+' · Mic: '+S.mic;
 [MOD,...S.panelP,ME].forEach(p=>{const on=S.speaker===p.id||(p.id==='me'&&st==='LISTENING'&&S.mic==='listening');$('#av-'+p.id).classList.toggle('on',on);$('#sp-'+p.id).textContent=on?(p.id==='me'?'listening…':'speaking…'):''});
 $('#ti').disabled=$('#bs').disabled=st!=='LISTENING';
 $('#bm').disabled=st!=='LISTENING'||!SR;$('#bm').textContent=!SR?'🎤 Mic unavailable':S.micWanted&&S.mic!=='unavailable'?'⏹ Stop mic':'🎤 Start mic';
 $('#bi').disabled=!(st==='AI_SPEAKING'||st==='PROCESSING');$('#be').disabled=!(st==='LISTENING'||st==='PROCESSING'||st==='AI_SPEAKING');
 $('#bv').textContent=S.muted?'🔇 Voice off':'🔊 Voice on';
 $('#im').textContent=S.interim?'Hearing: '+S.interim:S.buf?'Captured: '+S.buf:'';
 const er=$('#er');er.hidden=!S.err;er.innerHTML=esc(S.err)+(S.failed?' <button id="rt">Retry AI reply</button>':'');
 const tr=$('#tr');tr.innerHTML=S.turns.length?S.turns.map(t=>`<div class="tn ${t.id==='me'?'me':''} ${t.interrupted?'int':''}"><b>${esc(t.name)}</b><span class="sm">#${t.n} · ${esc(t.role)}${t.id==='me'||t.id==='mod'?'':' · AI'}${t.interrupted?' · interrupted':''}</span><div>${esc(t.text)}</div></div>`).join(''):'<p class="sm">The transcript will appear here once the moderator starts.</p>';
 tr.scrollTop=tr.scrollHeight}
function vReport(){const r=S.rep;return `<div class="top"><span class="logo">📊 Your GD report</span><span class="sm">${esc(r.date)}</span></div>
<section class="card"><h2>A. Session summary</h2><p><b>Topic:</b> ${esc(r.topic)}<br><b>Planned duration:</b> ${r.dur} min · <b>Session length:</b> ${fmt(r.elapsed*1000)} · <b>AI participants:</b> ${r.panel} + moderator<br><b>Your turns:</b> ${r.meTurns} · <b>Your words:</b> ${r.meWords}</p>
<p>${r.meTurns?`You took part in ${r.meTurns} turn(s) and spoke ${r.meWords} words out of ${r.all} in total.`:'You did not speak in this session.'}</p>${r.saved===false?'<p class="err">This session could not be saved in this browser (storage unavailable).</p>':''}</section>
<section class="card"><h2>B. Speaker statistics: kisne kitna bola <span class="chip">Measured from transcript</span></h2><div style="overflow-x:auto"><table><tr><th>Speaker</th><th>Turns</th><th>Words</th><th>Share</th><th>Est. time*</th></tr>${r.stats.map(s=>`<tr><td>${esc(s.name)}<br><span class="sm">${esc(s.role)}</span></td><td>${s.turns}</td><td>${s.words}</td><td>${s.share}%<div class="bar"><i style="width:${s.share}%"></i></div></td><td>~${s.estSec}s</td></tr>`).join('')}</table></div><p class="sm">*Estimate only: words ÷ 150 wpm. Microphone timing is not measured. Interrupted turns are excluded.</p></section>
<section class="card"><h2>C. Student feedback <span class="chip">Rule-based analysis, not live AI</span></h2><p class="sm">Every observation cites an exact transcript quote, checked against the cited turn. Where evidence is missing, it says so.</p>
${r.fb.map(f=>`<div style="border-top:1px solid var(--bd);padding:10px 0"><b>${esc(f.cat)}</b> <span class="pill ${f.rating==='Strength'?'Strength':f.rating==='Needs work'?'Needs':'Ins'}">${f.rating}</span><p>${esc(f.expl)}</p>${f.quote?`<blockquote>“${esc(f.quote)}” <span class="sm">— turn #${f.turn}</span></blockquote>`:''}<p class="sm"><b>Try:</b> ${esc(f.sug)}</p></div>`).join('')}</section>
<section class="card"><h2>D. Actionable improvements</h2><ul>${[...new Set(r.fb.filter(f=>f.rating==='Needs work').map(f=>f.sug))].map(s=>`<li>${esc(s)}</li>`).join('')||'<li>Keep practising to build evidence for each category.</li>'}</ul>
<p><b>A stronger response looks like:</b></p><blockquote>“I believe [position] because [reason]. For example, [real example]. Building on [Name]'s point, I'd add [new idea]. In conclusion, [position] because [reason].”</blockquote>
<p><b>Next practice goals:</b></p><ul><li>Speak in at least 3 turns of 2–3 sentences.</li><li>Give one example in every turn.</li><li>Refer to another speaker by name once.</li><li>Finish with a 2-sentence conclusion.</li></ul></section>
<div id="trv" class="card" hidden><h3>Transcript</h3>${S.turns.map(t=>`<div class="tn ${t.id==='me'?'me':''}"><b>${esc(t.name)}</b><span class="sm">#${t.n} · ${esc(t.role)}${t.interrupted?' · interrupted':''}</span><div>${esc(t.text)}</div></div>`).join('')}</div>
<div class="btns"><button data-go="landing">Dashboard</button><button class="sec" id="rtv">Review transcript</button><button class="sec" id="again">Practise this topic again</button><button class="danger" data-del="${r.id}">Delete this session</button></div>`}
function render(){app.innerHTML=({landing:vLanding,setup:vSetup,confirm:vConfirm,room:vRoom,report:vReport})[S.view]();if(S.view==='room'){upd()}}

/* events */
app.addEventListener('click',e=>{const b=e.target.closest('button');if(!b)return;
 if(b.dataset.go){go(b.dataset.go)}
 else if(b.dataset.open){const x=ld().find(i=>i.id===b.dataset.open);if(x){S.rep=x.rep;S.turns=x.turns;go('report')}}
 else if(b.dataset.del){sv(ld().filter(i=>i.id!==b.dataset.del));go('landing')}
 else if(b.id==='th'){const r=document.documentElement;r.dataset.theme=(r.dataset.theme==='dark'||(!r.dataset.theme&&matchMedia('(prefers-color-scheme:dark)').matches))?'light':'dark'}
 else if(b.id==='rv')review();
 else if(b.id==='go'){b.disabled=true;startGD()}
 else if(b.id==='bs')submit();
 else if(b.id==='bi')interrupt();
 else if(b.id==='bv'){S.muted=!S.muted;if(S.muted)cancelSpeech();upd()}
 else if(b.id==='be')beginClosing();
 else if(b.id==='bm'){if(S.micWanted&&S.mic!=='unavailable'){S.micWanted=false;stopRec()}else{clearErr();S.micWanted=true;S.mic='idle';startRec()}upd()}
 else if(b.id==='rt'&&S.failed){const items=S.failed.items;clearErr();S.st='PROCESSING';stopRec();upd();afterRun(items,++S.tok)}
 else if(b.id==='rtv'){const t=$('#trv');t.hidden=!t.hidden}
 else if(b.id==='again'){go('setup')}});
app.addEventListener('change',e=>{const c=S.cfg,t=e.target;
 if(t.name==='tp'){c.useCustom=t.value==='c';if(!c.useCustom)c.topic=TOPICS[+t.value]}
 else if(t.name==='pp'){c.panel=PS.filter(p=>{const el=app.querySelector(`input[name=pp][value=${p.id}]`);return el&&el.checked}).map(p=>p.id)}
 else if(t.id==='du')c.dur=+t.value;else if(t.id==='lg')c.lang=t.value;else if(t.id==='pa')c.pause=+t.value;else if(t.id==='wa')c.wait=+t.value;else if(t.id==='vi')c.vi=t.checked});
app.addEventListener('input',e=>{if(e.target.id==='ct'){S.cfg.custom=e.target.value;S.cfg.useCustom=true;const r=app.querySelector('input[name=tp][value=c]');if(r)r.checked=true}});
function review(){
 const c=S.cfg;let m='';
 if(c.useCustom){const t=c.custom.trim().replace(/\s+/g,' ');
  if(!t)m='Please enter a custom topic.';else if(t.length<5)m='The custom topic is too short (minimum 5 characters).';else if(t.length>120)m='The custom topic is too long (maximum 120 characters).';else if(/[<>]/.test(t))m='The custom topic cannot contain < or >.';else c.topic=t}
 if(!m&&(c.panel.length<3||c.panel.length>5))m='Choose between 3 and 5 AI participants.';
 if(m){const e=$('#er');e.textContent=m;e.hidden=false;return}
 S.topic=c.topic;S.panelP=PS.filter(p=>c.panel.includes(p.id));go('confirm')}
document.addEventListener('keydown',e=>{if(e.key==='Enter'&&(e.ctrlKey||e.metaKey)&&S.view==='room')submit()});
window.addEventListener('offline',()=>setErr('Network connection lost. The demo keeps working offline; browser speech recognition may stop until you reconnect.'));
window.addEventListener('online',()=>{if(S.err.startsWith('Network'))clearErr();upd()});
if('speechSynthesis' in window)speechSynthesis.onvoiceschanged=()=>{if(S.view==='confirm')render()};
setInterval(()=>{if(S.view!=='room'||!S.endAt||!$('#tm'))return;
 const rem=Math.max(0,S.endAt-Date.now());$('#tm').textContent=fmt(rem);$('#pb').style.width=(100*rem/(S.cfg.dur*60000))+'%';
 if(rem<=0&&S.st!=='CLOSING'&&S.st!=='COMPLETED'){beginClosing();return}
 if(!S.warned&&S.st==='LISTENING'&&rem<=Math.max(30000,S.cfg.dur*15000)){S.warned=true;modNote()}
 const first=S.turns.every(t=>t.id==='mod'),idle=!S.buf&&!S.interim&&!$('#ti').value;
 if(S.st==='LISTENING'&&first&&S.openAt){if(!idle)S.openAt=Date.now()+5000;else if(Date.now()>S.openAt){S.openAt=null;aiStarts();return}}
 $('#nudge').textContent=S.st!=='LISTENING'?'':first&&S.openAt?`Take the lead! If you don't start, an AI will begin in ${Math.max(0,Math.ceil((S.openAt-Date.now())/1000))}s.`:Date.now()-S.act>25000?`Reminder: you haven't spoken for ${Math.round((Date.now()-S.act)/1000)}s. Share a thought when ready.`:''},250);
window.addEventListener('beforeunload',()=>{cancelSpeech()});
render();
</script>
</body>
</html>
