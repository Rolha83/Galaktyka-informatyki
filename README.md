<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Informatyka Klasa 4 – Platforma Edukacyjna</title>
    <style>
        :root {
            --primary: #2C3E50;
            --accent: #3498DB;
            --success: #2ECC71;
            --warning: #F39C12;
            --danger: #E74C3C;
            --creative: #9B59B6;
            --bg: #F4F6F9;
            --card: #FFFFFF;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            margin: 0;
            padding: 0;
            color: #333;
        }

        header {
            background: var(--primary);
            color: white;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.15);
        }

        header h1 { margin: 0; font-size: 1.4em; }

        .user-panel {
            background: rgba(255,255,255,0.2);
            padding: 8px 15px;
            border-radius: 8px;
        }

        select {
            padding: 6px 12px;
            border-radius: 6px;
            border: none;
            font-weight: bold;
            cursor: pointer;
        }

        .main-layout {
            display: flex;
            max-width: 1200px;
            margin: 20px auto;
            gap: 20px;
            padding: 0 15px;
        }

        nav.sidebar {
            width: 280px;
            background: var(--card);
            border-radius: 12px;
            padding: 15px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            height: fit-content;
        }

        nav.sidebar h3 {
            margin-top: 0;
            color: var(--primary);
            border-bottom: 2px solid #ECF0F1;
            padding-bottom: 10px;
        }

        .nav-btn {
            display: block;
            width: 100%;
            text-align: left;
            background: none;
            border: none;
            padding: 12px 10px;
            margin: 5px 0;
            border-radius: 8px;
            cursor: pointer;
            font-size: 0.95em;
            color: #555;
            transition: all 0.2s;
        }

        .nav-btn:hover, .nav-btn.active {
            background: var(--accent);
            color: white;
            font-weight: bold;
        }

        main.content {
            flex: 1;
            background: var(--card);
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
        }

        .module { display: none; }
        .module.active { display: block; }

        .task-card {
            border: 1px solid #E2E8F0;
            border-left: 5px solid var(--accent);
            border-radius: 8px;
            padding: 18px;
            margin-bottom: 20px;
            background: #FAFAFA;
        }

        .task-card.creative-card {
            border-left-color: var(--creative);
            background: #FAF5FF;
        }

        .badge {
            display: inline-block;
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 0.8em;
            font-weight: bold;
            color: white;
            margin-bottom: 10px;
        }

        .b-easy { background: var(--success); }
        .b-medium { background: var(--warning); }
        .b-creative { background: var(--creative); }

        .options label {
            display: block;
            background: white;
            padding: 10px 14px;
            margin: 6px 0;
            border-radius: 6px;
            border: 1px solid #CBD5E1;
            cursor: pointer;
        }

        .options label:hover { background: #F1F5F9; }

        textarea, input[type="text"] {
            width: 100%;
            padding: 10px;
            border-radius: 6px;
            border: 1px solid #CBD5E1;
            box-sizing: border-box;
            margin-top: 8px;
            font-family: inherit;
        }

        .btn-submit {
            background: var(--accent);
            color: white;
            font-size: 1.1em;
            font-weight: bold;
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            width: 100%;
            margin-top: 15px;
        }

        .btn-submit:hover { background: #2980B9; }

        .result-box {
            display: none;
            margin-top: 25px;
            padding: 20px;
            border-radius: 10px;
            background: #F8FAFC;
            border: 2px solid #CBD5E1;
        }

        .score { font-size: 2em; font-weight: bold; text-align: center; }
    </style>
</head>
<body>

<header>
    <h1>Informatyka Klasa 4 – Portal Lekcyjny</h1>
    <div class="user-panel">
        <label for="studentSelect"><strong>Uczeń: </strong></label>
        <select id="studentSelect">
            <option value="">-- Wybierz kod --</option>
        </select>
    </div>
</header>

<div class="main-layout">
    <nav class="sidebar">
        <h3>Spis Lekcji</h3>
        <button class="nav-btn active" onclick="showModule('m1', this)">1. Bezpieczni w sieci</button>
        <button class="nav-btn" onclick="showModule('m2', this)">2. Sprzęt i BHP</button>
        <button class="nav-btn" onclick="showModule('m3', this)">3. Grafika w Paint</button>
    </nav>

    <main class="content">

        <!-- TEMAT LEKCJI I OPRACOWANIE STRON 34–40 -->
<div class="lesson-section">
  <h2>Lekcja 1: Bezpieczni w cyfrowym świecie (str. 34–40)</h2>
  <p><strong>Cel lekcji:</strong> Nauczysz się rozpoznawać zagrożenia w internecie, chronić swoje dane osobiste oraz tworzyć bezpieczne hasła.</p>
  <p><em>Przeczytaj materiał w podręczniku i wykonaj poniższe zadania o różnym stopniu trudności.</em></p>

  <!-- ================= POZIOM 1: PODSTAWY ================= -->
  <div class="level-box level-1" style="border: 2px solid #28a745; padding: 15px; margin-bottom: 20px; border-radius: 8px;">
    <span class="badge" style="background: #28a745; color: white; padding: 5px 10px; border-radius: 4px; font-weight: bold;">Poziom 1: Podstawy (Pytania testowe)</span>

    <div class="question-block" style="margin-top: 15px;">
      <h3>1. Phishing / Wyłudzanie danych (str. 35)</h3>
      <p>Po czym najczęściej rozpoznasz niebezpieczną wiadomość e-mail lub SMS?</p>
      <label><input type="radio" name="q1" value="a"> Informuje o wygranej w konkursie, w którym nie brało się udziału</label><br>
      <label><input type="radio" name="q1" value="b"> Jest napisana przez kolegę z klasy</label><br>
      <label><input type="radio" name="q1" value="c"> Zawiera plan lekcji na jutrzejszy dzień</label>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>2. Pojęcie Deepfake (str. 36)</h3>
      <p>Co oznacza pojęcie Deepfake?</p>
      <label><input type="radio" name="q2" value="a"> Trudną grę zręcznościową dla młodzieży</label><br>
      <label><input type="radio" name="q2" value="b"> Fałszywe, ale bardzo realistyczne zdjęcie, film lub nagranie głosu stworzone przez komputer</label><br>
      <label><input type="radio" name="q2" value="c"> Darmowy program do rysowania grafiki</label>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>3. Bezpieczne hasło (str. 38)</h3>
      <p>Jaka jest zalecana minimalna długość silnego hasła według podręcznika?</p>
      <label><input type="radio" name="q3" value="a"> Co najmniej 6 znaków</label><br>
      <label><input type="radio" name="q3" value="b"> Co najmniej 14 znaków</label><br>
      <label><input type="radio" name="q3" value="c"> Dokładnie 8 cyfr</label>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>4. Bezpieczne połączenie https:// (str. 37)</h3>
      <p>Co oznacza kłódka i adres zaczynający się od https://?</p>
      <label><input type="radio" name="q4" value="a"> Połączenie ze stroną jest szyfrowane</label><br>
      <label><input type="radio" name="q4" value="b"> Strona w 100% nie zawiera żadnych oszustw</label><br>
      <label><input type="radio" name="q4" value="c"> Strona jest przeznaczona tylko dla nauczycieli</label>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>5. Fake News (str. 36)</h3>
      <p>Czym są tzw. fake newsy?</p>
      <label><input type="radio" name="q5" value="a"> Najnowszymi wiadomościami sportowymi</label><br>
      <label><input type="radio" name="q5" value="b"> Fałszywymi informacjami tworzonymi celowo, aby wprowadzić w błąd lub wzbudzić emocje</label><br>
      <label><input type="radio" name="q5" value="c"> Ciekawostkami naukowymi z podręcznika</label>
    </div>
  </div>

  <!-- ================= POZIOM 2: ANALIZA I ROZUMIENIE ================= -->
  <div class="level-box level-2" style="border: 2px solid #ffc107; padding: 15px; margin-bottom: 20px; border-radius: 8px;">
    <span class="badge" style="background: #ffc107; color: black; padding: 5px 10px; border-radius: 4px; font-weight: bold;">Poziom 2: Analiza pojęć</span>

    <div class="question-block" style="margin-top: 15px;">
      <h3>6. Cechy podejrzenia (str. 35)</h3>
      <p>Wymień 3 cechy, po których można poznać, że otrzymana wiadomość może być próbą oszustwa:</p>
      <textarea name="q6" rows="3" style="width: 100%;" placeholder="1. ... 2. ... 3. ..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>7. Ochrona prywatności (str. 34)</h3>
      <p>Jakich 4 ważnych informacji o sobie nigdy nie wolno podawać nieznajomym w sieci?</p>
      <textarea name="q7" rows="3" style="width: 100%;" placeholder="Wpisz np. adres, szkołę..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>8. Poprawianie słabego hasła (str. 38–39)</h3>
      <p>Dlaczego hasło <code>Magda1234</code> jest łatwe do złamania? Zaproponuj, jak je zmienić na silne:</p>
      <textarea name="q8" rows="3" style="width: 100%;" placeholder="Wyjaśnij powód i podaj nową wersję hasła..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>9. Szkodliwe oprogramowanie (str. 37)</h3>
      <p>Opisz, co złego może się stać z komputerem, jeśli pobierzemy z sieci wirusa lub szkodliwy program:</p>
      <textarea name="q9" rows="3" style="width: 100%;" placeholder="Opisz skutki..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>10. Rozpoznawanie Prawdy (str. 37)</h3>
      <p>Jakie 2 pytania warto sobie zadać przed udostępnieniem dalej jakiejś informacji z internetu?</p>
      <textarea name="q10" rows="3" style="width: 100%;" placeholder="Napisz pytania kontrolne..."></textarea>
    </div>
  </div>

  <!-- ================= POZIOM 3: SYTUACJE PRAKTYCZNE ================= -->
  <div class="level-box level-3" style="border: 2px solid #fd7e14; padding: 15px; margin-bottom: 20px; border-radius: 8px;">
    <span class="badge" style="background: #fd7e14; color: white; padding: 5px 10px; border-radius: 4px; font-weight: bold;">Poziom 3: Sytuacje praktyczne</span>

    <div class="question-block" style="margin-top: 15px;">
      <h3>11. Reakcja na podejrzaną wiadomość (str. 40)</h3>
      <p>Kolega przysyła Ci wiadomość na czacie z prośbą o szybkie przesłanie kodu BLIK lub pieniędzy. Co robisz krok po kroku?</p>
      <textarea name="q11" rows="3" style="width: 100%;" placeholder="Opisz swoje postępowanie..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>12. Pomoc i numery zaufania (str. 39)</h3>
      <p>Gdzie i do kogo możesz się zgłosić, jeśli spotka Cię nieprzyjemna lub groźna sytuacja w internecie?</p>
      <textarea name="q12" rows="3" style="width: 100%;" placeholder="Wymień osoby lub numery telefonów zaufania..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>13. Tworzenie własnego szyfru / silnego hasła (str. 39)</h3>
      <p>Napisz jedno zdanie o swoim hobby, a następnie zmień je w silne hasło (usuń spacje, zmień litery na cyfry/znaki specjalne):</p>
      <textarea name="q13" rows="3" style="width: 100%;" placeholder="Zdanie: ... -> Hasło: ..."></textarea>
    </div>
  </div>

  <!-- ================= POZIOM 4: ZADANIA TWÓRCZE (DLA ZAANGAŻOWANIA) ================= -->
  <div class="level-box level-4" style="border: 2px solid #6f42c1; padding: 15px; margin-bottom: 20px; border-radius: 8px;">
    <span class="badge" style="background: #6f42c1; color: white; padding: 5px 10px; border-radius: 4px; font-weight: bold;">Poziom 4: Wyzwania twórcze</span>

    <div class="question-block" style="margin-top: 15px;">
      <h3>14. Projekt Komiksu lub Scenariusza (str. 36)</h3>
      <p>Ułóż krótki dialog (4 zdania) między Cyfrowym Detektywem a osobą, która o mały włos nie kliknęła w fałszywy link z wygraną:</p>
      <textarea name="q14" rows="4" style="width: 100%;" placeholder="Detektyw: ... / Uczeń: ..."></textarea>
    </div>

    <div class="question-block" style="margin-top: 15px;">
      <h3>15. Dekalog Bezpiecznego Internauty (str. 40)</h3>
      <p>Stwórz krótką listę 3 najważniejszych haseł ostrzegawczych, które umieściłbyś/umieściłabyś na plakacie szkolnym o bezpieczeństwie w sieci:</p>
      <textarea name="q15" rows="3" style="width: 100%;" placeholder="1. ... 2. ... 3. ..."></textarea>
    </div>
  </div>
</div>


        <!-- LEKCJA 2 -->
        <div id="m2" class="module">
            <h2>Lekcja 2: Komputer i zasady BHP</h2>
            <form id="formM2">
                <div class="task-card">
                    <span class="badge b-easy">Poziom 1</span>
                    <h3>1. Urządzenia wprowadzające</h3>
                    <p>Które urządzenie pozwala wpisywać tekst do komputera?</p>
                    <div class="options">
                        <label><input type="radio" name="m2_q1" value="A"> Monitor</label>
                        <label><input type="radio" name="m2_q1" value="B"> Klawiatura</label>
                        <label><input type="radio" name="m2_q1" value="C"> Drukarka</label>
                    </div>
                </div>

                <div class="task-card creative-card">
                    <span class="badge b-creative">Poziom 3: Zadanie Twórcze</span>
                    <h3>2. Zasady Zdrowej Pracy</h3>
                    <p>Opisz 2 zasady BHP, które chronią Twój wzrok i kręgosłup podczas pracy przy biurku:</p>
                    <textarea id="m2_q2" rows="3" placeholder="Wpisz zasady..."></textarea>
                </div>

                <button type="button" class="btn-submit" onclick="gradeM2()">Sprawdź wynik Lekcji 2</button>
            </form>

            <div id="resM2" class="result-box">
                <div id="scoreM2" class="score"></div>
                <ul id="feedbackM2"></ul>
            </div>
        </div>

        <!-- LEKCJA 3 -->
        <div id="m3" class="module">
            <h2>Lekcja 3: Edytor graficzny Paint</h2>
            <form id="formM3">
                <div class="task-card">
                    <span class="badge b-medium">Poziom 2</span>
                    <h3>1. Wypełnianie kolorem</h3>
                    <p>Jakim narzędziem zamalujesz cały zamknięty kształt w programie Paint?</p>
                    <div class="options">
                        <label><input type="radio" name="m3_q1" value="A"> Ołówek</label>
                        <label><input type="radio" name="m3_q1" value="B"> Kubełek z farbą (Wypełnienie kolorem)</label>
                        <label><input type="radio" name="m3_q1" value="C"> Gumka</label>
                    </div>
                </div>

                <div class="task-card creative-card">
                    <span class="badge b-creative">Poziom 3: Projekt</span>
                    <h3>2. Opis projektu</h3>
                    <p>Opisz pomysł na plakat „Bezpieczna Sieć”. Jakich kolorów i narzędzi z Painta użyjesz?</p>
                    <textarea id="m3_q2" rows="3" placeholder="Opisz swój projekt..."></textarea>
                </div>

                <button type="button" class="btn-submit" onclick="gradeM3()">Sprawdź wynik Lekcji 3</button>
            </form>

            <div id="resM3" class="result-box">
                <div id="scoreM3" class="score"></div>
                <ul id="feedbackM3"></ul>
            </div>
        </div>

    </main>
</div>

<script>
    const select = document.getElementById('studentSelect');
    for (let i = 1; i <= 28; i++) {
        let code = 'A' + (i < 10 ? '0' + i : i);
        let opt = document.createElement('option');
        opt.value = code;
        opt.innerText = 'Uczeń ' + code;
        select.appendChild(opt);
    }

    function showModule(modId, btn) {
        document.querySelectorAll('.module').forEach(m => m.classList.remove('active'));
        document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
        document.getElementById(modId).classList.add('active');
        btn.classList.add('active');
    }

    function checkUser() {
        const u = select.value;
        if (!u) {
            alert('Wybierz swój kod ucznia (A01–A28) z listy na górze!');
            return null;
        }
        return u;
    }

    function gradeM1() {
        const u = checkUser(); if (!u) return;
        let s = 0, w = [];
        const q1 = document.querySelector('input[name="m1_q1"]:checked');
        if (q1 && q1.value === 'A') s += 35; else w.push('Phishing (str. 35)');

        const q2 = document.querySelector('input[name="m1_q2"]:checked');
        if (q2 && q2.value === 'B') s += 35; else w.push('Deepfake i fałszywe treści (str. 36)');

        const q3 = document.getElementById('m1_q3').value.trim();
        if (q3.length >= 15) s += 30; else w.push('Zadanie twórcze: Tworzenie silnego hasła');

        showRes('resM1', 'scoreM1', 'feedbackM1', s, w, u);
    }

    function gradeM2() {
        const u = checkUser(); if (!u) return;
        let s = 0, w = [];
        const q1 = document.querySelector('input[name="m2_q1"]:checked');
        if (q1 && q1.value === 'B') s += 50; else w.push('Sprzęt komputerowy');

        const q2 = document.getElementById('m2_q2').value.trim();
        if (q2.length >= 15) s += 50; else w.push('Zadanie twórcze: Zasady BHP');

        showRes('resM2', 'scoreM2', 'feedbackM2', s, w, u);
    }

    function gradeM3() {
        const u = checkUser(); if (!u) return;
        let s = 0, w = [];
        const q1 = document.querySelector('input[name="m3_q1"]:checked');
        if (q1 && q1.value === 'B') s += 50; else w.push('Narzędzia malarskie w Paint');

        const q2 = document.getElementById('m3_q2').value.trim();
        if (q2.length >= 15) s += 50; else w.push('Zadanie twórcze: Projekt plakatu');

        showRes('resM3', 'scoreM3', 'feedbackM3', s, w, u);
    }

    function showRes(boxId, scoreId, listId, score, weak, student) {
        document.getElementById(boxId).style.display = 'block';
        const sc = document.getElementById(scoreId);
        sc.innerText = `Uczeń ${student} – Wynik: ${score}%`;
        sc.style.color = score >= 70 ? '#2ECC71' : '#E74C3C';

        const list = document.getElementById(listId);
        list.innerHTML = '';
        if (weak.length === 0) {
            list.innerHTML = '<li style="color: green;"><strong>Świetnie!</strong> Opanowałeś cały materiał tej lekcji!</li>';
        } else {
            let h = document.createElement('li');
            h.innerHTML = '<strong>Powtórz następujące zagadnienia:</strong>';
            list.appendChild(h);
            weak.forEach(item => {
                let li = document.createElement('li');
                li.style.color = '#C0392B';
                li.innerText = '• ' + item;
                list.appendChild(li);
            });
        }
    }
</script>
<!-- Przycisk do sprawdzania pytań testowych -->
<button onclick="sprawdzTest()" style="padding: 10px 20px; font-size: 16px; cursor: pointer; background-color: #007bff; color: white; border: none; border-radius: 5px;">Sprawdź odpowiedzi z Poziomu 1</button>

<p id="wynik-testu" style="font-weight: bold; font-size: 18px; margin-top: 15px;"></p>

<script>
function sprawdzTest() {
  // Poprawne odpowiedzi do Poziomu 1
  const poprawne = {
    q1: "a",
    q2: "b",
    q3: "b",
    q4: "a",
    q5: "b"
  };

  let punkty = 0;
  let lacznie = 5;

  for (let q in poprawne) {
    let zaznaczona = document.querySelector(`input[name="${q}"]:checked`);
    if (zaznaczona && zaznaczona.value === poprawne[q]) {
      punkty++;
    }
  }

  document.getElementById("wynik-testu").innerText = `Twój wynik z części testowej: ${punkty} / ${lacznie} pkt.`;
}
</script>


</body>
</html>
