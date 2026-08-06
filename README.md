# PROJETO-CSS-1.0
/* ============================================================
   1. CONFIGURAÇÕES BASE (RESETS E ESTRUTURA GLOBAL)
   ============================================================ */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
}

body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  transition: background-color 0.4s ease, color 0.4s ease;
}

/* --- Layout do Card --- */
.card {
  width: 100%;
  max-width: 360px;
  padding: 32px 24px;
  border-radius: 24px;
  text-align: center;
  transition: all 0.4s ease;
}

/* --- Elementos Internos --- */
.profile-img {
  width: 96px;
  height: 96px;
  border-radius: 50%;
  margin-bottom: 16px;
  object-fit: cover;
}

h1 {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 6px;
}

.bio {
  font-size: 0.95rem;
  margin-bottom: 24px;
  opacity: 0.85;
}

/* --- Menu de Seleção de Temas --- */
.style-picker {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-bottom: 28px;
}

.style-picker button {
  padding: 8px 16px;
  border-radius: 12px;
  border: none;
  font-size: 0.85rem;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.style-picker button:active {
  transform: scale(0.95);
}

/* --- Botões de Links --- */
.links {
  display: flex;
  flex-direction: column;
  gap: 14px;
}

.btn {
  display: block;
  text-decoration: none;
  padding: 14px 20px;
  border-radius: 14px;
  font-weight: 600;
  font-size: 0.95rem;
  transition: all 0.3s ease;
}

.btn:hover {
  transform: translateY(-2px);
}


/* ============================================================
   2. ESTILO 1: CLEAN / MINIMALISTA
   ============================================================ */

body.theme-clean {
  --bg-body: #f8fafc;
  --bg-card: #ffffff;
  --text-main: #0f172a;
  --btn-bg: #2563eb;
  --btn-text: #ffffff;
  --picker-bg: #e2e8f0;
  --picker-text: #334155;
  --shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.05);

  background-color: var(--bg-body);
  color: var(--text-main);
}

.theme-clean .card {
  background-color: var(--bg-card);
  box-shadow: var(--shadow);
}

.theme-clean .btn {
  background-color: var(--btn-bg);
  color: var(--btn-text);
}

.theme-clean .btn:hover {
  background-color: #1d4ed8;
  box-shadow: 0 10px 15px -3px rgba(37, 99, 235, 0.3);
}

.theme-clean .style-picker button {
  background-color: var(--picker-bg);
  color: var(--picker-text);
}


/* ============================================================
   3. ESTILO 2: GLASSMORPHISM (Efeito Vidro Fosco)
   ============================================================ */

body.theme-glass {
  --text-main: #ffffff;
  --glass-bg: rgba(255, 255, 255, 0.12);
  --glass-border: rgba(255, 255, 255, 0.25);
  --glass-blur: blur(16px);

  background: linear-gradient(135deg, #4f46e5 0%, #7c3aed 50%, #db2777 100%);
  color: var(--text-main);
}

.theme-glass .card {
  background: var(--glass-bg);
  backdrop-filter: var(--glass-blur);
  -webkit-backdrop-filter: var(--glass-blur);
  border: 1px solid var(--glass-border);
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
}

.theme-glass .btn {
  background: rgba(255, 255, 255, 0.2);
  color: var(--text-main);
  border: 1px solid var(--glass-border);
}

.theme-glass .btn:hover {
  background: rgba(255, 255, 255, 0.35);
}

.theme-glass .style-picker button {
  background: rgba(255, 255, 255, 0.2);
  color: var(--text-main);
  border: 1px solid rgba(255, 255, 255, 0.15);
}


/* ============================================================
   4. ESTILO 3: NEOMORPHISM (Soft UI / Efeito 3D)
   ============================================================ */

body.theme-neo {
  --bg-neo: #e0e5ec;
  --text-neo: #2d3748;
  --shadow-light: #ffffff;
  --shadow-dark: #a3b1c6;

  background-color: var(--bg-neo);
  color: var(--text-neo);
}

.theme-neo .card {
  background-color: var(--bg-neo);
  box-shadow: 9px 9px 16px var(--shadow-dark), 
             -9px -9px 16px var(--shadow-light);
}

.theme-neo .btn {
  background-color: var(--bg-neo);
  color: var(--text-neo);
  box-shadow: 6px 6px 12px var(--shadow-dark), 
             -6px -6px 12px var(--shadow-light);
}

.theme-neo .btn:active {
  box-shadow: inset 4px 4px 8px var(--shadow-dark), 
              inset -4px -4px 8px var(--shadow-light);
}

.theme-neo .style-picker button {
  background-color: var(--bg-neo);
  color: var(--text-neo);
  box-shadow: 3px 3px 6px var(--shadow-dark), 
             -3px -3px 6px var(--shadow-light);
}
