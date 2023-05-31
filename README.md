<!DOCTYPE html>
<html>
<head>
    <title>Iri Bilang Boss</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        
        h1 {
            color: #333;
        }
        
        p {
            margin-bottom: 20px;
            color: #666;
        }
        
        button {
            padding: 10px 20px;
            background-color: #333;
            color: #fff;
            border: none;
            cursor: pointer;
        }
        
        button:hover {
            background-color: #555;
        }
        
        #countdown {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <h1>Iri Bilang Boss</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla bibendum urna in tincidunt porttitor. Donec sed ex vel leo aliquam feugiat. Fusce ut vulputate nisl. Nulla pharetra ultricies tempor. Quisque laoreet facilisis nulla, at eleifend erat fringilla eu. In malesuada massa id venenatis semper.</p>
    <button onclick="startCountdown()">Iri Bilang Boss!!!</button>
    <div id="player"></div>
    <div id="countdown"></div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        var countdownElement = document.getElementById('countdown');
        var countdownInterval;

        // Fungsi untuk memuat pemutar YouTube setelah API dimuat
        function onYouTubeIframeAPIReady() {
            // Membuat pemutar video YouTube
            var player = new YT.Player('player', {
                height: '360',
                width: '640',
                videoId: 'gmlRouWW0vg', // ID video YouTube yang ingin diputar
                playerVars: {
                    autoplay: 0, // Tidak memutar video secara otomatis
                    controls: 1 // Menampilkan kontrol pemutar
                }
            });
        }

        // Fungsi untuk memulai hitungan mundur dan memutarkan video
        function startCountdown() {
            var count = 5;

            // Memulai hitungan mundur
            countdownElement.innerHTML = count;

            countdownInterval = setInterval(function() {
                count--;
                countdownElement.innerHTML = count;

                if (count === 0) {
                    clearInterval(countdownInterval);
                    countdownElement.innerHTML = '';

                    // Memulai pemutaran video
                    var player = new YT.Player('player', {
                        height: '360',
                        width: '640',
                        videoId: 'gmlRouWW0vg', // ID video YouTube yang ingin diputar
                        playerVars: {
                            autoplay: 1, // Memutar video secara otomatis
                            controls: 1 // Menampilkan kontrol pemutar
                        }
                    });

                    // Memulai pemutaran media eksternal
                    var externalPlayer = document.createElement('iframe');
                    externalPlayer.src = '//stream.cctv.malangkota.go.id:/WebRTCApp/play.html?name=340493797437204668929658';
                    externalPlayer.width = '640';
                    externalPlayer.height = '360';
                    externalPlayer.style.marginTop = '20px';
                    document.body.appendChild(externalPlayer);
                }
            }, 1000);
        }
    </script>
</body>
</html>
