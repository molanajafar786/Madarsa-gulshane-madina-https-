<!doctype html>
<html lang="hi">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Madarsa Gulshan-e-Madina Panaravad (v9)</title>
<link rel="manifest" href="data:application/manifest+json,{%22name%22:%22Madarsa%20Portal%22,%22short_name%22:%22Madarsa%22,%22start_url%22:%22.%22,%22display%22:%22standalone%22,%22background_color%22:%22%23075e3d%22,%22theme_color%22:%22%23075e3d%22}">
<style>
body{margin:0;font-family:Arial,sans-serif;background:#f0f4f1;color:#1a2e1f}
header{background:linear-gradient(135deg,#075e3d,#b88620);color:#fff;padding:18px;text-align:center}
.wrap{max-width:1100px;margin:auto;padding:12px}
.card{background:#fff;border-radius:14px;padding:16px;margin:12px 0;box-shadow:0 3px 12px rgba(0,0,0,0.07)}
input,select,button{width:100%;box-sizing:border-box;padding:11px;margin:6px 0;border:1px solid #ccc;border-radius:8px;font-size:15px}
button{background:#075e3d;color:#fff;border:0;font-weight:bold;cursor:pointer}
.gold{background:#b88620}
.danger{background:#b71c1c}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:8px}
.hidden{display:none}
.msg{padding:10px;border-radius:8px;background:#fff3cd;margin:8px 0;font-size:13px}
.studentPhoto{width:80px;height:80px;border-radius:50%;object-fit:cover;background:#eee;border:2px solid #b88620}
.molana-card{background:#e8f5e9;border:1.5px solid #075e3d;border-radius:12px;padding:12px;display:flex;align-items:center;gap:12px;flex-wrap:wrap}
.chip{display:inline-block;padding:3px 8px;border-radius:15px;color:#fff;font-size:12px;text-decoration:none}
.badge{background:#c8e6c9;color:#256029;padding:3px 8px;border-radius:5px;font-weight:bold;font-size:12px}
.tag-p{background:#e8f5e9;color:#1b5e20;padding:2px 6px;border-radius:4px;font-weight:bold}
.tag-a{background:#ffebee;color:#b71c1c;padding:2px 6px;border-radius:4px;font-weight:bold}
</style>
</head>
<body>

<header>
  <h2 style="margin:0">🕌 Madarsa Gulshan-e-Madina Panaravad</h2>
  <small>Official Portal v9</small>
</header>

<div class="wrap">
  <!-- Login Screen -->
  <div id="login" class="card">
    <h3>🔐 Portal Login</h3>
    <div class="grid">
      <select id="role">
        <option value="student">Student</option>
        <option value="admin">Admin</option>
        <option value="teacher">Teacher</option>
      </select>
      <input id="uid" placeholder="User ID / Student ID (e.g. MG001)">
      <input id="pin" type="password" placeholder="PIN Daalein">
    </div>
    <button onclick="loginNow()">Login Karein</button>
    <div id="loginMsg" class="msg">Student: <b>MG001 se MG050</b> | Admin: <b>admin / 7860</b></div>
    <hr>
    <button class="gold" onclick="$('backupFile').click()">♻️ Madarsa Data Restore Karein (JSON)</button>
    <input type="file" id="backupFile" class="hidden" accept=".json" onchange="restoreBackup(event)">
  </div>

  <!-- Dashboard -->
  <div id="app" class="hidden">
    <div class="molana-card">
      <div style="flex:1">
        <b style="color:#075e3d">Molana Jafar Raza</b><br>
        📞 <a class="chip" style="background:#075e3d" href="tel:8140851723">8140851723</a>
        🤝 <a class="chip" style="background:#b88620" href="tel:9898935542">Trustee: 9898935542</a>
      </div>
      <div>
        <span id="welcome" style="font-weight:bold"></span><br>
        <button class="danger" style="width:auto;padding:5px 12px;margin-top:4px" onclick="location.reload()">Logout</button>
      </div>
    </div>

    <!-- Admin View -->
    <div id="adminPanel" class="hidden">
      <!-- Hazri Section -->
      <div class="card">
        <h3>📅 Rozana Hazri (Attendance)</h3>
        <input type="date" id="attDate">
        <div id="attList" style="max-height:220px;overflow-y:auto;border:1px solid #ddd;padding:6px;border-radius:8px"></div>
        <button onclick="saveAttendance()" style="margin-top:8px">Hazri Mehfooz Karein</button>
      </div>

      <!-- Add Student Section -->
      <div class="card">
        <h3>➕ Naya Student Jodein (Auto-Compress Photo)</h3>
        <div class="grid">
          <input id="sname" placeholder="Student Ka Naam">
          <input id="sfather" placeholder="Walid Ka Naam">
          <input id="sclass" placeholder="Darja (Darse Nizami)">
          <input id="smobile" placeholder="Mobile No.">
          <input id="spin" placeholder="PIN (7860)">
          <div>
            <label style="font-size:12px;font-weight:bold">Photo (Camera / Gallery):</label>
            <input type="file" id="sphoto" accept="image/*">
          </div>
        </div>
        <button onclick="addNewStudent()">Student Save Karein</button>
      </div>

      <!-- Backup Tools -->
      <div class="card">
        <h3>💾 Data Backup (Halka Size)</h3>
        <button class="gold" onclick="downloadBackup()">Naya Safe Backup Download Karein</button>
      </div>

      <!-- Student Directory -->
      <div class="card">
        <h3>👥 Registered Students (<span id="count">0</span>)</h3>
        <div id="studentsList"></div>
      </div>
    </div>

    <!-- Student View -->
    <div id="studentPanel" class="hidden">
      <div class="card" style="text-align:center">
        <div id="myPhotoBox"></div>
        <h2 id="myName" style="margin:8px 0"></h2>
        <div id="myData" style="text-align:left;line-height:1.7"></div>
        <hr>
        <h4>Meri Hazri Summary</h4>
        <div id="myAttSummary"></div>
      </div>
    </div>
  </div>
</div>

<script>
const KEY = 'madarsa_live_data_v9';
let D = JSON.parse(localStorage.getItem(KEY) || 'null');

if (!D || !D.students) {
  let defaultStudents = [];
  for (let i = 1; i <= 50; i++) {
    let id = "MG" + String(i).padStart(3, '0');
    defaultStudents.push({
      id: id,
      name: "Student " + id,
      father: "Walid",
      class: "Darse Nizami",
      mobile: "",
      pin: "7860",
      photo: ""
    });
  }
  D = { students: defaultStudents, attendance: {} };
  localStorage.setItem(KEY, JSON.stringify(D));
}
if (!D.attendance) D.attendance = {};

const $ = id => document.getElementById(id);
const clean = x => String(x || '').trim().toLowerCase();

function compressPhoto(file, callback) {
  let r = new FileReader();
  r.onload = e => {
    let img = new Image();
    img.onload = () => {
      let c = document.createElement('canvas');
      let max = 150, w = img.width, h = img.height;
      if (w > h) { if (w > max) { h *= max / w; w = max; } }
      else { if (h > max) { w *= max / h; h = max; } }
      c.width = w; c.height = h;
      c.getContext('2d').drawImage(img, 0, 0, w, h);
      callback(c.toDataURL('image/jpeg', 0.65));
    };
    img.src = e.target.result;
  };
  r.readAsDataURL(file);
}

function getNextId() {
  let nums = D.students.map(s => {
    let m = String(s.id).match(/\d+/);
    return m ? parseInt(m[0], 10) : 0;
  });
  let next = 1;
  while (nums.includes(next)) next++;
  return "MG" + String(next).padStart(3, '0');
}

function addNewStudent() {
  let name = $('sname').value.trim();
  let father = $('sfather').value.trim();
  let sclass = $('sclass').value.trim() || 'Darse Nizami';
  let mobile = $('smobile').value.trim();
  let pin = $('spin').value.trim() || '7860';
  let photoFile = $('sphoto').files[0];

  if (!name) return alert("Student ka naam zaroori hai!");

  let id = getNextId();
  function save(pic) {
    D.students.push({ id, name, father, class: sclass, mobile, pin, photo: pic || '' });
    localStorage.setItem(KEY, JSON.stringify(D));
    alert("Student Mehfooz! ID: " + id);
    $('sname').value = ''; $('sfather').value = '';$('smobile').value = ''; $('spin').value = '';$('sphoto').value = '';
    renderAdmin();
  }

  if (photoFile) compressPhoto(photoFile, save);
  else save('');
}

function loginNow() {
  let role = $('role').value, uid = clean($('uid').value), pin = clean($('pin').value);
  if (role === 'admin' && ((uid === 'admin' && pin === '7860') || (uid === '7860' && pin === 'admin'))) {
    openAdmin(); return;
  }
  let s = D.students.find(x => clean(x.id) === uid && clean(x.pin) === pin);
  if (s) { openStudent(s); return; }
  $('loginMsg').innerHTML = '❌ Galat ID ya PIN! Dubara check karein.';
}

function openAdmin() {
  $('login').classList.add('hidden');
  $('app').classList.remove('hidden');$('adminPanel').classList.remove('hidden');
  $('welcome').innerText = 'Admin Portal';$('attDate').valueAsDate = new Date();
  renderAdmin();
}

function renderAdmin() {
  $('count').innerText = D.students.length;
  $('studentsList').innerHTML = D.students.map(s => `
    <div style="display:flex;align-items:center;gap:10px;border-bottom:1px solid #eee;padding:6px 0">
      ${s.photo ? `<img src="${s.photo}" style="width:36px;height:36px;border-radius:50%;object-fit:cover">` : `<div style="width:36px;height:36px;border-radius:50%;background:#ccc;text-align:center;line-height:36px;font-size:11px">Pic</div>`}
      <div style="flex:1"><b>${s.id}</b> — ${s.name} (PIN: ${s.pin})<br><small>${s.class} | Walid: ${s.father||'N/A'}</small></div>
    </div>
  `).join('');

  let dt = $('attDate').value || new Date().toISOString().slice(0,10);
  let cur = D.attendance[dt] || {};
  $('attList').innerHTML = D.students.map(s => `
    <div style="display:flex;justify-content:space-between;padding:4px 0">
      <span>${s.id} - ${s.name}</span>
      <select id="att_${s.id}" style="width:auto;margin:0;padding:2px 8px">
        <option value="P" ${cur[s.id]!=='A'?'selected':''}>Hazir (P)</option>
        <option value="A" ${cur[s.id]==='A'?'selected':''}>Gair-Hazir (A)</option>
      </select>
    </div>
  `).join('');
}

function saveAttendance() {
  let dt = $('attDate').value;
  if (!dt) return alert("Date chunein!");
  if (!D.attendance[dt]) D.attendance[dt] = {};
  D.students.forEach(s => {
    let el = $('att_' + s.id);
    if (el) D.attendance[dt][s.id] = el.value;
  });
  localStorage.setItem(KEY, JSON.stringify(D));
  alert("Tareekh " + dt + " ki hazri mehfooz ho gayi!");
}

function openStudent(s) {
  $('login').classList.add('hidden');$('app').classList.remove('hidden');
  $('studentPanel').classList.remove('hidden');$('welcome').innerText = s.name;
  $('myName').innerText = s.name;
  $('myPhotoBox').innerHTML = s.photo ? `<img src="${s.photo}" class="studentPhoto">` : `<div class="studentPhoto" style="display:inline-block;line-height:80px">Photo</div>`;
  $('myData').innerHTML = `
    <p><b>Student ID:</b> ${s.id}</p>
    <p><b>Darja:</b> ${s.class}</p>
    <p><b>Walid Ka Naam:</b> ${s.father || 'N/A'}</p>
    <p><b>Mobile:</b> ${s.mobile || 'N/A'}</p>
    <span class="badge">Verified Student</span>
  `;
  let pCount = 0, aCount = 0;
  Object.keys(D.attendance || {}).forEach(d => {
    if (D.attendance[d][s.id] === 'P') pCount++;
    if (D.attendance[d][s.id] === 'A') aCount++;
  });
  $('myAttSummary').innerHTML = `<span class="tag-p">Hazir: ${pCount} din</span> &nbsp; <span class="tag-a">Gair-Hazir: ${aCount} din</span>`;
}

function downloadBackup() {
  let b = new Blob([JSON.stringify(D, null, 2)], { type: 'application/json' });
  let a = document.createElement('a');
  a.href = URL.createObjectURL(b);
  a.download = 'madarsa_v9_backup.json';
  a.click();
}

function restoreBackup(e) {
  let f = e.target.files[0];
  if (!f) return;
  let r = new FileReader();
  r.onload = ev => {
    try {
      let data = JSON.parse(ev.target.result);
      if (data.students) {
        D = data;
        localStorage.setItem(KEY, JSON.stringify(D));
        alert('Data kamiyabi se restore ho gaya!');
        location.reload();
      }
    } catch(err) { alert('File load nahi hui: ' + err.message); }
  };
  r.readAsText(f);
}
</script>
</body>
</html>
