```aura width=800 height=400 align=center
<div style={{
  display: 'flex',
  flexDirection: 'column',
  width: '800px',
  height: '400px',
  background: '#0a0d14',
  border: '1px solid #1f2a44',
  borderRadius: '20px',
  padding: '28px',
  fontFamily: 'Inter, system-ui, sans-serif',
  color: '#c9d1d9',
  position: 'relative',
  overflow: 'hidden'
}}>
  {/* CSS Keyframe Animations parsed directly by the browser */}
  <style>{`
    @keyframes pulse {
      0% { opacity: 0.3; transform: scale(0.98); }
      50% { opacity: 1; transform: scale(1); }
      100% { opacity: 0.3; transform: scale(0.98); }
    }
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-5px); }
      100% { transform: translateY(0px); }
    }
  `}</style>

  {/* Background Scanline Layer */}
  <div style={{
    display: 'flex',
    position: 'absolute',
    top: 0, left: 0, right: 0, bottom: 0,
    background: 'linear-gradient(rgba(0, 191, 255, 0.03) 50%, rgba(0, 0, 0, 0) 50%)',
    backgroundSize: '100% 4px',
    pointerEvents: 'none'
  }} />

  {/* Header Row */}
  <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'center' }}>
    <div style={{ display: 'flex', alignItems: 'center', gap: '12px' }}>
      {/* Animated Heartbeat Indicator */}
      <div style={{
        display: 'flex',
        width: '12px',
        height: '12px',
        borderRadius: '50%',
        backgroundColor: '#00BFFF',
        animation: 'pulse 2s infinite ease-in-out'
      }} />
      <span style={{ fontSize: '18px', fontWeight: '800', color: '#ffffff', letterSpacing: '1px', textTransform: 'uppercase' }}>
        Sivabalan Core Engine HUD
      </span>
    </div>
    <div style={{ display: 'flex', fontSize: '11px', color: '#58a6ff', fontFamily: 'monospace', border: '1px solid #1f2a44', padding: '4px 10px', borderRadius: '6px', background: '#161b22' }}>
      SYS_STATUS: ACTIVE_OK
    </div>
  </div>

  {/* Main Content Grid */}
  <div style={{ display: 'flex', flex: 1, marginTop: '24px', gap: '24px' }}>
    
    {/* Left Column: Diagnostics Gauges */}
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1.2, gap: '16px' }}>
      <span style={{ fontSize: '12px', color: '#8b949e', textTransform: 'uppercase', letterSpacing: '1px', fontWeight: 'bold' }}>
        ⚡ Performance Engine Diagnostics
      </span>
      
      {/* Gauge 1: Database Latency */}
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <div style={{ display: 'flex', justifyContent: 'space-between', fontSize: '13px', marginBottom: '6px' }}>
          <span style={{ color: '#c9d1d9', fontWeight: '600' }}>🗄️ DB Latency (EXPLAIN Optimized)</span>
          <span style={{ color: '#00BFFF', fontWeight: 'bold', fontFamily: 'monospace' }}>0.8ms</span>
        </div>
        <div style={{ display: 'flex', width: '100%', height: '8px', background: '#161b22', borderRadius: '4px', overflow: 'hidden', border: '1px solid #1f2a44' }}>
          <div style={{ display: 'flex', width: '98%', height: '100%', background: 'linear-gradient(90deg, #00BFFF 0%, #00ffff 100%)', borderRadius: '4px' }} />
        </div>
      </div>

      {/* Gauge 2: API Throughput Efficiency */}
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <div style={{ display: 'flex', justifyContent: 'space-between', fontSize: '13px', marginBottom: '6px' }}>
          <span style={{ color: '#c9d1d9', fontWeight: '600' }}>⚡ FastAPI Pipeline Throughput</span>
          <span style={{ color: '#39ff14', fontWeight: 'bold', fontFamily: 'monospace' }}>99.9%</span>
        </div>
        <div style={{ display: 'flex', width: '100%', height: '8px', background: '#161b22', borderRadius: '4px', overflow: 'hidden', border: '1px solid #1f2a44' }}>
          <div style={{ display: 'flex', width: '99%', height: '100%', background: 'linear-gradient(90deg, #39ff14 0%, #00ff88 100%)', borderRadius: '4px' }} />
        </div>
      </div>

      {/* Gauge 3: LLM Autopilot Reliability */}
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <div style={{ display: 'flex', justifyContent: 'space-between', fontSize: '13px', marginBottom: '6px' }}>
          <span style={{ color: '#c9d1d9', fontWeight: '600' }}>🤖 Agentic Autopilot Load</span>
          <span style={{ color: '#bd00ff', fontWeight: 'bold', fontFamily: 'monospace' }}>94.2%</span>
        </div>
        <div style={{ display: 'flex', width: '100%', height: '8px', background: '#161b22', borderRadius: '4px', overflow: 'hidden', border: '1px solid #1f2a44' }}>
          <div style={{ display: 'flex', width: '94%', height: '100%', background: 'linear-gradient(90deg, #bd00ff 0%, #ff00ff 100%)', borderRadius: '4px' }} />
        </div>
      </div>
    </div>

    {/* Right Column: Dynamic System Console Logs */}
    <div style={{
      display: 'flex',
      flexDirection: 'column',
      flex: 0.8,
      background: '#0d1117',
      border: '1px solid #1f2a44',
      borderRadius: '12px',
      padding: '16px',
      fontSize: '11px',
      fontFamily: 'monospace',
      color: '#8b949e',
      justifyContent: 'space-between',
      animation: 'float 4s infinite ease-in-out'
    }}>
      <div style={{ display: 'flex', flexDirection: 'column', gap: '8px' }}>
        <span style={{ color: '#00BFFF', fontWeight: 'bold' }}>&gt; init_sivabalan_hud.sh</span>
        <span style={{ color: '#39ff14' }}>[ OK ] FastAPI Server Online.</span>
        <span style={{ color: '#39ff14' }}>[ OK ] EXPLAIN plan index tuned.</span>
        <span style={{ color: '#39ff14' }}>[ OK ] LLM Semantic Worker active.</span>
        <span style={{ color: '#bd00ff' }}>[ LOAD ] Running agentic loops...</span>
      </div>
      
      <div style={{ display: 'flex', flexDirection: 'column', borderTop: '1px solid #1f2a44', paddingTop: '10px', marginTop: '10px' }}>
        <span style={{ color: '#ffffff', fontWeight: 'bold' }}>♟️ CHESS_STRATEGY:</span>
        <span style={{ fontSize: '10px', color: '#8b949e', marginTop: '4px', lineHeight: '1.3' }}>
          Refactor code when center control is secure. Always secure the core logic.
        </span>
      </div>
    </div>
  </div>

  {/* Footer */}
  <div style={{ display: 'flex', borderTop: '1px solid #1f2a44', paddingTop: '14px', justifyContent: 'space-between', fontSize: '11px', color: '#8b949e' }}>
    <span>* Interactive CSS animations render dynamically in browser</span>
    <span>v1.2.0-cyberpunk-hud</span>
  </div>
</div>
```

---

### 🚀 About Me

I am a **Senior Software Developer** with a passion for designing and optimizing robust backends, microservice architectures, and modern API engines. I bring engineering concepts to life by focusing on clean, scalable code, advanced database performance tuning, and building intelligent automation workflows.

* ⚙️ **Distributed Systems**: Engineering responsive microservices and high-throughput async APIs using FastAPI, Flask, and Tornado.
* ⚡ **Performance Tuning**: Turning slow, sequential database queries into sub-millisecond lookups using query optimization and `EXPLAIN` plan analysis.
* 🤖 **Intelligent Workflows**: Exploring and integrating NLP, semantic analyzers, and background workers into reliable data aggregation pipelines.
* ♟️ **Architectural Philosophy**: *"Great software is like chess — control the center (core logic), understand value (trade-offs), and know when to retreat (refactor)."*

---

### 📊 Real-Time GitHub Analytics

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=sivabalanb&theme=tokyonight" alt="Sivabalan's GitHub Activity Graph" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=sivabalanb&theme=tokyonight&hide_border=false" alt="GitHub Streak" />
</p>

---

```aura width=800 height=320 align=center
<div style={{
  display: 'flex',
  flexDirection: 'column',
  width: '800px',
  height: '320px',
  background: '#0d1117',
  border: '1px solid #30363d',
  borderRadius: '16px',
  padding: '24px',
  fontFamily: 'Inter, system-ui, sans-serif',
  color: '#c9d1d9',
  justifyContent: 'space-between'
}}>
  <div style={{ display: 'flex', flexDirection: 'column' }}>
    <span style={{ fontSize: '20px', fontWeight: '700', color: '#ffffff', borderBottom: '1px solid #21262d', paddingBottom: '10px' }}>
      🧠 Core Expertise & Tech Stack
    </span>
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', gap: '14px' }}>
    {/* Row 1 */}
    <div style={{ display: 'flex', alignItems: 'center' }}>
      <span style={{ width: '180px', fontSize: '14px', color: '#8b949e', fontWeight: '600' }}>🐍 Backend & APIs:</span>
      <div style={{ display: 'flex', gap: '8px' }}>
        <span style={{ padding: '4px 10px', background: '#3776AB22', border: '1px solid #3776AB', borderRadius: '6px', fontSize: '12px', color: '#3776AB', fontWeight: 'bold' }}>Python</span>
        <span style={{ padding: '4px 10px', background: '#00968822', border: '1px solid #009688', borderRadius: '6px', fontSize: '12px', color: '#009688', fontWeight: 'bold' }}>FastAPI</span>
        <span style={{ padding: '4px 10px', background: '#4479A122', border: '1px solid #4479A1', borderRadius: '6px', fontSize: '12px', color: '#4479A1', fontWeight: 'bold' }}>Flask</span>
        <span style={{ padding: '4px 10px', background: '#092E2022', border: '1px solid #092E20', borderRadius: '6px', fontSize: '12px', color: '#092E20', fontWeight: 'bold' }}>Django</span>
      </div>
    </div>

    {/* Row 2 */}
    <div style={{ display: 'flex', alignItems: 'center' }}>
      <span style={{ width: '180px', fontSize: '14px', color: '#8b949e', fontWeight: '600' }}>🗄️ Databases & Cache:</span>
      <div style={{ display: 'flex', gap: '8px' }}>
        <span style={{ padding: '4px 10px', background: '#4169E122', border: '1px solid #4169E1', borderRadius: '6px', fontSize: '12px', color: '#4169E1', fontWeight: 'bold' }}>PostgreSQL</span>
        <span style={{ padding: '4px 10px', background: '#4479A122', border: '1px solid #4479A1', borderRadius: '6px', fontSize: '12px', color: '#4479A1', fontWeight: 'bold' }}>MySQL</span>
        <span style={{ padding: '4px 10px', background: '#D1191922', border: '1px solid #D11919', borderRadius: '6px', fontSize: '12px', color: '#D11919', fontWeight: 'bold' }}>SQLAlchemy</span>
      </div>
    </div>

    {/* Row 3 */}
    <div style={{ display: 'flex', alignItems: 'center' }}>
      <span style={{ width: '180px', fontSize: '14px', color: '#8b949e', fontWeight: '600' }}>🧩 Frontend:</span>
      <div style={{ display: 'flex', gap: '8px' }}>
        <span style={{ padding: '4px 10px', background: '#61DAFB22', border: '1px solid #61DAFB', borderRadius: '6px', fontSize: '12px', color: '#61DAFB', fontWeight: 'bold' }}>React</span>
        <span style={{ padding: '4px 10px', background: '#3178C622', border: '1px solid #3178C6', borderRadius: '6px', fontSize: '12px', color: '#3178C6', fontWeight: 'bold' }}>TypeScript</span>
      </div>
    </div>

    {/* Row 4 */}
    <div style={{ display: 'flex', alignItems: 'center' }}>
      <span style={{ width: '180px', fontSize: '14px', color: '#8b949e', fontWeight: '600' }}>☁️ DevOps & Tools:</span>
      <div style={{ display: 'flex', gap: '8px' }}>
        <span style={{ padding: '4px 10px', background: '#2496ED22', border: '1px solid #2496ED', borderRadius: '6px', fontSize: '12px', color: '#2496ED', fontWeight: 'bold' }}>Docker</span>
        <span style={{ padding: '4px 10px', background: '#2088FF22', border: '1px solid #2088FF', borderRadius: '6px', fontSize: '12px', color: '#2088FF', fontWeight: 'bold' }}>GitHub Actions</span>
        <span style={{ padding: '4px 10px', background: '#0089D622', border: '1px solid #0089D6', borderRadius: '6px', fontSize: '12px', color: '#0089D6', fontWeight: 'bold' }}>Azure</span>
      </div>
    </div>
  </div>

  <div style={{ borderTop: '1px solid #21262d', paddingTop: '10px', display: 'flex', justifyContent: 'space-between', fontSize: '11px', color: '#8b949e' }}>
    <span>* Compiled dynamically using Vercel Satori vectors</span>
    <span>sivabalan.xyz</span>
  </div>
</div>
```

---

```aura width=800 height=380 align=center
<div style={{
  display: 'flex',
  flexDirection: 'column',
  width: '800px',
  height: '380px',
  background: '#0d1117',
  border: '1px solid #30363d',
  borderRadius: '16px',
  padding: '24px',
  fontFamily: 'Inter, system-ui, sans-serif',
  color: '#c9d1d9',
  justifyContent: 'space-between'
}}>
  <div style={{ display: 'flex', flexDirection: 'column' }}>
    <span style={{ fontSize: '20px', fontWeight: '700', color: '#ffffff', borderBottom: '1px solid #21262d', paddingBottom: '10px' }}>
      🧭 Featured Engineering Projects
    </span>
  </div>

  <div style={{ display: 'flex', gap: '15px' }}>
    {/* Card 1 */}
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, padding: '16px', background: '#161b22', border: '1px solid #21262d', borderRadius: '10px', height: '240px', justifyContent: 'space-between' }}>
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <span style={{ fontSize: '15px', fontWeight: 'bold', color: '#58a6ff' }}>🧮 SQL Perf Visualizer</span>
        <span style={{ fontSize: '12px', color: '#8b949e', marginTop: '6px', lineHeight: '1.4' }}>
          Visual compare of query EXPLAIN plans to debug slow lookups in joins/scans.
        </span>
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: '4px', fontSize: '10px', color: '#00BFFF', fontWeight: '600' }}>
        <span>#FastAPI</span>
        <span>#React</span>
        <span>#PostgreSQL</span>
      </div>
    </div>

    {/* Card 2 */}
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, padding: '16px', background: '#161b22', border: '1px solid #21262d', borderRadius: '10px', height: '240px', justifyContent: 'space-between' }}>
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <span style={{ fontSize: '15px', fontWeight: 'bold', color: '#58a6ff' }}>🚗 WhosOn Route</span>
        <span style={{ fontSize: '12px', color: '#8b949e', marginTop: '6px', lineHeight: '1.4' }}>
          Real-time office ride sharing. Pub/sub worker channels for driver coordinate matching.
        </span>
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: '4px', fontSize: '10px', color: '#00BFFF', fontWeight: '600' }}>
        <span>#Tornado</span>
        <span>#React</span>
        <span>#Docker</span>
      </div>
    </div>

    {/* Card 3 */}
    <div style={{ display: 'flex', flexDirection: 'column', flex: 1, padding: '16px', background: '#161b22', border: '1px solid #21262d', borderRadius: '10px', height: '240px', justifyContent: 'space-between' }}>
      <div style={{ display: 'flex', flexDirection: 'column' }}>
        <span style={{ fontSize: '15px', fontWeight: 'bold', color: '#58a6ff' }}>🧠 AI Sentiment (POC)</span>
        <span style={{ fontSize: '12px', color: '#8b949e', marginTop: '6px', lineHeight: '1.4' }}>
          NLP worker pipelines that ingest customer reviews and build feedback insights.
        </span>
      </div>
      <div style={{ display: 'flex', flexWrap: 'wrap', gap: '4px', fontSize: '10px', color: '#00BFFF', fontWeight: '600' }}>
        <span>#FastAPI</span>
        <span>#OpenAI</span>
        <span>#Docker</span>
      </div>
    </div>
  </div>
</div>
```

---

```aura width=800 height=380 align=center
<div style={{
  display: 'flex',
  flexDirection: 'column',
  width: '800px',
  height: '380px',
  background: 'linear-gradient(135deg, #0d1117 0%, #151b23 100%)',
  border: '1px solid #30363d',
  borderRadius: '16px',
  padding: '24px',
  fontFamily: 'Inter, system-ui, sans-serif',
  color: '#c9d1d9',
  justifyContent: 'space-between'
}}>
  <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'center', borderBottom: '1px solid #21262d', paddingBottom: '10px' }}>
    <span style={{ fontSize: '20px', fontWeight: '700', color: '#ffffff' }}>
      🤖 AI, LLM & Workflow Automation
    </span>
    <span style={{ fontSize: '11px', color: '#00BFFF', background: '#00BFFF22', border: '1px solid #00BFFF', padding: '3px 8px', borderRadius: '12px' }}>
      Active Engineering
    </span>
  </div>

  <div style={{ display: 'flex', flexDirection: 'column', gap: '15px' }}>
    {/* Topic 1 */}
    <div style={{ display: 'flex', gap: '15px', alignItems: 'flex-start' }}>
      <div style={{ fontSize: '24px', padding: '10px', background: '#161b22', border: '1px solid #21262d', borderRadius: '10px' }}>🧠</div>
      <div style={{ display: 'flex', flexDirection: 'column', flex: 1 }}>
        <span style={{ fontSize: '15px', fontWeight: 'bold', color: '#ffffff' }}>NLP Sentiment Feedback Pipeline</span>
        <span style={{ fontSize: '12px', color: '#8b949e', marginTop: '4px', lineHeight: '1.4' }}>
          Ingests customer support logs, routes through semantic analyzers (OpenAI APIs), and structures profiles to identify pain points and satisfaction trends.
        </span>
      </div>
    </div>

    {/* Topic 2 */}
    <div style={{ display: 'flex', gap: '15px', alignItems: 'flex-start' }}>
      <div style={{ fontSize: '24px', padding: '10px', background: '#161b22', border: '1px solid #21262d', borderRadius: '10px' }}>⚙️</div>
      <div style={{ display: 'flex', flexDirection: 'column', flex: 1 }}>
        <span style={{ fontSize: '15px', fontWeight: 'bold', color: '#ffffff' }}>LLM Agentic Workflow Automation</span>
        <span style={{ fontSize: '12px', color: '#8b949e', marginTop: '4px', lineHeight: '1.4' }}>
          Building reliable agent loops that leverage tools (APIs, databases, bash) to automate high-friction development tasks and orchestrate microservice checks.
        </span>
      </div>
    </div>
  </div>

  <div style={{ display: 'flex', gap: '8px', borderTop: '1px solid #21262d', paddingTop: '12px', fontSize: '11px', color: '#8b949e' }}>
    <span>💡 Core Tech:</span>
    <span style={{ color: '#00BFFF' }}>LangChain</span>
    <span>•</span>
    <span style={{ color: '#00BFFF' }}>OpenAI / Gemini APIs</span>
    <span>•</span>
    <span style={{ color: '#00BFFF' }}>FastAPI Background Tasks</span>
  </div>
</div>
```

---

### 💬 Let's Connect

<p align="center">
  <a href="https://sivabalan.xyz" target="_blank">
    <img src="https://img.shields.io/badge/Website-sivabalan.xyz-00BFFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website" />
  </a>
  <a href="https://www.linkedin.com/in/sivacsus/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Sivabalan-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://github.com/sivabalanb" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-sivabalanb-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</p>
