
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Informatyka Kl. 4 – Bezpieczni w cyfrowym świecie</title>
    <style>
        :root {
            --primary: #2980b9;
            --secondary: #3498db;
            --success: #2ecc71;
            --warning: #e67e22;
            --danger: #e74c3c;
            --bg: #f4f7f6;
            --card: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background-color: var(--bg);
            margin: 0;
            padding: 20px;
            color: #2c3e50;
        }

        .container {
            max-width: 850px;
            margin: 0 auto;
            background: var(--card);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        h1 { text-align: center; color: #2c3e50; margin-bottom: 5px; }
        .subtitle { text-align: center; color: #7f8c8d; margin-bottom: 25px; font-weight: 500; }

        .login-section {
            background: #e8f4f8;
            padding: 18px;
            border-radius: 10px;
            text-align: center;
            margin-bottom: 25px;
            border: 2px solid var(--secondary);
        }

        select {
            font-size: 1.05em;
            padding: 8px 12px;
            border-radius: 6px;
            border: 1px solid #bdc3c7;
            margin-left: 10px;
            cursor: pointer;
        }

        .task-card {
            border: 1px solid #e0e0e0;
            border-left: 5px solid var(--secondary);
            border-radius: 8px;
            padding: 18px;
            margin-bottom: 20px;
            background: #fafafa;
        }

        .badge {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 0.8em;
            font-weight: bold;
            color: white;
            margin-bottom: 8px;
        }

        .easy { background-color: #27ae60; }
        .medium { background-color: #f39c12; }
        .hard { background-color: #8e44ad; }

        .options label {
            display: block;
            background: white;
            padding: 10px 14px;
            margin: 6px 0;
            border-radius: 6px;
            border: 1px solid #dcdde1;
            cursor: pointer;
            transition: background 0.2s;
        }

        .options label:hover {
            background: #f1f2f6;
        }

        textarea {
            width: 100%;
            padding: 10px;
            border-radius: 6px;
            border: 1px solid #ccc;
            box-sizing: border-box;
            margin-top: 8px;
            font-family: inherit;
            resize: vertical;
        }

        .btn-submit {
            display: block;
            width: 100%;
            background: var(--primary);
            color: white;
            font-size: 1.2em;
            font-weight: bold;
            padding: 15px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            margin-top: 20px;
            transition: background 0.2s;
        }

        .btn-submit:hover {
            background: #1c5980;
        }

        .result-box {
            display: none;
            margin-top: 30px;
            padding: 25px;
            border-radius: 10px;
            background: #f8f9fa;
            border: 2px solid #bdc3c7;
        }

        .score-header {
            text-align: center;
            font-size: 2.2em;
            font-weight: bold;
            margin: 15px 0;
        }

        .feedback-list {
            margin-top: 15px;
            padding-left: 20px;
            line-height: 1.6;
        }

        .feedback-list li {
            margin-bottom: 8px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Informatyka Klasa 4</h1>
    <p class="subtitle">Lekcja 2: Bezpieczni w cyfrowym świecie (Podręcznik str. 34–40)</p>

    <!-- Wybór Loginu Ucznia -->
    <div class="login-section">
        <label for="studentSelect"><strong>Wybierz Twój numer ucznia:</strong></label>
        <select id="studentSelect">
            <option value="">-- Wybierz kod --</option>
            <!-- Opcje A01-A28 generowane w JS -->
        </select>
    </div>

    <form id="quizForm">

        <!-- Zadanie 1 -->
        <div class="task-card">
            <span class="badge easy">Zadanie 1 (10%)</span>
            <h3>Co należy zrobić, gdy osoba poznana w sieci pyta o Twój adres, szkołę lub imię?</h3>
            <div class="options">
                <label><input type="radio" name="q1" value="A"> Podać te informacje, aby być uprzejmym.</label>
                <label><input type="radio" name="q1" value="B"> Nie odpowiadać na pytania i powiedzieć o tym zaufanemu dorosłemu.</label>
                <label><input type="radio" name="q2" value="C"> Wymienić się ze znajomym numerem telefonu.</label>
            </div>
        </div>

        <!-- Zadanie 2 -->
        <div class="task-card">
            <span class="badge easy">Zadanie 2 (10%)</span>
            <h3>Jak nazywamy niebezpieczne wiadomości e-mail lub SMS, których celem jest wyłudzenie danych logowania?</h3>
            <div class="options">
                <label><input type="radio" name="q2" value="A"> Wiadomości wyłudzające dane (phishing / oszustwo).</label>
                <label><input type="radio" name="q2" value="B"> Bezpieczne aktualizacje systemowe.</label>
                <label><input type="radio" name="q2" value="C"> Darmowe powiadomienia konkursowe.</label>
            </div>
        </div>

        <!-- Zadanie 3 -->
        <div class="task-card">
            <span class="badge easy">Zadanie 3 (10%)</span>
            <h3>Po czym najczęściej można rozpoznać podejrzaną wiadomość? (str. 35)</h3>
            <div class="options">
                <label><input type="radio" name="q3" value="A"> Jest wysłana przez kolegę z klasy z podpisem.</label>
                <label><input type="radio" name="q3" value="B"> Informuje o wygranej w konkursie, w którym nie brało się udziału, lub straszy blokadą konta.</label>
                <label><input type="radio" name="q3" value="C"> Zawiera tylko same życzenia urodzinowe.</label>
            </div>
        </div>

        <!-- Zadanie 4 -->
        <div class="task-card">
            <span class="badge medium">Zadanie 4 (10%)</span>
            <h3>Czym są fałszywe wiadomości określane jako "Fake news"? (str. 36)</h3>
            <div class="options">
                <label><input type="radio" name="q4" value="A"> To wyłącznie zabawne dowcipy przesyłane w wiadomościach prywatnych.</label>
                <label><input type="radio" name="q4" value="B"> To nieprawdziwe informacje przygotowane celowo, by wprowadzić w błąd lub wywołać emocje.</label>
                <label><input type="radio" name="q4" value="C"> To oficjalne komunikaty publikowane przez szkołę.</label>
            </div>
        </div>

        <!-- Zadanie 5 -->
        <div class="task-card">
            <span class="badge medium">Zadanie 5 (10%)</span>
            <h3>Co oznacza pojęcie "Deepfake"? (str. 36)</h3>
            <div class="options">
                <label><input type="radio" name="q5" value="A"> Bardzo trudna gra komputerowa wymagająca szybkiego pisania.</label>
                <label><input type="radio" name="q5" value="B"> Fałszywe, ale bardzo realistyczne zdjęcia, filmy lub nagrania głosu stworzone przez komputer.</label>
                <label><input type="radio" name="q5" value="C"> Szybkie połączenie z siecią Wi-Fi w szkole.</label>
            </div>
        </div>

        <!-- Zadanie 6 -->
        <div class="task-card">
            <span class="badge medium">Zadanie 6 (10%)</span>
            <h3>Jakie oznaczenie w adresie strony internetowej informuje, że połączenie jest szyfrowane? (str. 37)</h3>
            <div class="options">
                <label><input type="radio" name="q6" value="A"> Początek adresu https:// oraz ikona kłódki.</label>
                <label><input type="radio" name="q6" value="B"> Czerwony wykrzyknik przy pasku adresu.</label>
                <label><input type="radio" name="q6" value="C"> Napis "WWWW" przed nazwą strony.</label>
            </div>
        </div>

        <!-- Zadanie 7 -->
        <div class="task-card">
            <span class="badge medium">Zadanie 7 (10%)</span>
            <h3>Czym jest wirus komputerowy? (str. 37)</h3>
            <div class="options">
                <label><input type="radio" name="q7" value="A"> Przyjaznym programem ułatwiającym granie w sieci.</label>
                <label><input type="radio" name="q7" value="B"> Przykładem szkodliwego programu, który może zablokować komputer lub wykraść dane.</label>
                <label><input type="radio" name="q7" value="C"> Awarią monitora komputerowego.</label>
            </div>
        </div>

        <!-- Zadanie 8 -->
        <div class="task-card">
            <span class="badge hard">Zadanie 8 (10%)</span>
            <h3>Która z poniższych zasad dotyczy tworzenia silnego i bezpiecznego hasła? (str. 38)</h3>
            <div class="options">
                <label><input type="radio" name="q8" value="A"> Hasło powinno być krótkie, np. "12345", żeby go nie zapomnieć.</label>
                <label><input type="radio" name="q8" value="B"> Hasło powinno zawierać przynajmniej 14 znaków, małe i wielkie litery, cyfry oraz znaki specjalne.</label>
                <label><input type="radio" name="q8" value="C"> Jako hasło najlepiej podać swoje imię i rok urodzenia.</label>
            </div>
        </div>

        <!-- Zadanie 9 -->
        <div class="task-card">
            <span class="badge hard">Zadanie 9 (10%)</span>
            <h3>Dlaczego hasło "Magda1234" NIE JEST bezpiecznym hasłem? (Ćwiczenie 4, str. 39)</h3>
            <div class="options">
                <label><input type="radio" name="q9" value="A"> Ponieważ jest za długie do wpisania na telefonie.</label>
                <label><input type="radio" name="q9" value="B"> Ponieważ zawiera popularne imię oraz prostą sekwencję cyfr, przez co łatwo je odgadnąć.</label>
                <label><input type="radio" name="q9" value="C"> Ponieważ nie wolno używać wielkich liter w hasłach.</label>
            </div>
        </div>

        <!-- Zadanie 10 -->
        <div class="task-card">
            <span class="badge hard">Zadanie 10 (10%)</span>
            <h3>Gdzie możesz szukać pomocy lub zgłosić problem, gdy w sieci spotka Cię coś niepokojącego? (str. 39)</h3>
            <p>Opisz krótko (przynajmniej jednym zdaniem), do kogo się zwrócisz lub pod jaki numer zadzwonisz:</p>
            <textarea id="q10" rows="3" placeholder="Wpisz swoją odpowiedź (np. dorosły, telefon zaufania 116 111)..."></textarea>
        </div>

        <button type="button" class="btn-submit" onclick="gradeQuiz()">Prześlij rozwiązanie i sprawdź ocenę</button>
    </form>

    <!-- Wyniki -->
    <div id="resultBox" class="result-box">
        <h2 id="studentTitle" style="text-align: center; margin: 0;"></h2>
        <div id="scoreDisplay" class="score-header"></div>
        <hr style="border: none; border-top: 1px solid #ccc; margin: 20px 0;">
        <h3>Raport i zalecenia do powtórki z podręcznika:</h3>
        <ul id="feedbackList" class="feedback-list"></ul>
    </div>
</div>

<script>
    // Generowanie listy kont A01 - A28
    const select = document.getElementById('studentSelect');
    for (let i = 1; i <= 28; i++) {
        let num = i < 10 ? '0' + i : i;
        let code = 'A' + num;
        let opt = document.createElement('option');
        opt.value = code;
        opt.innerText = 'Uczeń ' + code;
        select.appendChild(opt);
    }

    // Klucz odpowiedzi połączony z tematami i stronami z podręcznika
    const questionsKey = {
        q1: { ans: 'B', topic: 'Bezpieczne kontakty w sieci i ochrona danych osobowych (str. 34)' },
        q2: { ans: 'A', topic: 'Wiadomości wyłudzające dane / Phishing (str. 35)' },
        q3: { ans: 'B', topic: 'Rozpoznawanie niebezpiecznych wiadomości (str. 35)' },
        q4: { ans: 'B', topic: 'Fałszywe informacje – Fake news (str. 36)' },
        q5: { ans: 'B', topic: 'Technologia Deepfake i modyfikacja multimediów (str. 36)' },
        q6: { ans: 'A', topic: 'Bezpieczne strony WWW i protokół HTTPS (str. 37)' },
        q7: { ans: 'B', topic: 'Szkodliwe oprogramowanie i wirusy komputerowe (str. 37)' },
        q8: { ans: 'B', topic: 'Zasady tworzenia silnego i bezpiecznego hasła (str. 38)' },
        q9: { ans: 'B', topic: 'Analiza błędów w słabych hasłach (str. 39)' }
    };

    function gradeQuiz() {
        const student = select.value;
        if (!student) {
            alert('Wybierz swój kod ucznia (A01–A28) przed przesłaniem zadań!');
            window.scrollTo({ top: 0, behavior: 'smooth' });
            return;
        }

        let score = 0;
        let weakTopics = [];

        // Ocena pytań 1-9 (po 10% każde)
        for (let q in questionsKey) {
            const selected = document.querySelector(`input[name="${q}"]:checked`);
            if (selected && selected.value === questionsKey[q].ans) {
                score += 10;
            } else {
                weakTopics.push(questionsKey[q].topic);
            }
        }

        // Ocena pytania 10 (10%) - automatyczna analiza słów kluczowych
        const q10Text = document.getElementById('q10').value.trim().toLowerCase();
        const keywords = ['rodzic', 'nauczyciel', 'dorosł', '116 111', '116111', '800 12 12 12', '800121212', 'telefon', 'policja', 'zgłoś', '800'];
        let q10Passed = keywords.some(key => q10Text.includes(key));

        if (q10Text.length >= 10 && q10Passed) {
            score += 10;
        } else {
            weakTopics.push('Reagowanie na zagrożenia i numery zaufania: 116 111 / 800 12 12 12 (str. 39)');
        }

        // Prezentacja wyników
        document.getElementById('studentTitle').innerText = `Karta Wyników – Uczeń ${student}`;
        const scoreDisplay = document.getElementById('scoreDisplay');
        scoreDisplay.innerText = `Wynik: ${score}% / 100%`;

        if (score >= 80) {
            scoreDisplay.style.color = '#2ecc71';
        } else if (score >= 50) {
            scoreDisplay.style.color = '#e67e22';
        } else {
            scoreDisplay.style.color = '#e74c3c';
        }

        const feedbackList = document.getElementById('feedbackList');
        feedbackList.innerHTML = '';

        if (weakTopics.length === 0) {
            let li = document.createElement('li');
            li.style.color = '#2ecc71';
            li.innerHTML = '<strong>Doskonale!</strong> Znasz wszystkie zasady bezpieczeństwa w sieci opisane w podręczniku!';
            feedbackList.appendChild(li);
        } else {
            let titleLi = document.createElement('li');
            titleLi.innerHTML = '<strong>Musisz jeszcze raz przeczytać i przeanalizować następujące tematy z podręcznika:</strong>';
            feedbackList.appendChild(titleLi);

            weakTopics.forEach(topic => {
                let li = document.createElement('li');
                li.style.color = '#c0392b';
                li.innerText = '• ' + topic;
                feedbackList.appendChild(li);
            });
        }

        document.getElementById('resultBox').style.display = 'block';
        window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
    }
</script>

</body>
</html>
