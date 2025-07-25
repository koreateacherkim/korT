<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>배드민턴 대회 대진표 프로그램</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- SheetJS (js-xlsx) for Excel import -->
    <script src="https://unpkg.com/xlsx/dist/xlsx.full.min.js"></script>
    <style>
        body {
            font-family: "Inter", sans-serif;
            background-color: #f0f4f8;
        }
        /* Custom scrollbar for player list */
        .player-list-container::-webkit-scrollbar {
            width: 8px;
        }
        .player-list-container::-webkit-scrollbar-track {
            background: #e2e8f0;
            border-radius: 10px;
        }
        .player-list-container::-webkit-scrollbar-thumb {
            background: #cbd5e1;
            border-radius: 10px;
        }
        .player-list-container::-webkit-scrollbar-thumb:hover {
            background: #94a3b8;
        }
    </style>
</head>
<body class="p-4 bg-gray-100 min-h-screen flex flex-col items-center">
    <div class="container max-w-6xl mx-auto bg-white p-8 rounded-xl shadow-lg space-y-8">
        <h1 class="text-4xl font-extrabold text-center text-blue-800 mb-8">🏸 배드민턴 대회 대진표</h1>

        <!-- Player Input Section -->
        <section class="bg-blue-50 p-6 rounded-lg shadow-md">
            <h2 class="text-2xl font-bold text-blue-700 mb-6">선수 등록</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <!-- Manual Input -->
                <div class="bg-white p-5 rounded-lg shadow-sm border border-blue-200">
                    <h3 class="text-xl font-semibold text-blue-600 mb-4">수동 입력</h3>
                    <div class="space-y-4">
                        <div>
                            <label for="playerName" class="block text-sm font-medium text-gray-700">이름</label>
                            <input type="text" id="playerName" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" placeholder="선수 이름">
                        </div>
                        <div>
                            <label for="playerGender" class="block text-sm font-medium text-gray-700">성별</label>
                            <select id="playerGender" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm">
                                <option value="">선택</option>
                                <option value="Male">남성</option>
                                <option value="Female">여성</option>
                            </select>
                        </div>
                        <div>
                            <label for="playerAge" class="block text-sm font-medium text-gray-700">나이대</label>
                            <select id="playerAge" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm">
                                <option value="">선택</option>
                                <option value="20s">20대</option>
                                <option value="30s">30대</option>
                                <option value="40s">40대</option>
                                <option value="45s">45대</option>
                                <option value="50s">50대</option>
                                <option value="60s">60대</option>
                                <option value="70s">70대</option>
                            </select>
                        </div>
                        <div>
                            <label for="playerSkill" class="block text-sm font-medium text-gray-700">급수</label>
                            <select id="playerSkill" class="mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm">
                                <option value="">선택</option>
                                <option value="A">A급</option>
                                <option value="B">B급</option>
                                <option value="C">C급</option>
                                <option value="D">D급</option>
                                <option value="E">E급</option>
                            </select>
                        </div>
                        <button id="addPlayerBtn" class="w-full bg-blue-600 text-white py-2 px-4 rounded-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2 transition duration-200 ease-in-out shadow-md">선수 추가</button>
                    </div>
                </div>

                <!-- Excel Input -->
                <div class="bg-white p-5 rounded-lg shadow-sm border border-blue-200">
                    <h3 class="text-xl font-semibold text-blue-600 mb-4">엑셀 파일 일괄 입력</h3>
                    <p class="text-sm text-gray-600 mb-4">
                        엑셀 파일은 다음 열을 포함해야 합니다: <code class="font-mono">이름</code>, <code class="font-mono">성별</code>, <code class="font-mono">나이대</code>, <code class="font-mono">급수</code>.
                        <br>성별은 '남성' 또는 '여성', 나이대는 '20대', '30대' 등으로, 급수는 'A', 'B' 등으로 정확히 입력해주세요.
                    </p>
                    <input type="file" id="excelFileInput" accept=".xlsx, .xls" class="block w-full text-sm text-gray-500
                        file:mr-4 file:py-2 file:px-4
                        file:rounded-md file:border-0
                        file:text-sm file:font-semibold
                        file:bg-blue-50 file:text-blue-700
                        hover:file:bg-blue-100 transition duration-200 ease-in-out">
                    <button id="importExcelBtn" class="mt-4 w-full bg-green-600 text-white py-2 px-4 rounded-md hover:bg-green-700 focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-offset-2 transition duration-200 ease-in-out shadow-md">엑셀에서 선수 가져오기</button>
                    <a href="#" id="downloadSampleExcel" class="mt-4 block text-center text-blue-500 hover:underline text-sm">샘플 엑셀 파일 다운로드</a>
                </div>
            </div>
            <div id="messageBox" class="mt-6 p-3 rounded-md text-center hidden"></div>
        </section>

        <!-- Player List Section -->
        <section class="bg-gray-50 p-6 rounded-lg shadow-md">
            <h2 class="text-2xl font-bold text-gray-700 mb-6">등록된 선수 목록 (<span id="playerCount">0</span>명)</h2>
            <div class="flex justify-end mb-4">
                <button id="clearPlayersBtn" class="bg-red-500 text-white py-2 px-4 rounded-md hover:bg-red-600 focus:outline-none focus:ring-2 focus:ring-red-500 focus:ring-offset-2 transition duration-200 ease-in-out shadow-md">모든 선수 초기화</button>
            </div>
            <div class="overflow-x-auto player-list-container max-h-96">
                <table class="min-w-full bg-white rounded-lg shadow-sm">
                    <thead>
                        <tr class="bg-gray-200 text-gray-600 uppercase text-sm leading-normal">
                            <th class="py-3 px-6 text-left rounded-tl-lg">이름</th>
                            <th class="py-3 px-6 text-left">성별</th>
                            <th class="py-3 px-6 text-left">나이대</th>
                            <th class="py-3 px-6 text-left">급수</th>
                            <th class="py-3 px-6 text-left">상태</th>
                            <th class="py-3 px-6 text-left rounded-tr-lg">액션</th>
                        </tr>
                    </thead>
                    <tbody id="playerList" class="text-gray-700 text-sm font-light">
                        <!-- Player rows will be inserted here -->
                    </tbody>
                </table>
            </div>
        </section>

        <!-- Match Generation and Courts Section -->
        <section class="bg-purple-50 p-6 rounded-lg shadow-md">
            <h2 class="text-2xl font-bold text-purple-700 mb-6">경기 매칭 및 코트 배정</h2>
            <div class="flex flex-col sm:flex-row justify-center gap-4 mb-8">
                <button id="generateMatchesBtn" class="bg-purple-600 text-white py-3 px-6 rounded-md text-lg font-semibold hover:bg-purple-700 focus:outline-none focus:ring-2 focus:ring-purple-500 focus:ring-offset-2 transition duration-200 ease-in-out shadow-lg">
                    경기 매칭 시작
                </button>
                <button id="endRoundBtn" class="bg-yellow-600 text-white py-3 px-6 rounded-md text-lg font-semibold hover:bg-yellow-700 focus:outline-none focus:ring-2 focus:ring-yellow-500 focus:ring-offset-2 transition duration-200 ease-in-out shadow-lg opacity-50 cursor-not-allowed" disabled>
                    라운드 종료 (선수 휴식)
                </button>
            </div>

            <div id="courtsContainer" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                <!-- Courts will be dynamically generated here -->
                <div class="court-card bg-white p-5 rounded-lg shadow-md border border-purple-200">
                    <h3 class="text-xl font-semibold text-purple-600 mb-3">코트 1</h3>
                    <p class="text-gray-500 text-sm mb-2">현재 경기 없음</p>
                    <ul class="list-disc list-inside text-gray-700 space-y-1"></ul>
                </div>
                <div class="court-card bg-white p-5 rounded-lg shadow-md border border-purple-200">
                    <h3 class="text-xl font-semibold text-purple-600 mb-3">코트 2</h3>
                    <p class="text-gray-500 text-sm mb-2">현재 경기 없음</p>
                    <ul class="list-disc list-inside text-gray-700 space-y-1"></ul>
                </div>
                <div class="court-card bg-white p-5 rounded-lg shadow-md border border-purple-200">
                    <h3 class="text-xl font-semibold text-purple-600 mb-3">코트 3</h3>
                    <p class="text-gray-500 text-sm mb-2">현재 경기 없음</p>
                    <ul class="list-disc list-inside text-gray-700 space-y-1"></ul>
                </div>
                <div class="court-card bg-white p-5 rounded-lg shadow-md border border-purple-200">
                    <h3 class="text-xl font-semibold text-purple-600 mb-3">코트 4</h3>
                    <p class="text-gray-500 text-sm mb-2">현재 경기 없음</p>
                    <ul class="list-disc list-inside text-gray-700 space-y-1"></ul>
                </div>
            </div>
        </section>
    </div>

    <script>
        // Player data array
        let players = [];
        let currentRound = 0; // To track rounds for lastPlayed logic
        const MAX_COURTS = 4;

        // DOM elements
        const playerNameInput = document.getElementById('playerName');
        const playerGenderSelect = document.getElementById('playerGender');
        const playerAgeSelect = document.getElementById('playerAge');
        const playerSkillSelect = document.getElementById('playerSkill');
        const addPlayerBtn = document.getElementById('addPlayerBtn');
        const excelFileInput = document.getElementById('excelFileInput');
        const importExcelBtn = document.getElementById('importExcelBtn');
        const downloadSampleExcel = document.getElementById('downloadSampleExcel');
        const playerListTableBody = document.getElementById('playerList');
        const playerCountSpan = document.getElementById('playerCount');
        const clearPlayersBtn = document.getElementById('clearPlayersBtn');
        const generateMatchesBtn = document.getElementById('generateMatchesBtn');
        const endRoundBtn = document.getElementById('endRoundBtn');
        const courtsContainer = document.getElementById('courtsContainer');
        const messageBox = document.getElementById('messageBox');

        // Mapping for strength calculation
        const ageMap = { '20s': 1, '30s': 2, '40s': 3, '45s': 4, '50s': 5, '60s': 6, '70s': 7 };
        const skillMap = { 'A': 5, 'B': 4, 'C': 3, 'D': 2, 'E': 1 };
        const genderMap = { 'Male': 0, 'Female': 1 }; // For tie-breaking or specific mixed doubles logic

        // --- Utility Functions ---

        // Generate a unique ID for players
        function generateUniqueId() {
            return '_' + Math.random().toString(36).substr(2, 9);
        }

        // Show message box
        function showMessage(message, type = 'info') {
            messageBox.textContent = message;
            messageBox.className = `mt-6 p-3 rounded-md text-center ${type === 'error' ? 'bg-red-100 text-red-700' : 'bg-green-100 text-green-700'} block`;
            setTimeout(() => {
                messageBox.classList.add('hidden');
            }, 5000);
        }

        // Calculate player strength based on skill and age
        function calculatePlayerStrength(player) {
            // Skill has higher weight (e.g., 10 times age group value)
            // Higher skill value (A=5) means higher strength.
            // Higher age group value (70s=7) means higher strength (can be adjusted if older implies less strength)
            // For matching similar skill, we want players with similar strength scores.
            // Let's make skill contribute more significantly.
            const skillValue = skillMap[player.skillLevel] || 0;
            const ageValue = ageMap[player.ageGroup] || 0;
            return (skillValue * 100) + (ageValue * 10) + (genderMap[player.gender] || 0); // Gender as minor tie-breaker
        }

        // Update player list in the UI
        function renderPlayerList() {
            playerListTableBody.innerHTML = '';
            players.forEach(player => {
                const row = playerListTableBody.insertRow();
                row.className = 'border-b border-gray-200 hover:bg-gray-100';
                row.innerHTML = `
                    <td class="py-3 px-6 text-left whitespace-nowrap">${player.name}</td>
                    <td class="py-3 px-6 text-left">${player.gender === 'Male' ? '남성' : '여성'}</td>
                    <td class="py-3 px-6 text-left">${player.ageGroup}대</td>
                    <td class="py-3 px-6 text-left">${player.skillLevel}급</td>
                    <td class="py-3 px-6 text-left">
                        <span class="px-2 py-1 rounded-full text-xs font-semibold ${player.isPlaying ? 'bg-yellow-200 text-yellow-800' : (player.lastPlayed === currentRound ? 'bg-gray-200 text-gray-800' : 'bg-blue-100 text-blue-800')}">
                            ${player.isPlaying ? '경기 중' : (player.lastPlayed === currentRound ? '휴식 중' : '대기 중')}
                        </span>
                    </td>
                    <td class="py-3 px-6 text-left">
                        <button data-id="${player.id}" class="delete-player-btn bg-red-400 text-white px-3 py-1 rounded-md text-xs hover:bg-red-500 transition duration-200 ease-in-out">삭제</button>
                    </td>
                `;
            });
            playerCountSpan.textContent = players.length;

            // Attach event listeners for delete buttons
            document.querySelectorAll('.delete-player-btn').forEach(button => {
                button.addEventListener('click', (event) => {
                    const playerIdToDelete = event.target.dataset.id;
                    players = players.filter(p => p.id !== playerIdToDelete);
                    renderPlayerList();
                    showMessage('선수가 삭제되었습니다.', 'info');
                });
            });
        }

        // Clear all courts UI
        function clearCourtsUI() {
            for (let i = 1; i <= MAX_COURTS; i++) {
                const courtCard = courtsContainer.children[i - 1];
                const statusParagraph = courtCard.querySelector('p');
                const playerListUl = courtCard.querySelector('ul');
                statusParagraph.textContent = '현재 경기 없음';
                playerListUl.innerHTML = '';
            }
        }

        // --- Event Listeners ---

        // Add Player button click
        addPlayerBtn.addEventListener('click', () => {
            const name = playerNameInput.value.trim();
            const gender = playerGenderSelect.value;
            const ageGroup = playerAgeSelect.value;
            const skillLevel = playerSkillSelect.value;

            if (!name || !gender || !ageGroup || !skillLevel) {
                showMessage('모든 선수 정보를 입력해주세요.', 'error');
                return;
            }

            const newPlayer = {
                id: generateUniqueId(),
                name,
                gender,
                ageGroup,
                skillLevel,
                strength: calculatePlayerStrength({ ageGroup, skillLevel, gender }),
                lastPlayed: 0, // Round number when they last played
                isPlaying: false
            };
            players.push(newPlayer);
            renderPlayerList();
            showMessage(`${name} 선수가 추가되었습니다.`, 'success');

            // Clear form
            playerNameInput.value = '';
            playerGenderSelect.value = '';
            playerAgeSelect.value = '';
            playerSkillSelect.value = '';
        });

        // Import Excel button click
        importExcelBtn.addEventListener('click', () => {
            const file = excelFileInput.files[0];
            if (!file) {
                showMessage('엑셀 파일을 선택해주세요.', 'error');
                return;
            }

            const reader = new FileReader();
            reader.onload = (e) => {
                const data = new Uint8Array(e.target.result);
                const workbook = XLSX.read(data, { type: 'array' });
                const firstSheetName = workbook.SheetNames[0];
                const worksheet = workbook.Sheets[firstSheetName];
                const json = XLSX.utils.sheet_to_json(worksheet);

                let importedCount = 0;
                json.forEach(row => {
                    const name = row['이름']?.toString().trim();
                    const gender = row['성별']?.toString().trim();
                    const ageGroup = row['나이대']?.toString().trim();
                    const skillLevel = row['급수']?.toString().trim();

                    // Validate data
                    const isValidGender = ['남성', '여성'].includes(gender);
                    const isValidAgeGroup = ['20대', '30대', '40대', '45대', '50대', '60대', '70대'].includes(ageGroup);
                    const isValidSkill = ['A', 'B', 'C', 'D', 'E'].includes(skillLevel);

                    if (name && isValidGender && isValidAgeGroup && isValidSkill) {
                        const newPlayer = {
                            id: generateUniqueId(),
                            name,
                            gender: gender === '남성' ? 'Male' : 'Female',
                            ageGroup: ageGroup.replace('대', 's'), // Convert '20대' to '20s'
                            skillLevel,
                            strength: calculatePlayerStrength({ ageGroup: ageGroup.replace('대', 's'), skillLevel, gender: gender === '남성' ? 'Male' : 'Female' }),
                            lastPlayed: 0,
                            isPlaying: false
                        };
                        players.push(newPlayer);
                        importedCount++;
                    } else {
                        console.warn('Skipping invalid row:', row);
                    }
                });
                renderPlayerList();
                showMessage(`${importedCount}명의 선수가 엑셀에서 성공적으로 가져와졌습니다.`, 'success');
                excelFileInput.value = ''; // Clear the file input
            };
            reader.readAsArrayBuffer(file);
        });

        // Download Sample Excel
        downloadSampleExcel.addEventListener('click', (e) => {
            e.preventDefault();
            const ws_data = [
                ["이름", "성별", "나이대", "급수"],
                ["홍길동", "남성", "30대", "B"],
                ["김영희", "여성", "40대", "C"],
                ["이철수", "남성", "20대", "A"]
            ];
            const ws = XLSX.utils.aoa_to_sheet(ws_data);
            const wb = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(wb, ws, "선수목록");
            XLSX.writeFile(wb, "배드민턴_선수_샘플.xlsx");
        });

        // Clear All Players button click
        clearPlayersBtn.addEventListener('click', () => {
            if (confirm('정말로 모든 선수를 초기화하시겠습니까?')) { // Using confirm for simplicity, would use custom modal in production
                players = [];
                currentRound = 0;
                renderPlayerList();
                clearCourtsUI();
                showMessage('모든 선수가 초기화되었습니다.', 'info');
                endRoundBtn.disabled = true;
                endRoundBtn.classList.add('opacity-50', 'cursor-not-allowed');
            }
        });

        // --- Match Generation Logic ---

        function generateMatches() {
            if (players.length < 4) {
                showMessage('경기를 생성하려면 최소 4명 이상의 선수가 필요합니다.', 'error');
                return;
            }

            // Increment round number
            currentRound++;

            // Reset isPlaying status for all players from previous round
            players.forEach(p => {
                if (p.isPlaying) {
                    p.isPlaying = false;
                }
            });

            // Clear previous matches from UI
            clearCourtsUI();

            // Enable End Round button
            endRoundBtn.disabled = false;
            endRoundBtn.classList.remove('opacity-50', 'cursor-not-allowed');

            let availablePlayers = players.filter(p => !p.isPlaying && p.lastPlayed !== currentRound);

            // Sort available players:
            // 1. Prioritize players who haven't played for the longest time (smaller lastPlayed value)
            // 2. Then by strength (descending, to group stronger players together initially)
            availablePlayers.sort((a, b) => {
                if (a.lastPlayed !== b.lastPlayed) {
                    return a.lastPlayed - b.lastPlayed;
                }
                return b.strength - a.strength; // Stronger players first
            });

            let matches = [];
            let playersOnCourtThisRound = new Set();

            for (let courtIndex = 0; courtIndex < MAX_COURTS; courtIndex++) {
                // Filter out players already selected for this round
                let currentAvailable = availablePlayers.filter(p => !playersOnCourtThisRound.has(p.id));

                if (currentAvailable.length < 4) {
                    // Not enough players for another match
                    break;
                }

                // Try to find the best 4 players for this court
                // This is a simplified greedy approach. For a truly optimal solution,
                // a more complex algorithm (e.g., min-cost max-flow or a genetic algorithm)
                // would be needed, but for a club setting, this should be sufficient.

                // Take the top N players (e.g., 8-12) from the sorted list to consider for the current match
                // This helps in finding better matches than just taking the first 4.
                const candidates = currentAvailable.slice(0, Math.min(currentAvailable.length, 12)); // Consider up to 12 candidates

                let bestMatch = null;
                let minDiff = Infinity;

                // Iterate through all combinations of 4 players from candidates
                // This can be computationally intensive for large candidate pools.
                // For 12 candidates, C(12,4) = 495 combinations.
                for (let i = 0; i < candidates.length; i++) {
                    for (let j = i + 1; j < candidates.length; j++) {
                        for (let k = j + 1; k < candidates.length; k++) {
                            for (let l = k + 1; l < candidates.length; l++) {
                                const p1 = candidates[i];
                                const p2 = candidates[j];
                                const p3 = candidates[k];
                                const p4 = candidates[l];

                                // Check if any of these players are already selected for another court in this round
                                if (playersOnCourtThisRound.has(p1.id) || playersOnCourtThisRound.has(p2.id) ||
                                    playersOnCourtThisRound.has(p3.id) || playersOnCourtThisRound.has(p4.id)) {
                                    continue;
                                }

                                // Try all possible team pairings for these 4 players
                                const pairings = [
                                    [[p1, p2], [p3, p4]],
                                    [[p1, p3], [p2, p4]],
                                    [[p1, p4], [p2, p3]]
                                ];

                                for (const pairing of pairings) {
                                    const teamA = pairing[0];
                                    const teamB = pairing[1];

                                    const teamAStrength = teamA[0].strength + teamA[1].strength;
                                    const teamBStrength = teamB[0].strength + teamB[1].strength;
                                    const matchStrengthDiff = Math.abs(teamAStrength - teamBStrength);

                                    // Prioritize gender balance for mixed doubles if strengths are similar
                                    // This is a simple heuristic; more complex logic might be needed for strict mixed doubles rules.
                                    const teamAGenderMix = (teamA[0].gender !== teamA[1].gender);
                                    const teamBGenderMix = (teamB[0].gender !== teamB[1].gender);
                                    let genderBonus = 0;
                                    if (teamAGenderMix && teamBGenderMix) {
                                        genderBonus = -10; // Small bonus for mixed doubles matches
                                    } else if (teamAGenderMix || teamBGenderMix) {
                                        genderBonus = -5; // Small bonus for at least one mixed team
                                    }

                                    const totalDiff = matchStrengthDiff + genderBonus; // Incorporate gender preference

                                    if (totalDiff < minDiff) {
                                        minDiff = totalDiff;
                                        bestMatch = { players: [p1, p2, p3, p4], teamA: teamA, teamB: teamB };
                                    }
                                }
                            }
                        }
                    }
                }

                if (bestMatch) {
                    matches.push(bestMatch);
                    bestMatch.players.forEach(p => {
                        playersOnCourtThisRound.add(p.id);
                        // Update player status in the main players array
                        const playerInMainArray = players.find(mainP => mainP.id === p.id);
                        if (playerInMainArray) {
                            playerInMainArray.isPlaying = true;
                            playerInMainArray.lastPlayed = currentRound;
                        }
                    });
                } else {
                    // No suitable match found with remaining players
                    break;
                }
            }

            // Render matches to UI
            matches.forEach((match, index) => {
                const courtCard = courtsContainer.children[index];
                const statusParagraph = courtCard.querySelector('p');
                const playerListUl = courtCard.querySelector('ul');

                statusParagraph.textContent = `경기 중 (라운드 ${currentRound})`;
                playerListUl.innerHTML = `
                    <li><strong>${match.teamA[0].name} & ${match.teamA[1].name}</strong> (VS) </li>
                    <li><strong>${match.teamB[0].name} & ${match.teamB[1].name}</strong></li>
                `;
            });

            renderPlayerList(); // Update player status in the list
            if (matches.length > 0) {
                showMessage(`${matches.length}개의 경기가 성공적으로 매칭되었습니다.`, 'success');
            } else {
                showMessage('매칭할 수 있는 경기가 없습니다. 선수 수를 확인하거나 다음 라운드를 기다려주세요.', 'error');
            }
        }

        generateMatchesBtn.addEventListener('click', generateMatches);

        endRoundBtn.addEventListener('click', () => {
            // Mark all players who were playing as resting (lastPlayed = currentRound)
            // and clear their isPlaying status
            players.forEach(p => {
                if (p.isPlaying) {
                    p.isPlaying = false;
                    // p.lastPlayed is already set to currentRound during match generation
                }
            });
            renderPlayerList();
            clearCourtsUI();
            showMessage('현재 라운드가 종료되었습니다. 선수들이 휴식 중입니다.', 'info');
            endRoundBtn.disabled = true;
            endRoundBtn.classList.add('opacity-50', 'cursor-not-allowed');
        });

        // Initial render
        renderPlayerList();
        clearCourtsUI();
    </script>
</body>
</html>
