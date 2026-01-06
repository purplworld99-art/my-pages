# my-pages
Moje strony 
<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<title>VIRUS.EXE</title>
<style>
    body {
        background: black;
        color: lime;
        font-family: monospace;
        margin: 0;
        padding: 20px;
    }
    .warning {
        font-size: 22px;
        color: red;
        animation: blink 0.5s infinite;
    }
    @keyframes blink {
        50% { opacity: 0; }
    }
    .log {
        margin-top: 20px;
        border: 1px solid lime;
        padding: 10px;
        height: 300px;
        overflow-y: auto;
    }
</style>
</head>
<body>

<div class="warning">⚠ SYSTEM ZAINFEKOWANY ⚠</div>
<div class="log" id="log"></div>

<script>
const log = document.getElementById("log");
const messages = [
    "Łączenie z serwerem...",
    "Skanowanie plików systemowych...",
    "Wykryto 12 zagrożeń",
    "Usuwanie zabezpieczeń...",
    "Kopiowanie danych...",
    "Błąd: dostęp odmówiony",
    "Próba ponowna...",
    "SYSTEM NIE ODPOWIADA",
    "ŻARTOWAŁEM. WYLUZUJ."
];

let i = 0;
setInterval(() => {
    if (i < messages.length) {
        log.innerHTML += "> " + messages[i] + "<br>";
        log.scrollTop = log.scrollHeight;
        i++;
    }
}, 1000);
</script>

</body>
</html>
