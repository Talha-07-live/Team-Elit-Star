<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="theme-color" content="#0b1020" />
  <title>Preparing your download</title>
  <style>
    :root {
      --bg: #070b16;
      --card: rgba(18, 26, 52, .78);
      --border: rgba(255,255,255,.12);
      --text: #f5f7ff;
      --muted: #a8b2cf;
      --primary: #7c5cff;
      --secondary: #19d3ae;
      --danger: #ff6b81;
    }

    * { box-sizing: border-box; }
    body {
      margin: 0;
      min-height: 100vh;
      display: grid;
      place-items: center;
      padding: 24px;
      color: var(--text);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, Segoe UI, sans-serif;
      background:
        radial-gradient(circle at 15% 15%, rgba(124,92,255,.22), transparent 32%),
        radial-gradient(circle at 85% 85%, rgba(25,211,174,.14), transparent 30%), var(--bg);
    }

    .shell { width: min(100%, 560px); }
    .brand { text-align: center; margin-bottom: 18px; color: var(--muted); font-size: 13px; letter-spacing: .16em; text-transform: uppercase; }
    .card {
      position: relative;
      overflow: hidden;
      padding: clamp(26px, 6vw, 44px);
      border: 1px solid var(--border);
      border-radius: 28px;
      background: linear-gradient(145deg, rgba(27,38,76,.86), var(--card));
      box-shadow: 0 25px 80px rgba(0,0,0,.36), inset 0 1px rgba(255,255,255,.06);
      backdrop-filter: blur(18px);
    }
    .card::before { content: ""; position: absolute; width: 180px; height: 180px; right: -80px; top: -80px; border-radius: 50%; background: rgba(124,92,255,.28); filter: blur(25px); }
    .icon { width: 76px; height: 76px; display: grid; place-items: center; margin: 0 auto 22px; border-radius: 24px; background: linear-gradient(135deg, var(--primary), #a88dff); box-shadow: 0 12px 30px rgba(124,92,255,.35); font-size: 35px; }
    h1 { position: relative; margin: 0 0 10px; text-align: center; font-size: clamp(25px, 5vw, 34px); }
    .subtitle { position: relative; margin: 0 auto 28px; max-width: 410px; color: var(--muted); text-align: center; line-height: 1.65; }
    .status { display: flex; align-items: center; gap: 10px; justify-content: center; margin-bottom: 24px; color: var(--secondary); font-weight: 700; }
    .dot { width: 9px; height: 9px; border-radius: 50%; background: currentColor; box-shadow: 0 0 0 6px rgba(25,211,174,.12); animation: pulse 1.4s infinite; }
    @keyframes pulse { 50% { transform: scale(.65); opacity: .55; } }
    .progress-wrap { position: relative; height: 11px; overflow: hidden; border-radius: 100px; background: rgba(255,255,255,.1); }
    .progress { width: 0%; height: 100%; border-radius: inherit; background: linear-gradient(90deg, var(--primary), var(--secondary)); transition: width .45s ease; }
    .meta { display: flex; justify-content: space-between; gap: 12px; margin-top: 11px; color: var(--muted); font-size: 13px; }
    .count { color: var(--text); font-weight: 800; }
    .actions { display: flex; gap: 12px; margin-top: 28px; }
    button, .button { flex: 1; border: 0; border-radius: 14px; padding: 14px 18px; font: inherit; font-weight: 800; cursor: pointer; text-align: center; text-decoration: none; transition: transform .2s, opacity .2s, box-shadow .2s; }
    button:hover, .button:hover { transform: translateY(-2px); }
    .primary { color: #fff; background: linear-gradient(135deg, var(--primary), #6246df); box-shadow: 0 10px 24px rgba(124,92,255,.28); }
    .secondary { color: var(--text); background: rgba(255,255,255,.09); border: 1px solid var(--border); }
    button:disabled { opacity: .5; cursor: not-allowed; transform: none; box-shadow: none; }
    .destination { margin-top: 25px; padding: 13px 15px; border: 1px solid var(--border); border-radius: 12px; color: var(--muted); font-size: 12px; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
    .destination strong { color: var(--text); }
    .footer { margin-top: 18px; color: #7782a3; font-size: 12px; text-align: center; }
    .error { color: var(--danger); }
    @media (max-width: 430px) { .actions { flex-direction: column; } }
  </style>
</head>
<body>
  <main class="shell">
    <div class="brand">Secure download gateway</div>
    <section class="card" aria-live="polite">
      <div class="icon" id="icon">↓</div>
      <h1 id="title">Your download is ready</h1>
      <p class="subtitle" id="subtitle">You will be securely redirected to the destination page. Please wait a few seconds.</p>

      <div class="status" id="status"><span class="dot"></span><span id="statusText">Verifying your link...</span></div>
      <div class="progress-wrap"><div class="progress" id="progress"></div></div>
      <div class="meta"><span id="progressText">Preparing download</span><span class="count" id="count">05s</span></div>

      <div class="actions">
        <button class="primary" id="continueBtn" disabled>Continue now</button>
        <button class="secondary" id="cancelBtn">Cancel</button>
      </div>

      <div class="destination"><strong>Destination:</strong> <span id="destinationText">https://example.com/download</span></div>
    </section>
    <div class="footer">Your data is not being stored • SSL secured connection</div>
  </main>

  <script>
    // ====== Easy configuration ======
    const REDIRECT_URL = "https://github.com/Talha-07-live/Team-Elit-Star/raw/refs/heads/main/app.apk";
    const COUNTDOWN_SECONDS = 5;
    const AUTO_REDIRECT = true;
    // =====================================

    const $ = (id) => document.getElementById(id);
    const state = { remaining: COUNTDOWN_SECONDS, cancelled: false, timer: null };

    $("destinationText").textContent = REDIRECT_URL;
    $("count").textContent = String(state.remaining).padStart(2, "0") + "s";

    function goToDestination() {
      if (state.cancelled) return;
      $("statusText").textContent = "Redirecting now...";
      $("progressText").textContent = "Complete";
      $("progress").style.width = "100%";
      window.location.assign(REDIRECT_URL);
    }

    function finish() {
      $("continueBtn").disabled = false;
      $("statusText").textContent = "Ready to continue";
      $("progressText").textContent = "Ready";
      $("count").textContent = "00s";
      if (AUTO_REDIRECT) setTimeout(goToDestination, 450);
    }

    function tick() {
      const elapsed = COUNTDOWN_SECONDS - state.remaining;
      $("progress").style.width = ((elapsed / COUNTDOWN_SECONDS) * 100) + "%";
      if (state.remaining <= 0) return finish();
      state.remaining -= 1;
      $("count").textContent = String(state.remaining).padStart(2, "0") + "s";
      state.timer = setTimeout(tick, 1000);
    }

    $("continueBtn").addEventListener("click", goToDestination);
    $("cancelBtn").addEventListener("click", () => {
      state.cancelled = true;
      clearTimeout(state.timer);
      $("status").classList.add("error");
      $("statusText").textContent = "Redirect cancelled";
      $("progressText").textContent = "Cancelled";
      $("icon").textContent = "×";
      $("continueBtn").disabled = false;
      $("continueBtn").textContent = "Continue anyway";
    });

    tick();
  </script>
</body>
</html>
