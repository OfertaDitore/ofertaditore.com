---
layout: default
title: Oferta Ditore
---

# Mirë se vini

Na vizitoni cdo dite që të gjeni ofertat ditore më të mira nga Tannins dhe Partnerët tanë!

## Ofertat më të mira:

# Kërko ofertat:
<input type="text" id="offerSearch" placeholder="Search for offers...">


<div id="offersList">
{% for offer in site.data.offers %}
	<div class="offer-item">

	    <h3><a href="{{ offer.link }}">{{ offer.title }}</a></h3>
	    <img src="{{ offer.image }}" class='offer-img'/>
	    <!-- ![{{ offer.title }}]({{ offer.image }}){: .offer-img} -->
	    {{ offer.description }}
	</div>
{% endfor %}
</div>