<!DOCTYPE html>
<html>
<head>
    <title>{{ page.title }}</title>
    <link rel="stylesheet" href="/assets/css/style.css">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-4bw+/aepP/YC94hEpVNVgiZdgIC5+VKNBQNGCHeKRQN+PtmoHDEXuppvnDJzQIu9" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-HwwvtgBNo3bZJJLYd8oVXjrBZt8cqVSpeBNS5n7C8IVInixGAoxmnlMuBnhbgrkm" crossorigin="anonymous"></script>
</head>
<body>
    <header>
        <h1>Oferta nga kompanitë partnere të Tannins në Prishtina Mall</h1>
    </header>
    <main>
        <div>
        {{ content }}
        </div>

    </main>
    <footer>
        <p>© 2023 Daily Offers. All rights reserved.</p>
    </footer>

    <script>
    document.getElementById('offerSearch').addEventListener('input', function() {
        let searchTerm = this.value.toLowerCase();
        let offers = document.querySelectorAll('.offer-item');

        offers.forEach(function(offer) {
            let offerTitle = offer.querySelector('h3').textContent.toLowerCase();

            if (offerTitle.includes(searchTerm)) {
                offer.style.display = 'block';
            } else {
                offer.style.display = 'none';
            }
        });
    });
    </script>
</script>
</body>
</html>