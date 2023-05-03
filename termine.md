---
layout: default
title: Termine
---

# Termine

**Hast du noch nie beim CoderDojo teilgenommnen, musst du dich für die Teilnahme an deinem ersten Termin anmelden. Wenn es dir gefällt und du wiederkommen möchtest, kannst du ohne weitere Anmeldung zu allen Terminen kommen.**

## ___Da der letzte Sonntag im Mai auf den Pfingstsonntag fällt, findet das CoderDojo ausnahmsweise eine Woche früher am 21. Mai statt.___

<p class="text-center"><a class="btn btn-material-luzern-blue" href="/anmeldung.html">Zur Anmeldung</a></p>

<table class="table" id="eventsTable">
	<thead>
		<tr>
			<th>Datum</th>
			<th>Zeit</th>
			<th>Ort</th>
		</tr>
	</thead>
	<tbody>
	</tbody>
</table>

<p class="loadingText">Die Termine werden geladen ...</p>

<script language="javascript">
	Date.prototype.addDays = function(days) {
		var dat = new Date(this.valueOf());
		dat.setDate(dat.getDate() + days);
		return dat;
	}
	var eventsTable = $("#eventsTable");


	$.get("https://www.googleapis.com/calendar/v3/calendars/coderdojo.luzern@gmail.com/events?key=AIzaSyDuL2gUksesWq33UDNoACL4mdyjQcsS6vk", function(data) {

		//Compare dates
		const comp = function(a, b){  new Date(a.start.dateTime || a.start.date).getTime() - new Date(b.start.dateTime || b.start.date).getTime(); };

		data.items.sort(comp).forEach(function(event) {
			var row = "";

			var dateStart = moment(new Date(event.start.dateTime));
			var dateEnd = moment(new Date(event.end.dateTime));

			row += "<tr>";
			row += "<td>" + dateStart.format("dddd, Do MMM YYYY") + "</td>";
			row += "<td>" + dateStart.format("H:mm") + " - " + dateEnd.format("H:mm") +"</td>";
			row += "<td>";

			if (event.location) {
				row += event.location;
			} else {
					row += "<a href=\"https://www.google.com/maps/place/bbv+Software+Services+AG/@47.0638419,8.3090783,17z/data=!3m1!4b1!4m5!3m4!1s0x0:0x67769a64439d9bad!8m2!3d47.0638419!4d8.311267\" target=\"_blank\">bbv Software Services AG</a>, 2. Stock, Blumenrain 10, 6002 Luzern";
			}
			row += "</td>";
			row += "</tr>";
			eventsTable.append(row);
		});

		$(".loadingText").hide();
	});
</script>
