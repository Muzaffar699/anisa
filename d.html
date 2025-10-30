<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Календарь бронирования квартир</title>
  <style>
    :root {
      --primary-color: #1e40af;
      --secondary-color: #3b82f6;
      --light-bg: #eff6ff;
      --cell-bg: #e0f2fe;
      --success-color: #4caf50;
      --warning-color: #ffa726;
      --danger-color: #f44336;
    }
    
    * {
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #dbeafe, #eff6ff);
      margin: 0;
      padding: 10px;
      color: #333;
      line-height: 1.5;
    }
    
    h2 {
      text-align: center;
      margin-bottom: 15px;
      font-size: 24px;
      color: var(--primary-color);
    }
    
    .controls {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 15px;
      justify-content: center;
      align-items: center;
    }
    
    .controls label {
      display: flex;
      flex-direction: column;
      font-size: 14px;
      font-weight: 500;
    }
    
    select, button, input {
      font-size: 16px;
      padding: 10px 12px;
      border: none;
      border-radius: 6px;
      background: var(--cell-bg);
      color: var(--primary-color);
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      min-height: 44px;
    }
    
    #newRoomName {
      flex-grow: 1;
      min-width: 150px;
    }
    
    button {
      cursor: pointer;
      font-weight: 500;
      transition: all 0.2s;
      white-space: nowrap;
    }
    
    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 4px 8px rgba(0,0,0,0.15);
    }
    
    .export-btn {
      background: var(--secondary-color);
      color: #fff;
    }
    
    .stats {
      display: flex;
      gap: 15px;
      margin: 15px 0;
      flex-wrap: wrap;
      justify-content: center;
    }
    
    .stat-card {
      background: white;
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      min-width: 120px;
      text-align: center;
      flex: 1;
    }
    
    .stat-card h3 {
      margin: 0 0 8px 0;
      font-size: 14px;
      color: #666;
    }
    
    .stat-card div {
      font-size: 24px;
      font-weight: bold;
      color: var(--primary-color);
    }
    
    .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 15px;
      justify-content: center;
    }
    
    .filters input, .filters select {
      flex: 1;
      min-width: 150px;
    }
    
    .calendar {
      overflow-x: auto;
      border-radius: 10px;
      background: #ffffff;
      box-shadow: 0 4px 10px rgba(0,0,0,0.08);
      margin-bottom: 20px;
      -webkit-overflow-scrolling: touch;
    }
    
    table {
      border-collapse: collapse;
      width: 100%;
      min-width: 800px;
    }
    
    th, td {
      border: 1px solid #e5e7eb;
      text-align: center;
      padding: 5px;
      font-size: 13px;
      height: 32px;
      position: relative;
    }
    
    th {
      background: #f1f5f9;
      position: sticky;
      top: 0;
      z-index: 2;
      font-weight: 600;
      color: #111827;
    }
    
    .room-name {
      background: #f3f4f6;
      font-weight: bold;
      position: sticky;
      left: 0;
      z-index: 1;
      cursor: pointer;
      transition: background 0.2s;
      min-width: 120px;
    }
    
    .room-name:hover {
      background: #dbeafe;
    }
    
    .cell {
      cursor: pointer;
      transition: background 0.2s;
      min-width: 35px;
    }
    
    .cell:hover {
      background: #e0f2fe;
    }
    
    .occupied {
      color: #fff;
      font-weight: bold;
      border-radius: 4px;
    }
    
    .occupied.confirmed {
      background: var(--success-color);
    }
    
    .occupied.pending {
      background: var(--warning-color);
    }
    
    .occupied.cancelled {
      background: var(--danger-color);
    }
    
    .occupied.deposit {
      background: #2196f3;
    }
    
    .occupied.maintenance {
      background: #9e9e9e;
    }
    
    .occupied span {
      display: block;
      font-size: 11px;
      line-height: 1.2;
    }
    
    .room-color-0 { color: #dc2626; }
    .room-color-1 { color: #16a34a; }
    .room-color-2 { color: #2563eb; }
    .room-color-3 { color: #d97706; }
    .room-color-4 { color: #7c3aed; }
    .room-color-5 { color: #059669; }
    .room-color-6 { color: #be123c; }

    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.5);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 10;
      padding: 15px;
    }
    
    .modal-content {
      background: #ffffff;
      padding: 20px;
      width: 100%;
      max-width: 450px;
      border-radius: 10px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      max-height: 90vh;
      overflow-y: auto;
    }
    
    .modal-content input, .modal-content select {
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: 1px solid #d1d5db;
      border-radius: 6px;
      font-size: 16px;
    }
    
    .modal-content button {
      width: 48%;
      padding: 12px;
      border: none;
      color: #fff;
      margin-top: 10px;
      cursor: pointer;
      border-radius: 6px;
      font-weight: bold;
    }
    
    .modal-content .save {
      background: var(--success-color);
    }
    
    .modal-content .delete {
      background: var(--danger-color);
    }
    
    .modal-buttons {
      display: flex;
      justify-content: space-between;
      gap: 10px;
    }
    
    .repeat-options {
      display: none;
      margin-top: 10px;
      padding: 10px;
      background: #f8fafc;
      border-radius: 6px;
    }
    
    .notification {
      position: fixed;
      top: 20px;
      right: 20px;
      background: #4caf50;
      color: white;
      padding: 15px;
      border-radius: 5px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.3);
      z-index: 1000;
      max-width: 300px;
    }
    
    .backup-controls {
      text-align: center;
      margin: 15px 0;
    }
    
    .backup-controls button {
      margin: 0 5px;
    }
    
    /* Мобильная адаптация */
    @media (max-width: 768px) {
      body {
        padding: 5px;
      }
      
      h2 {
        font-size: 20px;
        margin-bottom: 10px;
      }
      
      .controls, .filters {
        flex-direction: column;
        align-items: stretch;
      }
      
      .controls label, .filters label {
        width: 100%;
      }
      
      select, button, input {
        width: 100%;
        margin: 3px 0;
      }
      
      .stats {
        flex-direction: column;
      }
      
      .stat-card {
        width: 100%;
        max-width: 100%;
      }
      
      .modal-content {
        padding: 15px;
        margin: 10px;
      }
      
      .modal-buttons {
        flex-direction: column;
      }
      
      .modal-content button {
        width: 100%;
      }
      
      th, td {
        padding: 3px;
        font-size: 12px;
      }
      
      .occupied span {
        font-size: 9px;
      }
    }
    
    @media (max-width: 480px) {
      th, td {
        padding: 2px;
        font-size: 11px;
        height: 28px;
      }
      
      .room-name {
        min-width: 100px;
      }
      
      .cell {
        min-width: 30px;
      }
    }
  </style>
</head>
<body>

<h2>Календарь бронирования</h2>

<div class="controls">
  <label>Год:
    <select id="yearSelect"></select>
  </label>
  <label>Месяц:
    <select id="monthSelect">
      <option value="0">Январь</option><option value="1">Февраль</option>
      <option value="2">Март</option><option value="3">Апрель</option>
      <option value="4">Май</option><option value="5">Июнь</option>
      <option value="6">Июль</option><option value="7">Август</option>
      <option value="8">Сентябрь</option><option value="9">Октябрь</option>
      <option value="10">Ноябрь</option><option value="11">Декабрь</option>
    </select>
  </label>
  <input id="newRoomName" placeholder="Название квартиры" />
  <button onclick="addRoom()">➕ Добавить объект</button>
  <button class="export-btn" onclick="exportToCSV()">📥 Экспорт в CSV</button>
</div>

<div class="filters">
  <input id="searchRoom" placeholder="🔍 Поиск квартиры" oninput="filterRooms()">
  <select id="statusFilter" onchange="filterRooms()">
    <option value="all">Все статусы</option>
    <option value="free">Свободные</option>
    <option value="booked">Забронированные</option>
  </select>
  <select id="categoryFilter" onchange="filterRooms()">
    <option value="all">Все категории</option>
    <option value="standard">Стандарт</option>
    <option value="luxury">Люкс</option>
    <option value="family">Семейный</option>
  </select>
</div>

<div class="stats">
  <div class="stat-card">
    <h3>Загрузка</h3>
    <div id="occupancyRate">0%</div>
  </div>
  <div class="stat-card">
    <h3>Ожидаемый доход</h3>
    <div id="expectedIncome">0 ₽</div>
  </div>
  <div class="stat-card">
    <h3>Броней</h3>
    <div id="totalBookings">0</div>
  </div>
</div>

<div class="backup-controls">
  <button onclick="createBackup()">💾 Создать резервную копию</button>
  <button onclick="restoreBackup()">🔄 Восстановить из копии</button>
  <button onclick="exportToGoogleCalendar()">📅 Экспорт в календарь</button>
</div>

<div class="calendar">
  <table id="calendarTable">
    <thead><tr><th class="room-name">Квартира</th></tr></thead>
    <tbody></tbody>
  </table>
</div>

<!-- Модалка -->
<div class="modal" id="bookingModal">
  <div class="modal-content">
    <input id="guestName" placeholder="Имя арендатора">
    <input id="guestPhone" placeholder="Телефон">
    <input id="priceTotal" type="number" placeholder="Сумма всего">
    <input id="pricePaid" type="number" placeholder="Оплачено">

    <div id="remainingAmount" style="margin-top:5px;font-weight:bold;color:#1e40af;">
      Осталось: 0
    </div>

    <select id="bookingStatus">
      <option value="confirmed">Подтверждено</option>
      <option value="pending">Ожидание</option>
      <option value="deposit">Депозит</option>
      <option value="cancelled">Отменено</option>
      <option value="maintenance">Техобслуживание</option>
    </select>

    <input id="dateFrom" type="date">
    <input id="dateTo" type="date">
    
    <label>
      <input type="checkbox" id="repeatBooking" onchange="toggleRepeatOptions()"> Повторять бронирование
    </label>
    
    <div class="repeat-options" id="repeatOptions">
      <select id="repeatType">
        <option value="weekly">Еженедельно</option>
        <option value="monthly">Ежемесячно</option>
        <option value="yearly">Ежегодно</option>
      </select>
      <select id="repeatCount">
        <option value="1">1 раз</option>
        <option value="2">2 раза</option>
        <option value="4">4 раза</option>
        <option value="12">12 раз</option>
      </select>
    </div>
    
    <div class="modal-buttons">
      <button class="save" onclick="saveBooking()">💾 Сохранить</button>
      <button class="delete" onclick="deleteBooking()">🗑 Удалить</button>
    </div>
  </div>
</div>

<script>
// Инициализация данных
let rooms = JSON.parse(localStorage.getItem('rooms') || '[]');
if (rooms.length === 0) {
  rooms = Array.from({ length: 15 }, (_, i) => ({
    name: `🌇 Апартаменты №${101 + i}`,
    category: i < 10 ? 'standard' : (i < 13 ? 'luxury' : 'family'),
    price: i < 10 ? 2500 : (i < 13 ? 5000 : 3500),
    capacity: i < 10 ? 2 : (i < 13 ? 4 : 6),
    amenities: ['wifi', 'tv']
  }));
}

const monthSel = document.getElementById('monthSelect');
const yearSel = document.getElementById('yearSelect');
const table = document.getElementById('calendarTable');
const modal = document.getElementById('bookingModal');

let bookings = JSON.parse(localStorage.getItem('bookings') || '[]');
let activeCell = null;
let activeMonth = new Date().getMonth();
let activeYear = new Date().getFullYear();

// Инициализация приложения
function init() {
  populateYears();
  drawCalendar();
  calculateStats();
  checkUpcomingBookings();
  
  // Запрос разрешения на уведомления
  if ('Notification' in window && Notification.permission === 'default') {
    Notification.requestPermission();
  }
}

function populateYears() {
  const y = new Date().getFullYear();
  yearSel.innerHTML = '';
  for (let i = y - 5; i <= y + 5; i++) {
    const opt = document.createElement('option');
    opt.value = i;
    opt.textContent = i;
    yearSel.appendChild(opt);
  }
  yearSel.value = activeYear;
  monthSel.value = activeMonth;
}

function drawCalendar(m = activeMonth, y = activeYear) {
  activeMonth = +m;
  activeYear = +y;
  const days = new Date(y, activeMonth + 1, 0).getDate();
  const head = table.tHead.rows[0];
  head.innerHTML = '<th class="room-name">Квартира</th>';
  for (let d = 1; d <= days; d++) {
    const th = document.createElement('th');
    th.textContent = d.toString().padStart(2, '0');
    head.append(th);
  }

  const body = table.tBodies[0];
  body.innerHTML = '';
  rooms.forEach((r, i) => {
    const tr = document.createElement('tr');
    const td = document.createElement('td');
    td.textContent = typeof r === 'object' ? r.name : r;
    td.className = `room-name room-color-${i % 7}`;
    td.onclick = () => renameRoom(i);
    tr.append(td);
    for (let d = 1; d <= days; d++) {
      const c = document.createElement('td');
      c.className = 'cell';
      c.dataset.room = i;
      c.dataset.day = d;
      c.onclick = () => openModal(c);
      tr.append(c);
    }
    body.append(tr);
  });

  paintBookings();
  calculateStats();
  initDragAndDrop();
}

function addRoom() {
  const name = document.getElementById('newRoomName').value.trim();
  if (!name) return alert('Введите имя квартиры');
  
  rooms.push({
    name: name,
    category: 'standard',
    price: 2500,
    capacity: 2,
    amenities: ['wifi', 'tv']
  });
  
  localStorage.setItem('rooms', JSON.stringify(rooms));
  document.getElementById('newRoomName').value = '';
  drawCalendar();
}

function renameRoom(index) {
  const newName = prompt('Введите новое имя для квартиры:', 
    typeof rooms[index] === 'object' ? rooms[index].name : rooms[index]);
  if (newName && newName.trim()) {
    if (typeof rooms[index] === 'object') {
      rooms[index].name = newName.trim();
    } else {
      rooms[index] = {
        name: newName.trim(),
        category: 'standard',
        price: 2500,
        capacity: 2,
        amenities: ['wifi', 'tv']
      };
    }
    localStorage.setItem('rooms', JSON.stringify(rooms));
    drawCalendar();
  }
}

function paintBookings() {
  document.querySelectorAll('td.cell').forEach(c => { 
    c.className = 'cell'; 
    c.textContent = ''; 
    c.innerHTML = '';
    c.setAttribute('draggable', 'false');
  });
  
  bookings
    .filter(b => b.month == activeMonth && b.year == activeYear)
    .forEach(b => {
      b.days.forEach(d => {
        const row = table.tBodies[0].rows[b.room];
        if (!row) return;
        const cell = row.querySelector(`td[data-day="${d}"]`);
        if (!cell) return;
        cell.classList.add('occupied', b.status || 'confirmed');
        cell.innerHTML = `<span>${b.name}</span><span>${b.phone}</span>`;
        cell.setAttribute('draggable', 'true');
      });
    });
}

function openModal(cell) {
  activeCell = cell;
  const r = +cell.dataset.room, d = +cell.dataset.day;
  const exist = bookings.find(b => b.room === r && b.month == activeMonth && b.year == activeYear && b.days.includes(d));
  
  document.getElementById('guestName').value = exist?.name || '';
  document.getElementById('guestPhone').value = exist?.phone || '';
  document.getElementById('priceTotal').value = exist?.total || '';
  document.getElementById('pricePaid').value = exist?.paid || '';
  document.getElementById('bookingStatus').value = exist?.status || 'confirmed';
  document.getElementById('dateFrom').value = exist?.from || '';
  document.getElementById('dateTo').value = exist?.to || '';
  
  // Сброс повторяющихся опций
  document.getElementById('repeatBooking').checked = false;
  document.getElementById('repeatOptions').style.display = 'none';
  
  updateRemaining();
  modal.style.display = 'flex';
}

function closeModal() { 
  modal.style.display = 'none'; 
}

function saveBooking() {
  const room = +activeCell.dataset.room;
  const name = document.getElementById('guestName').value.trim();
  const phone = document.getElementById('guestPhone').value.trim();
  const total = +document.getElementById('priceTotal').value;
  const paid = +document.getElementById('pricePaid').value;
  const status = document.getElementById('bookingStatus').value;
  const from = document.getElementById('dateFrom').value;
  const to = document.getElementById('dateTo').value;
  const repeat = document.getElementById('repeatBooking').checked;
  const repeatType = document.getElementById('repeatType').value;
  const repeatCount = +document.getElementById('repeatCount').value;
  
  if (!name || !phone || !from || !to || !total) {
    alert('Заполните все обязательные поля');
    return;
  }
  
  const d1 = new Date(from), d2 = new Date(to);
  if (d1 > d2) {
    alert('Дата начала не может быть позже даты окончания');
    return;
  }
  
  const days = [];
  for (let d = d1.getDate(); d <= d2.getDate(); d++) days.push(d);
  
  const baseBooking = { 
    room, 
    year: activeYear, 
    month: activeMonth, 
    name, 
    phone, 
    total, 
    paid, 
    status,
    from, 
    to, 
    days 
  };
  
  if (repeat) {
    saveRecurringBooking(baseBooking, repeatType, repeatCount);
  } else {
    // Удаляем существующие бронирования для этих дней
    bookings = bookings.filter(b => !(b.room === room && b.month == activeMonth && b.year == activeYear && b.days.some(x => days.includes(x))));
    bookings.push(baseBooking);
  }
  
  localStorage.setItem('bookings', JSON.stringify(bookings));
  createBackup(); // Авто-бэкап
  closeModal();
  paintBookings();
  calculateStats();
}

function saveRecurringBooking(baseBooking, repeatType, repeatCount) {
  const bookingsToSave = [baseBooking];
  
  for (let i = 1; i <= repeatCount; i++) {
    const newBooking = {...baseBooking};
    const fromDate = new Date(baseBooking.from);
    const toDate = new Date(baseBooking.to);
    
    if (repeatType === 'weekly') {
      fromDate.setDate(fromDate.getDate() + (7 * i));
      toDate.setDate(toDate.getDate() + (7 * i));
    } else if (repeatType === 'monthly') {
      fromDate.setMonth(fromDate.getMonth() + i);
      toDate.setMonth(toDate.getMonth() + i);
    } else if (repeatType === 'yearly') {
      fromDate.setFullYear(fromDate.getFullYear() + i);
      toDate.setFullYear(toDate.getFullYear() + i);
    }
    
    newBooking.from = fromDate.toISOString().split('T')[0];
    newBooking.to = toDate.toISOString().split('T')[0];
    newBooking.year = fromDate.getFullYear();
    newBooking.month = fromDate.getMonth();
    
    // Пересчитать дни для нового месяца
    const days = [];
    for (let d = fromDate.getDate(); d <= toDate.getDate(); d++) days.push(d);
    newBooking.days = days;
    
    // Удалить существующие брони для этих дней
    bookings = bookings.filter(b => !(
      b.room === newBooking.room && 
      b.month == newBooking.month && 
      b.year == newBooking.year && 
      b.days.some(x => days.includes(x))
    ));
    
    bookingsToSave.push(newBooking);
  }
  
  bookingsToSave.forEach(booking => {
    bookings.push(booking);
  });
}

function deleteBooking() {
  if (!activeCell) return;
  const room = +activeCell.dataset.room;
  const day = +activeCell.dataset.day;
  
  bookings = bookings.filter(b => !(b.room === room && b.month == activeMonth && b.year == activeYear && b.days.includes(day)));
  localStorage.setItem('bookings', JSON.stringify(bookings));
  createBackup(); // Авто-бэкап
  closeModal();
  paintBookings();
  calculateStats();
}

// Фильтрация и поиск
function filterRooms() {
  const search = document.getElementById('searchRoom').value.toLowerCase();
  const status = document.getElementById('statusFilter').value;
  const category = document.getElementById('categoryFilter').value;
  
  document.querySelectorAll('tbody tr').forEach((row, i) => {
    const room = rooms[i];
    const roomName = (typeof room === 'object' ? room.name : room).toLowerCase();
    const roomCategory = typeof room === 'object' ? room.category : 'standard';
    const hasBooking = row.querySelector('.occupied');
    
    let show = true;
    if (search && !roomName.includes(search)) show = false;
    if (status === 'free' && hasBooking) show = false;
    if (status === 'booked' && !hasBooking) show = false;
    if (category !== 'all' && roomCategory !== category) show = false;
    
    row.style.display = show ? '' : 'none';
  });
}

// Статистика
function calculateStats() {
  const totalDays = rooms.length * new Date(activeYear, activeMonth + 1, 0).getDate();
  let bookedDays = 0;
  let expectedIncome = 0;
  let totalBookings = new Set();
  
  bookings
    .filter(b => b.month == activeMonth && b.year == activeYear)
    .forEach(b => {
      bookedDays += b.days.length;
      expectedIncome += b.total;
      totalBookings.add(`${b.room}-${b.name}-${b.from}`);
    });
  
  const occupancyRate = totalDays > 0 ? ((bookedDays / totalDays) * 100).toFixed(1) : 0;
  document.getElementById('occupancyRate').textContent = `${occupancyRate}%`;
  document.getElementById('expectedIncome').textContent = `${expectedIncome} ₽`;
  document.getElementById('totalBookings').textContent = totalBookings.size;
}

// Уведомления
function checkUpcomingBookings() {
  const today = new Date();
  const nextWeek = new Date(today);
  nextWeek.setDate(nextWeek.getDate() + 7);
  
  const upcoming = bookings.filter(b => {
    const bookingDate = new Date(b.from);
    return bookingDate >= today && bookingDate <= nextWeek;
  });
  
  if (upcoming.length > 0) {
    showNotification(`На следующей неделе ${upcoming.length} бронирований`);
  }
}

function showNotification(message) {
  // Создаем уведомление в интерфейсе
  const notification = document.createElement('div');
  notification.className = 'notification';
  notification.textContent = message;
  document.body.appendChild(notification);
  
  setTimeout(() => {
    notification.remove();
  }, 5000);
  
  // Показываем браузерное уведомление, если разрешено
  if ('Notification' in window && Notification.permission === 'granted') {
    new Notification('Календарь бронирования', {
      body: message,
      icon: 'data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="%234caf50"><path d="M19 3h-1V1h-2v2H8V1H6v2H5c-1.11 0-1.99.9-1.99 2L3 19a2 2 0 0 0 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 16H5V8h14v11zM7 10h5v5H7z"/></svg>'
    });
  }
}

// Drag & Drop
function initDragAndDrop() {
  document.querySelectorAll('.cell').forEach(cell => {
    cell.addEventListener('dragstart', (e) => {
      if (cell.classList.contains('occupied')) {
        e.dataTransfer.setData('text/plain', JSON.stringify({
          room: cell.dataset.room,
          day: cell.dataset.day
        }));
      }
    });
    
    cell.addEventListener('dragover', (e) => {
      e.preventDefault();
    });
    
    cell.addEventListener('drop', (e) => {
      e.preventDefault();
      const data = JSON.parse(e.dataTransfer.getData('text/plain'));
      if (data) {
        moveBooking(data.room, data.day, cell.dataset.room, cell.dataset.day);
      }
    });
  });
}

function moveBooking(fromRoom, fromDay, toRoom, toDay) {
  fromRoom = +fromRoom;
  fromDay = +fromDay;
  toRoom = +toRoom;
  toDay = +toDay;
  
  // Найти бронирование
  const booking = bookings.find(b => 
    b.room === fromRoom && b.month == activeMonth && 
    b.year == activeYear && b.days.includes(fromDay)
  );
  
  if (booking) {
    // Вычислить смещение дней
    const dayDiff = toDay - fromDay;
    const roomDiff = toRoom - fromRoom;
    
    // Обновить бронирование
    booking.days = booking.days.map(d => d + dayDiff);
    booking.room = toRoom;
    
    // Обновить даты
    const fromDate = new Date(booking.from);
    const toDate = new Date(booking.to);
    fromDate.setDate(fromDate.getDate() + dayDiff);
    toDate.setDate(toDate.getDate() + dayDiff);
    booking.from = fromDate.toISOString().split('T')[0];
    booking.to = toDate.toISOString().split('T')[0];
    
    localStorage.setItem('bookings', JSON.stringify(bookings));
    paintBookings();
    showNotification('Бронирование перемещено');
  }
}

// Резервное копирование
function createBackup() {
  const data = {
    rooms: rooms,
    bookings: bookings,
    timestamp: new Date().toISOString()
  };
  
  // Сохранение в localStorage как резервная копия
  const backupKey = 'backup_' + new Date().toISOString().replace(/[:.]/g, '-');
  localStorage.setItem(backupKey, JSON.stringify(data));
  
  // Ограничиваем количество резервных копий (последние 10)
  const backups = Object.keys(localStorage)
    .filter(key => key.startsWith('backup_'))
    .sort()
    .reverse();
    
  if (backups.length > 10) {
    for (let i = 10; i < backups.length; i++) {
      localStorage.removeItem(backups[i]);
    }
  }
  
  showNotification('Резервная копия создана');
}

function restoreBackup() {
  const backups = Object.keys(localStorage)
    .filter(key => key.startsWith('backup_'))
    .sort()
    .reverse();
    
  if (backups.length === 0) {
    alert('Резервные копии не найдены');
    return;
  }
  
  const backupList = backups.map((key, i) => 
    `${i+1}. ${new Date(key.replace('backup_', '')).toLocaleString()}`
  ).join('\n');
  
  const choice = prompt(`Выберите резервную копию для восстановления:\n\n${backupList}\n\nВведите номер:`);
  const index = parseInt(choice) - 1;
  
  if (index >= 0 && index < backups.length) {
    const backup = JSON.parse(localStorage.getItem(backups[index]));
    rooms = backup.rooms;
    bookings = backup.bookings;
    localStorage.setItem('rooms', JSON.stringify(rooms));
    localStorage.setItem('bookings', JSON.stringify(bookings));
    drawCalendar();
    showNotification('Данные восстановлены из резервной копии');
  }
}

// Экспорт
function exportToCSV() {
  let csv = 'Квартира,День,Месяц,Год,Имя,Телефон,Статус,Оплачено,Всего,Дата заезда,Дата выезда\n';
  bookings.forEach(b => {
    b.days.forEach(d => {
      const roomName = typeof rooms[b.room] === 'object' ? rooms[b.room].name : rooms[b.room];
      csv += `${roomName},${d},${+b.month + 1},${b.year},${b.name},${b.phone},${b.status},${b.paid},${b.total},${b.from},${b.to}\n`;
    });
  });
  
  downloadFile(csv, `брони_${activeYear}_${activeMonth+1}.csv`, 'text/csv;charset=utf-8;');
}

function exportToGoogleCalendar() {
  const events = bookings.map(b => {
    const start = new Date(b.year, b.month, b.days[0]);
    const end = new Date(b.year, b.month, b.days[b.days.length - 1]);
    end.setDate(end.getDate() + 1);
    
    const roomName = typeof rooms[b.room] === 'object' ? rooms[b.room].name : rooms[b.room];
    
    return {
      title: `Бронь: ${roomName} - ${b.name}`,
      start: start.toISOString().replace(/[-:]/g, '').split('.')[0] + 'Z',
      end: end.toISOString().replace(/[-:]/g, '').split('.')[0] + 'Z',
      description: `Телефон: ${b.phone}\nСумма: ${b.total}₽\nОплачено: ${b.paid}₽\nСтатус: ${b.status}`
    };
  });
  
  const icsContent = generateICS(events);
  downloadFile(icsContent, 'bookings.ics', 'text/calendar');
}

function generateICS(events) {
  let ics = 'BEGIN:VCALENDAR\nVERSION:2.0\nPRODID:-//Booking Calendar//RU\n';
  
  events.forEach(event => {
    ics += 'BEGIN:VEVENT\n';
    ics += `DTSTART:${event.start}\n`;
    ics += `DTEND:${event.end}\n`;
    ics += `SUMMARY:${event.title}\n`;
    ics += `DESCRIPTION:${event.description.replace(/\n/g, '\\n')}\n`;
    ics += `UID:${Math.random().toString(36).substr(2, 9)}@booking\n`;
    ics += 'END:VEVENT\n';
  });
  
  ics += 'END:VCALENDAR';
  return ics;
}

function downloadFile(content, fileName, mimeType) {
  const blob = new Blob([content], { type: mimeType });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = fileName;
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  URL.revokeObjectURL(url);
}

// Вспомогательные функции
function toggleRepeatOptions() {
  const repeatOptions = document.getElementById('repeatOptions');
  repeatOptions.style.display = document.getElementById('repeatBooking').checked ? 'block' : 'none';
}

// Обновление остатка суммы
const totalInput = document.getElementById('priceTotal');
const paidInput = document.getElementById('pricePaid');
const remainingDiv = document.getElementById('remainingAmount');

function updateRemaining() {
  const total = Number(totalInput.value) || 0;
  const paid = Number(paidInput.value) || 0;
  const remaining = total - paid;
  remainingDiv.textContent = 'Осталось: ' + remaining;
  
  if (remaining > 0) {
    remainingDiv.style.color = '#ef4444';
  } else if (remaining === 0) {
    remainingDiv.style.color = '#10b981';
  } else {
    remainingDiv.style.color = '#f59e0b';
  }
}

totalInput.addEventListener('input', updateRemaining);
paidInput.addEventListener('input', updateRemaining);

// Обработчики событий
yearSel.onchange = () => drawCalendar(monthSel.value, yearSel.value);
monthSel.onchange = () => drawCalendar(monthSel.value, yearSel.value);
modal.onclick = e => { if (e.target === modal) closeModal(); };

// Инициализация при загрузке
document.addEventListener('DOMContentLoaded', init);
</script>

</body>
</html>
