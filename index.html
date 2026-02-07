<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>背景ジェネレーター - Backdrop Meeting</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script defer src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body { font-family: 'Noto Sans JP', sans-serif; }
        .scrollbar-hide::-webkit-scrollbar { display: none; }
        .scrollbar-hide { -ms-overflow-style: none; scrollbar-width: none; }
        [x-cloak] { display: none !important; }
        .custom-scrollbar::-webkit-scrollbar { width: 6px; }
        .custom-scrollbar::-webkit-scrollbar-track { background: #f1f1f1; }
        .custom-scrollbar::-webkit-scrollbar-thumb { background: #d1d5db; border-radius: 3px; }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover { background: #9ca3af; }
    </style>
</head>
<body class="bg-gray-100 h-screen flex flex-col overflow-hidden" x-data="generator()" x-init="init()">

    <!-- Header -->
    <header class="bg-white border-b border-gray-200 h-14 flex items-center justify-between px-6 z-10 shrink-0">
        <div class="flex items-center gap-2">
            <i class="fa-solid fa-video text-indigo-600"></i>
            <h1 class="font-bold text-gray-800 text-lg">Backdrop Meeting</h1>
        </div>
        <div>
            <button @click="downloadSingle" class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-1.5 px-6 rounded-full shadow transition text-sm flex items-center gap-2">
                <i class="fa-solid fa-download"></i> ダウンロード
            </button>
        </div>
    </header>

    <div class="flex flex-1 overflow-hidden">
        <!-- Left Sidebar (Settings) -->
        <aside class="w-full md:w-96 bg-white border-r border-gray-200 flex flex-col z-10 shadow-lg">
            
            <!-- Tabs -->
            <div class="flex border-b border-gray-200">
                <button @click="tab = 'basic'" :class="{'border-indigo-600 text-indigo-600': tab === 'basic', 'border-transparent text-gray-500 hover:text-gray-700': tab !== 'basic'}" class="flex-1 py-3 text-sm font-medium border-b-2 transition">
                    基本情報
                </button>
                <button @click="tab = 'design'" :class="{'border-indigo-600 text-indigo-600': tab === 'design', 'border-transparent text-gray-500 hover:text-gray-700': tab !== 'design'}" class="flex-1 py-3 text-sm font-medium border-b-2 transition">
                    デザイン
                </button>
                <button @click="tab = 'extra'" :class="{'border-indigo-600 text-indigo-600': tab === 'extra', 'border-transparent text-gray-500 hover:text-gray-700': tab !== 'extra'}" class="flex-1 py-3 text-sm font-medium border-b-2 transition">
                    ロゴ・QR
                </button>
                <button @click="tab = 'bulk'" :class="{'border-indigo-600 text-indigo-600': tab === 'bulk', 'border-transparent text-gray-500 hover:text-gray-700': tab !== 'bulk'}" class="flex-1 py-3 text-sm font-medium border-b-2 transition">
                    一括生成
                </button>
            </div>

            <!-- Form Content -->
            <div class="flex-1 overflow-y-auto p-6 custom-scrollbar">
                <form id="generatorForm" action="#" onsubmit="return false;" method="POST" target="_blank" enctype="multipart/form-data">
                    
                    <!-- Basic Info Tab -->
                    <div x-show="tab === 'basic'">
                        <div class="space-y-4">
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-1">会社名 / 所属</label>
                                <input type="text" name="company" x-model="text.company" @input="draw()"
                                    class="w-full bg-gray-50 border border-gray-300 rounded px-3 py-2 text-sm focus:outline-none focus:border-indigo-500 transition"
                                    placeholder="株式会社〇〇">
                            </div>

                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-1">部門・役職</label>
                                <input type="text" name="position" x-model="text.position" @input="draw()"
                                    class="w-full bg-gray-50 border border-gray-300 rounded px-3 py-2 text-sm focus:outline-none focus:border-indigo-500 transition"
                                    placeholder="営業部 マネージャー">
                            </div>

                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-1">お名前</label>
                                <input type="text" name="name" x-model="text.name" @input="draw()"
                                    class="w-full bg-gray-50 border border-gray-300 rounded px-3 py-2 text-sm focus:outline-none focus:border-indigo-500 transition"
                                    placeholder="山田 太郎">
                            </div>
                            
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-1">英語表記 / その他</label>
                                <input type="text" name="english_name" x-model="text.english_name" @input="draw()"
                                    class="w-full bg-gray-50 border border-gray-300 rounded px-3 py-2 text-sm focus:outline-none focus:border-indigo-500 transition"
                                    placeholder="Taro Yamada">
                            </div>
                        </div>
                    </div>

                    <!-- Design Tab -->
                    <div x-show="tab === 'design'" x-cloak>
                        <div class="space-y-6">
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-2">テンプレート選択</label>
                                <div class="grid grid-cols-2 gap-3 mb-4">
                                    <template x-for="t in templates" :key="t.id">
                                        <label class="cursor-pointer relative group">
                                            <input type="radio" name="template_id" :value="t.id" 
                                                @change="changeTemplate(t); clearCustomBg()"
                                                class="peer hidden" :checked="t.id == template.id">
                                            <div class="h-20 rounded-lg border-2 border-gray-200 peer-checked:border-indigo-500 peer-checked:ring-2 peer-checked:ring-indigo-200 bg-gray-100 flex items-center justify-center overflow-hidden">
                                                <div class="text-xs font-bold text-gray-500 text-center px-1" x-text="t.name"></div>
                                            </div>
                                            <div class="absolute inset-0 bg-black bg-opacity-0 group-hover:bg-opacity-5 transition rounded-lg"></div>
                                        </label>
                                    </template>
                                </div>

                                <label class="block text-gray-700 text-xs font-bold mb-2">または背景画像をアップロード</label>
                                <div class="flex items-center justify-center w-full mb-2">
                                    <label class="flex flex-col w-full h-24 border-2 border-gray-300 border-dashed rounded cursor-pointer hover:bg-gray-50 transition"
                                           :class="{'border-indigo-500 bg-indigo-50': bgImage}">
                                        <div class="flex flex-col items-center justify-center pt-5">
                                            <i class="fa-solid fa-image text-gray-400 text-xl mb-1" :class="{'text-indigo-500': bgImage}"></i>
                                            <p class="text-xs text-gray-500 group-hover:text-gray-700" x-text="bgImage ? '変更する' : 'クリックしてアップロード'"></p>
                                        </div>
                                        <input type="file" name="bg_file" class="hidden" accept="image/*" @change="handleBgUpload">
                                    </label>
                                </div>
                                <div x-show="bgImage" class="flex items-center gap-2 mb-4">
                                    <p class="text-xs text-green-600"><i class="fa-solid fa-check"></i> カスタム背景適用中</p>
                                    <button type="button" @click="clearCustomBg" class="text-xs text-red-500 underline">リセット</button>
                                </div>
                            </div>
                            
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-2">文字色</label>
                                <div class="flex gap-2 mb-4">
                                    <template x-for="color in ['#333333', '#ffffff', '#1f2937', '#2563eb', '#dc2626']">
                                        <button type="button" @click="text.color = color; draw()"
                                            class="w-8 h-8 rounded-full border border-gray-300 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500"
                                            :style="`background-color: ${color}`"></button>
                                    </template>
                                    <input type="color" x-model="text.color" @input="draw()" class="h-8 w-8 p-0 border-0 rounded-full overflow-hidden cursor-pointer">
                                </div>
                            </div>
                            
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-2">テキスト背景（帯）</label>
                                <div class="space-y-3">
                                    <!-- 背景ON/OFF -->
                                    <label class="flex items-center">
                                        <input type="checkbox" x-model="textBg.enabled" @change="draw()" class="form-checkbox h-4 w-4 text-indigo-600 transition duration-150 ease-in-out">
                                        <span class="ml-2 text-sm text-gray-700">テキスト背景を表示する</span>
                                    </label>
                                    
                                    <div x-show="textBg.enabled" class="pl-4 space-y-3 border-l-2 border-gray-200">
                                        <!-- 背景色 -->
                                        <div>
                                            <label class="block text-gray-600 text-xs mb-1">背景色</label>
                                            <div class="flex gap-2">
                                                <template x-for="color in ['#ffffff', '#000000', '#f3f4f6', '#1f2937']">
                                                    <button type="button" @click="textBg.color = color; draw()"
                                                        class="w-6 h-6 rounded border border-gray-300 focus:outline-none focus:ring-1 focus:ring-indigo-500"
                                                        :style="`background-color: ${color}`"></button>
                                                </template>
                                                <input type="color" x-model="textBg.color" @input="draw()" class="h-6 w-8 p-0 border-0 rounded cursor-pointer">
                                            </div>
                                        </div>
                                        
                                        <!-- 透明度 -->
                                        <div>
                                            <label class="block text-gray-600 text-xs mb-1">透明度 (<span>0% - 100%</span>)</label>
                                            <input type="range" x-model="textBg.opacity" @input="draw()" min="0" max="1" step="0.1" class="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer">
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Logo & QR Tab -->
                    <div x-show="tab === 'extra'" x-cloak>
                        <div class="space-y-6">
                            
                            <!-- Logo Upload -->
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-2">ロゴ画像</label>
                                <div class="flex items-center justify-center w-full">
                                    <label class="flex flex-col w-full h-32 border-2 border-gray-300 border-dashed rounded cursor-pointer hover:bg-gray-50 transition">
                                        <div class="flex flex-col items-center justify-center pt-7">
                                            <i class="fa-solid fa-cloud-arrow-up text-gray-400 text-2xl mb-2"></i>
                                            <p class="text-xs text-gray-500 group-hover:text-gray-700">クリックしてアップロード</p>
                                        </div>
                                        <input type="file" name="logo_file" class="hidden" accept="image/*" @change="handleLogoUpload">
                                    </label>
                                </div>
                                <div x-show="logoImage" class="mt-2 flex items-center gap-2">
                                    <p class="text-xs text-green-600"><i class="fa-solid fa-check"></i> 選択済み</p>
                                    <button type="button" @click="clearLogo" class="text-xs text-red-500 underline">削除（解除）</button>
                                </div>
                                
                                <div x-show="logoImage" class="mt-3 bg-gray-50 p-3 rounded">
                                    <label class="block text-gray-600 text-xs mb-1 flex justify-between">
                                        <span>サイズ調整</span>
                                        <span class="font-bold" x-text="logoSize + 'px'"></span>
                                    </label>
                                    <input type="range" x-model="logoSize" @input="draw()" min="50" max="600" step="10" class="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer">
                                </div>
                            </div>

                            <!-- QR Code -->
                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-2">QRコード生成</label>
                                <input type="text" name="qr_text" x-model="qrText" @input="generateQR"
                                    class="w-full bg-gray-50 border border-gray-300 rounded px-3 py-2 text-sm focus:outline-none focus:border-indigo-500 transition"
                                    placeholder="https://example.com (URLなど)">
                                <p class="text-xs text-gray-400 mt-1">※URLを入力するとQRコードが右下に配置されます。</p>
                                <div id="qrcode-container" class="hidden"></div>
                            </div>
                            
                            <hr class="border-gray-200">
                            
                            <!-- Notice -->
                            <div class="bg-blue-50 p-3 rounded border border-blue-100 text-xs text-blue-700">
                                <p><i class="fa-solid fa-circle-info mr-1"></i> ヒント</p>
                                <p class="mt-1">ダウンロード画像は高画質(1920x1080)で生成されます。プレビューと厳密な位置が異なる場合があります。</p>
                            </div>

                        </div>
                    </div>

                    <!-- Bulk Generation Tab -->
                    <div x-show="tab === 'bulk'" x-cloak>
                        <div class="space-y-6">
                            <div class="bg-yellow-50 p-3 rounded border border-yellow-100 text-xs text-yellow-800 mb-4">
                                <p class="font-bold"><i class="fa-solid fa-triangle-exclamation mr-1"></i> 使い方</p>
                                <p class="mt-1">CSVファイルを読み込むと、現在のデザイン設定（共通の会社名・ロゴなど）を使って人数分の画像を生成し、ZIPでまとめてダウンロードできます。</p>
                                <p class="mt-2 font-bold">CSVフォーマット（ヘッダーなし推奨）:</p>
                                <p class="font-mono bg-white p-1 border mt-1">1列目: 部門・役職<br>2列目: お名前<br>3列目: 英語表記</p>
                            </div>

                            <div>
                                <label class="block text-gray-700 text-xs font-bold mb-2">CSVファイル選択</label>
                                <input type="file" accept=".csv" @change="handleCsvUpload" class="block w-full text-sm text-gray-500 file:mr-4 file:py-2 file:px-4 file:rounded-full file:border-0 file:text-sm file:font-semibold file:bg-indigo-50 file:text-indigo-700 hover:file:bg-indigo-100 transition"/>
                            </div>

                            <div x-show="csvData.length > 0">
                                <div class="flex items-center justify-between mb-2">
                                    <h3 class="text-xs font-bold text-gray-700">読み込み結果 (<span x-text="csvData.length"></span>件)</h3>
                                    <button type="button" @click="generateBulkZip" :disabled="bulkLoading" class="bg-indigo-600 hover:bg-indigo-700 text-white text-xs font-bold py-1.5 px-3 rounded shadow transition flex items-center gap-1 disabled:opacity-50">
                                        <span x-show="!bulkLoading"><i class="fa-solid fa-file-zipper"></i> ZIP生成実行</span>
                                        <span x-show="bulkLoading"><i class="fa-solid fa-spinner fa-spin"></i> 生成中...</span>
                                    </button>
                                </div>
                                <div class="max-h-64 overflow-y-auto border rounded text-xs">
                                    <table class="min-w-full divide-y divide-gray-200">
                                        <thead class="bg-gray-50">
                                            <tr>
                                                <th class="px-3 py-2 text-left font-medium text-gray-500">役職</th>
                                                <th class="px-3 py-2 text-left font-medium text-gray-500">名前</th>
                                                <th class="px-3 py-2 text-left font-medium text-gray-500">英語名</th>
                                            </tr>
                                        </thead>
                                        <tbody class="bg-white divide-y divide-gray-200">
                                            <template x-for="(row, index) in csvData" :key="index">
                                                <tr>
                                                    <td class="px-3 py-2 text-gray-500" x-text="row.position"></td>
                                                    <td class="px-3 py-2 font-bold text-gray-800" x-text="row.name"></td>
                                                    <td class="px-3 py-2 text-gray-400" x-text="row.english_name"></td>
                                                </tr>
                                            </template>
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                    </div>
                </form>
            </div>
            
            <!-- Footer Area -->
            <div class="p-4 border-t border-gray-200 bg-gray-50">
                <p class="text-xs text-gray-500 text-center">© 2026 Backdrop Meeting Generator</p>
            </div>
        </aside>

        <!-- Main Preview Area -->
        <main class="flex-1 bg-gray-200 flex items-center justify-center p-8 relative overflow-hidden">
            <!-- Background Pattern -->
            <div class="absolute inset-0 opacity-10 pointer-events-none" style="background-image: radial-gradient(#6366f1 1px, transparent 1px); background-size: 20px 20px;"></div>

            <!-- Canvas Container -->
            <div class="relative shadow-2xl rounded-lg overflow-hidden bg-white max-w-full max-h-full" style="aspect-ratio: 16/9;">
                <canvas id="previewCanvas" width="1920" height="1080" class="w-full h-full block object-contain" style="max-height: 80vh; max-width: 100%;"></canvas>
                
                <!-- Loading Overlay -->
                <div x-show="loading" class="absolute inset-0 flex items-center justify-center bg-white bg-opacity-80 z-20">
                    <div class="animate-spin rounded-full h-12 w-12 border-b-2 border-indigo-600"></div>
                </div>
            </div>
        </main>
    </div>

    <script>
        const templates = [
            {
                id: 1,
                name: 'シンプル・オフィス',
                image_file: 'office_01.jpg',
                color: '#333333',
                layout: 'standard'
            },
            {
                id: 2,
                name: 'モダン・ブルー',
                image_file: 'modern_blue.jpg',
                color: '#ffffff',
                layout: 'centered'
            }
        ];

        // IndexedDB Helper for saving large images
        const dbName = 'BackdropDB';
        const storeName = 'images';

        function openDB() {
            return new Promise((resolve, reject) => {
                const request = indexedDB.open(dbName, 1);
                request.onupgradeneeded = (e) => {
                    if (!e.target.result.objectStoreNames.contains(storeName)) {
                        e.target.result.createObjectStore(storeName);
                    }
                };
                request.onsuccess = (e) => resolve(e.target.result);
                request.onerror = (e) => reject(e);
            });
        }

        async function saveImageToDB(key, blob) {
            try {
                const db = await openDB();
                const tx = db.transaction(storeName, 'readwrite');
                tx.objectStore(storeName).put(blob, key);
            } catch (e) { console.error('DB Save Error', e); }
        }

        async function getImageFromDB(key) {
            try {
                const db = await openDB();
                return new Promise((resolve) => {
                    const tx = db.transaction(storeName, 'readonly');
                    const req = tx.objectStore(storeName).get(key);
                    req.onsuccess = () => resolve(req.result);
                    req.onerror = () => resolve(null);
                });
            } catch (e) { 
                console.error('DB Load Error', e); 
                return null;
            }
        }

        async function deleteImageFromDB(key) {
            try {
                const db = await openDB();
                const tx = db.transaction(storeName, 'readwrite');
                tx.objectStore(storeName).delete(key);
            } catch (e) { console.error('DB Delete Error', e); }
        }

        function generator() {
            return {
                tab: 'basic',
                loading: false,
                bulkLoading: false,
                csvData: [],
                templates: templates,
                template: templates[0],
                text: {
                    company: '',
                    position: '',
                    name: '',
                    english_name: '',
                    color: '#333333'
                },
                textBg: {
                    enabled: false,
                    color: '#ffffff',
                    opacity: 0.8
                },
                qrText: '',
                logoSize: 350,
                logoImage: null, // Image object
                bgImage: null, // Image object (Custom Background)
                qrImage: null, // Image object
                canvas: null,
                ctx: null,
                
                init() {
                    this.canvas = document.getElementById('previewCanvas');
                    this.ctx = this.canvas.getContext('2d');
                    
                    // Load settings
                    this.loadSettings();

                    // Restore Images from DB
                    this.restoreImages();

                    // Initial Draw
                    this.draw();
                },

                changeTemplate(t) {
                    this.template = t;
                    this.draw();
                },

                async restoreImages() {
                    // Restore Custom Background
                    const bgFile = await getImageFromDB('bg_file');
                    if (bgFile) {
                         const reader = new FileReader();
                         reader.onload = (e) => {
                             const img = new Image();
                             img.onload = () => { this.bgImage = img; this.draw(); };
                             img.src = e.target.result;
                         };
                         reader.readAsDataURL(bgFile);
                    }

                    // Restore Logo
                    const logoFile = await getImageFromDB('logo_file');
                    if (logoFile) {
                         const reader = new FileReader();
                         reader.onload = (e) => {
                             const img = new Image();
                             img.onload = () => { this.logoImage = img; this.draw(); };
                             img.src = e.target.result;
                         };
                         reader.readAsDataURL(logoFile);
                    }
                },

                loadSettings() {
                    const saved = localStorage.getItem('backdrop_settings');
                    if (saved) {
                        try {
                            const data = JSON.parse(saved);
                            if (data.text) this.text = { ...this.text, ...data.text };
                            if (data.textBg) this.textBg = { ...this.textBg, ...data.textBg };
                            if (data.qrText) this.qrText = data.qrText;
                            if (data.logoSize) this.logoSize = data.logoSize;
                            
                            // Generate QR if needed
                            if (this.qrText) {
                                this.generateQR();
                            }
                        } catch(e) { console.error(e); }
                    } else {
                         this.text.color = this.template.color;
                    }
                },

                // 背景アップロード処理
                handleBgUpload(e) {
                    const file = e.target.files[0];
                    if (!file) return;
                    
                    saveImageToDB('bg_file', file); // Save to DB

                    const reader = new FileReader();
                    reader.onload = (event) => {
                        const img = new Image();
                        img.onload = () => {
                            this.bgImage = img;
                            this.draw();
                        };
                        img.src = event.target.result;
                    };
                    reader.readAsDataURL(file);
                },

                clearCustomBg() {
                    this.bgImage = null;
                    const input = document.querySelector('input[name="bg_file"]');
                    if (input) input.value = '';
                    deleteImageFromDB('bg_file'); // Delete from DB
                    this.draw();
                },

                // ロゴアップロード処理
                handleLogoUpload(e) {
                    const file = e.target.files[0];
                    if (!file) return;
                    
                    saveImageToDB('logo_file', file); // Save to DB

                    const reader = new FileReader();
                    reader.onload = (event) => {
                        const img = new Image();
                        img.onload = () => {
                            this.logoImage = img;
                            this.draw();
                        };
                        img.src = event.target.result;
                    };
                    reader.readAsDataURL(file);
                },

                clearLogo() {
                    this.logoImage = null;
                    const input = document.querySelector('input[name="logo_file"]');
                    if(input) input.value = '';
                    deleteImageFromDB('logo_file'); // Delete from DB
                    this.draw();
                },
                
                saveSettings() {
                    const settings = {
                        text: this.text,
                        textBg: this.textBg,
                        qrText: this.qrText,
                        logoSize: this.logoSize
                    };
                    localStorage.setItem('backdrop_settings', JSON.stringify(settings));
                },

                generateQR() {
                    if (!this.qrText) {
                        this.qrImage = null;
                        this.draw();
                        return;
                    }

                    // QRコード生成ライブラリを使用
                    const container = document.getElementById('qrcode-container');
                    container.innerHTML = '';
                    
                    try {
                        const qrcode = new QRCode(container, {
                            text: this.qrText,
                            width: 256,
                            height: 256,
                            correctLevel: QRCode.CorrectLevel.H
                        });

                        // Canvas変換待ち
                        setTimeout(() => {
                            const qrCanvas = container.querySelector('canvas');
                            if (qrCanvas) {
                                const img = new Image();
                                img.onload = () => {
                                    this.qrImage = img;
                                    this.draw();
                                };
                                img.src = qrCanvas.toDataURL();
                            } else {
                                // fallback for img based qrcode.js
                                const qrImg = container.querySelector('img');
                                if(qrImg) {
                                     const img = new Image();
                                     img.onload = () => {
                                         this.qrImage = img;
                                         this.draw();
                                     };
                                     img.src = qrImg.src;
                                }
                            }
                        }, 200);
                    } catch(e) {
                        console.error("QR Generation failed", e);
                    }
                },

                draw() {
                    this.saveSettings();
                    this.loading = true;
                    
                    // 背景クリア
                    this.ctx.fillStyle = '#ffffff';
                    this.ctx.fillRect(0, 0, this.canvas.width, this.canvas.height);

                    // 1. 背景描画
                    if (this.bgImage) {
                         // カスタム背景 (Cover)
                         const hRatio = this.canvas.width / this.bgImage.width;
                         const vRatio = this.canvas.height / this.bgImage.height;
                         const ratio  = Math.max(hRatio, vRatio);
                         const centerShift_x = (this.canvas.width - this.bgImage.width * ratio) / 2;
                         const centerShift_y = (this.canvas.height - this.bgImage.height * ratio) / 2;  
                         
                         this.ctx.drawImage(this.bgImage, 
                            0, 0, this.bgImage.width, this.bgImage.height,
                            centerShift_x, centerShift_y, this.bgImage.width * ratio, this.bgImage.height * ratio
                         );
                    } else if (this.template.id == 1) {
                         // オフィス
                         this.ctx.fillStyle = '#f3f4f6';
                         this.ctx.fillRect(0, 0, 1920, 1080);
                    } else {
                         // モダンブルー
                         this.ctx.fillStyle = '#eff6ff';
                         this.ctx.fillRect(0, 0, 1920, 1080);
                         this.ctx.fillStyle = '#3b82f6';
                         this.ctx.beginPath();
                         this.ctx.arc(1600, 200, 400, 0, 2 * Math.PI);
                         this.ctx.fill();
                    }

                    // 2. テキスト描画設定
                    this.ctx.fillStyle = this.text.color;
                    this.ctx.textAlign = (this.template.layout === 'centered') ? 'center' : 'left';
                    this.ctx.textBaseline = 'top';
                    
                    let x, y;
                    
                    if (this.template.layout === 'centered') {
                        x = 960;
                        y = 750; // 中央下部へ移動
                    } else {
                        x = 100; // 左端
                        y = 200; // 左上（ロゴの下あたり）
                    }

                    // 1.5 テキスト背景（帯）描画
                    if (this.textBg.enabled) {
                        this.ctx.save();
                        this.ctx.globalAlpha = this.textBg.opacity;
                        this.ctx.fillStyle = this.textBg.color;
                        
                        if (this.template.layout === 'centered') {
                             // 中央配置の場合は下部に帯
                             this.ctx.fillRect(0, 700, 1920, 380);
                        } else {
                             // 左配置の場合は左サイドバー（縦100%）
                             // 幅はテキストエリア＋余裕
                             this.ctx.fillRect(0, 0, 750, 1080);
                        }
                        
                        this.ctx.restore();
                    }

                    // 会社名
                    this.ctx.font = 'bold 40px "Noto Sans JP", sans-serif';
                    this.ctx.fillText(this.text.company, x, y);

                    // 部門・役職
                    y += 60;
                    this.ctx.font = '30px "Noto Sans JP", sans-serif';
                    this.ctx.fillText(this.text.position, x, y);

                    // 名前
                    y += 80;
                    this.ctx.font = 'bold 80px "Noto Sans JP", sans-serif';
                    this.ctx.fillText(this.text.name, x, y);

                    // 英語名
                    y += 100;
                    this.ctx.font = '30px "Noto Sans JP", sans-serif';
                    this.ctx.fillText(this.text.english_name, x, y);

                    // 3. ロゴ描画
                    if (this.logoImage) {
                        const w = parseInt(this.logoSize); 
                        const h = w * (this.logoImage.height / this.logoImage.width);
                        // 左上に配置
                        this.ctx.drawImage(this.logoImage, 100, 100, w, h);
                    }

                    // 4. QRコード描画
                    if (this.qrImage) {
                         const qrSize = 250;
                         // 右上に配置 (変更: 右下 -> 右上)
                         this.ctx.drawImage(this.qrImage, 1920 - qrSize - 50, 50, qrSize, qrSize);
                    }

                    this.loading = false;
                },

                // CSVアップロード処理
                 handleCsvUpload(e) {
                    const file = e.target.files[0];
                    if (!file) return;

                    const reader = new FileReader();
                    reader.onload = (event) => {
                        const buffer = event.target.result;
                        let text;
                        
                        // まずUTF-8で試みる
                        try {
                            const decoder = new TextDecoder("utf-8", { fatal: true });
                            text = decoder.decode(buffer);
                        } catch(e) {
                            // 失敗したらShift_JISで試みる
                            try {
                                const decoder = new TextDecoder("shift-jis");
                                text = decoder.decode(buffer);
                            } catch(e2) {
                                alert("ファイルの読み込みに失敗しました。");
                                return;
                            }
                        }
                        this.parseCSV(text);
                    };
                    reader.readAsArrayBuffer(file);
                },

                parseCSV(text) {
                    const lines = text.split(/\r\n|\n/);
                    const data = [];
                    
                    lines.forEach(line => {
                        // 空行スキップ
                        if (!line.trim()) return;
                        
                        // カンマ区切り（簡易パース。セル内のカンマなどは非対応）
                        const cols = line.split(',').map(c => c.trim().replace(/^"|"$/g, '')); // 引用符削除
                        
                        // データ生成（足りないカラムは空文字）
                        data.push({
                            position: cols[0] || '',
                            name: cols[1] || '',
                            english_name: cols[2] || ''
                        });
                    });
                    
                    this.csvData = data;
                },

                async generateBulkZip() {
                    if (this.csvData.length === 0) return;
                    
                    this.bulkLoading = true;
                    const zip = new JSZip();
                    
                    // 現在の入力値を保存（生成後に戻すため）
                    const originalText = { ...this.text };
                    
                    try {
                        // 1件ずつCanvasに描画してBlob化
                        for (let i = 0; i < this.csvData.length; i++) {
                            const row = this.csvData[i];
                            
                            // データをセット
                            this.text.position = row.position;
                            this.text.name = row.name;
                            this.text.english_name = row.english_name;
                            // 会社名は現在の入力値を使用
                            
                            // 描画 (同期的に行われるが、念のため)
                            this.draw();
                            
                            // CanvasからBlobを取得 (Promiseラッパー)
                            const blob = await new Promise(resolve => this.canvas.toBlob(resolve, 'image/png'));
                            
                            // ファイル名 (例: 1_山田太郎.png)
                            const fileName = `${i + 1}_${row.name || 'noname'}.png`;
                            zip.file(fileName, blob);
                        }
                        
                        // ZIP生成
                        const content = await zip.generateAsync({type: "blob"});
                        saveAs(content, "backdrops.zip");
                        
                    } catch (e) {
                        console.error(e);
                        alert('生成中にエラーが発生しました');
                    } finally {
                        // 元に戻す
                        this.text = originalText;
                        this.draw();
                        this.bulkLoading = false;
                    }
                },

                submitForm() {
                    // document.getElementById('generatorForm').submit();
                },

                // 単発ダウンロード（Canvasを直接保存）
                downloadSingle() {
                   this.canvas.toBlob((blob) => {
                       saveAs(blob, "backdrop_" + (this.text.name || 'meeting') + ".png");
                   });
                },
                
                // 角丸四角形描画ヘルパー
                roundRect(ctx, x, y, width, height, radius, fill, stroke) {
                    if (typeof stroke === 'undefined') { stroke = true; }
                    if (typeof radius === 'undefined') { radius = 5; }
                    if (typeof radius === 'number') { radius = {tl: radius, tr: radius, br: radius, bl: radius}; }
                    else {
                        var defaultRadius = {tl: 0, tr: 0, br: 0, bl: 0};
                        for (var side in defaultRadius) { radius[side] = radius[side] || defaultRadius[side]; }
                    }
                    ctx.beginPath();
                    ctx.moveTo(x + radius.tl, y);
                    ctx.lineTo(x + width - radius.tr, y);
                    ctx.quadraticCurveTo(x + width, y, x + width, y + radius.tr);
                    ctx.lineTo(x + width, y + height - radius.br);
                    ctx.quadraticCurveTo(x + width, y + height, x + width - radius.br, y + height);
                    ctx.lineTo(x + radius.bl, y + height);
                    ctx.quadraticCurveTo(x, y + height, x, y + height - radius.bl);
                    ctx.lineTo(x, y + radius.tl);
                    ctx.quadraticCurveTo(x, y, x + radius.tl, y);
                    ctx.closePath();
                    if (fill) { ctx.fill(); }
                    if (stroke) { ctx.stroke(); }
                }
            }
        }
    </script>
</body>
</html>