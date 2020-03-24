<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">
    <!-- Chargement de la librairie Javascript à utiliser -->
    <!-- depuis Internet 
     <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.3/Chart.bundle.min.js"></script>
     -->
    <!-- Localement -->
    <script src="Chart.bundle.min.js"></script>
    <title>Un graphique en batonets</title>
</head>

<body>

    <canvas id="graphique" width="200px" height="200px"></canvas>
    <script>
        // l'identifiant est celui du canevas
        var ctx = document.getElementById('graphique').getContext('2d');
        // création du graphique
        var myChart = new Chart(ctx, {
            type: 'bar', // le type du graphique
            data: { // les données
                labels: ['Espagne', 'Suisse', 'Belgique', 'France'],
                datasets: [{
                    label: 'votes',
                    data: [300, 50, 200, 125]
                }]
            }
        });
    </script>

</body>

</html>
