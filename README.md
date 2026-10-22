[Four Week Lean.html](https://github.com/user-attachments/files/33813324/Four.Week.Lean.html)
<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<title>Four Week Lean</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700;800&family=Hanken+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap">
<style>
/* Layout: one narrow training-log column on black. Red is the only accent. A knurled-grip texture divides sections. Session types use IWF plate colours, each plate drawn with a centre hole. */
:root{
  --bg:#000000; --surface:#0a0a0a; --surface2:#141414; --ink:#f1ede4; --muted:#9b9588; --line:#262524; --line-strong:#3b3833;
  --accent:#e5232b; --accent-ink:#ffffff; --good:#6fcf97; --warn:#e0b25a; --bad:#ef8a80;
  --plate-red:#b8322f; --plate-blue:#2f55b8; --plate-yellow:#c9a227; --plate-green:#2f8a5a; --plate-white:#d9d6cf; --plate-grey:#6b6860;
  --f-display:'Big Shoulders Display','Arial Narrow',Impact,sans-serif;
  --f-body:'Hanken Grotesk',system-ui,-apple-system,'Segoe UI',sans-serif;
  --f-mono:'IBM Plex Mono',ui-monospace,Menlo,Consolas,monospace;
  color-scheme:dark;
}
:root{background:var(--bg)}
*{box-sizing:border-box}
body{background:var(--bg);color:var(--ink);font:15px/1.55 var(--f-body);
  padding-block:20px 56px;
  padding-left:max(16px,env(safe-area-inset-left,0px));
  padding-right:max(16px,env(safe-area-inset-right,0px))}
.wrap{max-width:780px;margin:0 auto}
h1,h2,h3,h4,p,ul{margin:0}
h1{font:800 clamp(2.8rem,10vw,4.6rem)/.92 var(--f-display);text-transform:uppercase;letter-spacing:.05em;text-wrap:balance}
h2{font:700 1.7rem/1.05 var(--f-display);text-transform:uppercase;letter-spacing:.07em;text-wrap:balance}
h3{font:700 1rem/1.3 var(--f-body)}
h4{font:700 1rem/1.3 var(--f-body)}
.eyebrow{font:500 12px var(--f-mono);text-transform:uppercase;letter-spacing:.2em;color:var(--accent);margin-bottom:10px}
.knurl{height:12px;margin-bottom:22px;border-block:1px solid var(--line-strong);background-image:repeating-linear-gradient(45deg,var(--line-strong) 0 1px,transparent 1px 5px),repeating-linear-gradient(-45deg,var(--line-strong) 0 1px,transparent 1px 5px)}
.lede{max-width:60ch;color:var(--muted);margin-top:14px;font-size:16px}
.muted{color:var(--muted)}
.small{font-size:13px}
.mono{font-family:var(--f-mono);font-variant-numeric:tabular-nums}
.tabs{display:grid;grid-template-columns:repeat(4,1fr);border-bottom:1px solid var(--line-strong);margin:26px 0 24px}
.tabs button{background:none;border:0;border-bottom:3px solid transparent;margin-bottom:-2px;padding:12px 2px 10px;
  font:700 1.1rem var(--f-display);text-transform:uppercase;letter-spacing:.16em;color:var(--muted);cursor:pointer}
.tabs button[aria-selected="true"]{color:var(--accent);border-bottom-color:var(--accent)}
.tabs button:disabled{opacity:.4;cursor:not-allowed}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
.stack{display:grid;gap:18px}
.stack>*{min-width:0}
.card{background:var(--surface);border:1px solid var(--line);border-top:1px solid var(--line-strong);border-radius:2px;padding:22px}
.card>*+*{margin-top:12px}
.split{display:grid;grid-template-columns:minmax(0,1.5fr) minmax(0,1fr);gap:18px;align-items:start}
@media (max-width:640px){.split{grid-template-columns:minmax(0,1fr)}}
.lbl{display:block;font-weight:600;font-size:13px;margin-bottom:6px}
.in{width:100%;font:16px var(--f-body);padding:11px 12px;background:var(--surface2);color:var(--ink);border:1px solid var(--line-strong);border-radius:2px}
.row2{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:14px}
.seg{display:flex;flex-wrap:wrap;gap:6px;position:relative}
.seg input{position:absolute;opacity:0;pointer-events:none}
.seg label{flex:1 1 0;min-width:46px;text-align:center;padding:10px 8px;border:1px solid var(--line-strong);border-radius:2px;cursor:pointer;background:var(--surface2);font-weight:600}
.seg input:checked+label{background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
.seg input:focus-visible+label{outline:2px solid var(--accent);outline-offset:2px}
.btn{font:700 .9rem var(--f-body);text-transform:uppercase;letter-spacing:.1em;padding:13px 20px;border-radius:2px;border:1px solid var(--accent);background:var(--accent);color:var(--accent-ink);cursor:pointer}
.btn.ghost{background:none;color:var(--accent)}
.btn.danger{border-color:var(--bad);background:none;color:var(--bad)}
.btns{display:flex;flex-wrap:wrap;gap:10px}
.errs{border:1px solid var(--bad);color:var(--bad);border-radius:2px;padding:10px 14px;font-size:14px}
.errs ul{padding-left:18px}
.plate{width:34px;height:34px;border-radius:50%;flex:none;border:1px solid var(--line-strong);box-shadow:inset 0 0 0 2px rgba(0,0,0,.35);
  background:radial-gradient(circle at center,var(--bg) 0 3.5px,var(--c) 4.5px)}
.day{display:grid;grid-template-columns:40px 34px minmax(0,1fr);gap:12px;align-items:center;padding:10px 0;border-top:1px solid var(--line)}
.day:first-of-type{border-top:0}
.wd{font:500 12px var(--f-mono);text-transform:uppercase;letter-spacing:.1em;color:var(--muted)}
.tblwrap{overflow-x:auto}
.tbl{width:100%;border-collapse:collapse;font-size:14px}
.tbl th,.tbl td{padding:9px 8px;border-bottom:1px solid var(--line);text-align:left;vertical-align:top}
.tbl th{font:500 11px var(--f-mono);text-transform:uppercase;letter-spacing:.08em;color:var(--muted)}
.tbl td.n,.tbl th.n{text-align:right;font-family:var(--f-mono);font-variant-numeric:tabular-nums;white-space:nowrap}
.tbl .cue{display:block;color:var(--muted);font-size:13px;margin-top:2px}
details.sess{border-top:1px solid var(--line);padding:10px 0}
details.sess summary{display:flex;align-items:center;gap:12px;cursor:pointer;list-style:none}
details.sess summary::-webkit-details-marker{display:none}
details.sess summary::after{content:"+";margin-left:auto;font:500 20px var(--f-mono);color:var(--muted)}
details.sess[open] summary::after{content:"\2212"}
details.sess .tblwrap{margin-top:10px}
.kcal{font:800 clamp(3.2rem,13vw,5.4rem)/.95 var(--f-display);font-variant-numeric:tabular-nums;color:var(--accent);letter-spacing:.02em}
.kcal small{font:500 14px var(--f-mono);letter-spacing:.08em;color:var(--muted);text-transform:uppercase;margin-left:6px}
.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:1px;background:var(--line-strong);border:1px solid var(--line-strong);border-radius:2px;overflow:hidden}
.stat{background:var(--bg);padding:14px 16px}
.stat b{display:block;font:700 2rem/1.1 var(--f-display);font-variant-numeric:tabular-nums}
.stat span{font:500 11px var(--f-mono);text-transform:uppercase;letter-spacing:.08em;color:var(--muted)}
.note{border-left:3px solid var(--accent);padding:4px 0 4px 12px;color:var(--ink);font-size:14px}
ul.plain{padding-left:18px;display:grid;gap:6px}
.pills{display:flex;flex-wrap:wrap;gap:8px}
.pill{font:600 13px var(--f-body);text-transform:uppercase;letter-spacing:.08em;padding:9px 14px;border:1px solid var(--line-strong);background:var(--surface2);color:var(--ink);border-radius:2px;cursor:pointer;display:inline-flex;align-items:center;gap:8px}
.pill[aria-pressed="true"]{background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
.pill .plate{width:16px;height:16px;background:radial-gradient(circle at center,var(--surface2) 0 1.5px,var(--c) 2.5px)}
.ex{border-top:1px solid var(--line);padding:16px 0}
.ex:first-child{border-top:0;padding-top:0}
.exhead{display:flex;justify-content:space-between;gap:12px;align-items:baseline;flex-wrap:wrap}
.tag{font:500 13px var(--f-mono);color:var(--muted);white-space:nowrap}
.cue{color:var(--muted);font-size:13px;margin-top:2px}
.sug{font-size:13px;margin:8px 0 10px;padding:8px 12px;background:var(--surface2);border-left:2px solid var(--accent);border-radius:0}
.sets{display:grid;grid-template-columns:40px minmax(0,1fr) minmax(0,1fr);gap:8px;align-items:center;max-width:380px}
.sets .h{font:500 11px var(--f-mono);text-transform:uppercase;letter-spacing:.08em;color:var(--muted)}
.sets .sn{font:500 14px var(--f-mono);color:var(--muted)}
.num{width:100%;font:500 16px var(--f-mono);text-align:center;padding:10px 6px;background:var(--surface2);color:var(--ink);border:1px solid var(--line-strong);border-radius:2px}
.num::placeholder{color:var(--muted);opacity:.55}
.bar{display:grid;grid-template-columns:56px minmax(0,1fr) 92px;gap:10px;align-items:center;margin:8px 0;font-size:13px}
.track{height:14px;background:var(--surface2);border:1px solid var(--line-strong);border-radius:0;overflow:hidden}
.fill{height:100%;background:var(--accent)}
.check{display:flex;gap:10px;align-items:center;font-weight:600}
.check input{width:20px;height:20px}
.foot{margin-top:32px;font-size:12.5px;color:var(--muted);max-width:70ch}

details.how{margin:8px 0 0}
details.how summary{cursor:pointer;display:inline-block;font:600 12px var(--f-mono);text-transform:uppercase;letter-spacing:.12em;color:var(--accent);list-style:none;padding:4px 0}
details.how summary::-webkit-details-marker{display:none}
details.how summary::before{content:"+ "}
details.how[open] summary::before{content:"\2212 "}
.howbody{border-left:2px solid var(--accent);padding:4px 0 4px 14px;margin-top:6px;display:grid;gap:8px;font-size:14px;color:var(--ink)}
.howbody b{font:600 11px var(--f-mono);text-transform:uppercase;letter-spacing:.1em;color:var(--muted);margin-right:4px}
.howbody .demo{justify-self:start;color:var(--accent);font-weight:600;text-underline-offset:3px}
</style>

<div class="wrap">
  <div class="knurl" aria-hidden="true"></div>
  <header>
    <p class="eyebrow">30-day gym programme</p>
    <h1>Four Week Lean</h1>
    <p class="lede">Choose how many days you can train. You get a plan built around simple lifts, a daily calorie range, a food guide, and a log that tells you what to lift next week.</p>
  </header>
  <nav class="tabs" id="tabs" aria-label="Sections">
    <button type="button" data-go="profile" aria-selected="true">Profile</button>
    <button type="button" data-go="plan" aria-selected="false">Plan</button>
    <button type="button" data-go="food" aria-selected="false">Food</button>
    <button type="button" data-go="tracker" aria-selected="false">Tracker</button>
  </nav>
  <main id="view"></main>
  <p class="foot">This programme is general fitness guidance, not medical advice. If you have a medical condition, an injury, take medication, or are pregnant, check with your doctor before you start. Stop any exercise that causes sharp pain. For adults aged 18 and over. Calorie figures are estimates. Adjust them after two weeks based on how your weight is moving.</p>
</div>

<script>
// ==LOGIC START==
const FACTORS={2:1.3,3:1.375,4:1.45,5:1.55,6:1.6,7:1.65};
const r10=n=>Math.round(n/10)*10;
function calcNutrition(p){
  const hm=p.height/100, bmi=p.weight/(hm*hm);
  const bmr=10*p.weight+6.25*p.height-5*p.age+(p.sex==='male'?5:-161);
  const tdee=bmr*FACTORS[p.days];
  let deficit, mode='cut';
  if(bmi<18.5){deficit=-150;mode='gain';}
  else if(bmi<21){deficit=250;mode='gentle';}
  else deficit=Math.min(500,Math.round(tdee*0.2));
  const floor=p.sex==='male'?1500:1200;
  const target=r10(Math.max(tdee-deficit,floor));
  const realDeficit=Math.round(tdee-target);
  const base=bmi>30?27*hm*hm:p.weight;
  const protein=Math.round(2*base);
  const fat=Math.round(target*0.25/9);
  const carbs=Math.max(0,Math.round((target-protein*4-fat*9)/4));
  const weekly=realDeficit>0?realDeficit*7/7700:0;
  return {
    bmi, bmr:Math.round(bmr), tdee:Math.round(tdee), mode, target, lo:r10(target-100), hi:r10(target+100),
    deficit:realDeficit, protein, fat, carbs, weekly,
    healthyLo:18.5*hm*hm, healthyHi:24.9*hm*hm,
    meals:{breakfast:r10(target*.25),lunch:r10(target*.30),dinner:r10(target*.30),snacks:r10(target*.15)}
  };
}
function validateProfile(v){
  const e=[];
  if(v.sex!=='male'&&v.sex!=='female')e.push('Choose male or female.');
  if(!(v.age>=18&&v.age<=70))e.push('Age must be between 18 and 70.');
  if(!(v.height>=120&&v.height<=230))e.push('Height must be between 120 and 230 cm.');
  if(!(v.weight>=35&&v.weight<=250))e.push('Weight must be between 35 and 250 kg.');
  if(!/^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/.test(v.email||''))e.push('Enter a valid email address.');
  if(!(v.days>=2&&v.days<=7))e.push('Choose 2 to 7 training days.');
  return e;
}
function fmt(n){return Number.isInteger(n)?String(n):n.toFixed(1).replace(/\.0$/,'');}
function suggest(prev,ex,range){
  const sets=prev.filter(s=>s&&parseFloat(s.reps)>0).map(s=>({kg:parseFloat(s.kg)||0,reps:parseFloat(s.reps)}));
  if(!sets.length)return null;
  const kg=Math.max(...sets.map(s=>s.kg));
  const top=sets.filter(s=>s.kg===kg);
  const list=top.map(s=>s.reps).join(', ');
  const last=ex.u==='s'?`Last week: ${kg?fmt(kg)+' kg for ':''}${list} seconds.`:`Last week: ${fmt(kg)} kg for ${list} reps.`;
  if(ex.u==='s')return last+' Add 5 seconds to each set.';
  const hit=top.length>=Math.min(range.sets,2)&&top.every(s=>s.reps>=range.hi);
  if(hit)return `${last} You reached the top of the range. Go up to ${fmt(kg+ex.inc)} kg and aim for ${range.lo} reps.`;
  return `${last} Stay at ${fmt(kg)} kg and add one rep to each set.`;
}
// ==LOGIC END==

const EX={
  squat:{n:'Back squat (or leg press)',inc:5,u:'r',cue:'Feet shoulder-width. Sit down between your hips, heels flat, chest up.'},
  legpress:{n:'Leg press',inc:5,u:'r',cue:'Feet shoulder-width on the platform. Lower until knees are about 90 degrees, press through your whole foot.'},
  goblet:{n:'Goblet squat',inc:2,u:'r',cue:'Hold one dumbbell at your chest. Sit down between your heels, elbows inside your knees.'},
  rdl:{n:'Romanian deadlift',inc:5,u:'r',cue:'Soft knees, push your hips back, slide the bar down your thighs until your hamstrings stretch. Back flat.'},
  lunge:{n:'Walking lunge',inc:2,u:'r',cue:'Long step, back knee nearly touches the floor, drive up through the front heel. Reps are per leg. Log one dumbbell.'},
  bss:{n:'Bulgarian split squat',inc:2,u:'r',cue:'Back foot on a bench. Lower straight down with the front heel planted. Reps are per leg.'},
  hipthrust:{n:'Hip thrust',inc:5,u:'r',cue:'Upper back on a bench, bar over your hips. Drive up, squeeze your glutes, keep your ribs down.'},
  legcurl:{n:'Leg curl',inc:2.5,u:'r',cue:'Curl your heels toward your glutes, lower for three seconds.'},
  legext:{n:'Leg extension',inc:2.5,u:'r',cue:'Straighten your knees fully and pause for one second at the top.'},
  calf:{n:'Standing calf raise',inc:5,u:'r',cue:'Rise onto the balls of your feet, pause at the top, stretch fully at the bottom.'},
  seatedcalf:{n:'Seated calf raise',inc:5,u:'r',cue:'Same as the standing raise. Slow and full range.'},
  bench:{n:'Bench press',inc:2.5,u:'r',cue:'Shoulder blades pinched, feet planted. Lower to mid-chest, press up.'},
  dbbench:{n:'Dumbbell bench press',inc:2,u:'r',cue:'Lower until your elbows are just below the bench, press up. Log one dumbbell.'},
  incline:{n:'Incline dumbbell press',inc:2,u:'r',cue:'Bench at about 30 degrees. Press straight up over your upper chest. Log one dumbbell.'},
  ohp:{n:'Dumbbell shoulder press',inc:2,u:'r',cue:'Seated with back support. Press overhead without arching your lower back. Log one dumbbell.'},
  lateral:{n:'Lateral raise',inc:1,u:'r',cue:'Light weights. Lift out to the sides to shoulder height, leading with your elbows.'},
  tri:{n:'Triceps pushdown',inc:2.5,u:'r',cue:'Elbows pinned to your sides. Straighten your arms fully.'},
  ohtri:{n:'Overhead triceps extension',inc:2,u:'r',cue:'Hold one dumbbell behind your head with both hands. Extend up, elbows narrow.'},
  pulldown:{n:'Lat pulldown',inc:2.5,u:'r',cue:'Pull the bar to your upper chest, drive your elbows down. Do not lean back.'},
  cablerow:{n:'Seated cable row',inc:2.5,u:'r',cue:'Chest tall. Pull the handle to your belly and squeeze your shoulder blades.'},
  dbrow:{n:'One-arm dumbbell row',inc:2,u:'r',cue:'Hand and knee on a bench. Pull the dumbbell to your hip without twisting. Reps are per arm.'},
  facepull:{n:'Face pull',inc:2.5,u:'r',cue:'Rope at face height. Pull toward your forehead with elbows high.'},
  curl:{n:'Dumbbell curl',inc:2,u:'r',cue:'Elbows by your sides. Curl up, lower slowly.'},
  hammer:{n:'Hammer curl',inc:2,u:'r',cue:'Palms facing each other. Curl up with no swinging.'},
  plank:{n:'Plank',inc:0,u:'s',cue:'Forearms down, body in a straight line, squeeze your glutes. Log seconds.'},
  farmer:{n:"Farmer's carry",inc:2,u:'s',cue:'Heavy dumbbells, walk tall with short steps. Log seconds and one dumbbell weight.'}
};
const SESS={
  FA:{name:'Full Body A',focus:'Legs, chest, back, shoulders, core',plate:'--plate-white',ex:[['squat',3,8,10],['dbbench',3,8,12],['cablerow',3,8,12],['rdl',3,8,10],['ohp',2,10,12],['plank',3,30,45]]},
  FB:{name:'Full Body B',focus:'Legs, glutes, chest, back, shoulders',plate:'--plate-white',ex:[['legpress',3,10,12],['incline',3,8,12],['pulldown',3,8,12],['lunge',3,10,12],['hipthrust',3,8,12],['lateral',2,12,15]]},
  FC:{name:'Full Body C',focus:'Squat, bench, row, hamstrings, carry',plate:'--plate-white',ex:[['goblet',3,10,12],['bench',3,6,10],['dbrow',3,8,12],['legcurl',3,10,12],['facepull',3,12,15],['farmer',3,30,40]]},
  UA:{name:'Upper A',focus:'Chest, back, shoulders, arms',plate:'--plate-green',ex:[['bench',3,6,10],['pulldown',3,8,12],['ohp',3,8,12],['cablerow',3,8,12],['tri',2,10,15],['curl',2,10,15]]},
  UB:{name:'Upper B',focus:'Upper chest, back, rear delts, arms',plate:'--plate-green',ex:[['incline',3,8,12],['dbrow',3,8,12],['lateral',3,12,15],['facepull',3,12,15],['ohtri',2,10,15],['hammer',2,10,15]]},
  LA:{name:'Lower A',focus:'Quads, hamstrings, calves, core',plate:'--plate-yellow',ex:[['squat',3,6,10],['rdl',3,8,10],['lunge',2,10,12],['legcurl',3,10,12],['calf',3,12,15],['plank',3,30,45]]},
  LB:{name:'Lower B',focus:'Quads, glutes, hamstrings, calves',plate:'--plate-yellow',ex:[['legpress',3,10,12],['hipthrust',3,8,12],['bss',3,8,10],['legext',2,12,15],['seatedcalf',3,12,15],['plank',3,30,45]]},
  PushA:{name:'Push A',focus:'Chest, shoulders, triceps',plate:'--plate-red',ex:[['bench',3,6,10],['incline',3,8,12],['ohp',3,8,12],['lateral',3,12,15],['tri',3,10,15]]},
  PushB:{name:'Push B',focus:'Chest, shoulders, triceps',plate:'--plate-red',ex:[['dbbench',3,8,12],['ohp',3,10,12],['lateral',3,12,15],['ohtri',3,10,15]]},
  PullA:{name:'Pull A',focus:'Back, rear delts, biceps',plate:'--plate-blue',ex:[['pulldown',3,8,12],['cablerow',3,8,12],['facepull',3,12,15],['curl',3,10,15]]},
  PullB:{name:'Pull B',focus:'Back, rear delts, biceps',plate:'--plate-blue',ex:[['dbrow',3,8,12],['pulldown',3,10,12],['facepull',3,12,15],['hammer',3,10,15]]},
  AR:{name:'Active Recovery',focus:'Walk, easy cycle and mobility',plate:'--plate-grey',ex:[],
    note:'Walk briskly or cycle easily for 30 to 40 minutes. Then stretch hips, hamstrings, chest and upper back for 10 minutes. Keep it easy. This day helps you recover for the next lift.'}
};
const SEQ={2:['FA','FB'],3:['FA','FB','FC'],4:['UA','LA','UB','LB'],5:['PushA','PullA','LA','UB','LB'],
  6:['PushA','PullA','LA','PushB','PullB','LB'],7:['PushA','PullA','LA','PushB','PullB','LB','AR']};
const WD={2:[0,3],3:[0,2,4],4:[0,1,3,4],5:[0,1,3,4,5],6:[0,1,2,3,4,5],7:[0,1,2,3,4,5,6]};
const WDN=['Mon','Tue','Wed','Thu','Fri','Sat','Sun'];
const SPLIT={2:'Full body, twice a week',3:'Full body, three times a week',4:'Upper / Lower, twice each',5:'Push, Pull, Legs, Upper, Lower',6:'Push / Pull / Legs, twice each',7:'Push / Pull / Legs twice, plus an active recovery day'};
const HINT={2:'Two full-body sessions. Every muscle is trained twice a week. Best when time is tight.',
  3:'Three full-body sessions. A strong all-round choice with a rest day between lifts.',
  4:'Upper and lower days, each twice a week. More volume per muscle, still plenty of recovery.',
  5:'Push, pull, legs, then an upper and a lower day. Most muscles get hit twice.',
  6:'Push, pull and legs twice a week. High volume. You need good sleep and food to recover.',
  7:'Six lifting days plus one easy recovery day. Only choose this if you are already used to training often.'};
const WEEKS=[
  {w:1,t:'Learn the movements',rir:'Stop 3 reps before you could not do another',fin:'7 out of 10 effort'},
  {w:2,t:'Build',rir:'Stop 2 reps before failure',fin:'8 out of 10 effort'},
  {w:3,t:'Push',rir:'Stop 1 to 2 reps before failure',fin:'8 to 9 out of 10 effort'},
  {w:4,t:'Peak',rir:'Stop 0 to 1 reps before failure on the last set',fin:'9 out of 10 effort'}
];
const EAT=[
  ['Chicken breast, grilled','150 g cooked',250,46],['Lean beef mince (5% fat)','150 g cooked',280,38],['Eggs','2 large',150,12],
  ['Salmon fillet','150 g',310,33],['Hake or white fish','150 g',150,30],['Tuna in water','1 tin, drained',110,25],
  ['Greek yoghurt, fat-free','200 g',120,20],['Cottage cheese, low fat','150 g',120,17],['Whey protein','1 scoop (30 g)',120,24],['Biltong','50 g',130,25],
  ['Oats','50 g dry',190,7],['Brown rice','150 g cooked',165,4],['Potato, boiled','200 g',150,4],['Sweet potato','200 g',170,3],
  ['Wholewheat bread','2 slices',180,8],['Pap (maize meal)','200 g cooked',140,3],['Lentils or beans','150 g cooked',170,12],
  ['Banana','1 medium',105,1],['Apple','1 medium',80,0],['Berries','100 g',45,1],['Broccoli, spinach or mixed veg','150 g',50,4],
  ['Avocado','half',120,2],['Olive oil','1 tablespoon',120,0],['Peanut butter','1 tablespoon',95,4],['Almonds','30 g',175,6]
];
const LIMIT=[
  ['Soft drink','330 ml',140],['Fruit juice','250 ml',110],['Beer','340 ml',150],['Wine','150 ml',125],
  ['Chips or fries, takeaway','medium',380],['Takeaway burger','1 burger',700],['Pizza','1 slice',300],
  ['Chocolate bar','50 g',260],['Croissant or pastry','1',270],['Biscuits','3',160],['Ice cream','2 scoops',270],['Sweetened cereal','60 g',230]
];

const HOW={
  squat:['Set the bar on your upper back, not your neck. Feet shoulder-width, toes slightly out. Take a big breath and tighten your stomach.','Push your hips back and bend your knees together. Go down until your thighs are about parallel to the floor, then drive up through your whole foot.','Heels lifting, knees caving in, or your chest dropping forward. Lower the weight if any of these happen. Use the leg press instead if squats are new to you.'],
  legpress:['Sit with your back and hips flat on the pad. Feet shoulder-width, in the middle of the platform.','Lower slowly until your knees are about 90 degrees, then press up without locking your knees.','Your hips lifting off the seat, or your knees collapsing inward.'],
  goblet:['Hold one dumbbell upright at your chest with both hands. Feet a little wider than your shoulders.','Sit straight down between your legs with your elbows inside your knees, then stand back up.','Rounding your back, or letting the weight pull you forward.'],
  rdl:['Hold the bar at your thighs. Feet hip-width, knees slightly bent.','Push your hips back as far as you can, sliding the bar down your legs until your hamstrings stretch. Squeeze your glutes to stand tall.','Rounding your lower back, or bending your knees more as you go down. That turns it into a squat.'],
  lunge:['Hold a dumbbell in each hand by your sides and stand tall.','Step forward into a long stride. Lower until your back knee nearly touches the floor, then push off the front foot into the next step.','Short steps, leaning forward, or your front knee caving in.'],
  bss:['Stand about 60 cm in front of a bench and rest the top of your back foot on it.','Lower straight down until your front thigh is parallel to the floor, then drive up through the front heel.','Standing too close to the bench, or letting your front knee cave inward.'],
  hipthrust:['Sit on the floor with your upper back against a bench and roll the bar over your hips. Use a pad on the bar. Feet flat, knees bent.','Drive your hips up until your body is level from shoulders to knees. Squeeze your glutes for a second, then lower.','Arching your lower back at the top. Keep your ribs down.'],
  legcurl:['Adjust the pad so it sits just above your heels. Keep your hips pressed down.','Curl your heels toward your glutes, pause, then lower for 3 seconds.','Lifting your hips, or using momentum to move the weight.'],
  legext:['Adjust the seat so your knees line up with the machine pivot and the pad rests on your lower shins.','Straighten your legs, pause for one second, then lower under control.','Swinging the weight up, or snapping your knees straight.'],
  calf:['Stand on a step or machine with the balls of your feet on the edge and your heels hanging off.','Lower your heels for a full stretch, then rise as high as you can and pause.','Bouncing, or a short range of motion.'],
  seatedcalf:['Sit with the pad on your thighs and the balls of your feet on the platform.','Lower for a deep stretch, then press up and pause at the top.','Bouncing out of the bottom.'],
  bench:['Lie with your eyes under the bar. Pull your shoulder blades together and down, and keep your feet flat on the floor.','Unrack the bar over your shoulders. Lower it to your mid-chest with elbows about 45 degrees from your body, then press up.','Bouncing the bar off your chest, flaring your elbows wide, or lifting your hips. Use a spotter for heavy sets.'],
  dbbench:['Sit with the dumbbells on your thighs, lie back and bring them to chest level.','Press up until your arms are straight above your chest, then lower until your elbows are just below the bench.','Letting the dumbbells drift wide, or arching your back.'],
  incline:['Set the bench to about 30 degrees. Pull your shoulder blades back.','Press the dumbbells up over your upper chest, then lower slowly to chest height.','A bench set too steep. That turns it into a shoulder press.'],
  ohp:['Sit with your back supported and the dumbbells at shoulder height, palms facing forward.','Press up until your arms are almost straight, then lower to ear level.','Arching your back. Squeeze your glutes and tighten your stomach.'],
  lateral:['Stand holding light dumbbells at your sides with a slight bend in your elbows.','Raise your arms out to the sides to shoulder height, leading with your elbows. Lower slowly.','Swinging the weights or shrugging. Go lighter than you think you need to.'],
  tri:['Stand facing a cable with a bar or rope attached. Tuck your elbows at your sides.','Press down until your arms are straight and squeeze, then let the handle rise until your forearms are just above level.','Letting your elbows drift forward, or leaning over the weight.'],
  ohtri:['Hold one dumbbell with both hands overhead, standing or sitting.','Bend your elbows to lower it behind your head, then straighten your arms.','Elbows flaring wide.'],
  pulldown:['Hold the bar slightly wider than shoulder-width. Tuck your thighs under the pad and keep your chest tall.','Pull the bar to your upper chest by driving your elbows down. Control it back up.','Leaning far back, or pulling the bar behind your neck.'],
  cablerow:['Sit with your knees slightly bent and your chest tall, holding the handle with straight arms.','Pull the handle to your belly and squeeze your shoulder blades together. Return slowly.','Rocking your body to move the weight.'],
  dbrow:['Put one hand and the same-side knee on a bench. Keep your back flat with the dumbbell hanging from your other hand.','Pull the dumbbell toward your hip, keeping your elbow close to your body. Lower it fully.','Twisting your body or shrugging.'],
  facepull:['Set a rope at face height. Step back until your arms are straight.','Pull the rope toward your forehead with your elbows high and wide. Squeeze your upper back.','Using too much weight, which turns it into a row.'],
  curl:['Stand tall holding dumbbells by your sides, palms facing forward.','Curl up without moving your elbows, then lower slowly.','Swinging your body to lift the weight.'],
  hammer:['Stand holding dumbbells with your palms facing each other.','Curl up keeping your palms facing in, then lower slowly.','Swinging, or letting your elbows drift forward.'],
  plank:['Put your forearms on the floor with your elbows under your shoulders and your legs straight.','Hold a straight line from head to heels. Squeeze your glutes, tighten your stomach and breathe normally.','Hips sagging or piking up. End the set when your form breaks.'],
  farmer:['Pick up heavy dumbbells with a flat back and stand tall.','Walk with short, quick steps, shoulders back and stomach tight.','Leaning, shrugging, or letting the weights swing.']
};
function howHTML(k){
  const w=HOW[k], e=EX[k]; if(!w)return '';
  const q=encodeURIComponent(e.n+' proper form');
  return `<details class="how"><summary>How to do it</summary><div class="howbody"><p><b>Set up.</b> ${w[0]}</p><p><b>Move.</b> ${w[1]}</p><p><b>Avoid.</b> ${w[2]}</p><a class="demo" href="https://www.youtube.com/results?search_query=${q}" target="_blank" rel="noopener">Watch a demo video</a></div></details>`;
}

// state
const KEY='fwl-v1';
let S={profile:null,log:{},bw:{},done:{}};
function load(){try{const r=localStorage.getItem(KEY);if(r){const o=JSON.parse(r);if(o&&typeof o==='object')S=Object.assign(S,o);}}catch(e){}}
function save(){try{localStorage.setItem(KEY,JSON.stringify(S));}catch(e){}}
const ui={tab:'profile',week:1,sid:null,confirm:false};
const $v=()=>document.getElementById('view');
const esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const num=n=>Math.round(n).toLocaleString('en-US');
const planFor=d=>SEQ[d].map((sid,i)=>({sid,wd:WD[d][i]}));
const plateHTML=v=>`<span class="plate" style="--c:var(${v})" aria-hidden="true"></span>`;

// views
function viewProfile(){
  const p=S.profile||{};
  const c=(n,v)=>p[n]===v?'checked':'';
  const days=[2,3,4,5,6,7].map(d=>`<input type="radio" name="days" id="d${d}" value="${d}" ${p.days===d?'checked':''}><label for="d${d}">${d}</label>`).join('');
  return `<div class="split">
  <form class="card" id="f" novalidate>
    <h2>${S.profile?'Your details':'Start here'}</h2>
    <div><span class="lbl">Sex</span><div class="seg" role="radiogroup" aria-label="Sex">
      <input type="radio" name="sex" id="sm" value="male" ${c('sex','male')}><label for="sm">Male</label>
      <input type="radio" name="sex" id="sf" value="female" ${c('sex','female')}><label for="sf">Female</label></div></div>
    <div class="row2">
      <div><label class="lbl" for="age">Age</label><input class="in" id="age" type="number" inputmode="numeric" min="18" max="70" placeholder="e.g. 29" value="${p.age||''}"></div>
      <div><label class="lbl" for="height">Height (cm)</label><input class="in" id="height" type="number" inputmode="decimal" min="120" max="230" placeholder="e.g. 175" value="${p.height||''}"></div>
      <div><label class="lbl" for="weight">Weight (kg)</label><input class="in" id="weight" type="number" inputmode="decimal" step="0.1" min="35" max="250" placeholder="e.g. 82" value="${p.weight||''}"></div>
    </div>
    <div><label class="lbl" for="email">Email</label><input class="in" id="email" type="email" autocomplete="email" placeholder="you@example.com" value="${esc(p.email||'')}"></div>
    <div><span class="lbl">Training days per week</span><div class="seg" role="radiogroup" aria-label="Training days per week">${days}</div>
      <p class="small muted" id="hint" style="margin-top:8px">${p.days?HINT[p.days]:'Pick the number of days you can train every week.'}</p></div>
    <div id="errs" aria-live="polite"></div>
    <div class="btns"><button class="btn" type="submit">${S.profile?'Update my plan':'Build my plan'}</button></div>
    <p class="small muted">Your details and training log are saved in this browser only. Nothing is sent anywhere.</p>
  </form>
  <aside class="card">
    <h2>What you get</h2>
    <ul class="plain">
      <li>A 2 to 7 day plan with plain, proven lifts.</li>
      <li>A four-week progression from easier to hardest.</li>
      <li>A daily calorie range and protein target from your numbers.</li>
      <li>Foods to eat and avoid with calories per portion.</li>
      <li>A log for every set, with a suggested weight for next week.</li>
    </ul>
    ${S.profile?`<div style="margin-top:18px">${ui.confirm
      ?`<p class="small">Delete your profile and all logged sets from this browser?</p><div class="btns" style="margin-top:8px"><button class="btn danger" type="button" data-act="wipe">Yes, delete</button><button class="btn ghost" type="button" data-act="nowipe">Cancel</button></div>`
      :`<button class="btn ghost" type="button" data-act="askwipe">Clear my data</button>`}</div>`:''}
  </aside></div>`;
}

function viewPlan(){
  const p=S.profile, plan=planFor(p.days);
  const rest=WDN.filter((_,i)=>!WD[p.days].includes(i));
  const days=plan.map(d=>{const s=SESS[d.sid];return `<div class="day"><span class="wd">${WDN[d.wd]}</span>${plateHTML(s.plate)}<div><b>${s.name}</b><br><span class="muted small">${s.focus}</span></div></div>`;}).join('');
  const sess=plan.map(d=>{
    const s=SESS[d.sid];
    let body;
    if(!s.ex.length)body=`<p style="margin-top:10px">${s.note}</p>`;
    else body=`<div class="tblwrap"><table class="tbl"><thead><tr><th>Exercise</th><th class="n">Sets x reps</th></tr></thead><tbody>${
      s.ex.map(([k,sets,lo,hi])=>{const e=EX[k];return `<tr><td><b>${e.n}</b><span class="cue">${e.cue}</span>${howHTML(k)}</td><td class="n">${sets} x ${lo}-${hi}${e.u==='s'?' s':''}</td></tr>`;}).join('')}</tbody></table></div>`;
    return `<details class="sess"><summary>${plateHTML(s.plate)}<span><b>${s.name}</b> <span class="muted small">${WDN[d.wd]}</span></span></summary>${body}</details>`;
  }).join('');
  const weeks=WEEKS.map(w=>`<tr><td class="n">${w.w}</td><td><b>${w.t}</b></td><td>${w.rir}</td><td>${w.fin}</td></tr>`).join('');
  return `<div class="stack">
  <section class="card"><p class="eyebrow">${p.days} days a week</p><h2>${SPLIT[p.days]}</h2>
    <div style="margin-top:14px">${days}</div>
    <p class="small muted">${rest.length?`Rest days: ${rest.join(', ')}. You can move sessions around, keep a rest day between hard lower-body days when you can.`:'Day 7 is easy on purpose. Do not skip the recovery.'}</p>
    <div class="btns"><button class="btn" type="button" data-go="food">See my calories</button><button class="btn ghost" type="button" data-go="tracker">Open tracker</button></div>
  </section>
  <section class="card"><h2>How every session runs</h2>
    <ul class="plain">
      <li><b>Warm up</b> for 5 minutes with light cardio. Then do 1 or 2 light sets of your first exercise.</li>
      <li><b>Rest</b> 2 to 3 minutes after heavy compound lifts. Rest 60 to 90 seconds after the smaller ones.</li>
      <li><b>Control the weight.</b> Lift it in about 1 second, lower it in 2 to 3 seconds.</li>
      <li><b>Finisher</b> after lifting: 10 rounds of 30 seconds hard and 30 seconds easy on a bike, rower or fast incline walk.</li>
      <li><b>Steps</b> every day: aim for 8,000 to 10,000. This burns extra fat without hurting recovery.</li>
    </ul></section>
  <section class="card"><h2>Four-week progression</h2>
    <div class="tblwrap"><table class="tbl"><thead><tr><th class="n">Week</th><th>Focus</th><th>Effort on each set</th><th>Finisher</th></tr></thead><tbody>${weeks}</tbody></table></div>
    <p class="small muted">Each week, try to add one rep per set. When you reach the top of the rep range on every set, add a little weight and drop back to the low end of the range. The tracker works this out for you.</p></section>
  <section class="card"><h2>Your sessions</h2><div>${sess}</div></section>
  <section class="card"><h2>Why this works</h2>
    <ul class="plain">
      <li>Training each muscle about twice a week builds more muscle than once a week (Schoenfeld, Ogborn and Krieger, 2016 meta-analysis).</li>
      <li>Adding reps or weight over time, called progressive overload, is what keeps muscle and strength growing.</li>
      <li>A protein intake of at least 1.6 g per kg of body weight supports muscle gain and keeps it while you lose fat (Morton et al., 2018 meta-analysis).</li>
      <li>Interval cardio gives similar fat loss to steady cardio in less time (Wewege et al., 2017 meta-analysis).</li>
      <li>A moderate calorie deficit of about 20% loses fat without wrecking your training.</li>
    </ul>
    <p class="small muted">Results vary. A realistic one-month outcome is about 1.5 to 3 kg of fat lost, better strength, and a visibly tighter look, if you follow the plan and the food guide.</p></section>
  </div>`;
}

function viewFood(){
  const p=S.profile, n=calcNutrition(p);
  const goal=n.mode==='gain'?'Your weight is below the usual healthy range for your height, so this target is set slightly above maintenance to help you build muscle instead of cutting.'
    :n.mode==='gentle'?'You are already fairly lean, so this uses a smaller deficit. It will be slower, and that protects your muscle.':
    `This is about ${n.deficit} kcal a day below what you burn. That is roughly ${fmt(Math.round(n.weekly*10)/10)} kg of fat a week, about ${fmt(Math.round(n.weekly*4*10)/10)} kg over the four weeks. The first week often shows extra water loss too.`;
  const eatRows=EAT.map(r=>`<tr><td><b>${r[0]}</b><span class="cue">${r[1]}</span></td><td class="n">${r[2]}</td><td class="n">${r[3]}</td></tr>`).join('');
  const limRows=LIMIT.map(r=>`<tr><td><b>${r[0]}</b><span class="cue">${r[1]}</span></td><td class="n">${r[2]}</td></tr>`).join('');
  return `<div class="stack">
  <section class="card">
    <p class="eyebrow">Daily calories</p>
    <div class="kcal">${num(n.lo)} to ${num(n.hi)}<small>kcal</small></div>
    <p>${goal}</p>
    <div class="stats">
      <div class="stat"><b>${n.protein} g</b><span>Protein</span></div>
      <div class="stat"><b>${n.carbs} g</b><span>Carbs</span></div>
      <div class="stat"><b>${n.fat} g</b><span>Fat</span></div>
      <div class="stat"><b>${num(n.target)}</b><span>Aim for</span></div>
    </div>
    <p class="small muted">Worked out with the Mifflin-St Jeor formula: resting burn ${num(n.bmr)} kcal, times an activity factor for ${p.days} training days, gives about ${num(n.tdee)} kcal to maintain your weight. Weigh yourself once a week. If you lose more than 1 kg a week, eat 150 kcal more. If you lose less than 0.25 kg a week after two weeks, eat 150 kcal less.</p>
    <p class="small muted">Your BMI is ${fmt(Math.round(n.bmi*10)/10)}. A healthy weight for your height is about ${fmt(Math.round(n.healthyLo))} to ${fmt(Math.round(n.healthyHi))} kg. BMI does not separate muscle from fat, so use it as a rough guide only.</p>
  </section>
  <section class="card"><h2>Meal budget</h2>
    <div class="stats">
      <div class="stat"><b>${num(n.meals.breakfast)}</b><span>Breakfast</span></div>
      <div class="stat"><b>${num(n.meals.lunch)}</b><span>Lunch</span></div>
      <div class="stat"><b>${num(n.meals.dinner)}</b><span>Dinner</span></div>
      <div class="stat"><b>${num(n.meals.snacks)}</b><span>Snacks</span></div>
    </div>
    <h3 style="margin-top:16px">Example day, about 1,580 kcal</h3>
    <ul class="plain">
      <li><b>Breakfast:</b> 50 g oats, 1 scoop whey and a banana. About 415 kcal.</li>
      <li><b>Lunch:</b> 150 g chicken, 150 g brown rice and 150 g vegetables. About 465 kcal.</li>
      <li><b>Snack:</b> 200 g Greek yoghurt with 100 g berries. About 165 kcal.</li>
      <li><b>Dinner:</b> 150 g salmon, 200 g sweet potato and vegetables. About 530 kcal.</li>
    </ul>
    <p class="small muted">To reach your own number, keep the protein portions and change the carbs and fats. Add or remove rice, potato, oats, olive oil or nuts until the day lands inside your range.</p>
  </section>
  <section class="card"><h2>Eat these</h2>
    <p class="small muted">Build most meals from a protein, a carb and a vegetable. Values are approximate.</p>
    <div class="tblwrap"><table class="tbl"><thead><tr><th>Food</th><th class="n">kcal</th><th class="n">Protein g</th></tr></thead><tbody>${eatRows}</tbody></table></div>
  </section>
  <section class="card"><h2>Limit these</h2>
    <p class="small muted">You do not need to ban them. Keep them to one small serving a week, or skip them for the month.</p>
    <div class="tblwrap"><table class="tbl"><thead><tr><th>Food</th><th class="n">kcal</th></tr></thead><tbody>${limRows}</tbody></table></div>
  </section>
  <section class="card"><h2>Daily habits</h2>
    <ul class="plain">
      <li>Drink 2 to 3 litres of water.</li>
      <li>Sleep 7 to 9 hours. Poor sleep cuts fat loss and strength.</li>
      <li>Eat protein at every meal, about 25 to 40 g each.</li>
      <li>Weigh yourself on the same morning each week, after the toilet and before eating.</li>
      <li>Stay consistent about 80% of the time. One flexible meal a week is fine.</li>
    </ul></section>
  </div>`;
}

const lk=(w,sid,i,s)=>`${w}|${sid}|${i}|${s}`;
function viewTracker(){
  const p=S.profile, plan=planFor(p.days);
  if(!ui.sid||!plan.some(d=>d.sid===ui.sid))ui.sid=plan[0].sid;
  const wk=WEEKS[ui.week-1], s=SESS[ui.sid];
  const weeks=WEEKS.map(w=>`<button type="button" class="pill" data-week="${w.w}" aria-pressed="${w.w===ui.week}">Week ${w.w}</button>`).join('');
  const sessBtns=plan.map(d=>{const q=SESS[d.sid];return `<button type="button" class="pill" data-sid="${d.sid}" aria-pressed="${d.sid===ui.sid}">${plateHTML(q.plate)}${q.name}</button>`;}).join('');
  let body;
  if(!s.ex.length){
    const dk=`${ui.week}|${ui.sid}`;
    body=`<p>${s.note}</p><label class="check" style="margin-top:14px"><input type="checkbox" data-done="${dk}" ${S.done[dk]?'checked':''}> Completed this week</label>`;
  }else{
    body=s.ex.map(([k,sets,lo,hi],i)=>{
      const e=EX[k];
      const prev=[];
      for(let j=0;j<sets;j++)prev.push(S.log[lk(ui.week-1,ui.sid,i,j)]);
      const sg=ui.week>1?suggest(prev,e,{sets,lo,hi}):null;
      const tip=sg||(ui.week===1?'Start light. Pick a weight where you could do 3 more reps than the top of the range, then build from there.':'No log from last week. Pick a weight that matches this week\'s effort: '+wk.rir.toLowerCase()+'.');
      const rows=[];
      for(let j=0;j<sets;j++){
        const cur=S.log[lk(ui.week,ui.sid,i,j)]||{};
        const pv=prev[j]||{};
        rows.push(`<span class="sn">${j+1}</span>
          <input class="num" type="number" inputmode="decimal" step="0.5" min="0" aria-label="${e.n} set ${j+1} weight in kg" data-k="${lk(ui.week,ui.sid,i,j)}" data-f="kg" placeholder="${pv.kg!==undefined&&pv.kg!==''?pv.kg:'0'}" value="${cur.kg!==undefined?cur.kg:''}">
          <input class="num" type="number" inputmode="numeric" step="1" min="0" aria-label="${e.n} set ${j+1} ${e.u==='s'?'seconds':'reps'}" data-k="${lk(ui.week,ui.sid,i,j)}" data-f="reps" placeholder="${pv.reps!==undefined&&pv.reps!==''?pv.reps:lo}" value="${cur.reps!==undefined?cur.reps:''}">`);
      }
      return `<article class="ex"><div class="exhead"><h4>${e.n}</h4><span class="tag">${sets} x ${lo}-${hi}${e.u==='s'?' s':' reps'}</span></div>
        <p class="cue">${e.cue}</p>${howHTML(k)}<p class="sug">${tip}</p>
        <div class="sets"><span class="h">Set</span><span class="h">kg</span><span class="h">${e.u==='s'?'Seconds':'Reps'}</span>${rows.join('')}</div></article>`;
    }).join('');
  }
  const start=p.weight;
  return `<div class="stack">
  <section class="card">
    <div class="pills" role="group" aria-label="Week">${weeks}</div>
    <h2>Week ${wk.w}: ${wk.t}</h2>
    <p>${wk.rir}. Finisher at ${wk.fin}.</p>
    <div><label class="lbl" for="bw">Weigh-in for week ${wk.w} (kg)</label>
      <input class="in" style="max-width:200px" id="bw" type="number" inputmode="decimal" step="0.1" min="30" max="300" placeholder="${fmt(start)}" value="${S.bw[ui.week]!==undefined?S.bw[ui.week]:''}">
      <p class="small muted" id="bwnote" style="margin-top:6px"></p></div>
  </section>
  <section class="card">
    <div class="pills" role="group" aria-label="Session">${sessBtns}</div>
    <h2>${s.name}</h2>
    <p class="small muted">Grey numbers show last week. For dumbbell lifts, log the weight of one dumbbell.</p>
    <div>${body}</div>
  </section>
  <section class="card"><h2>Weekly volume</h2>
    <p class="small muted">Weight x reps added up over every logged set. It should climb week by week.</p>
    <div id="vol"></div></section>
  </div>`;
}

// tracker helpers
function volumes(){
  const v=[0,0,0,0,0];
  for(const k in S.log){
    const [w,sid,i]=k.split('|');
    const ex=SESS[sid]&&SESS[sid].ex[+i];
    if(!ex||EX[ex[0]].u==='s')continue;
    const kg=parseFloat(S.log[k].kg), reps=parseFloat(S.log[k].reps);
    if(kg>0&&reps>0&&v[+w]!==undefined)v[+w]+=kg*reps;
  }
  return v;
}
function updateVol(){
  const el=document.getElementById('vol'); if(!el)return;
  const v=volumes(), max=Math.max(...v.slice(1));
  if(!max){el.innerHTML='<p class="muted">Log a weight and reps to see your volume here.</p>';return;}
  el.innerHTML=[1,2,3,4].map(w=>`<div class="bar"><span class="mono">Week ${w}</span><div class="track"><div class="fill" style="width:${(v[w]/max*100).toFixed(1)}%"></div></div><span class="mono" style="text-align:right">${num(v[w])} kg</span></div>`).join('');
}
function updateBW(){
  const el=document.getElementById('bwnote'); if(!el)return;
  const ws=Object.keys(S.bw).map(Number).filter(w=>parseFloat(S.bw[w])>0).sort((a,b)=>a-b);
  if(!ws.length){el.textContent=`Starting weight: ${fmt(S.profile.weight)} kg.`;return;}
  const last=parseFloat(S.bw[ws[ws.length-1]]), d=last-S.profile.weight;
  el.textContent=`Starting weight: ${fmt(S.profile.weight)} kg. Latest: ${fmt(last)} kg (${d>0?'+':d<0?'−':''}${fmt(Math.abs(Math.round(d*10)/10))} kg).`;
}

// navigation
function render(){
  document.querySelectorAll('#tabs button').forEach(b=>{
    const t=b.dataset.go;
    b.setAttribute('aria-selected',String(t===ui.tab));
    b.disabled=!S.profile&&t!=='profile';
  });
  $v().innerHTML=ui.tab==='profile'?viewProfile():ui.tab==='plan'?viewPlan():ui.tab==='food'?viewFood():viewTracker();
  if(ui.tab==='tracker'){updateVol();updateBW();}
}
function go(t){
  if(!S.profile&&t!=='profile')return;
  ui.tab=t;render();
  try{document.getElementById('tabs').scrollIntoView({block:'start'});}catch(e){}
}

document.addEventListener('click',e=>{
  const g=e.target.closest('[data-go]'); if(g){go(g.dataset.go);return;}
  const w=e.target.closest('[data-week]'); if(w){ui.week=+w.dataset.week;render();return;}
  const s=e.target.closest('[data-sid]'); if(s){ui.sid=s.dataset.sid;render();return;}
  const a=e.target.closest('[data-act]'); if(!a)return;
  if(a.dataset.act==='askwipe'){ui.confirm=true;render();}
  if(a.dataset.act==='nowipe'){ui.confirm=false;render();}
  if(a.dataset.act==='wipe'){S={profile:null,log:{},bw:{},done:{}};try{localStorage.removeItem(KEY);}catch(x){}ui.confirm=false;ui.tab='profile';render();}
});
document.addEventListener('input',e=>{
  const el=e.target;
  if(el.dataset&&el.dataset.k){
    const o=S.log[el.dataset.k]||(S.log[el.dataset.k]={});
    if(el.value==='')delete o[el.dataset.f];else o[el.dataset.f]=el.value;
    if(!Object.keys(o).length)delete S.log[el.dataset.k];
    save();updateVol();
  }else if(el.id==='bw'){
    if(el.value==='')delete S.bw[ui.week];else S.bw[ui.week]=el.value;
    save();updateBW();
  }
});
document.addEventListener('change',e=>{
  const el=e.target;
  if(el.dataset&&el.dataset.done){if(el.checked)S.done[el.dataset.done]=1;else delete S.done[el.dataset.done];save();}
  if(el.name==='days'){const h=document.getElementById('hint');if(h)h.textContent=HINT[+el.value];}
});
document.addEventListener('submit',e=>{
  if(e.target.id!=='f')return;
  e.preventDefault();
  const f=e.target, sx=f.elements.sex.value, dy=f.elements.days.value;
  const v={sex:sx,age:parseFloat(f.age.value),height:parseFloat(f.height.value),weight:parseFloat(f.weight.value),email:f.email.value.trim(),days:dy?+dy:0};
  const errs=validateProfile(v), box=document.getElementById('errs');
  if(errs.length){box.innerHTML='<div class="errs"><ul>'+errs.map(x=>`<li>${x}</li>`).join('')+'</ul></div>';return;}
  S.profile=v;save();ui.tab='plan';render();
  try{document.getElementById('tabs').scrollIntoView({block:'start'});}catch(x){}
});

load();
if(S.profile)ui.tab='plan';
render();
</script>

</body></html>
