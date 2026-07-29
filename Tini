<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>for you</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&family=Caveat:wght@500;700&family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400&family=UnifrakturMaguntia&family=Pirata+One&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #07060a;
    --rose: #ff8fa3;
    --rose-dim: #7a3a4a;
    --gold: #f0c987;
    --cream: #fdf3ec;
    --crimson: #b3123f;
  }
  *{ margin:0; padding:0; box-sizing:border-box; }
  html,body{
    background: var(--bg);
    color: var(--cream);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
    width: 100%;
    height: 100%;
  }
  #rain{
    position: fixed;
    top:0; left:0;
    width:100%; height:100%;
    z-index: 1;
    display:block;
  }

  /* ---------- INTRO SEQUENCE ---------- */
  #intro{
    position: fixed;
    inset:0;
    z-index: 5;
    display:flex;
    align-items:center;
    justify-content:center;
    pointer-events:none;
  }
  #intro-word{
    position: relative;
    font-family: 'Pirata One', 'UnifrakturMaguntia', cursive;
    font-weight: 400;
    background: linear-gradient(120deg, var(--cream) 0%, var(--gold) 45%, var(--rose) 75%, var(--cream) 100%);
    background-size: 300% auto;
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    filter: drop-shadow(0 0 14px rgba(255,143,163,0.65)) drop-shadow(0 0 46px rgba(179,18,63,0.4));
    letter-spacing: 0.01em;
    opacity: 0;
    transform: scale(0.85);
    text-align:center;
    padding: 0 6vw;
  }
  #intro-word.count{
    font-size: clamp(6rem, 26vw, 15rem);
  }
  #intro-word.word{
    font-size: clamp(3.4rem, 13vw, 7.5rem);
  }

  /* ---------- FLOWER COUNTDOWN ---------- */
  #intro-flower{
    display: none;
    position: relative;
    width: 42vw;
    max-width: 220px;
    aspect-ratio: 1;
  }
  #intro-flower.show{ display: block; }
  .flower-center{
    position: absolute;
    top: 50%; left: 50%;
    width: 14%; height: 14%;
    margin: -7% 0 0 -7%;
    border-radius: 50%;
    background: radial-gradient(circle, var(--gold), var(--rose));
    box-shadow: 0 0 26px rgba(255,143,163,0.85), 0 0 60px rgba(179,18,63,0.4);
  }
  .petal-slot{
    position: absolute;
    inset: 0;
  }
  .petal-slot[data-i="0"]{ transform: rotate(0deg); }
  .petal-slot[data-i="1"]{ transform: rotate(120deg); }
  .petal-slot[data-i="2"]{ transform: rotate(240deg); }
  .petal-pos{
    position: absolute;
    top: 50%; left: 50%;
    width: 22%;
    height: 50%;
    transform: translate(-50%, -100%);
  }
  .petal-shape{
    width: 100%;
    height: 100%;
    background: linear-gradient(180deg, var(--cream) 0%, var(--rose) 55%, rgba(255,111,145,0.4) 100%);
    border-radius: 50% 50% 50% 50% / 65% 65% 35% 35%;
    box-shadow: 0 0 18px rgba(255,143,163,0.6);
    opacity: 1;
  }
  .petal-shape.fallen{
    animation: petalFall 1.3s ease-in forwards;
  }
  @keyframes petalFall{
    0%   { transform: translate(0,0) rotate(0deg); opacity: 1; }
    100% { transform: translate(15%, 140%) rotate(80deg); opacity: 0; }
  }

  /* ---------- I LOVE YOU HEART FIELD ---------- */
  #heart-layer{
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    pointer-events: none;
    opacity: 0;
    transition: opacity 0.7s ease;
  }
  #heart-layer.show{ opacity: 1; }

  #heart-stage{
    position: relative;
    width: 450px;
    height: 450px;
    transform: scale(var(--heart-scale, 1));
  }

  .love{
    position: absolute;
    top: 50%;
    left: 50%;
    margin: -225px 0 0 -225px;
  }

  .love_word{
    color: var(--rose);
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 1rem;
    letter-spacing: 2px;
    white-space: nowrap;
    text-shadow: 0 0 10px rgba(253,243,236,0.9), 0 0 18px rgba(255,143,163,0.6);
    transform: translateY(-100%) rotate(-30deg);
  }

  .love_horizontal{
    animation: heartHorizontal 10s infinite alternate ease-in-out;
    animation-delay: calc(var(--i) * -300ms);
  }

  .love_vertical{
    animation: heartVertical 20s infinite linear;
    animation-delay: calc(var(--i) * -300ms);
  }

  @keyframes heartHorizontal{
    from{ transform: translateX(0); }
    to{ transform: translateX(450px); }
  }

  @keyframes heartVertical{
    0%{ transform: translateY(180px); }
    10%{ transform: translateY(45px); }
    15%{ transform: translateY(4.5px); }
    18%{ transform: translateY(0); }
    20%{ transform: translateY(4.5px); }
    22%{ transform: translateY(34.61538px); }
    24%{ transform: translateY(64.28571px); }
    25%{ transform: translateY(112.5px); }
    26%{ transform: translateY(64.28571px); }
    28%{ transform: translateY(34.61538px); }
    30%{ transform: translateY(4.5px); }
    32%{ transform: translateY(0); }
    35%{ transform: translateY(4.5px); }
    40%{ transform: translateY(45px); }
    50%{ transform: translateY(180px); }
    71%{ transform: translateY(428.57143px); }
    72.5%{ transform: translateY(441.17647px); }
    75%{ transform: translateY(450px); }
    77.5%{ transform: translateY(441.17647px); }
    79%{ transform: translateY(428.57143px); }
    100%{ transform: translateY(180px); }
  }
  #intro-word.show{
    animation: introPop 0.95s cubic-bezier(.2,.9,.25,1) forwards, introShimmer 0.95s linear forwards;
  }
  #intro-word::before,
  #intro-word::after{
    content: attr(data-text);
    position:absolute;
    left:0; top:0; width:100%;
    background: none;
    -webkit-background-clip: initial;
    background-clip: initial;
    opacity:0;
    pointer-events:none;
  }
  #intro-word.show::before{
    color: var(--gold);
    clip-path: inset(0 0 55% 0);
    animation: glitchTop 0.6s cubic-bezier(.2,.9,.25,1) forwards;
  }
  #intro-word.show::after{
    color: var(--rose);
    clip-path: inset(55% 0 0 0);
    animation: glitchBottom 0.6s cubic-bezier(.2,.9,.25,1) forwards;
  }
  @keyframes introPop{
    0%   { opacity:0; transform: scale(0.7) skewX(10deg); filter: blur(8px); }
    28%  { opacity:1; transform: scale(1.08) skewX(-5deg); filter: blur(0); }
    45%  { opacity:1; transform: scale(1) skewX(0deg); }
    65%  { opacity:1; transform: scale(1); }
    100% { opacity:0; transform: scale(1.14); filter: blur(2px); }
  }
  @keyframes introShimmer{
    0%{ background-position: 0% center; }
    100%{ background-position: 180% center; }
  }
  @keyframes glitchTop{
    0%{ opacity:0; transform:translate(0,0); }
    12%{ opacity:0.85; transform:translate(-7px,-3px); }
    24%{ opacity:0.5; transform:translate(5px,1px); }
    36%{ opacity:0; transform:translate(0,0); }
    100%{ opacity:0; }
  }
  @keyframes glitchBottom{
    0%{ opacity:0; transform:translate(0,0); }
    12%{ opacity:0.85; transform:translate(7px,3px); }
    24%{ opacity:0.5; transform:translate(-5px,-1px); }
    36%{ opacity:0; transform:translate(0,0); }
    100%{ opacity:0; }
  }

  #skip-intro{
    position: fixed;
    bottom: 28px;
    right: 28px;
    z-index: 6;
    background: transparent;
    border: 1px solid rgba(253,243,236,0.25);
    color: rgba(253,243,236,0.6);
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.08em;
    padding: 8px 14px;
    border-radius: 999px;
    cursor: pointer;
    transition: all 0.25s ease;
  }
  #skip-intro:hover{
    border-color: var(--rose);
    color: var(--rose);
  }

  /* ---------- HERO ---------- */
  #hero{
    position: relative;
    z-index: 3;
    min-height: 100vh;
    display:flex;
    flex-direction: column;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding: 8vh 6vw;
    opacity: 0;
    transition: opacity 1.4s ease;
  }
  #hero.reveal{ opacity: 1; }

  .eyebrow{
    font-size: 0.72rem;
    letter-spacing: 0.35em;
    color: var(--rose);
    text-transform: uppercase;
    margin-bottom: 22px;
    opacity: 0.85;
  }
  .eyebrow::before{ content: "> "; color: var(--gold); }

  .hero-name{
    font-family: 'Pirata One', 'Caveat', cursive;
    font-size: clamp(3.4rem, 12vw, 8rem);
    color: var(--cream);
    line-height: 1;
    text-shadow: 0 0 40px rgba(255,143,163,0.35);
    margin-bottom: 18px;
  }

  .hero-line{
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1.05rem, 2.4vw, 1.5rem);
    color: rgba(253,243,236,0.75);
    max-width: 42ch;
    margin: 0 auto 46px;
    line-height: 1.6;
  }

  .terminal-tag{
    display:inline-flex;
    align-items:center;
    gap: 10px;
    font-size: 0.78rem;
    color: var(--gold);
    border: 1px solid rgba(240,201,135,0.3);
    padding: 10px 20px;
    border-radius: 999px;
    letter-spacing: 0.05em;
  }
  .terminal-tag .dot{
    width:7px; height:7px; border-radius:50%;
    background: var(--rose);
    box-shadow: 0 0 8px var(--rose);
    animation: blink 1.6s infinite ease-in-out;
  }
  @keyframes blink{ 0%,100%{opacity:1;} 50%{opacity:0.25;} }

  .scroll-cue{
    position:absolute;
    bottom: 40px;
    left:50%;
    transform: translateX(-50%);
    font-size: 0.65rem;
    letter-spacing: 0.3em;
    color: rgba(253,243,236,0.45);
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:8px;
  }
  .scroll-cue .bar{
    width:1px; height: 34px;
    background: linear-gradient(to bottom, var(--rose), transparent);
    animation: scrollPulse 1.8s infinite ease-in-out;
  }
  @keyframes scrollPulse{
    0%{ transform: scaleY(0.3); opacity:0.3; }
    50%{ transform: scaleY(1); opacity:1; }
    100%{ transform: scaleY(0.3); opacity:0.3; }
  }

  /* ---------- HANGING POLAROIDS ---------- */
  #polaroid-layer{
    position: fixed;
    inset: 0;
    z-index: 2;
    overflow: hidden;
    pointer-events: none;
  }
  .polaroid-hang{
    position: absolute;
    top: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    opacity: 0;
    transition: opacity 0.8s ease;
  }
  .polaroid-hang.show{ opacity: 1; }

  .rope{
    width: 2px;
    height: 0;
    background: linear-gradient(to bottom,
      rgba(255,143,163,0.05),
      rgba(255,143,163,0.6) 45%,
      rgba(240,201,135,0.75));
    box-shadow: 0 0 6px rgba(255,143,163,0.35);
    transition: height 2.1s cubic-bezier(.22,.75,.2,1);
  }

  .polaroid-frame{
    position: relative;
    width: 76px;
    padding: 6px 6px 20px 6px;
    background: #0b0b0d;
    border: 1px solid rgba(255,143,163,0.18);
    border-radius: 2px;
    box-shadow:
      0 10px 22px rgba(0,0,0,0.6),
      0 0 16px rgba(255,143,163,0.28);
    transform-origin: top center;
    transform: rotate(-4deg);
    pointer-events: auto;
    cursor: grab;
    touch-action: none;
  }
  .polaroid-frame.dragging{
    cursor: grabbing;
    transition: none !important;
    animation: none !important;
  }
  .polaroid-frame.swing{
    animation: swingMotion 5.2s ease-in-out infinite;
  }
  @keyframes swingMotion{
    0%,100%{ transform: rotate(-5deg); }
    50%{ transform: rotate(5deg); }
  }
  .polaroid-frame img{
    width: 100%;
    height: 76px;
    object-fit: cover;
    display: block;
    filter: sepia(0.15) saturate(1.05) contrast(1.02);
  }
  .polaroid-caption{
    position: absolute;
    bottom: 3px;
    left: 0;
    width: 100%;
    text-align: center;
    font-family: 'Caveat', cursive;
    font-size: 0.62rem;
    line-height: 1.1;
    color: #ff5c92;
    text-shadow: 0 0 5px rgba(255,92,146,0.6);
    padding: 0 3px;
    white-space: nowrap;
  }

  .mini-heart{
    position: absolute;
    font-size: 0.65rem;
    line-height: 1;
    color: var(--rose);
    text-shadow: 0 0 6px rgba(255,143,163,0.85);
    animation: heartFloat 2.6s ease-in-out infinite;
    pointer-events: none;
  }
  @keyframes heartFloat{
    0%,100%{ transform: translateY(0) scale(1); opacity: 0.75; }
    50%{ transform: translateY(-7px) scale(1.2); opacity: 1; }
  }
</style>
</head>
<body>

<canvas id="rain"></canvas>
<div id="polaroid-layer"></div>

<div id="intro">
  <div id="intro-word" class="count"></div>
  <div id="intro-flower">
    <div class="flower-center"></div>
    <div class="petal-slot" data-i="0"><div class="petal-pos"><div class="petal-shape"></div></div></div>
    <div class="petal-slot" data-i="1"><div class="petal-pos"><div class="petal-shape"></div></div></div>
    <div class="petal-slot" data-i="2"><div class="petal-pos"><div class="petal-shape"></div></div></div>
  </div>
  <div id="heart-layer">
    <div id="heart-stage"></div>
  </div>
</div>


<button id="skip-intro">skip ›</button>

<section id="hero">
  <div class="eyebrow">national girlfriend's day</div>
  <div class="hero-name" id="heroName">for you</div>
  <p class="hero-line">A little corner of the internet, compiled from scratch,<br>for the only person who's ever debugged my heart.</p>
  <div class="terminal-tag"><span class="dot"></span> still loading how much you mean to me...</div>
  <div class="scroll-cue"><span>scroll</span><span class="bar"></span></div>
</section>

<script>
/* ============ CONFIG ============ */
const HER_NAME = "for you"; // <-- swap in her name/nickname here
document.getElementById('heroName').textContent = HER_NAME;

/* ============ HANGING POLAROIDS ============ */
const PHOTOS = [
  "data:image/jpeg;base64,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",
  "data:image/jpeg;base64,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",
  "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCAEIASwDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwDG2g0oA9BRQD70ALtHTFLge35U3NLuoAMD0FGBjoKAeKUdKAEwPSnKo9BQDjtTxQAbQOwo4znA/Klzk0GgBoUYPFIQPalJ4qteXCW0DSuflAoAr6nqMWnwF2ALH7q+tcXd6hc3cxd5WGegBwBS6leSXtw0jnj+Eegqoo5oAl82b/nq/wD30aQyzf8APV/++jTtvFNIoATzpf8Anq//AH0aPNl/56yf99GkK0AZoAXzZf8Anq//AH0av2ksnGZHP/AjUMFuXOSK0Le3GQfSgB213HLv/wB9GoHtpQcpJJ/30a1EixT/AC6AMCYXCjmR/wDvo03T9Rms7kMzsyHhlJzW5JCrDDLkVmX2nZBaLr6UAdVY3kNwgIYdKvrgjjGK4LSLx4pBA7EYPyn0rtLOfeoVuHA5H9RQBawOw/SjGO1KORnrRwO3IoAQgdgKMD0FLR+NADcD0FLtB7UoBxjrSntxQAwgdKTaAelOI5pSPSgCPb7Ubad9aKAG7RSYp9N4NAEdHSlxR+dADe5pfxpQKXaKAEzSj2owB0pQOaAHZGKUN7fpSCloAUtyKCTjpRQT7UANbgZPTvXJ+I77zpfJRv3adfc1t6xdeRbsQcHoK4m4kLuSepOaAIWOT7U5cCmlsUgOTQBLupwAqOnbsCgBX6VLaxB3BNQEljgVp2iBVFAFqCHnjirsUYHamQDAq3GoC5oAQJxxQVqULQy5oAgIqGRatMtQyLQBz2pReRcLMgOCf1rpNNm+0QRjOGAyprNv4PNgZe+Mijw/OTGU/ijP6UAdZA25OQNw4IqXFV4W3MCO681YA496AEI59qAKUClHWgAozSnikxQA0ijFOx1NIRxQAzGfSjpwadnHFIcUAHbNMOAadTSOetADBS80gHSlzzigAA5pc0oNH8qAEPSgCgnvSigBaUikNJzjmgBTmo3cKKHfaMiqWo3K20BdjzjgUAYPiG83ybAeFrnmcljU17cNNMzN1JqvQAUqmm5pRTAfmgH1ppIApFbe2BSAt267jmtSFcVVtogoFaMYoAsQcYq9FVSIVaQ4xQBMBRim+ZxzQHGOtACMMVDJT3kBqjd3BjXjrQA6TaOprPs8W2qcH5JKrhprhyf4fU1MLXywJFIypzQB19jyGJ7cD6VbHSqGnyBgpHdBmr46CgBf5UClpfSgBMZ60uOaXHvSc0ANI560mKcTz0pMfhQA09abj3p/GKaevSgBvWk69adjJ6Um2gCIc9KQGlwR0pCRQA7INLxjpTF56U8c9aAAD1o6GkFL0oAdnimlto5oJx9KYxBPNAEbnqxPArlddvTLIyg/KDwK2dXvPJi2KeTXH3MpkkJ7UAQMcnNNNKxpuM0wCndBSdBTGbPFACOSTVizXL5NVqu2Y70gNWAdKuKyquWNUQ4Rc05Q0o+YkCgCzLfpGPl5NVTqspOOQKeTbxEBhub0AzTJJIz0iUexIoAmivpH+82RV2GYsM1lx7TwVC/SrcHBHNAFwiQyBg3yY5XHes7UZQGwSBjua1oSCmDWTrNq0ikx9aAKkEclw6pGpAcZVn6H6CpvIu7ctG/IZT1pml2720yyyYyOig1qM8k8is+AB0AoA0NIfMcPP3lrZjOV9xWDpx8uQRkfdbcv071ux8HPagCWnDGaRaCcHigBSfTpTScUhbg1BNMFKpn5jQBIzjNOGSKrRku/HQGrIA96ACkI/KnYpOemKAGg9hikI5p2MdqTGfSgCH8abS4pQPagBo4pcUuB3ppPpQA4YpCeKD1prGgAJNQzTiONix6U5pVUEk1ha1fJ5ZRDyaAMrU7prmdyCcdMVlt1qdyo6nrUDug75oAbjJoI2jmmNNj7oqNnLdTQA53z0poNNApTxQA4HJFaFsvy1nxjLCtW3XgUAWApOM9BSXVw0Ufy9auRw7kBHpUNxYNKfYUAYwmZnzISVzyoOM102mW9pLp6tLEiZzjPWqMdltwDHnHfFXo4Xx9w0AV7i1jSUm1JA/ut0NSxjBHGPbNWPIJ5Y49qTYFoAcjYPFSsFkXDd6hFPQ0ARi2QHqRViKFR05pSvGafG3Y0AI6EDcn3hyK0rC6WeLIOGHVT2qnximpHEzckxydmU4zQBtqecU13wazCbqIcXCH03CkWDUJjkzKi+y80AXLu8jt15ILHoo6mqdustw5durdT6D0qaHS4kffM7Sue7Gr6qqDCgAUANhiEaAVN0pAB1peKAE7Uh9acR+dIfSgBtN/CnEUUAVc0oYZppPFJuGc0APak700tS+9AC1UuJzv8qIZfuPSrLHBqtEVSV84yxzzQAx4dsbPcOenReK4vUple4byxwOK63XLjyrJiveuFkJLE0ANZiTyabQTzzTSc0ABxRxSUUAKKQ09Bmn+WCM96AGwj5hWvb/drLVSpzV+2k6UAbdqfkAq6gGazrduBV6JqALSoMU4pTYmzVgkY4oAquvWqkzBauStwazb9iiB8cZ5oAcGJp6OFPNVBdRqu4sOO1VZtQLHEaH6mgDaMwPFCuCeDWXazNLjHWr8S7AcnJPJNAFgS0ySSPcokAIz0qEgFsg81T1Hc0kaqfmHNAHR2wh27otp9c1ZWffwikEd8Vz2m3Kq+y4T5vX1rpICmwFOlAEsakjn9aeB+VAzmloAOwpRzS8UYGeaAAknk0jcnNL2wKafegBCKZk+lPPSm4zQBmByByaUNxTKQgnjBoAk3Uqy4PPSoTG1N8hiOGP50AW2nSq8tzCoyxWoJLbapZ5MD1rDvXVnK72IHvxQAa7qEc/yRHIHWueY88VZusA4WqpBoAaRSYp1GKYDcUEU6mtQBNbrv3AdRyBViNP3ZOKpxM0bh06ite1kikVmK5RvvqByh9fpSAolTSxMVerU0S5/durCqbBgcsOaANm2lyBzV6KT3rDtJD0rQjfpQBsJKMU7zazlkOOtSCQkdaALJk3HrTXCupVhkGoN2wc0x7qNRksKAEGn24bcVJ9jVhYIB8vlJj6VTN8G4QZNNP2mUHhgP9kUAX2WGFflCr9Kg88E/LyKpLHKDh9341aiUDFAE0ee4xmo7u1lJWVV7cVaiUErkd62mhUxgY4AoA5LedwzwQa6LS5NygE8iqWq2arHuAwe1O0RiXCnr3oA6JacPpSDB7UtACmg8UnQcUpH50AHvTT0peaM57UANNJk040wk9gKAM0CnDpSUm7HSgBW6daQyLGuWPAqGSUL97pWPq2o4G2M4NAEmoXxkYop4HWsa4kJyBRb755Noz7mrE1qIlz396AMh87uTTcU6c4c1Hk0AI1Np+3NHAoAaeBTDTm5p0Kb5FHbqaAHrHhASOaj814pA8bFWHcVLK+agPNAGjBdi7YRuoWQ9CO9PubdoZmifGQM8GslSVYMDgjpVua7kJB2bARwf71AD4n2PjPStKFwcViIxJyauQykUAbKGpl9qzopx3qykwoAssAww3SojY25GdnP1pRJmp0OVoAreSsX3c05ZZF4DHFWdoNL5QPagCmSznnJNTwxkkE1OIMc4qZIwMUAOtot80a/7Wa2WIUYzzVTT0HmE+g4p07kSnC5xQBV1Ri4CqOaj0aMI+fwzRcNuPlxHfI3UjtWhZWvkIoI5HWgC8lO/OmpxTuTQAtDYpAcUZoATtSAmkzz0oz7UAGKbnFP7U08UAZLtgGqz3YUcqalmztJFUJXU5ycGgCtd6gBnOQKxpX8xyxPWrN8+4kAVXjt93LZFAGrpcUUcW/eN3eq2p3SHIBGfaqUimNSA7AfWqMhJPJoAQncxNOFMooAkpp4FCmmk5NAABT1OxCR1bj8KYOtOc847CgBhOaB0pDxQOc4oAQKWOFHNWdRRolgjZQNq8Hua2tNtobe0EjIDIy5JNRXMSXMLI/3gpKn0oAwUbB5qwjVUHWp4zQBdR6nST3qmOnFPVyOtAGgsvpViG55weKy1mHepQ4PQ0AbsUitgmraFDXPRXDLwatx3XvQBqs4zxjFAcVQFyD1NWYg0g3H5EHc0AaunnhmzVt4w/J4P0qlppBB29PcVfFADI4Ej5A5+lTAUD0xSjigB2OKWmg07qKAEoJxSmm59T+FABR1pM0d6AFOKbTjx9aYTQBktyKzruMDOVq+WxzTJSCvNAGF5aN3yRUciFBUt/ugfzIhkA/MvrVea8iliyCQfQ0AUpyTVOTrViWTOaqOcmgBM0CkoFADs0maTNBNADkPzU7qTUYPNPU9fcUANbrU9gu64Hy78DO3HX2qA1NZ3b2cxkjVGJGPmGRQB0LtJNCT5aQsxwEB6fSm2sDRFnb94QOF96ikSOWa2dbhDI7Ana33ePTtSiJomkujOu9GbClxggeooAxtUAW8ZRF5ZHUe9QIadczNcStK/3mOTikhGWxQBZiGRUuypraDGCRWgLVWTpQBkbKcq4q9LZsvK8+1QbMHkUANSp4xk0xUq1bREnJoAt2qDjgVdAaM7l529qjt4wMVcKgLntigB9qfKlXaxKPwM9j/9etNazLFMpHkdOQa0kzjpQBIPanduKb2560Ak9elADuBSg8c038KWgAzkdKD0o4o5xigAHSkopPpQApNMyacelMLc0AYb71JDY9iKhkkYdelSzHk1UnfapyRQBVvcSAmsmSEcnNSXtwQ2FOfpVKSZyOTQBFIeajpxOTTTQAlBpTTaYBRRRQAUoNJRQIM0UVb0iJZtQhSQZUnnikM1dE02GYhriTyzn72Ogqpq9jHbSt5T7kz1Pet+MR7CgTgNj5D3rL1uECFpCXBz3HB/GgDAbpVzT4dzbiKrxQNK4HQetbVsIYAMt+lAFuCLOOKupERxUNtcWx/5arn34rQiCsMgg/Q0AReUGHIqGSxR+a0AtO20AZA08KfWp0t9p6VdZcGjbkUANijxVg/cpkZH3TxUgyOKALUEWUDJ0qyEOAe1ZIeRD+7fa36VoWd95nyXCbG9R0NAE+CKTBxVhI8EYOc050U4449KAKgPFKfbNSSRlDxyKYeaAEyRml5pKXPFACUHjtRn0oNADTTGPNPbgcVGwGelAGG5zmsbULjBKir13ceXGQPvGufnkLStuNAEcjZ5NV3anyPUPWgAooopgBppp1GKAGUU7FBpANopaMUwEpUdkYMjFWHQijFTW8BkOT90UgLVhe30LZilbGc4Y5Gau3ErXaIJ1X5fTvUKKAMAVIBQAgUAYUAClxTsUYoAiaMGnIXjP7t2X6Gn7aTFAFiLUrqLjzNw/wBoVdg1kcCaIj3XmsojNJjFAHRre28o+Rx9O9PDk8rXNYB+tXLXUJbcgN86eh6igDbCv14zUiuR98c+tRW91FcpmNue47ipSOKABiN2RTlPNR96UHigDRs71Y3WKY/K3Ck1pYxgg8VzkiCRCpOD2PpWno98Zgba4IEqd/X3oA0mA6npVeVMHIHFWCSOh5psvzLn86AKh47UHpSvxzTKAF70HNIKCaAEJ96jJ9jTmphNAHG38wFwS/IVeB71hO5JJPXNbGojEk59hisXqDQA0800089KaRQAUtNzSg0AFKKSigBaaetBOaM0AAHNSIuaYOtWoEL8AUARpDuar0aBVwKkjgKjpUmzFADAOOKcKWlxigBKKUDNOCigBhFGKlwKTAoAjpKlwDTStAEZoB7UpHrRigBVZkbdGxUjuDWjaau6/JcruH94dazQKfsDUAdFHKko3RsGHtTgea5tDLbvuiYg/pWla6orELcDa394dKANYUyRWDLLEcSp09/alQhgGUgg9xT6ANbT79LuPO35hwy9wastwcDFc2shtLlZ14QnD/410SMHRWDAhhxQAyReDzz2queDxVpxgCqzcNigBtB6UDg80h65oAQ9MUw5p7Uw0Acbfo7RytxsY8msMriugviPs5WsSUDaPpQBWNNNONMJoAM0UAZNPMZVcnvTAZSZNKaSgAzRmkJp0SGRsCkBNDGZGAH51r2kawp6k96rW8YRQKuRigCdBupkq4qRKbKRQBXA5qRRTAKeKAH7MjJOKCo7HNJ1pw+lADcAdqC6gYIpwpCAR0oAb8p70HnvSbBRsFAEZGDzSU5+KavIJ7UAPUVLGOcVAMq2O1XIVXvn8KAJEiDDBFJLYEjKjPtVy3TpWhbx7iFxQBnaXaXCMMEiM9Qavb18xkVgSvXFT3QljgaOJgrHoSOtc23mQzbskOOpoA3ZF3xlccEYrU0p99hH6gYrBtL4SjZL8r9j2NbWj/8AHlj/AGj/ADoAutUEnLGrHBHJqGUYxQBGeBSZ4pDxScc0AB5ppNLTD70AcdduNpyeaxpW4q/dNuUkmsyQ5zQAwmm4zS4p6r8uaAC3Ub8mnzHccUxQVGcVLt+TNAFdhimGnueajJoAACTgVp2kOxAe9VLSPc2T2rSUYGKAHL1qzGeKrAVKh4oAsKcUyQ8UqHIyaa9ADRTgKbTqAH4paaKM4oAdSbsds0hcU0uBQAFs0m/FBcGmEjtQAO2e1RB9oAU/N6EVJSsrfZ1A2tz949VPpQA5cuMFSD7jrVu1OflPUVVimyqo4II/IVbgUtJ8tAGpboOK07aLgNnpVC2QhcsKuRTbKAJ7oLIuDw3rWJfWpOcjkdK2HcOMio5EWVMgc0Ac1twcN1rZ0fU/JIt7jhD916q3dqTkjqKis4/MYCRcr6mgDrc8Ar07U1xuHIrGj1VbacQyf6rpu9K2QysqkHIboaAIWBphqZ1NQtQA0nimnrTjTDQBwlzC20lsgVmuMV0Op48s1gHk0ARCpgvFRgc1ZiXdigCRYx5DZHaoScQVcbiFvpVCU4jx70AVmNCKWYDFGM1ct4sAetAEsCbRVgU1RgUvegB4p45pgp60ASx8DmhmpM4WmMc0ALuFLu9KizSFqAJt1NLjuagaT0oVGf2oAe0tMMuTxk/SpRaKRk04QbfpQBAJT/cb8qf5mMZRgD3xxT24zkUiSYOD0oAUEHpSBdjghSQevNSMqgbh0pyRM8anu3IXvigCe2MURLS7QD0LDP4Vp6fDGsZlJwuThj6Vlw/dGDnjgmp5CUiUK74Bwysf1FAGmb5XkMcY+UDr60eYTWXAfnY1aVyO9AGlbyZ4zUykqd3Ud6zoXwwrVtyGHNACvbq4yO9Zl/JFaJtRcljz7VsZC/SsbWotymROnegDJkYOSRWjo+qG2byJjmIngn+GsdWI60/ryKAO5BDDIPHrTHTcPesbw/qB5tpySP4D/StwrgnNAFRwVJB7VHVuWPcpPeqjcHGKAOP1I/KaxaKKAADmrcAxRRQBNN/qjWbP1AoooASFNzir6LgUUUAPxS9qKKADpUi0UUAPb7tRE0UUAMJpmSxwozRRQBKFVF9WqaNdo560UUAP8xVG0jOaDOMYAOKKKAGF89qiIoooAFc7gg5z6nFWYJ3CY24bpuz0H0oooAljGABVpokuEVmYIU6kjtRRQBFFwzYOfcVOGoooAfG3zDmte0OzkniiigCeVwynHWqLnOVblSMGiigDCu4DBMR/CeRUKnBoooA0lCLbxuF2tu6+ldBYzmaH5/vjrRRQBYJ469agZRmiigD/2Q==",
  "data:image/jpeg;base64,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"
];
const polaroidLayer = document.getElementById('polaroid-layer');
let polaroidStarted = false;

// left position, how far the rope drops (stays well above the hero text),
// which photo, and a small tilt so they don't look identical
const HANG_CONFIGS = [
  { left: '9%',  drop: '13vh', photo: 0, tilt: -6 },
  { left: '36%', drop: '17vh', photo: 1, tilt: 4 },
  { left: '63%', drop: '14vh', photo: 2, tilt: -3 },
  { left: '88%', drop: '19vh', photo: 3, tilt: 5 },
];

function createHangingPolaroid(cfg, delayMs){
  const wrap = document.createElement('div');
  wrap.className = 'polaroid-hang';
  wrap.style.left = cfg.left;

  const rope = document.createElement('div');
  rope.className = 'rope';

  const frame = document.createElement('div');
  frame.className = 'polaroid-frame';
  frame.style.transform = `rotate(${cfg.tilt}deg)`;

  const img = document.createElement('img');
  img.src = PHOTOS[cfg.photo % PHOTOS.length];
  frame.appendChild(img);

  const caption = document.createElement('div');
  caption.className = 'polaroid-caption';
  caption.textContent = 'still crushing on you';
  frame.appendChild(caption);

  // little hearts tucked around the white border of the polaroid
  const heartSpots = [
    {top:'-8px', left:'-8px', delay:'0s'},
    {top:'-8px', right:'-8px', delay:'0.5s'},
    {bottom:'-6px', left:'-8px', delay:'1s'},
    {bottom:'-6px', right:'-8px', delay:'1.5s'},
  ];
  heartSpots.forEach(spot=>{
    const h = document.createElement('span');
    h.className = 'mini-heart';
    h.textContent = '♥';
    Object.keys(spot).forEach(k=>{
      if(k !== 'delay') h.style[k] = spot[k];
    });
    h.style.animationDelay = spot.delay;
    frame.appendChild(h);
  });

  wrap.appendChild(rope);
  wrap.appendChild(frame);
  polaroidLayer.appendChild(wrap);

  // drag/touch: grab the photo and it swings with you, like it's really on the string
  let dragging = false;
  let startX = 0;
  let baseRot = cfg.tilt;

  function onDown(e){
    dragging = true;
    frame.classList.add('dragging');
    startX = (e.touches ? e.touches[0].clientX : e.clientX);
  }
  function onMove(e){
    if(!dragging) return;
    const x = (e.touches ? e.touches[0].clientX : e.clientX);
    const deltaX = x - startX;
    const rot = Math.max(-45, Math.min(45, baseRot + deltaX * 0.35));
    frame.style.transform = `rotate(${rot}deg)`;
  }
  function onUp(){
    if(!dragging) return;
    dragging = false;
    frame.classList.remove('dragging');
    frame.style.transform = `rotate(${cfg.tilt}deg)`;
    frame.classList.remove('swing');
    void frame.offsetWidth;
    frame.classList.add('swing');
  }

  frame.addEventListener('pointerdown', onDown);
  window.addEventListener('pointermove', onMove);
  window.addEventListener('pointerup', onUp);
  frame.addEventListener('touchstart', onDown, {passive:true});
  window.addEventListener('touchmove', onMove, {passive:true});
  window.addEventListener('touchend', onUp);

  // gentle scroll parallax so the photos drift as the page scrolls, like they're really hanging in the room
  const parallaxDepth = 0.04 + Math.random() * 0.05;
  function onScroll(){
    if(dragging) return;
    wrap.style.transform = `translateY(${window.scrollY * parallaxDepth}px)`;
  }
  window.addEventListener('scroll', onScroll, {passive:true});

  setTimeout(()=>{
    wrap.classList.add('show');
    requestAnimationFrame(()=>{
      rope.style.height = cfg.drop;
    });
    // once the drop finishes, start the gentle swing
    setTimeout(()=>{
      frame.classList.add('swing');
    }, 2150);
  }, delayMs);
}

function startPolaroidRain(){
  if(polaroidStarted) return;
  polaroidStarted = true;
  // one at a time: each waits for the previous drop to finish before starting
  const DROP_TIME = 2150;
  const GAP = 500;
  HANG_CONFIGS.forEach((cfg, i)=> createHangingPolaroid(cfg, i * (DROP_TIME + GAP)));
}

/* ============ MATRIX / CODE RAIN ============ */
const canvas = document.getElementById('rain');
const ctx = canvas.getContext('2d');
let w, h, columns, drops, heartColumns, heartDrops, heartSpeed;
const glyphs = "01♥{}<>/=+*love#$%code&";
const fontSize = 13;
const heartGap = 30;

function resize(){
  w = canvas.width = window.innerWidth;
  h = canvas.height = window.innerHeight;
  columns = Math.floor(w / fontSize);
  drops = new Array(columns).fill(0).map(()=> Math.random() * -100);

  heartColumns = Math.floor(w / heartGap);
  heartDrops = new Array(heartColumns).fill(0).map(()=> Math.random() * -60);
  heartSpeed = new Array(heartColumns).fill(0).map(()=> 0.25 + Math.random()*0.35);
}
window.addEventListener('resize', resize);
resize();

function draw(){
  // lower alpha = slower fade = denser, longer trails
  ctx.fillStyle = 'rgba(7,6,10,0.09)';
  ctx.fillRect(0,0,w,h);

  ctx.font = fontSize + "px 'JetBrains Mono', monospace";

  for(let i=0;i<columns;i++){
    // draw two glyphs per column per frame for extra volume
    for(let k=0;k<2;k++){
      const char = glyphs[Math.floor(Math.random()*glyphs.length)];
      const x = i * fontSize;
      const y = (drops[i] - k*0.6) * fontSize;

      const isHighlight = Math.random() > 0.955;
      ctx.fillStyle = isHighlight
        ? 'rgba(240,201,135,0.95)'
        : 'rgba(255,143,163,' + (Math.random()*0.6 + 0.22) + ')';
      ctx.fillText(char, x, y);
    }

    if(drops[i] * fontSize > h && Math.random() > 0.955){
      drops[i] = 0;
    }
    drops[i] += 0.85 + Math.random()*0.5;
  }

  // dedicated heart layer, same rose/gold family, falling slower on top
  ctx.font = "17px 'JetBrains Mono', monospace";
  for(let j=0;j<heartColumns;j++){
    const x = j * heartGap + (j % 2 === 0 ? 4 : 14);
    const y = heartDrops[j] * fontSize;
    const isGold = j % 7 === 0;
    ctx.fillStyle = isGold
      ? 'rgba(240,201,135,' + (Math.random()*0.4 + 0.4) + ')'
      : 'rgba(255,143,163,' + (Math.random()*0.45 + 0.4) + ')';
    ctx.fillText('♥', x, y);

    if(y > h && Math.random() > 0.96){
      heartDrops[j] = 0;
    }
    heartDrops[j] += heartSpeed[j];
  }

  requestAnimationFrame(draw);
}
draw();

/* ============ INTRO SEQUENCE ============ */
const sequence = [
  {type:"flower", remaining:3},
  {type:"flower", remaining:2},
  {type:"flower", remaining:1},
  {type:"heart"},
  {type:"word", text:"Happy", cls:"word"},
  {type:"word", text:"National", cls:"word"},
  {type:"word", text:"Girlfriend's", cls:"word"},
  {type:"word", text:"Day", cls:"word"},
];

const introEl = document.getElementById('intro');
const wordEl = document.getElementById('intro-word');
const flowerEl = document.getElementById('intro-flower');
const petals = Array.from(flowerEl.querySelectorAll('.petal-shape'));
const heartLayerEl = document.getElementById('heart-layer');
const heartStageEl = document.getElementById('heart-stage');
const hero = document.getElementById('hero');
const skipBtn = document.getElementById('skip-intro');
let step = 0;
let timer = null;
let finished = false;
const HEART_TOTAL = 70; // fewer than the original 100, kinder to phones

function setFlowerStage(remaining){
  const fallenCount = 3 - remaining;
  if(fallenCount <= 0){
    petals.forEach(p => p.classList.remove('fallen'));
  } else {
    petals[fallenCount - 1].classList.add('fallen');
  }
}

function sizeHeartStage(){
  const scale = Math.min(1, (window.innerWidth * 0.82) / 450, (window.innerHeight * 0.55) / 450);
  heartStageEl.style.setProperty('--heart-scale', scale);
}
window.addEventListener('resize', sizeHeartStage);

function buildHeartField(){
  if(heartStageEl.childElementCount) return;
  for(let i = 1; i <= HEART_TOTAL; i++){
    const love = document.createElement('div');
    love.className = 'love';
    love.style.setProperty('--i', i);
    love.innerHTML = `
      <div class="love_horizontal">
        <div class="love_vertical">
          <div class="love_word">I love you</div>
        </div>
      </div>
    `;
    heartStageEl.appendChild(love);
  }
}

function showHeartField(){
  sizeHeartStage();
  buildHeartField();
  heartLayerEl.classList.add('show');
}

function hideHeartField(){
  heartLayerEl.classList.remove('show');
  // fully clear it after the fade-out so the 70 looping animations
  // stop costing anything for the rest of the page
  setTimeout(()=>{ heartStageEl.innerHTML = ''; }, 750);
}

function playStep(){
  if(step >= sequence.length){
    endIntro();
    return;
  }
  const item = sequence[step];

  if(item.type === "flower"){
    wordEl.classList.remove('show');
    wordEl.style.display = "none";
    heartLayerEl.classList.remove('show');
    flowerEl.classList.add('show');
    setFlowerStage(item.remaining);
    step++;
    timer = setTimeout(playStep, 1150);
    return;
  }

  if(item.type === "heart"){
    wordEl.classList.remove('show');
    wordEl.style.display = "none";
    flowerEl.classList.remove('show');
    showHeartField();
    step++;
    timer = setTimeout(()=>{
      hideHeartField();
      playStep();
    }, 3600);
    return;
  }

  flowerEl.classList.remove('show');
  heartLayerEl.classList.remove('show');
  wordEl.style.display = "block";
  wordEl.textContent = item.text;
  wordEl.setAttribute('data-text', item.text);
  wordEl.className = item.cls; // reset classes
  void wordEl.offsetWidth; // reflow to restart animation
  wordEl.classList.add('show');
  if(item.text === "Happy"){
    startPolaroidRain();
  }
  step++;
  timer = setTimeout(playStep, 850);
}

function endIntro(){
  if(finished) return;
  finished = true;
  clearTimeout(timer);
  startPolaroidRain();
  introEl.style.transition = "opacity 0.8s ease";
  introEl.style.opacity = "0";
  skipBtn.style.transition = "opacity 0.4s ease";
  skipBtn.style.opacity = "0";
  setTimeout(()=>{
    introEl.style.display = "none";
    skipBtn.style.display = "none";
    heartStageEl.innerHTML = '';
  }, 800);
  hero.classList.add('reveal');
}

skipBtn.addEventListener('click', endIntro);

setTimeout(playStep, 400);
</script>

</body>
</html>