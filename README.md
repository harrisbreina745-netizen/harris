# HerInner


<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>HerInner — Daily Tips</title>
<style>
  :root {
    --bg: #ffffff;
    --ink: #222222;
    --soft: #6d5ba6;
    --muted: #666;
    --card: #faf8ff;
  }
  body {
    margin: 0;
    font-family: system-ui, Arial, sans-serif;
    color: var(--ink);
    background: var(--bg);
    line-height: 1.6;
  }
  header { background: #fff; border-bottom: 1px solid #eee; position: sticky; top: 0; }
  .wrap { max-width: 1000px; margin: 0 auto; padding: 0 20px; }
  nav { display: flex; gap: 18px; padding: 14px 0; flex-wrap: wrap; align-items: center; }
  nav a { text-decoration: none; color: var(--ink); font-weight: 600; }
  nav a:hover { color: var(--soft); }
  .brand { margin-right: auto; font-weight: 800; color: var(--soft); }
  .hero { padding: 60px 0 30px; background: radial-gradient(1000px 400px at 20% -10%, #efeaff 0%, #fff 70%); }
  .hero h1 { font-size: clamp(28px, 5vw, 42px); margin-bottom: 12px; }
  .hero p { font-size: clamp(16px, 3.4vw, 19px); color: var(--muted); max-width: 850px; }

  section { padding: 40px 0; }
  h2 { font-size: clamp(22px, 4vw, 30px); margin-bottom: 24px; color: var(--soft); }

  /* Magazine-style tip cards */
  .tip-card {
    display: flex;
    gap: 20px;
    background: var(--card);
    border-radius: 12px;
    overflow: hidden;
    margin-bottom: 30px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    flex-wrap: wrap;
  }
  .tip-card img {
    flex: 1 1 300px;
    width: 100%;
    height: auto;
    object-fit: cover;
  }
  .tip-content {
    flex: 2 1 400px;
    padding: 20px;
    display: flex;
    flex-direction: column;
  }
  .tip-content h3 { margin-top: 0; color: var(--soft); }
  .tip-content p { margin-bottom: 12px; }

  .share-btn {
    margin-right: 8px;
    margin-top: 6px;
    padding: 6px 12px;
    font-size: 14px;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    background: var(--soft);
    color: #fff;
  }
  .share-btn:hover { filter: brightness(0.9); }

  footer { border-top: 1px solid #eee; padding: 24px 0 60px; color: var(--muted); font-size: 14px; text-align: center; }

  /* Responsive */
  @media(max-width:800px){
    .tip-card { flex-direction: column; }
    .tip-content { flex: 1 1 100%; }
  }
</style>
</head>
<body>

<header>
  <div class="wrap">
    <nav>
      <div class="brand">HerInner</div>
      <a href="#home">Home</a>
      <a href="#daily-tip">Daily Tips</a>
      <a href="#purpose">Purpose</a>
      <a href="#wealth">Wealth</a>
      <a href="#community">Community</a>
      <a href="#about">About</a>
    </nav>
  </div>
</header>

<main id="home" class="hero">
  <div class="wrap">
    <h1>Daily encouragement for single moms and young professionals.</h1>
    <p>
      HerInner gives you clear, supportive tips every day—whether you’re raising kids on your own or building your career. Come here daily for wisdom on purpose, money, and inner strength.
    </p>
  </div>
</main>

<section id="daily-tip">
  <div class="wrap">
    <h2>Daily Tips</h2>

    <!-- Purpose Tip -->
    <div class="tip-card">
      <img id="purposeImg" src="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?crop=entropy&cs=tinysrgb&fit=max&h=400&w=800" alt="Woman planning her goals">
      <div class="tip-content">
        <h3>🌸 Purpose Tip</h3>
        <p id="purposeTip">Loading...</p>
        <div>
          <button class="share-btn" onclick="shareTip('purposeTip')">WhatsApp</button>
          <button class="share-btn" onclick="shareTipTwitter('purposeTip')">Twitter</button>
          <button class="share-btn" onclick="copyTip('purposeTip')">Copy</button>
        </div>
      </div>
    </div>

    <!-- Money Tip -->
    <div class="tip-card">
      <img id="moneyImg" src="https://images.unsplash.com/photo-1554224154-22dec7ec8818?crop=entropy&cs=tinysrgb&fit=max&h=400&w=800" alt="Woman budgeting">
      <div class="tip-content">
        <h3>💰 Money Tip</h3>
        <p id="moneyTip">Loading...</p>
        <div>
          <button class="share-btn" onclick="shareTip('moneyTip')">WhatsApp</button>
          <button class="share-btn" onclick="shareTipTwitter('moneyTip')">Twitter</button>
          <button class="share-btn" onclick="copyTip('moneyTip')">Copy</button>
        </div>
      </div>
    </div>

    <!-- Encouragement Tip -->
    <div class="tip-card">
      <img id="encourageImg" src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?crop=entropy&cs=tinysrgb&fit=max&h=400&w=800" alt="Happy woman">
      <div class="tip-content">
        <h3>🤱 Encouragement</h3>
        <p id="encourageTip">Loading...</p>
        <div>
          <button class="share-btn" onclick="shareTip('encourageTip')">WhatsApp</button>
          <button class="share-btn" onclick="shareTipTwitter('encourageTip')">Twitter</button>
          <button class="share-btn" onclick="copyTip('encourageTip')">Copy</button>
        </div>
      </div>
    </div>

  </div>
</section>

<footer>
  <p>© <span id="year"></span> HerInner. All rights reserved.</p>
</footer>

<script>
  const purposeTips = [
    "Purpose grows when you serve others. Look for one person you can help today. Your actions inspire not only yourself but those around you.",
    "If you feel lost, list what excites you and what drains you. Passion often points to purpose. Small daily steps will guide your path.",
    "Purpose is revealed in small steps, not giant leaps. Start with what’s in front of you and celebrate tiny wins."
  ];
  const moneyTips = [
    "Automate savings—even $10 per week builds financial freedom. Consider budgeting apps to make it easier.",
    "Track your spending for one week. Awareness is the first step to wealth. Review and adjust weekly for better control.",
    "Invest in skills. They pay the best interest over time and increase both income and confidence."
  ];
  const encourageTips = [
    "Single moms: You’re doing enough. Your love is your children’s foundation. Remember to give yourself grace.",
    "Young professionals: Don’t compare your chapter 1 to someone’s chapter 10. Growth takes time and patience.",
    "Take a breath. You’re allowed to rest without losing progress. Even short breaks boost focus and clarity."
  ];

  const today = new Date();
  const index = today.getDate();
  document.getElementById("purposeTip").textContent = purposeTips[index % purposeTips.length];
  document.getElementById("moneyTip").textContent = moneyTips[index % moneyTips.length];
  document.getElementById("encourageTip").textContent = encourageTips[index % encourageTips.length];

  document.getElementById("year").textContent = today.getFullYear();

  // Share functions
  function shareTip(id){
    const tip = document.getElementById(id).textContent;
    const shareText = encodeURIComponent(tip + " — via HerInner");
    window.open("https://api.whatsapp.com/send?text=" + shareText, "_blank");
  }
  function shareTipTwitter(id){
    const tip = document.getElementById(id).textContent;
    const url = encodeURIComponent("https://herinner.com"); // Replace with your site URL
    const text = encodeURIComponent(tip + " — via HerInner");
    window.open(`https://twitter.com/intent/tweet?text=${text}&url=${url}`, "_blank");
  }
  function copyTip(id){
    const tip = document.getElementById(id).textContent;
    navigator.clipboard.writeText(tip + " — via HerInner")
      .then(()=>alert("Tip copied to clipboard!"))
      .catch(()=>alert("Failed to copy."));
  }
</script>

</body>
</html>
```

