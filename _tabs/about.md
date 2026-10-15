---
title: About Me
icon: fas fa-user
order: 1
---

<style>
/* ── Color Tokens ── */
:root {
  --accent: #4a9eff;
  --accent-glow: rgba(74, 158, 255, .18);
  --card-bg: rgba(255,255,255,.05);
  --card-border: rgba(255,255,255,.08);
  --text-muted: #8b949e;
}

/* ── Reveal Animation ── */
.reveal {
  opacity: 0;
  transform: translateY(24px);
  transition: opacity .7s ease, transform .7s ease;
}
.reveal.in {
  opacity: 1;
  transform: translateY(0);
}

/* ── Hero Section ── */
.hero-section {
  text-align: center;
  padding: 2rem 0 3rem;
}
.hero-section h1 {
  font-size: 2.4rem;
  font-weight: 800;
  margin-bottom: .5rem;
  background: linear-gradient(135deg, #fff 0%, var(--accent) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.hero-section .tagline {
  font-size: 1.15rem;
  color: var(--text-muted);
  margin-bottom: 1.5rem;
  line-height: 1.6;
}
.hero-section .highlight {
  color: var(--accent);
  font-weight: 600;
  -webkit-text-fill-color: var(--accent);
}
.typing-cursor::after {
  content: '|';
  animation: blink 1s step-end infinite;
  color: var(--accent);
  -webkit-text-fill-color: var(--accent);
}
@keyframes blink {
  50% { opacity: 0; }
}

/* ── Section Title ── */
.section-title {
  font-size: 1.3rem;
  font-weight: 700;
  margin: 3rem 0 1.5rem;
  padding-bottom: .5rem;
  border-bottom: 2px solid var(--accent);
  display: inline-block;
}

/* ── Cards Grid ── */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1rem;
  margin: 1rem 0;
}
.card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 12px;
  padding: 1.5rem;
  transition: transform .3s ease, box-shadow .3s ease, border-color .3s ease;
  cursor: default;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 28px -8px rgba(74, 158, 255, .15);
  border-color: var(--accent);
}
.card .card-icon {
  font-size: 1.8rem;
  margin-bottom: .8rem;
  display: block;
}
.card h4 {
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: .4rem;
  color: #e6edf3;
}
.card p {
  font-size: .88rem;
  color: var(--text-muted);
  line-height: 1.5;
  margin: 0;
}

/* ── Timeline ── */
.timeline {
  position: relative;
  padding-left: 2rem;
  margin: 1.5rem 0;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 6px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: var(--card-border);
}
.timeline-item {
  position: relative;
  margin-bottom: 1.8rem;
  padding-left: .5rem;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -1.85rem;
  top: 6px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: var(--text-muted);
  border: 2px solid #1a1a2e;
  transition: all .3s ease;
}
.timeline-item.now::before {
  background: var(--accent);
  box-shadow: 0 0 0 5px var(--accent-glow);
}
.timeline-item .period {
  font-size: .8rem;
  color: var(--accent);
  font-weight: 600;
  margin-bottom: .2rem;
}
.timeline-item .role {
  font-size: 1rem;
  font-weight: 700;
  color: #e6edf3;
}
.timeline-item .company {
  font-size: .9rem;
  color: var(--text-muted);
}
.timeline-item .desc {
  font-size: .85rem;
  color: var(--text-muted);
  margin-top: .3rem;
  line-height: 1.5;
}

/* ── Skill Tags ── */
.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: .5rem;
  margin: 1rem 0;
}
.skill-tag {
  background: rgba(74, 158, 255, .1);
  border: 1px solid rgba(74, 158, 255, .25);
  color: var(--accent);
  padding: .35rem .85rem;
  border-radius: 20px;
  font-size: .82rem;
  font-weight: 500;
  transition: all .3s ease;
}
.skill-tag:hover {
  background: rgba(74, 158, 255, .2);
  transform: scale(1.05);
}

/* ── Interest Cards ── */
.interest-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin: 1rem 0;
}
.interest-card {
  background: var(--card-bg);
  border: 1px solid var(--card-border);
  border-radius: 12px;
  padding: 1.2rem;
  text-align: center;
  transition: transform .3s ease, border-color .3s ease;
}
.interest-card:hover {
  transform: translateY(-3px);
  border-color: var(--accent);
}
.interest-card .emoji {
  font-size: 2rem;
  margin-bottom: .5rem;
  display: block;
}
.interest-card span:last-child {
  font-size: .85rem;
  color: var(--text-muted);
}

/* ── Responsive ── */
@media (max-width: 768px) {
  .hero-section h1 { font-size: 1.8rem; }
  .cards-grid { grid-template-columns: 1fr; }
  .interest-grid { grid-template-columns: repeat(3, 1fr); }
}

/* ── Reduce motion ── */
@media (prefers-reduced-motion: reduce) {
  .reveal { opacity: 1; transform: none; transition: none; }
  .card:hover { transform: none; }
}
</style>

<div class="hero-section reveal">
  <h1>안녕하세요, 박승찬입니다<span class="typing-cursor"></span></h1>
  <p class="tagline">
    <span class="highlight">문제를 정의</span>하고, <span class="highlight">데이터로 분석</span>하고,<br>
    <span class="highlight">서비스까지 만드는</span> 일을 하고 있습니다.
  </p>
</div>

<div class="section-title reveal">What I Do</div>

<div class="cards-grid">
  <div class="card reveal">
    <span class="card-icon">🎯</span>
    <h4>Problem Solving</h4>
    <p>전사에서 발생하는 문제를 찾아내어 정의하고, 구조화하여 해결합니다.</p>
  </div>
  <div class="card reveal">
    <span class="card-icon">📊</span>
    <h4>Data Analysis</h4>
    <p>SQL과 데이터 분석을 통해 근거 기반의 의사결정을 이끌어냅니다.</p>
  </div>
  <div class="card reveal">
    <span class="card-icon">🛠️</span>
    <h4>Vibe Coding</h4>
    <p>AI와 함께 작지만 진짜 돌아가는 서비스를 직접 만듭니다.</p>
  </div>
</div>

<div class="section-title reveal">Career</div>

<div class="timeline">
  <div class="timeline-item now reveal">
    <div class="period">2025.09 — Present</div>
    <div class="role">전략 PM</div>
    <div class="company">쿠팡이츠 · Business Excellence Team</div>
    <div class="desc">전사 문제 해결 전담 조직에서 문제정의 → 데이터 분석 → 솔루션 수립</div>
  </div>
  <div class="timeline-item now reveal">
    <div class="period">2025.09 — Present</div>
    <div class="role">석사과정</div>
    <div class="company">KAIST 경영대학원 · 정보경영프로그램(IMMS) 14기</div>
    <div class="desc">AI-Driven Business, IT경영 전략</div>
  </div>
  <div class="timeline-item reveal">
    <div class="period">2021.03 — 2025.04</div>
    <div class="role">PM</div>
    <div class="company">NHN PAYCO · 서비스기획팀</div>
    <div class="desc">캠퍼스 사업 수익 구조 개선, 제휴 프로모션, 결제 서비스 채널링</div>
  </div>
  <div class="timeline-item reveal">
    <div class="period">2019.07 — 2021.02</div>
    <div class="role">SCM</div>
    <div class="company">SK케미칼</div>
    <div class="desc">공급망 관리 및 운영 최적화</div>
  </div>
  <div class="timeline-item reveal">
    <div class="period">— 2019</div>
    <div class="role">국제학과 졸업</div>
    <div class="company">경희대학교</div>
    <div class="desc">Global Business 심화</div>
  </div>
</div>

<div class="section-title reveal">Skills</div>

<div class="skill-tags reveal">
  <span class="skill-tag">Problem Solving</span>
  <span class="skill-tag">Data Analysis</span>
  <span class="skill-tag">SQL</span>
  <span class="skill-tag">Product Management</span>
  <span class="skill-tag">Vibe Coding</span>
  <span class="skill-tag">Service Planning</span>
  <span class="skill-tag">Strategic Partnerships</span>
  <span class="skill-tag">Business Development</span>
</div>

<div class="section-title reveal">Interests</div>

<div class="interest-grid reveal">
  <div class="interest-card">
    <span class="emoji">🏀</span>
    <span>농구</span>
  </div>
  <div class="interest-card">
    <span class="emoji">⚾</span>
    <span>삼성라이온즈</span>
  </div>
  <div class="interest-card">
    <span class="emoji">🍽️</span>
    <span>미식</span>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('in'), i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.15 });

  document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
});
</script>
