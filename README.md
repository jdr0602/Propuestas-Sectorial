# Propuestas-Sectorial
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Propuestas Estratégicas — CIIU 0141</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Crimson+Pro:ital,wght@0,300;0,400;0,600;1,300&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
:root{
  --azul:#0D2137;--azul-med:#1A3A5C;--azul-clr:#2E6DA4;
  --azul-glass:rgba(13,33,55,0.65);
  --verde:#4A5E35;--verde-clr:#7A9A50;--verde-suave:#B8CFA0;
  --dorado:#C9A84C;--dorado-clr:#E8C86A;--dorado-suave:#F5E4B0;
  --crema:#F7F3EC;--gris:#8A9BB0;--gris-clr:#4A5568;
  --blanco:#FFFFFF;--negro:#0A0E14;
  --rojo:#C0392B;--verde-ok:#27AE60;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'Crimson Pro',Georgia,serif;background:var(--azul);color:var(--blanco);overflow-x:hidden;}

/* ── ANIMACIONES ── */
@keyframes fadeUp{from{opacity:0;transform:translateY(28px);}to{opacity:1;transform:translateY(0);}}
@keyframes pulse{from{opacity:.6;transform:scale(1);}to{opacity:1;transform:scale(1.05);}}
@keyframes gridFade{from{opacity:0;}to{opacity:1;}}
@keyframes fillBar{from{width:0;}to{width:var(--fill);}}
@keyframes countUp{from{opacity:0;}to{opacity:1;}}
@keyframes shimmer{0%{background-position:-400px 0;}100%{background-position:400px 0;}}

/* ══ PORTADA ══ */
.portada{min-height:100vh;background:linear-gradient(145deg,#070F1B 0%,var(--azul) 40%,#0F2D1A 100%);display:flex;flex-direction:column;align-items:center;justify-content:center;position:relative;overflow:hidden;padding:60px 40px;}
.portada-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(201,168,76,.05) 1px,transparent 1px),linear-gradient(90deg,rgba(201,168,76,.05) 1px,transparent 1px);background-size:70px 70px;animation:gridFade 4s ease both;}
.glow{position:absolute;border-radius:50%;filter:blur(80px);animation:pulse 6s ease-in-out infinite alternate;}
.g1{width:500px;height:300px;background:rgba(201,168,76,.08);top:10%;left:-10%;}
.g2{width:400px;height:400px;background:rgba(74,94,53,.10);bottom:5%;right:0%;}
.g3{width:300px;height:200px;background:rgba(46,109,164,.08);top:40%;left:50%;}

.p-badge{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:4px;color:var(--dorado);text-transform:uppercase;border:1px solid rgba(201,168,76,.35);padding:7px 22px;margin-bottom:28px;position:relative;z-index:2;animation:fadeUp .8s ease both;}
.p-title{font-family:'Playfair Display',serif;font-size:clamp(32px,5vw,64px);font-weight:900;text-align:center;line-height:1.08;position:relative;z-index:2;max-width:960px;animation:fadeUp .8s .15s ease both;}
.p-title .gold{color:var(--dorado-clr);font-style:italic;}
.p-sub{font-family:'Crimson Pro',serif;font-size:19px;font-weight:300;color:var(--verde-suave);text-align:center;margin-top:18px;letter-spacing:1px;position:relative;z-index:2;animation:fadeUp .8s .3s ease both;}
.p-divider{width:100px;height:2px;background:linear-gradient(90deg,transparent,var(--dorado),transparent);margin:30px auto;position:relative;z-index:2;animation:fadeUp .8s .4s ease both;}

.idx-pills{display:flex;gap:14px;flex-wrap:wrap;justify-content:center;position:relative;z-index:2;animation:fadeUp .8s .5s ease both;}
.idx-pill{background:rgba(255,255,255,.05);border:1px solid rgba(201,168,76,.22);border-radius:3px;padding:12px 20px;text-align:center;backdrop-filter:blur(10px);transition:transform .3s,box-shadow .3s;}
.idx-pill:hover{transform:translateY(-4px);box-shadow:0 16px 40px rgba(0,0,0,.4);}
.idx-pill .val{font-family:'Space Mono',monospace;font-size:22px;font-weight:700;color:var(--dorado-clr);}
.idx-pill .lbl{font-size:11px;color:var(--gris);letter-spacing:1px;margin-top:3px;}
.idx-pill .st{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;color:var(--verde-suave);margin-top:2px;text-transform:uppercase;}

.p-meta{display:flex;gap:48px;flex-wrap:wrap;justify-content:center;margin-top:36px;position:relative;z-index:2;animation:fadeUp .8s .6s ease both;}
.p-meta-item{text-align:center;}
.pm-val{font-family:'Playfair Display',serif;font-size:30px;font-weight:900;color:var(--dorado-clr);}
.pm-lbl{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;color:var(--gris);text-transform:uppercase;margin-top:4px;}

/* ══ SECCIÓN LABEL GENÉRICO ══ */
.sec{padding:70px 40px;max-width:1200px;margin:0 auto;}
.sec-tag{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:3px;color:var(--dorado);text-transform:uppercase;display:flex;align-items:center;gap:12px;margin-bottom:10px;}
.sec-tag::before{content:'';display:inline-block;width:24px;height:1px;background:var(--dorado);}
.sec-title{font-family:'Playfair Display',serif;font-size:32px;font-weight:700;margin-bottom:8px;}
.sec-sub{font-size:16px;color:var(--gris);font-weight:300;margin-bottom:36px;}

/* ══ PROBLEMAS ══ */
.prob-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:14px;margin-bottom:50px;}
.prob-card{background:rgba(192,57,43,.08);border:1px solid rgba(192,57,43,.2);border-radius:3px;padding:18px 16px;position:relative;overflow:hidden;transition:transform .3s;}
.prob-card:hover{transform:translateY(-3px);}
.prob-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,var(--rojo),rgba(192,57,43,.3));}
.prob-num{font-family:'Space Mono',monospace;font-size:28px;font-weight:700;color:rgba(192,57,43,.4);line-height:1;}
.prob-title{font-size:14px;font-weight:600;color:rgba(255,255,255,.85);margin-top:8px;line-height:1.3;}
.prob-stat{font-family:'Space Mono',monospace;font-size:11px;color:var(--rojo);margin-top:8px;}

/* ══ KPI PANORAMA ══ */
.kpi-pan{background:rgba(0,0,0,.25);border-top:1px solid rgba(201,168,76,.12);border-bottom:1px solid rgba(201,168,76,.12);padding:50px 40px;}
.kpi-inner{max-width:1200px;margin:0 auto;}
.kpi-row{display:grid;grid-template-columns:repeat(5,1fr);gap:20px;}
.kpi-box{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.07);border-radius:3px;padding:22px 20px;backdrop-filter:blur(8px);transition:border-color .3s,box-shadow .3s;}
.kpi-box:hover{border-color:rgba(201,168,76,.25);box-shadow:0 8px 30px rgba(0,0,0,.3);}
.kpi-lbl{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;color:var(--gris);text-transform:uppercase;margin-bottom:8px;}
.kpi-cur{font-family:'Playfair Display',serif;font-size:32px;font-weight:900;color:var(--dorado-clr);line-height:1;}
.kpi-tgt{font-family:'Space Mono',monospace;font-size:13px;color:var(--verde-suave);margin-top:4px;}
.kpi-delta{font-family:'Space Mono',monospace;font-size:11px;margin-top:6px;}
.up{color:var(--verde-ok);font-weight:700;}
.dn{color:var(--rojo);font-weight:700;}
.pb{width:100%;height:4px;background:rgba(255,255,255,.08);border-radius:2px;margin-top:10px;overflow:hidden;}
.pf{height:100%;border-radius:2px;animation:fillBar 1.5s ease both;animation-delay:.5s;}
.fg{background:linear-gradient(90deg,var(--dorado),var(--dorado-clr));}
.fv{background:linear-gradient(90deg,var(--verde),var(--verde-clr));}
.fb{background:linear-gradient(90deg,var(--azul-med),var(--azul-clr));}

/* ══ PROPUESTAS ══ */
.props-sec{padding:70px 40px;max-width:1200px;margin:0 auto;}

.prop-card{background:linear-gradient(135deg,rgba(255,255,255,.04) 0%,rgba(255,255,255,.01) 100%);border:1px solid rgba(255,255,255,.07);border-radius:3px;padding:50px;margin-bottom:52px;position:relative;overflow:hidden;backdrop-filter:blur(6px);transition:transform .35s,box-shadow .35s;animation:fadeUp .7s ease both;}
.prop-card:hover{transform:translateY(-4px);box-shadow:0 24px 70px rgba(0,0,0,.45);}
.prop-card:nth-child(1){animation-delay:.1s;}
.prop-card:nth-child(2){animation-delay:.2s;}
.prop-card:nth-child(3){animation-delay:.3s;}
.prop-card::before{content:'';position:absolute;left:0;top:0;bottom:0;width:4px;}
.prop-card::after{content:'';position:absolute;top:-60px;right:-60px;width:220px;height:220px;border-radius:50%;opacity:.04;}
.c1::before{background:linear-gradient(180deg,var(--dorado),var(--verde-clr));}
.c1::after{background:var(--dorado);}
.c2::before{background:linear-gradient(180deg,var(--azul-clr),var(--dorado));}
.c2::after{background:var(--azul-clr);}
.c3::before{background:linear-gradient(180deg,var(--verde-clr),var(--azul-clr));}
.c3::after{background:var(--verde-clr);}

/* Header de prop */
.ph{display:grid;grid-template-columns:auto 1fr auto;gap:24px;align-items:start;margin-bottom:36px;}
.ph-icon{width:68px;height:68px;border-radius:3px;display:flex;align-items:center;justify-content:center;font-size:30px;flex-shrink:0;}
.c1 .ph-icon{background:rgba(201,168,76,.12);border:1px solid rgba(201,168,76,.25);}
.c2 .ph-icon{background:rgba(46,109,164,.12);border:1px solid rgba(46,109,164,.25);}
.c3 .ph-icon{background:rgba(122,154,80,.12);border:1px solid rgba(122,154,80,.25);}
.ph-tag{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:3px;text-transform:uppercase;margin-bottom:8px;}
.c1 .ph-tag{color:var(--dorado);}
.c2 .ph-tag{color:#7BB8E8;}
.c3 .ph-tag{color:var(--verde-suave);}
.ph-title{font-family:'Playfair Display',serif;font-size:26px;font-weight:700;line-height:1.15;}
.ph-hz{background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.09);border-radius:3px;padding:10px 18px;text-align:center;flex-shrink:0;}
.hz-lbl{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;color:var(--gris);text-transform:uppercase;}
.hz-val{font-family:'Space Mono',monospace;font-size:13px;font-weight:700;margin-top:4px;}
.c1 .hz-val{color:var(--dorado-clr);}
.c2 .hz-val{color:#7BB8E8;}
.c3 .hz-val{color:var(--verde-suave);}

/* Objetivo SMART */
.smart-lbl{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;color:var(--gris);text-transform:uppercase;margin-bottom:6px;}
.smart-box{background:rgba(0,0,0,.2);border:1px solid rgba(255,255,255,.06);border-radius:3px;padding:20px 24px 20px 36px;margin-bottom:26px;font-size:16px;line-height:1.7;color:rgba(255,255,255,.88);font-weight:300;position:relative;}
.smart-box::before{content:'';position:absolute;left:16px;top:50%;transform:translateY(-50%);width:6px;height:6px;border-radius:50%;}
.c1 .smart-box::before{background:var(--dorado);}
.c2 .smart-box::before{background:#7BB8E8;}
.c3 .smart-box::before{background:var(--verde-suave);}

/* Grid descripción */
.desc-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-bottom:26px;}
.db{background:rgba(0,0,0,.18);border:1px solid rgba(255,255,255,.05);border-radius:3px;padding:20px 22px;}
.db-lbl{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2.5px;text-transform:uppercase;margin-bottom:10px;display:flex;align-items:center;gap:8px;}
.db-lbl::before{content:'';display:inline-block;width:14px;height:1px;}
.c1 .db-lbl{color:var(--dorado);}
.c1 .db-lbl::before{background:var(--dorado);}
.c2 .db-lbl{color:#7BB8E8;}
.c2 .db-lbl::before{background:#7BB8E8;}
.c3 .db-lbl{color:var(--verde-suave);}
.c3 .db-lbl::before{background:var(--verde-suave);}
.db-txt{font-size:15px;line-height:1.68;color:rgba(255,255,255,.80);font-weight:300;}

/* Antes vs Después */
.avd-title{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:3px;text-transform:uppercase;color:var(--gris);margin-bottom:16px;display:flex;align-items:center;gap:10px;}
.avd-title::after{content:'';flex:1;height:1px;background:rgba(255,255,255,.07);}
.avd-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:28px;}
.avd-card{border-radius:3px;padding:16px;text-align:center;position:relative;overflow:hidden;}
.avd-card.antes{background:rgba(192,57,43,.08);border:1px solid rgba(192,57,43,.2);}
.avd-card.desp{background:rgba(39,174,96,.08);border:1px solid rgba(39,174,96,.2);}
.avd-ind{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--gris);margin-bottom:8px;}
.avd-va{font-family:'Space Mono',monospace;font-size:20px;font-weight:700;color:var(--rojo);}
.avd-vd{font-family:'Space Mono',monospace;font-size:20px;font-weight:700;color:var(--verde-ok);}
.avd-desc{font-size:11px;color:rgba(255,255,255,.5);margin-top:4px;}
.avd-arrow{font-size:18px;margin-top:4px;}

/* Tags indicadores */
.ind-row{display:flex;gap:10px;flex-wrap:wrap;align-items:center;margin-bottom:24px;}
.ind-lbl-t{font-family:'Space Mono',monospace;font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--gris);}
.ind-tag{font-family:'Space Mono',monospace;font-size:11px;font-weight:700;padding:5px 14px;border-radius:2px;}
.c1 .ind-tag{background:rgba(201,168,76,.14);color:var(--dorado-clr);border:1px solid rgba(201,168,76,.22);}
.c2 .ind-tag{background:rgba(46,109,164,.14);color:#7BB8E8;border:1px solid rgba(46,109,164,.28);}
.c3 .ind-tag{background:rgba(122,154,80,.14);color:var(--verde-suave);border:1px solid rgba(122,154,80,.22);}

/* KPI impacto */
.ki-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;}
.ki-box{background:rgba(0,0,0,.25);border:1px solid rgba(255,255,255,.06);border-radius:3px;padding:14px 16px;text-align:center;}
.ki-val{font-family:'Space Mono',monospace;font-size:22px;font-weight:700;line-height:1;}
.c1 .ki-val{color:var(--dorado-clr);}
.c2 .ki-val{color:#7BB8E8;}
.c3 .ki-val{color:var(--verde-suave);}
.ki-desc{font-size:12px;color:var(--gris);margin-top:6px;line-height:1.3;}

/* ══ ÍNDICES IMPACTO ══ */
.idx-sec{background:rgba(0,0,0,.2);border-top:1px solid rgba(201,168,76,.1);border-bottom:1px solid rgba(201,168,76,.1);padding:70px 40px;}
.idx-inner{max-width:1200px;margin:0 auto;}
.idx-cards{display:grid;grid-template-columns:repeat(5,1fr);gap:16px;margin-top:40px;}
.idx-card{background:rgba(255,255,255,.04);border:1px solid rgba(255,255,255,.07);border-radius:3px;padding:26px 20px;text-align:center;transition:transform .3s,box-shadow .3s;}
.idx-card:hover{transform:translateY(-5px);box-shadow:0 16px 50px rgba(0,0,0,.4);}
.idx-name{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:2px;text-transform:uppercase;color:var(--gris);margin-bottom:16px;}
.idx-before{font-family:'Space Mono',monospace;font-size:13px;color:rgba(192,57,43,.9);margin-bottom:6px;}
.idx-now{font-family:'Playfair Display',serif;font-size:38px;font-weight:900;color:var(--dorado-clr);line-height:1;}
.idx-delta{font-family:'Space Mono',monospace;font-size:12px;color:var(--verde-ok);margin-top:8px;}
.idx-cat{font-family:'Space Mono',monospace;font-size:9px;text-transform:uppercase;letter-spacing:1px;margin-top:6px;}
.idx-bar{width:100%;height:5px;background:rgba(255,255,255,.07);border-radius:3px;margin-top:14px;overflow:hidden;}
.idx-fill{height:100%;border-radius:3px;animation:fillBar 1.8s ease both;animation-delay:.8s;}
.b-gold{background:linear-gradient(90deg,var(--dorado),var(--dorado-clr));}
.b-green{background:linear-gradient(90deg,var(--verde),var(--verde-clr));}
.b-blue{background:linear-gradient(90deg,var(--azul-med),var(--azul-clr));}

/* ══ TABLA VARIABLES ══ */
.vars-sec{padding:70px 40px;max-width:1200px;margin:0 auto;}
.var-table{border:1px solid rgba(255,255,255,.07);border-radius:3px;overflow:hidden;}
.vt-hdr{display:grid;grid-template-columns:2fr 1fr 1fr 1fr 1fr;background:rgba(201,168,76,.08);padding:16px 24px;font-family:'Space Mono',monospace;font-size:10px;letter-spacing:2px;text-transform:uppercase;color:var(--gris);}
.vt-row{display:grid;grid-template-columns:2fr 1fr 1fr 1fr 1fr;padding:16px 24px;border-top:1px solid rgba(255,255,255,.04);align-items:center;transition:background .2s;}
.vt-row:hover{background:rgba(255,255,255,.03);}
.vn{font-size:15px;font-weight:400;color:rgba(255,255,255,.85);}
.vp{font-family:'Space Mono',monospace;font-size:12px;color:var(--gris);}
.va{font-family:'Space Mono',monospace;font-size:13px;color:rgba(192,57,43,.9);}
.ve{font-family:'Space Mono',monospace;font-size:13px;color:var(--verde-ok);}
.vc{font-family:'Space Mono',monospace;font-size:13px;font-weight:700;}
.cu{color:var(--verde-ok);}
.cd{color:var(--rojo);}

/* ══ FOOTER ══ */
.footer-sec{background:linear-gradient(135deg,rgba(0,0,0,.35),rgba(10,20,35,.4));border-top:1px solid rgba(201,168,76,.15);padding:60px 40px;text-align:center;}
.f-title{font-family:'Playfair Display',serif;font-size:24px;font-weight:700;color:var(--dorado);margin-bottom:18px;}
.f-text{font-size:16px;color:var(--gris);max-width:800px;margin:0 auto;line-height:1.78;font-weight:300;}
.f-ius{margin:40px auto 0;display:inline-block;background:rgba(201,168,76,.08);border:1px solid rgba(201,168,76,.25);border-radius:3px;padding:22px 48px;}
.ius-lbl{font-family:'Space Mono',monospace;font-size:10px;letter-spacing:3px;color:var(--gris);text-transform:uppercase;}
.ius-val{font-family:'Playfair Display',serif;font-size:52px;font-weight:900;color:var(--dorado-clr);line-height:1;margin:4px 0;}
.ius-cat{font-family:'Space Mono',monospace;font-size:12px;letter-spacing:2px;color:var(--verde-suave);text-transform:uppercase;}
.f-meta{margin-top:36px;font-family:'Space Mono',monospace;font-size:10px;letter-spacing:2px;color:rgba(138,155,176,.4);text-transform:uppercase;}

/* Separador */
.sep{width:100%;height:1px;background:linear-gradient(90deg,transparent,rgba(201,168,76,.18),transparent);margin:8px 0 56px;}

/* Responsive */
@media(max-width:900px){
  .prob-grid,.kpi-row,.idx-cards{grid-template-columns:1fr 1fr;}
  .desc-grid{grid-template-columns:1fr;}
  .avd-grid,.ki-grid{grid-template-columns:1fr 1fr;}
  .ph{grid-template-columns:auto 1fr;gap:16px;}
  .ph-hz{grid-column:1/-1;width:fit-content;}
  .vt-hdr,.vt-row{grid-template-columns:1.5fr 1fr 1fr 1fr;}
  .vp{display:none;}
}
@media(max-width:600px){
  .prop-card{padding:30px 24px;}
  .idx-cards{grid-template-columns:1fr 1fr;}
  .idx-now{font-size:28px;}
}
</style>
</head>
<body>

<!-- ════════════════════ PORTADA ════════════════════ -->
<section class="portada">
  <div class="portada-grid"></div>
  <div class="glow g1"></div>
  <div class="glow g2"></div>
  <div class="glow g3"></div>

  <div class="p-badge">Diagnóstico Sectorial · Colombia · Vigencia 2025–2030</div>

  <h1 class="p-title">
    Propuestas <span class="gold">Estratégicas</span><br>
    CIIU 0141 — Ganadería Bovina y Bufalina
  </h1>

  <p class="p-sub">Competitividad · Sostenibilidad Financiera · Eficiencia Operativa · Innovación Agroindustrial</p>
  <div class="p-divider"></div>

  <div class="idx-pills">
    <div class="idx-pill">
      <div class="val">3.68</div>
      <div class="lbl">ISS — Salud Sectorial</div>
      <div class="st">ESTADO BUENO</div>
    </div>
    <div class="idx-pill">
      <div class="val">3.78</div>
      <div class="lbl">IAS — Atractivo</div>
      <div class="st">ESTADO BUENO</div>
    </div>
    <div class="idx-pill">
      <div class="val">3.026</div>
      <div class="lbl">IPS — Prospectiva</div>
      <div class="st">ESTADO BUENO</div>
    </div>
    <div class="idx-pill">
      <div class="val">2.911</div>
      <div class="lbl">ICS — Competitividad</div>
      <div class="st">ESTADO BUENO
        
      </div>
    </div>
    <div class="idx-pill">
      <div class="val">3.48</div>
      <div class="lbl">IUS — Unificado</div>
      <div class="st">ESTADO BUENO</div>
    </div>
  </div>

  <div class="p-meta">
    <div class="p-meta-item">
      <div class="pm-val">2020–24</div>
      <div class="pm-lbl">Período analizado</div>
    </div>
    <div class="p-meta-item">
      <div class="pm-val">3</div>
      <div class="pm-lbl">Propuestas estratégicas</div>
    </div>
    <div class="p-meta-item">
      <div class="pm-val">4</div>
      <div class="pm-lbl">Problemas estructurales</div>
    </div>
    <div class="p-meta-item">
      <div class="pm-val">→3.85</div>
      <div class="pm-lbl">IUS proyectado</div>
    </div>
  </div>
</section>

<!-- ════════════════════ PROBLEMAS ════════════════════ -->
<div class="sec">
  <div class="sec-tag">Diagnóstico base</div>
  <h2 class="sec-title">Identificados</h2>
  <p class="sec-sub">Período 2020–2024 · Sector CIIU 0141 · Cría de Ganado Bovino y Bufalino en Colombia</p>

  <div class="prob-grid">
    <div class="prob-card">
      <div class="prob-num">01</div>
      <div class="prob-title">Altos costos financieros por tasas de interés elevadas</div>
      <div class="prob-stat">Costos financieros +58.1% en 2022–23</div>
    </div>
    <div class="prob-card">
      <div class="prob-num">02</div>
      <div class="prob-title">Período promedio de inventarios elevado</div>
      <div class="prob-stat">65.4 días en 2020-2024 </div>
    </div>
    <div class="prob-card">
      <div class="prob-num">03</div>
      <div class="prob-title">Rotación de cartera estructuralmente alta</div>
      <div class="prob-stat">PCC ~ 161 
         días promedio del período</div>
    </div>
    <div class="prob-card">
      <div class="prob-num">04</div>
      <div class="prob-title">Presión sobre márgenes operativos y rentabilidad</div>
      <div class="prob-stat">Utilidad neta −73.38
        % en 2023</div>
    </div>
  </div>
</div>

<!-- ════════════════════ KPI PANORAMA ════════════════════ -->
<div class="kpi-pan">
  <div class="kpi-inner">
    <div class="sec-tag" style="margin-bottom:8px;">Estado financiero actual</div>
    <h2 class="sec-title" style="font-size:26px;margin-bottom:28px;">Indicadores Financieros — Punto de Partida 2024</h2>
    <div class="kpi-row">
      <div class="kpi-box">
        <div class="kpi-lbl">ROE Actual</div>
        <div class="kpi-cur">4.01%</div>
        <div class="kpi-tgt">Objetivo: <span style="color:var(--dorado-clr)">6.78%</span></div>
        <div class="kpi-delta up">↑ +3.0 pp proyectado</div>
        <div class="pb"><div class="pf fg" style="--fill:52%;"></div></div>
      </div>
      <div class="kpi-box">
        <div class="kpi-lbl">ROA Actual</div>
        <div class="kpi-cur">2.80%</div>
        <div class="kpi-tgt">Objetivo: <span style="color:var(--dorado-clr)">4.80%</span></div>
        <div class="kpi-delta up">↑ +2.0 pp proyectado</div>
        <div class="pb"><div class="pf fg" style="--fill:45%;"></div></div>
      </div>
      <div class="kpi-box">
        <div class="kpi-lbl">PCC — Días Cartera</div>
        <div class="kpi-cur">~161 d </div>
        <div class="kpi-tgt">Objetivo: <span style="color:var(--verde-suave)">90–120d</span></div>
        <div class="kpi-delta up">↓ −60 días proyectado</div>
        <div class="pb"><div class="pf fv" style="--fill:35%;"></div></div>
      </div>
      <div class="kpi-box">
        <div class="kpi-lbl">Margen Neto</div>
        <div class="kpi-cur">14,00%</div>
        <div class="kpi-tgt">Objetivo: <span style="color:var(--dorado-clr)">17,15%</span></div>
        <div class="kpi-delta up">↑ +3.5 pp proyectado</div>
        <div class="pb"><div class="pf fg" style="--fill:65%;"></div></div>
      </div>
      <div class="kpi-box">
        <div class="kpi-lbl">Ciclo de Caja</div>
        <div class="kpi-cur">60,25d</div>
        <div class="kpi-tgt">Objetivo: <span style="color:var(--verde-suave)">&lt;45d</span></div>
        <div class="kpi-delta up">↓ −25% proyectado</div>
        <div class="pb"><div class="pf fv" style="--fill:55%;"></div></div>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════ PROPUESTAS ════════════════════ -->
<div class="props-sec">
  <div class="sec-tag">Soluciones estratégicas</div>
  <h2 class="sec-title">Las Tres Propuestas Estratégicas</h2>
  <p class="sec-sub">Diseñadas a partir del diagnóstico financiero y sectorial del período 2020–2024 del CIIU 0141</p>

  <!-- ── PROPUESTA 1 ── -->
  <div class="prop-card c1">
    <div class="ph">
      <div class="ph-icon">🌿</div>
      <div>
        <div class="ph-tag">Propuesta 01 · Financiero-Ambiental</div>
        <h3 class="ph-title">Refinanciamiento Verde y Bonos de Carbono Ganadero</h3>
      </div>
      <div class="ph-hz">
        <div class="hz-lbl">Horizonte</div>
        <div class="hz-val">MEDIANO</div>
        <div style="font-size:9px;color:var(--gris);margin-top:2px;">2–4 años</div>
      </div>
    </div>

    <div class="smart-lbl">Objetivo SMART</div>
    <div class="smart-box c1">
      Reducir en <strong>mínimo el 30% los costos financieros del sector</strong> en un horizonte de 3 años, mediante la migración progresiva de la deuda comercial a tasa variable hacia créditos verdes, líneas especiales de crédito (LEC) de Finagro y mecanismos de bonos de carbono en mercados voluntarios certificados, buscando una tasa efectiva por debajo del 10% anual alineada con el ciclo biológico de producción bovina de 18 a 36 meses.
    </div>

    <div class="desc-grid">
      <div class="db c1">
        <div class="db-lbl">Problema que resuelve</div>
        <div class="db-txt">Los costos financieros del sector CIIU 0141 crecieron un 76.3% entre 2022 y 2023, producto del ciclo alcista del Banco de la República que elevó la tasa de política monetaria al 13%. El sector financia su ciclo productivo —cuyo horizonte biológico es de 18 a 36 meses— con crédito comercial de corto plazo a tasas variables, generando una exposición estructural a la política monetaria que en un único ejercicio destruyó el 73.4% de la utilidad neta. El IPS de 3.026 refleja directamente esta presión sobre el entorno financiero prospectivo del sector.</div>
      </div>
      <div class="db c1">
        <div class="db-lbl">Estrategia de implementación</div>
        <div class="db-txt">Implementar modelos certificados de ganadería sostenible y sistemas silvopastoriles para acceder a: (i) créditos verdes y líneas LEC de Finagro con tasas preferenciales del 5%–8% anual; (ii) bonos de carbono en mercados voluntarios con precios de USD 15–35 por tonelada de CO₂ equivalente capturada, que actúen como cobertura ante choques de tasas; (iii) compra y refinanciación de cartera de deuda comercial existente hacia instrumentos de largo plazo alineados con el ciclo productivo bovino, reduciendo la presión de renovaciones frecuentes en contextos de tasas altas.</div>
      </div>
    </div>

    <div class="avd-title">Comparativo Antes → Después</div>
    <div class="avd-grid">
      <div class="avd-card antes">
        <div class="avd-ind">Costos Financieros</div>
        <div class="avd-va">+58,10%</div>
        <div class="avd-desc">Variación 2022–2023</div>
        <div class="avd-arrow">⬆️</div>
      </div>
      <div class="avd-card desp">
        <div class="avd-ind">Costos Financieros</div>
        <div class="avd-vd">−30%</div>
        <div class="avd-desc">Objetivo año 3</div>
        <div class="avd-arrow">⬇️</div>
      </div>
      <div class="avd-card antes">
        <div class="avd-ind">ROE Sectorial</div>
        <div class="avd-va">4.01%</div>
        <div class="avd-desc">Valor actual 2024</div>
        <div class="avd-arrow">📊</div>
      </div>
      <div class="avd-card desp">
        <div class="avd-ind">ROE Proyectado</div>
        <div class="avd-vd">6.78%</div>
        <div class="avd-desc">+2.77 pp con propuesta</div>
        <div class="avd-arrow">📈</div>
      </div>
    </div>

    <div class="ind-row c1">
      <span class="ind-lbl-t">Variables impactadas:</span>
      <span class="ind-tag">Costos financieros ↓ −30%</span>
      <span class="ind-tag">Endeudamiento ↓</span>
      <span class="ind-tag">Margen Neto ↑ +3.5pp</span>
      <span class="ind-tag">ROE ↑ +2.5pp</span>
      <span class="ind-tag">ROA ↑ +1.8pp</span>
      <span class="ind-tag">IPS ↑ 3.026→3.70</span>
      <span class="ind-tag">ISS ↑ 3.68→3.95</span>
    </div>

    <div class="ki-grid c1">
      <div class="ki-box">
        <div class="ki-val">−30%</div>
        <div class="ki-desc">Reducción costos financieros anuales (año 3)</div>
      </div>
      <div class="ki-box">
        <div class="ki-val">ISS→3.95</div>
        <div class="ki-desc">ISS mejora de 3.68 a 3.95 · +7.3%</div>
      </div>
      <div class="ki-box">
        <div class="ki-val">IPS→3.70</div>
        <div class="ki-desc">IPS mejora de 3.026 a 3.70 · +17.8%</div>
      </div>
    </div>
  </div>

  <div class="sep"></div>

  <!-- ── PROPUESTA 2 ── -->
  <div class="prop-card c2">
    <div class="ph">
      <div class="ph-icon">🤝</div>
      <div>
        <div class="ph-tag">Propuesta 02 · Comercial-Operativa</div>
        <h3 class="ph-title">Integración Comercial y Acuerdos Directos con Frigoríficos y Productores Lácteos</h3>
      </div>
      <div class="ph-hz">
        <div class="hz-lbl">Horizonte</div>
        <div class="hz-val">CORTO-MED</div>
        <div style="font-size:9px;color:var(--gris);margin-top:2px;">1–3 años</div>
      </div>
    </div>

    <div class="smart-lbl">Objetivo SMART</div>
    <div class="smart-box c2">
      Reducir el <strong>período promedio de inventarios en mínimo un 25%</strong> y disminuir los gastos de venta sobre ingresos al <strong>3%</strong> en un plazo máximo de 3 años, mediante la estructuración de ruedas de negocio y contratos de suministro directo que garanticen ventas anticipadas, optimicen la planeación productiva y eliminen la cadena de intermediación comercial no eficiente que encarece la comercialización del ganado bovino en Colombia.
    </div>

    <div class="desc-grid">
      <div class="db c2">
        <div class="db-lbl">Problema que resuelve</div>
        <div class="db-txt">El período de inventarios del sector pasó de 48.8 días en 2022 a 89.1 días en 2024, con inventarios corrientes que crecieron un 104.6% en el último año del período analizado. Simultáneamente, los gastos de venta alcanzaron el 7.7% de los ingresos en 2021 como consecuencia directa de la dependencia de ferias ganaderas, subastas físicas y comisionistas que absorben una fracción desproporcionada del precio final al productor. Esta estructura genera tiempos improductivos de permanencia del ganado que elevan el costo de oportunidad y presionan el ICS, que promedió 2.911 durante el período.</div>
      </div>
      <div class="db c2">
        <div class="db-lbl">Estrategia de implementación</div>
        <div class="db-txt">Generar ruedas de negocio departamentales y acuerdos marco de suministro directo entre productores del CIIU 0141, frigoríficos certificados y empresas lácteas con el propósito de: (i) garantizar ventas anticipadas con precio base y ajuste trimestral por indicadores de mercado; (ii) mejorar la planeación del ciclo productivo reduciendo los tiempos de permanencia improductiva del ganado; (iii) distribuir costos de transporte y logística entre múltiples productores agrupados en asociaciones regionales; (iv) disminuir los riesgos climáticos y logísticos mediante contratos de entrega escalonada que suavicen la presión sobre el inventario.</div>
      </div>
    </div>

    <div class="avd-title">Comparativo Antes → Después</div>
    <div class="avd-grid">
      <div class="avd-card antes">
        <div class="avd-ind">Período Inventarios</div>
        <div class="avd-va">69 días</div>
        <div class="avd-desc">Valor 2024</div>
        <div class="avd-arrow">⬆️</div>
      </div>
      <div class="avd-card desp">
        <div class="avd-ind">Período Inventarios</div>
        <div class="avd-vd">~67 días</div>
        <div class="avd-desc">Objetivo −25% (año 3)</div>
        <div class="avd-arrow">⬇️</div>
      </div>
      <div class="avd-card antes">
        <div class="avd-ind">Gastos de Venta</div>
        <div class="avd-va">3.00%</div>
        <div class="avd-desc">% sobre ingresos 2024</div>
        <div class="avd-arrow">⬆️</div>
      </div>
      <div class="avd-card desp">
        <div class="avd-ind">Gastos de Venta</div>
        <div class="avd-vd">2.8%</div>
        <div class="avd-desc">Objetivo año 3</div>
        <div class="avd-arrow">⬇️</div>
      </div>
    </div>

    <div class="ind-row c2">
      <span class="ind-lbl-t">Variables impactadas:</span>
      <span class="ind-tag">Inventarios ↓ −25%</span>
      <span class="ind-tag">Rot. activos ↑ +0.03x</span>
      <span class="ind-tag">Gastos venta ↓ −2pp</span>
      <span class="ind-tag">ROA ↑</span>
      <span class="ind-tag">ROE ↑</span>
      <span class="ind-tag">ICS ↑ 2.911→3.45</span>
      <span class="ind-tag">IUS ↑ 3.48→3.85</span>
    </div>

    <div class="ki-grid c2">
      <div class="ki-box">
        <div class="ki-val">−25%</div>
        <div class="ki-desc">Reducción período promedio de inventarios</div>
      </div>
      <div class="ki-box">
        <div class="ki-val">ICS→3.45</div>
        <div class="ki-desc">ICS mejora de 2.911 a 3.45 · +18.5%</div>
      </div>
      <div class="ki-box">
        <div class="ki-val">IUS→3.85</div>
        <div class="ki-desc">IUS mejora de 3.48 a 3.85 · +10.6%</div>
      </div>
    </div>
  </div>

  <div class="sep"></div>

  <!-- ── PROPUESTA 3 ── -->
  <div class="prop-card c3">
    <div class="ph">
      <div class="ph-icon">🏦</div>
      <div>
        <div class="ph-tag">Propuesta 03 · Financiero-Gremial</div>
        <h3 class="ph-title">Política Gremial de Cartera Inteligente con Acuerdos de Pago Sectorial</h3>
      </div>
      <div class="ph-hz">
        <div class="hz-lbl">Horizonte</div>
        <div class="hz-val">CORTO</div>
        <div style="font-size:9px;color:var(--gris);margin-top:2px;">1–2 años</div>
      </div>
    </div>

    <div class="smart-lbl">Objetivo SMART</div>
    <div class="smart-box c3">
      Reducir el <strong>período de cobro de cartera (PCC) desde aproximadamente 170 días hasta un rango de 90–120 días</strong> en un horizonte de 2 años, mediante la implementación de acuerdos gremiales vinculantes que establezcan condiciones mínimas de pago del 40% de contado, cartera máxima de 90 días y esquemas de descuento por pronto pago, fortaleciendo la liquidez corriente del sector en al menos 0.5 veces y reduciendo el ciclo de caja en un 40%.
    </div>

    <div class="desc-grid">
      <div class="db c3">
        <div class="db-lbl">Problema que resuelve</div>
        <div class="db-txt">El período de cobro de cartera del sector alcanzó 253.7 días en 2020 y se mantuvo en torno a 170 días como promedio estructural del período analizado, generando un ciclo de caja que llegó a 115 días en 2023. Esta situación obliga al sector a recurrir a financiamiento externo para cubrir necesidades operativas precisamente cuando los costos financieros son más elevados, creando un círculo vicioso de endeudamiento que erosiona la rentabilidad. El ISS de 3.68 refleja que la liquidez, pese a ser razonable, no está siendo aprovechada eficientemente por la lentitud estructural en el recaudo de cartera.</div>
      </div>
      <div class="db c3">
        <div class="db-lbl">Estrategia de implementación</div>
        <div class="db-txt">Implementar acuerdos gremiales articulados por Fedegán y las asociaciones departamentales donde: (i) los frigoríficos paguen mínimo el 40% de contado al momento de la entrega del ganado; (ii) el saldo restante tenga plazo máximo de 90 días con garantías reales verificadas; (iii) se apliquen descuentos por pronto pago del 2%–3% para compradores que cancelen en los primeros 30 días; (iv) se estructure acceso a factoring agropecuario que permita anticipar hasta el 80% del valor de la factura a tasa preferencial, aliviando la presión sobre el capital de trabajo operativo sin necesidad de nuevo endeudamiento.</div>
      </div>
    </div>

    <div class="avd-title">Comparativo Antes → Después</div>
    <div class="avd-grid">
      <div class="avd-card antes">
        <div class="avd-ind">PCC — Días Cartera</div>
        <div class="avd-va">~161 días</div>
        <div class="avd-desc">Promedio estructural</div>
        <div class="avd-arrow">⬆️</div>
      </div>
      <div class="avd-card desp">
        <div class="avd-ind">PCC Proyectado</div>
        <div class="avd-vd">90–120d</div>
        <div class="avd-desc">Objetivo año 2</div>
        <div class="avd-arrow">⬇️</div>
      </div>
      <div class="avd-card antes">
        <div class="avd-ind">Razón Corriente</div>
        <div class="avd-va">2.48x</div>
        <div class="avd-desc">Promedio período</div>
        <div class="avd-arrow">📊</div>
      </div>
      <div class="avd-card desp">
        <div class="avd-ind">Liquidez Proyectada</div>
        <div class="avd-vd">3.51x</div>
        <div class="avd-desc">+0.5x con propuesta</div>
        <div class="avd-arrow">📈</div>
      </div>
    </div>

    <div class="ind-row c3">
      <span class="ind-lbl-t">Variables impactadas:</span>
      <span class="ind-tag">Rot. cartera ↑ ↑</span>
      <span class="ind-tag">Ciclo de caja ↓ −40%</span>
      <span class="ind-tag">Liquidez ↑ +0.5x</span>
      <span class="ind-tag">Capital trabajo ↑</span>
      <span class="ind-tag">ISS ↑ 3.68→4.0</span>
      <span class="ind-tag">ICS ↑ 2.911→3.40</span>
    </div>

    <div class="ki-grid c3">
      <div class="ki-box">
        <div class="ki-val">−60d</div>
        <div class="ki-desc">Reducción PCC objetivo (año 2)</div>
      </div>
      <div class="ki-box">
        <div class="ki-val">ISS→4.0</div>
        <div class="ki-desc">ISS supera umbral Saludable (de 3.68)</div>
      </div>
      <div class="ki-box">
        <div class="ki-val">ICS→3.40</div>
        <div class="ki-desc">ICS sube de 2.911 a 3.40 · +16.8%</div>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════ IMPACTO EN ÍNDICES ════════════════════ -->
<div class="idx-sec">
  <div class="idx-inner">
    <div class="sec-tag">Impacto consolidado</div>
    <h2 class="sec-title">Proyección de Índices Sectoriales</h2>
    <p class="sec-sub">Implementación simultánea de las tres propuestas estratégicas · Horizonte 2027–2028</p>

    <div class="idx-cards">
      <div class="idx-card">
        <div class="idx-name">ISS · Salud Sectorial</div>
        <div class="idx-before">Actual: 3.68</div>
        <div class="idx-now">4.0</div>
        <div class="idx-delta up">↑ +0.32 pts (+8.7%)</div>
        <div class="idx-cat" style="color:var(--verde-suave);">Saludable</div>
        <div class="idx-bar"><div class="idx-fill b-gold" style="--fill:80%;"></div></div>
      </div>
      <div class="idx-card">
        <div class="idx-name">IAS · Atractivo</div>
        <div class="idx-before">Actual: 3.78</div>
        <div class="idx-now">3.90</div>
        <div class="idx-delta up">↑ +0.12 pts (+3.2%)</div>
        <div class="idx-cat" style="color:#7BB8E8;">Mod. Atractivo</div>
        <div class="idx-bar"><div class="idx-fill b-blue" style="--fill:78%;"></div></div>
      </div>
      <div class="idx-card">
        <div class="idx-name">IPS · Prospectiva</div>
        <div class="idx-before">Actual: 3.026</div>
        <div class="idx-now">3.70</div>
        <div class="idx-delta up">↑ +0.56 pts (+17.8%)</div>
        <div class="idx-cat" style="color:var(--verde-suave);">Mod. Saludable</div>
        <div class="idx-bar"><div class="idx-fill b-green" style="--fill:74%;"></div></div>
      </div>
      <div class="idx-card">
        <div class="idx-name">ICS · Competitividad</div>
        <div class="idx-before">Actual: 2.911</div>
        <div class="idx-now">3.45</div>
        <div class="idx-delta up">↑ +0.54 pts (+18.5%)</div>
        <div class="idx-cat" style="color:var(--dorado-clr);">Mod. Saludable</div>
        <div class="idx-bar"><div class="idx-fill b-gold" style="--fill:69%;"></div></div>
      </div>
      <div class="idx-card">
        <div class="idx-name">IUS · Unificado</div>
        <div class="idx-before">Actual: 3.48</div>
        <div class="idx-now">3.85</div>
        <div class="idx-delta up">↑ +0.37 pts (+10.6%)</div>
        <div class="idx-cat" style="color:var(--dorado-clr);">Bueno</div>
        <div class="idx-bar"><div class="idx-fill b-gold" style="--fill:77%;"></div></div>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════ TABLA VARIABLES ════════════════════ -->
<div class="vars-sec">
  <div class="sec-tag">Variables financieras</div>
  <h2 class="sec-title">Impacto sobre Indicadores Financieros Clave</h2>
  <p class="sec-sub">Comparativo actual vs. proyectado con implementación de las tres propuestas estratégicas</p>

  <div class="var-table">
    <div class="vt-hdr">
      <span>Variable Financiera</span>
      <span>Propuesta</span>
      <span>Valor Actual</span>
      <span>Valor Esperado</span>
      <span>Variación</span>
    </div>
    <div class="vt-row">
      <span class="vn">ROE — Retorno sobre Patrimonio</span>
      <span class="vp">P1 · P2</span>
      <span class="va">4.01%</span>
      <span class="ve">6.78%</span>
      <span class="vc cu">↑ +2.77 pp</span>
    </div>
    <div class="vt-row">
      <span class="vn">ROA — Retorno sobre Activos</span>
      <span class="vp">P1 · P2</span>
      <span class="va">2.80%</span>
      <span class="ve">4.80%</span>
      <span class="vc cu">↑ +2.00 pp</span>
    </div>
    <div class="vt-row">
      <span class="vn">Margen Neto sobre Ventas</span>
      <span class="vp">P1</span>
      <span class="va">14,00%</span>
      <span class="ve">17,15%</span>
      <span class="vc cu">↑ +3.5 pp</span>
    </div>
    <div class="vt-row">
      <span class="vn">Período de Cobro de Cartera (PCC)</span>
      <span class="vp">P3</span>
      <span class="va">~161 días</span>
      <span class="ve">90–120 días</span>
      <span class="vc cu">↓ −60 días</span>
    </div>
    <div class="vt-row">
      <span class="vn">Rotación de Inventarios</span>
      <span class="vp">P2</span>
      <span class="va">65,4 días</span>
      <span class="ve">~47 días</span>
      <span class="vc cu">↓ −28,13%</span>
    </div>
    <div class="vt-row">
      <span class="vn">Razón Corriente — Liquidez</span>
      <span class="vp">P3</span>
      <span class="va">3.056x</span>
      <span class="ve">3.51x</span>
      <span class="vc cu">↑ + 16,36%</span>
    </div>
    <div class="vt-row">
      <span class="vn">Rotación de Activos Totales</span>
      <span class="vp">P2</span>
      <span class="va">0.20x</span>
      <span class="ve">0.15x</span>
      <span class="vc cu">↑ -5 PP</span>
    </div>
    <div class="vt-row">
      <span class="vn">Gastos de Venta / Ingresos</span>
      <span class="vp">P2</span>
      <span class="va">3.00%</span>
      <span class="ve">4.20%</span>
      <span class="vc cu">↓ −1.20 pp</span>
    </div>
    <div class="vt-row">
      <span class="vn">Nivel de Endeudamiento Total</span>
      <span class="vp">P1</span>
      <span class="va">30.03%</span>
      <span class="ve">&lt;26.00%</span>
      <span class="vc cu">↓ −4.03 pp</span>
    </div>
    </div>
</div>

<!-- ════════════════════ CONCLUSIÓN ════════════════════ -->
<div class="footer-sec">
  <div class="f-title">Conclusión Estratégica — CIIU 0141 · Ganadería Bovina Colombia</div>
  <p class="f-text">
    Las tres propuestas estratégicas actúan de manera sistémica y complementaria sobre las vulnerabilidades estructurales identificadas en el diagnóstico financiero y sectorial del período 2020–2024. La <strong style="color:var(--dorado-clr)">Propuesta 1 — Refinanciamiento Verde</strong> ataca el costo de capital reduciendo la exposición a tasas variables mediante créditos verdes y bonos de carbono. La <strong style="color:#7BB8E8">Propuesta 2 — Integración Comercial</strong> transforma la cadena de comercialización, reduciendo el período de inventarios en un 25% y los gastos de venta al 3% de los ingresos. La <strong style="color:var(--verde-suave)">Propuesta 3 — Cartera Inteligente</strong> resuelve el problema estructural del período de cobro, fortaleciendo la liquidez en 0.5 veces y reduciendo el ciclo de caja en un 40%. Implementadas en conjunto en el horizonte 2025–2028, estas propuestas tienen el potencial de elevar el IUS sectorial del 3.48 actual a la categoría <strong style="color:var(--dorado-clr)">Bueno (3.85)</strong>, consolidando al CIIU 0141 como un sector financieramente sólido, operativamente eficiente y estratégicamente competitivo en el panorama agropecuario colombiano.
  </p>

  <div class="f-ius">
    <div class="ius-lbl">IUS Proyectado · Implementación de las 3 Propuestas</div>
    <div class="ius-val">3.85</div>
    <div class="ius-cat">Categoría: Bueno · ↑ +10.6% vs. actual (3.48)</div>
  </div>

  <div class="f-meta">CIIU 0141 · Cría de Ganado Bovino y Bufalino · Colombia · Diagnóstico Sectorial 2025</div>
</div>

</body>
</html>
