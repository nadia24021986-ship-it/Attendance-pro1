<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portal Kehadiran</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.2.0/umd/react.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.2.0/umd/react-dom.production.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-standalone/7.23.5/babel.min.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = { theme: { extend: {} } }
  </script>
  <style>
    .custom-scrollbar::-webkit-scrollbar { width: 4px; }
    .custom-scrollbar::-webkit-scrollbar-track { background: transparent; }
    .custom-scrollbar::-webkit-scrollbar-thumb { background-color: #cbd5e1; border-radius: 20px; }
  </style>
</head>
<body>
<div id="root"></div>

<script type="text/babel">
const { useState, useEffect, useRef } = React;

// ===================== ICONS =====================
const Icon = ({ d, size = 20, className = "" }) => (
  <svg width={size} height={size} viewBox="0 0 24 24" fill="none"
    stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"
    className={className}>
    <path d={d} />
  </svg>
);
const ClockIcon = (p) => <Icon size={p.size} className={p.className} d="M12 2a10 10 0 1 0 0 20A10 10 0 0 0 12 2zm0 4v6l4 2" />;
const LogOutIcon = (p) => <Icon size={p.size} className={p.className} d="M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4M16 17l5-5-5-5M21 12H9" />;
const FileTextIcon = (p) => <Icon size={p.size} className={p.className} d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8zM14 2v6h6M16 13H8M16 17H8M10 9H8" />;
const UsersIcon = (p) => <Icon size={p.size} className={p.className} d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2M9 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8zM23 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75" />;
const PrinterIcon = (p) => <Icon size={p.size} className={p.className} d="M6 9V2h12v7M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2M6 14h12v8H6z" />;
const CheckIcon = (p) => <Icon size={p.size} className={p.className} d="M22 11.08V12a10 10 0 1 1-5.93-9.14M22 4 12 14.01l-3-3" />;
const XIcon = (p) => <Icon size={p.size} className={p.className} d="M12 2a10 10 0 1 0 0 20A10 10 0 0 0 12 2zM15 9l-6 6M9 9l6 6" />;
const ChevronRightIcon = (p) => <Icon size={p.size} className={p.className} d="M9 18l6-6-6-6" />;
const UserPlusIcon = (p) => <Icon size={p.size} className={p.className} d="M16 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2M8.5 11a4 4 0 1 0 0-8 4 4 0 0 0 0 8zM20 8v6M23 11h-6" />;
const SearchIcon = (p) => <Icon size={p.size} className={p.className} d="M21 21l-4.35-4.35M17 11A6 6 0 1 1 5 11a6 6 0 0 1 12 0z" />;
const BriefcaseIcon = (p) => <Icon size={p.size} className={p.className} d="M20 7H4a2 2 0 0 0-2 2v10a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V9a2 2 0 0 0-2-2zM16 7V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v2" />;
const MapPinIcon = (p) => <Icon size={p.size} className={p.className} d="M21 10c0 7-9 13-9 13S3 17 3 10a9 9 0 0 1 18 0zM12 13a3 3 0 1 0 0-6 3 3 0 0 0 0 6z" />;
const ArrowLeftIcon = (p) => <Icon size={p.size} className={p.className} d="M19 12H5M12 19l-7-7 7-7" />;
const CameraIcon = (p) => <Icon size={p.size} className={p.className} d="M23 19a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h4l2-3h6l2 3h4a2 2 0 0 1 2 2zM12 17a4 4 0 1 0 0-8 4 4 0 0 0 0 8z" />;

// ===================== DATA =====================
const ADMIN_ID = 'admin456231';
const initialEmployees = [
  { id: 'KRY-001', name: 'Budi Santoso', position: 'Staff IT', location: 'Kantor Pusat' },
  { id: 'KRY-002', name: 'Siti Aminah', position: 'Admin Gudang', location: 'Gudang Sektor 4' },
  { id: 'KRY-003', name: 'Rudi Hartono', position: 'Security', location: 'Kantor Pusat' },
];
const initialRecords = [
  { id: 1, employeeId: 'KRY-001', name: 'Budi Santoso', location: 'Kantor Pusat', type: 'Check In', time: new Date().toISOString(), photo: 'https://placehold.co/150x150/e0e7ff/4f46e5?text=BS' },
  { id: 2, employeeId: 'KRY-002', name: 'Siti Aminah', location: 'Gudang Sektor 4', type: 'Check In', time: new Date(Date.now() - 3600000).toISOString(), photo: 'https://placehold.co/150x150/fce7f3/be185d?text=SA' },
];

// ===================== APP =====================
function App() {
  const [currentUser, setCurrentUser] = useState(null);
  const [employees, setEmployees] = useState(initialEmployees);
  const [records, setRecords] = useState(initialRecords);
  if (!currentUser) return <LoginScreen onLogin={setCurrentUser} employees={employees} />;
  if (currentUser === 'admin') return <AdminDashboard onLogout={() => setCurrentUser(null)} employees={employees} setEmployees={setEmployees} records={records} />;
  return <EmployeeDashboard currentUser={currentUser} onLogout={() => setCurrentUser(null)} records={records} setRecords={setRecords} />;
}

// ===================== LOGIN =====================
function LoginScreen({ onLogin, employees }) {
  const [inputId, setInputId] = useState('');
  const [error, setError] = useState('');
  const [loading, setLoading] = useState(false);
  const handleSubmit = (e) => {
    e.preventDefault(); setLoading(true); setError('');
    setTimeout(() => {
      if (inputId === ADMIN_ID) { onLogin('admin'); }
      else { const emp = employees.find(e => e.id === inputId); emp ? onLogin(emp) : setError('ID tidak valid. Periksa kembali ID Anda.'); }
      setLoading(false);
    }, 600);
  };
  return (
    <div className="min-h-screen bg-slate-50 flex items-center justify-center p-4 relative overflow-hidden">
      <div className="absolute top-0 left-0 w-full h-1/3 bg-indigo-600 rounded-b-3xl"></div>
      <div className="relative bg-white p-8 rounded-2xl shadow-2xl max-w-md w-full border border-slate-100">
        <div className="text-center mb-8">
          <div className="bg-indigo-50 w-20 h-20 rounded-2xl flex items-center justify-center mx-auto mb-4">
            <ClockIcon size={40} className="text-indigo-600" />
          </div>
          <h1 className="text-3xl font-extrabold text-slate-800">Portal Kehadiran</h1>
          <p className="text-slate-500 mt-1">Masuk untuk mengelola absensi Anda</p>
        </div>
        <form onSubmit={handleSubmit} className="space-y-5">
          <div>
            <label className="block text-sm font-medium text-slate-700 mb-2">ID Karyawan / Admin</label>
            <input type="password" placeholder="Masukkan ID Anda" required
              className="w-full px-5 py-4 rounded-xl border border-slate-200 bg-slate-50 outline-none text-slate-700 font-medium tracking-widest text-center focus:ring-2 focus:ring-indigo-500"
              value={inputId} onChange={e => setInputId(e.target.value)} />
          </div>
          {error && <div className="p-3 bg-red-50 border-l-4 border-red-500 text-red-700 text-sm rounded">{error}</div>}
          <button type="submit" disabled={loading}
            className="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-4 rounded-xl flex justify-center items-center gap-2 disabled:opacity-70">
            {loading ? 'Memverifikasi...' : 'Masuk ke Sistem'}
            {!loading && <ChevronRightIcon size={20} />}
          </button>
        </form>
        <p className="text-xs text-slate-400 text-center mt-6 pt-4 border-t border-slate-100">
          © {new Date().getFullYear()} Enterprise HR System
        </p>
      </div>
    </div>
  );
}

// ===================== ADMIN DASHBOARD =====================
function AdminDashboard({ onLogout, employees, setEmployees, records }) {
  const [tab, setTab] = useState('laporan');
  return (
    <div className="min-h-screen bg-slate-50 flex flex-col md:flex-row">
      <aside className="w-full md:w-64 bg-slate-900 text-slate-300 flex flex-col">
        <div className="p-6 flex items-center gap-3 border-b border-slate-800">
          <div className="bg-indigo-500 p-2 rounded-lg"><UsersIcon size={22} className="text-white" /></div>
          <div><h2 className="font-bold text-white">Admin Portal</h2><p className="text-xs text-slate-400">HR Management System</p></div>
        </div>
        <nav className="p-4 flex-1 flex flex-col gap-2">
          <p className="text-xs font-semibold text-slate-500 uppercase tracking-wider mt-3 mb-1">Menu</p>
          {[['laporan','Laporan Absensi',<FileTextIcon size={18}/>],['karyawan','Data Karyawan',<UsersIcon size={18}/>]].map(([key,label,icon])=>(
            <button key={key} onClick={()=>setTab(key)}
              className={`w-full flex items-center gap-3 px-4 py-3 rounded-xl text-left transition-all ${tab===key?'bg-indigo-600 text-white':'hover:bg-slate-800 hover:text-white'}`}>
              {icon}<span className="font-medium">{label}</span>
            </button>
          ))}
          <div className="mt-auto pt-6">
            <button onClick={onLogout} className="w-full flex items-center justify-center gap-2 px-4 py-3 rounded-xl text-red-400 hover:bg-red-500/10 border border-slate-800">
              <LogOutIcon size={18}/><span>Keluar</span>
            </button>
          </div>
        </nav>
      </aside>
      <main className="flex-1 p-6 md:p-8 overflow-auto min-h-screen">
        <div className="max-w-5xl mx-auto">
          {tab === 'karyawan' ? <AdminKaryawan employees={employees} setEmployees={setEmployees}/> : <AdminLaporan records={records}/>}
        </div>
      </main>
    </div>
  );
}

// ===================== ADMIN KARYAWAN =====================
function AdminKaryawan({ employees, setEmployees }) {
  const [form, setForm] = useState({ name:'', position:'', location:'' });
  const [showForm, setShowForm] = useState(false);
  const handleAdd = (e) => {
    e.preventDefault();
    const newId = `KRY-${String(employees.length+1).padStart(3,'0')}`;
    setEmployees([...employees, { id: newId, ...form }]);
    setForm({ name:'', position:'', location:'' }); setShowForm(false);
    alert(`✅ Berhasil!\n\nNama: ${form.name}\nID: ${newId}\n\nBerikan ID ini kepada karyawan.`);
  };
  return (
    <div className="space-y-6">
      <div className="flex justify-between items-center">
        <div><h1 className="text-2xl font-bold text-slate-800">Data Karyawan</h1><p className="text-slate-500 text-sm mt-1">Kelola karyawan & akses login</p></div>
        <button onClick={()=>setShowForm(!showForm)} className="bg-indigo-600 hover:bg-indigo-700 text-white px-4 py-2.5 rounded-xl font-medium flex items-center gap-2">
          {showForm ? <XIcon size={16}/> : <UserPlusIcon size={16}/>} {showForm?'Batal':'Tambah'}
        </button>
      </div>
      {showForm && (
        <div className="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm">
          <h3 className="font-bold text-slate-800 mb-4 pb-3 border-b">Karyawan Baru</h3>
          <form onSubmit={handleAdd} className="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div><label className="text-sm font-medium text-slate-700 block mb-1">Nama Lengkap</label>
              <input required value={form.name} onChange={e=>setForm({...form,name:e.target.value})} placeholder="Nama..." className="w-full border border-slate-200 bg-slate-50 p-3 rounded-xl outline-none"/></div>
            <div><label className="text-sm font-medium text-slate-700 block mb-1">Jabatan</label>
              <input required value={form.position} onChange={e=>setForm({...form,position:e.target.value})} placeholder="Staff IT..." className="w-full border border-slate-200 bg-slate-50 p-3 rounded-xl outline-none"/></div>
            <div className="md:col-span-2"><label className="text-sm font-medium text-slate-700 block mb-1">Lokasi</label>
              <input required value={form.location} onChange={e=>setForm({...form,location:e.target.value})} placeholder="Kantor Pusat..." className="w-full border border-slate-200 bg-slate-50 p-3 rounded-xl outline-none"/></div>
            <div className="md:col-span-2"><button type="submit" className="w-full bg-slate-900 text-white py-3 rounded-xl hover:bg-slate-800 font-medium">Simpan & Generate ID</button></div>
          </form>
        </div>
      )}
      <div className="bg-white rounded-2xl border border-slate-200 overflow-hidden">
        <table className="w-full text-left">
          <thead className="bg-slate-50 border-b border-slate-200 text-sm text-slate-600">
            <tr><th className="p-4 font-semibold">ID</th><th className="p-4 font-semibold">Profil</th><th className="p-4 font-semibold">Lokasi</th><th className="p-4 font-semibold text-right">Status</th></tr>
          </thead>
          <tbody className="divide-y divide-slate-100">
            {employees.map(emp=>(
              <tr key={emp.id} className="hover:bg-slate-50">
                <td className="p-4"><span className="px-2.5 py-1 rounded-md text-sm font-mono bg-indigo-50 text-indigo-700 border border-indigo-100">{emp.id}</span></td>
                <td className="p-4"><div className="font-semibold text-slate-800">{emp.name}</div><div className="text-xs text-slate-500 flex items-center gap-1 mt-0.5"><BriefcaseIcon size={12}/>{emp.position}</div></td>
                <td className="p-4 text-slate-600 text-sm flex items-center gap-1.5 mt-3"><MapPinIcon size={14} className="text-slate-400"/>{emp.location}</td>
                <td className="p-4 text-right"><span className="px-2.5 py-1 rounded-full text-xs font-medium bg-green-100 text-green-800">Aktif</span></td>
              </tr>
            ))}
          </tbody>
        </table>
      </div>
    </div>
  );
}

// ===================== ADMIN LAPORAN =====================
function AdminLaporan({ records }) {
  const [filterLoc, setFilterLoc] = useState('');
  const [filterPeriod, setFilterPeriod] = useState('Semua Waktu');
  const filtered = records.filter(r => {
    const matchLoc = !filterLoc || r.location.toLowerCase().includes(filterLoc.toLowerCase());
    const now = new Date(); const d = new Date(r.time);
    let matchPeriod = true;
    if (filterPeriod==='Hari Ini') matchPeriod = d.toDateString()===now.toDateString();
    else if (filterPeriod==='Minggu Ini') matchPeriod = d >= new Date(now-7*86400000);
    else if (filterPeriod==='Bulan Ini') matchPeriod = d.getMonth()===now.getMonth()&&d.getFullYear()===now.getFullYear();
    return matchLoc && matchPeriod;
  });
  return (
    <div className="space-y-6">
      <div className="flex justify-between items-center">
        <div><h1 className="text-2xl font-bold text-slate-800">Laporan Kehadiran</h1><p className="text-slate-500 text-sm mt-1">Real-time attendance report</p></div>
        <button onClick={()=>window.print()} className="bg-white border border-slate-200 hover:bg-slate-50 text-slate-700 px-4 py-2.5 rounded-xl font-medium flex items-center gap-2 shadow-sm">
          <PrinterIcon size={16}/> Cetak PDF
        </button>
      </div>
      <div className="bg-white p-5 rounded-2xl border border-slate-200 shadow-sm">
        <div className="flex items-center gap-2 mb-4 pb-3 border-b border-slate-100"><SearchIcon size={16} className="text-slate-400"/><span className="font-semibold text-slate-700">Filter</span></div>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
          <div><label className="text-xs font-medium text-slate-500 uppercase tracking-wider block mb-1.5">Periode</label>
            <select value={filterPeriod} onChange={e=>setFilterPeriod(e.target.value)} className="w-full border border-slate-200 bg-slate-50 p-2.5 rounded-lg text-sm outline-none">
              <option>Semua Waktu</option><option>Hari Ini</option><option>Minggu Ini</option><option>Bulan Ini</option>
            </select></div>
          <div><label className="text-xs font-medium text-slate-500 uppercase tracking-wider block mb-1.5">Wilayah</label>
            <input value={filterLoc} onChange={e=>setFilterLoc(e.target.value)} placeholder="Cari lokasi..." className="w-full border border-slate-200 bg-slate-50 p-2.5 rounded-lg text-sm outline-none"/></div>
        </div>
      </div>
      <div className="bg-white rounded-2xl border border-slate-200 overflow-hidden shadow-sm">
        <div className="overflow-x-auto">
          <table className="w-full text-left">
            <thead className="bg-slate-50 border-b border-slate-200">
              <tr><th className="p-4 font-semibold text-slate-600 text-sm">Waktu</th><th className="p-4 font-semibold text-slate-600 text-sm">Karyawan</th><th className="p-4 font-semibold text-slate-600 text-sm">Lokasi</th><th className="p-4 font-semibold text-slate-600 text-sm">Status</th><th className="p-4 font-semibold text-slate-600 text-sm text-center">Foto</th></tr>
            </thead>
            <tbody className="divide-y divide-slate-100">
              {filtered.length > 0 ? filtered.map(r=>(
                <tr key={r.id} className="hover:bg-slate-50">
                  <td className="p-4"><div className="text-sm text-slate-800">{new Date(r.time).toLocaleDateString('id-ID',{day:'2-digit',month:'short',year:'numeric'})}</div><div className="text-sm font-bold text-indigo-600">{new Date(r.time).toLocaleTimeString('id-ID',{hour:'2-digit',minute:'2-digit'})} WIB</div></td>
                  <td className="p-4"><div className="font-semibold text-slate-800">{r.name}</div><div className="text-xs text-slate-400 font-mono">{r.employeeId}</div></td>
                  <td className="p-4 text-slate-600 text-sm">{r.location}</td>
                  <td className="p-4"><span className={`px-3 py-1 rounded-full text-xs font-bold ${r.type==='Check In'?'bg-emerald-50 text-emerald-700':'bg-amber-50 text-amber-700'}`}>{r.type==='Check In'?'Masuk':'Pulang'}</span></td>
                  <td className="p-4 text-center"><img src={r.photo} alt="foto" className="w-10 h-10 rounded-lg object-cover mx-auto border border-slate-200"/></td>
                </tr>
              )) : (
                <tr><td colSpan="5" className="p-10 text-center text-slate-400">
                  <FileTextIcon size={36} className="mx-auto mb-2 opacity-20"/>
                  <p>Tidak ada data ditemukan</p>
                </td></tr>
              )}
            </tbody>
          </table>
        </div>
      </div>
    </div>
  );
}

// ===================== EMPLOYEE DASHBOARD =====================
function EmployeeDashboard({ currentUser, onLogout, records, setRecords }) {
  const [time, setTime] = useState(new Date());
  const [absenType, setAbsenType] = useState(null);
  const [cameraActive, setCameraActive] = useState(false);
  const [photoData, setPhotoData] = useState(null);
  const [stream, setStream] = useState(null);
  const videoRef = useRef(null);
  const canvasRef = useRef(null);

  useEffect(() => { const t = setInterval(()=>setTime(new Date()),1000); return ()=>clearInterval(t); }, []);
  useEffect(() => { if (cameraActive && videoRef.current && stream) videoRef.current.srcObject = stream; }, [cameraActive, stream]);

  const myRecords = records.filter(r=>r.employeeId===currentUser.id).sort((a,b)=>new Date(b.time)-new Date(a.time));

  const startCamera = async () => {
    setPhotoData(null);
    try {
      const s = await navigator.mediaDevices.getUserMedia({ video: { facingMode:'user' } });
      setStream(s); setCameraActive(true);
    } catch { alert('Izin kamera diperlukan.'); cancelFlow(); }
  };
  const stopCamera = () => { stream?.getTracks().forEach(t=>t.stop()); setStream(null); setCameraActive(false); };
  const cancelFlow = () => { stopCamera(); setAbsenType(null); setPhotoData(null); };
  const takePhoto = () => {
    if (!videoRef.current || !canvasRef.current) return;
    const ctx = canvasRef.current.getContext('2d');
    canvasRef.current.width = videoRef.current.videoWidth;
    canvasRef.current.height = videoRef.current.videoHeight;
    ctx.drawImage(videoRef.current, 0, 0);
    setPhotoData(canvasRef.current.toDataURL('image/jpeg', 0.8));
    stopCamera();
  };
  const confirmSubmit = () => {
    if (!photoData || !absenType) return;
    setRecords([{ id:Date.now(), employeeId:currentUser.id, name:currentUser.name, location:currentUser.location, type:absenType, time:new Date().toISOString(), photo:photoData }, ...records]);
    alert(`✅ Berhasil!\nAbsen ${absenType==='Check In'?'Masuk':'Pulang'} pukul ${new Date().toLocaleTimeString('id-ID')}`);
    cancelFlow();
  };

  return (
    <div className="min-h-screen bg-slate-100 flex flex-col">
      <header className="bg-white px-5 py-4 flex justify-between items-center shadow-sm sticky top-0 z-20">
        <div className="flex items-center gap-3">
          <div className="w-10 h-10 bg-indigo-100 rounded-full flex items-center justify-center text-indigo-700 font-bold border border-indigo-200">{currentUser.name.charAt(0)}</div>
          <div><p className="font-bold text-slate-800 leading-tight">{currentUser.name}</p><p className="text-xs text-slate-500">{currentUser.position}</p></div>
        </div>
        <button onClick={onLogout} className="text-slate-400 hover:text-red-500 p-2.5 rounded-full hover:bg-red-50"><LogOutIcon size={20}/></button>
      </header>

      <div className="flex-1 p-4 max-w-lg mx-auto w-full space-y-5 pb-10">
        {/* Clock */}
        <div className="relative overflow-hidden bg-slate-900 rounded-3xl p-7 text-center shadow-xl">
          <div style={{position:'absolute',top:0,right:0,width:'7rem',height:'7rem',background:'#6366f1',borderRadius:'50%',filter:'blur(40px)',opacity:.5,transform:'translate(50%,-50%)'}}/>
          <div style={{position:'absolute',bottom:0,left:0,width:'7rem',height:'7rem',background:'#3b82f6',borderRadius:'50%',filter:'blur(40px)',opacity:.5,transform:'translate(-50%,50%)'}}/>
          <div style={{position:'relative',zIndex:10}}>
            <p className="text-indigo-200 text-xs font-medium uppercase tracking-wide mb-2">{time.toLocaleDateString('id-ID',{weekday:'long',day:'numeric',month:'long',year:'numeric'})}</p>
            <h2 className="text-5xl font-mono font-bold text-white mb-3 tabular-nums">{time.toLocaleTimeString('id-ID',{hour:'2-digit',minute:'2-digit',second:'2-digit'})}</h2>
            <div className="inline-flex items-center gap-1.5 px-3 py-1 rounded-full bg-slate-800 border border-slate-700 text-xs text-slate-300">
              <MapPinIcon size={12}/> {currentUser.location}
            </div>
          </div>
        </div>

        {/* Absen Card */}
        <div className="bg-white rounded-3xl p-5 shadow-sm border border-slate-200">
          {!absenType ? (
            <>
              <div className="text-center mb-4"><h3 className="font-bold text-slate-800">Pilih Jenis Absen</h3><p className="text-sm text-slate-500">Klik untuk membuka kamera selfie</p></div>
              <div className="grid grid-cols-2 gap-4">
                <button onClick={()=>{setAbsenType('Check In');startCamera();}} className="flex flex-col items-center gap-3 bg-emerald-50 hover:bg-emerald-100 border-2 border-emerald-500 text-emerald-700 py-6 rounded-2xl font-bold active:scale-95 transition-transform">
                  <CheckIcon size={32}/><span className="text-lg">MASUK</span>
                </button>
                <button onClick={()=>{setAbsenType('Check Out');startCamera();}} className="flex flex-col items-center gap-3 bg-amber-50 hover:bg-amber-100 border-2 border-amber-500 text-amber-700 py-6 rounded-2xl font-bold active:scale-95 transition-transform">
                  <XIcon size={32}/><span className="text-lg">PULANG</span>
                </button>
              </div>
            </>
          ) : (
            <div className="space-y-4">
              <div className="flex items-center justify-between">
                <button onClick={cancelFlow} className="text-slate-400 hover:text-slate-700 flex items-center gap-1 text-sm"><ArrowLeftIcon size={16}/> Batal</button>
                <h3 className="font-bold text-slate-800">Absen {absenType==='Check In'?'Masuk':'Pulang'}</h3>
              </div>
              <div className="bg-slate-100 rounded-2xl overflow-hidden border-2 border-slate-200 flex items-center justify-center" style={{aspectRatio:'4/3'}}>
                {photoData ? <img src={photoData} alt="selfie" className="w-full h-full object-cover"/>
                  : cameraActive ? <video ref={videoRef} autoPlay playsInline muted className="w-full h-full object-cover"/>
                  : <p className="text-slate-400 text-sm">Memuat kamera...</p>}
                <canvas ref={canvasRef} className="hidden"/>
              </div>
              {!photoData && cameraActive && (
                <button onClick={takePhoto} className="w-full bg-slate-900 hover:bg-slate-800 text-white py-4 rounded-xl font-bold flex items-center justify-center gap-2">
                  <CameraIcon size={20}/> Jepret Foto
                </button>
              )}
              {photoData && (
                <div className="space-y-3">
                  <button onClick={confirmSubmit} className={`w-full text-white py-4 rounded-xl font-bold flex items-center justify-center gap-2 ${absenType==='Check In'?'bg-emerald-500 hover:bg-emerald-600':'bg-amber-500 hover:bg-amber-600'}`}>
                    Kirim Absen {absenType==='Check In'?'Masuk':'Pulang'}
                  </button>
                  <button onClick={startCamera} className="w-full text-sm font-medium text-slate-500 py-3 bg-slate-100 rounded-xl hover:bg-slate-200">Ulangi Foto</button>
                </div>
              )}
            </div>
          )}
        </div>

        {/* Riwayat */}
        <div className="bg-white rounded-3xl p-5 shadow-sm border border-slate-200">
          <div className="flex items-center justify-between mb-4">
            <h3 className="font-bold text-slate-800">Riwayat Absensi</h3>
            <span className="text-xs text-indigo-600 font-medium">Terbaru</span>
          </div>
          <div className="space-y-3 max-h-64 overflow-y-auto custom-scrollbar">
            {myRecords.length > 0 ? myRecords.map(r=>(
              <div key={r.id} className="flex items-center justify-between p-3.5 bg-slate-50 border border-slate-100 rounded-2xl">
                <div className="flex items-center gap-3">
                  <div className={`w-11 h-11 rounded-xl flex items-center justify-center text-white ${r.type==='Check In'?'bg-emerald-500':'bg-amber-500'}`}>
                    {r.type==='Check In'?<CheckIcon size={22}/>:<XIcon size={22}/>}
                  </div>
                  <div>
                    <p className="font-bold text-slate-800 text-sm">{r.type==='Check In'?'Absen Masuk':'Absen Pulang'}</p>
                    <p className="text-xs text-slate-500">{new Date(r.time).toLocaleDateString('id-ID',{weekday:'short',day:'numeric',month:'short'})}</p>
                  </div>
                </div>
                <p className="text-lg font-bold font-mono text-slate-700">{new Date(r.time).toLocaleTimeString('id-ID',{hour:'2-digit',minute:'2-digit'})}</p>
              </div>
            )) : (
              <div className="text-center py-8 text-slate-400">
                <FileTextIcon size={32} className="mx-auto mb-2 opacity-20"/>
                <p className="text-sm">Belum ada aktivitas</p>
              </div>
            )}
          </div>
        </div>
      </div>
    </div>
  );
}

ReactDOM.createRoot(document.getElementById('root')).render(<App/>);
</script>
</body>
</html>

