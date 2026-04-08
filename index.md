---
layout: null
permalink: /
sitemap: false
---
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Independent Compute Domain</title>
<link rel="alternate" hreflang="ja" href="https://icdomain.github.io/ja/">
<link rel="alternate" hreflang="en" href="https://icdomain.github.io/en/">
<link rel="alternate" hreflang="x-default" href="https://icdomain.github.io/en/">
<meta name="robots" content="noindex">
<script>
(function() {
  var chosen = null;
  try { chosen = localStorage.getItem('icd-lang'); } catch(e) {}
  if (chosen === 'ja' || chosen === 'en') {
    location.replace('/' + chosen + '/');
    return;
  }
  var lang = (navigator.language || navigator.userLanguage || 'en').toLowerCase();
  var target = lang.indexOf('ja') === 0 ? 'ja' : 'en';
  location.replace('/' + target + '/');
})();
</script>
</head>
<body>
<noscript>
  <p><a href="/en/">English</a> / <a href="/ja/">日本語</a></p>
</noscript>
</body>
</html>
