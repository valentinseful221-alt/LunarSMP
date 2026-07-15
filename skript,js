function copyIP() {
    navigator.clipboard.writeText("play.lunarsmp.ro");
    alert("IP copiat!\nplay.lunarsmp.ro");
}

async function loadServerStatus() {
    try {
        const response = await fetch("https://api.mcsrvstat.us/2/play.lunarsmp.ro");
        const data = await response.json();

        const players = document.getElementById("players");

        if (data.online) {
            players.innerHTML = `🟢 Online: ${data.players.online}/${data.players.max} jucători`;
        } else {
            players.innerHTML = "🔴 Server Offline";
        }
    } catch (e) {
        document.getElementById("players").innerHTML = "⚠️ Status indisponibil";
    }
}

loadServerStatus();
setInterval(loadServerStatus, 30000);
