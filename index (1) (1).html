<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deskload — Student Task Manager</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:opsz,wght@8..60,500;8..60,600;8..60,700&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#EEF0F4;
    --card:#FFFFFF;
    --ink:#1C2130;
    --ink-soft:#565E70;
    --line:#DEE1E9;
    --navy:#2B3A67;
    --navy-deep:#1E2A4C;
    --amber:#DB9A2E;
    --amber-soft:#FCEFD6;
    --green:#1F7A5C;
    --green-soft:#E1F3EB;
    --red:#C4443A;
    --red-soft:#FBE6E4;
    --radius:14px;
    --shadow:0 1px 2px rgba(28,33,48,0.06);
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --paper:#14161C;
      --card:#1C1F28;
      --ink:#EDEFF4;
      --ink-soft:#9BA1B0;
      --line:#2C303C;
      --navy:#7E93D6;
      --navy-deep:#AEBEEF;
      --amber:#E7B15C;
      --amber-soft:#3A2F17;
      --green:#5FBE97;
      --green-soft:#173229;
      --red:#E27A72;
      --red-soft:#3A2020;
      --shadow:0 1px 2px rgba(0,0,0,0.4);
    }
  }
  :root[data-theme="dark"]{
    --paper:#14161C;
    --card:#1C1F28;
    --ink:#EDEFF4;
    --ink-soft:#9BA1B0;
    --line:#2C303C;
    --navy:#7E93D6;
    --navy-deep:#AEBEEF;
    --amber:#E7B15C;
    --amber-soft:#3A2F17;
    --green:#5FBE97;
    --green-soft:#173229;
    --red:#E27A72;
    --red-soft:#3A2020;
    --shadow:0 1px 2px rgba(0,0,0,0.4);
  }

  *{box-sizing:border-box;}
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink);
    font-family:'IBM Plex Sans', system-ui, sans-serif;
    -webkit-font-smoothing:antialiased;
  }
  .wrap{
    max-width:1180px;
    margin:0 auto;
    padding:36px 24px 64px;
  }

  header{
    display:flex;
    justify-content:space-between;
    align-items:flex-start;
    gap:20px;
    margin-bottom:28px;
    flex-wrap:wrap;
  }
  .brand{display:flex; gap:14px; align-items:flex-start;}
  .brand-mark{
    width:42px; height:42px; border-radius:10px;
    background:var(--navy);
    display:flex; align-items:center; justify-content:center;
    color:#fff; font-family:'Source Serif 4', serif; font-weight:600; font-size:19px;
    flex-shrink:0;
  }
  h1{
    font-family:'Source Serif 4', serif;
    font-weight:600;
    font-size:26px;
    margin:0 0 4px;
    letter-spacing:-0.01em;
  }
  .subtitle{color:var(--ink-soft); font-size:14.5px; margin:0; max-width:46ch;}

  .stats{display:flex; gap:10px; flex-wrap:wrap;}
  .stat-pill{
    background:var(--card);
    border:1px solid var(--line);
    border-radius:999px;
    padding:9px 16px;
    font-size:13.5px;
    color:var(--ink-soft);
    white-space:nowrap;
  }
  .stat-pill b{color:var(--ink); font-weight:600;}
  .stat-pill.warn b{color:var(--red);}
  .stat-pill.good b{color:var(--green);}

  .grid{
    display:grid;
    grid-template-columns:1.15fr 0.85fr;
    gap:20px;
    align-items:start;
  }
  @media (max-width:860px){
    .grid{grid-template-columns:1fr;}
  }

  .card{
    background:var(--card);
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:22px 24px;
    box-shadow:var(--shadow);
    margin-bottom:20px;
  }
  .card h2{
    font-family:'Source Serif 4', serif;
    font-size:17.5px;
    font-weight:600;
    margin:0 0 4px;
  }
  .card p.hint{
    color:var(--ink-soft);
    font-size:13.5px;
    margin:0 0 18px;
    line-height:1.5;
  }

  .field-row{display:flex; gap:14px; margin-bottom:14px; flex-wrap:wrap;}
  .field{flex:1; min-width:150px; display:flex; flex-direction:column; gap:6px;}
  .field label{font-size:12.5px; color:var(--ink-soft); font-weight:500;}
  input[type=text], input[type=date], select{
    border:1px solid var(--line);
    background:var(--paper);
    color:var(--ink);
    border-radius:9px;
    padding:10px 12px;
    font-size:14px;
    font-family:inherit;
  }
  input:focus, select:focus, button:focus{
    outline:2px solid var(--navy);
    outline-offset:1px;
  }

  button.primary{
    width:100%;
    background:var(--navy);
    color:#fff;
    border:none;
    border-radius:9px;
    padding:12px 16px;
    font-size:14.5px;
    font-weight:600;
    font-family:inherit;
    cursor:pointer;
    transition:background .15s ease;
  }
  button.primary:hover{background:var(--navy-deep);}

  table{width:100%; border-collapse:collapse; margin-top:6px;}
  th{
    text-align:left;
    font-size:11.5px;
    color:var(--ink-soft);
    font-weight:600;
    padding:0 8px 10px;
    border-bottom:1px solid var(--line);
  }
  td{
    padding:11px 8px;
    border-bottom:1px solid var(--line);
    font-size:14px;
    vertical-align:middle;
  }
  tr:last-child td{border-bottom:none;}
  .task-title{font-weight:500;}
  .task-title.done{color:var(--ink-soft); text-decoration:line-through;}
  .subj-tag{
    display:inline-block;
    background:var(--paper);
    border:1px solid var(--line);
    border-radius:999px;
    padding:3px 10px;
    font-size:12px;
    color:var(--ink-soft);
  }
  .due{font-size:13px; color:var(--ink-soft);}
  .due.overdue{color:var(--red); font-weight:600;}
  .due.today{color:var(--amber); font-weight:600;}
  .row-actions{display:flex; gap:8px; align-items:center; justify-content:flex-end;}
  .chk{
    width:18px; height:18px;
    border-radius:5px;
    border:1.5px solid var(--line);
    cursor:pointer;
    background:var(--card);
    flex-shrink:0;
  }
  .chk.checked{background:var(--green); border-color:var(--green); position:relative;}
  .del{
    background:none; border:none; color:var(--ink-soft);
    cursor:pointer; font-size:15px; line-height:1; padding:4px;
  }
  .del:hover{color:var(--red);}
  .empty-row td{color:var(--ink-soft); text-align:center; padding:22px 8px; font-size:13.5px;}

  .console{
    background:var(--paper);
    border:1px solid var(--line);
    border-radius:10px;
    padding:14px 16px;
    font-family:'IBM Plex Mono', ui-monospace, monospace;
    font-size:12.5px;
    color:var(--ink-soft);
    margin-bottom:16px;
  }

  .overview-empty{
    color:var(--ink-soft);
    font-size:13.5px;
    padding:10px 0 4px;
  }
  .bar-row{display:flex; align-items:center; gap:10px; margin-bottom:10px;}
  .bar-label{width:88px; font-size:12.5px; color:var(--ink-soft); flex-shrink:0;}
  .bar-track{flex:1; height:8px; background:var(--paper); border-radius:99px; overflow:hidden;}
  .bar-fill{height:100%; background:var(--navy); border-radius:99px;}
  .bar-count{font-size:12.5px; color:var(--ink-soft); width:20px; text-align:right;}

  footer{
    margin-top:12px;
    text-align:center;
    font-size:12.5px;
    color:var(--ink-soft);
    line-height:1.6;
  }
  .reset-btn{
    margin-top:14px;
    background:none;
    border:1px solid var(--line);
    color:var(--ink-soft);
    border-radius:8px;
    padding:8px 16px;
    font-size:13px;
    cursor:pointer;
  }
  .reset-btn:hover{border-color:var(--red); color:var(--red);}
</style>
</head>
<body>
<div class="wrap">

  <header>
    <div class="brand">
      <div class="brand-mark">✓</div>
      <div>
        <h1>Deskload</h1>
        <p class="subtitle">Student task tracker &amp; weekly workload planner</p>
      </div>
    </div>
    <div class="stats" id="statPills"></div>
  </header>

  <div class="grid">
    <!-- LEFT COLUMN -->
    <div>
      <div class="card">
        <h2>Add a task</h2>
        <p class="hint">Log an assignment, reading or exam with a due date and subject.</p>

        <div class="field-row">
          <div class="field" style="flex:2;">
            <label for="taskTitle">Task</label>
            <input type="text" id="taskTitle" placeholder="e.g. Finish OOP case study">
          </div>
          <div class="field">
            <label for="taskDue">Due date</label>
            <input type="date" id="taskDue">
          </div>
        </div>
        <div class="field-row">
          <div class="field">
            <label for="taskSubject">Subject</label>
            <select id="taskSubject">
              <option>General</option>
              <option>Software Engineering</option>
              <option>Databases</option>
              <option>Math</option>
              <option>Thesis</option>
              <option>Other</option>
            </select>
          </div>
          <div class="field">
            <label for="taskPriority">Priority</label>
            <select id="taskPriority">
              <option value="Low">Low</option>
              <option value="Medium" selected>Medium</option>
              <option value="High">High</option>
            </select>
          </div>
        </div>
        <button class="primary" onclick="addTask()">Add task</button>
      </div>

      <div class="card">
        <h2>Your tasks</h2>
        <p class="hint">Everything on your plate, soonest deadline first.</p>
        <table>
          <thead>
            <tr>
              <th style="width:26px;"></th>
              <th>Task</th>
              <th>Subject</th>
              <th>Due</th>
              <th>Priority</th>
              <th></th>
            </tr>
          </thead>
          <tbody id="taskBody"></tbody>
        </table>
      </div>
    </div>

    <!-- RIGHT COLUMN -->
    <div>
      <div class="card">
        <h2>Sync status</h2>
        <p class="hint">Where this build stands right now.</p>
        <div class="console" id="syncConsole">&gt; Local store ready. Tasks are saved to this browser only.</div>
        <p class="hint" style="margin-bottom:0;">A future version connects this to the TaskService API — create, complete and list endpoints — instead of the browser store shown here.</p>
      </div>

      <div class="card">
        <h2>Workload by subject</h2>
        <p class="hint">Open tasks grouped by subject.</p>
        <div id="workloadBars"></div>
      </div>
    </div>
  </div>

  <footer>
    Data is stored only in this browser (no server, no account) — this is a Week 1 front-end skeleton.<br>
    The real build will call a TaskService REST API backed by a database, per the class design.
    <div>
      <button class="reset-btn" onclick="resetAll()">Reset all data</button>
    </div>
  </footer>

</div>

<script>
  const STORE_KEY = 'deskload_tasks_v1';

  function loadTasks(){
    try{
      const raw = localStorage.getItem(STORE_KEY);
      return raw ? JSON.parse(raw) : seedTasks();
    }catch(e){
      return seedTasks();
    }
  }
  function seedTasks(){
    const today = new Date();
    const iso = d => d.toISOString().slice(0,10);
    const t1 = new Date(today); t1.setDate(t1.getDate());
    const t2 = new Date(today); t2.setDate(t2.getDate()+2);
    const t3 = new Date(today); t3.setDate(t3.getDate()-1);
    return [
      {id:cryptoId(), title:'Draft class diagram for Task service', subject:'Software Engineering', due:iso(t1), priority:'High', done:false},
      {id:cryptoId(), title:'Read Ch.4 — Normalization', subject:'Databases', due:iso(t2), priority:'Medium', done:false},
      {id:cryptoId(), title:'Submit progress log', subject:'Thesis', due:iso(t3), priority:'High', done:false},
    ];
  }
  function cryptoId(){
    return 'id_' + Math.random().toString(36).slice(2,10);
  }
  function saveTasks(tasks){
    try{ localStorage.setItem(STORE_KEY, JSON.stringify(tasks)); }
    catch(e){ console.error('Storage error', e); }
  }

  let tasks = loadTasks();

  function todayISO(){
    return new Date().toISOString().slice(0,10);
  }

  function addTask(){
    const title = document.getElementById('taskTitle').value.trim();
    const due = document.getElementById('taskDue').value;
    const subject = document.getElementById('taskSubject').value;
    const priority = document.getElementById('taskPriority').value;

    if(!title){
      flashConsole('&gt; Task needs a title before it can be added.');
      return;
    }
    tasks.push({id:cryptoId(), title, subject, due: due || todayISO(), priority, done:false});
    saveTasks(tasks);
    document.getElementById('taskTitle').value = '';
    document.getElementById('taskDue').value = '';
    flashConsole('&gt; Added "'+escapeHtml(title)+'" to '+subject+'.');
    render();
  }

  function toggleDone(id){
    tasks = tasks.map(t => t.id === id ? {...t, done: !t.done} : t);
    saveTasks(tasks);
    render();
  }

  function deleteTask(id){
    tasks = tasks.filter(t => t.id !== id);
    saveTasks(tasks);
    render();
  }

  function resetAll(){
    tasks = seedTasks();
    saveTasks(tasks);
    flashConsole('&gt; All data reset to sample tasks.');
    render();
  }

  function flashConsole(html){
    document.getElementById('syncConsole').innerHTML = html;
  }

  function escapeHtml(s){
    return s.replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
  }

  function dueClass(dateStr, done){
    if(done) return '';
    if(dateStr < todayISO()) return 'overdue';
    if(dateStr === todayISO()) return 'today';
    return '';
  }
  function dueLabel(dateStr, done){
    const cls = dueClass(dateStr, done);
    if(!done && cls === 'overdue') return dateStr + ' · overdue';
    if(!done && cls === 'today') return dateStr + ' · due today';
    return dateStr;
  }

  function render(){
    // stats
    const openTasks = tasks.filter(t => !t.done);
    const overdue = openTasks.filter(t => t.due < todayISO()).length;
    const dueToday = openTasks.filter(t => t.due === todayISO()).length;
    const completed = tasks.filter(t => t.done).length;

    document.getElementById('statPills').innerHTML = `
      <div class="stat-pill">Open tasks <b>${openTasks.length}</b></div>
      <div class="stat-pill ${dueToday>0?'warn':''}">Due today <b>${dueToday}</b></div>
      <div class="stat-pill ${overdue>0?'warn':'good'}">Overdue <b>${overdue}</b></div>
      <div class="stat-pill good">Completed <b>${completed}</b></div>
    `;

    // table
    const body = document.getElementById('taskBody');
    const sorted = [...tasks].sort((a,b) => (a.done - b.done) || (a.due < b.due ? -1 : 1));
    if(sorted.length === 0){
      body.innerHTML = `<tr class="empty-row"><td colspan="6">No tasks yet — add one above to get started.</td></tr>`;
    }else{
      body.innerHTML = sorted.map(t => `
        <tr>
          <td><div class="chk ${t.done?'checked':''}" onclick="toggleDone('${t.id}')"></div></td>
          <td><span class="task-title ${t.done?'done':''}">${escapeHtml(t.title)}</span></td>
          <td><span class="subj-tag">${escapeHtml(t.subject)}</span></td>
          <td><span class="due ${dueClass(t.due,t.done)}">${dueLabel(t.due,t.done)}</span></td>
          <td>${t.priority}</td>
          <td class="row-actions"><button class="del" onclick="deleteTask('${t.id}')" aria-label="Delete task">✕</button></td>
        </tr>
      `).join('');
    }

    // workload bars
    const bySubject = {};
    openTasks.forEach(t => { bySubject[t.subject] = (bySubject[t.subject]||0) + 1; });
    const entries = Object.entries(bySubject).sort((a,b) => b[1]-a[1]);
    const max = entries.length ? entries[0][1] : 1;
    const wl = document.getElementById('workloadBars');
    if(entries.length === 0){
      wl.innerHTML = `<div class="overview-empty">No open tasks — your board is clear.</div>`;
    }else{
      wl.innerHTML = entries.map(([subj,count]) => `
        <div class="bar-row">
          <div class="bar-label">${escapeHtml(subj)}</div>
          <div class="bar-track"><div class="bar-fill" style="width:${(count/max*100).toFixed(0)}%"></div></div>
          <div class="bar-count">${count}</div>
        </div>
      `).join('');
    }
  }

  render();
</script>
</body>
</html>
