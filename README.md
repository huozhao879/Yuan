<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
  <meta name="theme-color" content="#070313">
  <meta name="description" content="Huo Zhao — Official Links">
  <title>Huo Zhao • Official Links</title>

  <style>
    :root{
      --bg:#05030d;
      --panel:rgba(13,10,29,.72);
      --panel-2:rgba(22,17,43,.55);
      --text:#fff;
      --muted:#aaa5bd;
      --purple:#9c6cff;
      --violet:#d5b7ff;
      --cyan:#54e7ff;
      --line:rgba(255,255,255,.12);
      --shadow:rgba(0,0,0,.55);
      --mx:50%;
      --my:30%;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      min-height:100svh;
      overflow-x:hidden;
      color:var(--text);
      font-family:Inter,ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial,sans-serif;
      background:
        radial-gradient(circle at var(--mx) var(--my),rgba(130,76,255,.19),transparent 25rem),
        radial-gradient(circle at 8% 92%,rgba(35,193,255,.12),transparent 24rem),
        radial-gradient(circle at 92% 12%,rgba(170,68,255,.13),transparent 22rem),
        linear-gradient(145deg,#03020a 0%,#0a0616 48%,#03040b 100%);
    }

    body::before{
      content:"";
      position:fixed;
      inset:0;
      z-index:-3;
      pointer-events:none;
      opacity:.22;
      background-image:
        linear-gradient(rgba(255,255,255,.035) 1px,transparent 1px),
        linear-gradient(90deg,rgba(255,255,255,.035) 1px,transparent 1px);
      background-size:42px 42px;
      mask-image:linear-gradient(to bottom,black,transparent 88%);
    }

    body::after{
      content:"";
      position:fixed;
      inset:-30%;
      z-index:-4;
      pointer-events:none;
      background:
        conic-gradient(from 180deg at 50% 50%,transparent,rgba(122,71,255,.08),transparent 25%,rgba(57,207,255,.05),transparent 55%);
      filter:blur(70px);
      animation:ambient 18s linear infinite;
    }

    a{color:inherit}
    button{font:inherit}

    .scene{
      position:fixed;
      inset:0;
      overflow:hidden;
      pointer-events:none;
      z-index:-1;
    }

    .orb{
      position:absolute;
      width:28rem;
      height:28rem;
      border-radius:50%;
      filter:blur(85px);
      opacity:.18;
      mix-blend-mode:screen;
    }
    .orb.one{left:-16rem;top:-13rem;background:#7a3dff;animation:orbOne 12s ease-in-out infinite}
    .orb.two{right:-17rem;bottom:-14rem;background:#19b9e8;animation:orbTwo 15s ease-in-out infinite}
    .orb.three{left:45%;top:40%;background:#d05cff;opacity:.07;animation:orbThree 10s ease-in-out infinite}

    .stars,.dust{position:absolute;inset:0}
    .star{
      position:absolute;
      width:2px;height:2px;
      border-radius:50%;
      background:#fff;
      box-shadow:0 0 9px rgba(211,190,255,.8);
      animation:twinkle var(--dur) ease-in-out infinite;
      animation-delay:var(--delay);
    }

    .dust i{
      position:absolute;
      bottom:-20px;
      width:3px;height:3px;
      border-radius:50%;
      background:#d9c8ff;
      box-shadow:0 0 14px rgba(175,125,255,.9);
      animation:rise var(--dur) linear infinite;
      animation-delay:var(--delay);
    }

    .wrap{
      width:min(100%,620px);
      margin:auto;
      padding:22px 16px 30px;
      position:relative;
    }

    .card{
      position:relative;
      isolation:isolate;
      overflow:hidden;
      border:1px solid rgba(212,190,255,.18);
      border-radius:34px;
      padding:30px 18px 21px;
      background:
        linear-gradient(145deg,rgba(29,20,55,.83),rgba(5,5,16,.83) 72%),
        radial-gradient(circle at 50% 0,rgba(174,120,255,.15),transparent 38%);
      backdrop-filter:blur(24px) saturate(135%);
      -webkit-backdrop-filter:blur(24px) saturate(135%);
      box-shadow:
        0 35px 100px var(--shadow),
        inset 0 1px rgba(255,255,255,.10),
        0 0 0 1px rgba(120,72,255,.04);
      transform:perspective(1100px) rotateX(var(--rx,0deg)) rotateY(var(--ry,0deg));
      transition:transform .18s ease-out,box-shadow .35s ease;
      animation:cardIn .9s cubic-bezier(.2,.8,.2,1) both;
    }

    .card::before{
      content:"";
      position:absolute;
      inset:-2px;
      z-index:-1;
      border-radius:36px;
      padding:1px;
      background:conic-gradient(from 0deg,transparent 0 25%,rgba(175,122,255,.65),transparent 42% 68%,rgba(65,215,255,.35),transparent 82%);
      -webkit-mask:linear-gradient(#000 0 0) content-box,linear-gradient(#000 0 0);
      -webkit-mask-composite:xor;
      mask-composite:exclude;
      animation:borderSpin 9s linear infinite;
    }

    .card::after{
      content:"";
      position:absolute;
      inset:0;
      z-index:-1;
      pointer-events:none;
      background:linear-gradient(115deg,transparent 20%,rgba(222,199,255,.12) 45%,transparent 60%);
      transform:translateX(-120%);
      animation:shine 6s ease-in-out infinite;
    }

    .top-line{
      width:90px;height:3px;
      margin:0 auto 22px;
      border-radius:99px;
      background:linear-gradient(90deg,transparent,var(--violet),var(--cyan),transparent);
      box-shadow:0 0 18px rgba(166,105,255,.8);
      animation:linePulse 2.8s ease-in-out infinite;
    }

    .hero{text-align:center}

    .logo-wrap{
      width:142px;
      height:142px;
      margin:0 auto 12px;
      display:grid;
      place-items:center;
      position:relative;
      animation:logoFloat 4s ease-in-out infinite;
    }

    .logo-halo{
      position:absolute;
      width:136px;height:136px;
      border-radius:50%;
      background:radial-gradient(circle,rgba(165,108,255,.22),transparent 64%);
      filter:blur(8px);
    }

    .logo-ring{
      position:absolute;
      width:122px;height:122px;
      border-radius:50%;
      border:1px solid rgba(218,198,255,.28);
      box-shadow:0 0 40px rgba(140,86,255,.22),inset 0 0 25px rgba(152,103,255,.08);
      animation:spin 14s linear infinite;
    }

    .logo-ring::before,.logo-ring::after{
      content:"";
      position:absolute;
      inset:9px;
      border-radius:50%;
      border:1px dashed rgba(217,197,255,.24);
    }
    .logo-ring::after{
      inset:23px;
      border-style:solid;
      border-color:rgba(255,255,255,.12);
      animation:spinReverse 8s linear infinite;
    }

    .logo-mark{
      width:82px;height:82px;
      display:grid;
      place-items:center;
      position:relative;
      border-radius:27px;
      border:1px solid rgba(255,255,255,.20);
      background:linear-gradient(145deg,rgba(171,125,255,.34),rgba(54,29,111,.62));
      box-shadow:0 16px 45px rgba(89,51,180,.35),inset 0 1px rgba(255,255,255,.2);
      transform:rotate(45deg);
    }

    .logo-mark span{
      display:block;
      transform:rotate(-45deg);
      font-family:"Noto Serif SC","Songti SC","STSong",serif;
      font-size:52px;
      line-height:1;
      font-weight:900;
      background:linear-gradient(180deg,#fff 0%,#e3cfff 42%,#8b62ff 100%);
      -webkit-background-clip:text;
      background-clip:text;
      color:transparent;
      filter:drop-shadow(0 0 15px rgba(187,140,255,.75));
    }

    .logo-spark{
      position:absolute;
      width:7px;height:7px;
      border-radius:50%;
      background:#fff;
      box-shadow:0 0 14px 5px rgba(181,127,255,.7);
    }
    .spark-a{top:13px;right:11px;animation:spark 2.1s ease-in-out infinite}
    .spark-b{bottom:18px;left:7px;animation:spark 2.6s .5s ease-in-out infinite}

    .badge{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding:7px 11px;
      margin:0 auto 13px;
      border:1px solid rgba(203,179,255,.2);
      border-radius:999px;
      background:rgba(255,255,255,.045);
      color:#cfc3e9;
      font-size:10px;
      font-weight:700;
      letter-spacing:.20em;
      text-transform:uppercase;
      box-shadow:inset 0 1px rgba(255,255,255,.06);
    }

    .status-dot{
      width:6px;height:6px;border-radius:50%;
      background:#79f2c0;
      box-shadow:0 0 12px #79f2c0;
      animation:status 1.8s ease-in-out infinite;
    }

    h1{
      margin:0;
      font-size:clamp(34px,8vw,46px);
      line-height:1;
      letter-spacing:-.045em;
      font-weight:850;
      text-shadow:0 4px 35px rgba(143,91,255,.22);
    }

    .sub{
      margin:10px 0 0;
      color:#c8b5ec;
      font-size:11px;
      font-weight:700;
      letter-spacing:.36em;
      text-transform:uppercase;
    }

    .desc{
      max-width:430px;
      margin:15px auto 27px;
      color:#aaa6b9;
      font-size:13px;
      line-height:1.7;
    }

    .divider{
      display:flex;
      align-items:center;
      gap:10px;
      margin:0 10px 18px;
      color:#887aa0;
      font-size:9px;
      letter-spacing:.25em;
      text-transform:uppercase;
    }
    .divider::before,.divider::after{
      content:"";
      height:1px;
      flex:1;
      background:linear-gradient(90deg,transparent,rgba(197,170,255,.22));
    }
    .divider::after{background:linear-gradient(90deg,rgba(197,170,255,.22),transparent)}

    .links{
      display:grid;
      gap:12px;
    }

    .link{
      --accent:#b28cff;
      --accent-soft:rgba(178,140,255,.15);
      min-height:78px;
      display:flex;
      align-items:center;
      gap:14px;
      padding:11px 13px 11px 12px;
      position:relative;
      overflow:hidden;
      isolation:isolate;
      text-decoration:none;
      border:1px solid rgba(255,255,255,.10);
      border-radius:22px;
      background:linear-gradient(110deg,rgba(255,255,255,.065),rgba(255,255,255,.025));
      box-shadow:inset 0 1px rgba(255,255,255,.055),0 10px 30px rgba(0,0,0,.12);
      transition:transform .25s ease,border-color .25s ease,box-shadow .25s ease,background .25s ease;
      animation:linkIn .65s cubic-bezier(.2,.8,.2,1) both;
    }
    .link:nth-child(1){animation-delay:.25s}
    .link:nth-child(2){animation-delay:.35s}
    .link:nth-child(3){animation-delay:.45s}

 
