---
layout: default
title: Oferta Ditore
---
<div class="d-flex justify-content-center">
	<h2>Na vizitoni cdo dite që të gjeni kompanitë me ofertat ditore më të mira nga Tannins dhe Partnerët tanë në Prishtina Mall!</h2>
</div>
<!-- <div class="d-flex justify-content-center">

<h3 class="align-center">Kërko kompani:</h3>
<input type="text" id="offerSearch" placeholder="Search for offers...">
</div> -->

<div id="offersList" class="row ">
{% for offer in site.data.offers %}
	<div class="col-xs-12 col-sm-12 col-md-4 col-lg-4 offer-item">
		<div class="card">
		  <img class="card-img-top" src="{{ offer.image }}" alt="Card image cap">
		  <div class="card-body">
		    <h5 class="card-title"><a target="_blank" href="{{ offer.link }}">{{ offer.title }}</a></h5>
		    <p class="card-text">{{ offer.description }}</p>
		    <a target="_blank" href="{{ offer.link }}" class="btn btn-primary">Vizito kompaninë</a>
		  </div>
		</div>
	</div> 
{% endfor %}
</div>