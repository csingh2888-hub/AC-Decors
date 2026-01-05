# AC-Decors
Official website for AC Decords – PVC panel, false ceiling &amp; interior decoration services.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AC Decords | PVC Panel Work</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f4f4f4;
    }
    header {
      background: #1e293b;
      color: #fff;
      padding: 15px;
      text-align: center;
    }
    nav {
      background: #334155;
      padding: 10px;
      text-align: center;
    }
    nav button {
      margin: 5px;
      padding: 8px 14px;
      border: none;
      cursor: pointer;
      background: #0ea5e9;
      color: white;
      border-radius: 5px;
    }
    .container {
      padding: 20px;
    }
    .card {
      background: #fff;
      padding: 15px;
      margin-bottom: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .editable {
      border: 1px dashed #94a3b8;
      padding: 6px;
    }
    .editable:focus {
      outline: 2px solid #0ea5e9;
      background: #f8fafc;
    }

    /* Gallery */
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 15px;
    }
    .gallery img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 8px;
    }

    footer {
      background: #1e293b;
      color: #fff;
      text-align: center;
      padding: 10px;
    }

    /* WhatsApp Button */
    .whatsapp {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #25d366;
      color: white;
      padding: 14px 16px;
      border-radius: 50%;
      font-size: 22px;
      text-decoration: none;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
  </style>
</head>

<body>

<header>
  <h1 contenteditable="true" class="editable">AC Decords</h1>
  <p contenteditable="true" class="editable">PVC Panel & Interior Work</p>
</header>

<nav>
  <button type="button" onclick="showSection('home')">Home</button>
  <button type="button" onclick="showSection('services')">Services</button>
  <button type="button" onclick="showSection('gallery')">Gallery</button>
  <button type="button" onclick="showSection('contact')">Contact</button>
</nav>

<div class="container" id="editableContent">

  <div id="home" class="card section">
    <h2 contenteditable="true" class="editable">Welcome</h2>
    <p contenteditable="true" class="editable">
      We provide premium PVC panel ceiling, wall, and interior decoration services.
    </p>
  </div>

  <div id="services" class="card section" style="display:none;">
    <h2 contenteditable="true" class="editable">Our Services</h2>
    <ul>
      <li><span contenteditable="true" class="editable">PVC Ceiling Panels</span></li>
      <li><span contenteditable="true" class="editable">Wall Panels</span></li>
      <li><span contenteditable="true" class="editable">Modular Interior Design</span></li>
      <li><span contenteditable="true" class="editable">False Ceiling Work</span></li>
    </ul>
  </div>

  <div id="gallery" class="card section" style="display:none;">
    <h2>Our Work Gallery</h2>
    <div class="gallery">
      <img src="https://picsum.photos/400/300?random=1">
      <img src="https://picsum.photos/400/300?random=2">
      <img src="https://picsum.photos/400/300?random=3">
      <img src="https://picsum.photos/400/300?random=4">
      <img src="https://picsum.photos/400/300?random=5">
      <img src="https://picsum.photos/400/300?random=6">
    </div>
  </div>

  <div id="contact" class="card section" style="display:none;">
    <h2 contenteditable="true" class="editable">Contact Us</h2>
    <p contenteditable="true" class="editable">📞 Phone: 9XXXXXXXXX</p>
    <p contenteditable="true" class="editable">📍 Location: Your City</p>
  </div>

  <button type="button" onclick="saveContent()">💾 Save Changes</button>

</div>

<footer>
  <p contenteditable="true" class="editable">© 2026 AC Decords</p>
</footer>

<!-- WhatsApp Button -->
<a class="whatsapp" href="https://wa.me/919XXXXXXXXX" target="_blank">💬</a>

<script>
  function showSection(id) {
    document.querySelectorAll('.section').forEach(sec => sec.style.display = 'none');
    document.getElementById(id).style.display = 'block';
  }

  function saveContent() {
    const content = document.getElementById('editableContent').innerHTML;
    localStorage.setItem('acDecordsData', content);
    alert('Content Saved!');
  }

  window.onload = function () {
    const saved = localStorage.getItem('acDecordsData');
    if (saved) {
      document.getElementById('editableContent').innerHTML = saved;
    }
  };
</script>

</body>
</html>
