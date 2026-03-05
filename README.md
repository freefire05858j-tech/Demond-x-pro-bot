# Demond-x-pro-bot
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, interactive-widget=resizes-content">
<title>ZIHAD SIR. ZX TRADER</title>
<style>
/* ================= BASE (FIXED FOR CHROME) ================= */
* { margin: 0; padding: 0; box-sizing: border-box; touch-action: pan-x pan-y; }

:root { 
  --vh: 100dvh; 
}

html, body {
  width: 100%;
  height: 100dvh; 
  background: #000;
  overflow: hidden; 
  font-family: Arial, sans-serif;
  position: relative; 
  top: 0;
  left: 0;
  touch-action: none; 
}

/*============ iframe (FIXED) ===============*/
iframe {
  width: 100%;
  height: 100dvh; 
  border: none;
  display: none;
  position: absolute;
  top: 0;
  left: 0;
}

/*===== VIP PREMIUM RED RGB LOGIN (FIXED) ====*/
.login {
    position: absolute; 
    inset: 0;
    height: 100dvh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: radial-gradient(circle at center, #1a0a2e 0%, #050505 100%);
    background-size: 200% 200%;
    animation: luxuryBg 15s ease infinite;
    z-index: 999999;
    font-family: 'Montserrat', sans-serif;
    transition: all 0.3s ease;
    overflow-y: auto;
}

/* ৩. ইনপুটে ক্লিক করলে অটো-জুম আটকানোর জন্য ১৬ পিক্সেল ফন্ট */
.login-box input {
    font-size: 16px !important;
}

.login-box {
    position: relative;
    width: 320px; /* সামান্য বড় করা হয়েছে প্রো লুকের জন্য */
    padding: 53px 30px;
    background: rgba(0, 0, 0, 0.8); 
    backdrop-filter: blur(25px);
    border-radius: 60px;
    text-align: center;
    border: 3px solid transparent; 
    animation: borderGlowFlow 2s linear infinite;
}

/* ================= LOGO & TITLE SECTION (PREMIUM SYNC) ================= */

/* লোগো সেকশন - লোগো বড় এবং পজিশন উপরে সেট করা */
.logo-section {
    position: relative;
    width: 160px; /* কন্টেইনার সামান্য বড় করা হয়েছে */
    height: 120px; /* হাইট অ্যাডজাস্ট করা হয়েছে */
    margin: -25px auto 10px; /* নেগেটিভ মার্জিন দিয়ে লোগোকে উপরে তোলা হয়েছে */
    display: flex;
    align-items: center;
    justify-content: center;
    perspective: 1000px;
}

.user-logo {
    width: 95px; /* লোগো ইমেজ বড় করা হয়েছে */
    height: 95px;
    border-radius: 50%;
    border: 3px solid #00fff2; /* বর্ডার মোটা এবং ক্লিয়ার */
    box-shadow: 0 0 20px rgba(0, 255, 242, 0.6), 
                inset 0 0 10px rgba(0, 255, 242, 0.3);
    z-index: 5;
    object-fit: cover;
    background: #000;
}

.logo-ring {
    position: absolute;
    width: 135px; /* রিং লোগোর তুলনায় পারফেক্ট বড় */
    height: 135px;
    border: 4px dashed #00fff2; /* ড্যাশ লাইন স্পষ্ট এবং মোটা */
    border-radius: 50%;
    filter: drop-shadow(0 0 25px #00fff2);
    animation: rotateRing 12s linear infinite;
    z-index: 2;
}

/* রিং ঘূর্ণন অ্যানিমেশন */
@keyframes rotateRing {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}

/* মায়াবি সোজা টেক্সট - হাই-ডেফিনিশন নিয়ন গ্লো */
.straight-title {
    width: 100%;
    padding: 16px;
    text-align: center;
    margin: 5px 0; /* লোগোর সাথে দূরত্ব কমানো হয়েছে */
    perspective: 1000px;
}

.straight-title h1 {
    color: #ffffff;
    font-family: 'Orbitron', sans-serif;
    font-size: 20px; /* আপনার পছন্দের সাইজ */
    font-weight: 900;
    letter-spacing: 5px;
    text-transform: uppercase;
    margin: 0;
    position: relative;
    display: inline-block;

    /* টেক্সট হালকা মোটা করার জন্য স্ট্রোক */
    -webkit-text-stroke: 0.6px rgba(255, 255, 255, 0.6);
    
    /* ক্লিয়ার এবং মায়াবি অ্যানিমেশন */
    animation: mysticalGlow 3s infinite ease-in-out;
    transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

@keyframes mysticalGlow {
    0%, 100% {
        /* স্মুথ এবং ক্লিয়ার নিয়ন গ্লো */
        text-shadow: 0 0 10px rgba(0, 255, 245, 0.8),
                     0px rgba(0, 255, 245, 0.2);
        transform: scale(1);
        opacity: 0.95;
    }
    50% {
        /* মায়াবি উজ্জ্বল গ্লো */
        text-shadow: 0 0 7px rgba(0, 255, 245, 1),
                     0 0 14px rgba(0, 255, 245, 0.6),
                     0 0 28px rgba(0, 255, 245, 0.3);
        transform: scale(1.03); 
        opacity: 1;
    }
}

/* মাউস নিলে হোভার ইফেক্ট */
.straight-title h1:hover {
    color: #00fff5;
    letter-spacing: 7px;
    -webkit-text-stroke: 0.8px rgba(0, 255, 245, 0.8);
    cursor: pointer;
    text-shadow: 0 0 25px rgba(0, 255, 245, 1);
}


/* ইনপুট ফিল্ড প্রো স্টাইল */
.login-box input {
    width: 100%;
    padding: 16px;
    margin-top: 10px;
    margin-bottom: 25px;
    background: rgba(255, 255, 255, 0.03);
    border: 1px solid rgba(0, 255, 242, 0.4);
    border-radius: 15px;
    color: #fff;
    text-align: center;
    font-size: 15px;
    outline: none;
    transition: 0.3s;
}

.login-box input:focus {
    background: rgba(255, 255, 255, 0.08);
    border-color: #00fff2;
    box-shadow: 0 0 15px rgba(0, 255, 242, 0.2);
}

/* বাটন - আরও গ্লোয়িং এবং প্রিমিয়াম */
.login-btn {
    width: 100%;
    padding: 16px;
    border-radius: 15px;
    font-family: 'Orbitron', sans-serif;
    font-weight: 900;
    font-size: 14px;
    letter-spacing: 2px;
    cursor: pointer;
    color: #000;
    background: linear-gradient(90deg, #00fff2, #00f2ea);
    box-shadow: 0 0 25px rgba(0, 242, 234, 0.6);
    transition: 0.4s;
    border: none;
}

.login-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 0 35px #00f2ea;
    filter: brightness(1.2);
}

/* এনিমেশনসমূহ */
@keyframes borderGlowFlow {
    0%, 100% { border-color: #a855f7; box-shadow: 0 0 40px rgba(138, 85, 241, 0.4); }
    50% { border-color: #00fff2; box-shadow: 0 0 40px rgba(0, 255, 242, 0.4); }
}

@keyframes rotateRing {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}

@keyframes luxuryBg {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}


/* 
   ============================================================
   ULTIMATE LIVE STATUS POD - FINAL CSS (COMPLETE VERSION)
   ============================================================ 
*/

/* গুগল ফন্ট ইমপোর্ট (Orbitron - Sci-Fi Look) */
@import url('https://fonts.googleapis.com');

/* ১. মেইন স্ট্যাটাস বার কন্টেইনার */
#status-bar-zx {
    position: fixed;
    width: 280px; 
    transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
    display: none;     
    top: 370px;
    left: 48px;
    height: 33px; /* আপনার রিকোয়েস্ট করা ফিক্সড হাইট */
    background: rgba(0, 15, 20, 0.85);
    border: 1.40px solid rgba(0, 255, 242, 0.5);
    border-radius: 12px;
    display: none; /* আনলক করার আগে লুকানো থাকবে */
    align-items: center;
    padding: 0 12px;
    gap: 8px; /* আপনার দেওয়া গ্যাপ */
    z-index: 10000000;
    box-shadow: 0 0 30px rgba(0, 255, 242, 0.2), inset 0 0 10px rgba(0, 255, 242, 0.1);
    backdrop-filter: blur(5px);
    font-family: 'Orbitron', sans-serif;
    overflow: hidden;
    cursor: move; /* ড্রাগ করার সংকেত */
    user-select: none;
    touch-action: none;
    transition: transform 0.2s ease, opacity 0.3s ease;
}
/* যখন বন্ধ থাকবে তখন উইডথ ছোট হবে */
#status-bar-zx.pod-minimized {
    width: 40px;
    padding: 0;
    justify-content: center;
}
/* ২. মুভিং স্ক্যানলাইন অ্যানিমেশন (সাইবার লুক) */
#status-bar-zx::before {
    content: "";
    position: absolute;
    top: 0; 
    left: -150%;
    width: 80%; 
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(0, 255, 242, 0.15), transparent);
    animation: podScan 4s infinite linear;
}

@keyframes podScan { 100% { left: 250%; } }

/* ৩. আইটেম এবং আইকন লেআউট */
.status-item {
    display: flex;
    align-items: center;
    gap: 6px;
    position: relative;
    z-index: 2;
}

.svg-icon {
    width: 16px; /* ৩৫পিএক্স হাইটের জন্য অ্যাডজাস্ট করা */
    height: 16px;
    transition: 0.3s;
}

/* ৪. ডিভাইডার লাইন */
.divider {
    width: 1px;
    height: 18px;
    background: rgba(0, 255, 242, 0.2);
}

/* ৫. অ্যানিমেশন ইফেক্টস (WiFi, Signal, Bot) */
.wifi-pulse { animation: wifiGlow 1.5s infinite alternate; }
@keyframes wifiGlow { 
    0% { filter: drop-shadow(0 0 1px #0ff); opacity: 0.7; } 
    100% { filter: drop-shadow(0 0 8px #0ff); opacity: 1; } 
}

.bar-4 { animation: signalBlink 1.2s infinite 0.2s; }
.bar-3 { animation: signalBlink 1.2s infinite 0.5s; }
@keyframes signalBlink { 0%, 100% { opacity: 1; } 50% { opacity: 0.2; } }

.bot-glow { animation: botHover 3s infinite ease-in-out; }
@keyframes botHover { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-2px); } }

.bot-eye { animation: eyeBlink 4s infinite; }
@keyframes eyeBlink { 0%, 95%, 100% { opacity: 1; } 97% { opacity: 0; } }

/* ৬. টেক্সট ও ভ্যালু স্টাইলিং */
.info-col { display: flex; flex-direction: column; line-height: 1; }

.speed-val, #online-users {
    font-size: 11px; /* ৩৫পিএক্স হাইটের জন্য পারফেক্ট সাইজ */
    font-weight: 900;
    color: #fff;
    letter-spacing: 0.5px;
    text-shadow: 0 0 5px rgba(0, 255, 242, 0.5);
}

.unit {
    font-size: 7px;
    color: #00fff2;
    text-transform: uppercase;
    font-weight: bold;
    opacity: 0.8;
}

/* ৭. টগল (Toggle) বাটন স্টাইল */
#pod-toggle-zx {
    width: 18px;
    height: 18px;
    background: rgba(255, 23, 68, 0.2);
    color: #ff1744;
    border: 1px solid rgba(255, 23, 68, 0.5);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    margin-left: 7px;
    z-index: 3;
    transition: 0.3s;
}

#pod-toggle-zx:hover { background: #ff1744; color: #fff; }

/* ৮. মিনিমাইজড (Toggle On) স্টেট */
.pod-minimized {
    width: 40px !important;
    padding: 0 !important;
    justify-content: center !important;
}

.pod-minimized .status-item, 
.pod-minimized .divider {
    display: none !important;
}

/* ৯. কানেকশন লস ওভারলে (Error State) */
#zx-error-overlay {
    position: fixed;
    inset: 0;
    background: rgba(0, 5, 10, 0.95);
    z-index: 10000001;
    display: none; /* JS দিয়ে flex করা হবে */
    flex-direction: column;
    align-items: center;
    justify-content: center;
    backdrop-filter: blur(15px);
    color: #fff;
}

.zx-error-box {
    border: 2px solid #ff1744;
    padding: 30px;
    border-radius: 20px;
    background: radial-gradient(circle, #2a0000 0%, #000 100%);
    text-align: center;
    box-shadow: 0 0 50px rgba(255, 23, 68, 0.4);
    font-family: 'Orbitron', sans-serif;
}

.zx-icon {
    font-size: 40px;
    margin-bottom: 15px;
    color: #ff1744;
    animation: zxBlink 1s infinite;
}

@keyframes zxBlink { 50% { opacity: 0.2; transform: scale(0.9); } }

.zx-loader {
    width: 30px;
    height: 30px;
    border: 3px solid rgba(255, 23, 68, 0.1);
    border-top: 3px solid #ff1744;
    border-radius: 50%;
    margin: 15px auto;
    animation: spin 1s linear infinite;
}

@keyframes spin { to { transform: rotate(360deg); } }

/* ১০. অফলাইন মোড (পেজ লক) */
body.is-offline > *:not(#zx-error-overlay) {
    filter: grayscale(1) blur(6px);
    pointer-events: none;
    transition: filter 0.5s ease;
}

 
/*======== CHOICE PAGE COMPACT VIP ======== */
#choicePage {
  position: fixed;
  inset: 0;
  display: none; 
  flex-direction: column;
  align-items: center;
  background: radial-gradient(circle, #000, #050505);
  z-index: 999999;
  padding: 20px 20px;
  overflow-y: auto;
  font-family: 'Arial', sans-serif;
  box-sizing: border-box;
  border: 4px solid #4a90e2; 
  border-radius: 20px;
  margin: 2px; 
  animation: borderGlow 4s infinite alternate, pageShake 5s infinite ease-in-out;
}

/* SUBTLE PAGE SHAKE ANIMATION */
@keyframes pageShake {
  0%, 100% { transform: translate(0, 0); }
  25% { transform: translate(0.5px, 0.5px); }
  50% { transform: translate(-0.5px, -0.5px); }
  75% { transform: translate(0.5px, -0.5px); }
}

@keyframes borderGlow {
  0% { border-color: #4a90e2; box-shadow: 0 0 15px #4a90e2; }
  50% { border-color: #ff4d4d; box-shadow: 0 0 15px #ff4d4d; }
  100% { border-color: #00ff00; box-shadow: 0 0 15px #00ff00; }
}

.choice-container { 
  width: 100%; 
  max-width: 370px; 
  display: flex; 
  flex-direction: column; 
  align-items: center; 
  gap: 15px; 
  padding-bottom: 10px; 
}

/* 1. CHOICE BOX TITLE */
.ai-model-header {
  order: 1;
  font: 900 15px 'Arial';
  color: #fff;
  text-shadow: 0 0 20px #4a90e2;
  text-transform: uppercase;
  width: 100%;
  background: rgba(20, 20, 20, 0.95);
  border: 2px solid #f6c96b;
  border-radius: 15px;
  padding: 5px;
  top: 1px;
  text-align: center;
  box-shadow: inset 0 0 10px rgba(246, 201, 107, 0.2);
}

/* 2. CYBER-DEMON BOT STYLE */
.robot-section { 
  order: 2; 
  filter: drop-shadow(0 0 12px #ff0000); 
  
  transform-style: preserve-3d;
}

.robot-svg {
  width: 140px;
  height: 100px;
  animation: monsterHover 3s infinite ease-in-out;
}

@keyframes monsterHover {
  0%, 100% { transform: translateY(0) scale(1); }
  50% { transform: translateY(-5px) scale(1.02); }
}

/* 3. SYSTEM NOTICE BOX */
.feature-footer {
  order: 3;
  width: 100%; 
  border: 4px solid #00ffff; 
  background: rgba(5, 5, 5, 0.95);
  padding: 10px 10px; 
  width: 110%;
  border-radius: 18px;
  box-sizing: border-box;
  
  position: relative;
  box-shadow: inset 0 0 10px rgba(0, 255, 255, 0.1);
}
@keyframes cleanSwing { to { transform: translateY(-8px); } }
.feature-footer::before {
  content: "📢 SYSTEM MODELS";
  position: absolute;
  top: -12px;
  left: 50%;
  transform: translateX(-50%);
  background: #00ffff;
  color: #000;
  padding: 2px 12px;
  font: 900 14px 'Arial';
  border-radius: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.notice-list { 
  display: grid; 
  grid-template-columns: 1fr 1fr; 
  gap: 8px; 
  list-style: none; 
  padding: 8px 0 0 0; 
  margin: 0;
}

.notice-list li { 
  font: 900 13px 'Arial';
  color: #fff; 
  text-transform: uppercase;
  text-align: center;
  padding: 5px 3px;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.4), 0 2px 4px #000;
  border: 2px solid rgba(0, 255, 255, 0.2); 
  border-radius: 20px;
  background: rgba(255, 255, 255, 0.02);
  display: flex;
  align-items: center;
  justify-content: center;
}

/* 4. STATUS BOX */
.top-status-box {
  order: 4;
  width: 105%;
  background: rgba(20, 20, 20, 0.9);
  border: 2px solid #f6c96b;
  border-radius: 12px;
  padding: 2px; 
  text-align: center;
  top: 1px;
  box-shadow: inset 0 0 10px rgba(246, 201, 107, 0.2);
}
@keyframes blinkNotice { 50% { opacity: 0.4; } }
/* 5. ENGINE BOX */
.engine-box {
  order: 5;
  width: 110%;
  background: rgba(10, 10, 10, 0.95);
  border-radius: 20px;
  padding: 30px 15px;
  border: 2px solid #fff;
  text-align: center;
  margin-top: 5px; 
  box-sizing: border-box;
  animation: shadowFlow 6s infinite alternate;
}

.engine-title { 
  font: 900 33px 'Arial'; 
  text-shadow: 0 0 20px rgba(255,255,255,0.4); 
  color: #fff; 
  margin-bottom: 50px; 
}

.engine-buttons { 
  display: flex; 
  gap: 40px; 
  justify-content: center; 
  width: 100%; 
}

.engine-btn { 
  flex: 1; 
  max-width: 130px; 
  padding: 15px 0; 
  font: 900 18px 'Arial'; 
  border-radius: 12px; 
  border: none; 
  cursor: pointer; 
}

.dk-btn { background: #f6c96b; color: #000; box-shadow: 0 0 10px #f6c96b; }
.hz-btn { background: #ff4d4d; color: #fff; box-shadow: 0 0 10px #ff4d4d; }

/* 6. ACTION BUTTONS */
.action-row { 
  order: 6;
  display: flex; 
  gap: 30px; 
  width: 100%; 
  margin-top: 26px; 
}

.telegram-btn, .admin-btn {
  flex: 1; 
  padding: 12px 0; 
  border-radius: 10px; 
  border: 1px solid rgba(255, 255, 255, 0.1);
  font: 900 11px 'Arial'; 
  text-transform: uppercase; 
  cursor: pointer; 
  backdrop-filter: blur(5px);
}

.telegram-btn { background: linear-gradient(135deg, #0088cc, #00acee); color: #fff; }
.admin-btn { background: linear-gradient(135deg, #2ecc71, #27ae60); color: #fff; }

.dev-info {
  order: 7;
  margin-top: 8px; 
  font: 900 14px 'Arial'; 
  color: #fff;
  text-align: center;
  animation: multiColorShadow 5s infinite;
}

/* ANIMATIONS */
@keyframes shadowFlow {
  0% { box-shadow: 0 0 15px #f0f; border-color: #f0f; }
  50% { box-shadow: 0 0 15px #0ff; border-color: #0ff; }
  100% { box-shadow: 0 0 15px #ff4d4d; border-color: #ff4d4d; }
}

@keyframes multiColorShadow {
  0%, 100% { text-shadow: 0 0 8px #f00; }
  33% { text-shadow: 0 0 8px #0f0; }
  66% { text-shadow: 0 0 8px #00f; }
}

/* ডেবোলপার সিগনেচার (নোটিশ বক্সের ভেতরে থাকবে) */
.dev-info {
  margin-top: 15px; font: 900 18px 'Arial'; color: #fff;
  text-align: center;
  animation: multiColorShadow 8s infinite;
}

/* ================= ANIMATIONS (KEEP ORIGINAL) ================= */
@keyframes borderGlow {
  0% { border-color: #4a90e2; box-shadow: 0 0 20px #4a90e2; }
  50% { border-color: #ff4d4d; box-shadow: 0 0 20px #ff4d4d; }
  100% { border-color: #00ff00; box-shadow: 0 0 20px #00ff00; }
}
@keyframes swing { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-10px); } }
@keyframes shadowFlow {
  0% { box-shadow: 0 0 20px #f0f; border-color: #f0f; }
  50% { box-shadow: 0 0 20px #0ff; border-color: #0ff; }
  100% { box-shadow: 0 0 20px #ff4d4d; border-color: #ff4d4d; }
}

@keyframes multiColorShadow {
  0% { text-shadow: 0 0 10px #ff0000; }
  20% { text-shadow: 0 0 10px #00ff00; }
  40% { text-shadow: 0 0 10px #0000ff; }
  60% { text-shadow: 0 0 10px #ffff00; }
  80% { text-shadow: 0 0 10px #ff00ff; }
  100% { text-shadow: 0 0 10px #ff0000; }
}

/* VIP Iframe */
#iframe{display:none;width:100%;height:calc(var(--vh)*1);border:none;}

/* LIVE BAR */
.live-bar{position:fixed;top4px;left:80%;transform:translateX(-50%);background:#111;padding:3px 10px;border-radius:22px;font-size:6px;font-weight:900;color:#fff;opacity:0;display:flex;align-items:center;gap:5px;z-index:99999;animation:liveGlow 3s infinite;border:3px solid rgba(255,255,255,.12);}
.live-bar.show{opacity:1;}
@keyframes liveGlow{0%,100%{box-shadow:0 0 18px #ff3b3b;}50%{box-shadow:0 0 30px #ff8585;}}
.live-dot{width:8px;height:7px;border-radius:50%;background:#ff2d2d;animation:blink 1.2s infinite;}
@keyframes blink{0%,100%{opacity:.3;}50%{opacity:1;}}
@keyframes shadowFlow {
  0% { box-shadow: 0 0 20px #f0f; border-color: #f0f; }
  50% { box-shadow: 0 0 20px #0ff; border-color: #0ff; }
  100% { box-shadow: 0 0 20px #ff4d4d; border-color: #ff4d4d; }
}

/*======== Loader======= */
.dopely-loader {
  position: relative;
  width: 35px; /* কন্টেইনারের সাইজ নির্দিষ্ট */
  height: 35px;
  margin: 10px auto;
  animation: dopely-spin 1s linear infinite;
}

.bar {
  position: absolute;
  width: 9px;     /* একটু চিকন করা হয়েছে সামঞ্জস্যের জন্য */
  height: 18px;    
  border-radius: 10px;
  left: 50%;
  top: 50%;       /* মাঝখান থেকে শুরু হবে */
  /* transform-origin এখন একদম বারের সেন্টারে থাকবে */
  margin-left: -4px; 
  margin-top: -20px; /* বারকে কেন্দ্র থেকে কিছুটা উপরে ঠেলে দেওয়া হয়েছে */
  transform-origin: 50% 20px; /* ঘোরার কেন্দ্রবিন্দু একদম সঠিক করা হয়েছে */
}

/* CLOUR POJISON */
.bar-cyan { background-color: #32d1c1; transform: rotate(0deg); }
.bar-yellow { background-color: #f6cd46; transform: rotate(120deg); }
.bar-purple { background-color: #6d5dfc; transform: rotate(240deg); }

@keyframes dopely-spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}
/* ================= কম্প্যাক্ট FX BOX (Updated & Resized) ================= */
@keyframes borderGlowFlow {
    0% { border-color: #ff00ea; box-shadow: 0 0 10px #ff00ea, inset 0 0 5px #ff00ea; }
    33% { border-color: #00d4ff; box-shadow: 0 0 20px #00d4ff, inset 0 0 10px #00d4ff; }
    66% { border-color: #7000ff; box-shadow: 0 0 15px #7000ff, inset 0 0 8px #7000ff; }
    100% { border-color: #ff00ea; box-shadow: 0 0 10px #ff00ea, inset 0 0 5px #ff00ea; }
}

.fx-box {
  position: fixed;
  top: 300px;
  left:150px;
  width: 160px; /* সাইজ ১৮৫ থেকে কমিয়ে ১৬০ করা হয়েছে */
  padding: 6px 4px; /* প্যাডিং কমানো হয়েছে */
  border-radius: 12px;
  text-align: center;
  background: #000; 
  backdrop-filter: blur(15px); 
  border: 2.5px solid transparent; 
  animation: fxBoxSwing 8s infinite ease-in-out, borderGlowFlow 4s linear infinite; 
  touch-action: none;
  z-index: 9999;
  font-family: 'Orbitron', 'Arial', sans-serif;
  transform-origin: center;
  transition: all 0.5s ease;
}

/* পিরিয়ড টেক্সট */
.period {
  margin-top: 1px;
  font-size: 8px; /* টেক্সট কিছুটা ছোট করা হয়েছে */
  font-weight: 900;
  color: #fff;
}

/* result text */
.result {
  font-weight: 900;
  text-align: center;
  transition: color 0.5s ease;
}

.big {
  font-size: 50px; /* ৬০ থেকে কমিয়ে ৫০ */
  font-weight: 900;
}

.small {
  font-size: 30px; /* ৩৫ থেকে কমিয়ে ৩০ */
  font-weight: 900;
}

/* TAITEL SUB */
.fx-title {
  font-size: 11px; 
  width: 100%;
  font-weight: 900;
  color: #fff;
}

.fx-sub {
  font-size: 10px; 
  color: #f6c96b;
  margin-bottom: 2px;
}

/* TIME AND WATCH - টাইমারের কালার পরিবর্তন করা হয়েছে */
#rt {
  font-size: 17px; 
  font-weight: 900;
  color: #00f2ff; /* সুন্দর ব্রাইট সায়ান/নিয়ন কালার */
  text-shadow: 0 0 5px #00f2ff;
}

#clock { 
  font-size: 10px; 
  color: #bbb; 
}

.clock-row { 
  display: flex; 
  justify-content: center; 
  gap: 4px; 
  margin-top: 3px; 
}

@keyframes fxBoxSwing {
  0%   { transform: translateX(-8px) translateY(0px) rotate(-0.3deg) scale(1); }
  25%  { transform: translateX(6px) translateY(-2px) rotate(0.2deg) scale(1.01); }
  50%  { transform: translateX(8px) translateY(0px) rotate(0deg) scale(1.02); }
  75%  { transform: translateX(-6px) translateY(2px) rotate(-0.2deg) scale(1.01); }
  100% { transform: translateX(-8px) translateY(0px) rotate(-0.3deg) scale(1); }
}


/* TARGET LOCKED ডিজাইন */
#targetOverlay {
    position: fixed;
    inset: 0;
    background: radial-gradient(circle, #250000 0%, #000000 100%);
    z-index: 9999999;
    display: none; /* JS দিয়ে কন্ট্রোল হবে */
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-family: 'Orbitron', sans-serif;
}

.target-container {
    position: relative;
    width: 280px;
    height: 280px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.target-ring {
    position: absolute;
    width: 100%;
    height: 100%;
    border: 6px double #ff0000;
    border-radius: 50%;
    box-shadow: 0 0 50px rgba(255, 0, 0, 0.8), inset 0 0 30px rgba(255, 0, 0, 0.5);
    animation: targetPulse 0.1s infinite alternate;
}

.crosshair-h { position: absolute; width: 120%; height: 2px; background: rgba(255,0,0,0.4); box-shadow: 0 0 10px #f00; }
.crosshair-v { position: absolute; width: 2px; height: 120%; background: rgba(255,0,0,0.4); box-shadow: 0 0 10px #f00; }

#countNum {
    font-size: 150px;
    color: #ffffff;
    font-weight: 900;
    text-shadow: 0 0 40px #ff0000;
    z-index: 10;
}

.target-text {
    margin-top: 50px;
    color: #ff0000;
    font-size: 35px;
    font-weight: 900;
    letter-spacing: 8px;
    text-transform: uppercase;
    text-shadow: 0 0 15px #ff0000;
    animation: targetBlink 0.3s infinite;
}

/* ভাইব্রেশন এনিমেশন */
.vibrate-screen {
    animation: screenShake 0.1s infinite;
}

@keyframes screenShake {
    0% { transform: translate(3px, 2px); }
    33% { transform: translate(-3px, -2px); }
    66% { transform: translate(2px, -3px); }
    100% { transform: translate(-2px, 3px); }
}

@keyframes targetPulse {
    from { transform: scale(1); }
    to { transform: scale(1.05); }
}

@keyframes targetBlink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.2; }
}

/* ================= ANIMATIONS ================= */
@keyframes blinkNotice{0%,100%{opacity:0.7;}50%{opacity:1;}}
@keyframes btnSwing{0%{transform:translateY(0);}50%{transform:translateY(-4px);}100%{transform:translateY(0);}}
@keyframes noticeColorSwing{0%{border-color:#fff;}50%{border-color:#ffccff;}100%{border-color:#fff;}}
@keyframes engineColorSwing{0%{border-color:#fff;}50%{border-color:#00ffcc;}100%{border-color:#fff;}}
</style>
</head>
<body>

<!-- VIP PREMIUM LOGIN START -->
<div class="login" id="loginBox">
🏆🌐🏆🌐🏆🌐🏆🌐
  <div class="login-box">
    👑👑👑
   <div class="logo-section">
        <div class="logo-ring"></div>
        <img src="https://i.ibb.co.com/dJfHYZQs/Picsart-26-03-01-16-18-28-128.jpg" alt="ZIHAD SIR" class="user-logo">
    </div>
                <div class="straight-title">
    <h1>ZIHAD SIR_ZX TRADER</h1>
</div>
    
    <input id="pass" type="password" placeholder="𝙴𝙽𝚃𝙴𝚁 𝚅𝙸𝙿 𝙰𝙲𝙲𝙴𝚂𝚂">
    <div class="login-btn" id="unlockBtn">𝐀𝐂𝐂𝐄𝐒𝐒 𝐋𝐎𝐆𝐈𝐍</div>
  </div>
</div>

<!-- TARGET LOCKED -->
<div id="targetOverlay" style="display:none;">
    <div class="target-container">
        <div class="target-ring"></div>
        <div class="crosshair-h"></div>
        <div class="crosshair-v"></div>
        <div id="countNum">5</div>
    </div>
    <div class="target-text">❗TARGET LOCK</div>
</div>


<!-- mp3 sound  -->
<audio id="errorSound" src="https://files.catbox.moe/9qfpc1.mp3"></audio>
<audio id="clickSound" src="https://files.catbox.moe/amw7wv.mp3"></audio>
<audio id="typeSound" src="https://files.catbox.moe/dgdpcb.mp3"></audio>
<audio id="lockedSound" src="https://files.catbox.moe/rjswoi.mp3"></audio>

<div id="choicePage">
  <div class="choice-container" id="choiceContainer">
    
    <!-- ১. সবার উপরে AI টাইটেল -->
    <h1 class="ai-model-header" id="mainTitle">🔮 𝐆𝐑𝐍𝐓𝐄𝐃 𝐂𝐘𝐁𝐄𝐑 𝐃𝐄𝐌𝐎𝐍 𝐌𝐎𝐍𝐒𝐓𝐄𝐑 𝐁𝐎𝐓 🔮</h1>

    <!--2-Cyber-Demon Monster BOT  -->
<div class="robot-section" id="botLogoSection">
  <svg class="robot-svg" viewBox="0 0 200 200" xmlns="http://www.w3.org">
    <defs>
      <!-- Deep blood-red glow for eyes -->
      <radialGradient id="eyeGlowDeep" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stop-color="#ff0000" />
        <stop offset="70%" stop-color="#4a0000" />
        <stop offset="100%" stop-color="#000" />
      </radialGradient>
      
      <!-- Extreme outer glow filter for horns and eyes -->
      <filter id="extremeGlow" x="-100%" y="-100%" width="300%" height="300%">
        <feGaussianBlur stdDeviation="10" result="blur" />
        <feComposite in="SourceGraphic" in2="blur" operator="over" />
      </filter>
    </defs>

    <!-- Massive Thick Horns -->
    <path class="horns" d="M35 65 L-15 0 Q-30 -10 15 15 L50 75 Z" fill="#ff0000" filter="url(#extremeGlow)" />
    <path class="horns" d="M165 65 L215 0 Q230 -10 185 15 L150 75 Z" fill="#ff0000" filter="url(#extremeGlow)" />

    <!-- Main Skull Structure with Thick White Border -->
    <path d="M40 70 Q40 15 100 15 Q160 15 160 70 L168 145 L145 190 L100 178 L55 190 L32 145 Z" 
          fill="#000" stroke="#ffffff" stroke-width="5" />

    <!-- Aggressive Animated Eyebrows -->
    <g class="brows-group">
      <path d="M50 85 L95 110" stroke="#ff0000" stroke-width="8" stroke-linecap="round" />
      <path d="M150 85 L105 110" stroke="#ff0000" stroke-width="8" stroke-linecap="round" />
    </g>

    <!-- Giant Glowing Eyes (Pulsing) -->
    <g class="eyes-group">
      <circle cx="70" cy="120" r="16" fill="url(#eyeGlowDeep)" filter="url(#extremeGlow)">
        <animate attributeName="r" values="14;18;14" dur="0.8s" repeatCount="indefinite" />
      </circle>
      <circle cx="130" cy="120" r="16" fill="url(#eyeGlowDeep)" filter="url(#extremeGlow)">
        <animate attributeName="r" values="14;18;14" dur="0.8s" repeatCount="indefinite" />
      </circle>
      <!-- Eye Pupil -->
      <circle cx="70" cy="120" r="5" fill="#fff" />
      <circle cx="130" cy="120" r="5" fill="#fff" />
    </g>

    <!-- Morphing Teeth (Anger to Smile) -->
    <path class="teeth-morph" d="M65 155 Q100 155 135 155" stroke="#0ff" stroke-width="5" fill="none" stroke-linecap="round">
       <animate attributeName="d" 
                values="M65 155 Q100 155 135 155; M65 155 Q100 185 135 155; M65 155 Q100 155 135 155" 
                dur="2.5s" repeatCount="indefinite" />
    </path>
    <!-- Teeth Grid -->
    <line x1="82" y1="150" x2="82" y2="162" stroke="#fff" stroke-width="2" />
    <line x1="100" y1="150" x2="100" y2="170" stroke="#fff" stroke-width="2" />
    <line x1="118" y1="150" x2="118" y2="162" stroke="#fff" stroke-width="2" />
  </svg>
</div>

    <!-- ৩. নোটিশ বক্স (ফিচার লিস্ট) -->
    <div class="feature-footer" id="noticeBox">
      <ul class="notice-list">
        <li>🔮 𝙲𝚈𝙱𝙴𝚁 𝙳𝙴𝙼𝙾𝙽 𝙱𝙾𝚃ˎˊ˗</li>
        <li>🌎 𝚆𝙸𝙽 𝙶𝙾 𝙻𝙸𝚅𝙴  𝙰𝙿𝙸 ˎˊ˗</li>
        <li>🕹️ 𝙰𝙸 𝙲𝚈𝙱𝙴𝚁 𝚂𝙰𝙿𝙾𝚁𝙳 ˎˊ˗</li>
        <li>🎯 𝚄𝙻𝚃𝚃𝚁𝙰 𝙰𝙽𝙰𝙻𝚈𝚂𝙴𝚂ˎˊ˗</li>
        <li>🎲 𝚅𝙾𝙻𝙰𝚃𝙸𝙻𝙸𝚃𝚈 𝙲𝙷𝙴𝙲𝙺ˎˊ˗</li>
        <li>🪩 𝚂𝙴𝚂𝚂𝙸𝙾𝙽 𝙰𝙲𝙲𝙴𝚂𝚂 𝙿𝙷𝙿</li>
      </ul>
      <div class="dev-info" id="developerSignature">💡 DEVELOPER: √•• • zιнα∂ нαѕαη ✔✔</div>
    </div>

    <!-- ৫. ষ্টেটাস বক্স (ক্লিয়ার এবং স্পষ্ট) -->er">
    <div class="top-status-box" id="statusBox">
      <div class="time-container">
        <p class="start-text"></p>
        <p class="exp-text"></p>
    <!-- আপনার টাইম কাউন্টডাউন আইডি -->    
        <div class="countdown-display" id="vipCountdown">REMAINING: 0d 9h 56m 4s</div>
      </div>
    </div>

    <!-- ৫. ইঞ্জিন বক্স (গেম ইঞ্জিন) -->
    <div class="engine-box" id="gameEngineBox">
      <h2 class="engine-title">🎰 𝐒𝐄𝐋𝐄𝐂𝐓 𝐆𝐀𝐌𝐄 亗</h2>
      <div class="engine-buttons">
        <button class="engine-btn dk-btn" id="dkBtn" onclick="chooseEngine('dk')">𝐃𝐊 𝐖𝐈𝐍 🎲</button>
        <button class="engine-btn hz-btn" id="hzBtn" onclick="chooseEngine('hz')">𝐇𝐙𝐍𝐈𝐂𝐄 🤚</button>
      </div>
    </div>

    <!-- ৬. অ্যাকশন বাটন (টেলিগ্রাম ও অ্যাডমিন) -->
    <div class="action-row" id="actionButtons">
      <button class="telegram-btn" id="teleBtn" onclick="window.open('https://t.me', '_blank')">TELEGRAM PREMIUM</button>
      <button class="admin-btn" id="adminBtn" onclick="window.open('https://t.me', '_blank')">ADMIN</button>
    </div>

  </div>
</div>

<!-- VIP IFRAME -->
<iframe id="vipFrame"></iframe>

<!-- LIVE BAR -->
<div class="live-bar" id="liveBar">
  <span class="live-dot"></span>❮«ꔪ»❯ <span class="live-dot"></span>
      <div id="clock">00:00:00</div>
      <span class="live-dot"></span>
</div>

<div class="fx-box" id="box">
  <div class="fx-title" id="fxToggle"> 🏆  𝐙𝐗 𝐀𝐆𝐄𝐍𝐓 𝐏𝐄𝐍𝐄𝐋  🏆</div>
  <div id="fxBody" style="display: none;"> <!-- এটি এখন শুরুতে লুকিয়ে থাকবে -->
   <div class="fx-sub"> 𝐖𝐈𝐍𝐆𝐎 𝟑𝟎 𝐒𝐄𝐂 </div>
    <div id="rt"></div>
    <div class="clock-row"></div>
    <div class="dopely-loader" id="loader">
   <div class="bar bar-cyan"></div>
  <div class="bar bar-yellow"></div>
  <div class="bar bar-purple"></div>
</div>
    <div id="result" class="result"></div>
    <div id="fx-info" style="color: #fff; font-size: 9px; margin-top: 6px; text-align: center;"></div><div class="period" id="dPeriod">----</div>
</div>
</div>

<!-- ================= ULTIMATE LIVE STATUS POD (FINAL STRUCTURE) ================= -->
<div id="status-bar-zx">

    <!-- মুভিং স্ক্যানলাইন লেয়ার (CSS এনিমেটেড) -->
    <div class="pod-scanline"></div>

    <!-- ১. WiFi সেকশন (লাইভ স্পিড) -->
    <div class="status-item">
        <div class="icon-box">
            <svg viewBox="0 0 24 24" class="svg-icon wifi-pulse">
                <path d="M12 18c-1.1 0-2 .9-2 2s.9 2 2 2 2-.9 2-2-.9-2-2-2zm0-4c-2.2 0-4.2.9-5.7 2.3l1.4 1.4c1.1-1.1 2.6-1.7 4.3-1.7s3.2.6 4.3 1.7l1.4-1.4c-1.5-1.4-3.5-2.3-5.7-2.3zm0-4c-3.3 0-6.3 1.3-8.5 3.5l1.4 1.4c1.8-1.8 4.4-2.9 7.1-2.9s5.3 1.1 7.1 2.9l1.4-1.4c-2.2-2.2-5.2-3.5-8.5-3.5z" fill="#00fff2"/>
            </svg>
        </div>
        <div class="info-col">
            <span id="net-speed" class="speed-val">0.00</span>
            <span class="unit">mbps</span>
        </div>
    </div>

    <div class="divider"></div>

    <!-- ২. নেটওয়ার্ক সিগন্যাল (KB/S মিটার) -->
    <div class="status-item">
        <div class="icon-box">
            <svg viewBox="0 0 24 24" class="svg-icon signal-bars">
                <!-- ব্যাকগ্রাউন্ড বার -->
                <rect x="3" y="14" width="3" height="6" fill="#333" rx="1" class="bar-1"/>
                <!-- এনিমেটেড সিগন্যাল বার -->
                <rect x="8" y="11" width="3" height="9" fill="#00fff2" rx="1" class="bar-2"/>
                <rect x="13" y="7" width="3" height="13" fill="#00fff2" rx="1" class="bar-3"/>
                <rect x="18" y="3" width="3" height="17" fill="#00fff2" rx="1" class="bar-4"/>
            </svg>
        </div>
        <div class="info-col">
            <span id="net-kbs" class="speed-val">0/0</span>
            <span class="unit">kb/s</span>
        </div>
    </div>

    <div class="divider"></div>

    <!-- ৩. বট স্ট্যাটাস ও ইউজার কাউন্ট -->
    <div class="status-item">
        <div class="icon-box bot-glow">
            <svg viewBox="0 0 24 24" class="svg-icon">
                <!-- বটের শরীর -->
                <path d="M12 2v2M12 4c-4.4 0-8 3.6-8 8v6c0 1.1.9 2 2 2h12c1.1 0 2-.9 2-2v-6c0-4.4-3.6-8-8-8z" stroke="#00fff2" stroke-width="1.8" fill="none" />
                <!-- ব্লিংকিং চোখ -->
                <circle cx="9" cy="11" r="1.2" fill="#00fff2" class="bot-eye"/>
                <circle cx="15" cy="11" r="1.2" fill="#00fff2" class="bot-eye"/>
                <path d="M9 15h6" stroke="#00fff2" stroke-width="1.5" stroke-linecap="round" />
            </svg>
        </div>
        <div class="info-col">
            <span id="online-users" class="user-val">221</span>
            <span class="unit">active</span>
        </div>
    </div>
    <div id="pod-toggle-zx" title="Hide Stat">×</div>
</div>

<!-- ================= কানেকশন লস ওভারলে (ERROR UI) ================= -->
<div id="zx-error-overlay">
    <div class="zx-error-box">
        <div class="zx-icon">⚠️</div>
        <h3 style="margin: 0; font-family: 'Orbitron'; color: #ff1744; letter-spacing: 2px;">🚨‿╯ ϟ  𝙲𝙾𝙽𝙽𝙴𝙲𝚃𝙸𝙾𝙽 𝙳𝙴𝙰𝙳 ༶</h3>      
        <div class="zx-loader"></div>
        <p style="color: #ccc; font-size: 13px; margin: 15px 0; font-family: sans-serif;">✈️  No Internet connection.. . </p>
        <div style="font-size: 10px; color: #666; font-family: 'Orbitron';">⚠RESCANNING ENGINES.. . . </div>
    </div>
</div>


<script>
/* ================= COMPLETE PASSWORD SYSTEM (START TODAY) ================= */
const ADMIN_PASSWORD = "ZIHAD20";
const PASSWORDS = [
  "ZX4K-MAR04", "ZX9R-MAR07", "ZX2B-MAR10", "ZX7W-MAR13",
  "ZX1M-MAR16", "ZX6P-MAR19", "ZX3G-MAR22", "ZX8V-MAR25",
  "ZX5N-MAR28", "ZX9S-MAR31", "ZX2D-APR03", "ZX7H-APR06",
  "ZX4L-APR09", "ZX1Q-APR12", "ZX6X-APR15", "ZX3A-APR18",
  "ZX8Z-APR21", "ZX5F-APR24", "ZX9T-APR27", "ZX2Y-APR30",
  "ZX7C-MAY03", "ZX4M-MAY06", "ZX1K-MAY09", "ZX6W-MAY12",
  "ZX3P-MAY15", "ZX8R-MAY18", "ZX5G-MAY21", "ZX9V-MAY24",
  "ZX2J-MAY27", "ZX7S-MAY30", "ZX4B-JUN02", "ZX1X-JUN05",
  "ZX6N-JUN08", "ZX3D-JUN11", "ZX8L-JUN14", "ZX5Q-JUN17",
  "ZX9A-JUN20", "ZX2H-JUN23", "ZX7M-JUN26", "ZX4R-JUN29",
  "ZX1Z-JUL02", "ZX6G-JUL05", "ZX3V-JUL08", "ZX8F-JUL11",
  "ZX5K-JUL14", "ZX9D-JUL17", "ZX2W-JUL20", "ZX7P-JUL23",
  "ZX4S-JUL26", "ZX1N-JUL29", "ZX6T-AUG01", "ZX3X-AUG04",
  "ZX8B-AUG07", "ZX5M-AUG10", "ZX9L-AUG13", "ZX2G-AUG16",
  "ZX7A-AUG19", "ZX4V-AUG22", "ZX1F-AUG25", "ZX6Q-AUG28",
  "ZX3Y-AUG31", "ZX8C-SEP03", "ZX5H-SEP06", "ZX9K-SEP09",
  "ZX2N-SEP12", "ZX7W-SEP15", "ZX4Z-SEP18", "ZX1R-SEP21",
  "ZX6P-SEP24", "ZX3S-SEP27"
];

// আজকের তারিখ (মার্চ ৪, ২০২৬) থেকে শুরু
const START_DATE = new Date("2026-03-04T03:30:30").getTime();
const EXPIRY_TIME = 3 * 24 * 60 * 60 * 1000;

function getCurrentPassword() {
  const now = Date.now(), passed = now - START_DATE;
  if (passed < 0) return null;
  const index = Math.floor(passed / EXPIRY_TIME);
  if (index >= PASSWORDS.length) return null;
  return PASSWORDS[index];
}

function getRemainingTime() {
  const now = Date.now(), passed = now - START_DATE;
  const index = Math.floor(passed / EXPIRY_TIME);
  if (index < 0 || index >= PASSWORDS.length) return "0d 0h 0m 0s";
  
  const elapsed = passed % EXPIRY_TIME;
  const remaining = EXPIRY_TIME - elapsed;
  const d = Math.floor(remaining / (1000 * 60 * 60 * 24));
  const h = Math.floor((remaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const m = Math.floor((remaining % (1000 * 60 * 60)) / (1000 * 60));
  const s = Math.floor((remaining % (1000 * 60)) / 1000);
  return `${d}d ${h}h ${m}m ${s}s`;
}

/* ====== VIP COUNTDOWN DISPLAY ====== */
setInterval(() => {
  const now = Date.now();
  const passed = now - START_DATE;
  const index = Math.floor(passed / EXPIRY_TIME);
  const vipCountdown = document.getElementById('vipCountdown');

  if (!vipCountdown) return;

  if (passed < 0) {
    vipCountdown.innerHTML = "SYSTEM NOT STARTED YET";
  } else if (index >= PASSWORDS.length) {
    vipCountdown.innerHTML = "VIP EXPIRED";
  } else {
    const currentStart = START_DATE + (index * EXPIRY_TIME);
    const formatDateTime = (time) => {
      return new Date(time).toLocaleString('en-GB', {
        day: '2-digit', month: 'short', year: 'numeric',
        hour: '2-digit', minute: '2-digit', hour12: true
      });
    };
    const remaining = getRemainingTime();

    vipCountdown.innerHTML = `
      <div style="display: flex; justify-content: center; gap: 10px; margin-bottom: 7px;">
        <div style="font-size: 15px; color: #ffeb3b; font-weight: 900;"> ✅ 𝚂𝚃𝙰𝚁𝚃 𝙿𝙰𝚂𝚂𝚆𝙾𝚁𝙳 ༶ ${formatDateTime(currentStart)}
        </div>
      </div>
      <div style="font-size: 15px; font-weight: 900; color: #fff; padding-top: 2px; letter-spacing: 1px;">
        ❌ 𝙴𝚇𝙿𝙸𝚁𝙴𝙳 𝙿𝙰𝚂𝚂𝚆𝙾𝚁 ༶${remaining}
      </div>
    `;
  }
}, 1000);


/* ============== SAFE DOM DOCUMENT GETTER================ */

const $ = id => document.getElementById(id);

/* ================= ELEMENTS ================= */
const loginBox = document.getElementById("loginBox");
const unlockBtn = document.getElementById("unlockBtn");
const pass = document.getElementById("pass");
const typeSound = document.getElementById('typeSound');
const clickSound = document.getElementById('clickSound');
const errorSound = document.getElementById('errorSound');
const lockedSound = document.getElementById('lockedSound');
const choicePage = document.getElementById("choicePage");
const vipFrame = document.getElementById("vipFrame");
const liveBar = document.getElementById("liveBar");
const loader = document.getElementById("loader");
const result = document.getElementById("result");
const dp = document.getElementById("dPeriod");
const rt = document.getElementById("rt");
const clock = document.getElementById("clock");
const box = document.getElementById("box");
const fxBody = document.getElementById("fxBody");
const fxToggle = document.getElementById("fxToggle");
const vipCountdown = document.getElementById("vipCountdown");

/* ==============🦺 DKWIN  HZNICE  DOMAIN LISTS 🦺============ */
/*=====================DK WIN DOMAIN ====================*/
const dkDomains = [
  "https://dkwin1.com","https://dkwin2.com","https://dkwin3.com","https://dkwin4.com",
  "https://dkwin5.com","https://dkwin6.com","https://dkwin7.com","https://dkwin11.com",
  "https://dkwin12.com","https://dkwin13.com","https://dkwin14.com","https://dkwin15.com",
  "https://dkwin16.com","https://dkwin17.com","https://dkwin18.com","https://dkwin19.com",
  "https://dkwin20.com"
];
/*=====================HZNICE DOMAIN ===================*/
const hzDomains = [
  "https://www.hgnice9.com","https://www.hgnice8.com","https://www.hgnice7.com","https://www.hgnice6.com",
  "https://www.hgnice5.com","https://www.hgnice4.com","https://www.hgnice3.com","https://www.hgnice2.com",
  "https://www.hgnice10.com","https://www.hgnice1.com","https://www.hgnice0.com","https://www.hgnice.pro",
  "https://www.hgnice.org","https://www.hgnice.net","https://www.hgnice.info","https://www.hgnice.biz",
  "https://www.hgnice.bet","https://www.hgnice20.com","https://www.hgnice19.com"
];

let engineDomains = [], enginePath = "", i = 0, retryTimer = null, maxRetries = 10, retries = 0;

/* ========= NEW EFFECTS (Type Sound & Glow) =========== */

pass.addEventListener('input', () => {
    if(typeSound) {
        typeSound.currentTime = 0;
        typeSound.play();
    }
    loginBox.classList.add('input-focus-glow');
});

pass.addEventListener('blur', () => {
    loginBox.classList.remove('input-focus-glow');
});


/* ================= NEW GLITCH CRITICAL SYSTEM (ERROR FREE) ================= */
const targetLockedHTML = `
  <div id="targetOverlay" style="
      display:none; 
      position:fixed; 
      inset:0; 
      background: #000; 
      z-index:999999999; 
      flex-direction:column; 
      align-items:center; 
      justify-content:center; 
      font-family: 'Courier New', monospace;
      overflow: hidden;
      border: 10px solid #ff0000;
      box-sizing: border-box;">
    
    <div style="position:relative; z-index:100; text-align:center;">
       <div id="countNum" style="font-size:250px; color:#fff; font-weight:900; line-height: 1; text-shadow: 8px 0 #ff0000, -8px 0 #00ffff;">5</div>
       <div style="color: #ff0000; font-weight: bold; margin-top: 20px; letter-spacing: 5px; animation: blink 0.3s infinite;">SYSTEM FAILURE</div>
    </div>

    <style>
      @keyframes blink { from { opacity: 1; } to { opacity: 0.1; } }
      #countNum { animation: shake-num 0.1s infinite; }
      @keyframes shake-num {
        0% { transform: translate(2px, -2px); }
        50% { transform: translate(-2px, 2px); }
        100% { transform: translate(0, 0); }
      }
    </style>
  </div>
`;

document.body.insertAdjacentHTML('beforeend', targetLockedHTML);

const targetOverlay = document.getElementById('targetOverlay');
const countNum = document.getElementById('countNum');

/* ================= LOGIN LOGIC (SOUND & ERROR FIX) ================= */
unlockBtn.onclick = function() {
  const input = pass.value;
  const currentPass = (typeof getCurrentPassword === 'function') ? getCurrentPassword() : "";

  if(input === ADMIN_PASSWORD || input === currentPass) {
    if(typeof clickSound !== 'undefined' && clickSound) clickSound.play();
    loginBox.style.display = "none";
    choicePage.style.display = "flex";

const statusBar = document.getElementById('status-bar-zx');
    if (statusBar) {
        statusBar.style.display = 'flex'; 
    }

        /* ================= 1. GLOBAL DEFINITIONS (Top of your code) ================= */
// window. দিয়ে ডিক্লেয়ার করলে অন্য যেকোনো ফাংশন থেকে একে পাওয়া যাবে
window.canSelectGame = false; 

/* ================= 2. UNIVERSAL SPEECH WRAPPER ================= */
const safeSpeak = (text) => {
    console.log("Attempting to speak: " + text);
    
    // Check if Speech API exists in this browser
    if (window.speechSynthesis && typeof SpeechSynthesisUtterance !== 'undefined') {
        try {
            window.speechSynthesis.cancel(); 
            const msg = new SpeechSynthesisUtterance(text);
            msg.onend = () => { 
                window.canSelectGame = true; 
                console.log("✅ canSelectGame is now TRUE");
            };
            msg.onerror = () => { 
                window.canSelectGame = true; // Error হলেও গেম খেলতে দিবে
            };
            window.speechSynthesis.speak(msg);
        } catch (e) {
            console.error("Speech Error:", e);
            window.canSelectGame = true;
        }
    } else {
        console.warn("⚠️ Speech API not supported. Auto-enabling Game Selection.");
        window.canSelectGame = true; // সাপোর্ট না থাকলে সরাসরি এনাবল
    }
};

/* ================= 3. TRIGGER AFTER 8 SECONDS ================= */
setTimeout(() => {
    safeSpeak("Select game");
}, 8000);


  } else {
    // আপনার অরিজিনাল সাউন্ড ও ভাইব্রেশন লজিক
    if (navigator.vibrate) navigator.vibrate([500, 100, 500]);
    document.body.classList.add('vibrate-screen'); 
    
    if(typeof lockedSound !== 'undefined' && lockedSound) {
        lockedSound.currentTime = 0;
        lockedSound.play();
    }

    setTimeout(() => {
        document.body.classList.remove('vibrate-screen');
        targetOverlay.style.display = "flex";
        
        let count = 5; 
        countNum.textContent = count; 

       // রিয়েল টাইম ভাইব্রেশনের জন্য এই আপডেট করা লজিকটি ব্যবহার করুন
let timer = setInterval(() => {
    count--;
    if(count > 0) {
        countNum.textContent = count;
        // রেডমি ফোনে কাজ করানোর জন্য প্যাটার্ন ভাইব্রেশন
        if (navigator.vibrate) {
            navigator.vibrate([1000, 50, 1000, 50, 1000, 50, 1000]); 
        }
    } else {
        clearInterval(timer);
        if (navigator.vibrate) navigator.vibrate(2000); 
        location.href = "https://t.me/+DlL7JBxnJQdjOTU1";
    }
    }, 1000);
    }, 4000);
  }
};

/* ================= CHOOSE ENGINE ================= */
function chooseEngine(type) {
  if (canSelectGame === false) return; // 

  // ১.SELECTED (DK/HZ selected)
  let selectedMsg = new SpeechSynthesisUtterance(type === "dk" ? "dk win selected" : "hznice selected");

  selectedMsg.onend = function() {
    const playAndStartTimer = () => {
      if(errorSound) {
        errorSound.currentTime = 0;
        errorSound.play().catch(()=>{});
        errorSound.onended = function() {
          console.log("Error sound finished. 29s timer started...");
          
          setTimeout(() => {
            liveBar.classList.add("show");
            startEngine();
            initPrediction();
            startTimer();
          }, 29000);
        };
      } else {       
        setTimeout(() => {
          liveBar.classList.add("show");
          startEngine();
          initPrediction();
          startTimer();
        }, 29000);
      }
      
      document.removeEventListener('click', playAndStartTimer);
      document.removeEventListener('touchstart', playAndStartTimer);
    };
    document.addEventListener('click', playAndStartTimer);
    document.addEventListener('touchstart', playAndStartTimer);
  };
  window.speechSynthesis.speak(selectedMsg);

  engineDomains = type === "dk" ? dkDomains : hzDomains;
  enginePath = type === "dk" ? "/#/register?invitationCode=63258962716" 
/*dk win☣️*/
                             : "/#/register?invitationCode=444451415893"; 
/*hznice ⛔*/

    choicePage.style.display = "none";
  vipFrame.style.display = "block";
  
  // এই লাইনটি এখানে ঢুকিয়ে দিন
  if(typeof globalViewportFix === 'function') globalViewportFix(); 
  
  loadDomain();
}

/* =========🏮 LOAD DOMAIN WITH SAFE RETRY 🏮============ */
function loadDomain() {
  if(!vipFrame || !engineDomains || engineDomains.length === 0) return;

  vipFrame.src = engineDomains[i] + enginePath;

  if(retryTimer) clearTimeout(retryTimer);

  retryTimer = setTimeout(() => {
    retries++;
    if(retries > maxRetries){
      alert("domains failed ");
      return;
    }
    i = (i + 1) % engineDomains.length;
    loadDomain();
  }, 6000);
}

vipFrame.onload = () => {
  if(retryTimer) clearTimeout(retryTimer);
};

/* ========= ADMIN AND TELIGRAM  BUTTONS VOICE ========== */

// ADMIN BOTOM
const adminBtn = document.querySelector('.admin-btn');
adminBtn.onclick = function() {
    speak("Admin connect");
    setTimeout(() => {
        window.open('https://t.me/owner_zihad_sir11', '_blank');
    }, 600); 
};
// TELIGRAM BOTOM
const telegramBtn = document.querySelector('.telegram-btn');
telegramBtn.onclick = function() {
    speak("Telegram connect");
    setTimeout(() => {
        window.open('https://t.me/+DlL7JBxnJQdjOTU1', '_blank');
    }, 600);
};

/* =================🔴 LIVE BAR 🔴================= */
["click","touchend"].forEach(e=>{liveBar.addEventListener(e,()=>location.reload());});

/* ================= FX TOGGLE (বন্ধ অবস্থা থেকে শুরু হবে) ================= */
fxToggle.onclick = () => {
    // যদি display 'none' থাকে (যা আমরা HTML-এ সেট করেছি), তবে 'block' হবে
    if (fxBody.style.display === "none") {
        fxBody.style.display = "block";
    } else {
        fxBody.style.display = "none";
    }
};

/*👑️===✅  ULTRA BEAST PREDICTION ENGINE (V8.0 FINAL)  ✅=== 👑️*/

const bigColors = ["#FFFFFF","#CDA0FF","#B19CD9","#A0D8EF","#90EE90","#FFFFA0","#FFB347","#FF7F7F","#87CEFA","#FF007F","#00FFEF","#CCFF00","#FFD700","#7B68EE","#FF4500","#ADFF2F","#FF69B4","#00FA9A","#F0E68C","#E6E6FA","#8A2BE2","#FF1493","#00BFFF"];
const smallColors = ["#CDA0FF","#FFFFFF","#B19CD9","#90EE90","#A0D8EF","#FFB347","#FF7F7F","#FFFFA0","#FF5E5E","#39FF14","#FFF01F","#BC13FE","#4D4DFF","#FF00FF","#08E8DE","#FFACEE","#BFFF00","#FFBF00","#9D00FF","#00FF7F","#FF44CC","#40E0D0"];

let history = [], rawNumbers = [];
let nextDisplay = "BIG", isWaitMode = false;
let hasSpoken = false, hasSynced = false, lastUsedColor = "";
let lossCount = 0; 

/* ================= 1. SPEAK FUNCTION (GLOBAL) ================= */
const speak = (text) => {
    if ('speechSynthesis' in window) {
        window.speechSynthesis.cancel(); 
        const utterance = new SpeechSynthesisUtterance(text);      
        utterance.rate = 1.0; utterance.pitch = 1.0; utterance.volume = 1.0; utterance.lang = 'en-US';
        window.speechSynthesis.speak(utterance);
    }
};

const getUniqueColor = (l) => {
    let c; do { c = l[Math.floor(Math.random() * l.length)]; } while (c === lastUsedColor);
    return lastUsedColor = c;
};

/* ================= 2. ALL BEAST ANALYSES LOGIC (V8.0) ================= */
const getBeastPrediction = (h, raw) => {
    if (h.length < 15) return Math.random() > 0.5 ? "BIG" : "SMALL";

    const last = h[0], prev = h[1], p2 = h[2], p3 = h[3];
    let aiScore = 0;

    // লজিক ১: SYMMETRY (আয়না প্যাটার্ন)
    if (h.slice(0, 5).join("") === h.slice(5, 10).join("")) aiScore += (last === "BIG" ? 2 : -2);

    // লজিক ২: RAW AVG (গাণিতিক গড়)
    const avgRaw = raw.slice(0, 5).reduce((a, b) => a + b, 0) / 5;
    aiScore += (avgRaw >= 5 ? 1.5 : -1.5);

    // লজিক ৩: DRAGON (টানা ট্রেন্ড)
    if (h.slice(0, 5).every(x => x === last)) return last;

    // লজিক ৪: TRIPLE BREAKER (টানা ৩টার পর ৪র্থ টি উল্টো)
    if (last === prev && prev === p2 && last !== p3) aiScore += (last === "BIG" ? -2.5 : 2.5);

    // লজিক ৫: PAIR LOGIC (জোড়া শনাক্তকরণ)
    if (last === prev && p2 === p3 && last !== p2) aiScore += (last === "BIG" ? 2 : -2);

    // লজিক ৬: RATIO REVERSION (মার্কেট ব্যালেন্স)
    const bigRatio = (h.slice(0, 30).filter(x => x === "BIG").length / 30) * 100;
    if (bigRatio > 65) aiScore -= 3; 
    if (bigRatio < 35) aiScore += 3;

    return aiScore >= 0 ? "BIG" : "SMALL";
};

/* ================= 3. API SYNC (FIXED CORS) ================= */
async function syncAndPredict() {
    if (hasSynced) return; 
    hasSynced = true; 
    
    try {
        const res = await fetch("https://www.gajarbotol.site/hack/30.php");
        const json = await res.json();
        const list = json?.data?.data?.list;
        const latest = Array.isArray(list) ? list[0] : list;
        
        if (latest) {
            const actual = parseInt(latest.number) >= 5 ? "BIG" : "SMALL";
            history.unshift(actual); 
            if (history.length > 20) history.pop();
        }
    } catch (e) { 
        console.log("Sync error: " + e.message); 
        hasSynced = false;
    }

    // ৫ লস বা জিগজ্যাগ প্যাটার্ন হলে WAIT
    isWaitMode = (lossCount >= 5);
    if (history.length >= 4) {
        const pattern = history.slice(0, 4).join("");
        if (pattern === "BIGSMALLBIGSMALL" || pattern === "SMALLBIGSMALLBIG") isWaitMode = true;
    }
    nextDisplay = isWaitMode ? "WAIT" : getBeastPrediction(history, rawNumbers);
}

/* ================= 5. MAIN ENGINE ================= */
function startEngine() {
    setInterval(() => {
        const now = new Date();
        const totalSec = now.getSeconds() % 30; 
        let displaySec = 30 - totalSec;
        const rt = document.getElementById("rt"), 
              clk = document.getElementById("clock"), 
              rs = document.getElementById("result"), 
              ld = document.getElementById("loader");
        if (clk) clk.textContent = now.toLocaleTimeString();
        if (rt) rt.textContent = (displaySec === 30) ? 0 : displaySec;
        if (displaySec === 29 && !hasSpoken) {
            updateUI(rs, nextDisplay); 
            setTimeout(() => {
                speak(nextDisplay === "WAIT" ? "Please wait" : `next prediction, ${nextDisplay}`);
            }, 300); 
            hasSpoken = true;
        }
        const isLoading = (displaySec >= 28 || displaySec <= 1);
        if (ld && rs) { 
            rs.style.display = isLoading ? "none" : "block"; 
            ld.style.display = isLoading ? "block" : "none"; 
        }

        if (totalSec === 2) {
            if (!hasSynced) { syncAndPredict(); hasSynced = true; }
        } else {
            hasSynced = false; 
            if (displaySec < 25) hasSpoken = false;
        }
    }, 500);
}
function updateUI(resDiv, display) {
    if (!resDiv) return;
    
    const clrList = (display === "BIG") ? bigColors : smallColors;
    const clr = (display === "WAIT") ? "#FF0000" : getUniqueColor(clrList);
    
    let isBig = (display.toUpperCase() === "BIG");
    let fontSizeClass = isBig ? "big" : "small";

    // লেখা পরিষ্কার করার জন্য শার্প শ্যাডো লজিক
    // এখানে 0 0 2px #fff অক্ষরের ধারগুলোকে সাদা এবং শার্প রাখবে
    let sharpStyle = `
        color: ${clr} !important;
        text-shadow: 0 0 2px #fff, 0 0 8px ${clr}; 
        font-weight: 900;
        letter-spacing: ${isBig ? '2px' : '1px'};
        -webkit-text-stroke: 0.5px rgba(255,255,255,0.5); /* হালকা সাদা স্ট্রোক */
        white-space: nowrap;
        line-height: 1;
        margin: 0;
        padding: 0;
        text-align: center;
    `;
    
    resDiv.innerHTML = `
    <div style="
        display: flex;   
        align-items: center;       
        justify-content: center;   
        width: 145px;            
        height: 48px;            
        background: rgba(0, 0, 0, 0.2); /* ব্যাকগ্রাউন্ড হালকা কালো যাতে লেখা ফুটে ওঠে */
        border-radius: 8px;
        border: 1px solid rgba(255, 255, 255, 0.2);
        margin: 2px auto;       
    ">
        <div class="result ${fontSizeClass}" style="${sharpStyle}">
            ${display}
        </div>
    </div>`;
}

// FX-BOX শ্যাডো এনিমেশন (আগের মতোই থাকবে)
const fb = document.querySelector('.fx-box');
if (fb) {
    const clrs = ['#FF3B3B','#38FF9C','#3B82FF','#FACC15','#FF85FF','#A855F7','#00D2FF','#F472B6'];
    let i = 0;
    fb.style.transition = "box-shadow 2.5s ease"; 
    setInterval(() => {
        const c = clrs[i++ % clrs.length];
        fb.style.boxShadow = `0 0 20px ${c}66, 0 0 40px ${c}33`;
    }, 1400);
}
/* ================= GLOBAL  ================= */
window.initPrediction = syncAndPredict;
window.syncAndPredict = syncAndPredict;
window.startTimer = startEngine;

document.addEventListener('click', () => { 
    speak("Hi trader");
    
}, { once: true });
window.selectGame = () => {
    startEngine();
    syncAndPredict();
};

/* ===== LIVE PERIOD 30 sec ===== */
function pad(n){return String(n).padStart(2,'0');}

function getCurrentWinGoPeriod(){
  const now = new Date();
  const utc6 = new Date(now.getTime() + 6 * 3600 * 1000);
  const dayStart = new Date(utc6); 
  dayStart.setUTCHours(6,0,0,0);
  
  let diffMs = utc6 - dayStart;
  let periodIndex = diffMs >= 0 ? Math.floor(diffMs/30000)+1 : Math.floor((diffMs+86400000)/30000)+1;
  
  if(periodIndex < 1) periodIndex = 1; 
  if(periodIndex > 2880) periodIndex = 2880;
  
  const y = utc6.getUTCFullYear(), m = pad(utc6.getUTCMonth()+1), d = pad(utc6.getUTCDate());
  return `${y}${m}${d}-${String(periodIndex).padStart(4,'0')}`;
}

(function liveWinGo(){
  const el = document.getElementById("dPeriod"); 
  
  // ৩০ সেকেন্ডের পিরিয়ড জেনারেট করে UI আপডেট
  const currentP = getCurrentWinGoPeriod();
  if(el) el.innerText = currentP;

  // পরবর্তী ৩০ সেকেন্ডের ঠিক শুরুর মুহূর্ত ক্যালকুলেশন
  const now = new Date();
  const ms = now.getMilliseconds();
  const sec = now.getSeconds() % 30; // ৩০ সেকেন্ডের ভাগশেষ (০০ বা ৩০ এর জন্য)
  
  // পরবর্তী ৩০ সেকেন্ডের মাথায় যেতে আর কত সময় বাকি (msUntilNext)
  const msUntilNext = (30 - sec) * 1000 - ms;

  // ঠিক ৩০ সেকেন্ড পর আবার রান হবে
  setTimeout(liveWinGo, msUntilNext + 10); 
})();


/* =================🖱️ DRAG FX BOX 🖱️================= */
let dragging=false,sx=0,sy=0,bx=0,by=0;
function startDrag(x,y){dragging=true;sx=x;sy=y;bx=box.offsetLeft;by=box.offsetTop;}
function moveDrag(x,y){if(!dragging)return;box.style.left=bx+(x-sx)+"px";box.style.top=by+(y-sy)+"px";}
box.addEventListener("mousedown",e=>startDrag(e.clientX,e.clientY));
window.addEventListener("mousemove",e=>moveDrag(e.clientX,e.clientY));
window.addEventListener("mouseup",()=>dragging=false);
box.addEventListener("touchstart",e=>{const t=e.touches[0];startDrag(t.clientX,t.clientY);});
window.addEventListener("touchmove",e=>{const t=e.touches[0];moveDrag(t.clientX,t.clientY);});
window.addEventListener("touchend",()=>dragging=false);

/* ================= 🎛️ CHROME & IFRAME KEYBOARD FIX (FINAL) 🎛️ ================= */
(function() {
  const loginSection = document.getElementById('loginBox');
  const iframeEl = document.getElementById("vipFrame");
  const choiceSection = document.getElementById("choicePage");

  function globalViewportFix() {
    // কিবোর্ডসহ বর্তমান দৃশ্যমান হাইট বের করা
    const vh = window.visualViewport ? window.visualViewport.height : window.innerHeight;
    
    // ১. ডাইনামিক ভেরিয়েবল আপডেট
    document.documentElement.style.setProperty("--vh", vh + "px");

    // ২. এলিমেন্টগুলোর হাইট ম্যানুয়ালি ফিক্স করা যেন কালো গ্যাপ না থাকে
    if (loginSection) {
        loginSection.style.height = vh + "px";
        // কিবোর্ড আসলে লগইন বক্সকে উপরে তোলা
        if (vh < window.innerHeight * 0.8) { 
            loginSection.style.justifyContent = "flex-start";
            loginSection.style.paddingTop = "15px";
        } else {
            loginSection.style.justifyContent = "center";
            loginSection.style.paddingTop = "0";
        }
    }

    if (iframeEl) iframeEl.style.height = vh + "px";
    if (choiceSection) choiceSection.style.height = vh + "px";
    
    // কিবোর্ড আসলে পেজ স্ক্রল রিসেট
    window.scrollTo(0, 0);
  }

  // ভিজ্যুয়াল ভিউপোর্ট লিসেনার
  if (window.visualViewport) {
    window.visualViewport.addEventListener("resize", globalViewportFix);
  }
  
  window.addEventListener("resize", globalViewportFix);
  
  // ইনপুট ফিল্ডে ফোকাস করলে ফিক্স কল করা
  document.querySelectorAll('input').forEach(input => {
    input.addEventListener('focus', () => setTimeout(globalViewportFix, 150));
    input.addEventListener('blur', globalViewportFix);
  });

  // আইফ্রেম লোড হওয়ার সাথে সাথে হাইট ফিক্স করা
  if(iframeEl) {
    iframeEl.addEventListener('load', globalViewportFix);
  }

  globalViewportFix(); // শুরুতে একবার রান হবে
})();


/* 
   ============================================================
   ULTIMATE LIVE STATUS MONITOR (SMOOTH SYNC ENGINE - FINAL)
   ============================================================ 
*/

// ১. এলিমেন্ট সিলেকশন
const netSpeedDisp = document.getElementById('net-speed');
const netKbsDisp = document.getElementById('net-kbs');
const userCountDisp = document.getElementById('online-users'); 
const errorOverlay = document.getElementById('zx-error-overlay');
const statusPod = document.getElementById('status-bar-zx');
const podToggle = document.getElementById('pod-toggle-zx');

let wasOffline = false; 

// ২. অফলাইন সাইরেন (Base64 Beep)
const backupErrorAudio = new Audio('data:audio/wav;base64,UklGRl9vT19XQVZFZm10IBAAAAABAAEAQB8AAEAfAAABAAgAZGF0YTdvT197e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3t7e3');
backupErrorAudio.loop = true;

// ৩. ভয়েস ইঞ্জিন
function systemSpeak(text) {
    if ('speechSynthesis' in window) {
        window.speechSynthesis.cancel(); 
        const msg = new SpeechSynthesisUtterance(text);
        msg.rate = 1.0; msg.pitch = 0.8; msg.lang = 'en-US';
        window.speechSynthesis.speak(msg);
    }
}

// ৪. ইউনিক ড্রাগ (Drag) এবং টগল (Toggle) লজিক
let isZxDragging = false;
let zxStartX, zxStartY, zxInitialL, zxInitialT;

// [শুরুতে বন্ধ রাখার ফাংশন]
function initPod() {
    if(statusPod) {
        statusPod.classList.add('pod-minimized');
        statusPod.style.width = "40px"; // ডিফল্ট বন্ধ
        if(podToggle) podToggle.innerText = '+';
    }
}

if(podToggle && statusPod) {
    podToggle.onclick = (e) => {
        e.stopPropagation();
        const isMin = statusPod.classList.toggle('pod-minimized');
        
        // ট্রানজিশন স্মুথ করার জন্য setTimeout ব্যবহার
        if(isMin) {
            statusPod.style.width = "40px";
            podToggle.innerText = "+";
        } else {
            statusPod.style.width = "270px"; // স্মুথলি বড় হবে
            podToggle.innerText = "×";
        }
    };
}

const zxStartMove = (e) => {
    if(e.target === podToggle) return;
    isZxDragging = true;
    const point = e.type.includes('touch') ? e.touches[0] : e;
    zxStartX = point.clientX;
    zxStartY = point.clientY;
    zxInitialL = statusPod.offsetLeft;
    zxInitialT = statusPod.offsetTop;
    statusPod.style.transition = 'none'; // ড্রাগ করার সময় অ্যানিমেশন বন্ধ
};

const zxDuringMove = (e) => {
    if (!isZxDragging) return;
    const point = e.type.includes('touch') ? e.touches[0] : e;
    let newX = zxInitialL + (point.clientX - zxStartX);
    let newY = zxInitialT + (point.clientY - zxStartY);

    newX = Math.max(0, Math.min(window.innerWidth - statusPod.offsetWidth, newX));
    newY = Math.max(0, Math.min(window.innerHeight - statusPod.offsetHeight, newY));

    statusPod.style.left = newX + 'px';
    statusPod.style.top = newY + 'px';
};

const zxStopMove = () => {
    isZxDragging = false;
    // ড্রাগ ছাড়ার পর অ্যানিমেশন আবার চালু
    statusPod.style.transition = 'width 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275), opacity 0.3s ease';
};

statusPod.addEventListener('mousedown', zxStartMove);
window.addEventListener('mousemove', zxDuringMove);
window.addEventListener('mouseup', zxStopMove);
statusPod.addEventListener('touchstart', zxStartMove, {passive: false});
window.addEventListener('touchmove', zxDuringMove, {passive: false});
window.addEventListener('touchend', zxStopMove);

// ৫. রিয়েল-টাইম সিস্টেম স্ট্যাটাস আপডেট
function updateSystemStats() {
    if (navigator.onLine) {
        if (wasOffline) {
            wasOffline = false;
            backupErrorAudio.pause();
            if (typeof lockedSound !== 'undefined') lockedSound.pause();
            systemSpeak("Connection Restored.");
            setTimeout(() => location.reload(), 1000); 
            return;
        }

        if(errorOverlay) errorOverlay.style.display = 'none';
        document.body.classList.remove('is-offline');

        const conn = navigator.connection || navigator.mozConnection || navigator.webkitConnection;
        let rawMbps = (conn && conn.downlink > 0) ? conn.downlink : (Math.random() * 1.5 + 1.2);
        let mbps = (rawMbps + (Math.random() * 0.4 - 0.2)).toFixed(2);
        
        if(netSpeedDisp) netSpeedDisp.innerText = mbps;
        if(netKbsDisp) netKbsDisp.innerText = Math.floor(mbps * 128) + '/' + Math.floor(mbps * 90);
        
        if(userCountDisp) {
            let current = parseInt(userCountDisp.innerText) || 221;
            userCountDisp.innerText = Math.max(150, current + (Math.floor(Math.random() * 3) - 1));
        }
    } else {
        if (!wasOffline) {
            wasOffline = true;
            systemSpeak("Connection lost.");
            if (typeof lockedSound !== 'undefined' && lockedSound) {
                lockedSound.play().catch(() => {});
            } else {
                backupErrorAudio.play().catch(() => {});
            }
        }
        if(errorOverlay) errorOverlay.style.display = 'flex';
        document.body.classList.add('is-offline');
    }
}

// ৬. ইনিশিয়ালাইজেশন
setInterval(updateSystemStats, 1000);
document.addEventListener('click', () => { 
    if (navigator.onLine) systemSpeak("System ready.");
}, { once: true });

window.addEventListener('online', updateSystemStats);
window.addEventListener('offline', updateSystemStats);

// রান
initPod();
updateSystemStats();

</script>
</body>
</html>
