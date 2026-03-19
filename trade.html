[okx-trade-pro.html](https://github.com/user-attachments/files/26120659/okx-trade-pro.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#0B0E11">
    <title>OKX Pro - 专业数字资产交易平台</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://unpkg.com/lightweight-charts@4.1.0/dist/lightweight-charts.standalone.production.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>
    
    <style>
        * { box-sizing: border-box; }
        body { background-color: #0B0E11; color: #E5E9F0; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; overflow-x: hidden; }
        ::-webkit-scrollbar { width: 6px; height: 6px; }
        ::-webkit-scrollbar-track { background: #1E2228; }
        ::-webkit-scrollbar-thumb { background: #363C49; border-radius: 3px; }
        
        .glass { background: rgba(30, 34, 40, 0.95); backdrop-filter: blur(12px); }
        .price-up { animation: flashGreen 0.5s ease-out; }
        .price-down { animation: flashRed 0.5s ease-out; }
        @keyframes flashGreen { 0% { background-color: rgba(0, 196, 140, 0.3); } 100% { background-color: transparent; } }
        @keyframes flashRed { 0% { background-color: rgba(246, 70, 93, 0.3); } 100% { background-color: transparent; } }
        .depth-bar { position: absolute; top: 0; bottom: 0; opacity: 0.15; transition: width 0.3s ease; }
        .depth-bar.ask { right: 0; background: #F6465D; }
        .depth-bar.bid { left: 0; background: #00C48C; }
        
        .toast { position: fixed; top: 80px; right: 20px; padding: 12px 20px; border-radius: 8px; color: white; font-size: 14px; z-index: 9999; transform: translateX(400px); transition: transform 0.3s ease; }
        .toast.show { transform: translateX(0); }
        .toast.success { background: linear-gradient(135deg, #00C48C, #00A376); }
        .toast.error { background: linear-gradient(135deg, #F6465D, #D63A4E); }
        
        .modal { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.8); z-index: 100; align-items: center; justify-content: center; padding: 20px; }
        .modal.active { display: flex; }
        .modal-content { background: #1E2228; border-radius: 16px; width: 100%; max-width: 420px; max-height: 90vh; overflow-y: auto; transform: scale(0.9); opacity: 0; transition: all 0.3s ease; }
        .modal.active .modal-content { transform: scale(1); opacity: 1; }
        
        .input-group { position: relative; margin-bottom: 16px; }
        .input-group input { width: 100%; background: #2A2E39; border: 1px solid #363C49; border-radius: 8px; padding: 12px 16px; color: white; font-size: 14px; transition: all 0.2s; }
        .input-group input:focus { outline: none; border-color: #00C48C; box-shadow: 0 0 0 3px rgba(0, 196, 140, 0.1); }
        .input-group input.error { border-color: #F6465D; }
        .input-group .error-msg { color: #F6465D; font-size: 12px; margin-top: 4px; display: none; }
        .input-group input.error + .error-msg { display: block; }
        .input-group .icon { position: absolute; left: 12px; top: 50%; transform: translateY(-50%); color: #6B7380; }
        .input-group input.has-icon { padding-left: 40px; }
        
        .btn-primary { background: linear-gradient(135deg, #00C48C, #00A376); color: white; padding: 12px 24px; border-radius: 8px; font-weight: 500; border: none; cursor: pointer; transition: all 0.2s; width: 100%; }
        .btn-primary:hover { transform: translateY(-1px); box-shadow: 0 4px 12px rgba(0, 196, 140, 0.3); }
        .btn-primary:active { transform: scale(0.98); }
        
        .user-menu { position: absolute; top: 100%; right: 0; margin-top: 8px; background: #1E2228; border: 1px solid #363C49; border-radius: 12px; min-width: 200px; padding: 8px 0; display: none; box-shadow: 0 10px 40px rgba(0,0,0,0.4); }
        .user-menu.active { display: block; }
        .user-menu-item { padding: 10px 16px; cursor: pointer; transition: background 0.2s; display: flex; align-items: center; gap: 10px; }
        .user-menu-item:hover { background: #2A2E39; }
        
        .verification-code-btn { position: absolute; right: 8px; top: 50%; transform: translateY(-50%); padding: 6px 12px; background: #363C49; border: none; border-radius: 6px; color: white; font-size: 12px; cursor: pointer; transition: all 0.2s; }
        .verification-code-btn:hover:not(:disabled) { background: #00C48C; }
        .verification-code-btn:disabled { opacity: 0.5; cursor: not-allowed; }
        
        #chart-container { width: 100%; height: 400px; }
        @media (max-width: 768px) { #chart-container { height: 280px; } .desktop-only { display: none !important; } }
        @media (min-width: 769px) { .mobile-only { display: none !important; } }
    </style>
</head>
<body>
    <div id="toast-container"></div>
    
    <header class="glass fixed top-0 left-0 right-0 z-50 border-b border-gray-800">
        <div class="max-w-7xl mx-auto px-4 h-14 flex items-center justify-between">
            <div class="flex items-center space-x-8">
                <div class="flex items-center space-x-2">
                    <div class="w-8 h-8 bg-gradient-to-br from-green-400 to-green-600 rounded-lg flex items-center justify-center">
                        <span class="text-white font-bold text-sm">OK</span>
                    </div>
                    <span class="text-xl font-bold text-white">OKX Pro</span>
                </div>
                <nav class="hidden md:flex items-center space-x-6 text-sm">
                    <a href="#" class="text-white hover:text-green-400 transition">行情</a>
                    <a href="#" class="text-gray-400 hover:text-green-400 transition">交易</a>
                    <a href="#" class="text-gray-400 hover:text-green-400 transition">订单</a>
                    <a href="#" class="text-gray-400 hover:text-green-400 transition">资产</a>
                </nav>
            </div>
            <div class="flex items-center space-x-3">
                <div id="auth-buttons">
                    <button onclick="openModal('login-modal')" class="px-4 py-1.5 text-gray-300 hover:text-white transition text-sm">登录</button>
                    <button onclick="openModal('register-modal')" class="px-4 py-1.5 bg-green-500 text-white rounded-lg text-sm font-medium hover:bg-green-600 transition">注册</button>
                </div>
                <div id="user-section" class="hidden relative">
                    <button onclick="toggleUserMenu()" class="flex items-center space-x-2 hover:bg-gray-800 px-3 py-1.5 rounded-lg transition">
                        <div class="w-8 h-8 rounded-full bg-gradient-to-br from-blue-400 to-blue-600 flex items-center justify-center text-white font-medium" id="user-avatar">U</div>
                        <span class="text-sm text-white hidden md:block" id="user-name">User</span>
                        <i class="fas fa-chevron-down text-gray-400 text-xs"></i>
                    </button>
                    <div class="user-menu" id="user-menu">
                        <div class="px-4 py-2 border-b border-gray-700">
                            <div class="text-white font-medium" id="menu-username">Username</div>
                            <div class="text-xs text-gray-400" id="menu-email">user@example.com</div>
                        </div>
                        <div class="user-menu-item" onclick="openModal('profile-modal')">
                            <i class="fas fa-user text-gray-400"></i><span>个人中心</span>
                        </div>
                        <div class="user-menu-item" onclick="openModal('security-modal')">
                            <i class="fas fa-shield-alt text-gray-400"></i><span>安全设置</span>
                        </div>
                        <div class="border-t border-gray-700 my-1"></div>
                        <div class="user-menu-item text-red-400" onclick="logout()">
                            <i class="fas fa-sign-out-alt"></i><span>退出登录</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- 登录弹窗 -->
    <div class="modal" id="login-modal">
        <div class="modal-content">
            <div class="p-6">
                <div class="flex justify-between items-center mb-6">
                    <h2 class="text-xl font-bold text-white">欢迎回来</h2>
                    <button onclick="closeModal('login-modal')" class="text-gray-400 hover:text-white"><i class="fas fa-times text-xl"></i></button>
                </div>
                <form id="login-form" onsubmit="handleLogin(event)">
                    <div class="input-group">
                        <i class="fas fa-user icon"></i>
                        <input type="text" id="login-account" class="has-icon" placeholder="用户名/手机号/邮箱" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-lock icon"></i>
                        <input type="password" id="login-password" class="has-icon" placeholder="密码" required>
                    </div>
                    <div class="flex justify-between items-center mb-6 text-sm">
                        <label class="flex items-center text-gray-400 cursor-pointer">
                            <input type="checkbox" id="remember-me" class="mr-2">记住我
                        </label>
                        <a href="#" class="text-green-400 hover:text-green-300">忘记密码?</a>
                    </div>
                    <button type="submit" class="btn-primary mb-4">登录</button>
                    <div class="text-center text-sm text-gray-400">
                        还没有账号? <button type="button" onclick="switchModal('login-modal', 'register-modal')" class="text-green-400 hover:text-green-300 ml-1">立即注册</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- 注册弹窗 -->
    <div class="modal" id="register-modal">
        <div class="modal-content">
            <div class="p-6">
                <div class="flex justify-between items-center mb-6">
                    <h2 class="text-xl font-bold text-white">创建账号</h2>
                    <button onclick="closeModal('register-modal')" class="text-gray-400 hover:text-white"><i class="fas fa-times text-xl"></i></button>
                </div>
                <form id="register-form" onsubmit="handleRegister(event)">
                    <div class="input-group">
                        <i class="fas fa-user icon"></i>
                        <input type="text" id="reg-username" class="has-icon" placeholder="用户名 (3-20位)" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-envelope icon"></i>
                        <input type="email" id="reg-email" class="has-icon" placeholder="邮箱地址" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-phone icon"></i>
                        <input type="tel" id="reg-phone" class="has-icon" placeholder="手机号" required>
                    </div>
                    <div class="input-group" style="position: relative;">
                        <i class="fas fa-shield-alt icon"></i>
                        <input type="text" id="reg-code" class="has-icon" placeholder="验证码" required style="padding-right: 100px;">
                        <button type="button" class="verification-code-btn" id="send-code-btn" onclick="sendCode()">获取验证码</button>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-lock icon"></i>
                        <input type="password" id="reg-password" class="has-icon" placeholder="密码 (8-20位)" required>
                    </div>
                    <div class="input-group">
                        <i class="fas fa-lock icon"></i>
                        <input type="password" id="reg-confirm" class="has-icon" placeholder="确认密码" required>
                    </div>
                    <div class="flex items-start mb-6 text-sm">
                        <input type="checkbox" id="agree-terms" class="mt-1 mr-2" required>
                        <span class="text-gray-400">我已阅读并同意 <a href="#" class="text-green-400">服务条款</a> 和 <a href="#" class="text-green-400">隐私政策</a></span>
                    </div>
                    <button type="submit" class="btn-primary mb-4">注册</button>
                    <div class="text-center text-sm text-gray-400">
                        已有账号? <button type="button" onclick="switchModal('register-modal', 'login-modal')" class="text-green-400 hover:text-green-300 ml-1">立即登录</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <!-- 个人中心 -->
    <div class="modal" id="profile-modal">
        <div class="modal-content" style="max-width: 500px;">
            <div class="p-6">
                <div class="flex justify-between items-center mb-6">
                    <h2 class="text-xl font-bold text-white">个人中心</h2>
                    <button onclick="closeModal('profile-modal')" class="text-gray-400 hover:text-white"><i class="fas fa-times text-xl"></i></button>
                </div>
                <div class="flex items-center mb-6">
                    <div class="w-20 h-20 rounded-full bg-gradient-to-br from-blue-400 to-blue-600 flex items-center justify-center text-white text-2xl font-bold mr-4" id="profile-avatar">U</div>
                    <div>
                        <h3 class="text-lg font-bold text-white" id="profile-username">Username</h3>
                        <p class="text-gray-400 text-sm" id="profile-email">user@example.com</p>
                        <span class="inline-block mt-2 px-3 py-1 bg-green-500/20 text-green-400 rounded-full text-xs"><i class="fas fa-check-circle mr-1"></i>已实名认证</span>
                    </div>
                </div>
                <div class="bg-gray-800 rounded-lg p-4 mb-4">
                    <div class="flex justify-between items-center mb-2">
                        <span class="text-gray-400 text-sm">注册时间</span>
                        <span class="text-white text-sm" id="profile-regtime">2024-01-01</span>
                    </div>
                    <div class="flex justify-between items-center">
                        <span class="text-gray-400 text-sm">UID</span>
                        <span class="text-white text-sm font-mono" id="profile-uid">12345678</span>
                    </div>
                </div>
                <div class="bg-gray-800 rounded-lg p-4">
                    <h4 class="text-white font-medium mb-3">安全设置</h4>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center"><div class="flex items-center"><i class="fas fa-envelope text-green-400 mr-2"></i><span class="text-sm text-white">邮箱</span></div><span class="text-green-400 text-sm">已绑定</span></div>
                        <div class="flex justify-between items-center"><div class="flex items-center"><i class="fas fa-phone text-green-400 mr-2"></i><span class="text-sm text-white">手机</span></div><span class="text-green-400 text-sm">已绑定</span></div>
                        <div class="flex justify-between items-center"><div class="flex items-center"><i class="fas fa-google text-gray-400 mr-2"></i><span class="text-sm text-white">谷歌验证</span></div><button class="text-green-400 text-sm hover:text-green-300">去绑定</button></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 交易界面 -->
    <div class="bg-gray-900 border-b border-gray-800 overflow-x-auto pt-14">
        <div class="flex space-x-6 px-4 py-3 min-w-max" id="ticker-bar"></div>
    </div>

    <div class="max-w-7xl mx-auto p-4">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-4">
            <div class="lg:col-span-2 space-y-4">
                <div class="bg-gray-800 rounded-xl p-4">
                    <div class="flex items-center space-x-4">
                        <div class="w-10 h-10 rounded-full bg-gradient-to-br from-orange-400 to-orange-600 flex items-center justify-center text-xl"><i class="fab fa-bitcoin text-white"></i></div>
                        <div><div class="flex items-center space-x-2"><span class="text-xl font-bold text-white">BTC/USDT</span><span class="px-2 py-0.5 bg-green-500/20 text-green-400 rounded text-xs">现货</span></div><div class="text-sm text-gray-400">比特币 / 泰达币</div></div>
                    </div>
                </div>

                <div class="bg-gray-800 rounded-xl p-4 text-center">
                    <div class="text-4xl font-bold text-green-400 font-mono" id="main-price">58,245.32</div>
                    <div class="text-sm text-gray-400 mt-1">≈ $58,245.32 USD</div>
                </div>

                <div class="bg-gray-800 rounded-xl p-4">
                    <div id="chart-container"></div>
                </div>

                <div class="bg-gray-800 rounded-xl overflow-hidden">
                    <div class="p-4 border-b border-gray-700"><h3 class="font-medium text-white">订单簿</h3></div>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-0">
                        <div class="border-r border-gray-700">
                            <div class="grid grid-cols-3 px-4 py-2 text-xs text-gray-500 border-b border-gray-700"><span>价格</span><span class="text-right">数量</span><span class="text-right">累计</span></div>
                            <div id="asks-list" class="text-sm max-h-48 overflow-y-auto"></div>
                        </div>
                        <div>
                            <div class="grid grid-cols-3 px-4 py-2 text-xs text-gray-500 border-b border-gray-700"><span>价格</span><span class="text-right">数量</span><span class="text-right">累计</span></div>
                            <div id="bids-list" class="text-sm max-h-48 overflow-y-auto"></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="space-y-4">
                <div class="bg-gray-800 rounded-xl p-4 sticky top-16">
                    <div class="flex mb-4">
                        <button id="buy-btn" class="flex-1 py-3 rounded-l-lg bg-green-500 text-white font-medium">买入</button>
                        <button id="sell-btn" class="flex-1 py-3 rounded-r-lg bg-gray-700 text-gray-400 font-medium">卖出</button>
                    </div>
                    <div class="space-y-4 mb-4">
                        <div><label class="text-xs text-gray-500 mb-1 block">价格 (USDT)</label><input type="number" id="trade-price" class="w-full bg-gray-700 rounded-lg px-4 py-2 text-white outline-none font-mono" value="58245.32"></div>
                        <div><label class="text-xs text-gray-500 mb-1 block">数量 (BTC)</label><input type="number" id="trade-amount" class="w-full bg-gray-700 rounded-lg px-4 py-2 text-white outline-none font-mono" placeholder="0.0000"></div>
                    </div>
                    <div class="flex justify-between mt-2 mb-4">
                        <button onclick="setPct(25)" class="px-3 py-1 rounded bg-gray-700 text-xs text-gray-400">25%</button>
                        <button onclick="setPct(50)" class="px-3 py-1 rounded bg-gray-700 text-xs text-gray-400">50%</button>
                        <button onclick="setPct(75)" class="px-3 py-1 rounded bg-gray-700 text-xs text-gray-400">75%</button>
                        <button onclick="setPct(100)" class="px-3 py-1 rounded bg-gray-700 text-xs text-gray-400">100%</button>
                    </div>
                    <button onclick="placeOrder()" id="order-action-btn" class="w-full py-4 bg-green-500 text-white rounded-lg font-bold text-lg hover:bg-green-600 transition">买入 BTC</button>
                </div>

                <div class="bg-gray-800 rounded-xl p-4">
                    <h3 class="font-medium text-white mb-4">资产概览</h3>
                    <div class="text-2xl font-bold text-white mb-1" id="total-asset">10,000.00</div>
                    <div class="text-sm text-gray-400 mb-4">USDT</div>
                    <div class="space-y-2 text-sm">
                        <div class="flex justify-between py-2 border-b border-gray-700"><span class="text-gray-400">USDT</span><span class="text-white" id="usdt-bal">10,000.00</span></div>
                        <div class="flex justify-between py-2 border-b border-gray-700"><span class="text-gray-400">BTC</span><span class="text-white" id="btc-bal">0.0000</span></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
    // ==================== 用户认证系统 ====================
    const Auth = {
        hashPassword(password, salt = 'okx-pro-salt') {
            return CryptoJS.SHA256(password + salt).toString();
        },
        
        generateUID() {
            return Math.floor(10000000 + Math.random() * 90000000).toString();
        },
        
        getUsers() {
            const users = localStorage.getItem('okx_users');
            return users ? JSON.parse(users) : {};
        },
        
        saveUsers(users) {
            localStorage.setItem('okx_users', JSON.stringify(users));
        },
        
        register(userData) {
            const users = this.getUsers();
            if (users[userData.username]) return { success: false, message: '用户名已被注册' };
            for (let key in users) {
                if (users[key].email === userData.email) return { success: false, message: '邮箱已被注册' };
            }
            const newUser = {
                uid: this.generateUID(),
                username: userData.username,
                email: userData.email,
                phone: userData.phone,
                passwordHash: this.hashPassword(userData.password),
                createdAt: new Date().toISOString(),
                lastLogin: null,
                isActive: true,
                kycStatus: 'verified'
            };
            users[userData.username] = newUser;
            this.saveUsers(users);
            return { success: true, message: '注册成功', user: newUser };
        },
        
        login(account, password) {
            const users = this.getUsers();
            const passwordHash = this.hashPassword(password);
            let user = users[account];
            if (!user) {
                for (let key in users) {
                    if (users[key].email === account || users[key].phone === account) {
                        user = users[key]; break;
                    }
                }
            }
            if (!user) return { success: false, message: '账号不存在' };
            if (user.passwordHash !== passwordHash) return { success: false, message: '密码错误' };
            user.lastLogin = new Date().toISOString();
            users[user.username] = user;
            this.saveUsers(users);
            localStorage.setItem('okx_current_session', JSON.stringify({ username: user.username, loginAt: new Date().toISOString() }));
            return { success: true, message: '登录成功', user };
        },
        
        logout() {
            localStorage.removeItem('okx_current_session');
        },
        
        getCurrentUser() {
            const session = localStorage.getItem('okx_current_session');
            if (!session) return null;
            const sessionData = JSON.parse(session);
            const users = this.getUsers();
            return users[sessionData.username] || null;
        },
        
        isLoggedIn() {
            return !!this.getCurrentUser();
        }
    };

    // ==================== UI 控制 ====================
    function openModal(modalId) {
        document.querySelectorAll('.modal').forEach(m => m.classList.remove('active'));
        document.getElementById(modalId).classList.add('active');
        document.body.style.overflow = 'hidden';
    }

    function closeModal(modalId) {
        document.getElementById(modalId).classList.remove('active');
        document.body.style.overflow = '';
    }

    function switchModal(fromId, toId) {
        closeModal(fromId);
        setTimeout(() => openModal(toId), 100);
    }

    function toggleUserMenu() {
        document.getElementById('user-menu').classList.toggle('active');
    }

    document.addEventListener('click', (e) => {
        const userSection = document.getElementById('user-section');
        if (userSection && !userSection.contains(e.target)) {
            document.getElementById('user-menu')?.classList.remove('active');
        }
    });

    // ==================== 表单处理 ====================
    let codeTimer = null;
    function sendCode() {
        const btn = document.getElementById('send-code-btn');
        const phone = document.getElementById('reg-phone').value;
        if (!phone) { showToast('请先输入手机号', 'error'); return; }
        showToast('验证码已发送: 123456', 'success');
        let seconds = 60;
        btn.disabled = true;
        btn.textContent = seconds + 's';
        codeTimer = setInterval(() => {
            seconds--;
            if (seconds <= 0) { clearInterval(codeTimer); btn.disabled = false; btn.textContent = '获取验证码'; }
            else btn.textContent = seconds + 's';
        }, 1000);
    }

    function handleRegister(e) {
        e.preventDefault();
        const username = document.getElementById('reg-username').value.trim();
        const email = document.getElementById('reg-email').value.trim();
        const phone = document.getElementById('reg-phone').value.trim();
        const code = document.getElementById('reg-code').value.trim();
        const password = document.getElementById('reg-password').value;
        const confirm = document.getElementById('reg-confirm').value;
        
        if (!/^[a-zA-Z0-9_]{3,20}$/.test(username)) { showToast('用户名格式错误：3-20位字母数字下划线', 'error'); return; }
        if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) { showToast('请输入有效的邮箱地址', 'error'); return; }
        if (!/^1[3-9]\d{9}$/.test(phone)) { showToast('请输入有效的手机号', 'error'); return; }
        if (code !== '123456') { showToast('验证码错误', 'error'); return; }
        if (password.length < 8) { showToast('密码长度需在8-20位之间', 'error'); return; }
        if (password !== confirm) { showToast('两次输入的密码不一致', 'error'); return; }
        
        const result = Auth.register({ username, email, phone, password });
        if (result.success) {
            showToast('注册成功！请登录', 'success');
            switchModal('register-modal', 'login-modal');
            document.getElementById('register-form').reset();
        } else showToast(result.message, 'error');
    }

    function handleLogin(e) {
        e.preventDefault();
        const account = document.getElementById('login-account').value.trim();
        const password = document.getElementById('login-password').value;
        const result = Auth.login(account, password);
        if (result.success) {
            showToast('登录成功！', 'success');
            closeModal('login-modal');
            updateUIForLogin(result.user);
        } else showToast(result.message, 'error');
    }

    function logout() {
        Auth.logout();
        showToast('已退出登录', 'success');
        document.getElementById('auth-buttons').classList.remove('hidden');
        document.getElementById('user-section').classList.add('hidden');
        document.getElementById('user-menu').classList.remove('active');
    }

    function updateUIForLogin(user) {
        document.getElementById('auth-buttons').classList.add('hidden');
        document.getElementById('user-section').classList.remove('hidden');
        document.getElementById('user-name').textContent = user.username;
        document.getElementById('menu-username').textContent = user.username;
        document.getElementById('menu-email').textContent = user.email;
        document.getElementById('profile-username').textContent = user.username;
        document.getElementById('profile-email').textContent = user.email;
        document.getElementById('profile-uid').textContent = user.uid;
        document.getElementById('profile-regtime').textContent = new Date(user.createdAt).toLocaleDateString();
        document.getElementById('user-avatar').textContent = user.username.charAt(0).toUpperCase();
        document.getElementById('profile-avatar').textContent = user.username.charAt(0).toUpperCase();
    }

    function showToast(msg, type) {
        const toast = document.createElement('div');
        toast.className = 'toast ' + type;
        toast.innerHTML = '<i class="fas fa-' + (type === 'success' ? 'check-circle' : type === 'error' ? 'exclamation-circle' : 'info-circle') + ' mr-2"></i>' + msg;
        document.getElementById('toast-container').appendChild(toast);
        setTimeout(() => toast.classList.add('show'), 10);
        setTimeout(() => { toast.classList.remove('show'); setTimeout(() => toast.remove(), 300); }, 3000);
    }

    // ==================== 交易功能 ====================
    const state = { price: 58245.32, side: 'buy', balance: { USDT: 10000, BTC: 0 } };
    
    document.addEventListener('DOMContentLoaded', () => {
        initChart(); initOrderBook(); initTicker(); updateUI();
        setInterval(simulatePrice, 2000);
        setInterval(updateOrderBook, 1000);
        const user = Auth.getCurrentUser();
        if (user) updateUIForLogin(user);
    });

    let chart, candleSeries;
    function initChart() {
        chart = LightweightCharts.createChart(document.getElementById('chart-container'), {
            layout: { background: { color: 'transparent' }, textColor: '#9DA3B4' },
