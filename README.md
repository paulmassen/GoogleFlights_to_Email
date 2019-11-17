# ✈️ Google Flights to Email ✈️
A bookmarklet to display data from Google Flights, into a nicely formatted email.

## Why

This bookmarklet is useful for anyone who work with Flights, or who regularly needs to send flight informations via email.

## Installation
Just frag and drop the following link: [Copy Flight Info](javascript:void function(t){var e=function(t){"use strict";var e=function s(e){var i="",r="",a=t(".gws-flights-results__slice-selection");a.each(function(e){var s=new Date(t(this).find(".gws-flights-results__itinerary-times>.gws-flights-results__times-row>span.flt-subhead1").text()),a=t(this).find(".gws-flights-results__leg");a.each(function(e){var a=t(this).find(".gws-flights-results__other-leg-info>span:last").text().replace(/\s/g,""),l=t(this).find(".gws-flights-results__leg-flight>div:first").text(),n=t(this).find(".gws-flights-results__leg-duration>div:first>span").text().replace(/\s/g,""),g=t(this).find(".gws-flights-results__leg-departure>div:last>span:first").text(),d=t(this).find(".gws-flights-results__leg-departure").find(".gws-flights-results__iata-code").text(),f=t(this).find(".gws-flights-results__leg-departure").find(".gws-flights__offset-days").text();""==f%26%26(f=0);var o=new Date(s);o.setDate(s.getDate()+parseInt(f));var h=t(this).find(".gws-flights-results__leg-departure>div:first>span>span:first").text(),u=t(this).find(".gws-flights-results__leg-arrival>div:last>span:first").text(),c=t(this).find(".gws-flights-results__leg-arrival").find(".gws-flights-results__iata-code").text(),_=t(this).find(".gws-flights-results__leg-arrival").find(".gws-flights__offset-days").text();""==_%26%26(_=0);var p=new Date(s);p.setDate(s.getDate()+parseInt(_));var v=t(this).find(".gws-flights-results__leg-arrival>div:first>span>span:first").text(),w="";w=w+"*"+l+" "+a+"*(dur: "+n+")\r\n",w=w+"🛫 Departure "+g+" ("+d+") "+o.toLocaleDateString("fr-FR",{day:"2-digit",month:"short"})+" "+h+"\r\n",w=w+"🛬 Arrival "+u+" ("+c+") "+p.toLocaleDateString("fr-FR",{day:"2-digit",month:"short"})+" "+v+"\r\n";var m="";m=m+"<b>"+l+" "+a+"</b> (dur: "+n+")<br/>",m=m+"Departure "+g+" ("+d+") "+o.toLocaleDateString("fr-FR",{day:"2-digit",month:"short"})+" "+h+"<br/>",m=m+"Arrival "+u+" ("+c+") "+p.toLocaleDateString("fr-FR",{day:"2-digit",month:"short"})+" "+v+"<br/>",i=i+w+"\r\n",r=r+m+"<br/>"})}),document.removeEventListener("copy",s,!0),e.preventDefault();var l=e.clipboardData;l.clearData(),l.setData("text/plain",i),l.setData("text/html",r)};document.addEventListener("copy",e,!0),console.log("addevent listener added"),document.execCommand("copy")},s=t%26%26t.fn%26%26parseFloat(t.fn.jquery)>=1.7;if(s)e(t);else{var i=document.createElement("script");i.src="//ajax.googleapis.com/ajax/libs/jquery/1/jquery.js",i.onload=i.onreadystatechange=function(){var t=this.readyState;t%26%26"loaded"!==t%26%26"complete"!==t||e(jQuery.noConflict())}}document.getElementsByTagName("head")[0].appendChild(i)}(window.jQuery);)

## Example output

*Air France AF1641*(dur: 1h20m)

🛫 Departure Amsterdam Airport Schiphol (AMS) 05 déc. 13:55

🛬 Arrival Paris-Charles De Gaulle (CDG) 05 déc. 15:15


## Credit and Thanks
90% of code is imported from the original projet: https://github.com/gschaer/GoogleFlightsExport
Thanks to Guillaume Schaer. 
