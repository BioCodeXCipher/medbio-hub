<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BioPath \u2014 Biology Career Mentor</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=Instrument+Serif:ital@0;1&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #f7f3ec;
  --ink: #1a1208;
  --green: #1d6b3a;
  --green-light: #e8f5ed;
  --green-mid: #2d8a4e;
  --amber: #c97c1a;
  --amber-light: #fef3e0;
  --rose: #b5383a;
  --rose-light: #fdeaea;
  --sky: #1a5d8a;
  --sky-light: #e8f2fa;
  --violet: #5c2d91;
  --violet-light: #f0ebf8;
  --teal: #1a7a6e;
  --teal-light: #e8f6f4;
  --border: #d6cdb8;
  --muted: #7a6e5a;
  --surface: #fff;
  --surface2: #f0ead9;
}

* { margin:0; padding:0; box-sizing:border-box; }

body {
  font-family: 'Syne', sans-serif;
  background: var(--bg);
  color: var(--ink);
  min-height: 100vh;
  overflow-x: hidden;
}

/* \u2500\u2500 NAV \u2500\u2500 */
nav {
  position: sticky; top: 0; z-index: 100;
  background: var(--ink);
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 28px;
  height: 56px;
  border-bottom: 2px solid var(--green);
}
.nav-logo {
  font-family: 'Instrument Serif', serif;
  font-size: 1.4rem; color: #fff;
  display: flex; align-items: center; gap: 8px;
}
.nav-logo span { color: #6ee89a; font-style: italic; }
.nav-links {
  display: flex; gap: 4px; flex-wrap: wrap;
}
.nav-links a {
  font-size: 11px; letter-spacing: 0.08em; text-transform: uppercase;
  color: #aaa; padding: 6px 10px; border-radius: 3px;
  cursor: pointer; border: none; background: none;
  transition: all 0.2s; white-space: nowrap;
}
.nav-links a:hover, .nav-links a.active { color: #6ee89a; background: rgba(110,232,154,0.08); }

/* \u2500\u2500 HERO \u2500\u2500 */
.hero {
  background: var(--ink);
  padding: 70px 40px 60px;
  text-align: center;
  position: relative; overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute; inset: 0;
  background: radial-gradient(ellipse 70% 60% at 50% 100%, rgba(29,107,58,0.35) 0%, transparent 70%);
}
.hero-eyebrow {
  font-family: 'JetBrains Mono', monospace;
  font-size: 11px; letter-spacing: 0.25em; text-transform: uppercase;
  color: #6ee89a; margin-bottom: 18px;
  position: relative;
}
.hero h1 {
  font-family: 'Instrument Serif', serif;
  font-size: clamp(2.8rem, 7vw, 5.5rem);
  color: #fff; line-height: 1.05;
  position: relative; margin-bottom: 16px;
}
.hero h1 em { color: #6ee89a; font-style: italic; }
.hero p {
  color: #aaa; font-size: 1rem; max-width: 560px;
  margin: 0 auto 36px; line-height: 1.7; position: relative;
}

/* Tab Pills */
.level-tabs {
  display: flex; gap: 8px; justify-content: center; flex-wrap: wrap;
  position: relative;
}
.level-tab {
  padding: 10px 22px; border-radius: 50px;
  border: 1.5px solid #333; background: transparent;
  color: #ccc; font-family: 'Syne', sans-serif; font-size: 13px; font-weight: 600;
  cursor: pointer; transition: all 0.25s;
}
.level-tab:hover { border-color: #6ee89a; color: #6ee89a; }
.level-tab.active { background: #6ee89a; border-color: #6ee89a; color: var(--ink); }

/* \u2500\u2500 AI MENTOR CHAT \u2500\u2500 */
.ai-section {
  background: var(--ink);
  padding: 0 0 60px;
}
.ai-box {
  max-width: 820px; margin: 0 auto; padding: 0 20px;
}
.ai-header {
  text-align: center; padding: 40px 0 28px;
}
.ai-header h2 {
  font-family: 'Instrument Serif', serif; font-size: 1.9rem; color: #fff;
  margin-bottom: 8px;
}
.ai-header p { color: #888; font-size: 0.9rem; }
.ai-badge {
  display: inline-block;
  font-family: 'JetBrains Mono', monospace; font-size: 10px;
  background: rgba(110,232,154,0.12); color: #6ee89a;
  border: 1px solid rgba(110,232,154,0.3);
  padding: 3px 10px; border-radius: 2px; margin-bottom: 10px;
  letter-spacing: 0.15em; text-transform: uppercase;
}

/* Quick prompts */
.quick-prompts {
  display: flex; gap: 8px; flex