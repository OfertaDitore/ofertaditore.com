<!DOCTYPE html>
<html>
<head>
    <title>{{ page.title }}</title>
    <link rel="stylesheet" href="/assets/css/style.css">
</head>
<body>
    <header>
        <h1>Daily Offers</h1>
    </header>
    <main>
        {{ content }}
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