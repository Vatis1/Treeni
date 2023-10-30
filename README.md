<!DOCTYPE html>
<html>
<head>
    <title>Kuntosalin Seuranta</title>
</head>
<body>
    <h1>Kuntosalin Seuranta</h1>

    <h2>Maastaveto</h2>
    <input type="text" id="maastaveto-kilot" placeholder="Kilomäärä">
    <input type="text" id="maastaveto-toistot" placeholder="Toistomäärä">
    <input type="text" id="maastaveto-viikko" placeholder="Viikko">
    <button onclick="tallennaTiedot('maastaveto')">Tallenna</button>

    <h2>Pystypunnerrus</h2>
    <input type="text" id="pystypunnerrus-kilot" placeholder="Kilomäärä">
    <input type="text" id="pystypunnerrus-toistot" placeholder="Toistomäärä">
    <input type="text" id="pystypunnerrus-viikko" placeholder="Viikko">
    <button onclick="tallennaTiedot('pystypunnerrus')">Tallenna</button>

    <h2>Pull-up lisäpainolla</h2>
    <input type="text" id="pull-up-kilot" placeholder="Kilomäärä">
    <input type="text" id="pull-up-toistot" placeholder="Toistomäärä">
    <input type="text" id="pull-up-viikko" placeholder="Viikko">
    <button onclick="tallennaTiedot('pull-up')">Tallenna</button>

    <h2>Dippi lisäpainoilla</h2>
    <input type="text" id="dippi-kilot" placeholder="Kilomäärä">
    <input type="text" id="dippi-toistot" placeholder="Toistomäärä">
    <input type="text" id="dippi-viikko" placeholder="Viikko">
    <button onclick="tallennaTiedot('dippi')">Tallenna</button>

    <h2>Seuranta</h2>
    <div id="seuranta"></div>

    <script>
        function tallennaTiedot(liike) {
            const kilot = document.getElementById(liike + '-kilot').value;
            const toistot = document.getElementById(liike + '-toistot').value;
            const viikko = document.getElementById(liike + '-viikko').value;

            const tiedot = `Liike: ${liike}, Kilot: ${kilot}, Toistot: ${toistot}, Viikko: ${viikko}`;
            document.getElementById('seuranta').innerHTML += `<p>${tiedot}</p>`;
        }
    </script>
</body>
</html>
