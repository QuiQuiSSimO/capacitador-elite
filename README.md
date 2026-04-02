# capacitador-elite
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#0A0A0A">
<title>Capacitador Elite Â· Logos Group 29239</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Crimson+Pro:ital,wght@0,400;0,600;1,400&family=IBM+Plex+Mono:wght@400;600&display=swap" rel="stylesheet">
<style>
:root {
  --gold: #C9A84C;
  --gold2: #E8C97A;
  --gold3: rgba(201,168,76,.12);
  --gold4: rgba(201,168,76,.06);
  --bg: #0A0A0A;
  --bg2: #111;
  --bg3: #161616;
  --card: #141414;
  --card2: #1A1A1A;
  --border: rgba(201,168,76,.18);
  --border2: rgba(255,255,255,.06);
  --text: #F5F0E8;
  --text2: #A09880;
  --text3: #555;
  --red: #C0392B;
  --green: #27AE60;
  --blue: #3A7BD5;
  --radius: 14px;
  --mode-color: var(--gold);
}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
html{scroll-behavior:smooth}
body{
  font-family:'Crimson Pro',Georgia,serif;
  background:var(--bg);color:var(--text);
  font-size:16px;line-height:1.7;overflow-x:hidden;
  padding-bottom:env(safe-area-inset-bottom);
}
::-webkit-scrollbar{width:2px}
::-webkit-scrollbar-thumb{background:var(--gold);border-radius:99px}

/* â•â•â• APP â•â•â• */
.app{max-width:480px;margin:0 auto;min-height:100vh}

/* â•â•â• HEADER â•â•â• */
.header{
  background:var(--bg2);border-bottom:1px solid var(--border);
  padding:14px 16px 10px;position:sticky;top:0;z-index:100;
}
.hdr-top{display:flex;align-items:center;gap:10px;margin-bottom:10px}
.hdr-logo{
  font-family:'Bebas Neue',sans-serif;font-size:20px;letter-spacing:2px;
  color:var(--gold);flex:1;
}
.hdr-logo span{color:var(--text3);font-size:11px;letter-spacing:3px;display:block;font-family:'IBM Plex Mono',monospace;margin-top:-4px}
.mode-toggle{
  display:flex;background:var(--bg3);border:1px solid var(--border2);
  border-radius:20px;overflow:hidden;
}
.mode-btn{
  padding:5px 12px;font-size:10px;font-weight:600;font-family:'IBM Plex Mono',monospace;
  letter-spacing:1px;text-transform:uppercase;border:none;background:transparent;
  color:var(--text3);cursor:pointer;transition:all .2s;
}
.mode-btn.active{background:var(--gold);color:#0A0A0A}
.hdr-progress{display:flex;align-items:center;gap:8px}
.prog-label{font-size:10px;color:var(--text3);font-family:'IBM Plex Mono',monospace;letter-spacing:1px}
.prog-track{flex:1;height:3px;background:var(--bg3);border-radius:99px}
.prog-fill{height:100%;background:var(--gold);border-radius:99px;transition:width .5s}
.prog-val{font-size:10px;color:var(--gold);font-family:'IBM Plex Mono',monospace;min-width:30px;text-align:right}

/* â•â•â• NAV TABS â•â•â• */
.nav-tabs{
  display:flex;overflow-x:auto;background:var(--bg2);
  border-bottom:1px solid var(--border2);
  position:sticky;top:85px;z-index:99;
}
.nav-tabs::-webkit-scrollbar{display:none}
.nt{
  flex-shrink:0;padding:10px 14px;font-size:10px;font-weight:600;
  font-family:'IBM Plex Mono',monospace;letter-spacing:1px;text-transform:uppercase;
  color:var(--text3);border:none;background:none;cursor:pointer;
  border-bottom:2px solid transparent;white-space:nowrap;transition:all .2s;
}
.nt.active{color:var(--gold);border-bottom-color:var(--gold)}

/* â•â•â• SCREENS â•â•â• */
.screen{display:none;padding-bottom:60px}
.screen.active{display:block}

/* â•â•â• CHAPTER CARDS â•â•â• */
.chapter-list{padding:14px}
.ch-card{
  background:var(--card);border:1px solid var(--border2);
  border-radius:var(--radius);margin-bottom:10px;overflow:hidden;
  cursor:pointer;transition:all .2s;
}
.ch-card:active{transform:scale(.98)}
.ch-card.completed{border-color:rgba(39,174,96,.3)}
.ch-card-top{display:flex;align-items:center;gap:12px;padding:14px}
.ch-num{
  font-family:'Bebas Neue',sans-serif;font-size:28px;color:var(--gold3);
  width:40px;text-align:center;flex-shrink:0;line-height:1;
  border:1px solid var(--border);border-radius:8px;padding:4px;
}
.ch-card.completed .ch-num{color:var(--green);border-color:rgba(39,174,96,.3)}
.ch-info{flex:1;min-width:0}
.ch-title{font-family:'Bebas Neue',sans-serif;font-size:16px;letter-spacing:.5px;color:var(--text);line-height:1.2}
.ch-sub{font-size:12px;color:var(--text2);margin-top:2px;font-style:italic}
.ch-meta{display:flex;gap:6px;margin-top:6px;flex-wrap:wrap}
.ch-tag{font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:1px;padding:2px 7px;border-radius:20px;background:var(--gold4);color:var(--gold);border:1px solid var(--border)}
.ch-arrow{color:var(--text3);font-size:18px;flex-shrink:0}

/* â•â•â• CHAPTER DETAIL â•â•â• */
.chapter-detail{display:none}
.chapter-detail.active{display:block}
.ch-detail-header{
  background:var(--bg2);border-bottom:1px solid var(--border);
  padding:14px 16px;position:sticky;top:85px;z-index:98;
}
.ch-back{
  display:flex;align-items:center;gap:8px;margin-bottom:8px;
  font-size:11px;color:var(--text3);font-family:'IBM Plex Mono',monospace;
  letter-spacing:1px;cursor:pointer;background:none;border:none;
}
.ch-back:hover{color:var(--gold)}
.ch-detail-title{font-family:'Bebas Neue',sans-serif;font-size:22px;letter-spacing:1px;color:var(--text)}
.ch-detail-sub{font-size:13px;color:var(--text2);font-style:italic;margin-top:2px}
.ch-tabs{display:flex;gap:0;margin-top:10px;background:var(--bg3);border-radius:8px;padding:3px}
.ch-tab{
  flex:1;padding:6px;font-size:10px;font-family:'IBM Plex Mono',monospace;
  letter-spacing:.5px;text-transform:uppercase;border:none;background:transparent;
  color:var(--text3);cursor:pointer;border-radius:6px;transition:all .2s;text-align:center;
}
.ch-tab.active{background:var(--gold);color:#0A0A0A;font-weight:600}

/* â•â•â• CONTENT PANEL â•â•â• */
.content-panel{padding:16px}
.content-block{margin-bottom:20px}

/* Content del manual */
.manual-text{font-size:15px;color:var(--text2);line-height:1.8}
.manual-text strong{color:var(--text)}
.manual-h3{font-family:'Bebas Neue',sans-serif;font-size:18px;letter-spacing:.5px;color:var(--gold);margin:20px 0 10px}
.distincion{
  background:var(--bg3);border:1px solid var(--border);
  border-radius:var(--radius);padding:14px;margin:14px 0;
}
.distincion-label{font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:2px;text-transform:uppercase;margin-bottom:6px}
.distincion-label.r{color:var(--red)}
.distincion-label.g{color:var(--green)}
.distincion-grid{display:grid;grid-template-columns:1fr auto 1fr;gap:8px;align-items:center}
.distincion-side{border-radius:8px;padding:10px;font-size:13px;line-height:1.5}
.distincion-side.r{background:rgba(192,57,43,.08);border:1px solid rgba(192,57,43,.2)}
.distincion-side.g{background:rgba(39,174,96,.08);border:1px solid rgba(39,174,96,.2)}
.distincion-arrow{color:var(--gold);font-size:18px;text-align:center}
.exercise-box{
  background:var(--gold4);border:1px solid var(--border);
  border-radius:var(--radius);padding:14px;margin:14px 0;
}
.exercise-label{font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:6px}
.callout{
  border-left:3px solid var(--gold);padding:12px 14px;
  font-style:italic;color:var(--text2);font-size:15px;margin:14px 0;
  background:var(--gold4);border-radius:0 8px 8px 0;
}

/* â•â•â• GUÃA CAPACITADOR â•â•â• */
.trainer-panel{background:var(--bg3);border-radius:var(--radius);padding:14px;margin-bottom:14px;border:1px solid var(--border)}
.trainer-section{margin-bottom:16px}
.trainer-section:last-child{margin-bottom:0}
.trainer-label{
  font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:2px;
  text-transform:uppercase;color:var(--gold);margin-bottom:8px;
  display:flex;align-items:center;gap:6px;
}
.trainer-label::before{content:'';display:block;width:16px;height:1px;background:var(--gold)}
.trainer-text{font-size:14px;color:var(--text2);line-height:1.7}
.trainer-text li{margin-bottom:6px;padding-left:14px;position:relative}
.trainer-text li::before{content:'â†’';position:absolute;left:0;color:var(--gold);font-size:12px}
.debate-q{
  background:var(--card2);border:1px solid var(--border2);
  border-radius:10px;padding:12px;margin-bottom:8px;
  font-size:14px;color:var(--text);
}
.debate-q-num{font-size:10px;font-family:'IBM Plex Mono',monospace;color:var(--gold);letter-spacing:1px;margin-bottom:4px}

/* â•â•â• TIMER â•â•â• */
.timer-widget{
  background:var(--card2);border:1px solid var(--border);
  border-radius:var(--radius);padding:14px;margin-bottom:14px;
  display:flex;align-items:center;gap:12px;
}
.timer-display{
  font-family:'Bebas Neue',sans-serif;font-size:36px;letter-spacing:2px;
  color:var(--gold);min-width:90px;text-align:center;
}
.timer-display.running{color:var(--green)}
.timer-display.warning{color:#E8A84C}
.timer-display.ended{color:var(--red)}
.timer-controls{display:flex;flex-direction:column;gap:6px;flex:1}
.timer-presets{display:flex;gap:4px;flex-wrap:wrap}
.timer-preset{
  padding:4px 8px;font-size:10px;font-family:'IBM Plex Mono',monospace;
  background:var(--bg3);border:1px solid var(--border2);border-radius:6px;
  color:var(--text3);cursor:pointer;transition:all .2s;
}
.timer-preset:hover,.timer-preset.active{background:var(--gold4);color:var(--gold);border-color:var(--border)}
.timer-btns{display:flex;gap:6px}
.tbtn{
  flex:1;padding:7px;font-size:11px;font-family:'IBM Plex Mono',monospace;
  letter-spacing:1px;text-transform:uppercase;border:none;border-radius:8px;
  cursor:pointer;font-weight:600;transition:all .2s;
}
.tbtn:active{transform:scale(.95)}
.tbtn-start{background:var(--green);color:#fff}
.tbtn-pause{background:var(--gold);color:#0A0A0A}
.tbtn-reset{background:var(--bg3);color:var(--text3);border:1px solid var(--border2)}

/* â•â•â• ROLEPLAY â•â•â• */
.roleplay-chat{
  background:var(--bg);border:1px solid var(--border2);border-radius:var(--radius);
  height:300px;overflow-y:auto;padding:12px;margin-bottom:10px;
}
.rp-msg{margin-bottom:10px;max-width:85%}
.rp-msg.ai{margin-left:0}
.rp-msg.user{margin-left:auto}
.rp-who{font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:1px;margin-bottom:3px;text-transform:uppercase}
.rp-who.ai{color:var(--red)}
.rp-who.user{color:var(--blue);text-align:right}
.rp-bubble{
  padding:10px 12px;border-radius:10px;font-size:14px;line-height:1.6;
}
.rp-bubble.ai{background:rgba(192,57,43,.1);border:1px solid rgba(192,57,43,.2);color:var(--text)}
.rp-bubble.user{background:rgba(58,123,213,.1);border:1px solid rgba(58,123,213,.2);color:var(--text)}
.rp-input-row{display:flex;gap:8px}
.rp-input{
  flex:1;background:var(--bg2);border:1px solid var(--border2);
  border-radius:10px;padding:10px 12px;font-size:14px;
  color:var(--text);font-family:'Crimson Pro',serif;outline:none;
  resize:none;height:48px;
}
.rp-input:focus{border-color:var(--border)}
.rp-send{
  background:var(--gold);color:#0A0A0A;border:none;
  border-radius:10px;padding:0 16px;font-size:18px;cursor:pointer;
}
.rp-scenarios{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:10px}
.rp-scenario{
  padding:5px 10px;font-size:11px;font-family:'IBM Plex Mono',monospace;
  background:var(--bg3);border:1px solid var(--border2);border-radius:20px;
  color:var(--text3);cursor:pointer;transition:all .2s;
}
.rp-scenario.active{background:var(--gold4);color:var(--gold);border-color:var(--border)}
.rp-loading{color:var(--text3);font-style:italic;font-size:13px;padding:8px 0}

/* â•â•â• SEGUIMIENTO â•â•â• */
.tracker-header{padding:14px;border-bottom:1px solid var(--border2)}
.add-member-row{display:flex;gap:8px;margin-bottom:14px}
.input-dark{
  flex:1;background:var(--bg2);border:1px solid var(--border2);
  border-radius:10px;padding:10px 12px;font-size:14px;
  color:var(--text);font-family:'Crimson Pro',serif;outline:none;
}
.input-dark:focus{border-color:var(--border)}
.btn-add{
  background:var(--gold);color:#0A0A0A;border:none;
  border-radius:10px;padding:0 16px;font-size:14px;font-weight:700;
  cursor:pointer;font-family:'IBM Plex Mono',monospace;
}
.member-card{
  background:var(--card);border:1px solid var(--border2);
  border-radius:var(--radius);margin:0 14px 10px;overflow:hidden;
}
.member-header{
  display:flex;align-items:center;gap:10px;padding:12px 14px;
  cursor:pointer;
}
.member-avatar{
  width:36px;height:36px;border-radius:50%;background:var(--gold4);
  border:1px solid var(--border);display:flex;align-items:center;justify-content:center;
  font-family:'Bebas Neue',sans-serif;font-size:16px;color:var(--gold);flex-shrink:0;
}
.member-name{font-size:15px;font-weight:600;flex:1}
.member-prog{font-size:11px;color:var(--gold);font-family:'IBM Plex Mono',monospace}
.member-chapters{padding:0 14px 12px;display:none}
.member-chapters.open{display:block}
.ch-progress-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:6px;margin-bottom:10px}
.ch-prog-item{
  aspect-ratio:1;border-radius:8px;border:1px solid var(--border2);
  background:var(--bg3);display:flex;flex-direction:column;
  align-items:center;justify-content:center;cursor:pointer;transition:all .2s;
}
.ch-prog-item.done{background:rgba(39,174,96,.12);border-color:rgba(39,174,96,.3)}
.ch-prog-item .cpn{font-family:'Bebas Neue',sans-serif;font-size:16px;color:var(--text3)}
.ch-prog-item.done .cpn{color:var(--green)}
.ch-prog-item .cpc{font-size:8px;color:var(--text3);font-family:'IBM Plex Mono',monospace;letter-spacing:.5px}
.member-notes-input{
  width:100%;background:var(--bg2);border:1px solid var(--border2);
  border-radius:8px;padding:8px 10px;font-size:13px;color:var(--text);
  font-family:'Crimson Pro',serif;resize:none;height:60px;outline:none;
}
.member-notes-input:focus{border-color:var(--border)}
.del-member{
  background:none;border:none;color:var(--text3);cursor:pointer;
  font-size:16px;padding:4px;
}
.del-member:hover{color:var(--red)}

/* â•â•â• NOTAS CAPACITADOR â•â•â• */
.notas-screen{padding:14px}
.notas-header{margin-bottom:14px}
.nota-card{
  background:var(--card);border:1px solid var(--border2);
  border-radius:var(--radius);margin-bottom:10px;overflow:hidden;
}
.nota-card-header{
  display:flex;align-items:center;justify-content:space-between;
  padding:10px 14px;border-bottom:1px solid var(--border2);
}
.nota-date{font-size:10px;color:var(--text3);font-family:'IBM Plex Mono',monospace}
.nota-ch{font-size:10px;color:var(--gold);font-family:'IBM Plex Mono',monospace}
.nota-text{padding:10px 14px;font-size:14px;color:var(--text2);line-height:1.7}
.new-nota-form{
  background:var(--bg2);border:1px solid var(--border);
  border-radius:var(--radius);padding:14px;margin-bottom:14px;
}
.nota-textarea{
  width:100%;background:var(--bg3);border:1px solid var(--border2);
  border-radius:8px;padding:10px;font-size:14px;color:var(--text);
  font-family:'Crimson Pro',serif;resize:none;height:80px;outline:none;
  margin-bottom:8px;
}
.nota-textarea:focus{border-color:var(--border)}
.nota-selects{display:flex;gap:8px;margin-bottom:8px}
.nota-select{
  flex:1;background:var(--bg3);border:1px solid var(--border2);
  border-radius:8px;padding:8px;font-size:13px;color:var(--text);
  font-family:'Crimson Pro',serif;outline:none;
}
.btn-save-nota{
  width:100%;background:var(--gold);color:#0A0A0A;border:none;
  border-radius:8px;padding:10px;font-size:13px;font-weight:700;
  font-family:'IBM Plex Mono',monospace;letter-spacing:1px;cursor:pointer;
}

/* â•â•â• COACH IA â•â•â• */
.coach-container{height:calc(100vh - 220px);display:flex;flex-direction:column}
.coach-messages{flex:1;overflow-y:auto;padding:14px}
.coach-msg{margin-bottom:12px;max-width:88%}
.coach-msg.ai{margin-left:0}
.coach-msg.user{margin-left:auto}
.coach-who{font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:1px;margin-bottom:3px;text-transform:uppercase;color:var(--gold)}
.coach-who.u{color:var(--blue);text-align:right}
.coach-bubble{
  padding:10px 14px;border-radius:12px;font-size:14px;line-height:1.7;
}
.coach-bubble.ai{background:var(--gold4);border:1px solid var(--border);color:var(--text)}
.coach-bubble.user{background:rgba(58,123,213,.1);border:1px solid rgba(58,123,213,.2);color:var(--text)}
.coach-loading{color:var(--text3);font-style:italic;font-size:13px;padding:8px 14px}
.coach-input-area{padding:10px 14px;border-top:1px solid var(--border2);background:var(--bg2)}
.coach-quick{display:flex;gap:6px;overflow-x:auto;margin-bottom:8px;padding-bottom:2px}
.coach-quick::-webkit-scrollbar{display:none}
.cq{
  flex-shrink:0;padding:5px 10px;font-size:11px;font-family:'IBM Plex Mono',monospace;
  background:var(--bg3);border:1px solid var(--border2);border-radius:20px;
  color:var(--text3);cursor:pointer;white-space:nowrap;transition:all .2s;
}
.cq:active{background:var(--gold4);color:var(--gold)}
.coach-row{display:flex;gap:8px}
.coach-in{
  flex:1;background:var(--bg3);border:1px solid var(--border2);
  border-radius:12px;padding:10px 12px;font-size:14px;
  color:var(--text);font-family:'Crimson Pro',serif;outline:none;resize:none;height:44px;
}
.coach-in:focus{border-color:var(--border)}
.coach-send{
  background:var(--gold);color:#0A0A0A;border:none;
  border-radius:12px;padding:0 16px;font-size:18px;cursor:pointer;
}

/* â•â•â• INICIO â•â•â• */
.inicio-hero{
  background:linear-gradient(180deg,var(--bg2) 0%,var(--bg) 100%);
  border-bottom:1px solid var(--border);padding:24px 16px 20px;text-align:center;
}
.hero-badge{
  font-size:9px;font-family:'IBM Plex Mono',monospace;letter-spacing:3px;
  text-transform:uppercase;color:var(--gold);border:1px solid var(--border);
  padding:4px 14px;border-radius:20px;display:inline-block;margin-bottom:16px;
}
.hero-title{font-family:'Bebas Neue',sans-serif;font-size:34px;letter-spacing:2px;color:var(--text);line-height:1}
.hero-title span{color:var(--gold);display:block}
.hero-sub{font-size:14px;color:var(--text2);font-style:italic;margin-top:8px}
.stat-row{display:flex;gap:8px;padding:14px}
.stat-card{
  flex:1;background:var(--card);border:1px solid var(--border2);
  border-radius:12px;padding:12px;text-align:center;
}
.stat-num{font-family:'Bebas Neue',sans-serif;font-size:28px;color:var(--gold)}
.stat-lbl{font-size:10px;color:var(--text3);font-family:'IBM Plex Mono',monospace;letter-spacing:1px;text-transform:uppercase;margin-top:2px}
.mode-info{
  margin:0 14px 14px;background:var(--gold4);border:1px solid var(--border);
  border-radius:var(--radius);padding:14px;
}
.mode-info.alumno{background:rgba(58,123,213,.06);border-color:rgba(58,123,213,.2)}
.mode-title{font-family:'Bebas Neue',sans-serif;font-size:16px;letter-spacing:1px;color:var(--gold);margin-bottom:4px}
.mode-title.alumno{color:var(--blue)}
.mode-desc{font-size:13px;color:var(--text2)}

/* â•â•â• TOAST â•â•â• */
.toast{
  position:fixed;bottom:80px;left:50%;transform:translateX(-50%) translateY(20px);
  background:var(--card2);border:1px solid var(--border);
  border-radius:20px;padding:8px 18px;font-size:13px;color:var(--text);
  font-family:'IBM Plex Mono',monospace;z-index:999;
  opacity:0;transition:all .3s;pointer-events:none;white-space:nowrap;
}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0)}

/* â•â•â• AJUSTES â•â•â• */
.ajustes-section{padding:14px}
.ajuste-card{background:var(--card);border:1px solid var(--border2);border-radius:var(--radius);margin-bottom:10px;overflow:hidden}
.ajuste-hdr{padding:12px 14px;border-bottom:1px solid var(--border2);font-size:11px;font-family:'IBM Plex Mono',monospace;letter-spacing:2px;color:var(--gold);text-transform:uppercase}
.ajuste-body{padding:14px}
.ajuste-label{font-size:11px;color:var(--text3);font-family:'IBM Plex Mono',monospace;letter-spacing:1px;margin-bottom:6px;text-transform:uppercase}
.ajuste-input{
  width:100%;background:var(--bg2);border:1px solid var(--border2);
  border-radius:8px;padding:10px 12px;font-size:14px;color:var(--text);
  font-family:'Crimson Pro',serif;outline:none;margin-bottom:12px;
}
.ajuste-input:focus{border-color:var(--border)}
.btn-save{
  width:100%;background:var(--gold);color:#0A0A0A;border:none;
  border-radius:10px;padding:12px;font-size:13px;font-weight:700;
  font-family:'IBM Plex Mono',monospace;letter-spacing:1px;cursor:pointer;
}
</style>
</head>
<body>
<div class="app">

<!-- HEADER -->
<div class="header">
  <div class="hdr-top">
    <div class="hdr-logo">
      Capacitador Elite
      <span>Logos Group 29239</span>
    </div>
    <div class="mode-toggle">
      <button class="mode-btn active" id="btn-capacitador" onclick="setMode('capacitador')">ðŸ‘‘ LÃ­der</button>
      <button class="mode-btn" id="btn-alumno" onclick="setMode('alumno')">ðŸ“– Alumno</button>
    </div>
  </div>
  <div class="hdr-progress">
    <span class="prog-label">PROGRESO</span>
    <div class="prog-track"><div class="prog-fill" id="prog-fill" style="width:0%"></div></div>
    <span class="prog-val" id="prog-val">0/9</span>
  </div>
</div>

<!-- NAV -->
<div class="nav-tabs" id="nav-tabs">
  <button class="nt active" onclick="goTab('inicio',this)">Inicio</button>
  <button class="nt" onclick="goTab('capitulos',this)">CapÃ­tulos</button>
  <button class="nt capacitador-only" onclick="goTab('seguimiento',this)">Equipo</button>
  <button class="nt capacitador-only" onclick="goTab('notas',this)">Notas</button>
  <button class="nt" onclick="goTab('coach',this)">Coach IA</button>
  <button class="nt" onclick="goTab('ajustes',this)">âš™ï¸</button>
</div>

<!-- INICIO -->
<div class="screen active" id="screen-inicio">
  <div class="inicio-hero">
    <div class="hero-badge">Manual de Alto Rendimiento</div>
    <div class="hero-title">Mentalidad<span>de Ã‰lite</span></div>
    <div class="hero-sub">Royal Prestige Â· Logos Group 29239</div>
  </div>
  <div class="stat-row">
    <div class="stat-card"><div class="stat-num" id="stat-caps">0</div><div class="stat-lbl">Caps Vistos</div></div>
    <div class="stat-card"><div class="stat-num" id="stat-members">0</div><div class="stat-lbl">En Equipo</div></div>
    <div class="stat-card"><div class="stat-num" id="stat-sessions">0</div><div class="stat-lbl">Sesiones</div></div>
  </div>
  <div class="mode-info" id="mode-info-box">
    <div class="mode-title">Modo Capacitador Activo</div>
    <div class="mode-desc">TenÃ©s acceso a la guÃ­a del capacitador, preguntas de debate, roleplay con IA y seguimiento de equipo en cada capÃ­tulo.</div>
  </div>
  <div style="padding:0 14px 14px">
    <button class="btn-save" onclick="goTab('capitulos',document.querySelectorAll('.nt')[1])">Ir a CapÃ­tulos â†’</button>
  </div>
</div>

<!-- CAPÃTULOS -->
<div class="screen" id="screen-capitulos">
  <!-- Lista -->
  <div id="chapter-list-view">
    <div class="chapter-list" id="chapter-list"></div>
  </div>
  <!-- Detalle -->
  <div id="chapter-detail-view" style="display:none">
    <div class="ch-detail-header">
      <button class="ch-back" onclick="backToList()">â† VOLVER A CAPÃTULOS</button>
      <div class="ch-detail-title" id="detail-title">Cap. 1</div>
      <div class="ch-detail-sub" id="detail-sub"></div>
      <div class="ch-tabs" id="detail-tabs">
        <button class="ch-tab active" onclick="switchDetailTab('contenido',this)">Contenido</button>
        <button class="ch-tab capacitador-only" onclick="switchDetailTab('guia',this)">GuÃ­a</button>
        <button class="ch-tab capacitador-only" onclick="switchDetailTab('debate',this)">Debate</button>
        <button class="ch-tab capacitador-only" onclick="switchDetailTab('roleplay',this)">Roleplay</button>
      </div>
    </div>
    <div id="detail-contenido" class="content-panel"></div>
    <div id="detail-guia" class="content-panel" style="display:none"></div>
    <div id="detail-debate" class="content-panel" style="display:none"></div>
    <div id="detail-roleplay" class="content-panel" style="display:none"></div>
  </div>
</div>

<!-- SEGUIMIENTO EQUIPO -->
<div class="screen" id="screen-seguimiento">
  <div class="tracker-header" style="padding:14px">
    <div class="add-member-row">
      <input class="input-dark" id="new-member-name" placeholder="Nombre del distribuidor..." onkeydown="if(event.key==='Enter')addMember()">
      <button class="btn-add" onclick="addMember()">+ Agregar</button>
    </div>
  </div>
  <div id="members-list"></div>
</div>

<!-- NOTAS -->
<div class="screen" id="screen-notas">
  <div class="notas-screen">
    <div class="new-nota-form">
      <div style="font-size:11px;font-family:'IBM Plex Mono',monospace;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-bottom:10px">Nueva Nota</div>
      <div class="nota-selects">
        <select class="nota-select" id="nota-member-select">
          <option value="">Miembro del equipo...</option>
        </select>
        <select class="nota-select" id="nota-cap-select">
          <option value="">CapÃ­tulo...</option>
        </select>
      </div>
      <textarea class="nota-textarea" id="nota-text" placeholder="Observaciones de la sesiÃ³n, fortalezas, Ã¡reas a mejorar..."></textarea>
      <button class="btn-save-nota" onclick="saveNota()">Guardar Nota</button>
    </div>
    <div id="notas-list"></div>
  </div>
</div>

<!-- COACH IA -->
<div class="screen" id="screen-coach">
  <div class="coach-container">
    <div class="coach-messages" id="coach-msgs">
      <div class="coach-msg ai">
        <div class="coach-who">ðŸ‘‘ Coach Â· Logos Group 29239</div>
        <div class="coach-bubble ai">Â¡Hola! Soy tu Coach IA especializado en capacitaciÃ³n del Logos Group 29239. Puedo ayudarte a preparar sesiones, responder dudas del manual, generar preguntas de debate o darte estrategias de liderazgo. Â¿Por dÃ³nde arrancamos?</div>
      </div>
    </div>
    <div class="coach-input-area">
      <div class="coach-quick">
        <button class="cq" onclick="askCoach('Â¿CÃ³mo inicio una sesiÃ³n de capacitaciÃ³n con el capÃ­tulo 1?')">Iniciar Cap 1</button>
        <button class="cq" onclick="askCoach('Dame 3 estrategias para motivar a un distribuidor que quiere abandonar')">Retener equipo</button>
        <button class="cq" onclick="askCoach('Â¿CÃ³mo manejo a alguien que no avanza con el manual?')">Distribuidor bloqueado</button>
        <button class="cq" onclick="askCoach('PrepÃ¡rame una reuniÃ³n de equipo de 45 minutos para esta semana')">ReuniÃ³n semanal</button>
        <button class="cq" onclick="askCoach('Dame seÃ±ales de que un distribuidor estÃ¡ listo para ser lÃ­der')">Detectar lÃ­deres</button>
      </div>
      <div class="coach-row">
        <textarea class="coach-in" id="coach-input" placeholder="Preguntale al Coach..." onkeydown="if(event.key==='Enter'&&!event.shiftKey){event.preventDefault();sendCoach()}"></textarea>
        <button class="coach-send" onclick="sendCoach()">â†‘</button>
      </div>
    </div>
  </div>
</div>

<!-- AJUSTES -->
<div class="screen" id="screen-ajustes">
  <div class="ajustes-section">
    <div class="ajuste-card">
      <div class="ajuste-hdr">Coach IA â€” Worker URL</div>
      <div class="ajuste-body">
        <div class="ajuste-label">URL del Worker de Cloudflare</div>
        <input class="ajuste-input" id="cfg-worker" placeholder="https://coach-ia.tuusuario.workers.dev">
        <button class="btn-save" onclick="saveConfig()">Guardar</button>
      </div>
    </div>
    <div class="ajuste-card">
      <div class="ajuste-hdr">InformaciÃ³n del Capacitador</div>
      <div class="ajuste-body">
        <div class="ajuste-label">Tu nombre</div>
        <input class="ajuste-input" id="cfg-name" placeholder="Nombre del lÃ­der capacitador">
        <button class="btn-save" onclick="saveConfig()">Guardar</button>
      </div>
    </div>
    <div class="ajuste-card">
      <div class="ajuste-hdr">Datos</div>
      <div class="ajuste-body" style="display:flex;gap:8px">
        <button class="btn-save" style="background:var(--bg3);color:var(--text3);border:1px solid var(--border2)" onclick="exportData()">Exportar Backup</button>
        <button class="btn-save" onclick="importData()">Importar</button>
      </div>
    </div>
  </div>
</div>

</div><!-- /app -->

<div class="toast" id="toast"></div>

<script>
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// DATOS
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
const CHAPTERS = [
  {
    id:'cap0', num:'00',
    title:'De Distribuidor a LÃ­der de Territorio',
    sub:'El paso que separa al distribuidor del lÃ­der no es una promociÃ³n. Es una decisiÃ³n.',
    time:'45 min',
    tags:['Liderazgo','Fundamentos'],
    contenido: `
      <div class="manual-h3">El Territorio como Empresa</div>
      <div class="manual-text">Muchos no se sienten profesionales en esta industria por temor al estigma externo o las crÃ­ticas. Pero el problema no estÃ¡ afuera: estÃ¡ en cÃ³mo se perciben a sÃ­ mismos.</div>
      <div class="trainer-panel" style="background:var(--gold4);border-color:var(--border)" id="cap0-gold">
        <div class="exercise-label">La Postura del LÃ­der</div>
        <div class="manual-text">Si no te sentÃ­s un lÃ­der gestionando Territorios, el entorno lo va a percibir. Debemos pasar de la "dependencia" a la "interdependencia". Un lÃ­der de territorio no espera que las cosas sucedan; se gestiona a sÃ­ mismo para que su equipo funcione de forma autÃ³noma.</div>
      </div>
      <div class="manual-h3">El Mito del Ã‰xito Microondas</div>
      <div class="distincion">
        <div class="distincion-grid">
          <div class="distincion-side r"><div class="distincion-label r">GestiÃ³n apresurada</div>Basada solo en el nÃºmero inmediato. Quema el territorio. Genera resultados fugaces.</div>
          <div class="distincion-arrow">â†’</div>
          <div class="distincion-side g"><div class="distincion-label g">GestiÃ³n de desarrollo humano</div>Basada en el proceso y las personas. Hace el territorio duradero. Construye patrimonio real.</div>
        </div>
      </div>
      <div class="manual-h3">De Meter Gente a Desarrollar Personas</div>
      <div class="manual-text">El reclutamiento es solo volumen. La clave es la <strong>duplicaciÃ³n</strong>. El mejor liderazgo es aquel que entrena profundamente a pocos para lograr una duplicaciÃ³n real.</div>
      <div class="exercise-box">
        <div class="exercise-label">Ejercicio</div>
        <div class="manual-text">TomÃ¡ una hoja y respondÃ© estas tres preguntas como si tu territorio fuera una empresa formal: Â¿CuÃ¡l es tu propuesta de valor como lÃ­der? Â¿QuÃ© sistema de formaciÃ³n tenÃ©s para tu equipo? Â¿CuÃ¡l es tu visiÃ³n a 3, 5 y 10 aÃ±os?</div>
      </div>
      <div class="callout">"El lÃ­der que no invierte en formarse a sÃ­ mismo no tiene nada real para darle a su equipo."</div>
    `,
    guia: {
      objetivo: 'Instalar la mentalidad de territorio como empresa y eliminar la idea del Ã©xito fÃ¡cil antes de empezar con el resto del manual.',
      intro: 'AbrÃ­ la sesiÃ³n con esta pregunta: "Â¿QuÃ© diferencia a alguien que dura 6 meses en esto de alguien que construye un negocio real?" DejÃ¡ que respondan. DespuÃ©s presentÃ¡ el capÃ­tulo como la respuesta a esa pregunta.',
      seÃ±ales: ['Hacen preguntas sobre cÃ³mo manejar a su equipo', 'Hablan de proyecciÃ³n a largo plazo', 'Dejan de preguntar solo por comisiones inmediatas'],
      errores: ['Apurarse al ejercicio sin generar el debate previo', 'Saltar la distinciÃ³n entre reclutamiento y duplicaciÃ³n', 'No cerrar con el ejercicio escrito â€” es la clave del capÃ­tulo'],
      duracion: '45 min'
    },
    roleplay: {
      escenarios: ['Distribuidor que quiere resultados rÃ¡pidos', 'Alguien que recluta sin criterio', 'Distribuidor que no se siente profesional'],
      system: 'Sos un distribuidor de Royal Prestige del Logos Group 29239 en Argentina. EstÃ¡s en la etapa inicial, querÃ©s resultados rÃ¡pidos y no entendÃ©s por quÃ© el lÃ­der te habla de "largo plazo". RespondÃ© de manera realista y desafiante a lo que te diga el capacitador. UsÃ¡ lenguaje argentino casual.'
    }
  },
  {
    id:'cap2', num:'02',
    title:'Resiliencia para el Campo Real',
    sub:'Los rechazos y cancelaciones no son obstÃ¡culos del negocio. Son el negocio.',
    time:'40 min',
    tags:['Resiliencia','Campo'],
    contenido: `
      <div class="manual-h3">Los 4 Tipos de Rechazo</div>
      <div class="trainer-panel" style="margin-bottom:10px">
        <div class="exercise-label" style="color:var(--gold)">Tipo 1 â€” El "No" Definitivo</div>
        <div class="manual-text">El mÃ¡s fÃ¡cil de manejar aunque parezca lo contrario. Es definitivo, es claro. AgradecÃ©, pedÃ­ un referido y cerrÃ¡ ese ciclo. Ese "no" te liberÃ³ tiempo para un "sÃ­".</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:10px">
        <div class="exercise-label" style="color:var(--gold)">Tipo 2 â€” La CancelaciÃ³n</div>
        <div class="manual-text">Reprogramar en el acto, antes de colgar. "Â¿Podemos el miÃ©rcoles o el jueves?" Si dejÃ¡s que pase el dÃ­a, ese prospecto se enfrÃ­a para siempre.</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:10px">
        <div class="exercise-label" style="color:var(--gold)">Tipo 3 â€” El Cierre CaÃ­do</div>
        <div class="manual-text">El peor de todos. Dos causas: falta de urgencia en el cierre, o falta de seguimiento post-demo. La resiliencia acÃ¡ no es aguantar: es aprender quÃ© hacer diferente.</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:10px;border-color:rgba(192,57,43,.3)">
        <div class="exercise-label" style="color:var(--red)">Tipo 4 â€” "Es Caro"</div>
        <div class="manual-text">No es un rechazo al producto. Es una seÃ±al de que el valor no quedÃ³ claro. La respuesta no es bajar el precio. Es subir el valor percibido.</div>
      </div>
      <div class="manual-h3">El Protocolo de RecuperaciÃ³n</div>
      <div class="manual-text"><strong>1.</strong> NombrÃ¡ lo que pasÃ³, sin dramatizarlo.<br><strong>2.</strong> ExtraÃ© el aprendizaje en menos de 5 minutos.<br><strong>3.</strong> HacÃ© una acciÃ³n inmediata.</div>
      <div class="distincion">
        <div class="distincion-grid">
          <div class="distincion-side r"><div class="distincion-label r">Resiliente frÃ¡gil</div>Aguanta en silencio. Acumula. Explota o abandona cuando ya no puede mÃ¡s.</div>
          <div class="distincion-arrow">â†’</div>
          <div class="distincion-side g"><div class="distincion-label g">Resiliente sÃ³lido</div>Procesa cada rechazo en el momento. Tiene un sistema, no solo voluntad.</div>
        </div>
      </div>
      <div class="exercise-box">
        <div class="exercise-label">Ejercicio â€” El Diario de Rechazos</div>
        <div class="manual-text">Durante 3 semanas: (1) QuÃ© pasÃ³ exactamente. (2) QuÃ© aprendÃ­. (3) QuÃ© hice inmediatamente despuÃ©s. Al final revisÃ¡ el patrÃ³n.</div>
      </div>
      <div class="callout">"La resiliencia no es la ausencia de dolor. Es la decisiÃ³n de seguir moviÃ©ndose a pesar de Ã©l."</div>
    `,
    guia: {
      objetivo: 'Dar herramientas concretas para procesar rechazos y cancelaciones sin que afecten la productividad. Instalar el sistema de 3 pasos.',
      intro: 'PreguntÃ¡ al grupo: "Â¿CuÃ¡l fue el rechazo mÃ¡s difÃ­cil que tuviste y cÃ³mo lo manejaste?" EscuchÃ¡ dos o tres respuestas. Eso abre el espacio emocional para el capÃ­tulo.',
      seÃ±ales: ['Describen rechazos sin catastrofizar', 'Preguntan por el protocolo de reprogramaciÃ³n', 'Reconocen la diferencia entre hecho y juicio'],
      errores: ['Quedarte solo en los tipos de rechazo sin llegar al protocolo', 'No hacer el roleplay de reprogramaciÃ³n en vivo', 'Dejar que la sesiÃ³n se convierta en una queja grupal sobre los clientes'],
      duracion: '40 min'
    },
    roleplay: {
      escenarios: ['Cliente que cancela el dÃ­a de la demo', 'Prospecto que dice que es muy caro', 'Cierre caÃ­do â€” cliente que llama para cancelar'],
      system: 'Sos un prospecto o cliente de Royal Prestige en Argentina. EstÃ¡s en una de estas situaciones segÃºn lo que te indique el capacitador: cancelando una demo, diciendo que es caro, o llamando para cancelar una compra. RespondÃ© de forma realista y con objeciones genuinas. UsÃ¡ lenguaje argentino natural.'
    }
  },
  {
    id:'cap3', num:'03',
    title:'Manejo de Emociones en Ventas Directas',
    sub:'Tu estado emocional es el primer producto que vendÃ©s en cada demo.',
    time:'35 min',
    tags:['Emociones','Ventas'],
    contenido: `
      <div class="manual-h3">Las Objeciones como InformaciÃ³n Emocional</div>
      <div class="manual-text">Una objeciÃ³n como "es caro" o "tengo que pensarlo" no es solo una objeciÃ³n lÃ³gica. Tiene una capa emocional debajo.</div>
      <div class="trainer-panel">
        <div class="exercise-label">Mapa Emocional de las 3 Objeciones</div>
        <div class="manual-text">
          <strong>"Es caro"</strong> â†’ Inseguridad financiera o falta de urgencia. Respuesta: subir el valor percibido.<br><br>
          <strong>"Tengo que pensarlo"</strong> â†’ Miedo a decidir mal. Respuesta: incluir a la pareja en la decisiÃ³n.<br><br>
          <strong>"No tengo plata"</strong> â†’ VergÃ¼enza o restricciÃ³n real. Respuesta: empatÃ­a + opciones de financiaciÃ³n.
        </div>
      </div>
      <div class="manual-h3">MotivaciÃ³n vs. Disciplina</div>
      <div class="distincion">
        <div class="distincion-grid">
          <div class="distincion-side r"><div class="distincion-label r">MotivaciÃ³n</div>Depende de cÃ³mo te sentÃ­s. Viene y va. Desaparece cuando mÃ¡s la necesitÃ¡s.</div>
          <div class="distincion-arrow">â†’</div>
          <div class="distincion-side g"><div class="distincion-label g">Disciplina</div>No depende de cÃ³mo te sentÃ­s. Es un sistema. Funciona siempre.</div>
        </div>
      </div>
      <div class="exercise-box">
        <div class="exercise-label">Ejercicio â€” El TermÃ³metro Emocional</div>
        <div class="manual-text">Al final de cada dÃ­a: (1) Â¿CuÃ¡l fue el momento de mayor energÃ­a positiva? (2) Â¿CuÃ¡l fue el de mayor dificultad emocional? (3) Â¿QuÃ© emociÃ³n dominÃ³ y cÃ³mo la gestionÃ©?</div>
      </div>
    `,
    guia: {
      objetivo: 'Desarrollar inteligencia emocional aplicada al campo. Que el distribuidor entienda que las objeciones son emocionales, no lÃ³gicas.',
      intro: 'PedÃ­ que alguien cuente una demo en la que se sintiÃ³ descolocado emocionalmente. Â¿QuÃ© pasÃ³? Â¿CÃ³mo afectÃ³ el resultado? Eso abre el capÃ­tulo de forma prÃ¡ctica.',
      seÃ±ales: ['Identifican la emociÃ³n detrÃ¡s de las objeciones', 'Distinguen motivaciÃ³n de disciplina', 'Se comprometen con el termÃ³metro emocional'],
      errores: ['Convertirlo en terapia grupal', 'No trabajar el mapa emocional de objeciones con ejemplos reales del equipo', 'Dejar que la distinciÃ³n motivaciÃ³n/disciplina quede solo como teorÃ­a'],
      duracion: '35 min'
    },
    roleplay: {
      escenarios: ['Demo con cliente difÃ­cil emocionalmente', 'Distribuidor desmotivado despuÃ©s de una mala semana', 'ObjeciÃ³n "tengo que pensarlo"'],
      system: 'Sos un prospecto en Argentina que estÃ¡ siendo visitado por un distribuidor de Royal Prestige. TenÃ©s objeciones emocionales genuinas: dudas sobre si podÃ©s pagarlo, si lo necesitÃ¡s, si es el momento correcto. No sos hostil pero sÃ­ cauteloso. RespondÃ© de forma realista y con las emociones que corresponden a la situaciÃ³n.'
    }
  },
  {
    id:'cap4', num:'04',
    title:'GestiÃ³n del Tiempo y Disciplina Diaria',
    sub:'La libertad de horarios no es ausencia de estructura. Es estructura elegida.',
    time:'40 min',
    tags:['HÃ¡bitos','Productividad'],
    contenido: `
      <div class="manual-h3">Los 4 Bloques de la Semana Productiva</div>
      <div class="trainer-panel" style="margin-bottom:8px"><div class="exercise-label">ProspecciÃ³n â€” 25-30 llamadas/semana</div><div class="manual-text">El bloque mÃ¡s importante y mÃ¡s fÃ¡cil de postergar. Horario fijo cada dÃ­a: inviolable.</div></div>
      <div class="trainer-panel" style="margin-bottom:8px"><div class="exercise-label">Demos â€” 6-7 por semana</div><div class="manual-text">OrganizÃ¡ por zona geogrÃ¡fica y tu propia energÃ­a. 2-3 horas por demo completa.</div></div>
      <div class="trainer-panel" style="margin-bottom:8px"><div class="exercise-label">Bloque Administrativo</div><div class="manual-text">Todo en un bloque, no en pequeÃ±as interrupciones. La fragmentaciÃ³n consume el doble de tiempo.</div></div>
      <div class="trainer-panel" style="margin-bottom:8px"><div class="exercise-label">Desarrollo Personal â€” 30 min/dÃ­a</div><div class="manual-text">Leer, escuchar audiolibros, formaciÃ³n. El distribuidor que no se desarrolla se estanca.</div></div>
      <div class="distincion">
        <div class="distincion-grid">
          <div class="distincion-side r"><div class="distincion-label r">Queja</div>"No tengo tiempo." Hablar del problema sin hacer nada.</div>
          <div class="distincion-arrow">â†’</div>
          <div class="distincion-side g"><div class="distincion-label g">Compromiso</div>"Esta semana hago 5 llamadas antes de las 10, todos los dÃ­as." AcciÃ³n especÃ­fica y medible.</div>
        </div>
      </div>
      <div class="exercise-box">
        <div class="exercise-label">Ejercicio â€” DiseÃ±Ã¡ Tu Semana Ideal</div>
        <div class="manual-text">DibujÃ¡ los 7 dÃ­as con bloques de tiempo. Asignale ProspecciÃ³n, Demos, Admin o Desarrollo a cada bloque. Comparala con la semana que viviste la semana pasada.</div>
      </div>
    `,
    guia: {
      objetivo: 'Que cada distribuidor diseÃ±e un sistema de bloques de tiempo realista y se comprometa a respetarlo la semana siguiente.',
      intro: 'PreguntÃ¡: "Â¿CuÃ¡ntas horas de la semana pasada fueron realmente productivas â€” es decir, acciones que generan demos o ingresos?" La respuesta honesta abre el debate perfecto.',
      seÃ±ales: ['Hacen el ejercicio de la semana ideal en serio', 'Identifican sus bloques de baja productividad', 'Se comprometen con un horario especÃ­fico para llamadas'],
      errores: ['No hacer el ejercicio de la semana ideal en la sesiÃ³n', 'Hablar de productividad sin que cada uno identifique SU problema especÃ­fico', 'Cerrar sin un compromiso concreto y verificable'],
      duracion: '40 min'
    },
    roleplay: {
      escenarios: ['Distribuidor que dice que no tiene tiempo', 'Alguien que trabaja mucho pero produce poco', 'Distribuidor que posterga las llamadas de prospecciÃ³n'],
      system: 'Sos un distribuidor de Royal Prestige en Argentina. TenÃ©s problemas con la gestiÃ³n del tiempo: dejÃ¡s para despuÃ©s las llamadas de prospecciÃ³n, siempre encontrÃ¡s razones para no hacerlas, te quedÃ¡s haciendo tareas administrativas en lugar de salir al campo. RespondÃ© honestamente a lo que te plantee el capacitador.'
    }
  },
  {
    id:'cap5', num:'05',
    title:'El Lenguaje que Crea Realidad',
    sub:'CÃ³mo hablÃ¡s determina cÃ³mo pensÃ¡s. CÃ³mo pensÃ¡s determina lo que hacÃ©s.',
    time:'35 min',
    tags:['ComunicaciÃ³n','Lenguaje'],
    contenido: `
      <div class="manual-h3">Lenguaje Interno â€” Transformaciones Clave</div>
      <div class="trainer-panel">
        <div class="manual-text">
          "No soy bueno para vender" â†’ <strong>"Estoy desarrollando mis habilidades de consultorÃ­a."</strong><br><br>
          "Me van a decir que no" â†’ <strong>"Voy a descubrir quÃ© necesita esta familia."</strong><br><br>
          "Este mes estuvo flojo" â†’ <strong>"Tengo informaciÃ³n clara de quÃ© ajustar."</strong><br><br>
          "Estoy fallando" â†’ <strong>"Estoy calibrando."</strong>
        </div>
      </div>
      <div class="manual-h3">Palabras que Cierran Puertas</div>
      <div class="trainer-panel" style="border-color:rgba(192,57,43,.3)">
        <div class="manual-text">
          âŒ "Te molesto un momento" â†’ Posiciona tu llamada como una molestia.<br>
          âŒ "Â¿EstarÃ­as interesado en...?" â†’ Invita al "no" de entrada.<br>
          âŒ "Solo querÃ­a saber..." â†’ Poca importancia para vos mismo.
        </div>
      </div>
      <div class="manual-h3">Palabras que Abren Puertas</div>
      <div class="trainer-panel" style="border-color:rgba(39,174,96,.3)">
        <div class="manual-text">
          âœ“ "Te llamo porque sÃ© que valorÃ¡s la calidad en tu cocina..."<br>
          âœ“ "Cuando puedas verlo en persona, vas a entender por quÃ© las familias no quieren dejarlo ir."<br>
          âœ“ "Â¿QuÃ© es lo que mÃ¡s te importa cuando cocinÃ¡s para tu familia?"
        </div>
      </div>
      <div class="distincion">
        <div class="distincion-grid">
          <div class="distincion-side r"><div class="distincion-label r">Juicio</div>"Esta semana fui un desastre." InterpretaciÃ³n cargada de emociÃ³n.</div>
          <div class="distincion-arrow">â†’</div>
          <div class="distincion-side g"><div class="distincion-label g">Hecho</div>"Hice 3 demos, cerrÃ© 0. Â¿QuÃ© ajusto?" InformaciÃ³n accionable.</div>
        </div>
      </div>
      <div class="callout">"Las palabras que usÃ¡s para describir tu negocio son las palabras que tu equipo va a usar con sus prospectos."</div>
    `,
    guia: {
      objetivo: 'Que cada distribuidor identifique su lenguaje limitante y lo reemplace con lenguaje de alto rendimiento. Activar la consciencia del lenguaje.',
      intro: 'PedÃ­ al grupo que complete la frase: "Cuando no cierro una venta, me digo a mÃ­ mismo que..." AnotÃ¡ las respuestas. Esas son exactamente las frases que van a trabajar en el capÃ­tulo.',
      seÃ±ales: ['Corrigen su lenguaje en tiempo real', 'Identifican sus frases limitantes habituales', 'Practican las transformaciones de lenguaje'],
      errores: ['Solo explicar la teorÃ­a sin que practiquen las transformaciones', 'No trabajar el lenguaje con los prospectos (solo el interno)', 'No cerrar con el ejercicio de las 3 llamadas grabadas'],
      duracion: '35 min'
    },
    roleplay: {
      escenarios: ['Llamada de prospecciÃ³n desde cero', 'Manejo de objeciÃ³n de precio', 'Cierre de una demo'],
      system: 'Sos un potencial prospecto o cliente en Argentina. RecibÃ­s una llamada o visita de un distribuidor de Royal Prestige. RespondÃ© de forma natural: a veces con interÃ©s, a veces con dudas, a veces con objeciones. PrestÃ¡ atenciÃ³n al lenguaje que usa el distribuidor y respondÃ© en consecuencia.'
    }
  },
  {
    id:'cap6', num:'06',
    title:'Construyendo Equipos que Escalen',
    sub:'De vendedor a lÃ­der: el salto mÃ¡s difÃ­cil y mÃ¡s rentable de este negocio.',
    time:'50 min',
    tags:['Liderazgo','Equipo'],
    contenido: `
      <div class="manual-h3">El Salto de Vendedor a LÃ­der</div>
      <div class="manual-text">Pasar de distribuidor a lÃ­der requiere dejar de ser el mejor vendedor para convertirse en el <strong>mejor desarrollador de personas</strong>. Son habilidades completamente diferentes.</div>
      <div class="distincion">
        <div class="distincion-grid">
          <div class="distincion-side r"><div class="distincion-label r">Jefe</div>Da Ã³rdenes, controla, resuelve los problemas del equipo, es indispensable para que todo funcione.</div>
          <div class="distincion-arrow">â†’</div>
          <div class="distincion-side g"><div class="distincion-label g">LÃ­der</div>Crea contexto, desarrolla capacidades, hace preguntas que generan crecimiento.</div>
        </div>
      </div>
      <div class="manual-h3">La Realidad de la RetenciÃ³n</div>
      <div class="manual-text">EntrarÃ¡n muchos y quedarÃ¡n pocos. No es el modelo, es la naturaleza humana. La meta es desarrollar un <strong>nÃºcleo de lÃ­deres</strong> que sepan enseÃ±ar a otros a gestionar sus propios territorios.</div>
      <div class="trainer-panel" style="background:var(--gold4);border-color:var(--border)">
        <div class="exercise-label">DuplicaciÃ³n EstratÃ©gica</div>
        <div class="manual-text">El mejor liderazgo es aquel que entrena profundamente a pocos para lograr una duplicaciÃ³n real. Un territorio sÃ³lido se basa en la <strong>calidad</strong> de sus lÃ­deres, no solo en la cantidad.</div>
      </div>
      <div class="exercise-box">
        <div class="exercise-label">Ejercicio â€” El Perfil del Distribuidor Ideal</div>
        <div class="manual-text">EscribÃ­ el perfil de tu mejor distribuidor actual: Â¿QuÃ© caracterÃ­sticas tiene? Â¿QuÃ© actitudes? Â¿QuÃ© comportamientos? UsÃ¡ ese perfil para evaluar a los prospectos de tu prÃ³ximo reclutamiento.</div>
      </div>
    `,
    guia: {
      objetivo: 'Instalar la mentalidad de multiplicador. Que el lÃ­der entienda que su trabajo no es hacer la tarea por el equipo sino crear el ambiente para que el equipo la haga.',
      intro: 'PreguntÃ¡ a los lÃ­deres del grupo: "Â¿QuÃ© porcentaje de tu tiempo pasÃ¡s haciendo el trabajo DE tu equipo versus ayudÃ¡ndoles a desarrollar sus propias capacidades?" Esa respuesta revela exactamente dÃ³nde estÃ¡ el problema.',
      seÃ±ales: ['Hablan de desarrollar personas, no de "manejar" gente', 'Identifican a sus distribuidores con mayor potencial', 'DiseÃ±an un plan de desarrollo especÃ­fico por persona'],
      errores: ['Hablar de liderazgo de forma abstracta sin aplicarlo al equipo real de cada participante', 'No distinguir entre apoyar y resolver todo', 'Cerrar sin el ejercicio del perfil ideal escrito'],
      duracion: '50 min'
    },
    roleplay: {
      escenarios: ['Distribuidor que quiere abandonar', 'Miembro del equipo que no sigue el sistema', 'Alguien con potencial que no lo estÃ¡ usando'],
      system: 'Sos un distribuidor de Royal Prestige en Argentina que forma parte del equipo del capacitador. TenÃ©s un problema especÃ­fico segÃºn la situaciÃ³n: estÃ¡s pensando en dejar el negocio, no estÃ¡s siguiendo el sistema que te enseÃ±aron, o tenÃ©s potencial pero no te estÃ¡s esforzando lo suficiente. RespondÃ© de forma honesta y realista.'
    }
  },
  {
    id:'cap7', num:'07',
    title:'Rituales Diarios de los que Llegan Lejos',
    sub:'La disciplina es lo que queda cuando la motivaciÃ³n se va.',
    time:'30 min',
    tags:['Rituales','Disciplina'],
    contenido: `
      <div class="manual-h3">Ritual de la MaÃ±ana â€” 60 minutos</div>
      <div class="trainer-panel">
        <div class="manual-text">
          <strong>0-10 min:</strong> Sin telÃ©fono. Sin redes. Solo vos y el dÃ­a. Hidratarte.<br><br>
          <strong>10-25 min:</strong> Movimiento fÃ­sico. 15 min de caminata o stretching.<br><br>
          <strong>25-45 min:</strong> RevisiÃ³n de objetivos del dÃ­a. Tres prioridades especÃ­ficas.<br><br>
          <strong>45-60 min:</strong> Lectura o audio de desarrollo.
        </div>
      </div>
      <div class="manual-h3">Ritual Pre-Demo â€” 15 minutos</div>
      <div class="trainer-panel">
        <div class="manual-text">
          <strong>Repaso:</strong> Â¿QuÃ© sabÃ©s de la familia? Â¿Restricciones alimentarias?<br><br>
          <strong>Estado emocional:</strong> Â¿En quÃ© estado llegÃ¡s? Â¿NecesitÃ¡s dos minutos para dejar la tensiÃ³n afuera?<br><br>
          <strong>Objetivo:</strong> Â¿QuÃ© querÃ©s lograr hoy? Â¿Cerrar? Â¿Referidos?
        </div>
      </div>
      <div class="manual-h3">Ritual de Cierre del DÃ­a â€” 5 minutos</div>
      <div class="trainer-panel">
        <div class="manual-text">
          <strong>1.</strong> Â¿QuÃ© tres cosas salieron bien hoy?<br>
          <strong>2.</strong> Â¿QuÃ© aprendÃ­ hoy que harÃ© diferente maÃ±ana?<br>
          <strong>3.</strong> Â¿CuÃ¡l es la primera acciÃ³n de maÃ±ana?
        </div>
      </div>
      <div class="exercise-box">
        <div class="exercise-label">Ejercicio</div>
        <div class="manual-text">EscribÃ­ tu ritual matutino ideal, tu ritual pre-demo y tu ritual de cierre. Adaptalo a tu vida real. Comprometete a practicarlo 21 dÃ­as sin excepciÃ³n.</div>
      </div>
      <div class="callout">"Lo que no se mide, no se mejora. Lo que no se mejora, se deteriora."</div>
    `,
    guia: {
      objetivo: 'Que cada participante diseÃ±e su propio conjunto de rituales concretos y se comprometa con ellos por 21 dÃ­as.',
      intro: 'PedÃ­ que levanten la mano los que tienen una rutina matutina definida. DespuÃ©s preguntÃ¡ a los que levantaron la mano: "Â¿QuÃ© tan seguido la cumplÃ­s?" Eso establece la brecha entre saber y hacer.',
      seÃ±ales: ['DiseÃ±an rituales especÃ­ficos, no genÃ©ricos', 'Adaptan los rituales a su situaciÃ³n real', 'Se comprometen con la prÃ¡ctica de 21 dÃ­as'],
      errores: ['Presentar rituales como fÃ³rmulas rÃ­gidas', 'No dar tiempo para el ejercicio de diseÃ±o personal', 'Hablar solo del ritual matutino y omitir el pre-demo y el cierre'],
      duracion: '30 min'
    },
    roleplay: {
      escenarios: ['Distribuidor que no tiene rutina matutina', 'Alguien que llega mal predispuesto a las demos', 'Distribuidor que no reflexiona sobre su dÃ­a'],
      system: 'Sos un distribuidor de Royal Prestige en Argentina. No tenÃ©s rituales establecidos: arrancÃ¡s el dÃ­a mirando el telÃ©fono, llegÃ¡s a las demos sin preparaciÃ³n y al final del dÃ­a no revisÃ¡s quÃ© saliÃ³ bien o mal. RespondÃ© honestamente a las preguntas del capacitador sobre tu rutina actual.'
    }
  },
  {
    id:'cap8', num:'08',
    title:'Las Perlas de los 30 Libros Clave',
    sub:'La biblioteca del distribuidor que quiere jugar en otro nivel.',
    time:'45 min',
    tags:['Lecturas','Desarrollo'],
    contenido: `
      <div class="manual-h3">Los libros mÃ¡s aplicados al campo</div>
      <div class="trainer-panel" style="margin-bottom:8px">
        <div class="exercise-label">01 â€” HÃ¡bitos AtÃ³micos Â· James Clear</div>
        <div class="manual-text"><strong>Perla:</strong> Los resultados son el fruto acumulado de sistemas, no de objetivos. Una mejora del 1% por dÃ­a genera un resultado 37 veces mayor al cabo de un aÃ±o.</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:8px">
        <div class="exercise-label">02 â€” El Efecto Compuesto Â· Darren Hardy</div>
        <div class="manual-text"><strong>Perla:</strong> La disciplina de hoy es la libertad de maÃ±ana. La indisciplina de hoy es la esclavitud de maÃ±ana.</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:8px">
        <div class="exercise-label">03 â€” Responsabilidad Extrema Â· Jocko Willink</div>
        <div class="manual-text"><strong>Perla:</strong> No hay malos equipos, solo malos lÃ­deres. Todo lo que pasa en tu territorio es tu responsabilidad. Sin excusas.</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:8px">
        <div class="exercise-label">La PsicologÃ­a de las Ventas Â· Brian Tracy</div>
        <div class="manual-text"><strong>Perla:</strong> El 80% del Ã©xito en ventas es psicologÃ­a. El prospecto no compra el producto: compra la confianza en el vendedor.</div>
      </div>
      <div class="trainer-panel" style="margin-bottom:8px">
        <div class="exercise-label">Multipliers Â· Liz Wiseman</div>
        <div class="manual-text"><strong>Perla:</strong> El lÃ­der mÃ¡s inteligente no es el que tiene las mejores respuestas. Es el que hace las mejores preguntas.</div>
      </div>
      <div class="exercise-box">
        <div class="exercise-label">CÃ³mo leer para mÃ¡ximo impacto</div>
        <div class="manual-text"><strong>1.</strong> LeÃ© con un cuaderno al lado. AnotÃ¡ las 3 ideas que mÃ¡s te impactaron.<br><strong>2.</strong> ElegÃ­ UNA idea para aplicar esta semana. No 10: una.<br><strong>3.</strong> CompartÃ­ la idea con alguien de tu equipo. EnseÃ±ar consolida el doble.<br><strong>4.</strong> DespuÃ©s de 30 dÃ­as aplicando, pasÃ¡ al siguiente libro.</div>
      </div>
    `,
    guia: {
      objetivo: 'Instalar el hÃ¡bito de lectura aplicada. Que cada distribuidor elija el primer libro de su fase y defina la idea concreta a aplicar esta semana.',
      intro: 'PreguntÃ¡: "Â¿CuÃ¡ndo fue la Ãºltima vez que leyeron un libro de desarrollo y aplicaron algo concreto al campo?" La respuesta honesta establece el punto de partida.',
      seÃ±ales: ['Eligen un libro concreto para empezar', 'Identifican UNA idea aplicable, no diez', 'Se comprometen con la metodologÃ­a de 30 dÃ­as'],
      errores: ['Recomendar todos los libros a la vez', 'No diferenciar las fases de lectura segÃºn la etapa de cada distribuidor', 'Dejar el capÃ­tulo sin que cada uno elija su prÃ³xima lectura y su idea de la semana'],
      duracion: '45 min'
    },
    roleplay: {
      escenarios: ['Distribuidor que dice que no tiene tiempo para leer', 'Alguien que lee pero no aplica nada', 'Distribuidor al que no le gustan los libros'],
      system: 'Sos un distribuidor de Royal Prestige en Argentina. TenÃ©s alguno de estos problemas con los libros: no tenÃ©s tiempo para leer, leÃ©s pero no aplicÃ¡s nada, o directamente no te gustan los libros. RespondÃ© honestamente a lo que te plantee el capacitador sobre el desarrollo personal.'
    }
  },
  {
    id:'checklist', num:'âœ“',
    title:'Checklist de Mentalidad Semanal',
    sub:'Esta checklist no es para marcar casillas. Es para ser honesto con vos mismo.',
    time:'15 min',
    tags:['Seguimiento','Herramienta'],
    contenido: `
      <div class="manual-h3">Mentalidad y Actitud</div>
      <div class="manual-text">
        â–¡ PractiquÃ© mi ritual matutino al menos 5 de los 7 dÃ­as.<br>
        â–¡ Cuando recibÃ­ un rechazo, lo procesÃ© conscientemente antes de la siguiente llamada.<br>
        â–¡ RevisÃ© mi "por quÃ©" escrito al menos una vez esta semana.<br>
        â–¡ UsÃ© lenguaje que construye en vez de lenguaje que destruye.<br>
        â–¡ IdentifiquÃ© mi emociÃ³n dominante y la gestionÃ© activamente.
      </div>
      <div class="manual-h3">NÃºmeros de Negocio</div>
      <div class="manual-text">
        â–¡ Hice mis 25-30 llamadas de prospecciÃ³n semanales.<br>
        â–¡ RealicÃ© mis 6-7 demos (o las que corresponden a mi etapa).<br>
        â–¡ PedÃ­ referidos en al menos el 80% de mis demos.<br>
        â–¡ RealicÃ© seguimiento post-demo en las primeras 24 horas.<br>
        â–¡ Ante cada cancelaciÃ³n, reprogramÃ© antes de colgar.
      </div>
      <div class="manual-h3">Desarrollo Personal</div>
      <div class="manual-text">
        â–¡ DediquÃ© al menos 30 minutos diarios a lectura o formaciÃ³n.<br>
        â–¡ ApliquÃ© una idea concreta de lo que leÃ­ al campo real.<br>
        â–¡ CompartÃ­ una idea del manual con alguien de mi equipo.
      </div>
      <div class="manual-h3">Equipo (si aplica)</div>
      <div class="manual-text">
        â–¡ Hice al menos una conversaciÃ³n de desarrollo con cada miembro activo.<br>
        â–¡ ReconocÃ­ pÃºblicamente al menos un logro de alguien del equipo.<br>
        â–¡ ModifiquÃ© mi comportamiento en un Ã¡rea que quiero que mi equipo adopte.
      </div>
      <div class="trainer-panel" style="background:var(--gold4);border-color:var(--border)">
        <div class="exercise-label">CÃ³mo leer los resultados</div>
        <div class="manual-text">
          <strong>14-17 checks:</strong> Semana de alto rendimiento.<br>
          <strong>9-13 checks:</strong> Semana correcta. IdentificÃ¡ los 3 Ã­tems sin check mÃ¡s importantes.<br>
          <strong>Menos de 9:</strong> Semana de anÃ¡lisis honesto. Â¿QuÃ© pasÃ³?
        </div>
      </div>
    `,
    guia: {
      objetivo: 'Revisar la checklist en equipo. Que cada distribuidor se autoevalÃºe honestamente y defina los 3 Ã­tems a priorizar la semana siguiente.',
      intro: 'ArrancÃ¡ con: "Sin que lo compartan pÃºblicamente, Â¿cuÃ¡ntos puntos de la checklist completaron la semana pasada?" Luego preguntÃ¡ voluntariamente. La honestidad grupal abre el espacio para el trabajo real.',
      seÃ±ales: ['Se autoevalÃºan con honestidad, sin exagerar ni minimizar', 'Identifican patrones de incumplimiento recurrentes', 'Se comprometen con acciones especÃ­ficas para la semana siguiente'],
      errores: ['Hacer la revisiÃ³n de forma superficial', 'No cerrar con compromisos concretos y verificables', 'Convertirlo en un ejercicio de culpa en lugar de anÃ¡lisis constructivo'],
      duracion: '15 min'
    },
    roleplay: {
      escenarios: ['Distribuidor que miente en el checklist', 'Alguien que siempre tiene excusas para los Ã­tems sin completar', 'Distribuidor que se autoflagela por los resultados'],
      system: 'Sos un distribuidor de Royal Prestige en Argentina haciendo la revisiÃ³n semanal del checklist con tu lÃ­der. Completaste entre 5 y 8 puntos de 17. TenÃ©s excusas para algunos, reconocÃ©s honestamente otros, y en algunos simplemente no sabÃ©s cÃ³mo mejorar. RespondÃ© de forma realista.'
    }
  }
];

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// ESTADO
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
let mode = 'capacitador';
let currentChapter = null;
let currentDetailTab = 'contenido';
let members = [];
let notas = [];
let coachHistory = [];
let timerInterval = null;
let timerSeconds = 0;
let timerRunning = false;
let timerTotal = 0;
let sessions = 0;
let rpHistory = [];
let currentScenario = null;

function sv(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}}
function ld(k,d){try{const v=localStorage.getItem(k);return v!==null?JSON.parse(v):d}catch(e){return d}}

function loadData(){
  members = ld('cap_members_v1',[]);
  notas = ld('cap_notas_v1',[]);
  sessions = ld('cap_sessions_v1',0);
  mode = ld('cap_mode_v1','capacitador');
}

function saveData(){
  sv('cap_members_v1',members);
  sv('cap_notas_v1',notas);
  sv('cap_sessions_v1',sessions);
  sv('cap_mode_v1',mode);
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// MODO
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function setMode(m){
  mode = m;
  sv('cap_mode_v1',m);
  document.getElementById('btn-capacitador').classList.toggle('active', m==='capacitador');
  document.getElementById('btn-alumno').classList.toggle('active', m==='alumno');
  document.querySelectorAll('.capacitador-only').forEach(el=>{
    el.style.display = m==='capacitador' ? '' : 'none';
  });
  const info = document.getElementById('mode-info-box');
  if(m==='capacitador'){
    info.className='mode-info';
    info.innerHTML='<div class="mode-title">Modo Capacitador Activo</div><div class="mode-desc">TenÃ©s acceso a la guÃ­a del capacitador, preguntas de debate, roleplay con IA y seguimiento de equipo en cada capÃ­tulo.</div>';
  } else {
    info.className='mode-info alumno';
    info.innerHTML='<div class="mode-title alumno">Modo Alumno Activo</div><div class="mode-desc">AccedÃ©s al contenido del manual. El lÃ­der usa su propio dispositivo en Modo Capacitador para conducir la sesiÃ³n.</div>';
  }
  showToast(m==='capacitador'?'ðŸ‘‘ Modo Capacitador':'ðŸ“– Modo Alumno');
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// TABS NAV
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function goTab(id, el){
  document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
  document.querySelectorAll('.nt').forEach(b=>b.classList.remove('active'));
  document.getElementById('screen-'+id).classList.add('active');
  if(el) el.classList.add('active');
  if(id==='capitulos'){
    backToList();
    renderChapters();
  }
  if(id==='seguimiento') renderMembers();
  if(id==='notas') renderNotas();
  if(id==='inicio') renderInicio();
  if(id==='ajustes') renderAjustes();
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// INICIO
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderInicio(){
  const completedCount = CHAPTERS.filter(c=>ld('ch_done_'+c.id,false)).length;
  document.getElementById('stat-caps').textContent = completedCount;
  document.getElementById('stat-members').textContent = members.length;
  document.getElementById('stat-sessions').textContent = sessions;
  updateProgress();
  setMode(mode);
}

function updateProgress(){
  const done = CHAPTERS.filter(c=>ld('ch_done_'+c.id,false)).length;
  const pct = Math.round(done/CHAPTERS.length*100);
  document.getElementById('prog-fill').style.width = pct+'%';
  document.getElementById('prog-val').textContent = done+'/'+CHAPTERS.length;
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// CAPÃTULOS â€” LISTA
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderChapters(){
  const list = document.getElementById('chapter-list');
  list.innerHTML = '';
  CHAPTERS.forEach(ch=>{
    const done = ld('ch_done_'+ch.id,false);
    const div = document.createElement('div');
    div.className = 'ch-card'+(done?' completed':'');
    div.innerHTML = `
      <div class="ch-card-top">
        <div class="ch-num">${ch.num}</div>
        <div class="ch-info">
          <div class="ch-title">${ch.title}</div>
          <div class="ch-sub">${ch.sub}</div>
          <div class="ch-meta">
            ${ch.tags.map(t=>`<span class="ch-tag">${t}</span>`).join('')}
            <span class="ch-tag">â± ${ch.time}</span>
            ${done?'<span class="ch-tag" style="background:rgba(39,174,96,.1);color:var(--green);border-color:rgba(39,174,96,.3)">âœ“ Completado</span>':''}
          </div>
        </div>
        <div class="ch-arrow">â€º</div>
      </div>`;
    div.onclick = ()=>openChapter(ch);
    list.appendChild(div);
  });
}

function openChapter(ch){
  currentChapter = ch;
  document.getElementById('chapter-list-view').style.display='none';
  document.getElementById('chapter-detail-view').style.display='block';
  document.getElementById('detail-title').textContent = 'Cap. '+ch.num+' â€” '+ch.title;
  document.getElementById('detail-sub').textContent = ch.sub;

  // Tabs segÃºn modo
  const tabs = document.querySelectorAll('.ch-tab');
  tabs.forEach(t=>{
    if(t.classList.contains('capacitador-only')){
      t.style.display = mode==='capacitador'?'':'none';
    }
  });

  switchDetailTab('contenido', document.querySelector('.ch-tab'));
  sessions++;
  sv('cap_sessions_v1',sessions);
  renderInicio();
}

function backToList(){
  document.getElementById('chapter-list-view').style.display='block';
  document.getElementById('chapter-detail-view').style.display='none';
  currentChapter = null;
  renderChapters();
  updateProgress();
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// DETALLE TABS
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function switchDetailTab(tab, el){
  currentDetailTab = tab;
  document.querySelectorAll('.ch-tab').forEach(b=>b.classList.remove('active'));
  if(el) el.classList.add('active');
  else { const tabs=document.querySelectorAll('.ch-tab'); if(tabs[0])tabs[0].classList.add('active'); }

  ['contenido','guia','debate','roleplay'].forEach(t=>{
    const panel = document.getElementById('detail-'+t);
    if(panel) panel.style.display = t===tab?'block':'none';
  });

  if(tab==='contenido') renderContenido();
  if(tab==='guia') renderGuia();
  if(tab==='debate') renderDebate();
  if(tab==='roleplay') renderRoleplay();
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// CONTENIDO
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderContenido(){
  if(!currentChapter) return;
  const panel = document.getElementById('detail-contenido');
  const done = ld('ch_done_'+currentChapter.id,false);
  panel.innerHTML = `
    <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:14px">
      <div style="font-size:10px;font-family:'IBM Plex Mono',monospace;letter-spacing:2px;color:var(--text3);text-transform:uppercase">DuraciÃ³n sugerida: ${currentChapter.time}</div>
      <button onclick="toggleDone('${currentChapter.id}')" style="background:${done?'rgba(39,174,96,.12)':'var(--gold4)'};border:1px solid ${done?'rgba(39,174,96,.3)':'var(--border)'};border-radius:20px;padding:5px 12px;font-size:11px;font-family:'IBM Plex Mono',monospace;color:${done?'var(--green)':'var(--gold)'};cursor:pointer">
        ${done?'âœ“ Completado':'Marcar completado'}
      </button>
    </div>
    ${currentChapter.contenido}
  `;
}

function toggleDone(id){
  const val = !ld('ch_done_'+id,false);
  sv('ch_done_'+id,val);
  renderContenido();
  updateProgress();
  renderChapters();
  showToast(val?'âœ… CapÃ­tulo completado':'â†© Marcado como pendiente');
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// GUÃA CAPACITADOR
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderGuia(){
  if(!currentChapter) return;
  const g = currentChapter.guia;
  const panel = document.getElementById('detail-guia');

  const timerHtml = `
    <div class="timer-widget">
      <div class="timer-display" id="timer-display">00:00</div>
      <div class="timer-controls">
        <div style="font-size:10px;font-family:'IBM Plex Mono',monospace;color:var(--text3);letter-spacing:1px;margin-bottom:4px">TEMPORIZADOR</div>
        <div class="timer-presets">
          <button class="timer-preset" onclick="setTimer(5)">5 min</button>
          <button class="timer-preset" onclick="setTimer(10)">10 min</button>
          <button class="timer-preset" onclick="setTimer(15)">15 min</button>
          <button class="timer-preset" onclick="setTimer(20)">20 min</button>
          <button class="timer-preset active" onclick="setTimer(${parseInt(g.duracion)})">Cap (${g.duracion})</button>
        </div>
        <div class="timer-btns">
          <button class="tbtn tbtn-start" id="timer-start-btn" onclick="toggleTimer()">â–¶ Iniciar</button>
          <button class="tbtn tbtn-reset" onclick="resetTimer()">â†º Reset</button>
        </div>
      </div>
    </div>`;

  panel.innerHTML = timerHtml + `
    <div class="trainer-panel">
      <div class="trainer-section">
        <div class="trainer-label">ðŸŽ¯ Objetivo del capÃ­tulo</div>
        <div class="trainer-text">${g.objetivo}</div>
      </div>
      <div class="trainer-section">
        <div class="trainer-label">ðŸŽ¤ CÃ³mo introducirlo</div>
        <div class="trainer-text">${g.intro}</div>
      </div>
      <div class="trainer-section">
        <div class="trainer-label">âœ… SeÃ±ales de que el grupo entendiÃ³</div>
        <div class="trainer-text"><ul>${g.seÃ±ales.map(s=>`<li>${s}</li>`).join('')}</ul></div>
      </div>
      <div class="trainer-section">
        <div class="trainer-label">âš ï¸ Errores comunes al capacitar este tema</div>
        <div class="trainer-text"><ul>${g.errores.map(e=>`<li>${e}</li>`).join('')}</ul></div>
      </div>
    </div>
  `;
  setTimer(parseInt(g.duracion));
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// TIMER
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function setTimer(mins){
  resetTimer();
  timerTotal = mins*60;
  timerSeconds = mins*60;
  updateTimerDisplay();
  document.querySelectorAll('.timer-preset').forEach(b=>{
    b.classList.toggle('active', b.textContent.includes(mins+' min')||b.textContent.includes('Cap'));
  });
}

function toggleTimer(){
  if(timerRunning){ pauseTimer(); }
  else { startTimer(); }
}

function startTimer(){
  if(timerSeconds<=0) return;
  timerRunning=true;
  document.getElementById('timer-start-btn').textContent='â¸ Pausar';
  document.getElementById('timer-start-btn').className='tbtn tbtn-pause';
  timerInterval = setInterval(()=>{
    timerSeconds--;
    updateTimerDisplay();
    if(timerSeconds<=0){
      clearInterval(timerInterval);
      timerRunning=false;
      document.getElementById('timer-display').className='timer-display ended';
      document.getElementById('timer-start-btn').textContent='â–¶ Iniciar';
      document.getElementById('timer-start-btn').className='tbtn tbtn-start';
      showToast('â° Â¡Tiempo terminado!');
    }
  },1000);
}

function pauseTimer(){
  clearInterval(timerInterval);
  timerRunning=false;
  document.getElementById('timer-start-btn').textContent='â–¶ Continuar';
  document.getElementById('timer-start-btn').className='tbtn tbtn-start';
}

function resetTimer(){
  clearInterval(timerInterval);
  timerRunning=false;
  timerSeconds=timerTotal;
  updateTimerDisplay();
  const disp = document.getElementById('timer-display');
  if(disp) disp.className='timer-display';
  const btn = document.getElementById('timer-start-btn');
  if(btn){btn.textContent='â–¶ Iniciar';btn.className='tbtn tbtn-start';}
}

function updateTimerDisplay(){
  const disp = document.getElementById('timer-display');
  if(!disp) return;
  const m = Math.floor(timerSeconds/60);
  const s = timerSeconds%60;
  disp.textContent = String(m).padStart(2,'0')+':'+String(s).padStart(2,'0');
  const pct = timerTotal>0?timerSeconds/timerTotal:1;
  if(timerRunning){
    disp.className = 'timer-display '+(pct>0.3?'running':'warning');
  }
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// DEBATE
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderDebate(){
  if(!currentChapter) return;
  const panel = document.getElementById('detail-debate');
  panel.innerHTML = `
    <div style="margin-bottom:14px;display:flex;align-items:center;justify-content:space-between">
      <div style="font-size:11px;font-family:'IBM Plex Mono',monospace;color:var(--text3);letter-spacing:1px;text-transform:uppercase">Preguntas de Debate</div>
      <button onclick="generateDebate()" style="background:var(--gold4);border:1px solid var(--border);border-radius:20px;padding:5px 12px;font-size:10px;font-family:'IBM Plex Mono',monospace;color:var(--gold);cursor:pointer;letter-spacing:1px">âœ¦ Generar con IA</button>
    </div>
    <div id="debate-questions-container">
      <div class="rp-loading">TocÃ¡ "Generar con IA" para crear preguntas personalizadas, o usÃ¡ las preguntas base:</div>
      ${getDefaultDebateQuestions()}
    </div>
  `;
}

function getDefaultDebateQuestions(){
  if(!currentChapter) return '';
  const defaults = {
    cap0: ['Â¿QuÃ© diferencia a alguien que construye un territorio sÃ³lido de alguien que trabaja muchos aÃ±os pero nunca despega?','Â¿En quÃ© momento de tu negocio sentiste que realmente pasaste de "hacer ventas" a "construir un negocio"?','Â¿QuÃ© caracterÃ­sticas tiene el distribuidor ideal que querÃ©s incorporar a tu equipo?'],
    cap2: ['Â¿CuÃ¡l fue el rechazo mÃ¡s difÃ­cil que tuviste y cÃ³mo lo procesaste?','Â¿QuÃ© diferencia hay entre cÃ³mo manejabas los rechazos cuando empezaste y cÃ³mo los manejÃ¡s ahora?','Â¿CuÃ¡ndo una cancelaciÃ³n es informaciÃ³n Ãºtil y cuÃ¡ndo es simplemente mala suerte?'],
    cap3: ['Â¿CÃ³mo reconocÃ©s cuando tu estado emocional estÃ¡ afectando negativamente tu demo?','Â¿QuÃ© hacÃ©s para llegar a una demo en el estado Ã³ptimo cuando el dÃ­a estuvo complicado?','Â¿En quÃ© objeciÃ³n de clientes notÃ¡s la mayor carga emocional y cÃ³mo la trabajÃ¡s?'],
    cap4: ['Â¿CuÃ¡l es el bloque de tiempo que mÃ¡s frecuentemente postponÃ©s y por quÃ©?','Â¿CÃ³mo distinguÃ­s entre estar ocupado y ser productivo en tu semana?','Si tuvieras que elegir una sola prÃ¡ctica de gestiÃ³n del tiempo que cambiarÃ­a todo, Â¿cuÃ¡l serÃ­a?'],
    cap5: ['Â¿CuÃ¡l es la frase limitante que mÃ¡s te repetÃ­s cuando las cosas no salen?','Â¿CÃ³mo cambiÃ³ el resultado de una demo cuando conscientemente cambiaste el lenguaje que usaste?','Â¿QuÃ© palabras de tu equipo notÃ¡s que delatan creencias limitantes?'],
    cap6: ['Â¿CuÃ¡ndo fue la Ãºltima vez que ayudaste a alguien de tu equipo a crecer en lugar de resolver su problema?','Â¿QuÃ© hace que un distribuidor se quede en el equipo a largo plazo?','Â¿En quÃ© te parecÃ©s mÃ¡s a un jefe y en quÃ© a un lÃ­der?'],
    cap7: ['Â¿CuÃ¡l de los tres rituales (maÃ±ana, pre-demo, cierre) te resulta mÃ¡s difÃ­cil mantener y por quÃ©?','Â¿CÃ³mo notÃ¡s la diferencia en tu rendimiento cuando cumplÃ­s vs. cuando no cumplÃ­s tu ritual matutino?','Â¿QuÃ© ajuste a un ritual existente harÃ­a la mayor diferencia esta semana?'],
    cap8: ['Â¿CuÃ¡l fue el libro que mÃ¡s impactÃ³ en tu forma de trabajar el campo y por quÃ©?','Â¿CuÃ¡l es la diferencia entre leer y aplicar? Â¿CuÃ¡ndo fuiste mÃ¡s allÃ¡ de leer?','Â¿QuÃ© idea de un libro aplicaste esta semana que te dio un resultado concreto?'],
    checklist: ['Â¿Con quÃ© frecuencia hacÃ©s el checklist honestamente vs. solo para cumplir?','Â¿CuÃ¡l es el Ã­tem que mÃ¡s frecuentemente dejÃ¡s sin completar y por quÃ©?','Â¿CÃ³mo cambia tu semana cuando completÃ¡s 14+ puntos versus cuando completÃ¡s menos de 9?']
  };
  const qs = defaults[currentChapter.id] || ['Â¿QuÃ© fue lo mÃ¡s relevante de este capÃ­tulo para tu situaciÃ³n actual?','Â¿QuÃ© vas a cambiar en tu prÃ¡ctica esta semana a partir de este contenido?','Â¿QuÃ© parte de este capÃ­tulo te costÃ³ mÃ¡s aceptar y por quÃ©?'];
  return qs.map((q,i)=>`
    <div class="debate-q">
      <div class="debate-q-num">PREGUNTA 0${i+1}</div>
      ${q}
    </div>
  `).join('');
}

async function generateDebate(){
  if(!currentChapter) return;
  const workerUrl = ld('cap_config_v1',{}).workerUrl||'';
  if(!workerUrl){showToast('âš ï¸ ConfigurÃ¡ el Worker en Ajustes');return;}
  const container = document.getElementById('debate-questions-container');
  container.innerHTML = '<div class="rp-loading">ðŸ‘‘ Generando preguntas personalizadas...</div>';
  try{
    const res = await fetch(workerUrl,{
      method:'POST',headers:{'Content-Type':'application/json'},
      body:JSON.stringify({
        model:'claude-haiku-4-5-20251001',max_tokens:800,
        system:'Sos un experto en capacitaciÃ³n de equipos de ventas directas para Royal Prestige en Argentina. GenerÃ¡s preguntas de debate profundas y prÃ¡cticas.',
        messages:[{role:'user',content:`GenerÃ¡ 4 preguntas de debate para una sesiÃ³n de capacitaciÃ³n del capÃ­tulo "${currentChapter.title}" del Manual de Mentalidad Elite del Logos Group 29239. Las preguntas deben: 1) ser aplicables directamente al campo real en Argentina (Goya, Corrientes), 2) generar reflexiÃ³n genuina y no respuestas superficiales, 3) estar conectadas con situaciones concretas del negocio de Royal Prestige. Formato: solo las 4 preguntas numeradas, sin introducciÃ³n ni explicaciÃ³n.`}]
      })
    });
    const data = await res.json();
    const text = data.content?.[0]?.text||data.response||'';
    if(!text){container.innerHTML=getDefaultDebateQuestions();return;}
    const lines = text.split('\n').filter(l=>l.trim());
    container.innerHTML = lines.map((l,i)=>`<div class="debate-q"><div class="debate-q-num">PREGUNTA 0${i+1}</div>${l.replace(/^\d+[\.\)]\s*/,'')}</div>`).join('');
  } catch(e){
    container.innerHTML = getDefaultDebateQuestions();
    showToast('âš ï¸ Usando preguntas base');
  }
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// ROLEPLAY
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderRoleplay(){
  if(!currentChapter) return;
  const panel = document.getElementById('detail-roleplay');
  rpHistory = [];
  const rp = currentChapter.roleplay;
  panel.innerHTML = `
    <div style="margin-bottom:10px;font-size:11px;font-family:'IBM Plex Mono',monospace;color:var(--text3);letter-spacing:1px;text-transform:uppercase">ElegÃ­ el escenario</div>
    <div class="rp-scenarios">
      ${rp.escenarios.map((e,i)=>`<button class="rp-scenario" onclick="selectScenario(${i},this)">${e}</button>`).join('')}
    </div>
    <div class="roleplay-chat" id="rp-chat">
      <div class="rp-loading">SeleccionÃ¡ un escenario para comenzar el roleplay. La IA harÃ¡ de distribuidor o prospecto. Vos practicÃ¡s como capacitador.</div>
    </div>
    <div class="rp-input-row">
      <textarea class="rp-input" id="rp-input" placeholder="Tu respuesta como capacitador..." onkeydown="if(event.key==='Enter'&&!event.shiftKey){event.preventDefault();sendRoleplay()}"></textarea>
      <button class="rp-send" onclick="sendRoleplay()">â†‘</button>
    </div>
  `;
}

function selectScenario(idx, el){
  if(!currentChapter) return;
  document.querySelectorAll('.rp-scenario').forEach(b=>b.classList.remove('active'));
  el.classList.add('active');
  currentScenario = idx;
  rpHistory = [];
  const rp = currentChapter.roleplay;
  const chat = document.getElementById('rp-chat');
  const scenarioName = rp.escenarios[idx];
  chat.innerHTML = `<div class="rp-msg ai"><div class="rp-who ai">ðŸŽ­ Escenario: ${scenarioName}</div><div class="rp-bubble ai">Voy a hacer de: <strong>${scenarioName}</strong>. EmpezÃ¡ la conversaciÃ³n cuando quieras.</div></div>`;
  rpHistory = [];
}

async function sendRoleplay(){
  const input = document.getElementById('rp-input');
  const msg = (input.value||'').trim();
  if(!msg||currentScenario===null){
    if(currentScenario===null) showToast('âš ï¸ ElegÃ­ un escenario primero');
    return;
  }
  const workerUrl = ld('cap_config_v1',{}).workerUrl||'';
  if(!workerUrl){showToast('âš ï¸ ConfigurÃ¡ el Worker en Ajustes');return;}
  input.value='';
  const chat = document.getElementById('rp-chat');
  chat.innerHTML += `<div class="rp-msg user"><div class="rp-who user">Vos (Capacitador)</div><div class="rp-bubble user">${msg}</div></div>`;
  chat.innerHTML += `<div class="rp-loading" id="rp-load">Respondiendo...</div>`;
  chat.scrollTop = chat.scrollHeight;
  rpHistory.push({role:'user',content:msg});
  try{
    const res = await fetch(workerUrl,{
      method:'POST',headers:{'Content-Type':'application/json'},
      body:JSON.stringify({
        model:'claude-haiku-4-5-20251001',max_tokens:400,
        system: currentChapter.roleplay.system + ` Escenario actual: ${currentChapter.roleplay.escenarios[currentScenario]}. RespondÃ© en no mÃ¡s de 3 oraciones cortas y directas.`,
        messages: rpHistory
      })
    });
    const data = await res.json();
    const text = data.content?.[0]?.text||data.response||'Sin respuesta.';
    rpHistory.push({role:'assistant',content:text});
    const load = document.getElementById('rp-load');
    if(load) load.remove();
    chat.innerHTML += `<div class="rp-msg ai"><div class="rp-who ai">ðŸŽ­ ${currentChapter.roleplay.escenarios[currentScenario]}</div><div class="rp-bubble ai">${text}</div></div>`;
    chat.scrollTop = chat.scrollHeight;
  } catch(e){
    const load = document.getElementById('rp-load');
    if(load) load.textContent='âš ï¸ Error. ConfigurÃ¡ el Worker.';
  }
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// EQUIPO / SEGUIMIENTO
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function addMember(){
  const input = document.getElementById('new-member-name');
  const name = (input.value||'').trim();
  if(!name) return;
  members.push({name, progress:{}, notes:''});
  saveData();
  input.value='';
  renderMembers();
  updateNotaMemberSelect();
  showToast('ðŸ‘¤ '+name+' agregado');
  renderInicio();
}

function renderMembers(){
  const list = document.getElementById('members-list');
  if(!members.length){
    list.innerHTML='<div style="padding:20px 14px;text-align:center;color:var(--text3);font-size:14px;font-style:italic">AgregÃ¡ los distribuidores de tu equipo para hacer seguimiento de su progreso.</div>';
    return;
  }
  list.innerHTML='';
  members.forEach((m,i)=>{
    const doneCount = Object.values(m.progress||{}).filter(Boolean).length;
    const div = document.createElement('div');
    div.className='member-card';
    div.innerHTML=`
      <div class="member-header" onclick="toggleMember(${i})">
        <div class="member-avatar">${m.name[0].toUpperCase()}</div>
        <div class="member-name">${m.name}</div>
        <div class="member-prog">${doneCount}/${CHAPTERS.length} caps</div>
        <button class="del-member" onclick="event.stopPropagation();deleteMember(${i})">âœ•</button>
      </div>
      <div class="member-chapters" id="member-ch-${i}">
        <div style="font-size:10px;font-family:'IBM Plex Mono',monospace;color:var(--text3);letter-spacing:1px;text-transform:uppercase;margin-bottom:8px">CapÃ­tulos completados</div>
        <div class="ch-progress-grid">
          ${CHAPTERS.map((ch,ci)=>`
            <div class="ch-prog-item ${(m.progress||{})[ch.id]?'done':''}" onclick="toggleMemberChapter(${i},'${ch.id}')">
              <div class="cpn">${ch.num}</div>
              <div class="cpc">${(m.progress||{})[ch.id]?'âœ“':''}</div>
            </div>
          `).join('')}
        </div>
        <div style="font-size:10px;font-family:'IBM Plex Mono',monospace;color:var(--text3);letter-spacing:1px;text-transform:uppercase;margin:8px 0 4px">Notas</div>
        <textarea class="member-notes-input" placeholder="Observaciones sobre ${m.name}..." onchange="saveMemberNote(${i},this.value)">${m.notes||''}</textarea>
      </div>
    `;
    list.appendChild(div);
  });
}

function toggleMember(i){
  const el = document.getElementById('member-ch-'+i);
  el.classList.toggle('open');
}

function toggleMemberChapter(memberIdx, chId){
  if(!members[memberIdx].progress) members[memberIdx].progress={};
  members[memberIdx].progress[chId] = !members[memberIdx].progress[chId];
  saveData();
  renderMembers();
}

function saveMemberNote(i,val){
  members[i].notes=val;
  saveData();
}

function deleteMember(i){
  if(!confirm('Â¿Eliminar a '+members[i].name+'?')) return;
  members.splice(i,1);
  saveData();
  renderMembers();
  updateNotaMemberSelect();
  renderInicio();
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// NOTAS
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function updateNotaMemberSelect(){
  const sel = document.getElementById('nota-member-select');
  if(!sel) return;
  sel.innerHTML='<option value="">Miembro del equipo...</option>'+members.map(m=>`<option value="${m.name}">${m.name}</option>`).join('');
  const capSel = document.getElementById('nota-cap-select');
  if(capSel) capSel.innerHTML='<option value="">CapÃ­tulo...</option>'+CHAPTERS.map(ch=>`<option value="${ch.id}">Cap. ${ch.num} â€” ${ch.title}</option>`).join('');
}

function saveNota(){
  const text = (document.getElementById('nota-text').value||'').trim();
  if(!text){showToast('âš ï¸ EscribÃ­ la observaciÃ³n');return;}
  const member = document.getElementById('nota-member-select').value||'General';
  const capId = document.getElementById('nota-cap-select').value||'';
  const cap = capId ? CHAPTERS.find(c=>c.id===capId) : null;
  notas.unshift({
    text, member,
    capTitle: cap?'Cap. '+cap.num+' â€” '+cap.title:'General',
    date: new Date().toLocaleDateString('es-AR')
  });
  sv('cap_notas_v1',notas);
  document.getElementById('nota-text').value='';
  renderNotas();
  showToast('ðŸ“ Nota guardada');
}

function renderNotas(){
  updateNotaMemberSelect();
  const list = document.getElementById('notas-list');
  if(!notas.length){
    list.innerHTML='<div style="text-align:center;color:var(--text3);font-size:14px;font-style:italic;padding:20px">Las notas de tus sesiones van a aparecer acÃ¡.</div>';
    return;
  }
  list.innerHTML = notas.map((n,i)=>`
    <div class="nota-card">
      <div class="nota-card-header">
        <div>
          <div style="font-size:12px;color:var(--text);font-weight:600">${n.member}</div>
          <div class="nota-ch">${n.capTitle}</div>
        </div>
        <div style="display:flex;align-items:center;gap:8px">
          <div class="nota-date">${n.date}</div>
          <button onclick="deleteNota(${i})" style="background:none;border:none;color:var(--text3);cursor:pointer;font-size:14px">âœ•</button>
        </div>
      </div>
      <div class="nota-text">${n.text}</div>
    </div>
  `).join('');
}

function deleteNota(i){
  notas.splice(i,1);
  sv('cap_notas_v1',notas);
  renderNotas();
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// COACH IA
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
async function sendCoach(){
  const input = document.getElementById('coach-input');
  const msg = (input.value||'').trim();
  if(!msg) return;
  const workerUrl = ld('cap_config_v1',{}).workerUrl||'';
  if(!workerUrl){showToast('âš ï¸ ConfigurÃ¡ el Worker en Ajustes');return;}
  input.value='';
  const msgs = document.getElementById('coach-msgs');
  msgs.innerHTML += `<div class="coach-msg user"><div class="coach-who u">Vos</div><div class="coach-bubble user">${msg}</div></div>`;
  msgs.innerHTML += `<div class="coach-loading" id="coach-load">ðŸ‘‘ Coach pensando...</div>`;
  msgs.scrollTop = msgs.scrollHeight;
  coachHistory.push({role:'user',content:msg});
  if(coachHistory.length>10) coachHistory=coachHistory.slice(-10);
  try{
    const res = await fetch(workerUrl,{
      method:'POST',headers:{'Content-Type':'application/json'},
      body:JSON.stringify({
        model:'claude-haiku-4-5-20251001',max_tokens:600,
        system:'Sos el Coach IA especializado en capacitaciÃ³n del Logos Group 29239 de Royal Prestige en Goya, Corrientes, Argentina. Tu rol es ayudar a los lÃ­deres capacitadores a preparar y conducir sesiones de formaciÃ³n con su equipo, basÃ¡ndote en el Manual de Mentalidad de Alto Rendimiento. Das consejos prÃ¡cticos, directos y aplicables al campo real argentino. UsÃ¡s lenguaje argentino natural. Sos conciso: respondÃ©s en no mÃ¡s de 4 pÃ¡rrafos.',
        messages: coachHistory
      })
    });
    const data = await res.json();
    const text = data.content?.[0]?.text||data.response||'Sin respuesta.';
    coachHistory.push({role:'assistant',content:text});
    const load = document.getElementById('coach-load');
    if(load) load.remove();
    msgs.innerHTML += `<div class="coach-msg ai"><div class="coach-who">ðŸ‘‘ Coach Â· Logos Group 29239</div><div class="coach-bubble ai">${text.replace(/\*\*(.*?)\*\*/g,'<strong>$1</strong>').replace(/\n/g,'<br>')}</div></div>`;
    msgs.scrollTop = msgs.scrollHeight;
  } catch(e){
    const load = document.getElementById('coach-load');
    if(load) load.textContent='âš ï¸ Error â€” configurÃ¡ el Worker en Ajustes';
  }
}

function askCoach(msg){
  document.getElementById('coach-input').value=msg;
  goTab('coach', document.querySelectorAll('.nt')[4]);
  sendCoach();
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// AJUSTES
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
function renderAjustes(){
  const cfg = ld('cap_config_v1',{});
  const wInput = document.getElementById('cfg-worker');
  const nInput = document.getElementById('cfg-name');
  if(wInput) wInput.value = cfg.workerUrl||'';
  if(nInput) nInput.value = cfg.name||'';
}

function saveConfig(){
  const workerUrl = (document.getElementById('cfg-worker').value||'').trim();
  const name = (document.getElementById('cfg-name').value||'').trim();
  sv('cap_config_v1',{workerUrl,name});
  showToast('âœ… ConfiguraciÃ³n guardada');
}

function exportData(){
  const data={members,notas,sessions,mode,config:ld('cap_config_v1',{})};
  const a=document.createElement('a');
  a.href='data:application/json;charset=utf-8,'+encodeURIComponent(JSON.stringify(data,null,2));
  a.download='capacitador_backup_'+new Date().toISOString().slice(0,10)+'.json';
  document.body.appendChild(a);a.click();document.body.removeChild(a);
  showToast('âœ… Backup exportado');
}

function importData(){
  const input=document.createElement('input');input.type='file';input.accept='.json';
  input.onchange=e=>{
    const file=e.target.files[0];if(!file)return;
    const r=new FileReader();
    r.onload=ev=>{
      try{
        const d=JSON.parse(ev.target.result);
        if(d.members) members=d.members;
        if(d.notas) notas=d.notas;
        if(d.sessions) sessions=d.sessions;
        if(d.config) sv('cap_config_v1',d.config);
        saveData();
        showToast('âœ… Datos restaurados');
        renderInicio();
      }catch(err){showToast('âš ï¸ Archivo invÃ¡lido');}
    };
    r.readAsText(file);
  };
  document.body.appendChild(input);input.click();document.body.removeChild(input);
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// TOAST
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
let toastTimeout;
function showToast(msg){
  const t=document.getElementById('toast');
  t.textContent=msg;t.classList.add('show');
  clearTimeout(toastTimeout);
  toastTimeout=setTimeout(()=>t.classList.remove('show'),2500);
}

// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
// INIT
// â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•
window.addEventListener('load',()=>{
  loadData();
  setMode(mode);
  renderInicio();
  renderChapters();
  updateNotaMemberSelect();
});
</script>
</body>
</html>
