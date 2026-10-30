
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Security Management System</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f1f5f9;
  color: #172554;
}
header {
  background: #12345a;
  color: white;
  padding: 22px;
}
header h2 { margin: 0; }
header p { margin-bottom: 0; color: #dbeafe; }
nav {
  display: flex;
  flex-wrap: wrap;
  background: #1e293b;
}
nav button {
  flex: 1;
  min-width: 100px;
  padding: 14px 8px;
  border: 0;
  background: transparent;
  color: white;
  cursor: pointer;
}
nav button:hover { background: #334155; }
main { padding: 18px; }
.card {
  background: white;
  padding: 18px;
  margin-bottom: 15px;
  border-radius: 10px;
  box-shadow: 0 2px 7px #0001;
}
input, select, textarea {
  width: 100%;
  padding: 12px;
  margin: 8px 0 14px;
  border: 1px solid #cbd5e1;
  border-radius: 6px;
}
.action {
  background: #12345a;
  color: white;
  border: 0;
  padding: 12px 18px;
  border-radius: 6px;
}
.page { display: none; }
.page.active { display: block; }
</style>
</head>
<body>

<header>
<h2>SECURITY MANAGEMENT SYSTEM</h2>
<p>Operational Information Dashboard</p>
</header>

<nav>
<button onclick="showPage('home')">Dashboard</button>
<button onclick="showPage('incidents')">Incidents</button>
<button onclick="showPage('patrols')">Patrols</button>
<button onclick="showPage('personnel')">Personnel</button>
<button onclick="showPage('operations')">Operations</button>
<button onclick="showPage('vehicles')">Vehicles</button>
<button onclick="showPage('actions')">Action Register</button>
</nav>

<main>
<section id="home" class="page active">
<div class="card">
<h2>Welcome</h2>
<p>Security Management System</p>
<p>Manage incidents, patrols, personnel and operations.</p>
</div>
<div class="card">
<h3>System modules</h3>
<p>Incident Management</p>
<p>Patrol Management</p>
<p>Personnel Management</p>
<p>Operations Management</p>
<p>Vehicle Management</p>
<p>Action Register</p>
</div>
</section>

<section id="incidents" class="page">
<div class="card">
<h2>Incident Management</h2>
<input placeholder="Incident type">
<input placeholder="Location">
<input type="datetime-local">
<textarea placeholder="Incident description"></textarea>
<button class="action">Save Incident</button>
</div>
</section>

<section id="patrols" class="page">
<div class="card">
<h2>Patrol Management</h2>
<input placeholder="Patrol area">
<input placeholder="Patrol commander">
<input type="datetime-local">
<textarea placeholder="Patrol observations"></textarea>
<button class="action">Save Patrol</button>
</div>
</section>

<section id="personnel" class="page">
<div class="card">
<h2>Personnel Management</h2>
<input placeholder="Full name">
<input placeholder="Rank">
<input placeholder="Duty">
<input placeholder="Assignment">
<button class="action">Save Personnel</button>
</div>
</section>

<section id="operations" class="page">
<div class="card">
<h2>Operations Management</h2>
<input placeholder="Operation name">
<input placeholder="Operation area">
<textarea placeholder="Operation details"></textarea>
<button class="action">Save Operation</button>
</div>
</section>

<section id="vehicles" class="page">
<div class="card">
<h2>Vehicle Management</h2>
<input placeholder="Vehicle registration">
<input placeholder="Vehicle type">
<input placeholder="Assigned driver">
<button class="action">Save Vehicle</button>
</div>
</section>

<section id="actions" class="page">
<div class="card">
<h2>Action Register</h2>
<input placeholder="Action description">
<input placeholder="Assigned officer">
<select>
<option>Pending</option>
<option>In progress</option>
<option>Completed</option>
</select>
<button class="action">Save Action</button>
</div>
</section>
</main>

<script>
function showPage(page) {
  document.querySelectorAll('.page').forEach(
    p => p.classList.remove('active')
  );
  document.getElementById(page).classList.add('active');
}
</script>

</body>
</html>
