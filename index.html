<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Smart AC Simulator - 智慧空調溫控模擬器</title>
    <style>
        :root {
            --primary: #2196F3;
            --primary-dark: #1976D2;
            --primary-light: #BBDEFB;
            --accent: #FF9800;
            --success: #4CAF50;
            --danger: #F44336;
            --bg-main: #F4F7F9;
            --card-bg: #FFFFFF;
            --text-main: #2C3E50;
            --text-sub: #7F8C8D;
            --border-radius: 16px;
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
            --shadow-hover: 0 15px 35px rgba(0, 0, 0, 0.12);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            user-select: none;
            -webkit-tap-highlight-color: transparent;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans TC", sans-serif;
            touch-action: manipulation;
        }

        html, body {
            width: 100%;
            height: 100%;
            height: 100dvh;
            overflow: hidden;
            background-color: var(--bg-main);
            color: var(--text-main);
        }

        body {
            display: flex;
            flex-direction: column;
        }

        /* App Container */
        #app-container {
            display: flex;
            flex: 1;
            width: 100%;
            max-width: 1440px;
            margin: 0 auto;
            padding: 16px;
            gap: 16px;
            height: 100dvh;
            max-height: 100dvh;
            box-sizing: border-box;
            overflow: hidden;
        }

        /* Room Column (Left) */
        .room-column {
            flex: 1.2;
            display: flex;
            flex-direction: column;
            position: relative;
            background: #EBF3F5;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            overflow: hidden;
        }

        #room-canvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .room-overlay-info {
            position: absolute;
            top: 16px;
            left: 16px;
            display: flex;
            gap: 10px;
            z-index: 10;
        }

        .badge {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(8px);
            padding: 6px 14px;
            border-radius: 20px;
            font-weight: 700;
            font-size: 13px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.06);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .badge-temp { color: #E65100; }
        .badge-comfort { color: #2E7D32; }

        /* Control Panel Column (Right) */
        .panel-column {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 12px;
            overflow-y: auto;
            padding-right: 4px;
        }

        .panel-column::-webkit-scrollbar {
            width: 4px;
        }
        .panel-column::-webkit-scrollbar-thumb {
            background: #CBD5E1;
            border-radius: 3px;
        }

        .card {
            background: var(--card-bg);
            border-radius: var(--border-radius);
            padding: 16px;
            box-shadow: var(--shadow);
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .card-title {
            font-size: 15px;
            font-weight: 700;
            color: var(--text-main);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        /* Status Dashboard */
        .grid-stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 8px;
        }

        .stat-box {
            background: #F8FAFC;
            border: 1px solid #E2E8F0;
            border-radius: 10px;
            padding: 8px;
            text-align: center;
        }

        .stat-label {
            font-size: 11px;
            color: var(--text-sub);
            margin-bottom: 2px;
        }

        .stat-value {
            font-size: 17px;
            font-weight: 800;
            color: var(--text-main);
        }

        .meter-container {
            margin-top: 10px;
        }

        .meter-header {
            display: flex;
            justify-content: space-between;
            font-size: 12px;
            margin-bottom: 4px;
            font-weight: 600;
        }

        .meter-bar {
            height: 8px;
            background: #E2E8F0;
            border-radius: 4px;
            overflow: hidden;
            position: relative;
        }

        .meter-fill {
            height: 100%;
            width: 0%;
            border-radius: 4px;
            transition: width 0.3s cubic-bezier(0.4, 0, 0.2, 1), background-color 0.3s;
        }

        /* Weather Card */
        .weather-box {
            background: linear-gradient(135deg, #E0F2FE 0%, #BAE6FD 100%);
            border: 1px solid #7DD3FC;
            border-radius: 12px;
            padding: 10px 14px;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .weather-icon {
            font-size: 32px;
            line-height: 1;
        }

        .weather-info {
            flex: 1;
        }

        .weather-title {
            font-weight: 800;
            font-size: 14px;
            color: #0369A1;
        }

        .weather-desc {
            font-size: 11px;
            color: #0284C7;
            margin-top: 1px;
        }

        /* Goal & Warning Banners */
        .goal-box {
            background: #FEF3C7;
            border: 1px solid #FDE68A;
            border-radius: 12px;
            padding: 10px 14px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .goal-text {
            font-size: 12px;
            color: #92400E;
            font-weight: 700;
        }

        .goal-timer {
            font-size: 16px;
            font-weight: 800;
            color: #D97706;
        }

        .warning-box {
            background: #FEE2E2;
            border: 2px dashed #EF4444;
            border-radius: 12px;
            padding: 10px 14px;
            display: none;
            align-items: center;
            justify-content: space-between;
            animation: pulse-border 1s infinite alternate;
        }

        .warning-box.active {
            display: flex;
        }

        @keyframes pulse-border {
            from { border-color: #EF4444; }
            to { border-color: #7F1D1D; }
        }

        /* Breakdown Card Alert */
        .breakdown-card {
            background: #FFF1F2;
            border: 2px solid #F43F5E;
            border-radius: var(--border-radius);
            padding: 12px 14px;
            display: none;
            flex-direction: column;
            gap: 8px;
            animation: bounce-in 0.3s ease;
        }

        .breakdown-card.active {
            display: flex;
        }

        @keyframes bounce-in {
            0% { transform: scale(0.9); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        /* Manual Controls */
        .controls-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 8px;
        }

        .btn {
            background: #F8FAFC;
            border: 1px solid #CBD5E1;
            padding: 10px 12px;
            border-radius: 10px;
            font-weight: 600;
            font-size: 12px;
            color: var(--text-main);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
            transition: all 0.15s;
            position: relative;
            overflow: hidden;
        }

        .btn:hover {
            background: #E2E8F0;
            border-color: #94A3B8;
        }

        .btn:active {
            transform: translateY(1px);
        }

        .btn-primary {
            background: var(--primary);
            color: white;
            border: none;
        }
        .btn-primary:hover {
            background: var(--primary-dark);
        }

        .btn-danger {
            background: #EF4444;
            color: white;
            border: none;
            font-weight: 800;
        }
        .btn-danger:hover {
            background: #DC2626;
        }

        .btn-power {
            background: #FFEBEE;
            color: var(--danger);
            border-color: #FFCDD2;
        }
        .btn-power.active {
            background: #E8F5E9;
            color: var(--success);
            border-color: #C8E6C9;
        }

        .btn-group {
            display: flex;
            gap: 6px;
            width: 100%;
        }

        .btn-group .btn {
            flex: 1;
        }

        /* Ripple Effect */
        .ripple {
            position: absolute;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.4);
            transform: scale(0);
            animation: ripple-anim 0.6s linear;
            pointer-events: none;
        }

        @keyframes ripple-anim {
            to {
                transform: scale(4);
                opacity: 0;
            }
        }

        /* Modal Styles */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: rgba(15, 23, 42, 0.6);
            backdrop-filter: blur(6px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 100;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s ease;
        }

        .modal-overlay.active {
            opacity: 1;
            pointer-events: auto;
        }

        .modal-card {
            background: white;
            border-radius: var(--border-radius);
            width: 90%;
            max-width: 500px;
            padding: 24px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
            transform: translateY(20px);
            transition: transform 0.3s ease;
            max-height: 90vh;
            overflow-y: auto;
        }

        .modal-overlay.active .modal-card {
            transform: translateY(0);
        }

        .modal-header {
            font-size: 20px;
            font-weight: 800;
            margin-bottom: 14px;
            color: var(--text-main);
            text-align: center;
        }

        .modal-body {
            font-size: 13px;
            line-height: 1.5;
            color: #475569;
            margin-bottom: 20px;
        }

        .instruction-item {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            margin-bottom: 12px;
        }

        .instruction-icon {
            width: 28px;
            height: 28px;
            border-radius: 50%;
            background: var(--primary-light);
            color: var(--primary-dark);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            flex-shrink: 0;
            font-size: 13px;
        }

        /* QTE Repair Mini Game Bar */
        .qte-container {
            margin: 16px 0;
            background: #F1F5F9;
            border-radius: 12px;
            padding: 16px;
            text-align: center;
        }

        .qte-track {
            height: 28px;
            background: #CBD5E1;
            border-radius: 14px;
            position: relative;
            overflow: hidden;
            margin: 12px 0;
            border: 2px solid #94A3B8;
        }

        .qte-target-zone {
            position: absolute;
            top: 0;
            bottom: 0;
            background: #4CAF50;
            box-shadow: 0 0 10px rgba(76, 175, 80, 0.6);
        }

        .qte-pointer {
            position: absolute;
            top: 0;
            bottom: 0;
            width: 6px;
            background: #EF4444;
            transform: translateX(-50%);
            box-shadow: 0 0 8px #EF4444;
        }

        /* Start Cover Screen */
        #cover-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: linear-gradient(135deg, #E0F2FE 0%, #BAE6FD 100%);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 90;
            padding: 20px;
            text-align: center;
        }

        .logo-title {
            font-size: 32px;
            font-weight: 900;
            color: #0369A1;
            margin-bottom: 6px;
            letter-spacing: -0.5px;
        }

        .logo-subtitle {
            font-size: 14px;
            color: #0284C7;
            margin-bottom: 24px;
            font-weight: 500;
        }

        .cover-hero-box {
            width: 100%;
            max-width: 440px;
            height: 180px;
            background: white;
            border-radius: 20px;
            margin-bottom: 24px;
            box-shadow: var(--shadow-hover);
            position: relative;
            overflow: hidden;
        }

        .cover-btns {
            display: flex;
            flex-direction: column;
            gap: 10px;
            width: 100%;
            max-width: 280px;
        }

        .btn-large {
            padding: 14px 20px;
            font-size: 15px;
            border-radius: 12px;
            font-weight: 700;
            box-shadow: 0 4px 14px rgba(33, 150, 243, 0.3);
        }

        /* Responsive Adjustments for Mobile View - Strict Single Screen Height */
        @media (max-width: 900px) {
            #app-container {
                flex-direction: column;
                height: 100dvh;
                max-height: 100dvh;
                padding: 8px;
                gap: 6px;
                overflow: hidden;
            }

            .room-column {
                height: 25vh;
                min-height: 150px;
                flex: none;
                border-radius: 12px;
            }

            .room-overlay-info {
                top: 8px;
                left: 8px;
                gap: 6px;
            }

            .badge {
                padding: 4px 10px;
                font-size: 11px;
                border-radius: 12px;
            }

            .panel-column {
                flex: 1;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                overflow-y: hidden;
                gap: 6px;
                padding-right: 0;
            }

            .card {
                padding: 8px 10px;
                border-radius: 10px;
            }

            .card-title {
                font-size: 13px;
                margin-bottom: 6px;
            }

            .weather-box {
                padding: 6px 10px;
                gap: 8px;
                border-radius: 10px;
            }

            .weather-icon {
                font-size: 24px;
            }

            .weather-title {
                font-size: 13px;
            }

            .weather-desc {
                font-size: 10px;
                margin-top: 0;
            }

            #ui-weather-req-mode {
                font-size: 10px !important;
                margin-top: 1px !important;
            }

            .goal-box {
                padding: 6px 10px;
                border-radius: 10px;
            }

            .goal-text {
                font-size: 11px;
            }

            .goal-timer {
                font-size: 15px;
            }

            .stat-box {
                padding: 4px 6px;
                border-radius: 8px;
            }

            .stat-label {
                font-size: 10px;
                margin-bottom: 1px;
            }

            .stat-value {
                font-size: 14px;
            }

            .grid-stats {
                gap: 4px;
            }

            .meter-container {
                margin-top: 6px;
            }

            .meter-header {
                font-size: 10px;
                margin-bottom: 2px;
            }

            .meter-bar {
                height: 6px;
            }

            .controls-grid {
                gap: 5px;
            }

            .btn {
                padding: 8px 4px;
                font-size: 11px;
                border-radius: 8px;
            }

            .warning-box {
                padding: 6px 10px;
            }

            .breakdown-card {
                padding: 6px 10px;
                gap: 4px;
            }

            .logo-title {
                font-size: 24px;
            }
            
            .logo-subtitle {
                font-size: 13px;
                margin-bottom: 16px;
            }

            .cover-hero-box {
                height: 140px;
                margin-bottom: 16px;
            }
        }
    </style>
</head>
<body>

    <!-- Cover Screen -->
    <div id="cover-screen">
        <div style="margin-bottom: 12px;">
            <svg width="56" height="56" viewBox="0 0 24 24" fill="none" stroke="#0284C7" stroke-width="2">
                <path d="M12 2v20M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"/>
                <circle cx="12" cy="12" r="9"/>
            </svg>
        </div>
        <h1 class="logo-title">Smart AC Simulator</h1>
        <p class="logo-subtitle">智慧空調溫控模擬器 (7秒緩衝保護版)</p>

        <div class="cover-hero-box">
            <canvas id="cover-canvas" width="440" height="180"></canvas>
        </div>

        <div class="cover-btns">
            <button class="btn btn-primary btn-large" id="btn-start-game">開始挑戰</button>
            <button class="btn btn-large" id="btn-show-instructions">遊戲規則說明</button>
        </div>
    </div>

    <!-- Instructions Modal -->
    <div class="modal-overlay" id="instructions-modal">
        <div class="modal-card">
            <div class="modal-header">遊戲規則與操作指南</div>
            <div class="modal-body">
                <div class="instruction-item">
                    <div class="instruction-icon">🛡️</div>
                    <div><strong>7秒緩衝機制：</strong> 當舒適度降至 <strong>50% 以下</strong> 時，系統會啟動 <strong>7 秒緩衝保護期</strong>。緩衝期間勝利秒數不受扣減，超過 7 秒後將開始加速倒扣！</div>
                </div>
                <div class="instruction-item">
                    <div class="instruction-icon">🌤️</div>
                    <div><strong>天氣與模式匹配：</strong> 天氣每 <strong>18 秒</strong> 切換。<strong>強烈寒流需開【暖氣】、炎熱酷暑需開【冷氣】、夏日陣雨需開【除濕】、怡人微風需開【送風】</strong>。</div>
                </div>
                <div class="instruction-item">
                    <div class="instruction-icon">🎛️</div>
                    <div><strong>實體面板控制：</strong> 透過手動面板開關冷氣、微調設定溫度、模式與風量，將室內溫度調至目標溫度。</div>
                </div>
                <div class="instruction-item">
                    <div class="instruction-icon">⚠️</div>
                    <div><strong>突發故障與 QTE 維修：</strong> 每 13 秒觸發一次！包含機件故障、微型濾網灰塵與高壓水槍沖洗。</div>
                </div>
                <div class="instruction-item">
                    <div class="instruction-icon">⏱️</div>
                    <div><strong>顧客滿意度警示：</strong> 若體感舒適度低於 <strong>50%</strong> 超過 <strong>50 秒</strong>，顧客將會不滿離去（遊戲失敗）！</div>
                </div>
                <div class="instruction-item">
                    <div class="instruction-icon">🏆</div>
                    <div><strong>獲勝條件：</strong> 保持顧客體感舒適度在 <strong>60% 以上</strong> 持續 <strong>25 秒</strong> 即可獲得勝利！</div>
                </div>
            </div>
            <button class="btn btn-primary" style="width: 100%; padding: 12px;" id="btn-close-instructions">我知道了，開始體驗</button>
        </div>
    </div>

    <!-- Victory Modal -->
    <div class="modal-overlay" id="victory-modal">
        <div class="modal-card" style="text-align: center;">
            <div style="font-size: 50px; margin-bottom: 10px;">🎉</div>
            <div class="modal-header" style="color: var(--success);">Mission Complete!</div>
            <p style="font-size: 15px; color: var(--text-sub); margin-bottom: 20px;" id="txt-victory-msg">
                恭喜！你成功維持顧客舒適環境長達 25 秒！
            </p>
            <button class="btn btn-primary" style="width: 100%; padding: 12px;" id="btn-restart-game">再玩一次</button>
        </div>
    </div>

    <!-- Failure Modal -->
    <div class="modal-overlay" id="failure-modal">
        <div class="modal-card" style="text-align: center;">
            <div style="font-size: 50px; margin-bottom: 10px;">💔</div>
            <div class="modal-header" style="color: var(--danger);">Game Over!</div>
            <p style="font-size: 15px; color: var(--text-sub); margin-bottom: 20px;" id="txt-failure-msg">
                顧客體感舒適度低於 50% 超過 50 秒，不滿意離去了！
            </p>
            <button class="btn btn-primary" style="width: 100%; padding: 12px;" id="btn-retry-game">重新挑戰</button>
        </div>
    </div>

    <!-- Timing QTE Repair Modal -->
    <div class="modal-overlay" id="qte-modal">
        <div class="modal-card" style="text-align: center;">
            <div style="font-size: 40px; margin-bottom: 6px;">🔧</div>
            <div class="modal-header" style="color: #0369A1;">緊急機件維修</div>
            <p style="font-size: 13px; color: #475569;" id="ui-qte-hint">
                當紅色指標進入「綠色區域」時，點擊【立即修復】按鈕或按下【空白鍵 Space】！
            </p>

            <div class="qte-container">
                <div style="display: flex; justify-content: space-between; font-size: 14px; font-weight: 700; color: #1E293B;">
                    <span id="ui-qte-stage">修復進度：0 / 3</span>
                    <span id="ui-qte-fails" style="color: #EF4444;">失敗次數：0 / 3</span>
                </div>
                <div class="qte-track">
                    <div class="qte-target-zone" id="ui-qte-target" style="left: 40%; width: 20%;"></div>
                    <div class="qte-pointer" id="ui-qte-pointer" style="left: 0%;"></div>
                </div>
            </div>

            <button class="btn btn-danger btn-large" style="width: 100%;" id="btn-qte-action">立即修復 (Space)</button>
        </div>
    </div>

    <!-- Filter Cleaning QTE Modal -->
    <div class="modal-overlay" id="filter-qte-modal">
        <div class="modal-card" style="text-align: center;">
            <div style="font-size: 40px; margin-bottom: 6px;">🧹</div>
            <div class="modal-header" style="color: #0369A1;">清理濾網細微灰塵</div>
            <p style="font-size: 13px; color: #475569;">
                請在 <strong>10 秒內</strong> 使用滑鼠點擊清除濾網上的所有微小灰塵塊！
            </p>
            <div style="display: flex; justify-content: space-between; font-weight: bold; margin: 12px 0; color: #1E293B; font-size: 14px;">
                <span id="ui-filter-timer" style="color: #DC2626;">⏱️ 剩餘時間: 10.0s</span>
                <span id="ui-filter-count" style="color: #0284C7;">🧹 剩餘灰塵: 10 / 10</span>
            </div>
            <div style="position: relative; width: 100%; height: 200px; background: #334155; border-radius: 12px; overflow: hidden; border: 3px solid #64748B;">
                <canvas id="filter-canvas" width="440" height="200" style="width: 100%; height: 100%; display: block; cursor: pointer;"></canvas>
            </div>
        </div>
    </div>

    <!-- Water Washing QTE Modal -->
    <div class="modal-overlay" id="water-qte-modal">
        <div class="modal-card" style="text-align: center;">
            <div style="font-size: 40px; margin-bottom: 6px;">💧</div>
            <div class="modal-header" style="color: #0369A1;">高壓水槍沖洗濾網</div>
            <p style="font-size: 13px; color: #475569;">
                <strong>按住</strong>按鈕或【空白鍵】水流加壓，<strong>放開</strong>減壓，將水流維持在<span style="color: #4CAF50; font-weight: bold;">綠色最佳區間</span>以完成沖洗！
            </p>
            <div style="display: flex; justify-content: space-between; font-weight: bold; margin: 12px 0; color: #1E293B; font-size: 14px;">
                <span id="ui-water-timer" style="color: #DC2626;">⏱️ 剩餘時間: 12.0s</span>
                <span id="ui-water-progress" style="color: #0284C7;">💧 清潔進度: 0%</span>
            </div>
            <div style="position: relative; width: 100%; height: 220px; background: #0F172A; border-radius: 12px; overflow: hidden; border: 3px solid #64748B;">
                <canvas id="water-canvas" width="440" height="220" style="width: 100%; height: 100%; display: block;"></canvas>
            </div>
            <button class="btn btn-primary btn-large" style="width: 100%; margin-top: 12px;" id="btn-water-action">按住持續噴水 (Press & Hold)</button>
        </div>
    </div>

    <!-- Main Game UI -->
    <div id="app-container">
        
        <!-- Left Column: Living Room Canvas -->
        <div class="room-column">
            <div class="room-overlay-info">
                <div class="badge badge-temp">
                    <span>室內:</span> <span id="ui-overlay-temp">28.0°C</span>
                </div>
                <div class="badge badge-comfort">
                    <span>體感舒適度:</span> <span id="ui-overlay-comfort">60%</span>
                </div>
            </div>
            <canvas id="room-canvas"></canvas>
        </div>

        <!-- Right Column: AC Control Dashboard -->
        <div class="panel-column">
            
            <!-- Weather Card -->
            <div class="weather-box">
                <div class="weather-icon" id="ui-weather-icon">☀️</div>
                <div class="weather-info">
                    <div class="weather-title" id="ui-weather-title">天氣預報：酷暑炎熱</div>
                    <div class="weather-desc" id="ui-weather-desc">外頭陽光酷熱曝曬，目標舒適溫度為 22.0°C</div>
                    <div id="ui-weather-req-mode" style="margin-top: 2px; font-size: 11px; font-weight: 800; color: #0284C7;">💡 搭配模式：冷氣</div>
                </div>
            </div>

            <!-- Goal Banner -->
            <div class="goal-box">
                <div>
                    <div class="goal-text">🏆 勝利目標：維持舒適度 ≥ 60%</div>
                    <div style="font-size: 10px; color: #B45309;">目標最佳溫度：<span id="ui-ideal-target-text">22.0°C</span></div>
                </div>
                <div class="goal-timer" id="ui-goal-timer">0 / 25s</div>
            </div>

            <!-- Low Comfort Danger Countdown Banner -->
            <div class="warning-box" id="ui-warning-box">
                <div style="display: flex; flex-direction: column;">
                    <span style="font-size: 12px; font-weight: 800; color: #991B1B;">⚠️ 警告：顧客滿意度過低 (&lt;50%)</span>
                    <span style="font-size: 10px; color: #B91C1C;" id="ui-warning-reason">請儘速調整溫度與模式，否則顧客即將離開！</span>
                </div>
                <div style="font-size: 18px; font-weight: 900; color: #DC2626;" id="ui-low-comfort-timer">50.0s</div>
            </div>

            <!-- AC Breakdown Alert Banner -->
            <div class="breakdown-card" id="ui-breakdown-card">
                <div style="display: flex; align-items: center; justify-content: space-between;">
                    <span style="font-size: 13px; font-weight: 800; color: #9F1239;" id="ui-breakdown-title">🚨 警告：冷氣機突發故障！</span>
                    <span style="font-size: 11px; font-weight: 700; color: #E11D48;" id="ui-efficiency-val">效能: 50%</span>
                </div>
                <div style="font-size: 11px; color: #881337;" id="ui-breakdown-desc">冷氣效能衰減中，請立即手動維修！</div>
                <button class="btn btn-danger" id="btn-trigger-qte" style="padding: 8px;">🔧 啟動緊急維修 (QTE)</button>
            </div>

            <!-- Dashboard Stats Card -->
            <div class="card">
                <div class="card-title">
                    <span>環境與空調狀態</span>
                    <span id="ui-power-status" style="font-size: 11px; padding: 2px 8px; border-radius: 10px; background: #FFEBEE; color: #D32F2F;">關機中</span>
                </div>

                <div class="grid-stats">
                    <div class="stat-box">
                        <div class="stat-label">室內溫度</div>
                        <div class="stat-value" id="ui-indoor-temp">28.0°C</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-label">設定溫度</div>
                        <div class="stat-value" id="ui-target-temp">24°C</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-label">室外溫度</div>
                        <div class="stat-value" id="ui-outdoor-temp">35.0°C</div>
                    </div>
                </div>

                <div class="grid-stats" style="margin-top: 6px;">
                    <div class="stat-box">
                        <div class="stat-label">運轉模式</div>
                        <div class="stat-value" id="ui-mode" style="font-size: 14px;">冷氣</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-label">目前風量</div>
                        <div class="stat-value" id="ui-fan" style="font-size: 14px;">三段</div>
                    </div>
                    <div class="stat-box">
                        <div class="stat-label">擺風狀態</div>
                        <div class="stat-value" id="ui-swing" style="font-size: 14px;">關閉</div>
                    </div>
                </div>

                <!-- Power Bar -->
                <div class="meter-container">
                    <div class="meter-header">
                        <span>即時耗電量</span>
                        <span id="ui-power-val">0 W</span>
                    </div>
                    <div class="meter-bar">
                        <div class="meter-fill" id="ui-power-bar" style="background: #4CAF50;"></div>
                    </div>
                </div>

                <!-- Comfort Bar -->
                <div class="meter-container">
                    <div class="meter-header">
                        <span>體感舒適度</span>
                        <span id="ui-comfort-val">60%</span>
                    </div>
                    <div class="meter-bar">
                        <div class="meter-fill" id="ui-comfort-bar" style="background: #FF9800; width: 60%;"></div>
                    </div>
                </div>
            </div>

            <!-- Manual Controls Panel -->
            <div class="card">
                <div class="card-title">實體控制面板</div>
                
                <div class="controls-grid">
                    <button class="btn btn-power" id="btn-power-toggle">
                        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M18.36 6.64a9 9 0 1 1-12.73 0M12 2v10"/>
                        </svg>
                        <span id="txt-power-btn">開啟空調</span>
                    </button>

                    <div class="btn-group">
                        <button class="btn" id="btn-temp-down">
                            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M5 12h14"/></svg>
                            降溫
                        </button>
                        <button class="btn" id="btn-temp-up">
                            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 5v14M5 12h14"/></svg>
                            升溫
                        </button>
                    </div>

                    <div class="btn-group">
                        <button class="btn" id="btn-mode-prev">◀ 模式</button>
                        <button class="btn" id="btn-mode-next">模式 ▶</button>
                    </div>

                    <div class="btn-group">
                        <button class="btn" id="btn-fan-prev">◀ 風量</button>
                        <button class="btn" id="btn-fan-next">風量 ▶</button>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <script>
        /**
         * Smart AC Simulator Engine (Optimized for Mobile Performance)
         */

        const WEATHERS = [
            { id: 'sun', name: '酷暑炎熱', icon: '☀️', outdoorTemp: 36.0, targetIdealTemp: 22.0, requiredMode: 'cool', requiredModeName: '冷氣', desc: '外頭陽光酷熱曝曬，目標舒適溫度為 22.0°C' },
            { id: 'rain', name: '夏日陣雨', icon: '🌦️', outdoorTemp: 31.0, targetIdealTemp: 24.0, requiredMode: 'dry', requiredModeName: '除濕', desc: '室外濕熱潮濕，目標舒適溫度為 24.0°C' },
            { id: 'autumn', name: '秋高氣爽', icon: '🌤️', outdoorTemp: 27.0, targetIdealTemp: 25.0, requiredMode: 'cool', requiredModeName: '冷氣', desc: '天氣舒適宜人，目標舒適溫度為 25.0°C' },
            { id: 'cold', name: '強烈寒流', icon: '❄️', outdoorTemp: 11.0, targetIdealTemp: 26.0, requiredMode: 'heat', requiredModeName: '暖氣', desc: '室外寒風刺骨，目標舒適溫度為 26.0°C' },
            { id: 'heatwave', name: '極致悶熱', icon: '🔥', outdoorTemp: 38.5, targetIdealTemp: 20.0, requiredMode: 'cool', requiredModeName: '冷氣', desc: '氣溫創新高，目標舒適溫度為 20.0°C' },
            { id: 'plum_rain', name: '梅雨時節', icon: '🌧️', outdoorTemp: 24.0, targetIdealTemp: 24.0, requiredMode: 'dry', requiredModeName: '除濕', desc: '梅雨季雨水綿綿、極度潮濕，目標舒適溫度為 24.0°C' },
            { id: 'typhoon', name: '颱風襲來', icon: '🌀', outdoorTemp: 28.0, targetIdealTemp: 23.5, requiredMode: 'dry', requiredModeName: '除濕', desc: '狂風暴雨帶來濃重濕氣，目標舒適溫度為 23.5°C' },
            { id: 'blizzard', name: '霸王級寒流', icon: '☃️', outdoorTemp: 5.0, targetIdealTemp: 27.0, requiredMode: 'heat', requiredModeName: '暖氣', desc: '極端冰凍低溫來襲，目標舒適溫度為 27.0°C' },
            { id: 'breeze', name: '柔風宜人', icon: '🍃', outdoorTemp: 25.0, targetIdealTemp: 25.0, requiredMode: 'fan', requiredModeName: '送風', desc: '室外氣溫適中僅需循環空氣，目標舒適溫度為 25.0°C' },
            { id: 'foehn', name: '乾熱焚風', icon: '🏜️', outdoorTemp: 40.0, targetIdealTemp: 21.0, requiredMode: 'cool', requiredModeName: '冷氣', desc: '山風下沉帶來強烈乾熱氣流，目標舒適溫度為 21.0°C' },
            { id: 'fog', name: '回南天潮濕', icon: '🌫️', outdoorTemp: 26.0, targetIdealTemp: 24.0, requiredMode: 'dry', requiredModeName: '除濕', desc: '空氣濕度達飽和、牆面吐水，目標舒適溫度為 24.0°C' },
            { id: 'cool_night', name: '晚風微涼', icon: '🌙', outdoorTemp: 17.5, targetIdealTemp: 25.0, requiredMode: 'heat', requiredModeName: '暖氣', desc: '入夜氣溫快速轉涼，目標舒適溫度為 25.0°C' },
            { id: 'auto_pleasant', name: '智慧怡人', icon: '☘️', outdoorTemp: 26.5, targetIdealTemp: 24.5, requiredMode: 'auto', requiredModeName: '自動', desc: '天氣舒適宜人，建議開啟智慧自動模式維持 24.5°C' }
        ];

        class SoundFX {
            constructor() {
                this.ctx = null;
                this.windGain = null;
                this.windFilter = null;
            }

            init() {
                if (!this.ctx) {
                    const AudioContext = window.AudioContext || window.webkitAudioContext;
                    this.ctx = new AudioContext();
                    this.setupWindNoise();
                }
                if (this.ctx.state === 'suspended') {
                    this.ctx.resume();
                }
            }

            playBeep(freq = 880, type = 'sine', duration = 0.1) {
                if (!this.ctx) return;
                const osc = this.ctx.createOscillator();
                const gain = this.ctx.createGain();
                osc.type = type;
                osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
                gain.gain.setValueAtTime(0.15, this.ctx.currentTime);
                gain.gain.exponentialRampToValueAtTime(0.001, this.ctx.currentTime + duration);
                osc.connect(gain);
                gain.connect(this.ctx.destination);
                osc.start();
                osc.stop(this.ctx.currentTime + duration);
            }

            playChime(success = true) {
                if (!this.ctx) return;
                const now = this.ctx.currentTime;
                if (success) {
                    [523.25, 659.25, 783.99, 1046.50].forEach((f, i) => {
                        const osc = this.ctx.createOscillator();
                        const gain = this.ctx.createGain();
                        osc.frequency.setValueAtTime(f, now + i * 0.08);
                        gain.gain.setValueAtTime(0.1, now + i * 0.08);
                        gain.gain.exponentialRampToValueAtTime(0.001, now + i * 0.08 + 0.2);
                        osc.connect(gain);
                        gain.connect(this.ctx.destination);
                        osc.start(now + i * 0.08);
                        osc.stop(now + i * 0.08 + 0.2);
                    });
                } else {
                    [300, 200].forEach((f, i) => {
                        const osc = this.ctx.createOscillator();
                        const gain = this.ctx.createGain();
                        osc.type = 'sawtooth';
                        osc.frequency.setValueAtTime(f, now + i * 0.12);
                        gain.gain.setValueAtTime(0.12, now + i * 0.12);
                        gain.gain.exponentialRampToValueAtTime(0.001, now + i * 0.12 + 0.18);
                        osc.connect(gain);
                        gain.connect(this.ctx.destination);
                        osc.start(now + i * 0.12);
                        osc.stop(now + i * 0.12 + 0.18);
                    });
                }
            }

            setupWindNoise() {
                const bufferSize = this.ctx.sampleRate * 2;
                const buffer = this.ctx.createBuffer(1, bufferSize, this.ctx.sampleRate);
                const output = buffer.getChannelData(0);
                for (let i = 0; i < bufferSize; i++) {
                    output[i] = Math.random() * 2 - 1;
                }

                const whiteNoise = this.ctx.createBufferSource();
                whiteNoise.buffer = buffer;
                whiteNoise.loop = true;

                this.windFilter = this.ctx.createBiquadFilter();
                this.windFilter.type = 'lowpass';
                this.windFilter.frequency.setValueAtTime(400, this.ctx.currentTime);

                this.windGain = this.ctx.createGain();
                this.windGain.gain.setValueAtTime(0, this.ctx.currentTime);

                whiteNoise.connect(this.windFilter);
                this.windFilter.connect(this.windGain);
                this.windGain.connect(this.ctx.destination);
                whiteNoise.start();
            }

            updateWindSound(powerOn, fanLevel) {
                if (!this.ctx || !this.windGain) return;
                const now = this.ctx.currentTime;
                if (powerOn) {
                    const targetGain = 0.02 + fanLevel * 0.02;
                    const targetFreq = 300 + fanLevel * 200;
                    this.windGain.gain.setTargetAtTime(targetGain, now, 0.3);
                    this.windFilter.frequency.setTargetAtTime(targetFreq, now, 0.3);
                } else {
                    this.windGain.gain.setTargetAtTime(0, now, 0.3);
                }
            }
        }

        const soundFX = new SoundFX();

        // Game State
        const gameState = {
            powerOn: false,
            indoorTemp: 28.0,
            targetTemp: 24,
            targetIdealTemp: 22.0,
            outdoorTemp: 35.0,
            weather: WEATHERS[0],
            weatherTimer: 0,
            humidity: 65,
            mode: 'cool',
            fanSpeed: 3,
            swing: false,
            powerUsage: 0,
            comfortScore: 60,
            holdTimer: 0,
            lowComfortTimer: 0,
            bufferPeriod: 7.0,      // 7秒緩衝期設定
            isGameWon: false,
            isGameOver: false,
            
            isBroken: false,
            breakdownType: 'timing',
            coolingEfficiency: 1.0,
            breakdownCheckTimer: 0,
            _brokenPowerNoise: 0.75,
            
            qte: {
                active: false,
                stage: 1,
                maxStages: 3,
                failCount: 0,
                pointerPos: 0,
                dir: 1,
                speed: 1.8,
                targetMin: 40,
                targetMax: 60
            },

            filterQTE: {
                active: false,
                timeLeft: 10.0,
                dustList: [],
                totalDust: 10
            },

            waterQTE: {
                active: false,
                timeLeft: 12.0,
                progress: 0,
                pressure: 0,
                targetMin: 40,
                targetMax: 70,
                isHolding: false,
                streamParticles: [],
                dripParticles: []
            },

            modesList: ['cool', 'heat', 'fan', 'dry', 'auto'],
            modeNames: { cool: '冷氣', heat: '暖氣', fan: '送風', dry: '除濕', auto: '自動' }
        };

        function setRandomWeather() {
            let nextWeather;
            do {
                nextWeather = WEATHERS[Math.floor(Math.random() * WEATHERS.length)];
            } while (WEATHERS.length > 1 && gameState.weather && nextWeather.id === gameState.weather.id);

            gameState.weather = nextWeather;
            gameState.outdoorTemp = nextWeather.outdoorTemp;
            gameState.targetIdealTemp = nextWeather.targetIdealTemp;

            document.getElementById('ui-weather-icon').innerText = nextWeather.icon;
            document.getElementById('ui-weather-title').innerText = `天氣預報：${nextWeather.name}`;
            document.getElementById('ui-weather-desc').innerText = nextWeather.desc;
            document.getElementById('ui-weather-req-mode').innerText = `💡 搭配模式：${nextWeather.requiredModeName}`;
            document.getElementById('ui-ideal-target-text').innerText = `${nextWeather.targetIdealTemp.toFixed(1)}°C`;
        }

        function triggerBreakdown() {
            if (gameState.isBroken || !gameState.powerOn) return;
            gameState.isBroken = true;
            gameState.coolingEfficiency = 0.5;
            
            const rand = Math.random();
            if (rand < 0.35) {
                gameState.breakdownType = 'timing';
            } else if (rand < 0.70) {
                gameState.breakdownType = 'filter';
            } else {
                gameState.breakdownType = 'wash';
            }

            soundFX.playChime(false);

            const card = document.getElementById('ui-breakdown-card');
            const titleEl = document.getElementById('ui-breakdown-title');
            const descEl = document.getElementById('ui-breakdown-desc');

            if (gameState.breakdownType === 'filter') {
                titleEl.innerText = '🚨 警告：濾網灰塵嚴重阻塞！';
                descEl.innerText = '濾網積灰導致運轉效能衰減，請點擊清除微小灰塵！';
            } else if (gameState.breakdownType === 'wash') {
                titleEl.innerText = '🚨 警告：濾網泥垢積聚嚴重！';
                descEl.innerText = '濾網沾滿頑固污垢，請使用高壓水槍進行沖洗！';
            } else {
                titleEl.innerText = '🚨 警告：冷氣機突發機件故障！';
                descEl.innerText = '機件過熱異常，請立即手動緊急維修！';
            }
            card.classList.add('active');
        }

        function openRepairModal() {
            if (gameState.breakdownType === 'filter') {
                openFilterQTEModal();
            } else if (gameState.breakdownType === 'wash') {
                openWaterQTEModal();
            } else {
                openTimingQTEModal();
            }
        }

        function openTimingQTEModal() {
            soundFX.init();
            soundFX.playBeep();
            gameState.qte.active = true;
            gameState.qte.stage = 1;
            gameState.qte.failCount = 0;
            updateQTEFailUI();
            resetQTETarget();
            document.getElementById('qte-modal').classList.add('active');
        }

        function updateQTEFailUI() {
            document.getElementById('ui-qte-fails').innerText = `失敗次數：${gameState.qte.failCount} / 3`;
        }

        function resetQTETarget() {
            const width = 20 - (gameState.qte.stage - 1) * 3;
            const min = 15 + Math.random() * (70 - width);
            gameState.qte.targetMin = min;
            gameState.qte.targetMax = min + width;
            gameState.qte.speed = 1.5 + gameState.qte.stage * 0.6;

            const targetEl = document.getElementById('ui-qte-target');
            targetEl.style.left = `${min}%`;
            targetEl.style.width = `${width}%`;
            document.getElementById('ui-qte-stage').innerText = `修復進度：${gameState.qte.stage - 1} / ${gameState.qte.maxStages}`;
        }

        function handleQTEClick() {
            if (!gameState.qte.active) return;
            soundFX.init();
            const pos = gameState.qte.pointerPos;
            
            if (pos >= gameState.qte.targetMin && pos <= gameState.qte.targetMax) {
                soundFX.playBeep(1200, 'sine', 0.15);
                gameState.qte.stage++;
                if (gameState.qte.stage > gameState.qte.maxStages) {
                    gameState.qte.active = false;
                    gameState.isBroken = false;
                    gameState.coolingEfficiency = 1.0;
                    soundFX.playChime(true);
                    document.getElementById('qte-modal').classList.remove('active');
                    document.getElementById('ui-breakdown-card').classList.remove('active');
                } else {
                    resetQTETarget();
                }
            } else {
                gameState.qte.failCount++;
                soundFX.playBeep(250, 'sawtooth', 0.2);
                updateQTEFailUI();

                if (gameState.qte.failCount >= 3) {
                    gameState.qte.active = false;
                    triggerGameOver("維修失敗！QTE 維修連續偏離目標區域達 3 次！");
                }
            }
        }

        function updateQTELoop() {
            if (!gameState.qte.active) return;
            gameState.qte.pointerPos += gameState.qte.dir * gameState.qte.speed;
            if (gameState.qte.pointerPos >= 100) {
                gameState.qte.pointerPos = 100;
                gameState.qte.dir = -1;
            } else if (gameState.qte.pointerPos <= 0) {
                gameState.qte.pointerPos = 0;
                gameState.qte.dir = 1;
            }
            document.getElementById('ui-qte-pointer').style.left = `${gameState.qte.pointerPos}%`;
        }

        function openFilterQTEModal() {
            soundFX.init();
            soundFX.playBeep();
            gameState.filterQTE.active = true;
            gameState.filterQTE.timeLeft = 10.0;
            
            const canvas = document.getElementById('filter-canvas');
            const fw = canvas.width;
            const fh = canvas.height;
            
            gameState.filterQTE.dustList = [];
            const numDust = 10;
            gameState.filterQTE.totalDust = numDust;

            for (let i = 0; i < numDust; i++) {
                gameState.filterQTE.dustList.push({
                    x: 50 + Math.random() * (fw - 100),
                    y: 40 + Math.random() * (fh - 80),
                    r: 11 + Math.random() * 4,
                    cleaned: false
                });
            }

            updateFilterQTEUI();
            document.getElementById('filter-qte-modal').classList.add('active');
            drawFilterQTE();
        }

        function updateFilterQTELoop() {
            if (!gameState.filterQTE.active) return;

            gameState.filterQTE.timeLeft -= 0.016;
            if (gameState.filterQTE.timeLeft <= 0) {
                gameState.filterQTE.timeLeft = 0;
                gameState.filterQTE.active = false;
                triggerGameOver("維修失敗！未能在 10 秒內清理完濾網上的灰塵！");
                return;
            }

            updateFilterQTEUI();
            drawFilterQTE();
        }

        function updateFilterQTEUI() {
            const remaining = gameState.filterQTE.dustList.filter(d => !d.cleaned).length;
            document.getElementById('ui-filter-timer').innerText = `⏱️ 剩餘時間: ${gameState.filterQTE.timeLeft.toFixed(1)}s`;
            document.getElementById('ui-filter-count').innerText = `🧹 剩餘灰塵: ${remaining} / ${gameState.filterQTE.totalDust}`;
        }

        function drawFilterQTE() {
            const canvas = document.getElementById('filter-canvas');
            if (!canvas) return;
            const ctx = canvas.getContext('2d');
            const w = canvas.width;
            const h = canvas.height;

            ctx.clearRect(0, 0, w, h);

            ctx.fillStyle = '#1E293B';
            ctx.fillRect(0, 0, w, h);

            ctx.strokeStyle = '#334155';
            ctx.lineWidth = 1.5;
            for (let x = 0; x < w; x += 14) {
                ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, h); ctx.stroke();
            }
            for (let y = 0; y < h; y += 14) {
                ctx.beginPath(); ctx.moveTo(0, y); ctx.lineTo(w, y); ctx.stroke();
            }

            ctx.strokeStyle = '#64748B';
            ctx.lineWidth = 8;
            ctx.strokeRect(0, 0, w, h);

            gameState.filterQTE.dustList.forEach(d => {
                if (!d.cleaned) {
                    ctx.fillStyle = '#78716C';
                    ctx.beginPath();
                    ctx.arc(d.x, d.y, d.r, 0, Math.PI * 2);
                    ctx.fill();

                    ctx.fillStyle = '#A8A29E';
                    ctx.beginPath();
                    ctx.arc(d.x - d.r * 0.3, d.y - d.r * 0.3, d.r * 0.4, 0, Math.PI * 2);
                    ctx.fill();
                }
            });
        }

        document.getElementById('filter-canvas').addEventListener('mousedown', (e) => {
            if (!gameState.filterQTE.active) return;
            soundFX.init();

            const canvas = document.getElementById('filter-canvas');
            const rect = canvas.getBoundingClientRect();
            const scaleX = canvas.width / rect.width;
            const scaleY = canvas.height / rect.height;

            const clickX = (e.clientX - rect.left) * scaleX;
            const clickY = (e.clientY - rect.top) * scaleY;

            let hit = false;
            gameState.filterQTE.dustList.forEach(d => {
                if (!d.cleaned) {
                    const dist = Math.hypot(clickX - d.x, clickY - d.y);
                    if (dist <= d.r + 14) {
                        d.cleaned = true;
                        hit = true;
                        soundFX.playBeep(1000, 'sine', 0.1);
                    }
                }
            });

            if (hit) {
                const remaining = gameState.filterQTE.dustList.filter(d => !d.cleaned).length;
                if (remaining === 0) {
                    gameState.filterQTE.active = false;
                    gameState.isBroken = false;
                    gameState.coolingEfficiency = 1.0;
                    soundFX.playChime(true);
                    document.getElementById('filter-qte-modal').classList.remove('active');
                    document.getElementById('ui-breakdown-card').classList.remove('active');
                }
            } else {
                soundFX.playBeep(200, 'sawtooth', 0.1);
            }
        });

        function openWaterQTEModal() {
            soundFX.init();
            soundFX.playBeep();
            const wQTE = gameState.waterQTE;
            wQTE.active = true;
            wQTE.timeLeft = 12.0;
            wQTE.progress = 0;
            wQTE.pressure = 0;
            wQTE.isHolding = false;
            wQTE.streamParticles = [];
            wQTE.dripParticles = [];

            updateWaterQTEUI();
            document.getElementById('water-qte-modal').classList.add('active');
            drawWaterQTE();
        }

        function updateWaterQTELoop() {
            if (!gameState.waterQTE.active) return;

            const wQTE = gameState.waterQTE;
            wQTE.timeLeft -= 0.016;
            if (wQTE.timeLeft <= 0) {
                wQTE.timeLeft = 0;
                wQTE.active = false;
                triggerGameOver("維修失敗！未能在 12 秒內將濾網完全沖洗乾淨！");
                return;
            }

            if (wQTE.isHolding) {
                wQTE.pressure = Math.min(100, wQTE.pressure + 2.2);
            } else {
                wQTE.pressure = Math.max(0, wQTE.pressure - 2.5);
            }

            if (wQTE.pressure >= wQTE.targetMin && wQTE.pressure <= wQTE.targetMax) {
                wQTE.progress = Math.min(100, wQTE.progress + 0.35);
            }

            if (wQTE.progress >= 100) {
                wQTE.active = false;
                gameState.isBroken = false;
                gameState.coolingEfficiency = 1.0;
                soundFX.playChime(true);
                document.getElementById('water-qte-modal').classList.remove('active');
                document.getElementById('ui-breakdown-card').classList.remove('active');
            }

            updateWaterQTEUI();
            drawWaterQTE();
        }

        function updateWaterQTEUI() {
            document.getElementById('ui-water-timer').innerText = `⏱️ 剩餘時間: ${gameState.waterQTE.timeLeft.toFixed(1)}s`;
            document.getElementById('ui-water-progress').innerText = `💧 清潔進度: ${Math.floor(gameState.waterQTE.progress)}%`;
        }

        function drawWaterQTE() {
            const canvas = document.getElementById('water-canvas');
            if (!canvas) return;
            const ctx = canvas.getContext('2d');
            const w = canvas.width;
            const h = canvas.height;
            const wQTE = gameState.waterQTE;

            ctx.clearRect(0, 0, w, h);

            ctx.fillStyle = '#0F172A';
            ctx.fillRect(0, 0, w, h);

            const filterX = 120;
            const filterY = 30;
            const filterW = 200;
            const filterH = 120;

            ctx.fillStyle = '#1E293B';
            ctx.fillRect(filterX, filterY, filterW, filterH);

            ctx.strokeStyle = '#334155';
            ctx.lineWidth = 1;
            for (let x = filterX; x <= filterX + filterW; x += 10) {
                ctx.beginPath(); ctx.moveTo(x, filterY); ctx.lineTo(x, filterY + filterH); ctx.stroke();
            }
            for (let y = filterY; y <= filterY + filterH; y += 10) {
                ctx.beginPath(); ctx.moveTo(filterX, y); ctx.lineTo(filterX + filterW, y); ctx.stroke();
            }

            const dirtAlpha = Math.max(0, 1 - wQTE.progress / 100);
            if (dirtAlpha > 0) {
                ctx.fillStyle = `rgba(120, 80, 40, ${dirtAlpha * 0.85})`;
                ctx.fillRect(filterX, filterY, filterW, filterH);
            }

            ctx.strokeStyle = '#64748B';
            ctx.lineWidth = 4;
            ctx.strokeRect(filterX, filterY, filterW, filterH);

            const nozzleX = 30;
            const nozzleY = 30;
            ctx.fillStyle = '#94A3B8';
            ctx.fillRect(nozzleX - 10, nozzleY - 10, 30, 20);
            ctx.fillStyle = '#0284C7';
            ctx.fillRect(nozzleX + 20, nozzleY - 6, 12, 12);

            if (wQTE.pressure > 0) {
                const streamCount = Math.floor(wQTE.pressure / 15) + 1;
                for (let i = 0; i < streamCount; i++) {
                    wQTE.streamParticles.push({
                        x: nozzleX + 30,
                        y: nozzleY,
                        vx: 6 + Math.random() * 4 + (wQTE.pressure * 0.08),
                        vy: (Math.random() - 0.2) * 2 + (wQTE.pressure * 0.02),
                        size: 2 + Math.random() * 3,
                        life: 1.0
                    });
                }
            }

            for (let i = wQTE.streamParticles.length - 1; i >= 0; i--) {
                const p = wQTE.streamParticles[i];
                p.x += p.vx;
                p.y += p.vy;
                p.life -= 0.04;

                ctx.fillStyle = '#38BDF8';
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                ctx.fill();

                if (p.x >= filterX && p.x <= filterX + filterW && p.y >= filterY && p.y <= filterY + filterH) {
                    if (Math.random() < 0.4) {
                        wQTE.dripParticles.push({
                            x: p.x + (Math.random() - 0.5) * 10,
                            y: filterY + filterH,
                            vy: 2 + Math.random() * 3,
                            size: 2 + Math.random() * 2,
                            alpha: 0.9
                        });
                    }
                    wQTE.streamParticles.splice(i, 1);
                    continue;
                }

                if (p.life <= 0 || p.x > w || p.y > h) {
                    wQTE.streamParticles.splice(i, 1);
                }
            }

            for (let i = wQTE.dripParticles.length - 1; i >= 0; i--) {
                const dp = wQTE.dripParticles[i];
                dp.y += dp.vy;
                dp.vy += 0.2;
                dp.alpha -= 0.02;

                ctx.fillStyle = `rgba(56, 189, 248, ${Math.max(0, dp.alpha)})`;
                ctx.beginPath();
                ctx.arc(dp.x, dp.y, dp.size, 0, Math.PI * 2);
                ctx.fill();

                if (dp.alpha <= 0 || dp.y > h - 40) {
                    wQTE.dripParticles.splice(i, 1);
                }
            }

            const barX = 40;
            const barY = 175;
            const barW = 360;
            const barH = 24;

            ctx.fillStyle = '#334155';
            ctx.fillRect(barX, barY, barW, barH);

            const targetMinX = barX + (wQTE.targetMin / 100) * barW;
            const targetWidth = ((wQTE.targetMax - wQTE.targetMin) / 100) * barW;
            ctx.fillStyle = 'rgba(76, 175, 80, 0.6)';
            ctx.fillRect(targetMinX, barY, targetWidth, barH);
            ctx.strokeStyle = '#4CAF50';
            ctx.lineWidth = 2;
            ctx.strokeRect(targetMinX, barY, targetWidth, barH);

            const pressureW = (wQTE.pressure / 100) * barW;
            const inZone = wQTE.pressure >= wQTE.targetMin && wQTE.pressure <= wQTE.targetMax;
            ctx.fillStyle = inZone ? '#22C55E' : '#38BDF8';
            ctx.fillRect(barX, barY + 4, pressureW, barH - 8);

            ctx.fillStyle = '#FFFFFF';
            ctx.fillRect(barX + pressureW - 2, barY - 3, 4, barH + 6);

            ctx.fillStyle = '#94A3B8';
            ctx.font = 'bold 11px sans-serif';
            ctx.fillText('水流加壓控制 (按住/放開)', barX, barY - 6);
            ctx.fillStyle = inZone ? '#22C55E' : '#94A3B8';
            ctx.fillText(inZone ? '✨ 最佳水壓 (高效沖洗中...)' : (wQTE.pressure < wQTE.targetMin ? '⚠️ 水壓不足' : '⚠️ 水壓過高'), barX + barW - 145, barY - 6);
        }

        const btnWater = document.getElementById('btn-water-action');
        const startWater = (e) => { if (e) e.preventDefault(); gameState.waterQTE.isHolding = true; };
        const stopWater = (e) => { if (e) e.preventDefault(); gameState.waterQTE.isHolding = false; };

        btnWater.addEventListener('mousedown', startWater);
        btnWater.addEventListener('mouseup', stopWater);
        btnWater.addEventListener('mouseleave', stopWater);
        btnWater.addEventListener('touchstart', startWater, { passive: false });
        btnWater.addEventListener('touchend', stopWater, { passive: false });

        window.addEventListener('keydown', (e) => {
            if (e.code === 'Space' || e.key === ' ') {
                if (gameState.qte.active) {
                    e.preventDefault();
                    if (!e.repeat) handleQTEClick();
                } else if (gameState.waterQTE.active) {
                    e.preventDefault();
                    gameState.waterQTE.isHolding = true;
                }
            }
        });

        window.addEventListener('keyup', (e) => {
            if (e.code === 'Space' || e.key === ' ') {
                if (gameState.waterQTE.active) {
                    e.preventDefault();
                    gameState.waterQTE.isHolding = false;
                }
            }
        });

        // --- Physics & Logic Loop ---
        function updateThermalPhysics() {
            if (gameState.isGameOver || gameState.isGameWon) return;

            // 天氣每 18 秒切換
            gameState.weatherTimer += 0.016;
            if (gameState.weatherTimer >= 18.0) {
                gameState.weatherTimer = 0;
                setRandomWeather();
            }

            // 維修事件每 13 秒觸發一次
            if (gameState.powerOn && !gameState.isBroken) {
                gameState.breakdownCheckTimer += 0.016;
                if (gameState.breakdownCheckTimer >= 13.0) {
                    gameState.breakdownCheckTimer = 0;
                    triggerBreakdown();
                }
            } else {
                gameState.breakdownCheckTimer = 0;
            }

            if (gameState.isBroken) {
                gameState.coolingEfficiency = Math.max(0.1, gameState.coolingEfficiency - 0.0008);
            } else {
                gameState.coolingEfficiency = 1.0;
            }

            if (gameState.powerOn) {
                let targetEffectiveTemp = gameState.targetTemp;
                
                if (gameState.mode === 'fan') {
                    targetEffectiveTemp = gameState.outdoorTemp;
                } else if (gameState.mode === 'auto') {
                    targetEffectiveTemp = gameState.targetIdealTemp;
                }

                const speedFactor = (0.005 + (gameState.fanSpeed * 0.003)) * gameState.coolingEfficiency;
                
                if (gameState.mode === 'cool' || (gameState.mode === 'auto' && gameState.indoorTemp > gameState.targetIdealTemp)) {
                    if (gameState.indoorTemp > targetEffectiveTemp) {
                        gameState.indoorTemp -= speedFactor;
                    } else if (gameState.indoorTemp < targetEffectiveTemp) {
                        gameState.indoorTemp += 0.001;
                    }
                } else if (gameState.mode === 'heat' || (gameState.mode === 'auto' && gameState.indoorTemp < gameState.targetIdealTemp)) {
                    if (gameState.indoorTemp < targetEffectiveTemp) {
                        gameState.indoorTemp += speedFactor;
                    }
                } else if (gameState.mode === 'dry') {
                    if (gameState.indoorTemp > targetEffectiveTemp) {
                        gameState.indoorTemp -= speedFactor * 0.5;
                    } else if (gameState.indoorTemp < targetEffectiveTemp) {
                        gameState.indoorTemp += 0.001;
                    }
                    gameState.humidity = Math.max(40, gameState.humidity - 0.05);
                }

                if (gameState.isBroken) {
                    const thermalLeak = (gameState.outdoorTemp - gameState.indoorTemp) * 0.0015 * (1 - gameState.coolingEfficiency);
                    gameState.indoorTemp += thermalLeak;
                }
                
                let basePower = 300;
                if (gameState.mode === 'cool') {
                    const diff = Math.max(0, gameState.outdoorTemp - gameState.targetTemp);
                    basePower += diff * 80 + (gameState.fanSpeed * 50);
                } else if (gameState.mode === 'heat') {
                    basePower += 600 + (gameState.fanSpeed * 60);
                } else if (gameState.mode === 'fan') {
                    basePower = 20 + gameState.fanSpeed * 10;
                }

                if (gameState.isBroken) {
                    if (Math.random() < 0.1) {
                        gameState._brokenPowerNoise = 0.6 + Math.random() * 0.3;
                    }
                    gameState.powerUsage = basePower * gameState._brokenPowerNoise;
                } else {
                    gameState.powerUsage = basePower;
                }
            } else {
                const driftRate = 0.002;
                if (gameState.indoorTemp < gameState.outdoorTemp) {
                    gameState.indoorTemp += driftRate;
                } else {
                    gameState.indoorTemp -= driftRate;
                }
                gameState.powerUsage = 0;
            }

            const tempDiff = Math.abs(gameState.indoorTemp - gameState.targetIdealTemp);
            let score = 100 - (tempDiff * 16);

            if (gameState.powerOn && gameState.weather.requiredMode) {
                if (gameState.mode !== gameState.weather.requiredMode) {
                    score -= 35;
                }
            }

            gameState.comfortScore = Math.max(0, Math.min(100, score));

            // 低體感滿意度計時器
            if (gameState.comfortScore < 50.0) {
                gameState.lowComfortTimer += 0.016;
                if (gameState.lowComfortTimer >= 50.0) {
                    triggerGameOver("顧客體感舒適度低於 50% 超過 50 秒，不滿意離去了！");
                }
            } else {
                gameState.lowComfortTimer = 0;
            }

            soundFX.updateWindSound(gameState.powerOn, gameState.fanSpeed);

            // 🏆 勝利條件與【7秒緩衝機制】整合邏輯
            if (gameState.comfortScore >= 60.0) {
                gameState.holdTimer += 0.016;
                if (gameState.holdTimer >= 25.0) {
                    triggerVictory();
                }
            } else if (gameState.comfortScore < 50.0) {
                if (gameState.lowComfortTimer <= gameState.bufferPeriod) {
                    // 7秒緩衝期內受保護，凍結不扣減
                } else {
                    let decayRate = 0.005 + (gameState.lowComfortTimer - gameState.bufferPeriod) * 0.025;
                    gameState.holdTimer = Math.max(0, gameState.holdTimer - decayRate);
                }
            } else {
                gameState.holdTimer = Math.max(0, gameState.holdTimer - 0.005);
            }
        }

        // --- Render UI (Throttled for zero flicker) ---
        function updateUI() {
            document.getElementById('ui-indoor-temp').innerText = `${gameState.indoorTemp.toFixed(1)}°C`;
            document.getElementById('ui-target-temp').innerText = `${gameState.targetTemp}°C`;
            document.getElementById('ui-outdoor-temp').innerText = `${gameState.outdoorTemp.toFixed(1)}°C`;
            document.getElementById('ui-overlay-temp').innerText = `${gameState.indoorTemp.toFixed(1)}°C`;
            
            const comfortPercent = Math.round(gameState.comfortScore);
            document.getElementById('ui-comfort-val').innerText = `${comfortPercent}%`;
            document.getElementById('ui-overlay-comfort').innerText = `${comfortPercent}%`;
            document.getElementById('ui-comfort-bar').style.width = `${comfortPercent}%`;

            if (comfortPercent > 80) {
                document.getElementById('ui-comfort-bar').style.background = '#4CAF50';
            } else if (comfortPercent >= 50) {
                document.getElementById('ui-comfort-bar').style.background = '#FF9800';
            } else {
                document.getElementById('ui-comfort-bar').style.background = '#F44336';
            }

            // ⚠️ 低舒適度與 7秒緩衝期 提示邏輯
            const warningBox = document.getElementById('ui-warning-box');
            if (gameState.comfortScore < 50.0) {
                warningBox.classList.add('active');
                const remaining = Math.max(0, 50.0 - gameState.lowComfortTimer);
                document.getElementById('ui-low-comfort-timer').innerText = `${remaining.toFixed(1)}s`;
                
                if (gameState.lowComfortTimer <= gameState.bufferPeriod) {
                    const bufRemain = (gameState.bufferPeriod - gameState.lowComfortTimer).toFixed(1);
                    document.getElementById('ui-warning-reason').innerText = `🛡️ 【7秒緩衝期】生效中 (剩數 ${bufRemain}s)，請儘速調整！`;
                } else if (gameState.powerOn && gameState.mode !== gameState.weather.requiredMode) {
                    document.getElementById('ui-warning-reason').innerText = `⚠️ 緩衝期已結束！模式不符，請切換至【${gameState.weather.requiredModeName}】！`;
                } else {
                    document.getElementById('ui-warning-reason').innerText = `⚠️ 緩衝期已結束！體感持續過低，勝利進度倒扣中！`;
                }
            } else {
                warningBox.classList.remove('active');
            }

            if (gameState.isBroken) {
                document.getElementById('ui-efficiency-val').innerText = `效能: ${Math.round(gameState.coolingEfficiency * 100)}%`;
            }

            document.getElementById('ui-mode').innerText = gameState.modeNames[gameState.mode];
            document.getElementById('ui-fan').innerText = `${gameState.fanSpeed} 段`;
            document.getElementById('ui-swing').innerText = gameState.swing ? '自動搖擺' : '關閉';

            const powerVal = Math.round(gameState.powerUsage);
            document.getElementById('ui-power-val').innerText = `${powerVal} W`;
            const powerRatio = Math.min(100, (powerVal / 1200) * 100);
            document.getElementById('ui-power-bar').style.width = `${powerRatio}%`;

            const pStatus = document.getElementById('ui-power-status');
            const pBtnText = document.getElementById('txt-power-btn');
            const pBtn = document.getElementById('btn-power-toggle');

            if (gameState.powerOn) {
                pStatus.innerText = gameState.isBroken ? "故障運轉中" : "運轉中";
                pStatus.style.background = gameState.isBroken ? "#FFE4E6" : "#E8F5E9";
                pStatus.style.color = gameState.isBroken ? "#E11D48" : "#2E7D32";
                pBtnText.innerText = "關閉空調";
                pBtn.classList.add('active');
            } else {
                pStatus.innerText = "關機中";
                pStatus.style.background = "#FFEBEE";
                pStatus.style.color = "#D32F2F";
                pBtnText.innerText = "開啟空調";
                pBtn.classList.remove('active');
            }

            document.getElementById('ui-goal-timer').innerText = `${Math.min(25, Math.floor(gameState.holdTimer))} / 25s`;
        }

        // --- Canvas Rendering Loop (Living Room) ---
        const canvas = document.getElementById('room-canvas');
        const ctx = canvas.getContext('2d');

        let louverAngle = 0;
        let particles = [];
        let confettiParticles = [];

        function resizeCanvas() {
            const rect = canvas.parentElement.getBoundingClientRect();
            canvas.width = rect.width;
            canvas.height = rect.height;
        }
        window.addEventListener('resize', resizeCanvas);

        function drawRoom() {
            const w = canvas.width;
            const h = canvas.height;
            if (w === 0 || h === 0) return;

            ctx.clearRect(0, 0, w, h);

            // Wall Background
            ctx.fillStyle = '#E2E8F0';
            ctx.fillRect(0, 0, w, h);

            // Floor
            const floorY = h * 0.72;
            ctx.fillStyle = '#CBD5E1';
            ctx.fillRect(0, floorY, w, h - floorY);
            
            ctx.strokeStyle = '#94A3B8';
            ctx.lineWidth = 1;
            for (let x = 0; x < w; x += 60) {
                ctx.beginPath();
                ctx.moveTo(x, floorY);
                ctx.lineTo(x - 40, h);
                ctx.stroke();
            }

            // Window & Weather View
            const winX = w * 0.08;
            const winY = h * 0.12;
            const winW = w * 0.32;
            const winH = h * 0.45;

            const wid = gameState.weather ? gameState.weather.id : 'sun';
            if (['cold', 'blizzard'].includes(wid)) {
                ctx.fillStyle = '#94A3B8';
            } else if (['rain', 'plum_rain', 'typhoon', 'fog'].includes(wid)) {
                ctx.fillStyle = '#64748B';
            } else if (['foehn', 'heatwave'].includes(wid)) {
                ctx.fillStyle = '#FDBA74';
            } else if (wid === 'cool_night') {
                ctx.fillStyle = '#1E293B';
            } else {
                ctx.fillStyle = '#7DD3FC';
            }
            
            ctx.fillRect(winX, winY, winW, winH);

            if (['sun', 'heatwave', 'foehn'].includes(wid)) {
                const sunX = winX + winW * 0.75;
                const sunY = winY + winH * 0.28;
                ctx.save();
                ctx.translate(sunX, sunY);
                ctx.rotate(Date.now() * 0.001);
                ctx.fillStyle = '#FACE15';
                ctx.beginPath();
                ctx.arc(0, 0, 18, 0, Math.PI * 2);
                ctx.fill();
                for (let i = 0; i < 8; i++) {
                    ctx.rotate(Math.PI / 4);
                    ctx.fillRect(22, -2, 6, 4);
                }
                ctx.restore();
            }

            ctx.strokeStyle = '#FFFFFF';
            ctx.lineWidth = 6;
            ctx.strokeRect(winX, winY, winW, winH);
            ctx.beginPath();
            ctx.moveTo(winX + winW / 2, winY);
            ctx.lineTo(winX + winW / 2, winY + winH);
            ctx.stroke();

            // Plant
            const plantX = w * 0.06;
            const plantY = floorY - 10;
            ctx.fillStyle = '#D97706';
            ctx.beginPath();
            ctx.moveTo(plantX, plantY);
            ctx.lineTo(plantX + 30, plantY);
            ctx.lineTo(plantX + 24, plantY + 40);
            ctx.lineTo(plantX + 6, plantY + 40);
            ctx.closePath();
            ctx.fill();
            
            const sway = Math.sin(Date.now() * 0.002) * 4;
            ctx.fillStyle = '#16A34A';
            ctx.beginPath();
            ctx.ellipse(plantX + 15, plantY - 15, 12, 24 + sway, 0.2, 0, Math.PI * 2);
            ctx.ellipse(plantX + 4, plantY - 22, 10, 20 - sway, -0.4, 0, Math.PI * 2);
            ctx.ellipse(plantX + 26, plantY - 18, 11, 22 + sway, 0.5, 0, Math.PI * 2);
            ctx.fill();

            // Sofa & Character
            const sofaX = w * 0.45;
            const sofaY = floorY - 50;
            const sofaW = w * 0.42;
            const sofaH = 65;

            ctx.fillStyle = '#0284C7';
            ctx.beginPath();
            ctx.roundRect(sofaX, sofaY, sofaW, sofaH, 12);
            ctx.fill();
            ctx.fillStyle = '#38BDF8';
            ctx.beginPath();
            ctx.roundRect(sofaX + 8, sofaY - 24, sofaW - 16, 36, 10);
            ctx.fill();

            drawCharacter(sofaX + sofaW * 0.5, sofaY + 8);

            // AC Unit
            const acX = w * 0.52;
            const acY = h * 0.12;
            const acW = w * 0.38;
            const acH = 55;

            ctx.fillStyle = '#FFFFFF';
            ctx.shadowColor = 'rgba(0,0,0,0.1)';
            ctx.shadowBlur = 10;
            ctx.beginPath();
            ctx.roundRect(acX, acY, acW, acH, 10);
            ctx.fill();
            ctx.shadowBlur = 0;

            ctx.fillStyle = '#94A3B8';
            ctx.font = 'bold 9px sans-serif';
            ctx.fillText('SMART AC', acX + 14, acY + 18);

            ctx.fillStyle = '#0F172A';
            ctx.fillRect(acX + acW - 60, acY + 10, 44, 18);
            if (gameState.powerOn) {
                ctx.fillStyle = gameState.isBroken ? '#F43F5E' : '#38BDF8';
                ctx.font = 'bold 11px monospace';
                ctx.fillText(`${Math.round(gameState.indoorTemp)}°C`, acX + acW - 55, acY + 23);
                
                ctx.fillStyle = gameState.isBroken ? '#EF4444' : '#22C55E';
                ctx.beginPath();
                ctx.arc(acX + acW - 10, acY + 19, 3, 0, Math.PI * 2);
                ctx.fill();
            }

            if (gameState.isBroken && gameState.powerOn) {
                if (Math.random() < 0.3) {
                    ctx.fillStyle = Math.random() > 0.5 ? '#F59E0B' : '#EF4444';
                    ctx.fillRect(acX + Math.random() * acW, acY + Math.random() * acH, 3, 3);
                }
            }

            const targetLouver = gameState.powerOn ? (gameState.swing ? Math.sin(Date.now() * 0.005) * 20 + 25 : 35) : 0;
            louverAngle += (targetLouver - louverAngle) * 0.1;

            ctx.save();
            ctx.translate(acX + 12, acY + acH - 5);
            ctx.rotate((louverAngle * Math.PI) / 180);
            ctx.fillStyle = '#CBD5E1';
            ctx.fillRect(0, 0, acW - 24, 5);
            ctx.restore();

            // Wind Particles
            if (gameState.powerOn && louverAngle > 5) {
                const spawnChance = gameState.isBroken ? 0.2 * gameState.coolingEfficiency : 0.6;
                if (Math.random() < spawnChance) {
                    particles.push({
                        x: acX + 20 + Math.random() * (acW - 40),
                        y: acY + acH,
                        vx: (-1.5 - Math.random() * 2 * (gameState.fanSpeed * 0.5)) * gameState.coolingEfficiency,
                        vy: (2 + Math.random() * 2) * gameState.coolingEfficiency,
                        alpha: 0.8,
                        size: 2.5 + Math.random() * 3
                    });
                }
            }

            for (let i = particles.length - 1; i >= 0; i--) {
                const p = particles[i];
                p.x += p.vx;
                p.y += p.vy;
                p.alpha -= 0.015;

                if (p.alpha <= 0) {
                    particles.splice(i, 1);
                    continue;
                }

                ctx.fillStyle = gameState.mode === 'heat' ? `rgba(251, 146, 60, ${p.alpha})` : `rgba(56, 189, 248, ${p.alpha})`;
                ctx.beginPath();
                ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
                ctx.fill();
            }

            if (gameState.isGameWon) {
                renderConfetti(w, h);
            }
        }

        function drawCharacter(cx, cy) {
            ctx.save();
            ctx.translate(cx, cy);

            const temp = gameState.indoorTemp;
            const target = gameState.targetIdealTemp;
            let state = 'normal';
            if (temp > target + 2.5) state = 'hot';
            else if (temp < target - 2.5) state = 'cold';

            let headX = 0;
            if (state === 'cold') {
                headX = (Math.random() - 0.5) * 3;
            }

            ctx.fillStyle = '#FDBA74';
            ctx.beginPath();
            ctx.arc(headX, -32, 18, 0, Math.PI * 2);
            ctx.fill();

            ctx.fillStyle = '#475569';
            ctx.beginPath();
            ctx.arc(headX, -38, 18, Math.PI, Math.PI * 2);
            ctx.fill();

            ctx.strokeStyle = '#1E293B';
            ctx.lineWidth = 2;
            if (state === 'hot') {
                ctx.beginPath();
                ctx.moveTo(headX - 8, -34); ctx.lineTo(headX - 2, -30);
                ctx.moveTo(headX + 8, -34); ctx.lineTo(headX + 2, -30);
                ctx.stroke();

                ctx.fillStyle = '#38BDF8';
                ctx.beginPath();
                ctx.arc(headX + 13, -36 + (Date.now() % 1000) * 0.02, 2.5, 0, Math.PI * 2);
                ctx.fill();

                ctx.beginPath();
                ctx.arc(headX, -22, 4, 0, Math.PI);
                ctx.stroke();
            } else if (state === 'cold') {
                ctx.beginPath();
                ctx.arc(headX - 6, -34, 1.5, 0, Math.PI * 2);
                ctx.arc(headX + 6, -34, 1.5, 0, Math.PI * 2);
                ctx.fill();

                ctx.beginPath();
                ctx.moveTo(headX - 5, -22);
                ctx.lineTo(headX - 2, -24);
                ctx.lineTo(headX + 2, -20);
                ctx.lineTo(headX + 5, -22);
                ctx.stroke();
            } else {
                ctx.beginPath();
                ctx.arc(headX - 6, -34, 3, Math.PI, 0);
                ctx.arc(headX + 6, -34, 3, Math.PI, 0);
                ctx.stroke();

                ctx.beginPath();
                ctx.arc(headX, -26, 6, 0, Math.PI);
                ctx.stroke();
            }

            ctx.fillStyle = state === 'hot' ? '#EF4444' : (state === 'cold' ? '#3B82F6' : '#10B981');
            ctx.beginPath();
            ctx.roundRect(-16, -12, 32, 36, 6);
            ctx.fill();

            ctx.restore();
        }

        function triggerVictory() {
            gameState.isGameWon = true;
            soundFX.playChime(true);
            document.getElementById('txt-victory-msg').innerText = `恭喜！你成功維持顧客目標舒適度長達 25 秒！`;
            document.getElementById('victory-modal').classList.add('active');

            for (let i = 0; i < 80; i++) {
                confettiParticles.push({
                    x: canvas.width / 2,
                    y: canvas.height / 2,
                    vx: (Math.random() - 0.5) * 10,
                    vy: -Math.random() * 8 - 3,
                    color: ['#FF5722', '#4CAF50', '#2196F3', '#FFEB3B', '#9C27B0'][Math.floor(Math.random() * 5)],
                    size: 5 + Math.random() * 5
                });
            }
        }

        function triggerGameOver(reason) {
            gameState.isGameOver = true;
            soundFX.playChime(false);
            
            const msgEl = document.getElementById('txt-failure-msg');
            if (msgEl && reason) {
                msgEl.innerText = reason;
            }

            document.getElementById('qte-modal').classList.remove('active');
            document.getElementById('filter-qte-modal').classList.remove('active');
            document.getElementById('water-qte-modal').classList.remove('active');
            document.getElementById('failure-modal').classList.add('active');
        }

        function renderConfetti(w, h) {
            for (let i = confettiParticles.length - 1; i >= 0; i--) {
                const c = confettiParticles[i];
                c.x += c.vx;
                c.y += c.vy;
                c.vy += 0.2;

                ctx.fillStyle = c.color;
                ctx.fillRect(c.x, c.y, c.size, c.size);

                if (c.y > h) confettiParticles.splice(i, 1);
            }
        }

        function resetGame() {
            setRandomWeather();
            gameState.powerOn = false;
            gameState.targetTemp = 24;
            gameState.holdTimer = 0;
            gameState.lowComfortTimer = 0;
            gameState.weatherTimer = 0;
            gameState.isGameWon = false;
            gameState.isGameOver = false;
            gameState.isBroken = false;
            gameState.coolingEfficiency = 1.0;
            gameState.breakdownCheckTimer = 0;

            gameState.indoorTemp = gameState.outdoorTemp > 20 ? gameState.outdoorTemp - 5 : gameState.outdoorTemp + 10;

            document.getElementById('victory-modal').classList.remove('active');
            document.getElementById('failure-modal').classList.remove('active');
            document.getElementById('qte-modal').classList.remove('active');
            document.getElementById('filter-qte-modal').classList.remove('active');
            document.getElementById('water-qte-modal').classList.remove('active');
            document.getElementById('ui-breakdown-card').classList.remove('active');
            document.getElementById('ui-warning-box').classList.remove('active');
            updateUI();
        }

        // --- Cover Screen Animation ---
        const coverCanvas = document.getElementById('cover-canvas');
        const coverCtx = coverCanvas.getContext('2d');
        function drawCoverAnimation() {
            const w = coverCanvas.width;
            const h = coverCanvas.height;
            coverCtx.clearRect(0, 0, w, h);

            coverCtx.fillStyle = '#F1F5F9';
            coverCtx.fillRect(0, 0, w, h);

            coverCtx.fillStyle = '#FFFFFF';
            coverCtx.fillRect(w * 0.3, 20, w * 0.4, 45);
            coverCtx.fillStyle = '#0284C7';
            coverCtx.font = 'bold 12px sans-serif';
            coverCtx.fillText('Smart AC', w * 0.3 + 15, 45);

            coverCtx.fillStyle = '#F59E0B';
            coverCtx.beginPath();
            coverCtx.arc(w - 50, 40, 20, 0, Math.PI * 2);
            coverCtx.fill();

            requestAnimationFrame(drawCoverAnimation);
        }
        drawCoverAnimation();

        // --- Event Listeners ---
        document.getElementById('btn-start-game').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep();
            resetGame();
            document.getElementById('cover-screen').style.display = 'none';
            resizeCanvas();
        });

        document.getElementById('btn-show-instructions').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep();
            document.getElementById('instructions-modal').classList.add('active');
        });

        document.getElementById('btn-close-instructions').addEventListener('click', () => {
            soundFX.playBeep();
            document.getElementById('instructions-modal').classList.remove('active');
        });

        document.getElementById('btn-restart-game').addEventListener('click', () => {
            soundFX.playBeep();
            resetGame();
        });

        document.getElementById('btn-retry-game').addEventListener('click', () => {
            soundFX.playBeep();
            resetGame();
        });

        document.getElementById('btn-trigger-qte').addEventListener('click', openRepairModal);
        document.getElementById('btn-qte-action').addEventListener('click', handleQTEClick);

        document.getElementById('btn-power-toggle').addEventListener('click', () => {
            soundFX.init();
            gameState.powerOn = !gameState.powerOn;
            soundFX.playBeep(gameState.powerOn ? 1000 : 500);
            updateUI();
        });

        document.getElementById('btn-temp-up').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep(900);
            gameState.targetTemp = Math.min(30, gameState.targetTemp + 1);
            if (!gameState.powerOn) gameState.powerOn = true;
            updateUI();
        });

        document.getElementById('btn-temp-down').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep(700);
            gameState.targetTemp = Math.max(16, gameState.targetTemp - 1);
            if (!gameState.powerOn) gameState.powerOn = true;
            updateUI();
        });

        document.getElementById('btn-mode-next').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep(800);
            const idx = gameState.modesList.indexOf(gameState.mode);
            gameState.mode = gameState.modesList[(idx + 1) % gameState.modesList.length];
            updateUI();
        });

        document.getElementById('btn-mode-prev').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep(800);
            const idx = gameState.modesList.indexOf(gameState.mode);
            gameState.mode = gameState.modesList[(idx - 1 + gameState.modesList.length) % gameState.modesList.length];
            updateUI();
        });

        document.getElementById('btn-fan-next').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep(850);
            gameState.fanSpeed = (gameState.fanSpeed % 5) + 1;
            updateUI();
        });

        document.getElementById('btn-fan-prev').addEventListener('click', () => {
            soundFX.init();
            soundFX.playBeep(850);
            gameState.fanSpeed = gameState.fanSpeed === 1 ? 5 : gameState.fanSpeed - 1;
            updateUI();
        });

        document.querySelectorAll('.btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                const circle = document.createElement('span');
                const diameter = Math.max(this.clientWidth, this.clientHeight);
                const radius = diameter / 2;
                const rect = this.getBoundingClientRect();
                circle.style.width = circle.style.height = `${diameter}px`;
                circle.style.left = `${e.clientX - rect.left - radius}px`;
                circle.style.top = `${e.clientY - rect.top - radius}px`;
                circle.classList.add('ripple');

                const ripple = this.getElementsByClassName('ripple')[0];
                if (ripple) ripple.remove();

                this.appendChild(circle);
            });
        });

        // Loop execution with UI update throttling to reduce frame thrashing & flicker
        let uiFrameCounter = 0;
        function gameLoop() {
            updateThermalPhysics();
            updateQTELoop();
            updateFilterQTELoop();
            updateWaterQTELoop();

            uiFrameCounter++;
            if (uiFrameCounter % 6 === 0) {
                updateUI();
            }

            drawRoom();
            requestAnimationFrame(gameLoop);
        }

        resizeCanvas();
        requestAnimationFrame(gameLoop);
    </script>
</body>
</html>
