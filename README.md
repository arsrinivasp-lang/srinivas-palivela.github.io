[index.html](https://github.com/user-attachments/files/25840290/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Srinivas Palivela — Project Manager</title>

<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:       #FFFFFF;
  --bg2:      #F2F2F7;
  --bg3:      #F9F9FB;
  --border:   rgba(0,0,0,0.07);
  --border2:  rgba(0,0,0,0.04);
  --t1:       #1C1C1E;
  --t2:       #48484A;
  --t3:       #8A8A8E;
  --t4:       #C7C7CC;
  --blue:     #1E7FE1;
  --blue-dk:  #0A6AD4;
  --blue-lt:  #EAF3FD;
  --blue-mid: rgba(30,127,225,0.10);
  --gold:     #B8842A;
  --gold-lt:  #FEF6EA;
  --radius:   18px;
  --radius-sm:11px;
  --shadow:   0 1px 8px rgba(0,0,0,0.05),0 3px 16px rgba(0,0,0,0.04);
  --shadow-md:0 4px 24px rgba(0,0,0,0.07),0 1px 4px rgba(0,0,0,0.04);
  --shadow-lg:0 12px 48px rgba(0,0,0,0.09),0 2px 8px rgba(0,0,0,0.04);
}

html{scroll-behavior:smooth}
body{
  font-family:-apple-system,'SF Pro Text','Helvetica Neue',Arial,sans-serif;
  background:var(--bg2);
  color:var(--t1);
  overflow-x:hidden;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
}

/* ── TOPBAR ──────────────────────────────────────────── */
.topbar{
  position:fixed;top:0;left:0;right:0;z-index:200;
  background:rgba(242,242,247,0.9);
  backdrop-filter:saturate(200%) blur(30px);
  -webkit-backdrop-filter:saturate(200%) blur(30px);
  border-bottom:1px solid rgba(0,0,0,0.06);
  height:56px;
  display:flex;align-items:center;
  padding:0 44px;gap:2px;
}
.topbar-logo{
  font-size:15px;font-weight:700;
  color:var(--t1);
  margin-right:auto;letter-spacing:-.2px;
}
.tab-btn{
  background:none;border:none;cursor:pointer;
  color:var(--t3);
  font-size:13px;font-weight:500;
  padding:7px 15px;border-radius:30px;
  transition:all .18s;
  letter-spacing:-.1px;
}
.tab-btn:hover{color:var(--t2);background:rgba(0,0,0,0.04)}
.tab-btn.active{
  background:var(--bg);
  color:var(--blue);
  font-weight:600;
  box-shadow:0 1px 6px rgba(0,0,0,0.08);
}

/* ── PANELS ──────────────────────────────────────────── */
.panel{display:none;min-height:100vh;padding-top:56px}
.panel.active{display:block}

/* ── SHARED FOOTER ───────────────────────────────────── */
.foot{
  background:rgba(242,242,247,0.8);
  border-top:1px solid rgba(0,0,0,0.06);
  padding:28px 44px;
  display:flex;justify-content:space-between;align-items:center;
}
.foot-name{font-size:13px;font-weight:500;color:var(--t3)}
.foot-links{display:flex;gap:20px}
.foot-links a{color:var(--t4);text-decoration:none;font-size:13px;transition:color .18s}
.foot-links a:hover{color:var(--blue)}

@keyframes fadeUp{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:.4}}

/* ════════════════════════════════════════════════════════
   HOME
════════════════════════════════════════════════════════ */
.home-wrap{
  max-width:980px;margin:0 auto;
  padding:80px 48px 72px;
  min-height:calc(100vh - 56px);
  display:flex;flex-direction:column;justify-content:center;
}

.avail-pill{
  display:inline-flex;align-items:center;gap:7px;
  background:var(--blue-lt);
  color:var(--blue);
  font-size:12px;font-weight:600;
  padding:6px 14px;border-radius:30px;
  margin-bottom:32px;
  width:fit-content;
  animation:fadeUp .6s ease both;
}
.avail-dot{
  width:7px;height:7px;border-radius:50%;
  background:var(--blue);animation:pulse 2s infinite;
}

.home-name{
  font-size:clamp(44px,6vw,80px);
  font-weight:700;
  color:var(--t1);
  line-height:1.05;
  letter-spacing:-2.5px;
  animation:fadeUp .6s .06s ease both;
}
.home-name em{
  font-style:normal;
  color:var(--blue);
}

.home-role{
  font-size:18px;font-weight:400;
  color:var(--t3);
  margin-top:18px;
  line-height:1.6;
  animation:fadeUp .6s .12s ease both;
}
.home-role strong{color:var(--t2);font-weight:600}

.home-divider{
  width:40px;height:2px;
  background:var(--blue);
  margin:28px 0;
  border-radius:2px;
  animation:fadeUp .6s .18s ease both;
}

.home-summary{
  font-size:17px;font-weight:400;
  color:var(--t2);line-height:1.8;
  max-width:620px;
  animation:fadeUp .6s .22s ease both;
}
.home-summary em{color:var(--blue);font-style:normal;font-weight:600}

/* Stat cards */
.home-cards{
  display:grid;grid-template-columns:repeat(4,1fr);
  gap:14px;margin-top:52px;
  animation:fadeUp .6s .32s ease both;
}
.h-card{
  background:var(--bg);
  border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);
  padding:22px 20px;
  box-shadow:var(--shadow);
  transition:all .22s;
}
.h-card:hover{
  box-shadow:var(--shadow-md);
  transform:translateY(-3px);
}
.h-card-icon{margin-bottom:12px;display:flex;align-items:center;}.h-card-icon svg{width:30px;height:30px;}
.h-card-val{
  font-family:-apple-system,'SF Pro Display','Helvetica Neue',sans-serif;
  font-size:26px;font-weight:700;
  color:var(--t1);line-height:1;
}
.h-card-lbl{
  font-size:12px;font-weight:500;
  color:var(--t3);margin-top:5px;line-height:1.4;
}

/* Bottom strip */
.home-strip{
  display:flex;gap:40px;
  margin-top:48px;padding-top:36px;
  border-top:1px solid var(--border);
  animation:fadeUp .6s .4s ease both;
}
.strip-item-num{
  font-family:-apple-system,'SF Pro Display','Helvetica Neue',sans-serif;
  font-size:32px;font-weight:700;
  color:var(--t1);line-height:1;
}
.strip-item-lbl{
  font-size:11px;font-weight:600;
  color:var(--t4);text-transform:uppercase;
  letter-spacing:1px;margin-top:4px;
}

/* ════════════════════════════════════════════════════════
   SHARED SECTION WRAPPER
════════════════════════════════════════════════════════ */
.section-hero{
  background:var(--bg);
  border-bottom:1px solid rgba(0,0,0,0.06);
  padding:56px 48px 48px;
}
.section-hero .sh-label{
  font-size:11px;font-weight:700;
  letter-spacing:1.8px;text-transform:uppercase;
  color:var(--blue);margin-bottom:12px;
}
.section-hero h1{
  font-size:clamp(30px,4vw,48px);
  font-weight:700;color:var(--t1);
  line-height:1.1;letter-spacing:-.5px;
}
.section-hero h1 em{font-style:normal;color:var(--blue)}
.section-hero p{
  font-size:16px;color:var(--t3);
  margin-top:12px;max-width:520px;line-height:1.72;
}

.section-body{max-width:1080px;margin:0 auto;padding:56px 48px}

/* ════════════════════════════════════════════════════════
   ABOUT
════════════════════════════════════════════════════════ */
.about-grid{display:grid;grid-template-columns:1.35fr 1fr;gap:64px;align-items:start}

.story p{font-size:15.5px;line-height:1.88;color:var(--t2);margin-bottom:20px}
.story p strong{color:var(--t1);font-weight:700}
.pull-quote{
  font-size:18px;font-style:italic;font-weight:400;
  color:var(--t3);line-height:1.6;
  border-left:2.5px solid var(--blue);
  padding:4px 0 4px 20px;
  margin:28px 0;
}

.sidebar{display:flex;flex-direction:column;gap:14px}
.s-card{
  background:var(--bg);
  border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);
  padding:22px 22px;
  box-shadow:var(--shadow);
  transition:box-shadow .2s,transform .2s;
}
.s-card:hover{box-shadow:var(--shadow-md);transform:translateY(-3px)}
.s-card-head{
  display:flex;align-items:center;gap:10px;
  margin-bottom:14px;
}
.s-card-icon{
  width:38px;height:38px;border-radius:10px;
  background:var(--blue-lt);
  display:flex;align-items:center;justify-content:center;
  flex-shrink:0;
}
.s-card-icon svg{width:20px;height:20px;}
.s-card h4{
  font-size:12px;font-weight:700;
  letter-spacing:1.2px;text-transform:uppercase;
  color:var(--t3);
}
.s-card p{font-size:13.5px;color:var(--t3);line-height:1.65}
.s-card p strong{color:var(--t2)}

.cert-list{display:flex;flex-direction:column;gap:0}
.cert-item{
  padding:10px 0;
  border-bottom:1px solid var(--border2);
}
.cert-item:last-child{border-bottom:none;padding-bottom:0}
.cert-item-name{
  font-size:13px;font-weight:600;
  color:var(--t1);margin-bottom:2px;
}
.cert-item-meta{font-size:11.5px;color:var(--t3)}
.cert-new-tag{
  display:inline-block;
  background:var(--blue-lt);color:var(--blue);
  font-size:10px;font-weight:700;
  padding:2px 7px;border-radius:20px;
  margin-left:6px;letter-spacing:.3px;
  vertical-align:middle;
}

.loc-pill{
  display:inline-flex;align-items:center;gap:6px;
  background:var(--gold-lt);
  border:1px solid rgba(176,125,47,.2);
  color:var(--gold);
  font-size:12.5px;font-weight:600;
  padding:7px 16px;border-radius:30px;
  margin-top:20px;
}

/* ════════════════════════════════════════════════════════
   EXPERIENCE
════════════════════════════════════════════════════════ */
.exp-body{max-width:780px;margin:0 auto;padding:56px 48px}

.timeline{position:relative;padding-left:28px}
.timeline::before{
  content:'';position:absolute;
  left:0;top:8px;bottom:0;width:1.5px;
  background:linear-gradient(to bottom,var(--blue),rgba(0,113,227,.15),transparent);
}
.tl-item{
  position:relative;margin-bottom:56px;
  opacity:0;transform:translateY(12px);
  transition:all .45s ease;
}
.tl-item.vis{opacity:1;transform:translateY(0)}
.tl-dot{
  position:absolute;left:-35px;top:8px;
  width:14px;height:14px;border-radius:50%;
  background:var(--blue);
  border:2.5px solid var(--bg);
  box-shadow:0 0 0 3px var(--blue-lt);
}
.tl-dot.old{background:var(--t4);box-shadow:0 0 0 3px var(--bg2)}

.tl-date{
  font-size:11px;font-weight:700;
  letter-spacing:1.2px;text-transform:uppercase;
  color:var(--blue);margin-bottom:6px;
}
.tl-role{
  font-size:22px;font-weight:700;
  color:var(--t1);line-height:1.2;margin-bottom:3px;
}
.tl-company{font-size:14px;font-weight:600;color:var(--t3);margin-bottom:4px}
.promo-tag{
  display:inline-block;
  background:var(--gold-lt);border:1px solid rgba(176,125,47,.2);
  color:var(--gold);font-size:11px;font-weight:700;
  padding:3px 11px;border-radius:20px;margin-bottom:14px;
}
.tl-body{font-size:14.5px;color:var(--t2);line-height:1.8;margin-bottom:14px}
.tl-ul{list-style:none;margin-bottom:16px}
.tl-ul li{
  font-size:13.5px;color:var(--t2);line-height:1.7;
  padding:4px 0 4px 18px;position:relative;
}
.tl-ul li::before{
  content:'';position:absolute;left:0;top:14px;
  width:5px;height:5px;border-radius:50%;
  background:var(--blue);
}
.tl-ul li strong{color:var(--t1);font-weight:700}

.tl-achieve{
  display:inline-flex;align-items:flex-start;gap:9px;
  background:var(--blue-lt);
  border:1px solid rgba(0,113,227,.15);
  color:var(--blue);
  font-size:13px;font-weight:500;
  padding:10px 15px;border-radius:var(--radius-sm);
  margin-top:4px;line-height:1.55;
}
.proj-tags{display:flex;flex-wrap:wrap;gap:7px;margin-top:14px}
.proj-tag{
  background:var(--bg2);border:1px solid var(--border);
  color:var(--t3);font-size:12px;font-weight:600;
  padding:5px 13px;border-radius:20px;
}

/* ════════════════════════════════════════════════════════
   PROJECTS
════════════════════════════════════════════════════════ */
.proj-total{
  display:flex;align-items:center;gap:24px;
  background:var(--blue);
  border-radius:var(--radius);
  padding:28px 36px;margin-bottom:32px;
}
.proj-total-num{
  font-size:44px;font-weight:700;
  color:rgba(255,255,255,0.95);line-height:1;
  white-space:nowrap;
}
.proj-total-txt h3{font-size:16px;font-weight:700;color:rgba(255,255,255,0.95);margin-bottom:3px}
.proj-total-txt p{font-size:13px;color:rgba(255,255,255,0.65)}

.proj-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.p-card{
  background:var(--bg);
  border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);
  padding:28px 24px;
  box-shadow:var(--shadow);
  transition:all .22s;
  position:relative;overflow:hidden;
}
.p-card::before{
  content:'';position:absolute;
  top:0;left:0;right:0;height:3px;
  background:var(--blue);
  transform:scaleX(0);transform-origin:left;
  transition:transform .25s;
}
.p-card:hover{box-shadow:var(--shadow-lg);transform:translateY(-4px)}
.p-card:hover::before{transform:scaleX(1)}
.p-val{
  font-family:-apple-system,'SF Pro Display','Helvetica Neue',sans-serif;
  font-size:32px;font-weight:700;
  color:var(--t1);line-height:1;margin-bottom:6px;
}
.p-name{font-size:14px;font-weight:700;color:var(--t1);margin-bottom:4px}
.p-type{font-size:11.5px;font-weight:600;color:var(--t4);text-transform:uppercase;letter-spacing:.8px;margin-bottom:14px}
.p-desc{font-size:13px;color:var(--t3);line-height:1.65}
.p-badge{
  display:inline-block;margin-top:14px;
  background:var(--blue-lt);color:var(--blue);
  font-size:11px;font-weight:700;
  padding:4px 12px;border-radius:20px;
}
.proj-note{
  background:var(--bg2);border:1px solid var(--border);
  border-radius:var(--radius);padding:24px 28px;margin-top:20px;
}
.proj-note h4{font-size:13px;font-weight:700;color:var(--t2);margin-bottom:6px}
.proj-note p{font-size:13px;color:var(--t3);line-height:1.7}
.proj-note p strong{color:var(--t2)}

/* ════════════════════════════════════════════════════════
   SKILLS
════════════════════════════════════════════════════════ */
.sk-label{
  font-size:12px;font-weight:700;
  letter-spacing:1.3px;text-transform:uppercase;
  color:var(--blue);margin-bottom:10px;margin-top:52px;
}
.sk-label:first-child{margin-top:0}
.sk-sub{font-size:15px;color:var(--t3);margin-bottom:24px}

.sk-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-bottom:8px}
.sk-card{
  background:var(--bg);border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);padding:24px 20px;
  box-shadow:var(--shadow);
  transition:all .22s;
}
.sk-card:hover{box-shadow:var(--shadow-md);transform:translateY(-3px)}
.sk-card-icon{
  width:44px;height:44px;border-radius:12px;
  background:var(--blue-lt);
  display:flex;align-items:center;justify-content:center;
  margin-bottom:14px;
}
.sk-card-icon svg{width:24px;height:24px;}
.sk-card h4{font-size:14px;font-weight:700;color:var(--t1);margin-bottom:6px}
.sk-card p{font-size:12.5px;color:var(--t3);line-height:1.6}

/* Cert cards */
.cert-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.ck{
  background:var(--bg);border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);padding:20px 18px;
  box-shadow:var(--shadow);
  transition:all .22s;
}
.ck:hover{box-shadow:var(--shadow-md);transform:translateY(-3px)}
.ck-icon{
  width:40px;height:40px;border-radius:10px;
  background:var(--blue-lt);
  display:flex;align-items:center;justify-content:center;
  margin-bottom:12px;
}
.ck-icon svg{width:22px;height:22px;}
.ck-title{font-size:13.5px;font-weight:700;color:var(--t1);margin-bottom:3px;line-height:1.4}
.ck-issuer{font-size:12px;font-weight:600;color:var(--blue);margin-bottom:2px}
.ck-date{font-size:11.5px;color:var(--t3)}
.ck-id{font-size:10.5px;color:var(--t4);margin-top:3px;font-family:monospace}
.ck-new{
  display:inline-block;margin-top:8px;
  background:var(--blue-lt);color:var(--blue);
  font-size:10px;font-weight:700;
  padding:2px 8px;border-radius:20px;
}

/* Software */
.sw-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:14px}
.sw-cat{
  background:var(--bg);border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);padding:22px;
  box-shadow:var(--shadow);
}
.sw-cat h5{
  font-size:11px;font-weight:700;
  letter-spacing:1.2px;text-transform:uppercase;
  color:var(--t3);margin-bottom:12px;
}
.sw-tags{display:flex;flex-wrap:wrap;gap:7px}
.sw-tag{
  background:var(--bg2);border:1px solid var(--border2);
  color:var(--t2);font-size:12.5px;font-weight:500;
  padding:5px 13px;border-radius:20px;transition:all .18s;
}
.sw-tag:hover{background:var(--blue-lt);color:var(--blue);border-color:rgba(0,113,227,.2)}
.sw-tag.hi{background:var(--blue-lt);color:var(--blue);border-color:rgba(0,113,227,.2);font-weight:700}

/* Competency chips */
.comp-wrap{display:flex;flex-wrap:wrap;gap:10px;margin-top:8px}
.comp-chip{
  display:flex;align-items:center;gap:8px;
  background:var(--bg);border:1px solid rgba(0,0,0,0.06);
  color:var(--t2);font-size:13px;font-weight:500;
  padding:10px 18px;border-radius:30px;
  box-shadow:0 1px 4px rgba(0,0,0,0.04);
  transition:all .18s;
}
.comp-chip::before{content:'✓';color:var(--blue);font-weight:800;font-size:12px}
.comp-chip:hover{background:var(--blue-lt);color:var(--blue);border-color:rgba(0,113,227,.2)}

/* ════════════════════════════════════════════════════════
   CONTACT
════════════════════════════════════════════════════════ */
.ct-body{max-width:800px;margin:0 auto;padding:56px 48px}

.ct-cards{display:grid;grid-template-columns:repeat(2,1fr);gap:14px;margin-bottom:32px}
.ct-card{
  background:var(--bg);border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);padding:26px 24px;
  display:flex;align-items:flex-start;gap:16px;
  box-shadow:var(--shadow);
  transition:all .22s;
}
.ct-card:hover{box-shadow:var(--shadow-md);transform:translateY(-3px)}
.ct-icon{
  width:48px;height:48px;border-radius:12px;
  background:var(--blue-lt);
  display:flex;align-items:center;justify-content:center;
  flex-shrink:0;
}
.ct-icon svg{width:24px;height:24px;}
.ct-card h4{
  font-size:11px;font-weight:700;
  letter-spacing:1.2px;text-transform:uppercase;
  color:var(--t4);margin-bottom:5px;
}
.ct-card a{
  font-size:15px;font-weight:600;
  color:var(--blue);text-decoration:none;
}
.ct-card a:hover{text-decoration:underline}
.ct-card .ct-plain{font-size:15px;font-weight:600;color:var(--t1)}
.ct-card .ct-sub{font-size:12.5px;color:var(--t3);margin-top:3px}

.open-box{
  background:var(--bg);border:1px solid rgba(0,0,0,0.05);
  border-radius:var(--radius);padding:36px;margin-bottom:20px;
  box-shadow:var(--shadow);
}
.open-box h3{
  font-family:-apple-system,'SF Pro Display','Helvetica Neue',sans-serif;
  font-size:24px;font-weight:700;color:var(--t1);margin-bottom:6px;
}
.open-box .ob-sub{font-size:14px;color:var(--t3);margin-bottom:18px}
.role-tags{display:flex;flex-wrap:wrap;gap:9px;margin-bottom:24px}
.role-tag{
  background:var(--bg2);border:1px solid var(--border);
  color:var(--t2);font-size:14px;font-weight:500;
  padding:10px 20px;border-radius:30px;
}
.role-tag-primary{
  background:var(--blue-lt);
  border-color:rgba(30,127,225,0.2);
  color:var(--blue);
  font-weight:700;
}
.loc-tags{display:flex;flex-wrap:wrap;gap:9px}
.loc-tag{
  display:flex;align-items:center;gap:5px;
  background:var(--gold-lt);
  border:1px solid rgba(176,125,47,.18);
  color:var(--gold);font-size:13px;font-weight:600;
  padding:7px 16px;border-radius:30px;
}

.avail-bar{
  background:var(--blue-lt);
  border:1px solid rgba(0,113,227,.15);
  border-radius:var(--radius-sm);
  padding:16px 20px;
  display:flex;align-items:center;gap:12px;
  font-size:14px;color:var(--t2);
}
.avail-bar strong{color:var(--t1)}

/* ── RESPONSIVE ──────────────────────────────────────── */
@media(max-width:900px){
  .home-wrap,.section-hero,.section-body,.exp-body,.ct-body{padding-left:20px;padding-right:20px}
  .topbar{padding:0 16px}
  .about-grid,.ct-cards{grid-template-columns:1fr}
  .proj-grid,.sk-grid,.cert-grid,.sw-grid{grid-template-columns:1fr 1fr}
  .home-cards{grid-template-columns:1fr 1fr}
  .home-strip{gap:24px}
  .topbar{padding:0 16px;gap:2px}
  .tab-btn{font-size:11px;padding:6px 10px}
  .foot{flex-direction:column;gap:12px;text-align:center}
}
@media(max-width:600px){
  .proj-grid,.sk-grid,.cert-grid,.sw-grid{grid-template-columns:1fr}
  .home-cards{grid-template-columns:1fr 1fr}
  .proj-total{flex-direction:column;gap:12px;padding:22px}
}
</style>
</head>
<body>

<!-- NAV -->
<nav class="topbar">
  <div class="topbar-logo">Srinivas Palivela</div>
  <button class="tab-btn active" onclick="showTab(this,'home')">Home</button>
  <button class="tab-btn" onclick="showTab(this,'about')">About</button>
  <button class="tab-btn" onclick="showTab(this,'experience')">Experience</button>
  <button class="tab-btn" onclick="showTab(this,'projects')">Projects</button>
  <button class="tab-btn" onclick="showTab(this,'skills')">Skills</button>
  <button class="tab-btn" onclick="showTab(this,'contact')">Contact</button>
</nav>

<!-- ══════════════════════════════════════════════════════
     HOME
═══════════════════════════════════════════════════════ -->
<div id="panel-home" class="panel active">
  <div class="home-wrap">
    <div class="avail-pill">
      <span class="avail-dot"></span>
      Available for new opportunities
    </div>

    <h1 class="home-name">Srinivas<br><em>Palivela</em></h1>

    <p class="home-role">
      <strong>Assistant Project Manager &nbsp;·&nbsp; Project Coordinator</strong><br>
      Construction &amp; Fit-Out &nbsp;·&nbsp; Offshore Coordination &nbsp;·&nbsp; AI Automation &nbsp;·&nbsp; Brisbane &amp; SEQ
    </p>

    <div class="home-divider"></div>

    <p class="home-summary">
      I deliver complex construction and fit-out projects across Queensland — managing everything from
      <em>factory scheduling</em> and <em>offshore supply chains</em> to <em>client sign-off</em>.
      Backed by a <em>Master of Architecture from UQ</em>, 4+ years of Tier 1 &amp; Tier 2
      experience, and <em>AI agents I've built myself</em> to make projects run smarter.
    </p>

    <div class="home-cards">
      <div class="h-card">
        <div class="h-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="4" x2="18" y2="32"/><line x1="18" y1="8" x2="30" y2="8"/><line x1="18" y1="8" x2="10" y2="14"/><line x1="30" y1="8" x2="30" y2="14"/><rect x="27" y="14" width="6" height="5" rx="1"/><line x1="18" y1="8" x2="22" y2="14"/><line x1="22" y1="14" x2="22" y2="20"/><rect x="9" y="28" width="18" height="4" rx="1.5"/><line x1="15" y1="28" x2="15" y2="24"/><line x1="21" y1="28" x2="21" y2="24"/><line x1="12" y1="24" x2="24" y2="24"/></svg></div>
        <div class="h-card-val">$18M+</div>
        <div class="h-card-lbl">Project portfolio coordinated</div>
      </div>
      <div class="h-card">
        <div class="h-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="18" cy="18" r="13"/><ellipse cx="18" cy="18" rx="5.5" ry="13"/><line x1="5" y1="18" x2="31" y2="18"/><path d="M6.5 12 Q18 15 29.5 12"/><path d="M6.5 24 Q18 21 29.5 24"/></svg></div>
        <div class="h-card-val">AU · CN · IN</div>
        <div class="h-card-lbl">Cross-border team coordination</div>
      </div>
      <div class="h-card">
        <div class="h-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="10" y="10" width="16" height="14" rx="3"/><line x1="14" y1="10" x2="14" y2="7"/><line x1="18" y1="10" x2="18" y2="7"/><line x1="22" y1="10" x2="22" y2="7"/><circle cx="14" cy="6" r="1.5"/><circle cx="18" cy="6" r="1.5"/><circle cx="22" cy="6" r="1.5"/><line x1="10" y1="15" x2="7" y2="15"/><line x1="10" y1="19" x2="7" y2="19"/><line x1="26" y1="15" x2="29" y2="15"/><line x1="26" y1="19" x2="29" y2="19"/><circle cx="7" cy="15" r="1.5"/><circle cx="7" cy="19" r="1.5"/><circle cx="29" cy="15" r="1.5"/><circle cx="29" cy="19" r="1.5"/><line x1="14" y1="24" x2="14" y2="30"/><line x1="22" y1="24" x2="22" y2="30"/><line x1="12" y1="30" x2="24" y2="30"/><circle cx="15" cy="17" r="1.5" fill="#1E7FE1" stroke="none"/><circle cx="21" cy="17" r="1.5" fill="#1E7FE1" stroke="none"/></svg></div>
        <div class="h-card-val">AI</div>
        <div class="h-card-lbl">Anthropic-certified · Building agents</div>
      </div>
      <div class="h-card">
        <div class="h-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 16 L18 9 L32 16 L18 23 Z"/><path d="M12 19.5 L12 27 Q18 30 24 27 L24 19.5"/><line x1="32" y1="16" x2="32" y2="24"/><circle cx="32" cy="25.5" r="1.5"/></svg></div>
        <div class="h-card-val">MArch</div>
        <div class="h-card-lbl">University of Queensland</div>
      </div>
    </div>

    <div class="home-strip">
      <div>
        <div class="strip-item-num">4+</div>
        <div class="strip-item-lbl">Years Experience</div>
      </div>
      <div>
        <div class="strip-item-num">6+</div>
        <div class="strip-item-lbl">Major Projects</div>
      </div>
      <div>
        <div class="strip-item-num">T1 &amp; T2</div>
        <div class="strip-item-lbl">Project Tiers</div>
      </div>
      <div>
        <div class="strip-item-num">2020</div>
        <div class="strip-item-lbl">UQ Graduate</div>
      </div>
    </div>
  </div>

  <footer class="foot">
    <div class="foot-name">Srinivas Palivela &nbsp;·&nbsp; Brisbane, QLD</div>
    <div class="foot-links">
      <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
      <a href="tel:0426928276">0426 928 276</a>
      <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">LinkedIn</a>
    </div>
  </footer>
</div>

<!-- ══════════════════════════════════════════════════════
     ABOUT
═══════════════════════════════════════════════════════ -->
<div id="panel-about" class="panel">
  <div class="section-hero">
    <div class="sh-label">Who I Am</div>
    <h1>From drawing board<br><em>to construction site.</em></h1>
    <p>A construction professional combining architectural design literacy, international coordination, and hands-on AI development — 4+ years of Tier 1 &amp; Tier 2 delivery across Queensland.</p>
  </div>

  <div class="section-body">
    <div class="about-grid">
      <div class="story">
        <p>I didn't start my career on a construction site — I started it behind a drawing board. After completing my <strong>Master of Architecture at the University of Queensland</strong>, I made a deliberate decision to move into construction project management, because I wanted to see things get built, not just designed.</p>

        <p>That decision led to 4+ years delivering <strong>Tier 1 and Tier 2 construction and fit-out projects</strong> across Queensland — from government correctional facilities and youth remand centres to airport kiosks, stadium fit-outs, and childcare centres.</p>

        <blockquote class="pull-quote">"I'm the person clients call when something goes sideways — and I've never missed a deadline because of it."</blockquote>

        <p>At <strong>Ingrams Australia</strong>, I progressed from APM to Project Manager in 18 months. Today I manage <strong>factory capacity plans</strong>, coordinate deliveries, run QA/QC, handle progress claims and variations, and keep documentation airtight in <strong>Aconex and Omtrak</strong>.</p>

        <p>More recently my scope expanded internationally. I now coordinate directly with <strong>manufacturers in China</strong> — managing drawing packages, approval workflows, quality requirements, and shipping logistics to align overseas production with Australian project timelines. I also manage a <strong>remote drafting team in India</strong>, briefing drafters, reviewing shop drawings, and integrating their output into live workflows without disrupting the program.</p>

        <p>Alongside this, I've been independently <strong>building AI automation agents using ChatGPT and Claude</strong> to streamline documentation, reporting, and internal workflows. I hold two <strong>Anthropic certifications (March 2026)</strong> backing this work up.</p>

        <p>My architecture background gives me a genuine edge — I read drawings fluently, catch constructability issues early, and bridge the gap between design intent and site delivery in a way most PMs simply can't.</p>

        <div class="loc-pill">📍 Brisbane · Gold Coast · Sunshine Coast · Ipswich · Toowoomba</div>
      </div>

      <div class="sidebar">
        <div class="s-card">
          <div class="s-card-head">
            <div class="s-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 16 L18 9 L32 16 L18 23 Z"/><path d="M12 19.5 L12 27 Q18 30 24 27 L24 19.5"/><line x1="32" y1="16" x2="32" y2="24"/><circle cx="32" cy="25.5" r="1.5"/></svg></div>
            <h4>Education</h4>
          </div>
          <p><strong>Master of Architecture (MArch)</strong><br>University of Queensland · 2018–2020 · AQF Level 9<br>Project Management, Contract Law, Procurement &amp; Tendering</p>
          <p style="margin-top:12px"><strong>Bachelor of Architecture (BArch)</strong><br>University of Mumbai · 2012–2017 · High Honours<br>Design, Construction Technology, Structural Systems</p>
        </div>

        <div class="s-card">
          <div class="s-card-head">
            <div class="s-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="6" width="18" height="24" rx="2"/><path d="M14 6 Q14 3 18 3 Q22 3 22 6"/><line x1="13" y1="14" x2="23" y2="14"/><line x1="13" y1="19" x2="23" y2="19"/><line x1="13" y1="24" x2="19" y2="24"/></svg></div>
            <h4>Certifications &amp; Licences</h4>
          </div>
          <div class="cert-list">
            <div class="cert-item">
              <div class="cert-item-name">AI Fluency Framework &amp; Foundations <span class="cert-new-tag">New</span></div>
              <div class="cert-item-meta">Anthropic · Mar 2026 · ID: h57vy2eijca6</div>
            </div>
            <div class="cert-item">
              <div class="cert-item-name">Claude 101 <span class="cert-new-tag">New</span></div>
              <div class="cert-item-meta">Anthropic · Mar 2026 · ID: vzo84jk8qthh</div>
            </div>
            <div class="cert-item">
              <div class="cert-item-name">Leveraging Generative AI for Project Management</div>
            </div>
            <div class="cert-item">
              <div class="cert-item-name">AI in Project Management</div>
            </div>
            <div class="cert-item">
              <div class="cert-item-name">White Card — Work Safely in Construction</div>
              <div class="cert-item-meta">CPCWHS1001 · 2024</div>
            </div>
            <div class="cert-item">
              <div class="cert-item-name">Architect Licence</div>
              <div class="cert-item-meta">India · CA/2018/91573</div>
            </div>
            <div class="cert-item">
              <div class="cert-item-name">TERI Sustainable Design Programme</div>
              <div class="cert-item-meta">2016</div>
            </div>
          </div>
        </div>

        <div class="s-card">
          <div class="s-card-head">
            <div class="s-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="18" cy="18" r="13"/><circle cx="18" cy="18" r="2"/><polygon points="18,8 20,17 18,16 16,17" fill="#1E7FE1" stroke="none"/><polygon points="18,28 16,19 18,20 20,19" fill="#AEAEB2" stroke="none"/></svg></div>
            <h4>What I'm Looking For</h4>
          </div>
          <p>Open to <strong>Assistant Project Manager</strong> roles across <strong>Construction</strong>, <strong>Fit-Out</strong>, and <strong>Product Development</strong> environments in South East Queensland.</p>
        </div>

        <div class="s-card">
          <div class="s-card-head">
            <div class="s-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 20 L10 14 L15 16 L21 12 L32 20"/><path d="M10 14 Q12 22 18 24 Q24 22 26 14"/><path d="M15 16 L18 19"/><path d="M21 12 L18 19"/><circle cx="18" cy="20" r="2"/><line x1="4" y1="20" x2="4" y2="26"/><line x1="32" y1="20" x2="32" y2="26"/></svg></div>
            <h4>How I Work</h4>
          </div>
          <p>I'm a communicator and systems thinker. Whether it's a factory in China, a drafting team in India, or a client on site — I keep every party aligned, informed, and moving forward.</p>
        </div>
      </div>
    </div>
  </div>

  <footer class="foot">
    <div class="foot-name">Srinivas Palivela &nbsp;·&nbsp; Brisbane, QLD</div>
    <div class="foot-links">
      <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
      <a href="tel:0426928276">0426 928 276</a>
      <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">LinkedIn</a>
    </div>
  </footer>
</div>

<!-- ══════════════════════════════════════════════════════
     EXPERIENCE
═══════════════════════════════════════════════════════ -->
<div id="panel-experience" class="panel">
  <div class="section-hero">
    <div class="sh-label">Career Journey</div>
    <h1>Experience</h1>
    <p>From graduate to Project Manager in four years — now coordinating internationally and building AI tools to work smarter.</p>
  </div>

  <div class="exp-body">
    <div class="timeline">

      <!-- PM -->
      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-date">May 2024 — Present</div>
        <div class="tl-role">Project Manager</div>
        <div class="promo-tag">⬆ Promoted from APM · 18 months</div>
        <div class="tl-company">Ingrams Australia Pty Ltd &nbsp;·&nbsp; Beenleigh, QLD</div>
        <p class="tl-body">Full end-to-end accountability across our construction and fit-out portfolio. My scope has grown to include international coordination — working directly with Chinese manufacturers and an offshore drafting team in India — alongside building AI automation tools to improve team efficiency.</p>
        <ul class="tl-ul">
          <li>Built and managed <strong>weekly factory capacity plans</strong> — allocating labour and machines across concurrent projects to hit production targets and avoid bottlenecks</li>
          <li>Coordinated with <strong>Chinese manufacturers</strong> — managing drawing packages, approval workflows, quality requirements, and shipping logistics to align overseas production with Australian timelines</li>
          <li>Managed <strong>remote drafting team in India</strong> — briefing drafters, reviewing shop drawings, and integrating output into live project workflows without program disruption</li>
          <li>Independently building <strong>AI automation agents using ChatGPT and Claude</strong> — streamlining document management, progress reporting, and internal workflows across active projects</li>
          <li>Organised all <strong>site deliveries</strong> — transport logistics, sequencing, site readiness alignment, and critical path protection</li>
          <li>Prepared <strong>fit-out estimations</strong> using Bluebeam and Microvellum — quantity take-offs, labour rates, material pricing, and subcontractor quotes</li>
          <li>Managed <strong>progress claims, variation approvals</strong>, and financial reporting end-to-end</li>
          <li>Administered all documentation via <strong>Aconex and Omtrak</strong> — O&amp;M manuals, Form 12, SDS, defect registers</li>
          <li>Directly supervised teams of up to <strong>5 assemblers and 10 installers</strong> on site</li>
          <li>Developed and maintained <strong>SWMS, Quality Plans, and Health Plans</strong> in full WHS compliance</li>
          <li>Implemented <strong>Green Star certification</strong> documentation and factory programs for the NPAV project</li>
        </ul>
        <div class="tl-achieve">⭐ Client praised fast-tracking of last-minute variations on Lady Ramsay — alternative products sourced, deadline met, repeat business earned</div>
        <div class="proj-tags">
          <span class="proj-tag">Lady Ramsay Child Care — $700K</span>
          <span class="proj-tag">Wacol Youth Remand — $850K</span>
          <span class="proj-tag">NPAV Project — $2.3M</span>
        </div>
      </div>

      <!-- APM -->
      <div class="tl-item">
        <div class="tl-dot"></div>
        <div class="tl-date">Nov 2022 — May 2024</div>
        <div class="tl-role">Assistant Project Manager</div>
        <div class="tl-company">Ingrams Australia Pty Ltd &nbsp;·&nbsp; Ipswich, QLD</div>
        <p class="tl-body">Supported senior PMs across high-compliance projects. The Southern Queensland Correctional Centre Stage 2 (~$15–18M) was the most demanding environment I've worked in — every document, delivery, and inspection had to be exactly right. Nominated for promotion after 18 months.</p>
        <ul class="tl-ul">
          <li>Assisted in developing <strong>weekly factory work schedules and capacity plans</strong></li>
          <li>Coordinated <strong>procurement and delivery logistics</strong> — transport, sequencing, supplier lead times, critical path milestones</li>
          <li>Conducted <strong>QA/QC site and factory inspections</strong>; managed O&amp;M and handover documentation</li>
          <li>Prepared all <strong>preconstruction safety documentation</strong>: SWMS, SDS, quality plans, health plans</li>
          <li>Managed <strong>drawing revisions, drafter coordination</strong>, and RFI management via Aconex</li>
          <li>Administered <strong>progress claims, variations, and defect rectification</strong> via Omtrak</li>
          <li>Supported <strong>client and consultant communications</strong> — meeting minutes, action tracking</li>
        </ul>
        <div class="tl-achieve">🏆 Nominated and promoted to Project Manager — recognised for initiative, reliability, and consistent delivery</div>
        <div class="proj-tags">
          <span class="proj-tag">SQCC Stage 2 — ~$15–18M</span>
          <span class="proj-tag">Fraser's Office Fit-Out</span>
          <span class="proj-tag">Cbus Stadium — $400K</span>
          <span class="proj-tag">Brisbane Airport Kiosk — $150–245K</span>
        </div>
      </div>

      <!-- Octeros -->
      <div class="tl-item">
        <div class="tl-dot old"></div>
        <div class="tl-date">Jun 2021 — Nov 2022</div>
        <div class="tl-role">Project Coordinator / Graduate Architect</div>
        <div class="tl-company">Octeros Cabinets &nbsp;·&nbsp; Bells Creek, QLD</div>
        <p class="tl-body">My first construction role — where I learned how a factory truly operates. I sat between the design office and the factory floor, developing production programs and shop drawings for high-specification joinery.</p>
        <ul class="tl-ul">
          <li>Developed <strong>factory production programs</strong> and documentation control</li>
          <li>Produced <strong>shop drawings</strong> for high-specification joinery to manufacturing tolerances</li>
          <li>Managed <strong>project submissions</strong> via Aconex</li>
          <li>Optimised <strong>workflows</strong> across design, production, and delivery teams</li>
        </ul>
      </div>

      <!-- CST -->
      <div class="tl-item">
        <div class="tl-dot old"></div>
        <div class="tl-date">Jan 2021 — Jul 2021</div>
        <div class="tl-role">Structural Draftsperson</div>
        <div class="tl-company">CST Consulting Engineers &nbsp;·&nbsp; Brisbane CBD, QLD</div>
        <p class="tl-body">Structural documentation for residential and commercial projects, working with engineers on code compliance and managing council submission processes.</p>
        <ul class="tl-ul">
          <li>Produced <strong>structural drawings</strong> for residential and commercial projects</li>
          <li>Supported <strong>code compliance</strong> checks and documentation</li>
          <li>Managed <strong>council submission</strong> processes for development approvals</li>
        </ul>
      </div>

      <!-- Enviroscape -->
      <div class="tl-item">
        <div class="tl-dot old"></div>
        <div class="tl-date">May 2017 — Apr 2018</div>
        <div class="tl-role">Architect — Licensed</div>
        <div class="tl-company">Enviroscape &nbsp;·&nbsp; Mumbai, India</div>
        <p class="tl-body">Led a team of three across urban development and commercial landscape projects from concept to council approval drawings. Contributed to the Smart City project in Hyderabad using QGIS.</p>
        <ul class="tl-ul">
          <li>Led a <strong>team of three</strong> across urban development projects</li>
          <li>Delivered <strong>council approval drawings and as-built documentation</strong></li>
          <li>Contributed to the <strong>Hyderabad Smart City project</strong> using QGIS</li>
          <li>Applied <strong>sustainable design</strong> and planting systems</li>
        </ul>
      </div>

    </div>
  </div>

  <footer class="foot">
    <div class="foot-name">Srinivas Palivela &nbsp;·&nbsp; Brisbane, QLD</div>
    <div class="foot-links">
      <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
      <a href="tel:0426928276">0426 928 276</a>
      <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">LinkedIn</a>
    </div>
  </footer>
</div>

<!-- ══════════════════════════════════════════════════════
     PROJECTS
═══════════════════════════════════════════════════════ -->
<div id="panel-projects" class="panel">
  <div class="section-hero">
    <div class="sh-label">Track Record</div>
    <h1>Key Projects</h1>
    <p>Government, commercial, aviation, and sports infrastructure — spanning Tier 1 &amp; Tier 2 across Queensland.</p>
  </div>

  <div class="section-body">
    <div class="proj-total">
      <div class="proj-total-num">$18M+</div>
      <div class="proj-total-txt">
        <h3>Total Portfolio Coordinated</h3>
        <p>Across Tier 1 &amp; Tier 2 construction and fit-out — government, commercial, aviation, sports infrastructure</p>
      </div>
    </div>

    <div class="proj-grid">
      <div class="p-card">
        <div class="p-val">~$15–18M</div>
        <div class="p-name">Southern Queensland Correctional Centre Stage 2</div>
        <div class="p-type">Government · High-Security · Construction</div>
        <p class="p-desc">Most compliance-intensive project I've worked on. Supported senior PM across procurement, scheduling, QA/QC, and full handover documentation in a high-security government environment.</p>
        <span class="p-badge">APM Role</span>
      </div>
      <div class="p-card">
        <div class="p-val">$2.3M</div>
        <div class="p-name">NPAV Project</div>
        <div class="p-type">Commercial · Joinery & Fit-Out · Green Star</div>
        <p class="p-desc">Full PM responsibility. Implemented Green Star documentation, streamlined factory programs, and coordinated delivery and installation to defect-free handover.</p>
        <span class="p-badge">PM Role</span>
      </div>
      <div class="p-card">
        <div class="p-val">$850K</div>
        <div class="p-name">Wacol Youth Remand Centre</div>
        <div class="p-type">Government · Compliance-Heavy · Fit-Out</div>
        <p class="p-desc">Government correctional fit-out delivered under budget through strategic supplier negotiation. Full factory scheduling, site delivery, WHS, and compliance documentation.</p>
        <span class="p-badge">PM Role</span>
      </div>
      <div class="p-card">
        <div class="p-val">$700K</div>
        <div class="p-name">Lady Ramsay Child Care Centre</div>
        <div class="p-type">Commercial · Client-Praised · Fast-Track</div>
        <p class="p-desc">Fast-tracked delivery under full PM responsibility. Last-minute design variations handled through creative procurement — on time, client praised, repeat business earned.</p>
        <span class="p-badge">PM Role</span>
      </div>
      <div class="p-card">
        <div class="p-val">$400K</div>
        <div class="p-name">Cbus Stadium Locker Room</div>
        <div class="p-type">Sports Infrastructure · Fit-Out</div>
        <p class="p-desc">Factory production and site delivery for a high-profile sports venue. Tight deadlines met through precise scheduling and sequencing to installation windows.</p>
        <span class="p-badge">APM Role</span>
      </div>
      <div class="p-card">
        <div class="p-val">$150–245K</div>
        <div class="p-name">Brisbane Airport Kiosk</div>
        <div class="p-type">Aviation · Fast-Track · Procurement</div>
        <p class="p-desc">Fast-tracked approvals and reduced manufacturing lead times within a highly regulated aviation environment. Material cost savings achieved through strategic procurement.</p>
        <span class="p-badge">APM → PM</span>
      </div>
    </div>

    <div class="proj-note">
      <h4>Earlier Experience</h4>
      <p>At <strong>Octeros Cabinets</strong> — factory production coordination and shop drawings for high-specification joinery. At <strong>CST Consulting Engineers</strong> — structural documentation for residential and commercial projects. At <strong>Enviroscape (India)</strong> — contributed to the Hyderabad Smart City project and delivered eight landscape architecture projects.</p>
    </div>
  </div>

  <footer class="foot">
    <div class="foot-name">Srinivas Palivela &nbsp;·&nbsp; Brisbane, QLD</div>
    <div class="foot-links">
      <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
      <a href="tel:0426928276">0426 928 276</a>
      <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">LinkedIn</a>
    </div>
  </footer>
</div>

<!-- ══════════════════════════════════════════════════════
     SKILLS
═══════════════════════════════════════════════════════ -->
<div id="panel-skills" class="panel">
  <div class="section-hero">
    <div class="sh-label">Capabilities</div>
    <h1>Skills &amp; Tools</h1>
    <p>Built through real projects — applied on site, in factories, across international supply chains, and in client meetings.</p>
  </div>

  <div class="section-body">

    <div class="sk-label">Core Competencies</div>
    <div class="sk-sub">What I bring to every project from day one.</div>
    <div class="sk-grid">
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="18" width="28" height="14" rx="1.5"/><path d="M4 18 L4 10 L13 18"/><path d="M13 18 L13 10 L22 18"/><path d="M22 18 L22 12 L32 18"/><rect x="8" y="22" width="5" height="10" rx="1"/><rect x="16" y="22" width="5" height="10" rx="1"/><rect x="24" y="24" width="4" height="4" rx="1"/></svg></div>
        <h4>Factory Scheduling &amp; Capacity Planning</h4>
        <p>Weekly production programs — allocating labour and machines, preventing bottlenecks, sequencing manufacturing to match site delivery windows.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="18" cy="18" r="13"/><ellipse cx="18" cy="18" rx="5.5" ry="13"/><line x1="5" y1="18" x2="31" y2="18"/><path d="M6.5 12 Q18 15 29.5 12"/><path d="M6.5 24 Q18 21 29.5 24"/></svg></div>
        <h4>Offshore &amp; International Coordination</h4>
        <p>Direct coordination with Chinese manufacturers and a remote drafting team in India — drawing approvals, logistics, quality, seamlessly integrated into live timelines.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="10" y="10" width="16" height="14" rx="3"/><line x1="14" y1="10" x2="14" y2="7"/><line x1="18" y1="10" x2="18" y2="7"/><line x1="22" y1="10" x2="22" y2="7"/><circle cx="14" cy="6" r="1.5"/><circle cx="18" cy="6" r="1.5"/><circle cx="22" cy="6" r="1.5"/><line x1="10" y1="15" x2="7" y2="15"/><line x1="10" y1="19" x2="7" y2="19"/><line x1="26" y1="15" x2="29" y2="15"/><line x1="26" y1="19" x2="29" y2="19"/><circle cx="7" cy="15" r="1.5"/><circle cx="7" cy="19" r="1.5"/><circle cx="29" cy="15" r="1.5"/><circle cx="29" cy="19" r="1.5"/><line x1="14" y1="24" x2="14" y2="30"/><line x1="22" y1="24" x2="22" y2="30"/><line x1="12" y1="30" x2="24" y2="30"/><circle cx="15" cy="17" r="1.5" fill="#1E7FE1" stroke="none"/><circle cx="21" cy="17" r="1.5" fill="#1E7FE1" stroke="none"/></svg></div>
        <h4>AI Process Automation</h4>
        <p>Building ChatGPT and Claude agents to automate document management and reporting. Anthropic-certified: AI Fluency Framework &amp; Claude 101 (Mar 2026).</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="5" y="12" width="26" height="19" rx="2.5"/><path d="M13 12 L13 8 Q13 6 18 6 Q23 6 23 8 L23 12"/><line x1="5" y1="20" x2="31" y2="20"/><line x1="16" y1="18" x2="20" y2="18"/><line x1="16" y1="22" x2="20" y2="22"/></svg></div>
        <h4>Client &amp; Stakeholder Communication</h4>
        <p>Primary client contact across all project stages — approvals, variations, RFI tracking, and relationships that generate repeat business.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><polygon points="6,30 6,8 28,30"/><line x1="6" y1="8" x2="28" y2="8"/><line x1="28" y1="8" x2="28" y2="30"/><line x1="10" y1="30" x2="10" y2="22"/><line x1="10" y1="22" x2="18" y2="22"/><line x1="14" y1="30" x2="14" y2="26"/><line x1="14" y1="26" x2="18" y2="26"/></svg></div>
        <h4>Fit-Out Estimation</h4>
        <p>Quantity take-offs, labour rates, material pricing, and subcontractor quotes using Bluebeam and Microvellum — tendering and pre-construction cost planning.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M18 4 L30 9 L30 20 Q30 28 18 32 Q6 28 6 20 L6 9 Z"/><polyline points="12,18 16,22 24,14"/></svg></div>
        <h4>Quality Assurance &amp; Compliance</h4>
        <p>ITPs, ITCs, factory and site inspections, SWMS, WHS documentation, NCC/BCA compliance — across government, commercial, and aviation environments.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 10 Q4 8 6 8 L14 8 L16 11 L30 11 Q32 11 32 13 L32 28 Q32 30 30 30 L6 30 Q4 30 4 28 Z"/><line x1="4" y1="16" x2="32" y2="16"/><line x1="11" y1="21" x2="25" y2="21"/><line x1="11" y1="25" x2="20" y2="25"/></svg></div>
        <h4>Document Control &amp; Reporting</h4>
        <p>Aconex, Omtrak, progress claims, O&amp;M manuals, Form 12, SDS, and defect registers — end-to-end project documentation.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M7 22 Q7 13 18 11 Q29 13 29 22 Z"/><rect x="5" y="22" width="26" height="4" rx="2"/><line x1="18" y1="11" x2="18" y2="22"/><circle cx="12" cy="30" r="2.5"/><circle cx="18" cy="30" r="2.5"/><circle cx="24" cy="30" r="2.5"/></svg></div>
        <h4>Team Supervision</h4>
        <p>Direct management of up to 5 assemblers and 10 installers — daily workflows, issue resolution, safety and quality standards.</p>
      </div>
      <div class="sk-card">
        <div class="sk-card-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="10" cy="18" r="5"/><line x1="15" y1="18" x2="21" y2="18"/><circle cx="26" cy="18" r="5"/><path d="M6 10 Q3 5 8 4 Q13 3 12 8"/><path d="M24 10 Q24 4 29 4 Q34 5 30 10"/><path d="M6 26 Q3 31 8 32 Q13 33 12 28"/><path d="M24 26 Q24 32 29 32 Q34 31 30 26"/></svg></div>
        <h4>Procurement &amp; Supply Chain</h4>
        <p>End-to-end procurement, supplier negotiation, material sourcing, and alternative product identification under time pressure.</p>
      </div>
    </div>

    <div class="sk-label" style="margin-top:52px">Certifications &amp; Licences</div>
    <div class="sk-sub">Verified credentials.</div>
    <div class="cert-grid">
      <div class="ck">
        <div class="ck-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><polygon points="18,4 28,10 28,22 18,28 8,22 8,10" stroke-width="1.5"/><polygon points="18,9 24,12.5 24,19.5 18,23 12,19.5 12,12.5" stroke-width="1" stroke="rgba(30,127,225,0.4)"/><circle cx="18" cy="16" r="3"/><line x1="18" y1="13" x2="18" y2="9"/><line x1="20.6" y1="14.5" x2="24" y2="12.5"/><line x1="20.6" y1="17.5" x2="24" y2="19.5"/><line x1="18" y1="19" x2="18" y2="23"/><line x1="15.4" y1="17.5" x2="12" y2="19.5"/><line x1="15.4" y1="14.5" x2="12" y2="12.5"/></svg></div>
        <div class="ck-title">AI Fluency Framework &amp; Foundations</div>
        <div class="ck-issuer">Anthropic</div>
        <div class="ck-date">Issued Mar 2026</div>
        <div class="ck-id">ID: h57vy2eijca6</div>
        <span class="ck-new">Anthropic Certified</span>
      </div>
      <div class="ck">
        <div class="ck-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><polygon points="18,4 28,10 28,22 18,28 8,22 8,10" stroke-width="1.5"/><polygon points="18,9 24,12.5 24,19.5 18,23 12,19.5 12,12.5" stroke-width="1" stroke="rgba(30,127,225,0.4)"/><circle cx="18" cy="16" r="3"/><line x1="18" y1="13" x2="18" y2="9"/><line x1="20.6" y1="14.5" x2="24" y2="12.5"/><line x1="20.6" y1="17.5" x2="24" y2="19.5"/><line x1="18" y1="19" x2="18" y2="23"/><line x1="15.4" y1="17.5" x2="12" y2="19.5"/><line x1="15.4" y1="14.5" x2="12" y2="12.5"/></svg></div>
        <div class="ck-title">Claude 101</div>
        <div class="ck-issuer">Anthropic</div>
        <div class="ck-date">Issued Mar 2026</div>
        <div class="ck-id">ID: vzo84jk8qthh</div>
        <span class="ck-new">Anthropic Certified</span>
      </div>
      <div class="ck">
        <div class="ck-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="4" width="28" height="28" rx="3"/><line x1="4" y1="25" x2="32" y2="25"/><polyline points="9,21 14,14 19,17 24,10 28,13"/><circle cx="9" cy="21" r="1.5" fill="#1E7FE1" stroke="none"/><circle cx="14" cy="14" r="1.5" fill="#1E7FE1" stroke="none"/><circle cx="19" cy="17" r="1.5" fill="#1E7FE1" stroke="none"/><circle cx="24" cy="10" r="1.5" fill="#1E7FE1" stroke="none"/><circle cx="28" cy="13" r="1.5" fill="#1E7FE1" stroke="none"/></svg></div>
        <div class="ck-title">Leveraging Generative AI for Project Management</div>
        <div class="ck-issuer">Online Certification</div>
        <div class="ck-date">Artificial Intelligence (AI)</div>
      </div>
      <div class="ck">
        <div class="ck-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="6" width="18" height="24" rx="2"/><path d="M14 6 Q14 3 18 3 Q22 3 22 6"/><line x1="13" y1="14" x2="23" y2="14"/><line x1="13" y1="19" x2="23" y2="19"/><line x1="13" y1="24" x2="19" y2="24"/></svg></div>
        <div class="ck-title">AI in Project Management</div>
        <div class="ck-issuer">Online Certification</div>
        <div class="ck-date">Artificial Intelligence (AI)</div>
      </div>
      <div class="ck">
        <div class="ck-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M4 8 L12 5 L18 10 L24 5 L32 8 L30 22 L22 22 L18 30 L14 22 L6 22 Z"/><line x1="18" y1="10" x2="18" y2="30"/><path d="M14 22 L6 22 L4 8"/><path d="M22 22 L30 22 L32 8"/></svg></div>
        <div class="ck-title">White Card — Work Safely in Construction</div>
        <div class="ck-issuer">CPCWHS1001</div>
        <div class="ck-date">Issued 2024</div>
      </div>
      <div class="ck">
        <div class="ck-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M18 30 Q18 18 30 6 Q30 6 18 6 Q6 6 6 18 Q6 26 18 30 Z"/><line x1="18" y1="30" x2="18" y2="18"/><line x1="18" y1="22" x2="24" y2="16"/><line x1="18" y1="26" x2="12" y2="20"/></svg></div>
        <div class="ck-title">TERI Sustainable Design Programme</div>
        <div class="ck-issuer">TERI Institute</div>
        <div class="ck-date">Issued 2016</div>
      </div>
    </div>

    <div class="sk-label" style="margin-top:52px">Software &amp; Tools</div>
    <div class="sk-sub">★ Used daily in my current role.</div>
    <div class="sw-grid">
      <div class="sw-cat">
        <h5>Document Control</h5>
        <div class="sw-tags">
          <span class="sw-tag hi">★ Aconex</span>
          <span class="sw-tag hi">★ Omtrak</span>
        </div>
      </div>
      <div class="sw-cat">
        <h5>Estimation &amp; Design</h5>
        <div class="sw-tags">
          <span class="sw-tag hi">★ Bluebeam</span>
          <span class="sw-tag hi">★ Microvellum</span>
          <span class="sw-tag">AutoCAD</span>
          <span class="sw-tag">Revit</span>
          <span class="sw-tag">SketchUp</span>
          <span class="sw-tag">Rhino</span>
        </div>
      </div>
      <div class="sw-cat">
        <h5>AI &amp; Automation</h5>
        <div class="sw-tags">
          <span class="sw-tag hi">★ Claude</span>
          <span class="sw-tag hi">★ ChatGPT</span>
        </div>
      </div>
      <div class="sw-cat">
        <h5>Project &amp; Office</h5>
        <div class="sw-tags">
          <span class="sw-tag">MS Project</span>
          <span class="sw-tag">MS Visio</span>
          <span class="sw-tag">MS Excel</span>
          <span class="sw-tag">MS Word</span>
        </div>
      </div>
    </div>

    <div class="sk-label" style="margin-top:52px">Key Competencies</div>
    <div class="sk-sub">What recruiters consistently look for — what I consistently deliver.</div>
    <div class="comp-wrap">
      <div class="comp-chip">Factory Scheduling &amp; Capacity Planning</div>
      <div class="comp-chip">Offshore &amp; International Coordination</div>
      <div class="comp-chip">AI Process Automation</div>
      <div class="comp-chip">Client &amp; Stakeholder Communication</div>
      <div class="comp-chip">RFI &amp; Variation Management</div>
      <div class="comp-chip">Procurement &amp; Supply Chain</div>
      <div class="comp-chip">Fit-Out Estimation &amp; Cost Planning</div>
      <div class="comp-chip">Quality Assurance (ITP / ITC)</div>
      <div class="comp-chip">Aconex &amp; Omtrak Document Control</div>
      <div class="comp-chip">SWMS, WHS &amp; Safety Documentation</div>
      <div class="comp-chip">Site Inspections &amp; Defect Tracking</div>
      <div class="comp-chip">Team Supervision &amp; Leadership</div>
    </div>

  </div>

  <footer class="foot">
    <div class="foot-name">Srinivas Palivela &nbsp;·&nbsp; Brisbane, QLD</div>
    <div class="foot-links">
      <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
      <a href="tel:0426928276">0426 928 276</a>
      <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">LinkedIn</a>
    </div>
  </footer>
</div>

<!-- ══════════════════════════════════════════════════════
     CONTACT
═══════════════════════════════════════════════════════ -->
<div id="panel-contact" class="panel">
  <div class="section-hero">
    <div class="sh-label">Get In Touch</div>
    <h1>Let's build something<br><em>great together.</em></h1>
    <p>Open to Assistant Project Manager roles in Construction, Fit-Out, and Product Development across Brisbane and South East Queensland. I respond within 24 hours.</p>
  </div>

  <div class="ct-body">
    <div class="ct-cards">
      <div class="ct-card">
        <div class="ct-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M8 6 L13 6 Q14 6 14.5 7.5 L16 12 Q16.5 13.5 15 14.5 L13 16 Q16 21 20 24 L21.5 22 Q22.5 20.5 24 21 L28.5 22.5 Q30 23 30 24 L30 29 Q30 30 28 30 Q10 30 6 8 Q6 6 8 6 Z"/></svg></div>
        <div>
          <h4>Phone</h4>
          <a href="tel:0426928276">0426 928 276</a>
          <p class="ct-sub">Mon–Fri, 7am–6pm AEST</p>
        </div>
      </div>
      <div class="ct-card">
        <div class="ct-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="8" width="28" height="20" rx="2"/><polyline points="4,8 18,20 32,8"/><line x1="4" y1="28" x2="13" y2="19"/><line x1="32" y1="28" x2="23" y2="19"/></svg></div>
        <div>
          <h4>Email</h4>
          <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
          <p class="ct-sub">Response within 24 hours</p>
        </div>
      </div>
      <div class="ct-card">
        <div class="ct-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="5" y="5" width="26" height="26" rx="4"/><line x1="11" y1="15" x2="11" y2="27"/><line x1="11" y1="11" x2="11" y2="13"/><line x1="16" y1="15" x2="16" y2="27"/><path d="M16 19 Q16 15 21 15 Q26 15 26 20 L26 27"/></svg></div>
        <div>
          <h4>LinkedIn</h4>
          <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">srinivas-palivela-03716a77</a>
          <p class="ct-sub">Connect directly</p>
        </div>
      </div>
      <div class="ct-card">
        <div class="ct-icon"><svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" stroke="#1E7FE1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M18 4 Q26 4 26 14 Q26 22 18 32 Q10 22 10 14 Q10 4 18 4 Z"/><circle cx="18" cy="14" r="4" fill="#EAF3FD" stroke-width="1.6"/></svg></div>
        <div>
          <h4>Location</h4>
          <div class="ct-plain">Brisbane, QLD, Australia</div>
          <p class="ct-sub">Open across South East Queensland</p>
        </div>
      </div>
    </div>

    <div class="open-box">
      <h3>What I'm Looking For</h3>
      <p class="ob-sub">Roles I'm actively applying for:</p>
      <div class="role-tags">
        <span class="role-tag role-tag-primary">👷 Assistant Project Manager</span>
        <span class="role-tag">🏗️ Construction</span>
        <span class="role-tag">🪵 Fit-Out</span>
        <span class="role-tag">📦 Product Development</span>
      </div>
      <p class="ob-sub">Locations I'm open to:</p>
      <div class="loc-tags">
        <span class="loc-tag">📍 Brisbane</span>
        <span class="loc-tag">📍 Gold Coast</span>
        <span class="loc-tag">📍 Sunshine Coast</span>
        <span class="loc-tag">📍 Ipswich</span>
        <span class="loc-tag">📍 Toowoomba</span>
      </div>
    </div>

    <div class="avail-bar">
      <div class="avail-dot"></div>
      <p><strong>Currently available</strong> — actively seeking roles in construction project management, fit-out coordination, and product project delivery. Open to full-time, part-time, or contract.</p>
    </div>
  </div>

  <footer class="foot">
    <div class="foot-name">Srinivas Palivela &nbsp;·&nbsp; Brisbane, QLD</div>
    <div class="foot-links">
      <a href="mailto:ar.srinivasp@gmail.com">ar.srinivasp@gmail.com</a>
      <a href="tel:0426928276">0426 928 276</a>
      <a href="https://linkedin.com/in/srinivas-palivela-03716a77" target="_blank">LinkedIn</a>
    </div>
  </footer>
</div>

<script>
function showTab(btn, name) {
  document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('panel-' + name).classList.add('active');
  btn.classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
  if (name === 'experience') {
    setTimeout(() => {
      const obs = new IntersectionObserver((entries) => {
        entries.forEach((e, i) => {
          if (e.isIntersecting) setTimeout(() => e.target.classList.add('vis'), i * 120);
        });
      }, { threshold: 0.08 });
      document.querySelectorAll('.tl-item').forEach(el => { el.classList.remove('vis'); obs.observe(el); });
    }, 80);
  }
}
// Auto-animate experience on first load if active
window.addEventListener('load', () => {
  const obs = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) setTimeout(() => e.target.classList.add('vis'), i * 120);
    });
  }, { threshold: 0.08 });
  document.querySelectorAll('.tl-item').forEach(el => obs.observe(el));
});
</script>
</body>
</html>
