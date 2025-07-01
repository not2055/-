<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>초시공 네트워크</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'HCR Dotum', sans-serif;
            background: linear-gradient(135deg, #7fb3d3 0%, #5a9fd4 100%);
            min-height: 100vh;
            overflow: hidden;
            position: relative;
        }

        /* === 데스크톱 아이콘 === */
        .desktop-icons {
            position: absolute;
            top: calc(50px + 2cm);
            left: 5cm;
            z-index: 1;
        }

        .desktop-icon {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 3cm;
            cursor: pointer;
            transition: transform 0.2s ease;
            opacity: 0;
            animation: iconFadeIn 0.6s ease-out forwards;
        }

        .desktop-icon:nth-child(1) { animation-delay: 0.2s; }
        .desktop-icon:nth-child(2) { animation-delay: 0.4s; }
        .desktop-icon:nth-child(3) { animation-delay: 0.6s; }

        .desktop-icon:hover {
            transform: scale(1.1);
        }

        @keyframes iconFadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* === 메인 창 === */
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: transparent;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }

        .overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .window {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0.7);
            width: 76%;
            max-width: 960px;
            height: 72%;
            background: #5B81B3;
            border-radius: 20px;
            overflow: hidden;
            opacity: 0;
            transition: all 0.5s cubic-bezier(0.34, 1.56, 0.64, 1);
            padding: 30px;
        }

        .overlay.active .window {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
        }

        .top-icons {
            position: absolute;
            top: 10px;
            right: 30px;
            display: flex;
            gap: 15px;
            z-index: 10;
        }

        .top-icon {
            width: 38px;
            height: 38px;
            cursor: pointer;
            transition: transform 0.2s ease;
            border-radius: 6px;
            background: transparent;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .top-icon:hover {
            transform: scale(1.1);
        }

        .top-icon img {
            width: 24px;
            height: 24px;
            object-fit: contain;
        }

        .window-content {
            height: calc(100% - 30px);
            background: #f5f5dc;
            border-radius: 15px;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            margin-top: 30px;
        }

        .main-content {
            flex: 1;
            padding: 30px;
            background: #f5f5dc;
            color: #333;
            font-size: 16px;
            line-height: 1.6;
            display: flex;
            flex-direction: column;
            height: 100%;
            overflow: hidden;
        }

        .hidden {
            display: none;
        }

        /* === 파일 탐색기 === */
        .file-explorer {
            flex: 1;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            height: 100%;
        }

        .file-explorer-content {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
            background: transparent;
            height: 100%;
            box-sizing: border-box;
        }

        .post-list {
            padding-top: 20px;
            height: calc(100vh - 300px);
            max-height: 600px;
            overflow-y: auto;
            overflow-x: hidden;
        }

        .post-item {
            padding: 15px;
            border-bottom: 1px solid #eee;
            transition: background-color 0.3s ease;
            cursor: pointer;
            position: relative;
        }

        .post-item:hover {
            background-color: #f8f9fa;
        }

        .post-title {
            font-weight: bold;
            color: #5B81B3;
            margin-bottom: 5px;
            font-size: 16px;
        }

        .post-content {
            color: #666;
            font-size: 14px;
            margin-bottom: 5px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            max-width: 100%;
        }

        .post-date {
            font-size: 12px;
            color: #999;
        }

        .empty-folder {
            text-align: center;
            color: #666;
            margin-top: 50px;
        }

        .empty-folder-icon {
            font-size: 64px;
            margin-bottom: 20px;
            opacity: 0.5;
        }

        /* === 갤러리 === */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .gallery-item {
            position: relative;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            cursor: pointer;
            transition: transform 0.2s ease;
        }

        .gallery-item:hover {
            transform: scale(1.05);
        }

        .gallery-item img {
            width: 100%;
            height: 150px;
            object-fit: cover;
        }

        /* === 관리자 페이지 === */
        .admin-login {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
        }

        .admin-login-box {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            text-align: center;
            max-width: 400px;
            width: 100%;
        }

        .admin-login-box h2 {
            color: #5B81B3;
            margin-bottom: 20px;
        }

        .admin-password-input {
            width: 100%;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            text-align: center;
            margin: 20px 0;
            transition: border-color 0.3s ease;
        }

        .admin-password-input:focus {
            outline: none;
            border-color: #5B81B3;
            box-shadow: 0 0 0 3px rgba(91, 129, 179, 0.1);
        }

        .admin-login-btn {
            width: 100%;
            padding: 12px;
            background: linear-gradient(135deg, #5B81B3 0%, #4a6d96 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .admin-login-btn:hover {
            background: linear-gradient(135deg, #4a6d96 0%, #3a5a7a 100%);
        }

        .admin-login-error {
            color: #ff4757;
            font-size: 14px;
            margin-top: 10px;
            display: none;
        }

        /* === 모달 === */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.6);
            display: none;
            justify-content: center;
            align-items: center;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }

        .modal-header {
            background: linear-gradient(135deg, #5B81B3 0%, #4a6d96 100%);
            color: white;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-header h3 {
            margin: 0;
            font-size: 18px;
        }

        .modal-close {
            background: rgba(255,255,255,0.2);
            border: none;
            color: white;
            font-size: 20px;
            width: 35px;
            height: 35px;
            border-radius: 50%;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s ease;
        }

        .modal-close:hover {
            background: rgba(255,255,255,0.3);
        }

        /* === 글 읽기 모달 === */
        .post-modal {
            background: rgba(0,0,0,0.7);
            z-index: 3000;
        }

        .post-modal-content {
            width: 90%;
            max-width: 800px;
            height: 85%;
            display: flex;
            flex-direction: column;
        }

        .post-modal-body {
            flex: 1;
            padding: 30px;
            overflow-y: auto;
            background: #fafafa;
        }

        .post-modal-date {
            color: #666;
            font-size: 14px;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .post-modal-text {
            line-height: 1.8;
            white-space: pre-wrap;
            color: #333;
            font-size: 16px;
            font-family: 'Malgun Gothic', sans-serif;
        }

        .post-modal-footer {
            padding: 20px 30px;
            border-top: 1px solid #eee;
            background: #f8f9fa;
            display: flex;
            justify-content: flex-end;
            align-items: center;
        }

        .modal-btn-group {
            display: flex;
            gap: 10px;
        }

        .modal-btn {
            padding: 10px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 500;
            transition: background-color 0.3s ease;
        }

        .modal-btn-close {
            background: #5B81B3;
            color: white;
        }

        .modal-btn-close:hover {
            background: #4a6d96;
        }

        /* === 이미지 모달 === */
        .image-modal {
            background: rgba(0,0,0,0.9);
            z-index: 5000;
        }

        .image-modal-content {
            position: relative;
            max-width: 660px;
            max-height: 660px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .image-modal-img {
            width: 100%;
            height: 100%;
            max-width: 550px;
            max-height: 550px;
            object-fit: contain;
            border-radius: 10px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.5);
        }

        .image-modal-close {
            position: absolute;
            top: -50px;
            right: -50px;
            width: 40px;
            height: 40px;
            background: rgba(255,255,255,0.2);
            border: none;
            border-radius: 50%;
            color: white;
            font-size: 20px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s ease;
        }

        .image-modal-close:hover {
            background: rgba(255,255,255,0.3);
        }

        .image-modal-info {
            position: absolute;
            bottom: -60px;
            left: 50%;
            transform: translateX(-50%);
            color: white;
            text-align: center;
            font-size: 14px;
            background: rgba(0,0,0,0.6);
            padding: 10px 20px;
            border-radius: 20px;
        }

        /* === 반응형 === */
        @media (max-width: 768px) {
            .desktop-icons {
                top: calc(30px + 2cm);
                left: 3cm;
            }
            
            .desktop-icon {
                margin-bottom: 2.5cm;
            }
        }
    </style>
</head>
<body>
    <!-- 데스크톱 아이콘들 -->
    <div class="desktop-icons">
        <div class="desktop-icon" data-type="folder">
            <div class="icon-image folder-icon">
                <img src="https://i.ibb.co/1Gt7DfcH/image.png" alt="폴더" style="width: 100px; height: 100px; object-fit: contain;">
            </div>
        </div>
        <div class="desktop-icon" data-type="gallery">
            <div class="icon-image image-icon">
                <img src="https://i.ibb.co/JwSq6T6N/image.png" alt="갤러리" style="width: 80px; height: 80px; object-fit: contain;">
            </div>
        </div>
        <div class="desktop-icon" data-type="browser">
            <div class="icon-image browser-icon">
                <img src="https://i.ibb.co/qMhQTP83/image.png" alt="브라우저" style="width: 80px; height: 80px; object-fit: contain;">
            </div>
        </div>
    </div>

    <!-- 메인 창 -->
    <div class="overlay" id="overlay">
        <div class="window" id="window">
            <!-- 상단 아이콘들 -->
            <div class="top-icons">
                <div class="top-icon">
                    <img src="https://i.ibb.co/C3kZTmHJ/image.png" alt="아이콘1" style="width: 30px; height: 30px; object-fit: contain;">
                </div>
                <div class="top-icon">
                    <img src="https://i.ibb.co/LbGhYHH/image.png" alt="동기화" style="width: 30px; height: 30px; object-fit: contain;">
                </div>
                <div class="top-icon" onclick="closeWindow()">
                    <img src="https://i.ibb.co/8LGG3FnW/x.png" alt="닫기" style="width: 30px; height: 30px; object-fit: contain;">
                </div>
            </div>
            
            <div class="window-content">
                <!-- 폴더 -->
                <div class="main-content" id="folderContent">
                    <div class="file-explorer">
                        <div class="file-explorer-content">
                            <div class="empty-folder" id="emptyFolder" style="display: none;">
                                <div class="empty-folder-icon">📂</div>
                                <p>폴더가 비어있습니다</p>
                            </div>
                            <div class="post-list" id="postList"></div>
                        </div>
                    </div>
                </div>

                <!-- 갤러리 -->
                <div class="main-content hidden" id="galleryContent">
                    <div class="file-explorer">
                        <div class="file-explorer-content">
                            <div class="empty-folder" id="emptyGallery" style="display: none;">
                                <div class="empty-folder-icon">🖼️</div>
                                <p>갤러리가 비어있습니다</p>
                            </div>
                            <div class="gallery-grid" id="galleryGrid"></div>
                        </div>
                    </div>
                </div>

                <!-- 브라우저 - 관리자 페이지 -->
                <div class="main-content hidden" id="browserContent">
                    <div class="admin-login">
                        <div class="admin-login-box">
                            <h2>🔐 관리자 로그인</h2>
                            <p>관리자 페이지에 접근하려면 비밀번호를 입력하세요</p>
                            <input type="password" id="adminPasswordInput" class="admin-password-input" placeholder="관리자 비밀번호 입력">
                            <button class="admin-login-btn" onclick="adminLogin()">로그인</button>
                            <div class="admin-login-error" id="adminLoginError">비밀번호가 틀렸습니다!</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 글 읽기 모달 -->
    <div class="modal post-modal" id="postModal">
        <div class="modal-content post-modal-content">
            <div class="modal-header">
                <h3 class="post-modal-title" id="modalTitle"></h3>
                <button class="modal-close" onclick="closePostModal()">×</button>
            </div>
            <div class="post-modal-body">
                <div class="post-modal-date" id="modalDate"></div>
                <div class="post-modal-text" id="modalContent"></div>
            </div>
            <div class="post-modal-footer">
                <div class="modal-btn-group">
                    <button class="modal-btn modal-btn-close" onclick="closePostModal()">닫기</button>
                </div>
            </div>
        </div>
    </div>

    <!-- 이미지 모달 -->
    <div class="modal image-modal" id="imageModal">
        <div class="image-modal-content">
            <button class="image-modal-close" onclick="closeImageModal()">×</button>
            <img class="image-modal-img" id="modalImage" src="" alt="">
            <div class="image-modal-info" id="modalImageInfo"></div>
        </div>
    </div>

    <script>
        console.log('🎉 초시공 네트워크 메인 시작...');
        
        // === 전역 변수 ===
        let posts = [];
        let images = [];
        let currentView = 'folder';
        let currentPostId = null;
        let isAdminLoggedIn = false;
        const ADMIN_PASSWORD = 'no.4';

        // === 미리 데이터 추가 ===
        function loadDemoData() {
            posts = [
                {
                    id: 1,
                    title: "초시공 네트워크에 오신 것을 환영합니다",
                    content: "이곳은 시공간을 초월한 디지털 공간입니다.\n\n다양한 차원의 정보와 이야기들이 교차하는 특별한 장소입니다.\n\n관리자 로그인을 통해 새로운 콘텐츠를 추가할 수 있습니다.",
                    created_at: "2024-12-01T10:00:00.000Z"
                },
                {
                    id: 2,
                    title: "차원 이동 로그 #001",
                    content: "오늘 새로운 차원을 발견했습니다.\n\n좌표: X-742, Y-338, Z-901\n상태: 안정\n\n이 차원은 특이하게도 시간의 흐름이 역방향으로 진행됩니다.\n과거로 향하는 메시지들을 확인할 수 있었습니다.\n\n추가 탐사가 필요합니다.",
                    created_at: "2024-12-02T14:30:00.000Z"
                },
                {
                    id: 3,
                    title: "연결된 세계들",
                    content: "네트워크를 통해 연결된 다양한 세계들:\n\n1. 디지털 공간\n2. 물리적 현실\n3. 의식의 영역\n4. 상상의 차원\n\n각각의 세계는 고유한 법칙과 특성을 가지고 있으며,\n초시공 네트워크를 통해 상호작용합니다.",
                    created_at: "2024-12-03T09:15:00.000Z"
                },
                {
                    id: 4,
                    title: "시간 여행자의 메모",
                    content: "2157년에서 온 메시지:\n\n'과거의 여러분에게 전합니다.\n미래는 여러분이 만드는 선택들로 이루어집니다.\n\n기술과 인간성의 균형을 잃지 마세요.\n초시공 네트워크는 그 균형의 상징입니다.'\n\n- 미래의 네트워크 관리자",
                    created_at: "2024-12-04T18:45:00.000Z"
                }
            ];

            images = [
                {
                    id: 'demo1',
                    name: '차원의_문.jpg',
                    url: 'data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjIwMCIgdmlld0JveD0iMCAwIDMwMCAyMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIzMDAiIGhlaWdodD0iMjAwIiBmaWxsPSJ1cmwoI2dyYWQpIi8+CjxjaXJjbGUgY3g9IjE1MCIgY3k9IjEwMCIgcj0iNTAiIGZpbGw9InJnYmEoMjU1LCAyNTUsIDI1NSwgMC4zKSIvPgo8dGV4dCB4PSIxNTAiIHk9IjEwNSIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZmlsbD0id2hpdGUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxNCI+8J+MgCDssKjsm5Q8L3RleHQ+CjxkZWZzPgo8bGluZWFyR3JhZGllbnQgaWQ9ImdyYWQiIHgxPSIwJSIgeTE9IjAlIiB4Mj0iMTAwJSIgeTI9IjEwMCUiPgo8c3RvcCBvZmZzZXQ9IjAlIiBzdHlsZT0ic3RvcC1jb2xvcjojNGY0NmU1O3N0b3Atb3BhY2l0eToxIiAvPgo8c3RvcCBvZmZzZXQ9IjEwMCUiIHN0eWxlPSJzdG9wLWNvbG9yOiM3YzNhZWQ7c3RvcC1vcGFjaXR5OjEiIC8+CjwvbGluZWFyR3JhZGllbnQ+CjwvZGVmcz4KPHN2Zz4K',
                    created_at: "2024-12-01T10:00:00.000Z"
                },
                {
                    id: 'demo2',
                    name: '시공간_지도.png',
                    url: 'data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjIwMCIgdmlld0JveD0iMCAwIDMwMCAyMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIzMDAiIGhlaWdodD0iMjAwIiBmaWxsPSIjMGQxMTE3Ii8+CjxwYXRoIGQ9Ik01MCA1MEwxMDAgMzBMMTUwIDgwTDIwMCA0MEwyNTAgNzBMMjgwIDUwIiBzdHJva2U9IiM2NjY2ZmYiIHN0cm9rZS13aWR0aD0iMiIgZmlsbD0ibm9uZSIvPgo8cGF0aCBkPSJNMjAgMTIwTDgwIDEwMEwxNDAgMTQwTDE4MCA5MEwyNDAgMTMwTDI5MCAyMDAiIHN0cm9rZT0iIzY2ZmY2NiIgc3Ryb2tlLXdpZHRoPSIyIiBmaWxsPSJub25lIi8+CjxjaXJjbGUgY3g9IjE1MCIgY3k9IjgwIiByPSI1IiBmaWxsPSIjZmY2NjY2Ii8+CjxjaXJjbGUgY3g9IjIwMCIgY3k9IjQwIiByPSI1IiBmaWxsPSIjZmZmZjY2Ii8+CjxjaXJjbGUgY3g9IjE0MCIgY3k9IjE0MCIgcj0iNSIgZmlsbD0iIzY2ZmZmZiIvPgo8dGV4dCB4PSIxNTAiIHk9IjE4MCIgdGV4dC1hbmNob3I9Im1pZGRsZSIgZmlsbD0id2hpdGUiIGZvbnQtZmFtaWx5PSJBcmlhbCIgZm9udC1zaXplPSIxMiI+8J+XuuKchO+4jyDsl5DqtJPrkJwg7KeA64+EPC90ZXh0Pgo8L3N2Zz4K',
                    created_at: "2024-12-02T14:30:00.000Z"
                },
                {
                    id: 'demo3',
                    name: '네트워크_허브.gif',
                    url: 'data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjIwMCIgdmlld0JveD0iMCAwIDMwMCAyMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIzMDAiIGhlaWdodD0iMjAwIiBmaWxsPSJ1cmwoI25ldEdyYWQpIi8+CjxjaXJjbGUgY3g9IjE1MCIgY3k9IjEwMCIgcj0iMjAiIGZpbGw9IiNmZmZmZmYiIG9wYWNpdHk9IjAuOSIvPgo8Y2lyY2xlIGN4PSI3NSIgY3k9IjYwIiByPSIxMCIgZmlsbD0iIzY2ZmY2NiIgb3BhY2l0eT0iMC43Ii8+CjxjaXJjbGUgY3g9IjIyNSIgY3k9IjYwIiByPSIxMCIgZmlsbD0iIzY2ZmY2NiIgb3BhY2l0eT0iMC43Ii8+CjxjaXJjbGUgY3g9Ijc1IiBjeT0iMTQwIiByPSIxMCIgZmlsbD0iIzY2ZmY2NiIgb3BhY2l0eT0iMC43Ii8+CjxjaXJjbGUgY3g9IjIyNSIgY3k9IjE0MCIgcj0iMTAiIGZpbGw9IiM2NmZmNjYiIG9wYWNpdHk9IjAuNyIvPgo8bGluZSB4MT0iMTUwIiB5MT0iMTAwIiB4Mj0iNzUiIHkyPSI2MCIgc3Ryb2tlPSIjZmZmZmZmIiBzdHJva2Utd2lkdGg9IjIiIG9wYWNpdHk9IjAuNSIvPgo8bGluZSB4MT0iMTUwIiB5MT0iMTAwIiB4Mj0iMjI1IiB5Mj0iNjAiIHN0cm9rZT0iI2ZmZmZmZiIgc3Ryb2tlLXdpZHRoPSIyIiBvcGFjaXR5PSIwLjUiLz4KPGxpbmUgeDE9IjE1MCIgeTE9IjEwMCIgeDI9Ijc1IiB5Mj0iMTQwIiBzdHJva2U9IiNmZmZmZmYiIHN0cm9rZS13aWR0aD0iMiIgb3BhY2l0eT0iMC41Ii8+CjxsaW5lIHgxPSIxNTAiIHkxPSIxMDAiIHgyPSIyMjUiIHkyPSIxNDAiIHN0cm9rZT0iI2ZmZmZmZiIgc3Ryb2tlLXdpZHRoPSIyIiBvcGFjaXR5PSIwLjUiLz4KPHR5ZXQgeD0iMTUwIiB5PSIxOTAiIHRleHQtYW5jaG9yPSJtaWRkbGUiIGZpbGw9IndoaXRlIiBmb250LWZhbWlseT0iQXJpYWwiIGZvbnQtc2l6ZT0iMTIiPvCfpKEg64Kg7Yq47JuI7YGs7ZuICOygleuztDwvdGV4dD4KPGRlZnM+CjxsaW5lYXJHcmFkaWVudCBpZD0ibmV0R3JhZCIgeDE9IjAlIiB5MT0iMCUiIHgyPSIxMDAlIiB5Mj0iMTAwJSI+CjxzdG9wIG9mZnNldD0iMCUiIHN0eWxlPSJzdG9wLWNvbG9yOiMxYTE2NWQ7c3RvcC1vcGFjaXR5OjEiIC8+CjxzdG9wIG9mZnNldD0iMTAwJSIgc3R5bGU9InN0b3AtY29sb3I6IzMzMTY2NjtzdG9wLW9wYWNpdHk6MSIgLz4KPC9saW5lYXJHcmFkaWVudD4KPC9kZWZzPgo8L3N2Zz4K',
                    created_at: "2024-12-03T09:15:00.000Z"
                }
            ];
        }

        // === 창 관리 ===
        function showWindow(type = 'folder') {
            const overlay = document.getElementById('overlay');
            currentView = type;
            
            document.getElementById('folderContent').classList.add('hidden');
            document.getElementById('galleryContent').classList.add('hidden');
            document.getElementById('browserContent').classList.add('hidden');
            
            if (type === 'folder') {
                document.getElementById('folderContent').classList.remove('hidden');
                updatePostList();
            } else if (type === 'gallery') {
                document.getElementById('galleryContent').classList.remove('hidden');
                updateGallery();
            } else if (type === 'browser') {
                document.getElementById('browserContent').classList.remove('hidden');
            }
            
            overlay.classList.add('active');
        }

        function closeWindow() {
            const overlay = document.getElementById('overlay');
            overlay.classList.remove('active');
        }

        // === 관리자 로그인 ===
        function adminLogin() {
            const adminPasswordInput = document.getElementById('adminPasswordInput');
            const adminLoginError = document.getElementById('adminLoginError');
            
            if (!adminPasswordInput) return;
            
            const inputPassword = adminPasswordInput.value.trim();
            
            if (inputPassword === ADMIN_PASSWORD) {
                isAdminLoggedIn = true;
                alert('관리자 로그인 성공! (관리 기능은 준비 중입니다)');
                console.log('✅ 관리자 로그인 성공');
            } else {
                if (adminLoginError) adminLoginError.style.display = 'block';
                adminPasswordInput.value = '';
                adminPasswordInput.focus();
                console.log('❌ 관리자 로그인 실패');
            }
        }

        // === 글 관리 ===
        function updatePostList() {
            const postList = document.getElementById('postList');
            const emptyFolder = document.getElementById('emptyFolder');
            
            if (!postList) return;
            
            postList.innerHTML = '';
            
            if (posts.length === 0) {
                if (emptyFolder) emptyFolder.style.display = 'block';
                return;
            }
            
            if (emptyFolder) emptyFolder.style.display = 'none';
            
            posts.forEach(post => {
                const postElement = document.createElement('div');
                postElement.className = 'post-item';
                
                const firstLine = post.content.split('\n')[0];
                const preview = firstLine.length > 80 ? firstLine.substring(0, 80) + '...' : firstLine;
                
                postElement.innerHTML = `
                    <div class="post-title">${escapeHtml(post.title)}</div>
                    <div class="post-content">${escapeHtml(preview)}</div>
                    <div class="post-date">${new Date(post.created_at).toLocaleString('ko-KR')}</div>
                `;
                
                postElement.addEventListener('click', () => {
                    viewPost(post.id);
                });
                
                postList.appendChild(postElement);
            });
        }

        function viewPost(postId) {
            const post = posts.find(p => p.id == postId);
            if (!post) return;
            
            currentPostId = postId;
            
            const modalTitle = document.getElementById('modalTitle');
            const modalDate = document.getElementById('modalDate');
            const modalContent = document.getElementById('modalContent');
            const postModal = document.getElementById('postModal');
            
            if (modalTitle) modalTitle.textContent = post.title;
            if (modalDate) modalDate.textContent = new Date(post.created_at).toLocaleString('ko-KR');
            if (modalContent) modalContent.textContent = post.content;
            if (postModal) postModal.classList.add('active');
        }

        function closePostModal() {
            const postModal = document.getElementById('postModal');
            if (postModal) postModal.classList.remove('active');
            currentPostId = null;
        }

        // === 갤러리 관리 ===
        function updateGallery() {
            const galleryGrid = document.getElementById('galleryGrid');
            const emptyGallery = document.getElementById('emptyGallery');
            
            if (!galleryGrid) return;
            
            galleryGrid.innerHTML = '';
            
            if (images.length === 0) {
                if (emptyGallery) emptyGallery.style.display = 'block';
                return;
            }
            
            if (emptyGallery) emptyGallery.style.display = 'none';
            
            images.forEach(imageData => addImageToGallery(imageData));
        }

        function addImageToGallery(imageData) {
            const galleryGrid = document.getElementById('galleryGrid');
            if (!galleryGrid) return;
            
            const imageElement = document.createElement('div');
            imageElement.className = 'gallery-item';
            imageElement.innerHTML = `<img src="${imageData.url}" alt="${imageData.name}" title="${imageData.name}">`;
            
            imageElement.addEventListener('click', () => {
                showImageModal(imageData);
            });
            
            galleryGrid.appendChild(imageElement);
        }

        function showImageModal(imageData) {
            const imageModal = document.getElementById('imageModal');
            const modalImage = document.getElementById('modalImage');
            const modalImageInfo = document.getElementById('modalImageInfo');
            
            if (modalImage) {
                modalImage.src = imageData.url;
                modalImage.alt = imageData.name;
            }
            if (modalImageInfo) modalImageInfo.textContent = imageData.name;
            if (imageModal) imageModal.classList.add('active');
        }

        function closeImageModal() {
            const imageModal = document.getElementById('imageModal');
            if (imageModal) imageModal.classList.remove('active');
        }

        // === 유틸리티 ===
        function escapeHtml(text) {
            const div = document.createElement('div');
            div.textContent = text;
            return div.innerHTML;
        }

        // === 이벤트 리스너 ===
        function initEventListeners() {
            const overlay = document.getElementById('overlay');
            if (overlay) {
                overlay.addEventListener('click', (e) => {
                    if (e.target.id === 'overlay') closeWindow();
                });
            }

            const imageModal = document.getElementById('imageModal');
            if (imageModal) {
                imageModal.addEventListener('click', (e) => {
                    if (e.target === imageModal) closeImageModal();
                });
            }

            document.addEventListener('keydown', (e) => {
                if (e.key === 'Escape') {
                    const imageModal = document.getElementById('imageModal');
                    const postModal = document.getElementById('postModal');
                    
                    if (imageModal && imageModal.classList.contains('active')) {
                        closeImageModal();
                    } else if (postModal && postModal.classList.contains('active')) {
                        closePostModal();
                    } else {
                        closeWindow();
                    }
                }
            });

            const adminPasswordInput = document.getElementById('adminPasswordInput');
            if (adminPasswordInput) {
                adminPasswordInput.addEventListener('keydown', (e) => {
                    if (e.key === 'Enter') adminLogin();
                });
            }

            document.querySelectorAll('.desktop-icon').forEach((icon) => {
                icon.addEventListener('click', () => {
                    const type = icon.dataset.type;
                    showWindow(type);
                });
            });
        }

        // === 전역 함수 등록 ===
        window.showWindow = showWindow;
        window.closeWindow = closeWindow;
        window.closePostModal = closePostModal;
        window.showImageModal = showImageModal;
        window.closeImageModal = closeImageModal;
        window.adminLogin = adminLogin;

        // === 초기화 ===
        window.addEventListener('load', () => {
            console.log('🎉 초시공 네트워크 메인 초기화 시작...');
            loadDemoData();
            initEventListeners();
            updatePostList();
            updateGallery();
            console.log('✅ 메인 초기화 완료!');
            console.log('📊 현재 데이터:', posts.length + '개 글, ' + images.length + '개 이미지');
        });
    </script>
</body>
</html>
