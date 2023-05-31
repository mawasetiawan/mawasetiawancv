<!DOCTYPE html>
<html>
<head>
    <title>Iri Bilang Boss</title>
</head>
<body>
    <div id="player"></div>

    <script src="https://www.youtube.com/iframe_api"></script>
    <script>
        // Fungsi untuk memuat pemutar YouTube setelah API dimuat
        function onYouTubeIframeAPIReady() {
            // Membuat pemutar video YouTube
            var player = new YT.Player('player', {
                height: '360',
                width: '640',
                videoId: 'gmlRouWW0vg', // ID video YouTube yang ingin diputar
                playerVars: {
                    autoplay: 1, // Memutar video secara otomatis
                    controls: 1 // Menampilkan kontrol pemutar
                }
            });
        }
    </script>
</body>
</html>
