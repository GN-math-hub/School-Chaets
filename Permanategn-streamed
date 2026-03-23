<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no,viewport-fit=cover"/>
<meta name="mobile-web-app-capable" content="yes"/>
<meta name="apple-mobile-web-app-capable" content="yes"/>
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent"/>
<title>StarStream</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"/>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Outfit:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
:root{
  --accent:#3b82f6;--accent2:#8b5cf6;--accent3:#06b6d4;
  --glow:rgba(59,130,246,.35);--glow2:rgba(139,92,246,.25);
  --bg:#05050f;--bg2:#080818;
  --surface:#0e0e20;--surface2:#141428;--surface3:#1c1c38;--surface4:#242445;
  --text:#eeeef8;--text2:#8888aa;--text3:#44446a;
  --border:rgba(255,255,255,.06);--border2:rgba(255,255,255,.1);--border3:rgba(59,130,246,.25);
  --r:14px;--ease:cubic-bezier(.4,0,.2,1);--spring:cubic-bezier(.34,1.56,.64,1);--bounce:cubic-bezier(.68,-.55,.27,1.55);
  --nav-h:68px;--hdr-h:62px;
  --st:env(safe-area-inset-top,0px);--sb:env(safe-area-inset-bottom,0px);
  --sl:env(safe-area-inset-left,0px);--sr:env(safe-area-inset-right,0px);
  --grad:linear-gradient(135deg,var(--accent),var(--accent2));
}
[data-theme="light"]{
  --bg:#f0f0fa;--bg2:#e8e8f5;--surface:#fff;--surface2:#f4f4fc;--surface3:#eaeaf8;--surface4:#e0e0f5;
  --text:#0a0a1a;--text2:#505075;--text3:#9090b8;--border:rgba(0,0,0,.06);--border2:rgba(0,0,0,.1);
}
html,body{overflow-x:hidden;max-width:100vw;height:100%;-webkit-font-smoothing:antialiased;text-rendering:optimizeLegibility}
body{font-family:'Outfit',-apple-system,sans-serif;background:var(--bg);color:var(--text);min-height:100%;line-height:1.5;transition:background .3s,color .3s}
body.locked{overflow:hidden;position:fixed;width:100%;height:100%}
img{display:block}
#popupPermissionModal{position:fixed;inset:0;z-index:999999;display:flex;align-items:center;justify-content:center;padding:20px;background:radial-gradient(ellipse at 50% 40%,rgba(59,130,246,.18) 0%,rgba(5,5,15,.98) 60%);backdrop-filter:blur(24px);-webkit-backdrop-filter:blur(24px)}
.ppm-box{background:var(--surface);border:1px solid var(--border3);border-radius:24px;max-width:400px;width:100%;overflow:hidden;box-shadow:0 0 80px rgba(59,130,246,.2),0 32px 64px rgba(0,0,0,.6);animation:ppmIn .5s var(--spring) forwards}
@keyframes ppmIn{from{opacity:0;transform:translateY(32px) scale(.94)}to{opacity:1;transform:translateY(0) scale(1)}}
.ppm-top{background:linear-gradient(135deg,rgba(59,130,246,.15),rgba(139,92,246,.1));border-bottom:1px solid var(--border);padding:28px 24px 22px;text-align:center;position:relative;overflow:hidden}
.ppm-top::before{content:'';position:absolute;inset:0;background:radial-gradient(ellipse at 50% 0%,rgba(59,130,246,.12),transparent 70%)}
.ppm-icon-ring{width:72px;height:72px;border-radius:50%;background:linear-gradient(135deg,var(--accent),var(--accent2));display:flex;align-items:center;justify-content:center;margin:0 auto 16px;font-size:28px;color:#fff;box-shadow:0 0 0 12px rgba(59,130,246,.1),0 0 0 24px rgba(59,130,246,.05);position:relative;z-index:1;animation:pulseRing 2.5s ease-in-out infinite}
@keyframes pulseRing{0%,100%{box-shadow:0 0 0 12px rgba(59,130,246,.1),0 0 0 24px rgba(59,130,246,.05)}50%{box-shadow:0 0 0 16px rgba(59,130,246,.15),0 0 0 32px rgba(59,130,246,.06)}}
.ppm-logo{font-family:'Bebas Neue',sans-serif;font-size:28px;letter-spacing:3px;background:var(--grad);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;position:relative;z-index:1}
.ppm-body{padding:22px 24px 24px}
.ppm-title{font-size:18px;font-weight:800;margin-bottom:8px;letter-spacing:-.3px}
.ppm-desc{font-size:13px;color:var(--text2);line-height:1.7;margin-bottom:18px}
.ppm-info-cards{display:flex;flex-direction:column;gap:8px;margin-bottom:22px}
.ppm-info-card{display:flex;align-items:center;gap:12px;background:var(--surface2);border:1px solid var(--border);border-radius:12px;padding:11px 14px}
.ppm-info-icon{width:34px;height:34px;border-radius:9px;display:flex;align-items:center;justify-content:center;font-size:14px;flex-shrink:0}
.ppm-info-icon.blue{background:rgba(59,130,246,.15);color:var(--accent)}
.ppm-info-icon.purple{background:rgba(139,92,246,.15);color:var(--accent2)}
.ppm-info-icon.cyan{background:rgba(6,182,212,.15);color:var(--accent3)}
.ppm-info-text{font-size:12px;color:var(--text2);line-height:1.5;flex:1}
.ppm-info-text strong{color:var(--text);font-weight:700}
.ppm-btn{width:100%;padding:15px;border-radius:12px;background:var(--grad);color:#fff;font-family:'Outfit',sans-serif;font-size:15px;font-weight:800;letter-spacing:.3px;border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:9px;transition:opacity .2s,transform .15s;box-shadow:0 8px 24px rgba(59,130,246,.35)}
.ppm-btn:active{opacity:.88;transform:scale(.98)}
.ppm-skip{width:100%;background:none;border:none;color:var(--text3);font-size:11px;font-weight:600;cursor:pointer;margin-top:12px;padding:6px;font-family:'Outfit',sans-serif;letter-spacing:.3px;text-transform:uppercase;transition:color .15s}
.ppm-skip:active{color:var(--text2)}
#startupTip{position:fixed;inset:0;background:rgba(0,0,0,.97);display:flex;align-items:center;justify-content:center;z-index:99999;padding:20px;backdrop-filter:blur(12px)}
.tip-box{background:var(--surface);border:1px solid var(--border2);border-radius:24px;max-width:380px;width:100%;overflow:hidden;box-shadow:0 32px 64px rgba(0,0,0,.5)}
.tip-top{background:var(--grad);padding:22px 24px;display:flex;align-items:center;gap:14px}
.tip-logo{font-family:'Bebas Neue',sans-serif;font-size:28px;letter-spacing:3px;color:#fff;display:flex;align-items:center;gap:8px}
.tip-tagline{font-size:10px;color:rgba(255,255,255,.75);font-weight:700;text-transform:uppercase;letter-spacing:1.8px;margin-top:3px}
.tip-body{padding:18px}
.tip-card{display:flex;gap:13px;padding:13px;background:var(--surface2);border-radius:12px;margin-bottom:10px;border:1px solid var(--border)}
.tip-card-ico{width:36px;height:36px;border-radius:9px;background:var(--surface3);display:flex;align-items:center;justify-content:center;font-size:15px;color:var(--text2);flex-shrink:0}
.tip-card h3{font-size:12px;font-weight:800;margin-bottom:3px;letter-spacing:-.2px}
.tip-card p{font-size:11px;color:var(--text2);line-height:1.6}
.tip-card strong{color:var(--accent);font-weight:700}
.tip-footer{display:flex;align-items:center;gap:12px;padding:0 18px 20px}
.tip-dismiss{flex:1;background:var(--grad);color:#fff;border:none;padding:14px;border-radius:12px;font-size:13px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;display:flex;align-items:center;justify-content:center;gap:9px;letter-spacing:.3px;box-shadow:0 6px 20px rgba(59,130,246,.3)}
.tip-countdown{font-family:'Bebas Neue',sans-serif;font-size:30px;color:var(--text3);min-width:34px;text-align:center}
#confirmModal{position:fixed;inset:0;background:rgba(0,0,0,.85);display:none;align-items:flex-end;justify-content:center;z-index:99998;padding:12px;backdrop-filter:blur(8px)}
#confirmModal.open{display:flex}
.confirm-box{background:var(--surface);border:1px solid var(--border2);border-radius:20px 20px 16px 16px;width:100%;max-width:420px;overflow:hidden}
.confirm-msg{padding:22px 20px 18px;text-align:center}
.confirm-msg h3{font-size:17px;font-weight:800;margin-bottom:7px;letter-spacing:-.3px}
.confirm-msg p{font-size:12px;color:var(--text2);line-height:1.6}
.confirm-actions{display:grid;grid-template-columns:1fr 1fr;border-top:1px solid var(--border)}
.confirm-cancel{background:transparent;color:var(--text2);border:none;border-right:1px solid var(--border);padding:16px;font-size:14px;font-weight:600;cursor:pointer;font-family:'Outfit',sans-serif}
.confirm-ok{background:transparent;color:#ef4444;border:none;padding:16px;font-size:14px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif}
header{position:fixed;top:0;left:0;right:0;height:calc(var(--hdr-h) + var(--st));padding-top:var(--st);z-index:500;display:flex;align-items:center;padding-left:calc(16px + var(--sl));padding-right:calc(16px + var(--sr));gap:10px;background:linear-gradient(to bottom,rgba(5,5,15,.95) 0%,transparent 100%);transition:background .3s}
header.solid{background:rgba(5,5,15,.98);border-bottom:1px solid var(--border);backdrop-filter:blur(20px)}
.logo{font-family:'Bebas Neue',sans-serif;font-size:26px;letter-spacing:3px;cursor:pointer;flex-shrink:0;background:var(--grad);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;line-height:1;display:flex;align-items:center;gap:7px}
.logo-star{width:30px;height:30px;border-radius:8px;background:var(--grad);display:flex;align-items:center;justify-content:center;font-size:14px;color:#fff;flex-shrink:0;box-shadow:0 4px 14px rgba(59,130,246,.4)}
.hdr-center{flex:1;display:flex;justify-content:center;padding:0 10px}
.hdr-nav{display:flex;gap:2px;background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:4px}
.hdr-nav-btn{background:none;border:none;color:var(--text3);font-size:11px;font-weight:700;letter-spacing:.5px;text-transform:uppercase;cursor:pointer;padding:6px 14px;border-radius:8px;font-family:'Outfit',sans-serif;transition:all .15s;white-space:nowrap}
.hdr-nav-btn.on{background:var(--surface3);color:var(--text)}
.hdr-right{display:flex;align-items:center;gap:6px;margin-left:auto}
.h-btn{width:38px;height:38px;border-radius:11px;border:1px solid var(--border2);background:var(--surface);color:var(--text2);display:flex;align-items:center;justify-content:center;font-size:14px;cursor:pointer;transition:all .15s;backdrop-filter:blur(12px);flex-shrink:0}
.h-btn:hover{border-color:var(--border3);color:var(--text);background:var(--surface2)}
.h-btn:active{transform:scale(.95)}
.h-profile-btn{width:36px;height:36px;border-radius:11px;background:var(--grad);display:flex;align-items:center;justify-content:center;font-size:14px;color:#fff;cursor:pointer;border:none;flex-shrink:0;box-shadow:0 4px 12px rgba(59,130,246,.35);transition:transform .15s,box-shadow .15s}
.h-profile-btn:hover{transform:scale(1.05);box-shadow:0 6px 18px rgba(59,130,246,.45)}
.srv-pill{display:flex;align-items:center;gap:6px;background:var(--surface);border:1px solid var(--border2);border-radius:11px;padding:5px 10px;backdrop-filter:blur(12px)}
.srv-dot{width:6px;height:6px;border-radius:50%;background:#22c55e;flex-shrink:0;box-shadow:0 0 6px rgba(34,197,94,.5)}
.srv-label{font-size:9px;color:var(--text3);font-weight:700;text-transform:uppercase;letter-spacing:.7px;white-space:nowrap}
.srv-select{background:transparent;color:var(--text);border:none;font-size:11px;font-weight:700;cursor:pointer;outline:none;font-family:'Outfit',sans-serif;max-width:90px}
#bottomNav{position:fixed;bottom:0;left:0;right:0;height:calc(var(--nav-h) + var(--sb));padding-bottom:var(--sb);background:rgba(5,5,15,.97);border-top:1px solid var(--border);z-index:500;display:flex;align-items:flex-start;padding-top:10px;backdrop-filter:blur(24px);-webkit-backdrop-filter:blur(24px)}
.nav-tab{flex:1;display:flex;flex-direction:column;align-items:center;gap:5px;cursor:pointer;padding:4px 0;border:none;background:none;color:var(--text3);font-family:'Outfit',sans-serif;-webkit-tap-highlight-color:transparent;position:relative;transition:color .2s}
.nav-tab.on{color:var(--accent)}
.nav-tab-icon{width:30px;height:30px;display:flex;align-items:center;justify-content:center;border-radius:10px;font-size:17px;transition:all .25s var(--spring);position:relative}
.nav-tab.on .nav-tab-icon{background:rgba(59,130,246,.15);transform:scale(1.1)}
.nav-tab-label{font-size:9px;font-weight:800;text-transform:uppercase;letter-spacing:.8px}
.nav-badge{position:absolute;top:-4px;right:-6px;background:var(--accent);color:#fff;font-size:8px;font-weight:900;padding:1px 4px;border-radius:6px;min-width:15px;text-align:center;line-height:15px;display:none;border:1.5px solid var(--bg)}
.nav-tab-active-bar{position:absolute;bottom:-10px;left:50%;transform:translateX(-50%);width:0;height:2px;background:var(--grad);border-radius:1px;transition:width .25s var(--spring)}
.nav-tab.on .nav-tab-active-bar{width:20px}
#mainContent{padding-top:var(--hdr-h);padding-bottom:var(--nav-h)}
#heroSection{position:relative;width:100%;height:calc(100svh - var(--nav-h));min-height:500px;max-height:820px;display:flex;align-items:flex-end;overflow:hidden}
.hero-bg{position:absolute;inset:0;background-size:cover;background-position:center 20%;transition:opacity .9s var(--ease)}
.hero-bg::after{content:'';position:absolute;inset:0;background:linear-gradient(to top,var(--bg) 0%,rgba(5,5,15,.65) 45%,transparent 100%),linear-gradient(to right,rgba(5,5,15,.92) 0%,rgba(5,5,15,.15) 65%,transparent 100%)}
.hero-bg::before{content:'';position:absolute;inset:0;background:radial-gradient(ellipse at 30% 60%,rgba(59,130,246,.08) 0%,transparent 60%);z-index:1;pointer-events:none}
[data-theme="light"] .hero-bg::after{background:linear-gradient(to top,var(--bg) 0%,rgba(240,240,250,.65) 45%,transparent 100%),linear-gradient(to right,rgba(240,240,250,.92) 0%,rgba(240,240,250,.15) 65%,transparent 100%)}
.hero-content{position:relative;z-index:3;padding:0 18px 28px}
.hero-eyebrow{display:inline-flex;align-items:center;gap:7px;background:rgba(59,130,246,.12);border:1px solid rgba(59,130,246,.28);color:var(--accent);padding:5px 12px;border-radius:24px;font-size:10px;font-weight:800;text-transform:uppercase;letter-spacing:1.5px;margin-bottom:12px;backdrop-filter:blur(8px)}
.hero-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(40px,10vw,76px);line-height:.92;letter-spacing:1px;color:var(--text);margin-bottom:10px;text-shadow:0 4px 30px rgba(0,0,0,.4)}
.hero-meta{display:flex;align-items:center;gap:8px;margin-bottom:10px;font-size:12px;color:var(--text2);flex-wrap:wrap}
.hero-cert{background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.2);padding:2px 7px;border-radius:5px;font-weight:800;font-size:10px}
.hero-rating{display:flex;align-items:center;gap:4px;background:rgba(255,200,0,.1);border:1px solid rgba(255,200,0,.2);padding:2px 8px;border-radius:5px;color:#fbbf24;font-weight:800;font-size:10px}
.hero-overview{font-size:13px;color:var(--text2);line-height:1.65;max-width:360px;margin-bottom:20px;display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden;font-weight:400}
.hero-btns{display:flex;gap:9px;flex-wrap:wrap;align-items:center}
.btn-play{background:var(--text);color:var(--bg);border:none;padding:13px 26px;border-radius:12px;font-size:14px;font-weight:800;cursor:pointer;display:flex;align-items:center;gap:8px;transition:all .2s;font-family:'Outfit',sans-serif;flex-shrink:0;letter-spacing:.2px;box-shadow:0 6px 22px rgba(0,0,0,.25)}
[data-theme="light"] .btn-play{background:#0a0a1a;color:#fff}
.btn-play:hover{transform:scale(1.03)}
.btn-play:active{opacity:.85;transform:scale(.98)}
.btn-info{background:rgba(255,255,255,.1);color:var(--text);border:1px solid rgba(255,255,255,.18);padding:13px 18px;border-radius:12px;font-size:14px;font-weight:700;cursor:pointer;display:flex;align-items:center;gap:8px;transition:all .2s;font-family:'Outfit',sans-serif;backdrop-filter:blur(12px);flex-shrink:0}
.btn-info:hover{background:rgba(255,255,255,.18)}
.btn-info:active{background:rgba(255,255,255,.25)}
.btn-icon-hero{background:rgba(255,255,255,.08);color:var(--text2);border:1px solid rgba(255,255,255,.14);width:44px;height:44px;border-radius:12px;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:17px;transition:all .2s;backdrop-filter:blur(10px);flex-shrink:0}
.btn-icon-hero:hover{background:rgba(255,255,255,.16);color:var(--text)}
.btn-icon-hero.active{background:rgba(59,130,246,.2);color:var(--accent);border-color:rgba(59,130,246,.35)}
.hero-dots{position:absolute;bottom:10px;right:16px;z-index:4;display:flex;gap:6px;align-items:center}
.hero-dot{width:5px;height:5px;border-radius:50%;background:rgba(255,255,255,.2);cursor:pointer;transition:all .35s var(--spring)}
.hero-dot.on{background:rgba(255,255,255,.8);width:20px;border-radius:3px}
.section{margin:24px 0;padding:0 16px;opacity:0;transform:translateY(14px);transition:opacity .55s var(--ease),transform .55s var(--ease)}
.section.vis{opacity:1;transform:translateY(0)}
.section-hd{display:flex;align-items:center;justify-content:space-between;margin-bottom:14px}
.section-title{font-size:11px;font-weight:900;display:flex;align-items:center;gap:9px;text-transform:uppercase;letter-spacing:2px;color:var(--text)}
.stbar{width:3px;height:16px;background:var(--grad);border-radius:2px;flex-shrink:0}
.view-all{color:var(--text3);font-size:10px;font-weight:800;cursor:pointer;transition:all .15s;text-transform:uppercase;letter-spacing:1px;display:flex;align-items:center;gap:5px;padding:5px 10px;border-radius:8px;border:1px solid transparent}
.view-all:active{color:var(--accent);background:rgba(59,130,246,.08);border-color:var(--border3)}
.row{display:flex;gap:11px;overflow-x:auto;scroll-behavior:smooth;padding:4px 0 14px;scrollbar-width:none;scroll-snap-type:x mandatory;-webkit-overflow-scrolling:touch}
.row::-webkit-scrollbar{display:none}
.card{flex:0 0 122px;border-radius:12px;overflow:hidden;cursor:pointer;position:relative;background:var(--surface2);scroll-snap-align:start;height:183px;transition:transform .25s var(--spring),box-shadow .25s;border:1px solid var(--border)}
.card:hover{transform:translateY(-3px) scale(1.02);box-shadow:0 14px 32px rgba(0,0,0,.4),0 0 0 1px var(--border3)}
.card:active{transform:scale(.97)}
.card img{width:100%;height:100%;object-fit:cover}
.card-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.95) 0%,rgba(0,0,0,.05) 55%,transparent 100%);display:flex;flex-direction:column;justify-content:flex-end;padding:9px}
.card-title{font-size:10px;font-weight:800;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;margin-bottom:4px;color:#fff;letter-spacing:.1px}
.card-meta{font-size:9px;color:rgba(255,255,255,.5);display:flex;align-items:center;gap:4px}
.card-badge{background:rgba(255,255,255,.08);padding:2px 6px;border-radius:4px;font-size:8px;font-weight:800;border:1px solid rgba(255,255,255,.07)}
.card-actions{position:absolute;top:7px;right:7px;display:flex;gap:4px}
.card-act{width:28px;height:28px;background:rgba(0,0,0,.75);border:1px solid rgba(255,255,255,.12);border-radius:7px;color:#fff;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:11px;transition:all .15s;backdrop-filter:blur(8px)}
.card-act:active,.card-act.on{background:rgba(59,130,246,.4);border-color:rgba(59,130,246,.6)}
.top10-wrap{flex:0 0 158px;display:flex;align-items:flex-end;cursor:pointer;scroll-snap-align:start;position:relative}
.top10-num{font-family:'Bebas Neue',sans-serif;font-size:115px;line-height:1;color:transparent;-webkit-text-stroke:2px rgba(255,255,255,.06);letter-spacing:-10px;margin-right:-20px;z-index:2;user-select:none;flex-shrink:0;transition:all .3s}
.top10-wrap:hover .top10-num{-webkit-text-stroke-color:rgba(59,130,246,.2)}
.top10-poster{width:102px;height:153px;border-radius:10px;overflow:hidden;flex-shrink:0;box-shadow:0 12px 32px rgba(0,0,0,.7);z-index:3;border:1px solid var(--border)}
.top10-poster img{width:100%;height:100%;object-fit:cover}
.hot-grid{display:grid;grid-template-columns:1fr;gap:8px}
.hot-item{display:flex;align-items:center;gap:11px;background:var(--surface);border-radius:12px;padding:11px 14px;border:1px solid var(--border);cursor:pointer;transition:all .15s}
.hot-item:hover{border-color:var(--border3);background:var(--surface2)}
.hot-item:active{background:var(--surface3)}
.hot-rank{font-family:'Bebas Neue',sans-serif;font-size:28px;background:var(--grad);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;min-width:30px;text-align:center;line-height:1}
.hot-poster{width:40px;height:60px;border-radius:7px;object-fit:cover;flex-shrink:0;border:1px solid var(--border)}
.hot-info{flex:1;min-width:0}
.hot-title{font-size:12px;font-weight:800;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;margin-bottom:3px;letter-spacing:-.1px}
.hot-meta{font-size:10px;color:var(--text3);display:flex;gap:5px;align-items:center}
.hot-score{background:rgba(59,130,246,.1);color:var(--accent);font-size:9px;font-weight:900;padding:2px 7px;border-radius:6px;border:1px solid rgba(59,130,246,.2);margin-left:auto;letter-spacing:.3px}
.wide-card{flex:0 0 225px;background:var(--surface);border-radius:12px;overflow:hidden;cursor:pointer;border:1px solid var(--border);transition:all .2s}
.wide-card:hover{border-color:var(--border3);transform:translateY(-2px);box-shadow:0 12px 28px rgba(0,0,0,.3)}
.wide-card:active{border-color:var(--border3)}
.wide-thumb{width:100%;height:127px;position:relative;overflow:hidden;background:#000}
.wide-thumb img{width:100%;height:100%;object-fit:cover;transition:transform .3s}
.wide-card:hover .wide-thumb img{transform:scale(1.04)}
.wide-play{position:absolute;inset:0;background:rgba(0,0,0,.4);display:flex;align-items:center;justify-content:center}
.wide-play-btn{width:42px;height:42px;background:rgba(255,255,255,.92);border-radius:50%;display:flex;align-items:center;justify-content:center;box-shadow:0 4px 16px rgba(0,0,0,.3)}
.wide-play-btn svg{width:15px;height:15px;fill:#000;margin-left:3px}
.wide-info{padding:9px 11px 11px}
.wide-title{font-size:12px;font-weight:800;margin-bottom:3px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;letter-spacing:-.1px}
.wide-meta{font-size:10px;color:var(--text3);display:flex;align-items:center;gap:7px}
.skeleton{background:linear-gradient(90deg,var(--surface2) 25%,var(--surface3) 50%,var(--surface2) 75%);background-size:200% 100%;animation:shimmer 1.8s infinite;border-radius:12px}
@keyframes shimmer{0%{background-position:200% 0}100%{background-position:-200% 0}}
#detailsModal{position:fixed;inset:0;background:rgba(0,0,0,.88);display:none;align-items:flex-end;justify-content:center;z-index:1000;backdrop-filter:blur(8px)}
#detailsModal.open{display:flex}
#detailsBox{width:100%;max-width:620px;background:var(--surface);border-radius:22px 22px 0 0;overflow:hidden;border:1px solid var(--border2);border-bottom:none;max-height:92svh;overflow-y:auto;-webkit-overflow-scrolling:touch;transform:translateY(100%);transition:transform .4s var(--spring);scrollbar-width:thin}
#detailsModal.open #detailsBox{transform:translateY(0)}
.details-handle{width:40px;height:4px;background:var(--surface4);border-radius:2px;margin:14px auto 0}
.details-hero{position:relative;width:100%;padding-bottom:52%;background:#000;overflow:hidden}
.details-poster{position:absolute;inset:0;width:100%;height:100%;object-fit:cover}
.details-grad{position:absolute;bottom:0;left:0;right:0;height:65%;background:linear-gradient(to top,var(--surface),transparent);z-index:1}
.details-trailer-btn{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);width:56px;height:56px;background:rgba(255,255,255,.1);border:1.5px solid rgba(255,255,255,.35);border-radius:50%;display:flex;align-items:center;justify-content:center;cursor:pointer;z-index:3;transition:all .2s;backdrop-filter:blur(10px)}
.details-trailer-btn:hover{background:rgba(255,255,255,.2);transform:translate(-50%,-50%) scale(1.08)}
.details-trailer-btn svg{width:20px;height:20px;fill:#fff;margin-left:3px}
.close-btn{position:fixed;top:calc(12px + var(--st));right:12px;width:38px;height:38px;background:rgba(10,10,24,.9);border:1px solid var(--border2);color:var(--text);border-radius:11px;font-size:14px;cursor:pointer;z-index:1001;display:flex;align-items:center;justify-content:center;backdrop-filter:blur(14px);transition:all .15s}
.close-btn:hover{background:var(--surface2);border-color:var(--border3)}
.details-info{padding:20px 16px 0;margin-top:-45px;position:relative;z-index:2}
.details-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(28px,7vw,42px);letter-spacing:1px;margin-bottom:9px;line-height:1}
.details-meta-row{display:flex;gap:7px;align-items:center;margin-bottom:14px;flex-wrap:wrap;color:var(--text2);font-size:11px}
.d-match{background:var(--grad);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;font-weight:900;font-size:14px}
.d-cert{background:var(--surface3);color:var(--text2);padding:2px 7px;border-radius:6px;font-weight:800;font-size:9px;border:1px solid var(--border2);-webkit-text-fill-color:var(--text2)}
.details-actions{display:flex;gap:9px;margin-bottom:16px;flex-wrap:wrap}
.btn-d{padding:11px 18px;border-radius:12px;font-size:12px;font-weight:800;cursor:pointer;border:none;display:flex;align-items:center;gap:8px;transition:all .15s;font-family:'Outfit',sans-serif;white-space:nowrap;letter-spacing:.2px}
.btn-d-play{background:var(--text);color:var(--bg);flex:1;box-shadow:0 4px 16px rgba(0,0,0,.2)}
[data-theme="light"] .btn-d-play{background:#0a0a1a;color:#fff}
.btn-d-play:hover{transform:scale(1.02)}
.btn-d-play:active{opacity:.85}
.btn-d-list{background:var(--surface2);color:var(--text);border:1px solid var(--border2)}
.btn-d-list:hover{border-color:var(--border3)}
.btn-d-list:active,.btn-d-list.on{background:var(--surface3);border-color:rgba(59,130,246,.4)}
.btn-d-dl{background:var(--surface2);color:var(--text);border:1px solid var(--border2)}
.btn-d-dl:hover{border-color:var(--border3)}
/* ── NEW: Open in New Tab button in details ── */
.btn-d-newtab{
  background:linear-gradient(135deg,rgba(59,130,246,.13),rgba(139,92,246,.13));
  color:#818cf8;
  border:1px solid rgba(99,102,241,.38);
  font-size:11px;
  flex-shrink:0;
}
.btn-d-newtab:hover{
  background:linear-gradient(135deg,rgba(59,130,246,.24),rgba(139,92,246,.24));
  border-color:rgba(99,102,241,.62);
}
/* ── NEW: Episode action row ── */
.ep-action-row{display:flex;gap:6px;margin-top:7px;flex-wrap:wrap}
.ep-action-btn{
  display:inline-flex;align-items:center;gap:5px;
  padding:5px 10px;border-radius:7px;
  border:1px solid var(--border2);background:var(--surface3);
  color:var(--text2);font-size:10px;font-weight:700;cursor:pointer;
  transition:all .15s;font-family:'Outfit',sans-serif;white-space:nowrap;line-height:1;
}
.ep-action-btn:hover{border-color:rgba(99,102,241,.5);color:#818cf8;background:rgba(99,102,241,.1)}
.ep-action-btn:active{opacity:.82;transform:scale(.96)}
.ep-action-btn.ep-dl{color:#34d399;border-color:rgba(52,211,153,.32);background:rgba(52,211,153,.07)}
.ep-action-btn.ep-dl:hover{background:rgba(52,211,153,.16);border-color:rgba(52,211,153,.6);color:#34d399}
#detailsBody{padding:0 16px 16px}
.details-sec{margin-bottom:18px}
.details-sec h3{font-size:9px;text-transform:uppercase;color:var(--text3);margin-bottom:9px;letter-spacing:2.5px;font-weight:900}
.details-sec p{color:var(--text2);line-height:1.75;font-size:12px;font-weight:400}
.cast-chips{display:flex;gap:6px;flex-wrap:wrap}
.cast-chip{background:var(--surface2);padding:6px 11px;border-radius:8px;font-size:10px;border:1px solid var(--border);font-weight:600;transition:all .15s}
.cast-chip:hover{border-color:var(--border3);background:var(--surface3)}
.ep-section{padding:0 16px 20px;border-top:1px solid var(--border)}
.ep-hd{display:flex;align-items:center;gap:11px;padding-top:18px;margin-bottom:14px;flex-wrap:wrap}
.ep-hd-title{font-family:'Bebas Neue',sans-serif;font-size:22px;letter-spacing:.8px}
.season-wrap{display:flex;align-items:center;gap:7px;margin-left:auto}
.season-wrap label{font-size:10px;color:var(--text3);font-weight:800;text-transform:uppercase;letter-spacing:1px}
.season-dd{background:var(--surface2);border:1px solid var(--border2);color:var(--text);border-radius:9px;padding:8px 28px 8px 12px;font-size:11px;font-weight:700;cursor:pointer;appearance:none;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='10' viewBox='0 0 12 12'%3E%3Cpath fill='%23666' d='M6 8L1 3h10z'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 9px center;font-family:'Outfit',sans-serif;outline:none;transition:border-color .15s}
.season-dd:focus{border-color:var(--border3)}
.ep-grid{display:flex;flex-direction:column;gap:9px}
.ep-card{display:flex;gap:11px;background:var(--surface2);border-radius:12px;overflow:hidden;cursor:pointer;border:1px solid var(--border);transition:all .15s}
.ep-card:hover{border-color:var(--border3);background:var(--surface3)}
.ep-card:active{background:var(--surface4)}
.ep-thumb{flex:0 0 122px;height:auto;min-height:70px;align-self:stretch;position:relative;background:#000;overflow:hidden}
.ep-thumb img{position:absolute;inset:0;width:100%;height:100%;object-fit:cover;transition:transform .3s}
.ep-card:hover .ep-thumb img{transform:scale(1.05)}
.ep-play{position:absolute;inset:0;background:rgba(0,0,0,.5);display:flex;align-items:center;justify-content:center}
.ep-play-btn{width:29px;height:29px;background:rgba(255,255,255,.92);border-radius:50%;display:flex;align-items:center;justify-content:center}
.ep-play-btn svg{width:12px;height:12px;fill:#000;margin-left:2px}
.ep-num{position:absolute;top:4px;left:4px;background:rgba(0,0,0,.85);color:#fff;font-size:8px;font-weight:900;padding:2px 6px;border-radius:4px;letter-spacing:.3px}
.ep-info{flex:1;padding:9px 11px;display:flex;flex-direction:column;justify-content:center;min-width:0}
.ep-title{font-size:12px;font-weight:800;margin-bottom:3px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;letter-spacing:-.1px}
.ep-meta{display:flex;align-items:center;gap:7px;margin-bottom:4px;font-size:9px;color:var(--text3);font-weight:600}
.ep-overview{font-size:10px;color:var(--text2);line-height:1.55;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;font-weight:400}
.recs-section{padding:0 16px 20px;border-top:1px solid var(--border)}
.recs-title{font-family:'Bebas Neue',sans-serif;font-size:20px;letter-spacing:.8px;padding-top:16px;margin-bottom:12px}
.recs-row{display:flex;gap:9px;overflow-x:auto;padding-bottom:4px;scrollbar-width:none;-webkit-overflow-scrolling:touch}
.recs-row::-webkit-scrollbar{display:none}
.rec-card{flex:0 0 auto;width:155px;height:87px;border-radius:9px;overflow:hidden;cursor:pointer;position:relative;transition:transform .2s;background:var(--surface2);border:1px solid var(--border)}
.rec-card:hover{transform:scale(1.03)}
.rec-card:active{transform:scale(.97)}
.rec-card img{width:100%;height:100%;object-fit:cover}
.rec-ov{position:absolute;bottom:0;left:0;right:0;padding:24px 8px 6px;background:linear-gradient(to top,rgba(0,0,0,.95),transparent)}
.rec-title{font-size:10px;font-weight:800;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;color:#fff}
.paw-section{padding:0 16px 18px;border-top:1px solid var(--border)}
.paw-title{font-size:10px;font-weight:900;padding-top:16px;margin-bottom:11px;text-transform:uppercase;letter-spacing:2px;color:var(--text3)}
.paw-row{display:flex;gap:8px;overflow-x:auto;padding-bottom:4px;scrollbar-width:none;-webkit-overflow-scrolling:touch}
.paw-row::-webkit-scrollbar{display:none}
.paw-card{flex:0 0 82px;background:var(--surface2);border-radius:9px;overflow:hidden;cursor:pointer;border:1px solid var(--border);transition:transform .15s}
.paw-card:hover{transform:scale(1.04)}
.paw-card:active{transform:scale(.97)}
.paw-card img{width:100%;height:50px;object-fit:cover}
.paw-card-title{padding:4px 6px;font-size:9px;font-weight:700;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;color:var(--text2)}
#profilesModal{position:fixed;inset:0;background:rgba(0,0,0,.94);display:none;align-items:center;justify-content:center;z-index:50000;padding:20px;backdrop-filter:blur(12px)}
#profilesModal.open{display:flex}
.profiles-wrap{text-align:center;width:100%;max-width:460px}
.profiles-main-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(34px,8vw,48px);letter-spacing:2.5px;margin-bottom:5px;background:var(--grad);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.profiles-subtitle{color:var(--text3);font-size:12px;margin-bottom:30px;font-weight:600;letter-spacing:.5px}
.profiles-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(92px,1fr));gap:13px;max-width:420px;margin:0 auto 26px}
.profile-item{cursor:pointer;transition:transform .2s var(--spring);position:relative}
.profile-item:active{transform:scale(.96)}
.profile-avatar-wrap{width:80px;height:80px;border-radius:16px;margin:0 auto 9px;border:2px solid var(--border);transition:all .2s;overflow:hidden;display:flex;align-items:center;justify-content:center;font-size:30px;background:var(--surface2)}
.profile-avatar-wrap.active{border-color:var(--accent);box-shadow:0 0 0 4px rgba(59,130,246,.15)}
.profile-name{font-size:12px;font-weight:700;color:var(--text2)}
.profile-remove-btn{position:absolute;top:-5px;right:3px;width:20px;height:20px;background:var(--surface3);border:1px solid var(--border);border-radius:50%;color:var(--text2);font-size:9px;cursor:pointer;display:flex;align-items:center;justify-content:center}
.profiles-footer{display:flex;gap:9px;justify-content:center;flex-wrap:wrap}
.profiles-manage-btn{background:transparent;border:1px solid var(--border2);color:var(--text2);padding:10px 20px;border-radius:10px;font-size:11px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .15s;text-transform:uppercase;letter-spacing:1px}
.profiles-manage-btn:hover{border-color:var(--border3);color:var(--text)}
.add-profile-form{background:var(--surface2);border:1px solid var(--border2);border-radius:16px;padding:20px;max-width:320px;margin:0 auto 22px;display:none;text-align:left}
.add-profile-form.vis{display:block}
.add-profile-form h3{font-family:'Bebas Neue',sans-serif;font-size:22px;letter-spacing:.8px;margin-bottom:14px;text-align:center}
.add-input{width:100%;padding:11px 14px;background:var(--surface3);border:1px solid var(--border2);border-radius:10px;color:var(--text);font-size:13px;margin-bottom:11px;outline:none;transition:border-color .2s;font-family:'Outfit',sans-serif;font-weight:600}
.add-input:focus{border-color:var(--accent)}
.icon-picker{display:flex;gap:7px;flex-wrap:wrap;justify-content:center;margin-bottom:14px}
.icon-opt{font-size:18px;cursor:pointer;padding:7px 9px;border-radius:9px;border:1.5px solid transparent;transition:all .15s;background:var(--surface3)}
.icon-opt:hover{border-color:var(--border2)}
.icon-opt.sel{border-color:var(--accent);background:rgba(59,130,246,.1)}
.add-profile-btns{display:flex;gap:8px}
.add-save-btn{flex:1;background:var(--grad);color:#fff;border:none;padding:12px;border-radius:10px;font-size:12px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif}
.add-cancel-btn{background:transparent;border:1px solid var(--border2);color:var(--text2);padding:12px 16px;border-radius:10px;font-size:12px;cursor:pointer;font-family:'Outfit',sans-serif}
#playerModal{position:fixed;inset:0;background:rgba(0,0,0,.98);display:none;align-items:center;justify-content:center;z-index:20000;padding:14px}
#playerModal.open{display:flex}
#playerWrap{width:100%;max-width:1100px;aspect-ratio:16/9;background:#000;border-radius:12px;overflow:hidden;position:relative;border:1px solid var(--border)}
#playerIframe{width:100%;height:100%;border:none}
.player-bar{position:absolute;top:-52px;right:0;display:flex;gap:7px;align-items:center}
.player-top-btn{background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.1);color:var(--text);padding:8px 14px;border-radius:9px;cursor:pointer;font-size:11px;font-weight:700;transition:all .15s;display:flex;align-items:center;gap:6px;font-family:'Outfit',sans-serif;letter-spacing:.3px}
.player-top-btn:hover{background:rgba(255,255,255,.15)}
.player-top-btn:active{background:rgba(255,255,255,.2)}
#playerControls{position:fixed;bottom:0;left:0;right:0;background:var(--surface);border-top:1px solid var(--border);z-index:20001;padding:18px 18px calc(18px + var(--sb));display:none;border-radius:20px 20px 0 0}
#playerControls.open{display:block}
.pc-handle{width:34px;height:4px;background:var(--surface4);border-radius:2px;margin:0 auto 16px}
.pc-title{font-family:'Bebas Neue',sans-serif;font-size:22px;letter-spacing:.8px;margin-bottom:18px;display:flex;align-items:center;justify-content:space-between}
.pc-close-btn{background:none;border:none;color:var(--text3);cursor:pointer;font-size:17px;padding:4px}
.pc-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
.pc-sec h4{font-size:9px;font-weight:900;text-transform:uppercase;color:var(--text3);letter-spacing:2px;margin-bottom:9px}
.pc-opts,.sub-opts{display:flex;flex-direction:column;gap:5px;max-height:185px;overflow-y:auto;scrollbar-width:thin}
.pc-opt,.sub-track{display:flex;align-items:center;justify-content:space-between;padding:9px 12px;background:var(--surface2);border-radius:9px;border:1px solid var(--border);cursor:pointer;transition:all .15s;font-size:11px;font-weight:600}
.pc-opt:hover,.sub-track:hover{background:var(--surface3);border-color:var(--border3)}
.pc-opt.sel,.sub-track.sel{border-color:rgba(59,130,246,.4);background:rgba(59,130,246,.07)}
.pc-check,.sub-check{color:var(--accent);font-size:12px;opacity:0}
.pc-opt.sel .pc-check,.sub-track.sel .sub-check{opacity:1}
.sub-flag{font-size:15px;flex-shrink:0;margin-right:7px}
.sub-name{flex:1}
#miniPlayer{position:fixed;bottom:calc(var(--nav-h) + 12px);right:13px;width:256px;height:145px;background:#000;border-radius:14px;overflow:hidden;z-index:25000;display:none;border:1px solid var(--border2);box-shadow:0 16px 40px rgba(0,0,0,.75)}
#miniPlayer.open{display:block}
#miniIframe{width:100%;height:100%;border:none}
.mini-controls{position:absolute;inset:0;background:rgba(0,0,0,0);transition:background .2s;display:flex;align-items:center;justify-content:center;gap:9px;opacity:0}
#miniPlayer:hover .mini-controls{background:rgba(0,0,0,.7);opacity:1}
.mini-btn{width:34px;height:34px;background:rgba(255,255,255,.1);border:1px solid rgba(255,255,255,.18);border-radius:8px;color:#fff;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:14px}
.mini-title{position:absolute;bottom:0;left:0;right:0;padding:20px 9px 6px;background:linear-gradient(to top,rgba(0,0,0,.97),transparent);font-size:9px;font-weight:700;color:#fff;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;letter-spacing:.2px}
#settingsModal{position:fixed;inset:0;background:rgba(0,0,0,.88);display:none;align-items:flex-end;justify-content:center;z-index:50000;backdrop-filter:blur(8px)}
#settingsModal.open{display:flex}
.settings-wrap{background:var(--surface);border-radius:22px 22px 0 0;width:100%;max-width:520px;max-height:88svh;overflow-y:auto;border:1px solid var(--border);border-bottom:none;scrollbar-width:thin;transform:translateY(100%);transition:transform .4s var(--spring)}
#settingsModal.open .settings-wrap{transform:translateY(0)}
.settings-handle{width:34px;height:4px;background:var(--surface4);border-radius:2px;margin:14px auto 0}
.settings-hd{padding:18px 20px 16px;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between}
.settings-hd-left{display:flex;align-items:center;gap:12px}
.settings-hd-icon{width:38px;height:38px;border-radius:11px;background:var(--surface2);border:1px solid var(--border2);display:flex;align-items:center;justify-content:center;font-size:16px;color:var(--text3)}
.settings-hd-title{font-family:'Bebas Neue',sans-serif;font-size:24px;letter-spacing:.8px}
.settings-hd-sub{font-size:10px;color:var(--text3);margin-top:1px;font-weight:600;letter-spacing:.3px}
.settings-close{background:var(--surface2);border:1px solid var(--border2);color:var(--text);width:32px;height:32px;border-radius:9px;cursor:pointer;font-size:13px;display:flex;align-items:center;justify-content:center;transition:all .15s}
.settings-close:hover{border-color:var(--border3)}
.settings-body{padding:18px 20px 30px;display:flex;flex-direction:column;gap:22px}
.settings-sec{border-bottom:1px solid var(--border);padding-bottom:20px}
.settings-sec:last-child{border-bottom:none;padding-bottom:0}
.settings-sec-title{font-size:9px;font-weight:900;text-transform:uppercase;letter-spacing:2.5px;color:var(--text3);margin-bottom:12px}
.settings-row{display:flex;align-items:center;justify-content:space-between;padding:11px 0;gap:14px;border-bottom:1px solid rgba(255,255,255,.025)}
.settings-row:last-child{border-bottom:none}
.settings-row-lbl{flex:1}
.settings-row-name{font-size:13px;font-weight:700;letter-spacing:-.1px}
.settings-row-desc{font-size:10px;color:var(--text3);line-height:1.5;margin-top:2px;font-weight:500}
.settings-select{background:var(--surface2);border:1px solid var(--border2);color:var(--text);border-radius:9px;padding:8px 26px 8px 11px;font-size:11px;font-weight:700;cursor:pointer;appearance:none;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='10' viewBox='0 0 12 12'%3E%3Cpath fill='%23666' d='M6 8L1 3h10z'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 9px center;outline:none;font-family:'Outfit',sans-serif;transition:border-color .15s}
.settings-select:focus{border-color:var(--accent)}
.toggle{position:relative;width:44px;height:24px;flex-shrink:0}
.toggle input{opacity:0;width:0;height:0;position:absolute}
.toggle-track{position:absolute;inset:0;background:var(--surface4);border-radius:12px;cursor:pointer;transition:all .2s;border:1px solid var(--border2)}
.toggle input:checked+.toggle-track{background:var(--accent);border-color:var(--accent)}
.toggle-track::after{content:'';position:absolute;left:3px;top:3px;width:16px;height:16px;background:#fff;border-radius:50%;transition:transform .2s var(--spring)}
.toggle input:checked+.toggle-track::after{transform:translateX(20px)}
.dev-cards{display:flex;flex-direction:column;gap:9px}
.dev-card{display:flex;align-items:center;gap:12px;background:var(--surface2);border:1px solid var(--border);border-radius:12px;padding:11px 14px}
.dev-avatar{width:40px;height:40px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:16px;flex-shrink:0;border:1px solid var(--border2);background:var(--surface3)}
.dev-name{font-size:13px;font-weight:800;letter-spacing:-.1px}
.dev-role{font-size:10px;color:var(--text3);font-weight:500}
.dev-badge{font-size:8px;font-weight:900;padding:2px 7px;border-radius:5px;background:rgba(59,130,246,.1);color:var(--accent);margin-top:4px;display:inline-block;text-transform:uppercase;letter-spacing:.8px;border:1px solid rgba(59,130,246,.2)}
.app-ver-row{display:flex;align-items:center;justify-content:space-between;background:var(--surface2);border-radius:9px;padding:10px 13px;border:1px solid var(--border);margin-bottom:6px}
.app-ver-lbl{font-size:10px;color:var(--text3);font-weight:800;text-transform:uppercase;letter-spacing:1px}
.app-ver-val{font-size:11px;font-weight:800;color:var(--text2)}
.settings-reset-btn{width:100%;background:transparent;border:1px solid rgba(239,68,68,.3);color:#ef4444;padding:13px;border-radius:10px;font-size:12px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .2s;text-transform:uppercase;letter-spacing:.8px;display:flex;align-items:center;justify-content:center;gap:9px}
.settings-reset-btn:hover{background:rgba(239,68,68,.07)}
.settings-reset-btn:active{background:rgba(239,68,68,.12)}
#starAppsPopup{position:fixed;inset:0;background:rgba(0,0,0,.9);display:none;align-items:flex-end;justify-content:center;z-index:60001;backdrop-filter:blur(10px)}
#starAppsPopup.open{display:flex}
.star-apps-wrap{background:var(--surface);border-radius:22px 22px 0 0;width:100%;max-width:460px;max-height:85svh;overflow-y:auto;border:1px solid var(--border);border-bottom:none;scrollbar-width:thin}
.star-apps-handle{width:34px;height:4px;background:var(--surface4);border-radius:2px;margin:14px auto 0}
.star-apps-hd{padding:18px 20px 14px;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;background:var(--surface);z-index:2}
.star-apps-hd-left{display:flex;align-items:center;gap:11px}
.star-apps-icon-wrap{width:36px;height:36px;border-radius:10px;background:var(--grad);display:flex;align-items:center;justify-content:center;font-size:16px;color:#fff;box-shadow:0 4px 12px rgba(59,130,246,.35)}
.star-apps-hd-title{font-family:'Bebas Neue',sans-serif;font-size:24px;letter-spacing:1px}
.star-apps-close{background:var(--surface2);border:1px solid var(--border2);color:var(--text);width:32px;height:32px;border-radius:9px;cursor:pointer;font-size:13px;display:flex;align-items:center;justify-content:center;transition:all .15s}
.star-apps-close:hover{border-color:var(--border3)}
.star-apps-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:11px;padding:16px 18px 20px}
.star-app-card{background:var(--surface2);border:1px solid var(--border);border-radius:14px;padding:18px 8px;cursor:pointer;transition:all .18s;display:flex;flex-direction:column;align-items:center;gap:9px;text-align:center}
.star-app-card:hover{border-color:var(--border3);background:var(--surface3);transform:translateY(-2px);box-shadow:0 8px 20px rgba(0,0,0,.2)}
.star-app-card:active{transform:scale(.96)}
.star-app-icon{width:44px;height:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:20px;background:var(--surface3);color:var(--text3);transition:all .18s;border:1px solid var(--border)}
.star-app-card:hover .star-app-icon{color:var(--accent);background:rgba(59,130,246,.1);border-color:rgba(59,130,246,.2)}
.star-app-name{font-size:11px;font-weight:800;letter-spacing:-.1px}
.star-app-desc{font-size:9px;color:var(--text3);line-height:1.4;font-weight:500}
#searchOverlay{position:fixed;inset:0;z-index:60000;background:var(--bg);display:flex;flex-direction:column;transform:translateY(100%);transition:transform .4s cubic-bezier(.22,1,.36,1);pointer-events:none}
#searchOverlay.active{transform:translateY(0);pointer-events:all}
#searchTopBar{display:flex;align-items:center;gap:11px;padding:calc(16px + var(--st)) 16px 0;flex-shrink:0}
#searchInputWrap{flex:1;display:flex;align-items:center;gap:9px;background:var(--surface2);border:1.5px solid var(--border2);border-radius:16px;padding:0 16px;height:50px;transition:border-color .2s}
#searchInputWrap:focus-within{border-color:var(--accent)}
#searchInputWrap .s-icon{font-size:15px;color:var(--text3);flex-shrink:0}
#searchOverlayInput{flex:1;background:none;border:none;outline:none;color:var(--text);font-size:16px;font-weight:600;font-family:'Outfit',sans-serif;caret-color:var(--accent)}
#searchOverlayInput::placeholder{color:var(--text3);font-weight:500}
#searchClearBtn{width:22px;height:22px;border-radius:50%;background:var(--text3);border:none;color:var(--bg);font-size:10px;display:none;align-items:center;justify-content:center;cursor:pointer;flex-shrink:0;transition:background .15s}
#searchClearBtn.vis{display:flex}
#searchCancelBtn{background:none;border:none;color:var(--accent);font-size:14px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;padding:6px 2px;white-space:nowrap;flex-shrink:0;letter-spacing:.2px}
#searchTabs{display:flex;padding:16px 16px 0;border-bottom:1px solid var(--border);flex-shrink:0;gap:0}
.s-tab{flex:1;text-align:center;padding:9px 4px;font-size:12px;font-weight:800;color:var(--text3);cursor:pointer;position:relative;border:none;background:none;font-family:'Outfit',sans-serif;transition:color .15s;letter-spacing:.3px;text-transform:uppercase}
.s-tab.on{color:var(--accent)}
.s-tab.on::after{content:'';position:absolute;bottom:-1px;left:25%;right:25%;height:2px;background:var(--grad);border-radius:1px}
#searchBody{flex:1;overflow-y:auto;scrollbar-width:none;-webkit-overflow-scrolling:touch;padding:18px 16px calc(18px + var(--sb))}
#searchBody::-webkit-scrollbar{display:none}
.s-section-hd{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px}
.s-section-label{font-size:10px;font-weight:900;text-transform:uppercase;letter-spacing:2px;color:var(--text3);display:flex;align-items:center;gap:7px}
.s-clear-btn{background:none;border:none;color:var(--text3);font-size:11px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;padding:3px 0;letter-spacing:.3px}
#trendingChips{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:24px}
.s-trend-chip{display:flex;align-items:center;gap:8px;background:var(--surface2);border:1px solid var(--border2);color:var(--text2);padding:9px 15px;border-radius:24px;font-size:12px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .15s}
.s-trend-chip:hover{background:rgba(59,130,246,.1);border-color:rgba(59,130,246,.3);color:var(--accent)}
.s-chip-icon{font-size:11px;color:var(--accent)}
#recentList{display:flex;flex-direction:column;gap:2px;margin-bottom:24px}
.s-recent-row{display:flex;align-items:center;gap:11px;padding:11px 7px;border-bottom:1px solid var(--border);cursor:pointer}
.s-recent-row:last-child{border-bottom:none}
.s-recent-row:active{background:var(--surface2);border-radius:10px;margin:0 -7px;padding:11px 14px}
.s-recent-ico{width:34px;height:34px;border-radius:9px;background:var(--surface2);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:13px;color:var(--text3);flex-shrink:0}
.s-recent-text{flex:1;font-size:13px;font-weight:700;color:var(--text2)}
.s-recent-del{width:30px;height:30px;border-radius:9px;background:none;border:none;color:var(--text3);font-size:13px;cursor:pointer;display:flex;align-items:center;justify-content:center;flex-shrink:0}
#categoryGrid{display:grid;grid-template-columns:repeat(2,1fr);gap:9px}
.s-cat-card{height:70px;border-radius:16px;cursor:pointer;display:flex;align-items:center;padding:0 16px;gap:12px;border:1px solid var(--border);background:var(--surface2);transition:all .15s;position:relative;overflow:hidden}
.s-cat-card:hover{border-color:var(--border3);transform:translateY(-1px)}
.s-cat-card:active{transform:scale(.97)}
.s-cat-icon{font-size:21px;flex-shrink:0;width:38px;height:38px;border-radius:11px;display:flex;align-items:center;justify-content:center;background:var(--surface3);transition:all .15s}
.s-cat-label{font-size:13px;font-weight:800;letter-spacing:-.1px}
#searchResultsBar{display:flex;align-items:center;gap:9px;padding:14px 0 12px;border-bottom:1px solid var(--border);margin-bottom:16px;flex-wrap:wrap}
.s-results-count{font-size:12px;color:var(--text3);font-weight:700;flex:1}
.s-results-count strong{color:var(--text);font-size:13px;font-weight:800}
.s-filter-row{display:flex;gap:7px;flex-wrap:wrap}
.s-filter-pill{background:var(--surface2);border:1px solid var(--border2);color:var(--text3);padding:6px 13px;border-radius:22px;font-size:11px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .15s;letter-spacing:.2px}
.s-filter-pill.on{background:rgba(59,130,246,.1);border-color:var(--accent);color:var(--accent)}
#searchResultsGrid{display:grid;grid-template-columns:repeat(3,1fr);gap:11px}
.sr-card{border-radius:12px;overflow:hidden;cursor:pointer;position:relative;background:var(--surface2);aspect-ratio:2/3;border:1px solid var(--border);transition:transform .15s}
.sr-card:hover{transform:scale(1.03)}
.sr-card:active{transform:scale(.97)}
.sr-card img{width:100%;height:100%;object-fit:cover;display:block}
.sr-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.97) 0%,rgba(0,0,0,.04) 55%,transparent 100%);display:flex;flex-direction:column;justify-content:flex-end;padding:8px 7px}
.sr-title{font-size:10px;font-weight:800;color:#fff;line-height:1.3;margin-bottom:3px;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;letter-spacing:.1px}
.sr-meta{font-size:8px;color:rgba(255,255,255,.5);display:flex;align-items:center;gap:3px;font-weight:600}
.sr-badge{position:absolute;top:6px;left:6px;background:rgba(59,130,246,.9);color:#fff;font-size:7px;font-weight:900;padding:2px 6px;border-radius:5px;text-transform:uppercase;letter-spacing:.8px}
.s-loading{grid-column:1/-1;display:flex;flex-direction:column;align-items:center;gap:16px;padding:55px 20px}
.s-spinner{width:30px;height:30px;border:2.5px solid var(--surface3);border-top-color:var(--accent);border-radius:50%;animation:spin .7s linear infinite}
.s-loading-txt{font-size:13px;color:var(--text3);font-weight:700;letter-spacing:.3px}
.s-empty{grid-column:1/-1;text-align:center;padding:55px 20px}
.s-empty-icon{font-size:42px;color:var(--text3);opacity:.3;margin-bottom:16px}
.s-empty h3{font-family:'Bebas Neue',sans-serif;font-size:28px;letter-spacing:1.5px;color:var(--text2);margin-bottom:7px}
.s-empty p{font-size:12px;color:var(--text3);line-height:1.65;font-weight:500}
.page-section{padding:calc(var(--hdr-h) + 16px) 0 calc(var(--nav-h) + 22px);display:none;min-height:100svh}
.page-section.active{display:block}
.page-inner{padding:0 16px}
.page-hd{display:flex;align-items:center;justify-content:space-between;margin-bottom:16px}
.back-btn{display:flex;align-items:center;gap:8px;background:var(--surface2);border:1px solid var(--border2);color:var(--text);padding:8px 14px;border-radius:10px;font-size:11px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .15s;letter-spacing:.2px}
.back-btn:hover{border-color:var(--border3)}
.upcoming-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:11px;margin-top:7px}
.upcoming-card{background:var(--surface);border-radius:14px;overflow:hidden;border:1px solid var(--border);cursor:pointer;transition:all .15s}
.upcoming-card:hover{border-color:var(--border3);transform:translateY(-2px)}
.upcoming-card:active{transform:scale(.98)}
.upcoming-poster{width:100%;height:125px;object-fit:cover}
.upcoming-info{padding:11px}
.upcoming-title{font-size:11px;font-weight:800;margin-bottom:4px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;letter-spacing:-.1px}
.upcoming-date{font-size:9px;color:var(--text3);font-weight:700;margin-bottom:4px;display:flex;align-items:center;gap:5px}
.upcoming-overview{font-size:9px;color:var(--text3);line-height:1.45;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden;font-weight:400}
.upcoming-countdown{background:rgba(59,130,246,.1);border-radius:6px;padding:4px 8px;font-size:9px;font-weight:900;color:var(--accent);display:inline-flex;align-items:center;gap:5px;margin-top:7px;border:1px solid rgba(59,130,246,.2);letter-spacing:.3px}
.history-grid{display:flex;flex-direction:column;gap:9px;margin-top:7px}
.history-item{display:flex;gap:11px;align-items:center;background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:11px;cursor:pointer;transition:all .15s}
.history-item:hover{border-color:var(--border3)}
.history-poster{width:44px;height:66px;border-radius:7px;object-fit:cover;flex-shrink:0;background:var(--surface2);border:1px solid var(--border)}
.history-info{flex:1;min-width:0}
.history-title{font-size:12px;font-weight:800;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;margin-bottom:3px;letter-spacing:-.1px}
.history-meta{font-size:9px;color:var(--text3);display:flex;gap:5px;align-items:center;flex-wrap:wrap;margin-bottom:3px;font-weight:600}
.history-time{font-size:9px;color:var(--text3);font-weight:500}
.history-badge{background:rgba(59,130,246,.1);padding:2px 7px;border-radius:5px;font-size:8px;font-weight:900;text-transform:uppercase;border:1px solid rgba(59,130,246,.2);color:var(--accent);letter-spacing:.5px}
.history-del-btn{background:none;border:none;color:var(--text3);cursor:pointer;font-size:14px;padding:7px;border-radius:8px;flex-shrink:0;transition:all .15s}
.history-del-btn:hover{background:var(--surface2);color:var(--text)}
.filter-row{display:flex;gap:7px;margin-bottom:14px;flex-wrap:wrap;align-items:center}
.filter-btn{background:var(--surface2);border:1px solid var(--border);color:var(--text3);padding:7px 15px;border-radius:22px;font-size:10px;font-weight:800;cursor:pointer;transition:all .15s;font-family:'Outfit',sans-serif;letter-spacing:.3px}
.filter-btn.on{background:rgba(59,130,246,.1);border-color:rgba(59,130,246,.4);color:var(--accent)}
.clear-btn{margin-left:auto;background:none;border:1px solid rgba(239,68,68,.3);color:#ef4444;padding:7px 13px;border-radius:22px;font-size:10px;font-weight:800;cursor:pointer;font-family:'Outfit',sans-serif}
.mylist-empty{text-align:center;padding:65px 20px;color:var(--text3)}
.mylist-empty i{font-size:44px;margin-bottom:16px;display:block;opacity:.25}
.mylist-empty h3{font-family:'Bebas Neue',sans-serif;font-size:26px;color:var(--text2);letter-spacing:1.5px;margin-bottom:7px}
.mylist-empty p{font-size:12px;line-height:1.65;font-weight:500}
#discoverSection{padding:30px 16px;border-top:1px solid var(--border)}
.discover-hd{text-align:center;margin-bottom:26px}
.discover-hd h2{font-family:'Bebas Neue',sans-serif;font-size:clamp(28px,7vw,44px);letter-spacing:2px;margin-bottom:9px;background:linear-gradient(135deg,var(--text),var(--text2));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text}
.discover-hd p{color:var(--text3);font-size:12px;max-width:320px;margin:0 auto;line-height:1.7;font-weight:500}
.discover-stats{display:flex;justify-content:center;gap:32px;margin-top:20px;flex-wrap:wrap}
.stat-val{font-family:'Bebas Neue',sans-serif;font-size:32px;letter-spacing:1.5px;background:var(--grad);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;display:block;margin-bottom:3px}
.stat-lbl{font-size:9px;color:var(--text3);text-transform:uppercase;letter-spacing:2.5px;font-weight:800}
.discover-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:9px;margin-bottom:26px}
.load-more-wrap{text-align:center;padding:12px 0}
.load-more-btn{background:transparent;color:var(--text2);border:1px solid var(--border2);padding:13px 34px;border-radius:12px;font-size:11px;font-weight:800;cursor:pointer;transition:all .2s;display:inline-flex;align-items:center;gap:9px;text-transform:uppercase;letter-spacing:1.5px;font-family:'Outfit',sans-serif}
.load-more-btn:hover{border-color:var(--border3);color:var(--accent)}
.fab{position:fixed;bottom:calc(var(--nav-h) + 14px);width:44px;height:44px;border-radius:12px;display:flex;align-items:center;justify-content:center;cursor:pointer;z-index:400;border:1px solid var(--border2);backdrop-filter:blur(14px);transition:all .2s}
.fab:hover{transform:scale(1.08)}
.fab-discord{left:calc(13px + var(--sl));background:rgba(88,101,242,.22)}
.fab-tiktok{left:calc(66px + var(--sl));background:rgba(0,0,0,.75)}
.fab svg{width:20px;height:20px}
#continueInline{display:none;padding:0 16px;margin:18px 0 0}
#continueInline .section-hd{margin-bottom:14px}
.toast{position:fixed;bottom:calc(var(--nav-h) + 16px);left:50%;transform:translateX(-50%) translateY(60px);background:var(--surface3);color:var(--text);padding:11px 20px;border-radius:24px;border:1px solid var(--border2);z-index:30000;opacity:0;transition:all .35s var(--spring);font-weight:700;font-size:12px;box-shadow:0 10px 28px rgba(0,0,0,.5);pointer-events:none;white-space:nowrap;backdrop-filter:blur(14px);letter-spacing:.2px}
.toast.vis{opacity:1;transform:translateX(-50%) translateY(0)}
.spinner-wrap{display:flex;justify-content:center;padding:38px}
.spinner{width:28px;height:28px;border:2.5px solid var(--surface3);border-top-color:var(--accent);border-radius:50%;animation:spin .75s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
.empty{color:var(--text3);padding:38px;text-align:center;font-size:12px;width:100%;font-weight:500}
body::before{content:'';position:fixed;top:-25%;left:-18%;width:55%;height:65%;background:radial-gradient(ellipse,rgba(59,130,246,.04) 0%,transparent 70%);pointer-events:none;z-index:0}
body::after{content:'';position:fixed;bottom:-18%;right:-14%;width:48%;height:58%;background:radial-gradient(ellipse,rgba(139,92,246,.03) 0%,transparent 70%);pointer-events:none;z-index:0}
</style>
</head>
<body>

<div id="popupPermissionModal">
  <div class="ppm-box">
    <div class="ppm-top">
      <div class="ppm-icon-ring"><i class="fa-solid fa-star"></i></div>
      <div class="ppm-logo"><i class="fa-solid fa-star" style="font-size:18px;color:#fff;margin-right:7px;-webkit-text-fill-color:#fff"></i>STARSTREAM</div>
    </div>
    <div class="ppm-body">
      <div class="ppm-title">Allow Popups to Continue</div>
      <div class="ppm-desc">StarStream opens Star Apps and streaming content in new windows. Please allow popups so everything works correctly.</div>
      <div class="ppm-info-cards">
        <div class="ppm-info-card"><div class="ppm-info-icon blue"><i class="fa-solid fa-star"></i></div><div class="ppm-info-text"><strong>Star Apps</strong> — Sports, TV, Music, Documentary &amp; more open in new windows.</div></div>
        <div class="ppm-info-card"><div class="ppm-info-icon purple"><i class="fa-solid fa-film"></i></div><div class="ppm-info-text"><strong>Trailers</strong> — YouTube previews launch in a new tab instantly.</div></div>
        <div class="ppm-info-card"><div class="ppm-info-icon cyan"><i class="fa-solid fa-shield-halved"></i></div><div class="ppm-info-text"><strong>Safe &amp; Private</strong> — We never open ads or unsolicited windows.</div></div>
      </div>
      <button class="ppm-btn" onclick="agreePopups()"><i class="fa-solid fa-check-circle"></i> I Agree — Allow Popups</button>
      <button class="ppm-skip" onclick="skipPopups()">Skip for now</button>
    </div>
  </div>
</div>

<div id="startupTip" style="display:none">
  <div class="tip-box">
    <div class="tip-top"><div><div class="tip-logo"><i class="fa-solid fa-star" style="color:#fff;-webkit-text-fill-color:#fff"></i>STARSTREAM</div><div class="tip-tagline">Quick tips before you dive in</div></div></div>
    <div class="tip-body">
      <div class="tip-card"><div class="tip-card-ico"><i class="fa-solid fa-hourglass-half"></i></div><div><h3>Content keeps buffering?</h3><p>Try <strong>switching servers</strong> in the header or restart your browser.</p></div></div>
      <div class="tip-card"><div class="tip-card-ico"><i class="fa-solid fa-shield-halved"></i></div><div><h3>Best Experience</h3><p>Use <strong>AutoEmbed</strong> or <strong>Star-Stream FLixy</strong> for cleaner playback.</p></div></div>
    </div>
    <div class="tip-footer"><div class="tip-countdown" id="tipCountNum">10</div><button class="tip-dismiss" onclick="dismissTip()"><i class="fa-solid fa-rocket"></i> Let's Go!</button></div>
  </div>
</div>

<div id="confirmModal">
  <div class="confirm-box">
    <div class="confirm-msg"><h3 id="confirmTitle">Are you sure?</h3><p id="confirmDesc"></p></div>
    <div class="confirm-actions"><button class="confirm-cancel" id="confirmCancel">Cancel</button><button class="confirm-ok" id="confirmOk">Confirm</button></div>
  </div>
</div>

<div id="starAppsPopup" onclick="if(event.target===this)closeStarApps()">
  <div class="star-apps-wrap" onclick="event.stopPropagation()">
    <div class="star-apps-handle"></div>
    <div class="star-apps-hd">
      <div class="star-apps-hd-left"><div class="star-apps-icon-wrap"><i class="fa-solid fa-star"></i></div><div class="star-apps-hd-title">Star Apps</div></div>
      <button class="star-apps-close" onclick="closeStarApps()"><i class="fa-solid fa-xmark"></i></button>
    </div>
    <div class="star-apps-grid">
      <div class="star-app-card" onclick="openStarApp('sports')"><div class="star-app-icon"><i class="fa-solid fa-trophy"></i></div><span class="star-app-name">Star-Sports</span><span class="star-app-desc">Live sports</span></div>
      <div class="star-app-card" onclick="openStarApp('tv')"><div class="star-app-icon"><i class="fa-solid fa-satellite-dish"></i></div><span class="star-app-name">Star-TV</span><span class="star-app-desc">Live TV</span></div>
      <div class="star-app-card" onclick="openStarApp('music')"><div class="star-app-icon"><i class="fa-solid fa-music"></i></div><span class="star-app-name">Star-Music</span><span class="star-app-desc">Stream music</span></div>
      <div class="star-app-card" onclick="openStarApp('podcast')"><div class="star-app-icon"><i class="fa-solid fa-microphone-lines"></i></div><span class="star-app-name">Star-Podcast</span><span class="star-app-desc">Podcasts</span></div>
      <div class="star-app-card" onclick="openStarApp('news')"><div class="star-app-icon"><i class="fa-solid fa-newspaper"></i></div><span class="star-app-name">Star-News</span><span class="star-app-desc">Latest news</span></div>
      <div class="star-app-card" onclick="openStarApp('radio')"><div class="star-app-icon"><i class="fa-solid fa-radio"></i></div><span class="star-app-name">Star-Radio</span><span class="star-app-desc">Live radio</span></div>
      <div class="star-app-card" onclick="openStarApp('books')"><div class="star-app-icon"><i class="fa-solid fa-book"></i></div><span class="star-app-name">Star-Books</span><span class="star-app-desc">eBooks</span></div>
      <div class="star-app-card" onclick="openStarApp('documentary')"><div class="star-app-icon"><i class="fa-solid fa-film"></i></div><span class="star-app-name">Star-Documentary</span><span class="star-app-desc">Documentaries</span></div>
    </div>
  </div>
</div>

<div id="searchOverlay">
  <div id="searchTopBar">
    <div id="searchInputWrap">
      <span class="s-icon"><i class="fa-solid fa-magnifying-glass"></i></span>
      <input id="searchOverlayInput" type="search" placeholder="Movies, shows, actors…" autocomplete="off" spellcheck="false" autocorrect="off"/>
      <button id="searchClearBtn"><i class="fa-solid fa-xmark"></i></button>
    </div>
    <button id="searchCancelBtn" onclick="closeSearchOverlay()">Cancel</button>
  </div>
  <div id="searchTabs">
    <button class="s-tab on" id="sTab-discover" onclick="switchSearchTab('discover')">Discover</button>
    <button class="s-tab" id="sTab-results" onclick="switchSearchTab('results')">Results</button>
  </div>
  <div id="searchBody">
    <div id="searchDiscoverView">
      <div id="recentSection" style="display:none;margin-bottom:24px">
        <div class="s-section-hd"><div class="s-section-label"><i class="fa-regular fa-clock"></i> Recent</div><button class="s-clear-btn" onclick="clearRecentSearches()">Clear all</button></div>
        <div id="recentList"></div>
      </div>
      <div style="margin-bottom:24px"><div class="s-section-hd"><div class="s-section-label"><i class="fa-solid fa-fire-alt"></i> Trending Searches</div></div><div id="trendingChips"></div></div>
      <div><div class="s-section-hd"><div class="s-section-label"><i class="fa-solid fa-compass"></i> Browse by Genre</div></div><div id="categoryGrid"></div></div>
    </div>
    <div id="searchResultsView" style="display:none"><div id="searchResultsBar"></div><div id="searchResultsGrid"></div></div>
  </div>
</div>

<a href="https://discord.gg/Yk6K4TkEm" target="_blank" class="fab fab-discord" title="Discord">
  <svg viewBox="0 0 24 24" fill="white"><path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057a.082.082 0 0 0 .031.057 19.9 19.9 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028c.462-.63.874-1.295 1.226-1.994a.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/></svg>
</a>
<a href="https://www.tiktok.com/@gnstream0" target="_blank" class="fab fab-tiktok" title="TikTok">
  <svg viewBox="0 0 24 24"><path d="M19.59 6.69a4.83 4.83 0 0 1-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 0 1-2.88 2.5 2.89 2.89 0 0 1-2.89-2.89 2.89 2.89 0 0 1 2.89-2.89c.28 0 .54.04.79.1V9.01a6.34 6.34 0 0 0-.79-.05 6.34 6.34 0 0 0-6.34 6.34 6.34 6.34 0 0 0 6.34 6.34 6.34 6.34 0 0 0 6.33-6.34V8.69a8.18 8.18 0 0 0 4.78 1.52V6.75a4.85 4.85 0 0 1-1.01-.06z" fill="white"/></svg>
</a>

<div id="profilesModal" onclick="if(event.target===this)closeProfiles()">
  <div class="profiles-wrap" onclick="event.stopPropagation()">
    <div class="profiles-main-title">Who's watching?</div>
    <div class="profiles-subtitle">Select your profile</div>
    <div class="add-profile-form" id="addProfileForm">
      <h3>New Profile</h3>
      <input class="add-input" id="newProfileName" type="text" placeholder="Profile name" maxlength="14" autocomplete="off"/>
      <div style="font-size:9px;color:var(--text3);margin-bottom:9px;font-weight:900;text-transform:uppercase;letter-spacing:1px">Choose icon</div>
      <div class="icon-picker" id="iconPicker"></div>
      <div class="add-profile-btns"><button class="add-cancel-btn" onclick="hideAddProfileForm()">Cancel</button><button class="add-save-btn" onclick="saveNewProfile()">Create</button></div>
    </div>
    <div class="profiles-grid" id="profilesGrid"></div>
    <div class="profiles-footer">
      <button class="profiles-manage-btn" onclick="showAddProfileForm()"><i class="fa-solid fa-plus"></i> Add Profile</button>
      <button class="profiles-manage-btn" onclick="closeProfiles()">Done</button>
    </div>
  </div>
</div>

<div id="playerControls">
  <div class="pc-handle"></div>
  <div class="pc-title"><span><i class="fa-solid fa-sliders"></i> Playback</span><button class="pc-close-btn" onclick="closePlayerControls()"><i class="fa-solid fa-xmark"></i></button></div>
  <div class="pc-grid">
    <div class="pc-sec"><h4>Speed</h4><div class="pc-opts" id="speedOpts">
      <div class="pc-opt" onclick="setSpeed(0.5,this)"><span>0.5×</span><span class="pc-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="pc-opt" onclick="setSpeed(0.75,this)"><span>0.75×</span><span class="pc-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="pc-opt sel" onclick="setSpeed(1,this)"><span>1× Normal</span><span class="pc-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="pc-opt" onclick="setSpeed(1.25,this)"><span>1.25×</span><span class="pc-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="pc-opt" onclick="setSpeed(1.5,this)"><span>1.5×</span><span class="pc-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="pc-opt" onclick="setSpeed(2,this)"><span>2×</span><span class="pc-check"><i class="fa-solid fa-check"></i></span></div>
    </div></div>
    <div class="pc-sec"><h4>Subtitles</h4><div class="sub-opts" id="subOpts">
      <div class="sub-track sel" onclick="setSub('off',this)"><span class="sub-flag"><i class="fa-solid fa-ban"></i></span><span class="sub-name">Off</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('en',this)"><span class="sub-flag">🇺🇸</span><span class="sub-name">English</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('es',this)"><span class="sub-flag">🇪🇸</span><span class="sub-name">Spanish</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('fr',this)"><span class="sub-flag">🇫🇷</span><span class="sub-name">French</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('de',this)"><span class="sub-flag">🇩🇪</span><span class="sub-name">German</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('ja',this)"><span class="sub-flag">🇯🇵</span><span class="sub-name">Japanese</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('pt',this)"><span class="sub-flag">🇧🇷</span><span class="sub-name">Portuguese</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
      <div class="sub-track" onclick="setSub('ko',this)"><span class="sub-flag">🇰🇷</span><span class="sub-name">Korean</span><span class="sub-check"><i class="fa-solid fa-check"></i></span></div>
    </div></div>
  </div>
</div>

<div id="settingsModal" onclick="if(event.target===this)closeSettings()">
  <div class="settings-wrap" onclick="event.stopPropagation()">
    <div class="settings-handle"></div>
    <div class="settings-hd">
      <div class="settings-hd-left"><div class="settings-hd-icon"><i class="fa-solid fa-gear"></i></div><div><div class="settings-hd-title">Settings</div><div class="settings-hd-sub">Customize StarStream</div></div></div>
      <button class="settings-close" onclick="closeSettings()"><i class="fa-solid fa-xmark"></i></button>
    </div>
    <div class="settings-body">
      <div class="settings-sec">
        <div class="settings-sec-title">Appearance</div>
        <div class="settings-row"><div class="settings-row-lbl"><div class="settings-row-name">Theme</div><div class="settings-row-desc">Dark or light mode</div></div><select class="settings-select" id="themeSelect" onchange="applyTheme(this.value)"><option value="dark">Dark</option><option value="light">Light</option></select></div>
      </div>
      <div class="settings-sec">
        <div class="settings-sec-title">Playback</div>
        <div class="settings-row"><div class="settings-row-lbl"><div class="settings-row-name">Default Server</div><div class="settings-row-desc">Streaming server preference</div></div><select class="settings-select" id="settingsServerSelect" onchange="changeServer(this.value)"><option value="1">AutoEmbed Test</option><option value="2">AutoEmbed Player</option><option value="3">Star-Stream FLixy</option><option value="4">Star Stream flixy 2</option><option value="5">2Embed</option><option value="6">MultiEmbed</option><option value="7">Embed.su</option><option value="8">VidSrc.xyz</option><option value="9">VidSrc.me</option><option value="10">VidSrc.in</option></select></div>
        <div class="settings-row"><div class="settings-row-lbl"><div class="settings-row-name">Autoplay Next</div><div class="settings-row-desc">Continue watching automatically</div></div><label class="toggle"><input type="checkbox" id="autoplayToggle" checked onchange="saveSetting('autoplay',this.checked)"><span class="toggle-track"></span></label></div>
      </div>
      <div class="settings-sec">
        <div class="settings-sec-title">Dev Team</div>
        <div class="dev-cards">
          <div class="dev-card"><div class="dev-avatar"><i class="fa-solid fa-code"></i></div><div><div class="dev-name">Corbini</div><div class="dev-role">Lead Dev · UI/UX</div><div class="dev-badge">Founder</div></div></div>
          <div class="dev-card"><div class="dev-avatar"><i class="fa-solid fa-robot"></i></div><div><div class="dev-name">VXII/System</div><div class="dev-role">Backend · Systems</div><div class="dev-badge">Co-Dev</div></div></div>
        </div>
        <div style="margin-top:14px"><div class="app-ver-row"><span class="app-ver-lbl">Version</span><span class="app-ver-val">Star-Stream v2.2.1-proxy</span></div><div class="app-ver-row"><span class="app-ver-lbl">Data Source</span><span class="app-ver-val">TMDB API</span></div></div>
      </div>
      <div class="settings-sec"><div class="settings-sec-title">Data</div><button class="settings-reset-btn" onclick="clearAllData()"><i class="fa-solid fa-trash-can"></i> Clear All Local Data</button></div>
    </div>
  </div>
</div>

<header id="mainHeader">
  <div class="logo" onclick="showHome()"><div class="logo-star"><i class="fa-solid fa-star" style="-webkit-text-fill-color:#fff"></i></div>STARSTREAM</div>
  <div class="srv-pill"><div class="srv-dot"></div><span class="srv-label">Srv</span><select id="serverSelect" class="srv-select" onchange="changeServer(this.value)"><option value="1">AutoEmbed Test</option><option value="2">AutoEmbed Player</option><option value="3">Star-Stream FLixy</option><option value="4">Star-stream flixy 2</option><option value="5">2Embed</option><option value="6">MultiEmbed</option><option value="7">Embed.su</option><option value="8">VidSrc.xyz</option><option value="9">VidSrc.me</option><option value="10">VidSrc.in</option></select></div>
  <div class="hdr-right"><button class="h-btn" onclick="openSearchOverlay()"><i class="fa-solid fa-magnifying-glass"></i></button><button class="h-btn" onclick="openSettings()"><i class="fa-solid fa-gear"></i></button><button class="h-profile-btn" onclick="openProfiles()" id="headerProfile"><i class="fa-solid fa-user"></i></button></div>
</header>

<nav id="bottomNav">
  <button class="nav-tab on" id="tab-home" onclick="showHome();setTab('home')"><div class="nav-tab-icon"><i class="fa-solid fa-house"></i></div><span class="nav-tab-label">Home</span><div class="nav-tab-active-bar"></div></button>
  <button class="nav-tab" id="tab-search" onclick="openSearchOverlay()"><div class="nav-tab-icon"><i class="fa-solid fa-magnifying-glass"></i></div><span class="nav-tab-label">Search</span><div class="nav-tab-active-bar"></div></button>
  <button class="nav-tab" id="tab-mylist" onclick="showMyList();setTab('mylist')"><div class="nav-tab-icon"><i class="fa-solid fa-bookmark"></i><span class="nav-badge" id="myListBadge"></span></div><span class="nav-tab-label">My List</span><div class="nav-tab-active-bar"></div></button>
  <button class="nav-tab" id="tab-apps" onclick="openStarApps()"><div class="nav-tab-icon"><i class="fa-solid fa-star"></i></div><span class="nav-tab-label">Apps</span><div class="nav-tab-active-bar"></div></button>
  <button class="nav-tab" id="tab-profile" onclick="openProfiles()"><div class="nav-tab-icon" id="tabProfileIcon"><i class="fa-solid fa-user"></i></div><span class="nav-tab-label">Profile</span><div class="nav-tab-active-bar"></div></button>
</nav>

<div id="mainContent">
  <div id="heroSection">
    <div class="hero-bg" id="heroBg"></div>
    <div class="hero-content">
      <div class="hero-eyebrow" id="heroEyebrow"><i class="fa-solid fa-fire-alt"></i> #1 Trending</div>
      <div class="hero-title" id="heroTitle">Loading…</div>
      <div class="hero-meta" id="heroMeta"></div>
      <p class="hero-overview" id="heroOverview"></p>
      <div class="hero-btns">
        <button class="btn-play" onclick="heroPlay()"><svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg>Play</button>
        <button class="btn-info" onclick="heroMoreInfo()"><i class="fa-solid fa-circle-info"></i> Info</button>
        <button class="btn-icon-hero" id="heroListBtn" onclick="heroToggleList()"><i class="fa-solid fa-plus"></i></button>
      </div>
    </div>
    <div class="hero-dots" id="heroDots"></div>
  </div>
  <div id="continueInline"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Continue Watching</div><div class="view-all" onclick="clearContinueConfirm()">Clear <i class="fa-solid fa-xmark"></i></div></div><div class="row" id="continueInlineRow"></div></div>
  <div id="homeContent">
    <div class="section" id="sec-hot"><div class="section-hd"><div class="section-title"><div class="stbar"></div> What's Hot</div></div><div class="hot-grid" id="hotGrid"></div></div>
    <div class="section" id="sec-trending"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Trending Now</div></div><div class="row" id="trendingRow"></div></div>
    <div class="section" id="sec-top10"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Top 10 This Week</div></div><div class="row" id="top10Row" style="padding-bottom:22px"></div></div>
    <div class="section" id="sec-newrel"><div class="section-hd"><div class="section-title"><div class="stbar"></div> New Releases</div></div><div class="row" id="newRelRow"></div></div>
    <div class="section" id="sec-action"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Action</div></div><div class="row" id="actionRow"></div></div>
    <div class="section" id="sec-comedy"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Comedy</div></div><div class="row" id="comedyRow"></div></div>
    <div class="section" id="sec-horror"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Horror</div></div><div class="row" id="horrorRow"></div></div>
    <div class="section" id="sec-scifi"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Sci-Fi</div></div><div class="row" id="scifiRow"></div></div>
    <div class="section" id="sec-romance"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Romance</div></div><div class="row" id="romanceRow"></div></div>
    <div class="section" id="sec-thriller"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Thriller</div></div><div class="row" id="thrillerRow"></div></div>
    <div class="section" id="sec-drama"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Drama</div></div><div class="row" id="dramaRow"></div></div>
    <div class="section" id="sec-anim"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Animation</div></div><div class="row" id="animRow"></div></div>
    <div class="section" id="sec-doc"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Documentary</div></div><div class="row" id="docRow"></div></div>
    <div class="section" id="sec-crime"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Crime</div></div><div class="row" id="crimeRow"></div></div>
    <div class="section" id="sec-mystery"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Mystery</div></div><div class="row" id="mysteryRow"></div></div>
    <div class="section" id="sec-fantasy"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Fantasy</div></div><div class="row" id="fantasyRow"></div></div>
    <div class="section" id="sec-family"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Family</div></div><div class="row" id="familyRow"></div></div>
    <div class="section" id="sec-adv"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Adventure</div></div><div class="row" id="advRow"></div></div>
    <div class="section" id="sec-movies"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Popular Movies</div></div><div class="row" id="moviesRow"></div></div>
    <div class="section" id="sec-tv"><div class="section-hd"><div class="section-title"><div class="stbar"></div> TV Shows</div></div><div class="row" id="tvRow"></div></div>
    <div class="section" id="sec-kdrama"><div class="section-hd"><div class="section-title"><div class="stbar"></div> K-Drama</div></div><div class="row" id="kdramaRow"></div></div>
    <div class="section" id="sec-anime"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Anime</div></div><div class="row" id="animeRow"></div></div>
    <div class="section" id="sec-award"><div class="section-hd"><div class="section-title"><div class="stbar"></div> Award Winners</div></div><div class="row" id="awardRow"></div></div>
  </div>
  <div id="discoverSection">
    <div class="discover-hd"><h2>Discover More</h2><p>Explore our massive library — updated daily with the latest releases</p><div class="discover-stats"><div><span class="stat-val" id="discoverCount">0+</span><span class="stat-lbl">Loaded</span></div><div><span class="stat-val">25+</span><span class="stat-lbl">Genres</span></div><div><span class="stat-val">Daily</span><span class="stat-lbl">Updated</span></div></div></div>
    <div class="discover-grid" id="discoverGrid"></div>
    <div class="load-more-wrap"><button class="load-more-btn" id="loadMoreBtn" onclick="loadMore()"><i class="fa-solid fa-arrow-down"></i> <span>Load More</span></button></div>
  </div>
  <div id="upcomingPage" class="page-section"><div class="page-inner"><div class="page-hd"><div class="section-title"><div class="stbar"></div> Upcoming</div><button class="back-btn" onclick="showHome()"><i class="fa-solid fa-arrow-left"></i> Back</button></div><div class="upcoming-grid" id="upcomingGrid"></div></div></div>
  <div id="myListPage" class="page-section"><div class="page-inner"><div class="page-hd"><div class="section-title"><div class="stbar"></div> My List</div></div><div id="myListContent"></div></div></div>
  <div id="historyPage" class="page-section"><div class="page-inner"><div class="page-hd"><div class="section-title"><div class="stbar"></div> Watch History</div><button class="back-btn" onclick="showHome()"><i class="fa-solid fa-arrow-left"></i> Back</button></div><div class="filter-row"><button class="filter-btn on" onclick="filterHistory('all',this)">All</button><button class="filter-btn" onclick="filterHistory('movie',this)">Movies</button><button class="filter-btn" onclick="filterHistory('tv',this)">TV Shows</button><button class="clear-btn" onclick="clearFullHistoryConfirm()"><i class="fa-solid fa-trash-can"></i> Clear</button></div><div class="history-grid" id="historyGrid"></div></div></div>
</div>

<!-- ══ DETAILS MODAL ── -->
<div id="detailsModal" onclick="closeDetailsBd(event)">
  <button class="close-btn" onclick="closeDetails()"><i class="fa-solid fa-xmark"></i></button>
  <div id="detailsBox" onclick="event.stopPropagation()">
    <div class="details-handle"></div>
    <div class="details-hero">
      <img class="details-poster" id="detailsPoster" src="" alt="">
      <div class="details-grad"></div>
      <button class="details-trailer-btn" onclick="playModalTrailer()"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></button>
    </div>
    <div class="details-info">
      <div class="details-title" id="detailsTitle"></div>
      <div class="details-meta-row">
        <span class="d-match" id="detailsMatch">98% Match</span>
        <span id="detailsYear"></span>
        <span id="detailsRuntime"></span>
        <span class="d-cert" id="detailsCert">NR</span>
        <span id="detailsGenre"></span>
      </div>
      <!-- ══ ACTIONS ROW — Play + My List + Download + NEW Open in New Tab ══ -->
      <div class="details-actions">
        <button class="btn-d btn-d-play" onclick="playContent()"><i class="fa-solid fa-play"></i> Play</button>
        <button class="btn-d btn-d-list" id="detailsListBtn" onclick="toggleListFromDetails()"><i class="fa-solid fa-plus"></i> My List</button>
        <button class="btn-d btn-d-dl" onclick="downloadContent()" title="Download"><i class="fa-solid fa-download"></i></button>
        <button class="btn-d btn-d-newtab" onclick="openInNewTab()" title="If the player does not load, open in a new tab (recommended)">
          <i class="fa-solid fa-arrow-up-right-from-square"></i> New Tab
          <span style="font-size:9px;opacity:.6;font-weight:600">(if not loading)</span>
        </button>
      </div>
    </div>
    <div id="detailsBody">
      <div class="details-sec"><h3>About</h3><p id="detailsOverview"></p></div>
      <div class="details-sec"><h3>Cast</h3><div class="cast-chips" id="detailsCast"></div></div>
    </div>
    <div class="ep-section" id="epSection" style="display:none">
      <div class="ep-hd">
        <div class="ep-hd-title">Episodes</div>
        <div class="season-wrap"><label>Season</label><select id="seasonDropdown" class="season-dd" onchange="onSeasonChange()"></select></div>
      </div>
      <div class="ep-grid" id="epGrid"></div>
    </div>
    <div class="paw-section" id="pawSection" style="display:none"><div class="paw-title">People Also Watched</div><div class="paw-row" id="pawRow"></div></div>
    <div class="recs-section"><div class="recs-title">More Like This</div><div class="recs-row" id="recsRow"></div></div>
  </div>
</div>

<!-- ══ PLAYER ── -->
<div id="playerModal" onclick="closePlayerBd(event)">
  <div id="playerWrap" onclick="event.stopPropagation()">
    <div class="player-bar">
      <button class="player-top-btn" onclick="openPlayerControls()"><i class="fa-solid fa-sliders"></i> Settings</button>
      <button class="player-top-btn" onclick="launchMini()"><i class="fa-solid fa-window-minimize"></i> Mini</button>
      <button class="player-top-btn" onclick="toggleFullscreen()" id="fsBtn"><i class="fa-solid fa-expand"></i> Full</button>
      <button class="player-top-btn" onclick="closePlayer()"><i class="fa-solid fa-xmark"></i> Close</button>
    </div>
    <iframe id="playerIframe" allowfullscreen allow="fullscreen; autoplay; encrypted-media; scripts; forms; popups; same-origin; top-navigation" referrerpolicy="no-referrer"></iframe>
  </div>
</div>

<div id="miniPlayer">
  <iframe id="miniIframe" allowfullscreen></iframe>
  <div class="mini-controls"><button class="mini-btn" onclick="expandMini()"><i class="fa-solid fa-expand"></i></button><button class="mini-btn" onclick="closeMini()"><i class="fa-solid fa-xmark"></i></button></div>
  <div class="mini-title" id="miniTitle">Now Playing</div>
</div>

<div class="toast" id="toast"></div>

<script>
function agreePopups(){localStorage.setItem('gnPopupAgreed','1');const modal=document.getElementById('popupPermissionModal');modal.style.transition='opacity .4s ease,transform .4s ease';modal.style.opacity='0';modal.style.transform='scale(.96)';setTimeout(()=>{modal.style.display='none';showStartupTip();},420);try{const t=window.open('about:blank','_blank');if(t)t.close();}catch(e){}toast('✓ Popups enabled — enjoy StarStream!');}
function skipPopups(){localStorage.setItem('gnPopupAgreed','skip');const modal=document.getElementById('popupPermissionModal');modal.style.transition='opacity .35s ease';modal.style.opacity='0';setTimeout(()=>{modal.style.display='none';showStartupTip();},370);}
(function initPopupModal(){if(localStorage.getItem('gnPopupAgreed')){document.getElementById('popupPermissionModal').style.display='none';setTimeout(showStartupTip,80);}})();
function showStartupTip(){if(localStorage.getItem('gnTipDone'))return;document.getElementById('startupTip').style.display='flex';startTipCountdown();}
function dismissTip(){const el=document.getElementById('startupTip');if(!el)return;localStorage.setItem('gnTipDone','1');el.style.transition='opacity .4s';el.style.opacity='0';setTimeout(()=>{try{el.remove()}catch(e){}},420);}
function startTipCountdown(){let n=10;const el=document.getElementById('tipCountNum');if(!el)return;const iv=setInterval(()=>{n--;if(el)el.textContent=n;if(n<=0){clearInterval(iv);dismissTip();}},1000);}
const API_KEY='3a73619bbb8fc6d47742d1b5b2b707b5';
const BASE='https://api.themoviedb.org/3';
const IMG='https://image.tmdb.org/t/p/';
const FB_P='https://via.placeholder.com/300x450/0e0e20/333?text=No+Poster';
const FB_B='https://via.placeholder.com/1280x720/0e0e20/333?text=No+Backdrop';
const GENRES={ACTION:28,COMEDY:35,HORROR:27,SCIFI:878,ROMANCE:10749,THRILLER:53,DRAMA:18,ANIMATION:16,DOC:99,CRIME:80,MYSTERY:9648,FANTASY:14,FAMILY:10751,ADVENTURE:12};
const SERVERS={
  '1':{name:'AutoEmbed Test',url:(id,tv,s,e)=>tv?`https://vidsrc.ru/embed/tv/${id}/${s}/${e}?autoplay=true`:`https://vidsrc.ru/embed/movie/${id}`},
  '2':{name:'AutoEmbed Player',url:(id,tv,s,e)=>tv?`https://player.vidify.top/embed/tv/${id}/${s}/${e}`:`https://player.vidify.top/embed/movie/${id}`},
  '3':{name:'Star-Stream FLixy',url:(id,tv,s,e)=>tv?`https://player.vidsrc.co/embed/tv/${id}/${s}/${e}`:`https://player.vidsrc.co/embed/movie/${id}`},
  '4':{name:'Star-Stream flixy2',url:(id,tv,s,e)=>tv?`https://player.videasy.net/embed/tv/${id}/${s}/${e}`:`https://player.videasy.net/embed/movie/${id}`},
  '5':{name:'2Embed',url:(id,tv,s,e)=>tv?`https://www.2embed.cc/embedtv/${id}&s=${s}&e=${e}`:`https://www.2embed.cc/embed/${id}`},
  '6':{name:'MultiEmbed',url:(id,tv,s,e)=>tv?`https://multiembed.mov/?video_id=${id}&tmdb=1&s=${s}&e=${e}`:`https://multiembed.mov/?video_id=${id}&tmdb=1`},
  '7':{name:'Embed.su',url:(id,tv,s,e)=>tv?`https://embed.su/embed/tv/${id}/${s}/${e}`:`https://embed.su/embed/movie/${id}`},
  '8':{name:'VidSrc.xyz',url:(id,tv,s,e)=>tv?`https://vidsrc.xyz/embed/tv?tmdb=${id}&season=${s}&episode=${e}`:`https://vidsrc.xyz/embed/movie?tmdb=${id}`},
  '9':{name:'VidSrc.me',url:(id,tv,s,e)=>tv?`https://vidsrc.me/embed/tv?tmdb=${id}&season=${s}&episode=${e}`:`https://vidsrc.me/embed/movie?tmdb=${id}`},
  '10':{name:'VidSrc.in',url:(id,tv,s,e)=>tv?`https://vidsrc.in/embed/tv?tmdb=${id}&season=${s}&episode=${e}`:`https://vidsrc.in/embed/movie?tmdb=${id}`}
};
const ICONS=['fa-solid fa-clapperboard','fa-solid fa-star','fa-solid fa-gamepad','fa-solid fa-music','fa-solid fa-trophy','fa-solid fa-cat','fa-solid fa-rocket','fa-solid fa-pizza-slice','fa-solid fa-robot','fa-solid fa-ghost','fa-solid fa-heart','fa-solid fa-face-laugh','fa-solid fa-moon','fa-solid fa-sun','fa-solid fa-bolt'];
const DEFAULT_PROFILES=[{id:1,name:'Main',icon:'fa-solid fa-clapperboard'},{id:2,name:'Guest',icon:'fa-solid fa-user'}];
const STAR_APPS={sports:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/GN-sports',name:'Sports'},tv:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/gn-tv-for-os.html',name:'TV'},music:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/GN-music-for-os.html',name:'Music'},podcast:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/Star-podcast.html',name:'Podcast'},news:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/star-news.html',name:'News'},radio:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/star-radio.html',name:'Radio'},books:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/Star-books.html',name:'Books'},documentary:{url:'https://raw.githubusercontent.com/GN-math-hub/School-Chaets/refs/heads/main/Star-documentry.html',name:'Documentary'}};
let profiles=JSON.parse(localStorage.getItem('gnProfiles')||JSON.stringify(DEFAULT_PROFILES));
let _sp=null;try{_sp=JSON.parse(localStorage.getItem('gnActiveProfile'));}catch(e){}
let activeProfile=(_sp&&profiles.find(p=>p.id===_sp.id))?_sp:profiles[0];
function loadMyList(){try{const p=localStorage.getItem(`gnList_${activeProfile.id}`);if(p)return JSON.parse(p);const l=localStorage.getItem('gnList');if(l)return JSON.parse(l);return[];}catch(e){return[];}}
function saveMyList(){try{localStorage.setItem(`gnList_${activeProfile.id}`,JSON.stringify(myList));}catch(e){}}
let myList=loadMyList();
let continueW=[];try{continueW=JSON.parse(localStorage.getItem('gnContinue')||'[]');}catch(e){}
let watchHist=[];try{watchHist=JSON.parse(localStorage.getItem('gnHistory')||'[]');}catch(e){}
let currentItem=null,histFilter='all',scrollPos=0;
let currentServer=localStorage.getItem('gnServer')||'1';
let discoverPage=1,discoverLoaded=0,isLoadingMore=false;
let heroItems=[],heroIdx=0,heroTimer=null;
let curSeason=1,curEp=1;
const cache=new Map(),CACHE_TTL=5*60*1000;
async function fetc(url){const c=cache.get(url);if(c&&Date.now()-c.t<CACHE_TTL)return c.d;try{const r=await fetch(url);const d=await r.json();cache.set(url,{d,t:Date.now()});return d;}catch(e){return null;}}
function showConfirm(title,desc,onOk){document.getElementById('confirmTitle').textContent=title;document.getElementById('confirmDesc').textContent=desc;document.getElementById('confirmModal').classList.add('open');document.getElementById('confirmOk').onclick=()=>{document.getElementById('confirmModal').classList.remove('open');onOk();};document.getElementById('confirmCancel').onclick=()=>{document.getElementById('confirmModal').classList.remove('open');};}
function initTheme(){const t=localStorage.getItem('gnTheme')||'dark';document.documentElement.setAttribute('data-theme',t);const sel=document.getElementById('themeSelect');if(sel)sel.value=t;}
function applyTheme(v){document.documentElement.setAttribute('data-theme',v);localStorage.setItem('gnTheme',v);const sel=document.getElementById('themeSelect');if(sel)sel.value=v;toast(v==='dark'?'🌙 Dark mode':'☀️ Light mode');}
const io=new IntersectionObserver(entries=>{entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('vis');io.unobserve(e.target);}});},{threshold:.05,rootMargin:'0px 0px -10px 0px'});
function observeAll(){document.querySelectorAll('.section:not(.vis)').forEach(s=>io.observe(s));}
window.addEventListener('scroll',()=>{document.getElementById('mainHeader').classList.toggle('solid',window.scrollY>80);},{passive:true});
function setTab(tab){document.querySelectorAll('.nav-tab').forEach(t=>t.classList.remove('on'));const el=document.getElementById(`tab-${tab}`);if(el)el.classList.add('on');}
const HOME_SECTIONS=['heroSection','continueInline','homeContent','discoverSection'];
const PAGE_SECTIONS=['upcomingPage','myListPage','historyPage'];
function hideAll(){[...HOME_SECTIONS,...PAGE_SECTIONS].forEach(id=>{const el=document.getElementById(id);if(el){el.style.display='none';el.classList.remove('active');}});}
function showHome(){hideAll();document.getElementById('heroSection').style.display='flex';document.getElementById('homeContent').style.display='block';document.getElementById('discoverSection').style.display='block';if(continueW.length>0){document.getElementById('continueInline').style.display='block';renderContinueInline();}setTab('home');observeAll();window.scrollTo(0,0);}
function showMyList(){hideAll();const p=document.getElementById('myListPage');p.style.display='block';p.classList.add('active');setTab('mylist');renderMyList();window.scrollTo(0,0);}
function showHistory(){hideAll();const p=document.getElementById('historyPage');p.style.display='block';p.classList.add('active');histFilter='all';document.querySelectorAll('.filter-btn').forEach((b,i)=>b.classList.toggle('on',i===0));renderHistory();window.scrollTo(0,0);}
async function showUpcoming(){hideAll();const p=document.getElementById('upcomingPage');p.style.display='block';p.classList.add('active');await loadUpcoming();window.scrollTo(0,0);}
function changeServer(v){currentServer=v;localStorage.setItem('gnServer',v);['serverSelect','settingsServerSelect'].forEach(id=>{const el=document.getElementById(id);if(el)el.value=v;});toast(`Server: ${SERVERS[v]?.name||v}`);}
function openStarApps(){document.getElementById('starAppsPopup').classList.add('open');document.body.classList.add('locked');}
function closeStarApps(){document.getElementById('starAppsPopup').classList.remove('open');document.body.classList.remove('locked');}
async function openStarApp(appKey){closeStarApps();const app=STAR_APPS[appKey];if(!app){toast('App not found');return;}toast(`Opening ${app.name}…`);try{const res=await fetch(app.url);if(!res.ok)throw new Error('HTTP '+res.status);const html=await res.text();const win=window.open('about:blank','_blank');if(!win){toast('⚠️ Allow popups to open Star Apps');return;}win.document.open();win.document.write(html);win.document.close();}catch(err){window.open(app.url,'_blank');}}
function toast(msg){const t=document.getElementById('toast');t.innerHTML=msg;t.className='toast vis';clearTimeout(t._t);t._t=setTimeout(()=>t.classList.remove('vis'),2800);}
async function loadHero(){const d=await fetc(`${BASE}/trending/all/day?api_key=${API_KEY}`);if(!d?.results?.length)return;heroItems=d.results.filter(i=>i.backdrop_path).slice(0,6);buildDots();setHero(0);heroTimer=setInterval(()=>setHero((heroIdx+1)%heroItems.length),7500);}
function buildDots(){const w=document.getElementById('heroDots');w.innerHTML='';heroItems.forEach((_,i)=>{const d=document.createElement('div');d.className='hero-dot'+(i===0?' on':'');d.onclick=()=>{clearInterval(heroTimer);setHero(i);heroTimer=setInterval(()=>setHero((heroIdx+1)%heroItems.length),7500);};w.appendChild(d);});}
function setHero(idx){heroIdx=idx;const item=heroItems[idx];if(!item)return;const isTv=!!item.first_air_date;const year=(item.release_date||item.first_air_date||'').slice(0,4);const rating=item.vote_average?.toFixed(1)||'';const bg=document.getElementById('heroBg');bg.style.opacity='0';setTimeout(()=>{bg.style.backgroundImage=`url(${IMG}original${item.backdrop_path})`;bg.style.opacity='1';},250);document.getElementById('heroTitle').textContent=item.title||item.name;document.getElementById('heroOverview').textContent=item.overview||'';document.getElementById('heroEyebrow').innerHTML=`<i class="fa-solid fa-fire-alt"></i> #${idx+1} ${isTv?'Series':'Movie'}`;document.getElementById('heroMeta').innerHTML=`<span style="font-weight:900;color:var(--text)">${Math.floor(Math.random()*15+83)}% Match</span><span>${year}</span>${rating?`<span class="hero-rating"><i class="fa-solid fa-star" style="font-size:9px"></i>${rating}</span>`:''}<span class="hero-cert" id="heroCert">NR</span><span style="color:var(--text3)">${isTv?'Series':'Film'}</span>`;getCert(item).then(c=>{const el=document.getElementById('heroCert');if(el)el.textContent=c;});document.querySelectorAll('.hero-dot').forEach((d,i)=>d.classList.toggle('on',i===idx));item.media_type=isTv?'tv':'movie';window._heroItem=item;updateHeroListBtn();}
function updateHeroListBtn(){const item=window._heroItem;if(!item)return;const inList=myList.some(i=>i.id===item.id);const btn=document.getElementById('heroListBtn');btn.innerHTML=inList?'<i class="fa-solid fa-check"></i>':'<i class="fa-solid fa-plus"></i>';btn.classList.toggle('active',inList);}
let heroTouchX=null;
document.getElementById('heroSection').addEventListener('touchstart',e=>{heroTouchX=e.touches[0].clientX;},{passive:true});
document.getElementById('heroSection').addEventListener('touchend',e=>{if(heroTouchX===null)return;const dx=e.changedTouches[0].clientX-heroTouchX;heroTouchX=null;if(Math.abs(dx)<50)return;clearInterval(heroTimer);const next=dx<0?(heroIdx+1)%heroItems.length:(heroIdx-1+heroItems.length)%heroItems.length;setHero(next);heroTimer=setInterval(()=>setHero((heroIdx+1)%heroItems.length),7500);},{passive:true});
function heroPlay(){const item=window._heroItem;if(!item)return;addHistory(item);addContinue(item,0,7200);openPlayer(item.id,item.media_type==='tv',1,1);}
function heroMoreInfo(){if(window._heroItem)openDetails(window._heroItem);}
function heroToggleList(){const item=window._heroItem;if(!item)return;toggleList(item);updateHeroListBtn();}
async function getCert(item){try{const isTv=item.media_type==='tv'||!!item.first_air_date;if(isTv){const d=await fetc(`${BASE}/tv/${item.id}/content_ratings?api_key=${API_KEY}`);return d?.results?.find(r=>r.iso_3166_1==='US')?.rating||'NR';}else{const d=await fetc(`${BASE}/movie/${item.id}/release_dates?api_key=${API_KEY}`);return d?.results?.find(r=>r.iso_3166_1==='US')?.release_dates?.[0]?.certification||'NR';}}catch(e){return'NR';}}
function toggleList(item){const idx=myList.findIndex(i=>i.id===item.id);const adding=idx===-1;if(adding){myList.push({id:item.id,title:item.title||item.name,poster_path:item.poster_path||null,backdrop_path:item.backdrop_path||null,media_type:item.media_type||(item.first_air_date?'tv':'movie'),vote_average:item.vote_average||0,overview:item.overview||'',release_date:item.release_date||'',first_air_date:item.first_air_date||'',genre_ids:item.genre_ids||[],_cert:item._cert||'NR'});}else{myList.splice(idx,1);}saveMyList();updateListCount();document.querySelectorAll(`.card-act[data-lid="${item.id}"]`).forEach(b=>{b.classList.toggle('on',adding);b.innerHTML=adding?'<i class="fa-solid fa-check"></i>':'<i class="fa-solid fa-plus"></i>';});toast(adding?'✓ Added to My List':'Removed from My List');if(document.getElementById('myListPage').classList.contains('active'))renderMyList();if(currentItem?.id===item.id)updateDetailsListBtn();}
function updateDetailsListBtn(){const btn=document.getElementById('detailsListBtn');if(!btn||!currentItem)return;const inL=myList.some(i=>i.id===currentItem.id);btn.innerHTML=inL?'<i class="fa-solid fa-check"></i> In List':'<i class="fa-solid fa-plus"></i> My List';btn.classList.toggle('on',inL);}
function toggleListFromDetails(){if(currentItem)toggleList(currentItem);}
function updateListCount(){const c=myList.length;const badge=document.getElementById('myListBadge');if(badge){badge.textContent=c>99?'99+':c;badge.style.display=c>0?'block':'none';}}
function renderMyList(){const c=document.getElementById('myListContent');if(!c)return;c.innerHTML='';if(!myList.length){c.innerHTML='<div class="mylist-empty"><i class="fa-solid fa-bookmark"></i><h3>Your List is Empty</h3><p>Add movies & shows by tapping the + button on any title.</p></div>';return;}const row=document.createElement('div');row.className='row';myList.forEach(item=>createCard(item,row));c.appendChild(row);}
function createCard(item,container){const card=document.createElement('div');card.className='card';const inL=myList.some(i=>i.id===item.id);const poster=item.poster_path?`${IMG}w342${item.poster_path}`:FB_P;window[`_item_${item.id}`]=item;card.innerHTML=`<img src="${poster}" alt="${item.title||item.name}" loading="lazy" onerror="this.src='${FB_P}'"><div class="card-overlay"><div class="card-title">${item.title||item.name}</div><div class="card-meta"><i class="fa-solid fa-star" style="color:#888;font-size:9px"></i>${(item.vote_average||0).toFixed(1)}<span class="card-badge">${item._cert||'NR'}</span></div></div><div class="card-actions"><button class="card-act ${inL?'on':''}" data-lid="${item.id}" onclick="event.stopPropagation();cardToggleList(${item.id})">${inL?'<i class="fa-solid fa-check"></i>':'<i class="fa-solid fa-plus"></i>'}</button></div>`;card.addEventListener('click',e=>{if(e.target.closest('.card-act'))return;openDetails(item);});container.appendChild(card);}
function cardToggleList(id){const item=window[`_item_${id}`];if(item)toggleList(item);}
function createTop10(item,num,container){const wrap=document.createElement('div');wrap.className='top10-wrap';const poster=item.poster_path?`${IMG}w342${item.poster_path}`:FB_P;wrap.innerHTML=`<div class="top10-num">${num}</div><div class="top10-poster"><img src="${poster}" alt="${item.title||item.name}" loading="lazy" onerror="this.src='${FB_P}'"></div>`;wrap.onclick=()=>openDetails(item);container.appendChild(wrap);}
function createWide(item,container){const card=document.createElement('div');card.className='wide-card';const img=item.backdrop_path?`${IMG}w300${item.backdrop_path}`:(item.poster_path?`${IMG}w342${item.poster_path}`:FB_B);card.innerHTML=`<div class="wide-thumb"><img src="${img}" alt="${item.title||item.name}" onerror="this.src='${FB_B}'"><div class="wide-play"><div class="wide-play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div></div><div class="wide-info"><div class="wide-title">${item.title||item.name}</div><div class="wide-meta"><span>${item._cert||'NR'}</span><span><i class="fa-solid fa-star" style="color:#888;font-size:10px"></i> ${(item.vote_average||0).toFixed(1)}</span></div></div>`;card.onclick=()=>openDetails(item);container.appendChild(card);}
async function loadHotToday(){const grid=document.getElementById('hotGrid');const d=await fetc(`${BASE}/trending/all/day?api_key=${API_KEY}`);grid.innerHTML='';if(!d?.results)return;d.results.slice(0,8).forEach((item,i)=>{item.media_type=item.first_air_date?'tv':'movie';const poster=item.poster_path?`${IMG}w92${item.poster_path}`:FB_P;const score=Math.round(80+Math.random()*19);const el=document.createElement('div');el.className='hot-item';el.innerHTML=`<div class="hot-rank">${i+1}</div><img class="hot-poster" src="${poster}" alt="${item.title||item.name}" onerror="this.src='${FB_P}'"><div class="hot-info"><div class="hot-title">${item.title||item.name}</div><div class="hot-meta"><span>${item.first_air_date?'TV':'Movie'}</span><span><i class="fa-solid fa-star" style="color:#888;font-size:10px"></i> ${(item.vote_average||0).toFixed(1)}</span><span class="hot-score">${score}🔥</span></div></div>`;el.onclick=()=>openDetails(item);grid.appendChild(el);});}
async function loadCat(endpoint,rowId,type,genreId=null){const c=document.getElementById(rowId);if(!c)return;c.innerHTML='';for(let i=0;i<5;i++){const s=document.createElement('div');s.className='skeleton card';c.appendChild(s);}let url=`${BASE}${endpoint}?api_key=${API_KEY}&language=en-US`;if(genreId)url+=`&with_genres=${genreId}`;const d=await fetc(url);c.innerHTML='';if(!d?.results)return;for(const item of d.results.slice(0,18)){item.media_type=type;item._cert=await getCert(item);window[`_item_${item.id}`]=item;createCard(item,c);}}
async function loadNewReleases(){const c=document.getElementById('newRelRow');c.innerHTML='';const d=await fetc(`${BASE}/movie/now_playing?api_key=${API_KEY}&language=en-US`);if(!d?.results)return;for(const item of d.results.slice(0,16)){item.media_type='movie';item._cert=await getCert(item);window[`_item_${item.id}`]=item;createCard(item,c);}}
function renderContinueInline(){const c=document.getElementById('continueInlineRow');c.innerHTML='';continueW.forEach(item=>createWide(item,c));}
function addContinue(item,progress,duration){const e={...item,progress,duration,addedAt:Date.now()};continueW=continueW.filter(i=>i.id!==item.id);continueW.unshift(e);if(continueW.length>50)continueW=continueW.slice(0,50);localStorage.setItem('gnContinue',JSON.stringify(continueW));}
function clearContinueConfirm(){showConfirm('Clear Continue Watching','Remove all in-progress titles?',()=>{continueW=[];localStorage.setItem('gnContinue','[]');document.getElementById('continueInline').style.display='none';document.getElementById('continueInlineRow').innerHTML='';toast('Cleared');});}
async function openDetails(item){currentItem=item;scrollPos=window.pageYOffset;const posterUrl=item.backdrop_path?`${IMG}w780${item.backdrop_path}`:(item.poster_path?`${IMG}w780${item.poster_path}`:FB_B);const pi=document.getElementById('detailsPoster');pi.src=posterUrl;pi.onerror=()=>{pi.src=FB_B;};document.getElementById('detailsTitle').textContent=item.title||item.name;document.getElementById('detailsYear').textContent=(item.release_date||item.first_air_date||'').slice(0,4);document.getElementById('detailsOverview').textContent=item.overview||'No overview available.';document.getElementById('detailsCert').textContent=item._cert||'NR';document.getElementById('detailsMatch').textContent=`${Math.floor(Math.random()*15+83)}% Match`;document.getElementById('detailsGenre').textContent=await getGenreNames(item.genre_ids);updateDetailsListBtn();await Promise.all([loadCast(item),loadRecs(item),loadPAW(item)]);const isTv=item.media_type==='tv'||!!item.first_air_date;const epSec=document.getElementById('epSection');if(isTv){epSec.style.display='block';curSeason=1;curEp=1;await loadSeasons(item.id);}else{epSec.style.display='none';}document.body.classList.add('locked');document.getElementById('detailsModal').classList.add('open');document.getElementById('detailsBox').scrollTop=0;}
function closeDetails(){document.getElementById('detailsModal').classList.remove('open');document.body.classList.remove('locked');setTimeout(()=>{document.getElementById('detailsPoster').src='';currentItem=null;},300);window.scrollTo(0,scrollPos);}
function closeDetailsBd(e){if(e.target===document.getElementById('detailsModal'))closeDetails();}
async function getGenreNames(ids){if(!ids?.length)return'Various';const d=await fetc(`${BASE}/genre/movie/list?api_key=${API_KEY}`);return(ids.map(id=>d?.genres?.find(g=>g.id===id)?.name).filter(Boolean).slice(0,3).join(', '))||'Various';}
async function loadCast(item){const c=document.getElementById('detailsCast');c.innerHTML='';const type=item.media_type==='tv'||item.first_air_date?'tv':'movie';const d=await fetc(`${BASE}/${type}/${item.id}/credits?api_key=${API_KEY}`);const cast=d?.cast?.slice(0,8)||[];if(!cast.length){c.innerHTML='<div class="cast-chip">Cast unavailable</div>';return;}cast.forEach(a=>{const el=document.createElement('div');el.className='cast-chip';el.textContent=a.name;c.appendChild(el);});}
async function loadRecs(item){const c=document.getElementById('recsRow');c.innerHTML='<div class="spinner-wrap" style="padding:12px"><div class="spinner"></div></div>';try{const type=item.first_air_date?'tv':'movie';const d=await fetc(`${BASE}/${type}/${item.id}/recommendations?api_key=${API_KEY}`);c.innerHTML='';if(!d?.results?.length){c.innerHTML='<div class="empty" style="padding:12px;font-size:11px">No recommendations</div>';return;}for(const rec of d.results.filter(r=>r.id!==item.id).slice(0,10)){rec.media_type=type;rec._cert=await getCert(rec);window[`_item_${rec.id}`]=rec;createRecCard(rec,c);}}catch(e){c.innerHTML='<div class="empty" style="padding:12px">Failed</div>';}}
function createRecCard(item,container){const card=document.createElement('div');card.className='rec-card';const img=item.backdrop_path?`${IMG}w300${item.backdrop_path}`:(item.poster_path?`${IMG}w342${item.poster_path}`:FB_B);card.innerHTML=`<img src="${img}" alt="${item.title||item.name}" loading="lazy" onerror="this.src='${FB_B}'"><div class="rec-ov"><div class="rec-title">${item.title||item.name}</div></div>`;card.onclick=()=>{closeDetails();setTimeout(()=>openDetails(item),300);};container.appendChild(card);}
async function loadPAW(item){const sec=document.getElementById('pawSection');const row=document.getElementById('pawRow');row.innerHTML='';sec.style.display='none';try{const type=item.first_air_date?'tv':'movie';const d=await fetc(`${BASE}/${type}/${item.id}/similar?api_key=${API_KEY}`);const results=d?.results?.filter(r=>r.id!==item.id)?.slice(0,8)||[];if(!results.length)return;sec.style.display='block';results.forEach(rec=>{rec.media_type=type;window[`_item_${rec.id}`]=rec;const card=document.createElement('div');card.className='paw-card';const img=rec.poster_path?`${IMG}w185${rec.poster_path}`:FB_P;card.innerHTML=`<img src="${img}" alt="${rec.title||rec.name}" loading="lazy" onerror="this.src='${FB_P}'"><div class="paw-card-title">${rec.title||rec.name}</div>`;card.onclick=()=>{closeDetails();setTimeout(()=>openDetails(rec),300);};row.appendChild(card);});}catch(e){}}
async function playModalTrailer(){if(!currentItem)return;const type=currentItem.first_air_date?'tv':'movie';const d=await fetc(`${BASE}/${type}/${currentItem.id}/videos?api_key=${API_KEY}`);const t=d?.results?.find(v=>v.type==='Trailer'&&v.site==='YouTube')||d?.results?.find(v=>v.site==='YouTube');if(t?.key){window.open(`https://www.youtube.com/watch?v=${t.key}`,'_blank');toast('Opening trailer…');}else toast('No trailer available');}
async function loadSeasons(tvId){const d=await fetc(`${BASE}/tv/${tvId}?api_key=${API_KEY}`);const seasons=(d?.seasons||[]).filter(s=>s.season_number>0);const sel=document.getElementById('seasonDropdown');sel.innerHTML='';seasons.forEach(s=>{const o=document.createElement('option');o.value=s.season_number;o.textContent=`Season ${s.season_number}`;sel.appendChild(o);});curSeason=seasons.length>0?seasons[0].season_number:1;sel.value=curSeason;await loadEps(tvId,curSeason);}
async function onSeasonChange(){const s=parseInt(document.getElementById('seasonDropdown').value);curSeason=s;curEp=1;if(currentItem)await loadEps(currentItem.id,s);}

// ══ LOAD EPISODES — includes Open in New Tab + Download buttons per card ══
async function loadEps(tvId,season){
  const grid=document.getElementById('epGrid');
  grid.innerHTML='<div class="spinner-wrap"><div class="spinner"></div></div>';
  try{
    const d=await fetc(`${BASE}/tv/${tvId}/season/${season}?api_key=${API_KEY}`);
    grid.innerHTML='';
    const eps=d?.episodes||[];
    if(!eps.length){grid.innerHTML='<div class="empty" style="padding:16px">No episodes found</div>';return;}
    eps.forEach(ep=>{
      const card=document.createElement('div');card.className='ep-card';
      const still=ep.still_path?`${IMG}w300${ep.still_path}`:(currentItem?.backdrop_path?`${IMG}w300${currentItem.backdrop_path}`:FB_B);
      const airDate=ep.air_date?new Date(ep.air_date).toLocaleDateString('en-US',{month:'short',day:'numeric',year:'numeric'}):'';
      const runtime=ep.runtime?`${ep.runtime}m`:'';
      card.innerHTML=`<div class="ep-thumb"><img src="${still}" alt="Ep ${ep.episode_number}" loading="lazy" onerror="this.src='${FB_B}'"><div class="ep-play"><div class="ep-play-btn"><svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg></div></div><div class="ep-num">E${ep.episode_number}</div></div><div class="ep-info"><div class="ep-title">${ep.name||'Episode '+ep.episode_number}</div><div class="ep-meta">${runtime?`<span>${runtime}</span>`:''}${airDate?`<span>${airDate}</span>`:''}</div><div class="ep-overview">${ep.overview||'No description.'}</div></div>`;

      // ── NEW: action row with Open in New Tab + Download ──
      const epNum=ep.episode_number;
      const epInfo=card.querySelector('.ep-info');
      const actionRow=document.createElement('div');
      actionRow.className='ep-action-row';

      // Open in New Tab
      const tabBtn=document.createElement('button');
      tabBtn.className='ep-action-btn';
      tabBtn.innerHTML='<i class="fa-solid fa-arrow-up-right-from-square"></i> Open in New Tab';
      tabBtn.title='Open in new tab (use if episode does not load)';
      tabBtn.onclick=function(ev){
        ev.stopPropagation();
        if(!currentItem)return;
        let url;
        try{url=SERVERS[currentServer].url(currentItem.id,true,season,epNum);}
        catch(_){url=`https://vidsrc.ru/embed/tv/${currentItem.id}/${season}/${epNum}`;}
        window.open(url,'_blank');
        toast(`Opened S${season}E${epNum} in new tab ↗`);
      };

      // Download
      const dlBtn=document.createElement('button');
      dlBtn.className='ep-action-btn ep-dl';
      dlBtn.innerHTML='<i class="fa-solid fa-download"></i> Download';
      dlBtn.title='Download this episode';
      dlBtn.onclick=function(ev){
        ev.stopPropagation();
        if(!currentItem)return;
        window.open(`https://dl.vidsrc.vip/tv/${currentItem.id}/${season}/${epNum}`,'_blank');
        toast(`Download started for S${season}E${epNum}`);
      };

      actionRow.appendChild(tabBtn);
      actionRow.appendChild(dlBtn);
      epInfo.appendChild(actionRow);
      // ── end new buttons ──

      card.onclick=()=>playEp(tvId,season,ep.episode_number,ep.name);
      grid.appendChild(card);
    });
  }catch(e){grid.innerHTML='<div class="empty" style="padding:16px">Failed to load episodes</div>';}
}

function playEp(tvId,season,ep){curSeason=season;curEp=ep;document.getElementById('detailsModal').classList.remove('open');document.body.classList.remove('locked');setTimeout(()=>{openPlayer(tvId,true,season,ep);toast(`Playing S${season}E${ep}`);},260);if(currentItem)addHistory(currentItem);}
function openPlayer(id,isTv,s=1,e=1){const src=SERVERS[currentServer].url(id,isTv,s,e);document.getElementById('playerIframe').src=src;document.getElementById('playerModal').classList.add('open');document.body.classList.add('locked');}
function playContent(){if(!currentItem)return;addContinue(currentItem,0,currentItem.runtime?currentItem.runtime*60:7200);addHistory(currentItem);const isTv=currentItem.media_type==='tv'||!!currentItem.first_air_date;document.getElementById('detailsModal').classList.remove('open');setTimeout(()=>openPlayer(currentItem.id,isTv,curSeason,curEp),260);}
function closePlayer(){document.getElementById('playerModal').classList.remove('open');document.getElementById('playerControls').classList.remove('open');document.getElementById('playerIframe').src='';if(currentItem){setTimeout(()=>{document.getElementById('detailsModal').classList.add('open');},260);}else{document.body.classList.remove('locked');}}
function closePlayerBd(e){if(e.target===document.getElementById('playerModal'))closePlayer();}

// ── Download current movie/show ──
function downloadContent(){
  if(!currentItem)return;
  const isTv=currentItem.media_type==='tv'||!!currentItem.first_air_date;
  window.open(isTv?`https://dl.vidsrc.vip/tv/${currentItem.id}/${curSeason}/${curEp}`:`https://dl.vidsrc.vip/movie/${currentItem.id}`,'_blank');
  toast('Download started');
}

// ── NEW: Open current movie/show in new tab (if not loading) ──
function openInNewTab(){
  if(!currentItem){toast('Nothing selected');return;}
  const isTv=currentItem.media_type==='tv'||!!currentItem.first_air_date;
  const id=currentItem.id;const s=curSeason||1;const e=curEp||1;
  let url;
  try{url=SERVERS[currentServer].url(id,isTv,s,e);}
  catch(_){url=isTv?`https://vidsrc.ru/embed/tv/${id}/${s}/${e}`:`https://vidsrc.ru/embed/movie/${id}`;}
  window.open(url,'_blank');
  toast('Opened in new tab ↗');
}

function toggleFullscreen(){const c=document.getElementById('playerWrap');const btn=document.getElementById('fsBtn');if(!document.fullscreenElement){(c.requestFullscreen||c.webkitRequestFullscreen).call(c);btn.innerHTML='<i class="fa-solid fa-compress"></i> Exit';}else{(document.exitFullscreen||document.webkitExitFullscreen||function(){}).call(document);btn.innerHTML='<i class="fa-solid fa-expand"></i> Full';}}
document.addEventListener('fullscreenchange',()=>{const btn=document.getElementById('fsBtn');if(btn)btn.innerHTML=document.fullscreenElement?'<i class="fa-solid fa-compress"></i> Exit':'<i class="fa-solid fa-expand"></i> Full';});
function launchMini(){const src=document.getElementById('playerIframe').src;if(!src||src==='about:blank'){toast('Nothing playing');return;}const title=currentItem?(currentItem.title||currentItem.name):'Now Playing';document.getElementById('miniIframe').src=src;document.getElementById('miniTitle').textContent=title;document.getElementById('miniPlayer').classList.add('open');closePlayer();toast('Mini player');}
function closeMini(){document.getElementById('miniPlayer').classList.remove('open');document.getElementById('miniIframe').src='';}
function expandMini(){const src=document.getElementById('miniIframe').src;if(!src||src==='about:blank')return;document.getElementById('playerIframe').src=src;document.getElementById('playerModal').classList.add('open');document.body.classList.add('locked');closeMini();}
async function loadUpcoming(){const grid=document.getElementById('upcomingGrid');grid.innerHTML='<div style="grid-column:1/-1" class="spinner-wrap"><div class="spinner"></div></div>';const today=new Date().toISOString().split('T')[0];const future=new Date(Date.now()+120*86400000).toISOString().split('T')[0];const d=await fetc(`${BASE}/discover/movie?api_key=${API_KEY}&sort_by=release_date.asc&primary_release_date.gte=${today}&primary_release_date.lte=${future}`);grid.innerHTML='';if(!d?.results?.length){grid.innerHTML='<div class="empty" style="grid-column:1/-1">No upcoming releases found</div>';return;}for(const item of d.results.slice(0,24)){item.media_type='movie';item._cert=await getCert(item);window[`_item_${item.id}`]=item;const card=document.createElement('div');card.className='upcoming-card';const poster=item.poster_path?`${IMG}w342${item.poster_path}`:FB_P;const rel=item.release_date||'';const days=rel?Math.max(0,Math.ceil((new Date(rel)-Date.now())/86400000)):'?';const fmtDate=rel?new Date(rel).toLocaleDateString('en-US',{month:'short',day:'numeric',year:'numeric'}):'TBA';card.innerHTML=`<img class="upcoming-poster" src="${poster}" alt="${item.title}" onerror="this.src='${FB_P}'"><div class="upcoming-info"><div class="upcoming-title">${item.title}</div><div class="upcoming-date"><i class="fa-solid fa-calendar-alt"></i> ${fmtDate}</div><div class="upcoming-overview">${item.overview||''}</div><div class="upcoming-countdown"><span>${days}</span>d away</div></div>`;card.onclick=()=>openDetails(item);grid.appendChild(card);}}
function addHistory(item){const e={id:item.id,title:item.title||item.name||'Unknown',poster_path:item.poster_path||null,backdrop_path:item.backdrop_path||null,media_type:item.media_type||(item.first_air_date?'tv':'movie'),vote_average:item.vote_average||0,overview:item.overview||'',release_date:item.release_date||'',first_air_date:item.first_air_date||'',genre_ids:item.genre_ids||[],_cert:item._cert||'NR',watchedAt:new Date().toISOString()};watchHist=watchHist.filter(h=>h.id!==item.id);watchHist.unshift(e);if(watchHist.length>100)watchHist=watchHist.slice(0,100);localStorage.setItem('gnHistory',JSON.stringify(watchHist));}
function renderHistory(){const grid=document.getElementById('historyGrid');grid.innerHTML='';const filtered=histFilter==='all'?watchHist:watchHist.filter(h=>h.media_type===histFilter);if(!filtered.length){grid.innerHTML='<div class="empty">No history yet. Start watching to see your history here.</div>';return;}filtered.forEach(item=>{const el=document.createElement('div');el.className='history-item';const poster=item.poster_path?`${IMG}w92${item.poster_path}`:FB_P;const ago=timeAgo(new Date(item.watchedAt));el.innerHTML=`<img class="history-poster" src="${poster}" alt="${item.title}" onerror="this.src='${FB_P}'"><div class="history-info"><div class="history-title">${item.title}</div><div class="history-meta"><span class="history-badge">${item.media_type==='tv'?'TV':'Film'}</span><span><i class="fa-solid fa-star" style="color:#888;font-size:9px"></i> ${(item.vote_average||0).toFixed(1)}</span></div><div class="history-time">${ago}</div></div><button class="history-del-btn" onclick="event.stopPropagation();removeHistory(${item.id})"><i class="fa-solid fa-xmark"></i></button>`;el.addEventListener('click',e=>{if(e.target.closest('.history-del-btn'))return;openDetails(item);});grid.appendChild(el);});}
function filterHistory(t,btn){histFilter=t;document.querySelectorAll('.filter-btn').forEach(b=>b.classList.remove('on'));btn.classList.add('on');renderHistory();}
function removeHistory(id){watchHist=watchHist.filter(h=>h.id!==id);localStorage.setItem('gnHistory',JSON.stringify(watchHist));renderHistory();toast('Removed');}
function clearFullHistoryConfirm(){showConfirm('Clear History','Remove your entire watch history?',()=>{watchHist=[];localStorage.setItem('gnHistory','[]');renderHistory();toast('History cleared');});}
function timeAgo(date){if(!(date instanceof Date)||isNaN(date))return'Unknown';const diff=Date.now()-date.getTime();const m=Math.floor(diff/60000),h=Math.floor(diff/3600000),d=Math.floor(diff/86400000);if(m<1)return'Just now';if(m<60)return`${m}m ago`;if(h<24)return`${h}h ago`;if(d<7)return`${d}d ago`;return date.toLocaleDateString('en-US',{month:'short',day:'numeric'});}
async function loadMore(){if(isLoadingMore||discoverLoaded>=600)return;isLoadingMore=true;const btn=document.getElementById('loadMoreBtn');btn.disabled=true;const grid=document.getElementById('discoverGrid');try{const eps=[`/movie/popular?api_key=${API_KEY}&language=en-US&page=${discoverPage}`,`/tv/popular?api_key=${API_KEY}&language=en-US&page=${discoverPage}`,`/movie/top_rated?api_key=${API_KEY}&language=en-US&page=${discoverPage}`,`/tv/top_rated?api_key=${API_KEY}&language=en-US&page=${discoverPage}`];const picked=eps.sort(()=>.5-Math.random()).slice(0,2);const results=await Promise.all(picked.map(u=>fetc(`${BASE}${u}`)));const seen=new Set();let items=[];results.forEach(d=>{if(d?.results)items=items.concat(d.results);});items=items.filter(i=>{if(seen.has(i.id))return false;seen.add(i.id);return true;});for(const item of items.slice(0,18)){if(discoverLoaded>=600)break;item.media_type=item.first_air_date?'tv':'movie';item._cert=await getCert(item);window[`_item_${item.id}`]=item;createCard(item,grid);discoverLoaded++;}discoverPage++;document.getElementById('discoverCount').textContent=`${discoverLoaded}+`;if(discoverLoaded>=600){btn.innerHTML='<span>All Loaded ✓</span>';btn.disabled=true;}else{btn.innerHTML=`<i class="fa-solid fa-arrow-down"></i> <span>Load More (${discoverLoaded}/600)</span>`;btn.disabled=false;}}catch(e){toast('Failed to load more');btn.disabled=false;}finally{isLoadingMore=false;}}
function openSettings(){document.getElementById('settingsModal').classList.add('open');document.body.classList.add('locked');document.getElementById('themeSelect').value=localStorage.getItem('gnTheme')||'dark';document.getElementById('settingsServerSelect').value=currentServer;}
function closeSettings(){document.getElementById('settingsModal').classList.remove('open');document.body.classList.remove('locked');}
function saveSetting(k,v){const s=JSON.parse(localStorage.getItem('gnSettings')||'{}');s[k]=v;localStorage.setItem('gnSettings',JSON.stringify(s));}
function clearAllData(){closeSettings();showConfirm('Clear All Data','This will delete your list, history, profiles, and settings. This cannot be undone.',()=>{['gnList','gnContinue','gnHistory','gnSettings','gnTheme','gnProfiles','gnActiveProfile','gnServer','gnTipDone','gnPopupAgreed'].forEach(k=>localStorage.removeItem(k));profiles.forEach(p=>localStorage.removeItem(`gnList_${p.id}`));toast('Data cleared — refreshing…');setTimeout(()=>location.reload(),1200);});}
function openPlayerControls(){document.getElementById('playerControls').classList.add('open');}
function closePlayerControls(){document.getElementById('playerControls').classList.remove('open');}
function setSpeed(s,el){document.querySelectorAll('#speedOpts .pc-opt').forEach(o=>o.classList.remove('sel'));el.classList.add('sel');toast(`Speed: ${s}×`);}
function setSub(l,el){document.querySelectorAll('#subOpts .sub-track').forEach(o=>o.classList.remove('sel'));el.classList.add('sel');const n={'off':'Off','en':'English','es':'Spanish','fr':'French','de':'German','ja':'Japanese','pt':'Portuguese','ko':'Korean'};toast(`Subtitles: ${n[l]||l}`);}
function openProfiles(){document.getElementById('profilesModal').classList.add('open');document.body.classList.add('locked');hideAddProfileForm();renderProfiles();}
function closeProfiles(){document.getElementById('profilesModal').classList.remove('open');document.body.classList.remove('locked');}
function renderProfiles(){const grid=document.getElementById('profilesGrid');grid.innerHTML='';profiles.forEach(p=>{const item=document.createElement('div');item.className='profile-item';const isActive=p.id===activeProfile.id;item.innerHTML=`<div class="profile-avatar-wrap ${isActive?'active':''}"><i class="${p.icon}" style="font-size:28px;color:var(--text2)"></i></div><div class="profile-name">${p.name}</div>${p.id>2?`<button class="profile-remove-btn" onclick="event.stopPropagation();removeProfile(${p.id})"><i class="fa-solid fa-xmark"></i></button>`:''}`;item.onclick=()=>selectProfile(p);grid.appendChild(item);});if(profiles.length<5){const add=document.createElement('div');add.className='profile-item';add.innerHTML=`<div class="profile-avatar-wrap" style="border-style:dashed;opacity:.6"><i class="fa-solid fa-plus" style="font-size:24px;color:var(--text3)"></i></div><div class="profile-name" style="color:var(--text3)">Add</div>`;add.onclick=showAddProfileForm;grid.appendChild(add);}}
function selectProfile(p){activeProfile=p;localStorage.setItem('gnActiveProfile',JSON.stringify(p));myList=loadMyList();updateListCount();updateProfileIcons(p);closeProfiles();toast(`Switched to ${p.name}`);}
function updateProfileIcons(p){document.getElementById('headerProfile').innerHTML=`<i class="${p.icon}" style="-webkit-text-fill-color:#fff"></i>`;document.getElementById('tabProfileIcon').innerHTML=`<i class="${p.icon}"></i>`;}
function removeProfile(id){showConfirm('Remove Profile','This will remove the profile and its saved list.',()=>{profiles=profiles.filter(p=>p.id!==id);localStorage.setItem('gnProfiles',JSON.stringify(profiles));localStorage.removeItem(`gnList_${id}`);if(activeProfile.id===id){activeProfile=profiles[0];localStorage.setItem('gnActiveProfile',JSON.stringify(activeProfile));myList=loadMyList();updateListCount();updateProfileIcons(activeProfile);}renderProfiles();toast('Profile removed');});}
function showAddProfileForm(){const f=document.getElementById('addProfileForm');f.classList.add('vis');document.getElementById('newProfileName').value='';let selIcon=ICONS[0];const picker=document.getElementById('iconPicker');picker.innerHTML='';ICONS.forEach(ic=>{const btn=document.createElement('div');btn.className='icon-opt'+(ic===selIcon?' sel':'');btn.innerHTML=`<i class="${ic}"></i>`;btn.onclick=()=>{selIcon=ic;document.querySelectorAll('.icon-opt').forEach(b=>b.classList.remove('sel'));btn.classList.add('sel');};picker.appendChild(btn);});}
function hideAddProfileForm(){document.getElementById('addProfileForm').classList.remove('vis');}
function saveNewProfile(){const name=document.getElementById('newProfileName').value.trim();if(!name){toast('Please enter a name');return;}const selEl=document.querySelector('.icon-opt.sel');const icon=selEl?selEl.querySelector('i').className:ICONS[0];const newP={id:Date.now(),name:name.slice(0,14),icon};profiles.push(newP);localStorage.setItem('gnProfiles',JSON.stringify(profiles));hideAddProfileForm();renderProfiles();toast(`Profile "${newP.name}" created`);}
document.addEventListener('keydown',e=>{if(e.target.tagName==='INPUT'||e.target.tagName==='TEXTAREA'||e.target.tagName==='SELECT'){if(e.key==='Escape')e.target.blur();return;}switch(e.key){case'/':e.preventDefault();openSearchOverlay();break;case'Escape':if(document.getElementById('starAppsPopup').classList.contains('open'))closeStarApps();else if(document.getElementById('settingsModal').classList.contains('open'))closeSettings();else if(document.getElementById('playerControls').classList.contains('open'))closePlayerControls();else if(document.getElementById('profilesModal').classList.contains('open'))closeProfiles();else if(document.getElementById('playerModal').classList.contains('open'))closePlayer();else if(document.getElementById('detailsModal').classList.contains('open'))closeDetails();else if(document.getElementById('searchOverlay').classList.contains('active'))closeSearchOverlay();else if(document.getElementById('confirmModal').classList.contains('open'))document.getElementById('confirmModal').classList.remove('open');break;}});
const CATEGORIES=[{label:'Action',icon:'fa-solid fa-hand-fist',color:'#ef4444',genreId:28},{label:'Comedy',icon:'fa-solid fa-face-laugh',color:'#f59e0b',genreId:35},{label:'Horror',icon:'fa-solid fa-ghost',color:'#8b5cf6',genreId:27},{label:'Sci-Fi',icon:'fa-solid fa-rocket',color:'#06b6d4',genreId:878},{label:'Romance',icon:'fa-solid fa-heart',color:'#ec4899',genreId:10749},{label:'Thriller',icon:'fa-solid fa-user-secret',color:'#64748b',genreId:53},{label:'Drama',icon:'fa-solid fa-masks-theater',color:'#a78bfa',genreId:18},{label:'Animation',icon:'fa-solid fa-wand-magic-sparkles',color:'#10b981',genreId:16},{label:'Crime',icon:'fa-solid fa-handcuffs',color:'#6b7280',genreId:80},{label:'Fantasy',icon:'fa-solid fa-dragon',color:'#7c3aed',genreId:14},{label:'Adventure',icon:'fa-solid fa-mountain-sun',color:'#f97316',genreId:12},{label:'Documentary',icon:'fa-solid fa-video',color:'#0ea5e9',genreId:99}];
const TRENDING_SEARCHES=['Stranger Things','Breaking Bad','Dune','Oppenheimer','The Bear','Inception','Avatar','Peaky Blinders','John Wick','Succession','Interstellar','The Last of Us'];
let recentSearches=[];try{recentSearches=JSON.parse(localStorage.getItem('gnRecentSearches')||'[]');}catch(e){}
let searchDebounceTimer=null,currentSearchTab='discover',lastSearchQuery='',lastSearchFilter='all';
function openSearchOverlay(){document.getElementById('searchOverlay').classList.add('active');document.body.classList.add('locked');buildDiscoverView();switchSearchTab('discover');setTimeout(()=>document.getElementById('searchOverlayInput').focus(),400);}
function closeSearchOverlay(){document.getElementById('searchOverlay').classList.remove('active');document.body.classList.remove('locked');document.getElementById('searchOverlayInput').value='';document.getElementById('searchClearBtn').classList.remove('vis');lastSearchQuery='';}
function switchSearchTab(tab){currentSearchTab=tab;document.querySelectorAll('.s-tab').forEach(t=>t.classList.remove('on'));document.getElementById(`sTab-${tab}`)?.classList.add('on');document.getElementById('searchDiscoverView').style.display=tab==='discover'?'block':'none';document.getElementById('searchResultsView').style.display=tab==='results'?'block':'none';}
function buildDiscoverView(){const recentSec=document.getElementById('recentSection');const recentList=document.getElementById('recentList');recentList.innerHTML='';if(recentSearches.length>0){recentSec.style.display='block';recentSearches.slice(0,6).forEach(q=>{const row=document.createElement('div');row.className='s-recent-row';row.innerHTML=`<div class="s-recent-ico"><i class="fa-solid fa-clock-rotate-left"></i></div><span class="s-recent-text">${q}</span><button class="s-recent-del" onclick="event.stopPropagation();deleteRecentSearch('${q.replace(/'/g,"\\'")}')"><i class="fa-solid fa-xmark"></i></button>`;row.addEventListener('click',e=>{if(e.target.closest('.s-recent-del'))return;triggerSearch(q);});recentList.appendChild(row);});}else{recentSec.style.display='none';}const tc=document.getElementById('trendingChips');tc.innerHTML='';TRENDING_SEARCHES.forEach(q=>{const chip=document.createElement('button');chip.className='s-trend-chip';chip.innerHTML=`<span class="s-chip-icon"><i class="fa-solid fa-fire-alt"></i></span>${q}`;chip.onclick=()=>triggerSearch(q);tc.appendChild(chip);});const cg=document.getElementById('categoryGrid');cg.innerHTML='';CATEGORIES.forEach(cat=>{const card=document.createElement('div');card.className='s-cat-card';card.innerHTML=`<div class="s-cat-icon" style="color:${cat.color};background:${cat.color}18"><i class="${cat.icon}"></i></div><span class="s-cat-label">${cat.label}</span>`;card.onclick=()=>browseGenre(cat.genreId,cat.label);cg.appendChild(card);});}
function triggerSearch(q){if(!q.trim())return;document.getElementById('searchOverlayInput').value=q;document.getElementById('searchClearBtn').classList.add('vis');addRecentSearch(q.trim());lastSearchQuery=q;lastSearchFilter='all';switchSearchTab('results');fetchAndRenderResults(q,'all');}
function addRecentSearch(q){recentSearches=recentSearches.filter(r=>r!==q);recentSearches.unshift(q);if(recentSearches.length>12)recentSearches=recentSearches.slice(0,12);localStorage.setItem('gnRecentSearches',JSON.stringify(recentSearches));}
function deleteRecentSearch(q){recentSearches=recentSearches.filter(r=>r!==q);localStorage.setItem('gnRecentSearches',JSON.stringify(recentSearches));buildDiscoverView();}
function clearRecentSearches(){recentSearches=[];localStorage.setItem('gnRecentSearches',JSON.stringify(recentSearches));buildDiscoverView();}
async function browseGenre(genreId,label){switchSearchTab('results');const bar=document.getElementById('searchResultsBar');const grid=document.getElementById('searchResultsGrid');bar.innerHTML=`<div class="s-results-count"><strong>${label}</strong></div>`;grid.innerHTML=`<div class="s-loading"><div class="s-spinner"></div><span class="s-loading-txt">Finding ${label} titles…</span></div>`;try{const[m,t]=await Promise.all([fetc(`${BASE}/discover/movie?api_key=${API_KEY}&with_genres=${genreId}&sort_by=popularity.desc`),fetc(`${BASE}/discover/tv?api_key=${API_KEY}&with_genres=${genreId}&sort_by=popularity.desc`)]);const items=[...(m?.results||[]).map(i=>({...i,media_type:'movie'})),...(t?.results||[]).map(i=>({...i,media_type:'tv'}))].sort((a,b)=>b.popularity-a.popularity);bar.innerHTML=`<div class="s-results-count"><strong>${label}</strong> · <span>${items.length} titles</span></div>`;renderResultsGrid(items.slice(0,60),grid);}catch(e){grid.innerHTML=`<div class="s-empty"><div class="s-empty-icon"><i class="fa-solid fa-triangle-exclamation"></i></div><h3>Couldn't Load</h3><p>Try again later</p></div>`;}}
async function fetchAndRenderResults(q,filter='all'){const bar=document.getElementById('searchResultsBar');const grid=document.getElementById('searchResultsGrid');bar.innerHTML=`<div class="s-results-count">Searching <strong>"${q}"</strong>…</div>`;grid.innerHTML=`<div class="s-loading"><div class="s-spinner"></div><span class="s-loading-txt">Searching…</span></div>`;try{const d=await fetc(`${BASE}/search/multi?api_key=${API_KEY}&query=${encodeURIComponent(q)}&include_adult=false`);let all=(d?.results||[]).filter(i=>i.media_type==='movie'||i.media_type==='tv');const total=all.length;let results=all;if(filter==='movie')results=all.filter(i=>i.media_type==='movie');else if(filter==='tv')results=all.filter(i=>i.media_type==='tv');bar.innerHTML='';const countDiv=document.createElement('div');countDiv.className='s-results-count';countDiv.innerHTML=`<strong>${total}</strong> result${total!==1?'s':''} for "${q}"`;bar.appendChild(countDiv);const filterRow=document.createElement('div');filterRow.className='s-filter-row';[['all','All'],['movie','Movies'],['tv','TV']].forEach(([f,label])=>{const btn=document.createElement('button');btn.className=`s-filter-pill${filter===f?' on':''}`;btn.textContent=label;btn.onclick=()=>{lastSearchFilter=f;fetchAndRenderResults(q,f);};filterRow.appendChild(btn);});bar.appendChild(filterRow);if(!results.length){grid.innerHTML=`<div class="s-empty"><div class="s-empty-icon"><i class="fa-solid fa-face-sad-tear"></i></div><h3>No Results</h3><p>Try a different title or use a genre instead</p></div>`;return;}renderResultsGrid(results.slice(0,60),grid);}catch(e){grid.innerHTML=`<div class="s-empty"><div class="s-empty-icon"><i class="fa-solid fa-wifi"></i></div><h3>Something Went Wrong</h3><p>Check your connection and try again</p></div>`;}}
function renderResultsGrid(items,grid){grid.innerHTML='';items.forEach(item=>{const poster=item.poster_path?`${IMG}w342${item.poster_path}`:FB_P;const year=(item.release_date||item.first_air_date||'').slice(0,4);const rating=item.vote_average?item.vote_average.toFixed(1):'';const isTv=item.media_type==='tv';window[`_item_${item.id}`]=item;const card=document.createElement('div');card.className='sr-card';card.innerHTML=`<img src="${poster}" alt="${item.title||item.name}" loading="lazy" onerror="this.src='${FB_P}'"><div class="sr-badge">${isTv?'TV':'Film'}</div><div class="sr-overlay"><div class="sr-title">${item.title||item.name}</div><div class="sr-meta">${rating?`<i class="fa-solid fa-star" style="color:#f59e0b;font-size:8px"></i>${rating}`:''}${year?`<span style="opacity:.6">·</span>${year}`:''}</div></div>`;card.addEventListener('click',()=>{closeSearchOverlay();setTimeout(()=>openDetails(item),200);});grid.appendChild(card);});}
document.getElementById('searchOverlayInput').addEventListener('input',function(){const q=this.value.trim();document.getElementById('searchClearBtn').classList.toggle('vis',q.length>0);clearTimeout(searchDebounceTimer);if(!q){switchSearchTab('discover');buildDiscoverView();return;}switchSearchTab('results');document.getElementById('searchResultsGrid').innerHTML=`<div class="s-loading"><div class="s-spinner"></div></div>`;document.getElementById('searchResultsBar').innerHTML='';searchDebounceTimer=setTimeout(()=>{lastSearchQuery=q;lastSearchFilter='all';fetchAndRenderResults(q,'all');},420);});
document.getElementById('searchOverlayInput').addEventListener('keydown',function(e){if(e.key==='Escape'){closeSearchOverlay();return;}if(e.key==='Enter'){const q=this.value.trim();if(q){addRecentSearch(q);lastSearchQuery=q;fetchAndRenderResults(q,lastSearchFilter);}}});
document.getElementById('searchClearBtn').addEventListener('click',()=>{document.getElementById('searchOverlayInput').value='';document.getElementById('searchClearBtn').classList.remove('vis');document.getElementById('searchOverlayInput').focus();switchSearchTab('discover');buildDiscoverView();});
function loadAllCats(){loadCat('/trending/all/day','trendingRow','movie');loadCat('/discover/movie','actionRow','movie',GENRES.ACTION);loadCat('/discover/movie','comedyRow','movie',GENRES.COMEDY);loadCat('/discover/movie','horrorRow','movie',GENRES.HORROR);loadCat('/discover/movie','scifiRow','movie',GENRES.SCIFI);loadCat('/discover/movie','romanceRow','movie',GENRES.ROMANCE);loadCat('/discover/movie','thrillerRow','movie',GENRES.THRILLER);loadCat('/discover/movie','dramaRow','movie',GENRES.DRAMA);loadCat('/discover/movie','animRow','movie',GENRES.ANIMATION);loadCat('/discover/movie','docRow','movie',GENRES.DOC);loadCat('/discover/movie','crimeRow','movie',GENRES.CRIME);loadCat('/discover/movie','mysteryRow','movie',GENRES.MYSTERY);loadCat('/discover/movie','fantasyRow','movie',GENRES.FANTASY);loadCat('/discover/movie','familyRow','movie',GENRES.FAMILY);loadCat('/discover/movie','advRow','movie',GENRES.ADVENTURE);loadCat('/movie/popular','moviesRow','movie');loadCat('/tv/popular','tvRow','tv');loadNewReleases();fetc(`${BASE}/trending/all/week?api_key=${API_KEY}`).then(d=>{const row=document.getElementById('top10Row');row.innerHTML='';if(d?.results)d.results.slice(0,10).forEach((item,i)=>{item.media_type=item.first_air_date?'tv':'movie';window[`_item_${item.id}`]=item;createTop10(item,i+1,row);});});fetc(`${BASE}/discover/tv?api_key=${API_KEY}&with_original_language=ko&sort_by=popularity.desc`).then(d=>{const c=document.getElementById('kdramaRow');c.innerHTML='';if(d?.results)d.results.slice(0,16).forEach(item=>{item.media_type='tv';window[`_item_${item.id}`]=item;createCard(item,c);});});fetc(`${BASE}/discover/tv?api_key=${API_KEY}&with_keywords=210024&sort_by=popularity.desc`).then(d=>{const c=document.getElementById('animeRow');c.innerHTML='';if(d?.results)d.results.slice(0,16).forEach(item=>{item.media_type='tv';window[`_item_${item.id}`]=item;createCard(item,c);});});fetc(`${BASE}/movie/top_rated?api_key=${API_KEY}&language=en-US`).then(d=>{const c=document.getElementById('awardRow');c.innerHTML='';if(d?.results)d.results.slice(0,16).forEach(item=>{item.media_type='movie';window[`_item_${item.id}`]=item;createCard(item,c);});});}
initTheme();updateListCount();updateProfileIcons(activeProfile);
document.getElementById('serverSelect').value=currentServer;document.getElementById('settingsServerSelect').value=currentServer;
if(continueW.length>0){document.getElementById('continueInline').style.display='block';renderContinueInline();}
showHome();loadHero();loadHotToday();loadAllCats();loadMore();loadMore();observeAll();
</script>
</body>
</html>
